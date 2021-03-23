---
title: UAV-Barrieren und Ressourcen Zustands Barrieren in directml
description: Beschreibt die Richtigkeit der Vorteile von Barrieren und wie Sie in directml mit Ihnen arbeiten können.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 9bfc93d4fb28cff5d7d196287c6573e3e494d1d5
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548687"
---
# <a name="uav-barriers-and-resource-state-barriers-in-directml"></a>UAV-Barrieren und Ressourcen Zustands Barrieren in directml

## <a name="unordered-access-view-uav-barrier-requirements"></a>Anforderungen für die ungeordnete Zugriffs Ansicht (UAV)

### <a name="uav-barriers-in-direct3d-12"></a>UAV-Barrieren in Direct3D 12

In Direct3D 12 können angrenzende Compute-Shader innerhalb derselben Befehlsliste parallel auf der GPU ausgeführt werden, es sei denn, Sie sind mit einer dazwischen liegenden UAV-Barriere (unsortierter Zugriffs Ansicht) synchronisiert. Dies kann die Leistung verbessern, indem GPU-Hardware erhöht wird. Ohne eine UAV-Barriere kann die parallele Ausführung von zwei benachbarten Verteilungen jedoch standardmäßig eine Racebedingung verursachen, wenn eine Daten Abhängigkeit zwischen den beiden Verteilungen vorhanden ist. oder wenn beide sendet UAV-Schreibvorgänge in die gleichen Speicherbereiche durchführen.

Eine UAV-Barriere zwingt, dass alle zuvor gesendeten sendet den exktions Vorgang auf der GPU vollständig ausführen, bevor nachfolgende sendet beginnen können. UAV-Barrieren werden verwendet, um eine Synchronisierung zwischen den Verteilungen in derselben Befehlsliste durchführen, um Daten Rassen zu vermeiden. Sie können eine UAV-Barriere mithilfe der [ **ID3D12GraphicsCommandList:: resourcebarrier** -Methode](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)ausstellen.

### <a name="uav-barriers-in-directml"></a>UAV-Barrieren in der directml

In directml werden Operatoren auf eine Weise verteilt, die der Art und Weise ähnelt, wie Compute-Shader in Direct3D 12 gesendet werden. Das heißt, dass angrenzende Verteiler von Operatoren parallel auf der GPU ausgeführt werden dürfen, es sei denn, zwischen Ihnen besteht eine dazwischen liegende UAV-Barriere. Ein typisches Machine Learning-Modell enthält Daten Abhängigkeiten zwischen seinen Operatoren. Beispielsweise wird die Ausgabe eines Operators in die Eingabe eines anderen Operators einfließen. Daher ist es wichtig, dass Sie für die ordnungsgemäße Synchronisierung von Verteilungen UAV-Barrieren verwenden.

Directml garantiert, dass Sie nur die Eingabe-Tensoren liest (und nie in diese schreiben). Außerdem wird sichergestellt, dass keine Schreibvorgänge in einen Ausgabe Mandanten außerhalb des Bereichs des Members [**DML_BUFFER_TENSOR_DESC:: totaltensorsizeinbytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) des Tensors erstellt werden. Dies bedeutet, dass die Daten Abhängigkeiten zwischen Operatoren in der directml durch die Betrachtung der Eingabe-und Ausgabe Bindungen eines Operators übermittelt werden können.

Diese Garantien ermöglichen es Ihnen beispielsweise, zwei Operatoren zu verteilen, die denselben Bereich einer Ressource als Eingabe binden, ohne eine dazwischen liegende UAV-Barriere ausgeben zu müssen. Dies ist immer sicher, weil directml nie in Eingabe-Tensoren schreibt. Ein weiteres Beispiel ist die Bindung der Ausgabe Tensoren von zwei gleichzeitigen Operator Verteilungen an dieselbe Direct3D 12-Ressource (solange sich Ihre Mandanten nicht überlappen), da directml niemals außerhalb der Grenzen eines Mandanten schreibt (wie durch den **DML_BUFFER_TENSOR_DESC:: totaltensorsizeinbytes** von tensorflow definiert).

Da UAV-Barrieren eine Art der Synchronisierung sind, kann die unnötige Verwendung von UAV-Barrieren die Leistung beeinträchtigen. Daher ist es am besten, die Mindestanzahl von UAV-Barrieren zu verwenden, die für die ordnungsgemäße Synchronisierung der Verteiler in einer Befehlsliste erforderlich sind.

### <a name="example-1"></a>Beispiel 1

Im folgenden Beispiel wird die Ausgabe eines Operator Operators in eine relu-Aktivierung eingefügt, gefolgt von einer Batch Normalisierung.

```console
    CONVOLUTION (conv1)
         |
  ACTIVATION_RELU (relu1)
         |
BATCH_NORMALIZATION (batch1)
```

Da zwischen allen drei Operatoren eine Daten Abhängigkeit vorhanden ist, benötigen Sie eine UAV-Barriere zwischen den einzelnen aufeinander folgenden Dispatch-Informationen (siehe [**idmlcommandrecorder:: recorddispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)).

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
2. `d3d12CommandList->ResourceBarrier(`**UAV-Barriere**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`
4. `d3d12CommandList->ResourceBarrier(`**UAV-Barriere**`)`
5. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**batch1**`)`

### <a name="example-2"></a>Beispiel 2

```console
     MAX_POOLING (pool1)
        /    \
CONVOLUTION  CONVOLUTION
  (conv1)      (conv2)
        \    /
         JOIN (join1)
```

Hier wird die Ausgabe von Pooling in zwei konvolutionen eingefügt, deren Ausgaben dann mithilfe des Join-Operators miteinander verkettet werden. Zwischen und sowie zwischen und sowie zwischen und und sind eine Daten Abhängigkeit vorhanden `pool1` `conv1` `conv2` `conv1` `conv2` `join1` . Im folgenden finden Sie eine gültige Methode zum Ausführen dieses Diagramms.

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`
2. `d3d12CommandList->ResourceBarrier(`**UAV-Barriere**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
4. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv2**`)`
5. `d3d12CommandList->ResourceBarrier(`**UAV-Barriere**`)`
6. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**join1**`)`

In diesem Fall `conv1` können und `conv2` gleichzeitig auf der GPU ausgeführt werden, wodurch die Leistung verbessert werden kann.

## <a name="resource-barrier-state-requirements"></a>Anforderungen an den Ressourcen Sperr Status

Als Aufrufer müssen Sie sicherstellen, dass sich alle Direct3D 12-Ressourcen im richtigen ressourcensperrungs-Zustand befinden, bevor directml-Verteiler auf der GPU ausgeführt werden. Directml führt keine Übergangs Barrieren in Ihrem Namen aus.

Vor der Ausführung von [**idmlcommandrecorder:: recorddispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) auf der GPU müssen Sie alle gebundenen Ressourcen in den **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** -Zustand oder einen Status, der implizit zu **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** herauf gestuft werden kann, z. b. **D3D12_RESOURCE_STATE_COMMON**, übertragen. Nachdem dieser Vorgang abgeschlossen ist, verbleiben die Ressourcen im **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** Status. Weitere Informationen finden Sie unter [binden in directml](dml-binding.md).

## <a name="see-also"></a>Siehe auch

* [Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
* [Bindung in DirectML](dml-binding.md)
