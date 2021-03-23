---
title: Bindung in DirectML
description: In directml bezieht sich Bindung auf die Anlage von Ressourcen an die Pipeline, die die GPU während der Initialisierung und Ausführung ihrer Machine Learning-Operatoren verwenden soll.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: a04bf0bcc63fff810604e3db72fe507cc10040f5
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104548686"
---
# <a name="binding-in-directml"></a>Bindung in DirectML

In directml bezieht sich *Bindung* auf die Anlage von Ressourcen an die Pipeline, die die GPU während der Initialisierung und Ausführung ihrer Machine Learning-Operatoren verwenden soll. Bei diesen Ressourcen kann es sich um Eingabe-und Ausgabe Tensoren handeln, z. b. um temporäre oder permanente Ressourcen, die der Operator benötigt.

In diesem Thema werden die konzeptionellen und prozeduralen Details der Bindung behandelt. Es wird empfohlen, dass Sie die Dokumentation für die von Ihnen aufzurufenden APIs auch vollständig lesen, einschließlich der Parameter und Hinweise.

## <a name="important-ideas-in-binding"></a>Wichtige Ideen in der Bindung

Die Liste der nachfolgenden Schritte enthält eine allgemeine Beschreibung der Aufgaben, die sich auf die Bindung beziehen. Sie müssen diese Schritte jedes Mal ausführen, wenn [Sie einen Verteiler](/windows/desktop/api/directml/nn-directml-idmldispatchable)ausführen &mdash; . ein Verteiler ist entweder ein Operator Initialisierer oder ein kompilierter Operator. Mit diesen Schritten werden wichtige Ideen, Strukturen und Methoden eingeführt, die an der directml-Bindung beteiligt sind.

In den nachfolgenden Abschnitten dieses Themas werden diese Bindungs Aufgaben ausführlicher erläutert und erläutert, und es werden anschauliche Code Ausschnitte aus dem [minimalen directml-Anwendungs](dml-min-app.md) Codebeispiel entnommen.

- Aufrufen von [**idmldispatchable:: getbindingproperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) für den Verteiler, um zu bestimmen, wie viele Deskriptoren benötigt werden, sowie die temporären/persistenten Ressourcenanforderungen.
- Erstellen Sie einen Direct3D 12-deskriptorheap, der für die Deskriptoren groß genug ist, und binden Sie ihn an die Pipeline.
- Rufen Sie [**idmldevice:: createbindingtable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) auf, um eine directml-Bindungs Tabelle zu erstellen, die die an die Pipeline gebundenen Ressourcen darstellt. Verwenden Sie die [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) -Struktur, um die Bindungs Tabelle zu beschreiben, einschließlich der Teilmenge der Deskriptoren, auf die Sie im deskriptorheap verweist.
- Erstellen Sie temporäre/persistente Ressourcen als Direct3D 12-Puffer Ressourcen, beschreiben Sie Sie mit [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) -und [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) Strukturen, und fügen Sie Sie der Bindungs Tabelle hinzu.
- Wenn der Verteiler ein kompilierter Operator ist, erstellen Sie einen Puffer mit tensorflow-Elementen als Direct3D 12-Puffer Ressource. Füllen Sie Sie auf, und laden Sie Sie hoch, beschreiben Sie Sie mit **DML_BUFFER_BINDING** -und **DML_BINDING_DESC** Strukturen, und fügen Sie Sie der Bindungs Tabelle hinzu.
- Übergeben Sie die Bindungs Tabelle als Parameter, wenn Sie [**idmlcommandrecorder:: recorddispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)aufrufen.

## <a name="retrieve-the-binding-properties-of-a-dispatchable"></a>Abrufen der Bindungseigenschaften eines verteilbaren Objekts

Die [**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties) Struktur beschreibt die Bindungs Anforderungen eines verteilbaren Operators (Operator Initialisierer oder kompilierter Operator). Zu diesen Bindungs bezogenen Eigenschaften zählen die Anzahl der Deskriptoren, die an den Verteiler gebunden werden sollen, sowie die Größe in Bytes für jede temporäre und/oder persistente Ressource, die benötigt wird.

> [!NOTE]
> Selbst bei mehreren Operatoren desselben Typs sollten Sie keine Annahmen darüber treffen, dass Sie die gleichen Bindungs Anforderungen haben. Fragen Sie die Bindungseigenschaften für jeden Initialisierer und Operator ab, den Sie erstellen.

Rufen Sie [**idmldispatchable:: getbindingproperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) auf, um eine **DML_BINDING_PROPERTIES** abzurufen.

```cppwinrt
winrt::com_ptr<::IDMLCompiledOperator> dmlCompiledOperator;
// Code to create and compile a DirectML operator goes here.

DML_BINDING_PROPERTIES executeDmlBindingProperties{
    dmlCompiledOperator->GetBindingProperties()
};

winrt::com_ptr<::IDMLOperatorInitializer> dmlOperatorInitializer;
// Code to create a DirectML operator initializer goes here.

DML_BINDING_PROPERTIES initializeDmlBindingProperties{
    dmlOperatorInitializer->GetBindingProperties()
};

UINT descriptorCount = ...
```

Der hier abzurufende `descriptorCount` Wert bestimmt die (minimale) Größe des deskriptorheaps und der Bindungs Tabelle, die Sie in den nächsten zwei Schritten erstellen.

**DML_BINDING_PROPERTIES** enthält auch ein-Element `TemporaryResourceSize` , das die minimale Größe der temporären Ressource in Bytes angibt, die an die Bindungs Tabelle für dieses dispatchbare Objekt gebunden werden muss. Der Wert 0 (null) bedeutet, dass eine temporäre Ressource nicht erforderlich ist.

Und ein- `PersistentResourceSize` Member, der die minimale Größe der persistenten Ressource in Bytes angibt, die an die Bindungs Tabelle für dieses dispatchbare Objekt gebunden werden muss. Der Wert 0 (null) bedeutet, dass eine persistente Ressource nicht erforderlich ist. Wenn eine persistente Ressource erforderlich ist, muss Sie während der Initialisierung eines kompilierten Operators (wo Sie als Ausgabe des operatorinitialisierers gebunden ist) und während der Ausführung angegeben werden. Weitere Informationen hierzu gibt es weiter unten in diesem Thema. Nur kompilierte Operatoren verfügen über persistente Ressourcen – operatorinitialisierer geben für diesen Member immer den Wert 0 zurück.

Wenn Sie **idmldispatchable:: getbindingproperties** für einen Operator Initialisierer sowohl vor als auch nach einem Aufrufen von [**idmloperatorinitializer:: Reset**](/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset)aufrufen, sind die beiden abgerufenen Bindungseigenschaften nicht garantiert identisch.

## <a name="describe-create-and-bind-a-descriptor-heap"></a>Beschreiben, erstellen und Binden eines deskriptorheaps

Im Hinblick auf Deskriptoren beginnt ihre Verantwortung mit dem deskriptorheap selbst und endet damit. Die directml selbst übernimmt das Erstellen und Verwalten der Deskriptoren in dem Heap, den Sie bereitstellen.

Verwenden Sie daher eine [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) Struktur, um einen Heap zu beschreiben, der groß genug für die Anzahl der Deskriptoren ist, die der Verteiler benötigt. Erstellen Sie diese dann mit [**ID3D12Device:: up-descriptorheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap). Und schließlich [**ID3D12GraphicsCommandList:: setdescriptorheaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) aufrufen, um den deskriptorheap an die Pipeline zu binden.

```cppwinrt
winrt::com_ptr<::ID3D12DescriptorHeap> d3D12DescriptorHeap;

D3D12_DESCRIPTOR_HEAP_DESC descriptorHeapDescription{};
descriptorHeapDescription.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
descriptorHeapDescription.NumDescriptors = descriptorCount;
descriptorHeapDescription.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;

winrt::check_hresult(
    d3D12Device->CreateDescriptorHeap(
        &descriptorHeapDescription,
        _uuidof(d3D12DescriptorHeap),
        d3D12DescriptorHeap.put_void()
    )
);

std::array<ID3D12DescriptorHeap*, 1> d3D12DescriptorHeaps{ d3D12DescriptorHeap.get() };
d3D12GraphicsCommandList->SetDescriptorHeaps(
    static_cast<UINT>(d3D12DescriptorHeaps.size()),
    d3D12DescriptorHeaps.data()
);
```

## <a name="describe-and-create-a-binding-table"></a>Beschreiben und Erstellen einer Bindungs Tabelle

Eine directml-Bindungs Tabelle stellt die Ressourcen dar, die Sie an die Pipeline binden, damit Sie von einem Verteiler verwendet werden können. Bei diesen Ressourcen kann es sich um Eingabe-und Ausgabe Tensoren (oder andere Parameter) für einen Operator handeln, oder es kann sich um verschiedene persistente und temporäre Ressourcen handeln, mit denen ein Verteiler arbeitet.

Verwenden Sie die [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) -Struktur, um die Bindungs Tabelle zu beschreiben, einschließlich des verteilbaren Objekts, für das die Bindungs Tabelle die Bindungen darstellt, und den Bereich der Deskriptoren (aus dem soeben erstellten deskriptorheap), auf den die Bindungs Tabelle verweisen soll (und in die die verzeichtml Deskriptoren schreiben kann). Der `descriptorCount` Wert (eine der Bindungseigenschaften, die wir im ersten Schritt abgerufen haben) teilt uns mit, welche Mindestgröße in den Deskriptoren für die Bindungs Tabelle ist, die für das dispatchbare Objekt erforderlich ist. Hier verwenden wir diesen Wert, um die maximale Anzahl von Deskriptoren anzugeben, die directml vom Beginn der bereitgestellten CPU-und GPU-Deskriptorhandles in den Heap schreiben darf.

Rufen Sie dann [**idmldevice:: deatebindingtable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) auf, um die directml-Bindungs Tabelle zu erstellen. In späteren Schritten fügen wir die Ressourcen zur Bindungs Tabelle hinzu, nachdem wir weitere Ressourcen für den Verteiler erstellt haben.

Anstatt eine **DML_BINDING_TABLE_DESC** an diesen-Befehl zu übergeben, können Sie übergeben `nullptr` , um eine leere Bindungs Tabelle anzugeben.

```cppwinrt
DML_BINDING_TABLE_DESC dmlBindingTableDesc{};
dmlBindingTableDesc.Dispatchable = dmlOperatorInitializer.get();
dmlBindingTableDesc.CPUDescriptorHandle = d3D12DescriptorHeap->GetCPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.GPUDescriptorHandle = d3D12DescriptorHeap->GetGPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.SizeInDescriptors = descriptorCount;

winrt::com_ptr<::IDMLBindingTable> dmlBindingTable;
winrt::check_hresult(
    dmlDevice->CreateBindingTable(
        &dmlBindingTableDesc,
        __uuidof(dmlBindingTable),
        dmlBindingTable.put_void()
    )
);
```

Die Reihenfolge, in der directml Deskriptoren in den Heap schreibt, ist nicht angegeben, sodass die Anwendung darauf achten muss, die von der Bindungs Tabelle umschließenen Deskriptoren nicht zu überschreiben. Die angegebenen CPU-und GPU-Deskriptorhandles können aus unterschiedlichen Heaps stammen, aber es liegt in der Verantwortung ihrer Anwendung, sicherzustellen, dass der gesamte Deskriptorbereich, auf den das CPU-Deskriptorhandle verweist, in den Bereich kopiert wird, auf den das GPU-Deskriptorhandle vor der Ausführung mithilfe dieser Bindungs Tabelle verweist. Der deskriptorheap, von dem die Handles bereitgestellt werden, muss den Typ **D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV** haben. Außerdem muss der Heap, auf den von verwiesen wird, `GPUDescriptorHandle` ein Shader-sichtbarer deskriptorheap sein.

Sie können eine Bindungs Tabelle zurücksetzen, um alle Ressourcen zu entfernen, die Sie hinzugefügt haben, und gleichzeitig eine beliebige Eigenschaft ändern, die Sie für die ursprüngliche **DML_BINDING_TABLE_DESC** festgelegt haben (um einen neuen Bereich von Deskriptoren zu umschließen oder Sie für einen anderen Verteiler zu verwenden). Nehmen Sie einfach die Änderungen an der Beschreibungs Struktur vor, und nennen Sie [**idmlbindingtable:: Reset**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-reset).

```cppwinrt
dmlBindingTableDesc.Dispatchable = pIDMLCompiledOperator.get();

winrt::check_hresult(
    pIDMLBindingTable->Reset(
        &dmlBindingTableDesc
    )
);
```

## <a name="describe-and-bind-any-temporarypersistent-resources"></a>Beschreiben und binden Sie temporäre/persistente Ressourcen.

Die **DML_BINDING_PROPERTIES** Struktur, die wir beim [Abrufen der Bindungseigenschaften](#retrieve-the-binding-properties-of-a-dispatchable) des dispatchbaren-Objekts aufgefüllt haben, enthält die Größe aller temporären und/oder permanenten Ressourcen, die der Verteiler benötigt, in Byte. Wenn eine dieser Größen ungleich NULL ist, erstellen Sie eine Direct3D 12-Puffer Ressource und fügen Sie der Bindungs Tabelle hinzu.

Im folgenden Codebeispiel wird eine temporäre Ressource ( `temporaryResourceSize` Bytes in Größe) für den Verteiler erstellt. Wir beschreiben, wie die Ressource gebunden werden soll, und dann fügen wir diese Bindung der Bindungs Tabelle hinzu.

Da wir eine einzelne Puffer Ressource binden, wird die Bindung mit einer [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) Struktur beschrieben. In dieser Struktur geben wir die Direct3D 12-Puffer Ressource (die Ressource muss über eine Dimensions [**D3D12_RESOURCE_DIMENSION_BUFFER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)verfügen) sowie eine Offset-und-Größe im Puffer an. Es ist auch möglich, eine Bindung für ein Array von Puffern (anstelle eines einzelnen Puffers) zu beschreiben, und die [**DML_BUFFER_ARRAY_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding) Struktur ist zu diesem Zweck vorhanden.

Um den Unterschied zwischen einer Puffer Bindung und einer Puffer Array Bindung zu abstrahieren, verwenden wir die  [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) Struktur. Sie können den- `Type` Member der- **DML_BINDING_DESC** entweder auf [**DML_BINDING_TYPE_BUFFER**](/windows/desktop/api/directml/ne-directml-dml_binding_type) oder **DML_BINDING_TYPE_BUFFER_ARRAY** festlegen. Sie können dann festlegen, dass der- `Desc` Member abhängig von entweder auf einen **DML_BUFFER_BINDING** oder auf einen **DML_BUFFER_ARRAY_BINDING** verweist `Type` .

Wir arbeiten mit der temporären Ressource in diesem Beispiel. daher fügen wir Sie der Bindungs Tabelle mit einem Aufrufen von [**idmlbindingtable:: bindtemporaryresource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource)hinzu.

```cppwinrt
D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
winrt::com_ptr<::ID3D12Resource> temporaryBuffer;

D3D12_RESOURCE_DESC temporaryBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(temporaryResourceSize) };
winrt::check_hresult(
    d3D12Device->CreateCommittedResource(
        &defaultHeapProperties,
        D3D12_HEAP_FLAG_NONE,
        &temporaryBufferDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        __uuidof(temporaryBuffer),
        temporaryBuffer.put_void()
    )
);

DML_BUFFER_BINDING bufferBinding{ temporaryBuffer.get(), 0, temporaryResourceSize };
DML_BINDING_DESC bindingDesc{ DML_BINDING_TYPE_BUFFER, &bufferBinding };
dmlBindingTable->BindTemporaryResource(&bindingDesc);
```

Bei einer temporären Ressource (falls erforderlich) handelt es sich um einen ungenügenden Speicher, der intern während der Ausführung des Operators verwendet wird, sodass Sie sich nicht mit dem Inhalt beschäftigen müssen. Und Sie müssen es auch nicht mehr tun, nachdem der-Befehl für [**idmlcommandrecorder:: recorddispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) auf der GPU abgeschlossen wurde. Dies bedeutet, dass Ihre Anwendung die temporäre Ressource in zwischen den sendet des kompilierten Operators freigeben oder überschreiben kann. Für den angegebenen Pufferbereich, der als temporäre Ressource gebunden werden soll, muss der Start Offset an [**DML_TEMPORARY_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md)ausgerichtet sein. Der Typ des Heaps, der dem Puffer zugrunde liegt, muss **D3D12_HEAP_TYPE_DEFAULT** werden.

Wenn der Verteiler eine Größe ungleich 0 (null) für seine langlebige persistente Ressource meldet, ist die Prozedur ein wenig anders. Erstellen Sie einen Puffer, und beschreiben Sie eine Bindung, die dem oben gezeigten Muster folgt. Fügen Sie Sie jedoch mithilfe eines Aufrufs von [**idmlbindingtable:: bindoutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs)zur Bindungs Tabelle Ihres Operator Initialisierers hinzu, da es sich um den Auftrag des Operator Initialisierers handelt, um die persistente Ressource zu initialisieren. Fügen Sie Sie dann der Bindungs Tabelle des kompilierten Operators hinzu, indem Sie [**idmlbindingtable:: bindpersistentresource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindpersistentresource)aufrufen. Weitere Informationen zu diesem Workflow finden Sie im Codebeispiel für die [minimale directml-Anwendung](dml-min-app.md) . Der Inhalt und die Lebensdauer der persistenten Ressource müssen beibehalten werden, solange der kompilierte Operator dies tut. Das heißt, wenn ein Operator eine persistente Ressource erfordert, muss die Anwendung diese während der Initialisierung bereitstellen und Sie dann auch für alle zukünftigen Ausführungen des Operators bereitstellen, ohne den Inhalt zu ändern. Die persistente Ressource wird in der Regel von directml verwendet, um Nachschlage Tabellen oder andere langlebige Daten zu speichern, die während der Initialisierung eines Operators berechnet und bei zukünftigen Ausführungen dieses Operators wieder verwendet werden. Für den angegebenen Pufferbereich, der als permanenter Puffer gebunden werden soll, muss der Start Offset an [**DML_PERSISTENT_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md)ausgerichtet sein. Der Typ des Heaps, der dem Puffer zugrunde liegt, muss **D3D12_HEAP_TYPE_DEFAULT** werden.

## <a name="describe-and-bind-any-tensors"></a>Alle Tensoren beschreiben und binden

Wenn Sie mit einem kompilierten Operator arbeiten (anstatt mit einem Operator Initialisierer), müssen Sie die Eingabe-und Ausgabe Ressourcen (für Tensoren und andere Parameter) an die Bindungs Tabelle des Operators binden. Die Anzahl der Bindungen muss genau mit der Anzahl der Eingaben des Operators übereinstimmen, einschließlich optionaler Tensoren. Die einzelnen Eingabe-und Ausgabe-Tensoren und andere Parameter, die ein Operator annimmt, sind im Thema für diesen Operator (z. b. [**DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_identity_operator_desc)) dokumentiert.

Eine tensorflow-Ressource ist ein Puffer, der die einzelnen Element Werte des Mandanten enthält. Sie können einen solchen Puffer mithilfe der regulären Direct3D 12-Techniken ([Hochladen von Ressourcen](/windows/desktop/direct3d12/uploading-resources) und [zurück Lesen von Daten über einen Puffer](/windows/desktop/direct3d12/readback-data-using-heaps)) in bzw. aus der GPU hochladen und zurück lesen. Weitere Informationen zu diesen Techniken finden Sie im Codebeispiel für die [minimale directml-Anwendung](dml-min-app.md) .

Beschreiben Sie schließlich die Eingabe-und Ausgabe Ressourcen Bindungen mit **DML_BUFFER_BINDING** -und **DML_BINDING_DESC** Strukturen, und fügen Sie Sie dann der Bindungs Tabelle des kompilierten Operators mit Aufrufen von [**idmlbindingtable:: bindinputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) und [**idmlbindingtable:: bindoutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs)hinzu. Wenn Sie eine **idmlbindingtable:: Bind \** _-Methode aufrufen, schreibt directml einen oder mehrere Deskriptoren in den Bereich der CPU-Deskriptoren.

```cppwinrt
DML_BUFFER_BINDING inputBufferBinding{ inputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC inputBindingDesc{ DML_BINDING_TYPE_BUFFER, &inputBufferBinding };
dmlBindingTable->BindInputs(1, &inputBindingDesc);

DML_BUFFER_BINDING outputBufferBinding{ outputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC outputBindingDesc{ DML_BINDING_TYPE_BUFFER, &outputBufferBinding };
dmlBindingTable->BindOutputs(1, &outputBindingDesc);
```

Einer der Schritte zum Erstellen eines directml-Operators (siehe [_ *idmldevice:: forateoperator* *](/windows/desktop/api/directml/nf-directml-idmldevice-createoperator)) besteht darin, eine oder mehrere [**DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) Strukturen zu deklarieren, um die tensorflow-Datenpuffer zu beschreiben, die der Operator annimmt und zurückgibt. Ebenso wie der Typ und die Größe des tensorflow-Puffers können Sie optional das [**DML_TENSOR_FLAG_OWNED_BY_DML**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags) -Flag angeben.

**DML_TENSOR_FLAG_OWNED_BY_DML** gibt an, dass die tensorflow-Daten von directml besessen und verwaltet werden sollen. Directml erstellt eine Kopie der tensorflow-Daten während der Initialisierung des Operators und speichert Sie in der persistenten Ressource. Dies ermöglicht es directml, die tensorflow-Daten in andere, effizientere Formulare umzuformatieren. Wenn dieses Flag festgelegt wird, kann die Leistung gesteigert werden, aber es ist in der Regel nur für Mandanten nützlich, deren Daten sich während der Lebensdauer des Operators (z. b. Gewichtungs Tensoren) nicht ändern. Das Flag kann nur für Eingabe Mandanten verwendet werden. Wenn das Flag für eine bestimmte tensorflow-Beschreibung festgelegt ist, muss der entsprechende tensorflow während der Initialisierung des Operators an die Bindungs Tabelle gebunden werden, nicht während der Ausführung (was zu einem Fehler führt). Das ist das Gegenteil des Standard Verhaltens (das Verhalten ohne das DML_TENSOR_FLAG_OWNED_BY_DML-Flag), bei dem der tensorflow während der Ausführung oder nicht während der Initialisierung gebunden werden soll. Wenn Sie die tensorflow-Daten für einen Operator Initialisierer bereitstellen, ist es zulässig, einen Upload anstelle eines Standard Heaps zu binden, da directml eine Kopie der Daten erstellt. In allen anderen Fällen müssen alle an directml gebundenen Ressourcen Standard Heap Ressourcen sein.

Weitere Informationen finden Sie unter [**idmlbindingtable:: bindinputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) und [**idmlbindingtable:: bindoutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs).

## <a name="execute-the-dispatchable"></a>Verteiler ausführen

Übergeben Sie die Bindungs Tabelle als Parameter, wenn Sie [**idmlcommandrecorder:: recorddispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)aufrufen.

Wenn Sie die Bindungs Tabelle während eines Aufrufes **idmlcommandrecorder:: recorddispatch** verwenden, bindet directml die entsprechenden GPU-Deskriptoren an die Pipeline. Die CPU-und GPU-Deskriptorhandles sind nicht erforderlich, um auf die gleichen Einträge in einem deskriptorheap zu verweisen. Allerdings ist es in der Verantwortung der Anwendung sicherzustellen, dass der gesamte Deskriptorbereich, auf den das CPU-Deskriptorhandle verweist, in den Bereich kopiert wird, auf den das GPU-Deskriptorhandle vor der Ausführung mithilfe dieser Bindungs Tabelle verweist.

```cppwinrt
winrt::com_ptr<::ID3D12GraphicsCommandList> d3D12GraphicsCommandList;
// Code to create a Direct3D 12 command list goes here.

winrt::com_ptr<::IDMLCommandRecorder> dmlCommandRecorder;
// Code to create a DirectML command recorder goes here.

dmlCommandRecorder->RecordDispatch(
    d3D12GraphicsCommandList.get(),
    dmlOperatorInitializer.get(),
    dmlBindingTable.get()
);
```

Schließen Sie abschließend die Direct3D 12-Befehlsliste, und übermitteln Sie Sie wie jede andere Befehlsliste zur Ausführung.

Vor der Ausführung von **recorddispatch** auf der GPU müssen Sie alle gebundenen Ressourcen in den **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** -Zustand oder einen Status, der implizit zu **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** herauf gestuft werden kann, z. b. **D3D12_RESOURCE_STATE_COMMON**, übertragen. Nachdem dieser Vorgang abgeschlossen ist, verbleiben die Ressourcen im **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** Status. Die einzige Ausnahme ist für das Hochladen von Heaps, die beim Ausführen eines Operator Initialisierers gebunden sind, und für eine oder mehrere Tensoren ist das **DML_TENSOR_FLAG_OWNED_BY_DML** -Flag festgelegt. In diesem Fall müssen sich alle für die Eingabe gebundenen uploadheaps im **D3D12_RESOURCE_STATE_GENERIC_READ** Zustand befinden und bleiben in diesem Zustand, wie für alle uploadheaps erforderlich. Wenn **DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE** beim Kompilieren des Operators nicht festgelegt wurde, müssen alle Bindungen für die Bindungs Tabelle festgelegt werden, bevor **recorddispatch** aufgerufen wird. andernfalls ist das Verhalten nicht definiert. Wenn ein Operator eine [späte Bindung](#optionally-specify-late-bound-operator-bindings)unterstützt, wird die Bindung von Ressourcen möglicherweise so lange verzögert, bis die Direct3D 12-Befehlsliste zur Ausführung an die Befehls Warteschlange gesendet wird.

**Recorddispatch** verhält sich logisch wie ein [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch). Daher sind ungeordnete Zuordnungen erforderlich, um eine korrekte Reihenfolge zu gewährleisten, wenn Daten Abhängigkeiten zwischen den Verteilungen bestehen. Diese Methode fügt keine UAV-Barrieren für Eingabe-und Ausgabe Ressourcen ein. Die Anwendung muss sicherstellen, dass die richtigen UAV-Barrieren für alle Eingaben durchgeführt werden, wenn Ihre Inhalte von einer upstreamverteilung abhängig sind, und für alle Ausgaben, wenn downstreamdispatches vorhanden sind, die von diesen Ausgaben abhängen.

## <a name="lifetime-and-synchronization-of-descriptors-and-binding-table"></a>Lebensdauer und Synchronisierung von Deskriptoren und Bindungs Tabellen

Ein gutes geistiges Modell der Bindung in directml besteht darin, dass die directml-Bindungs Tabelle im Hintergrund die von Ihnen bereitgestellten Deskriptoren im deskriptorheap erstellt und verwaltet. Daher gelten alle üblichen Direct3D 12-Regeln für die Synchronisierung des Zugriffs auf diesen Heap und seine Deskriptoren. Es ist Aufgabe Ihrer Anwendung, eine korrekte Synchronisierung zwischen der CPU-und GPU-Arbeit durchzuführen, die eine Bindungs Tabelle verwendet.

Eine Bindungs Tabelle kann einen Deskriptor nicht überschreiben, während der Deskriptor verwendet wird (z. b. durch einen vorherigen Frame). Wenn Sie also einen bereits gebundenen deskriptorheap wieder verwenden möchten (z. b. durch Aufrufen von BIND * für eine Bindungs Tabelle, die darauf verweist, oder indem Sie den deskriptorheap manuell überschreiben), sollten Sie warten, bis der Verteiler, der derzeit den deskriptorheap verwendet, auf der GPU ausgeführt wird. Eine Bindungs Tabelle behält keinen starken Verweis auf den deskriptorheap bei, in den Sie schreibt, sodass Sie den unterstützenden Shader-sichtbaren deskriptorheap erst freigeben dürfen, wenn alle arbeiten, die diese Bindungs Tabelle verwenden, die Ausführung auf der GPU abgeschlossen haben.

Während eine Bindungs Tabelle dagegen einen deskriptorheap angibt und verwaltet, *enthält* die Tabelle nicht selbst einen der Speicher. Sie können eine Bindungs Tabelle also jederzeit freigeben oder zurücksetzen, nachdem Sie [**idmlcommandrecorder:: recorddispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) aufgerufen haben (Sie müssen nicht warten, bis dieser Aufruf auf der GPU ausgeführt wird, solange die zugrunde liegenden Deskriptoren gültig bleiben).

Die Bindungs Tabelle behält keine starken Verweise auf Ressourcen bei, die mit der &mdash; Anwendung gebunden sind, und die Anwendung muss sicherstellen, dass Ressourcen nicht gelöscht werden, während die GPU noch verwendet wird. Außerdem ist eine Bindungs Tabelle nicht Thread sicher, dass &mdash; Ihre Anwendung keine Methoden für eine Bindungs Tabelle gleichzeitig aus verschiedenen Threads ohne Synchronisierung abrufen darf.

Beachten Sie, dass in jedem Fall die erneute Bindung nur erforderlich ist, wenn Sie ändern, welche Ressourcen gebunden werden. Wenn Sie die gebundenen Ressourcen nicht ändern müssen, können Sie eine Bindung beim Start durchlaufen und bei jedem Aufruf von **recorddispatch** dieselbe Bindungs Tabelle übergeben.

Stellen Sie zum Überarbeiten von Machine Learning-und renderingworkloads sicher, dass die Bindungs Tabellen jedes Frames auf Bereiche des deskriptorheaps verweisen, die nicht bereits auf der GPU verwendet werden.

## <a name="optionally-specify-late-bound-operator-bindings"></a>Optional fest gebundene Operator Bindungen angeben

Wenn Sie mit einem kompilierten Operator (nicht mit einem Operator Initialisierer) arbeiten, haben Sie die Möglichkeit, die späte Bindung für den Operator anzugeben. Ohne späte Bindung müssen Sie alle Bindungen in der Bindungs Tabelle festlegen, bevor Sie einen Operator in einer Befehlsliste aufzeichnen. Mit späterer Bindung können Sie Bindungen für Operatoren festlegen (oder ändern), die bereits in einer Befehlsliste aufgezeichnet wurden, bevor Sie an die Befehls Warteschlange übermittelt wurden.

Um die späte Bindung anzugeben, rufen Sie [**idmldevice:: compileoperator**](/windows/win32/api/directml/nf-directml-idmldevice-compileoperator) mit dem- `flags` Argument [**DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE**](/windows/desktop/api/directml/ne-directml-dml_execution_flags)auf.