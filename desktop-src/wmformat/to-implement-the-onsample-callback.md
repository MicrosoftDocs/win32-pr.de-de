---
title: So implementieren Sie den onsample-Rückruf
description: So implementieren Sie den onsample-Rückruf
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), Implementieren von OnStatus-Rückruf
- ASF (Advanced Systems Format), Implementieren von OnStatus-Rückruf
- Advanced Systems Format (ASF), OnStatus-Rückruf
- ASF (Advanced Systems Format), OnStatus-Rückruf
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, Implementieren des OnStatus-Rückrufs
- OnStatus-Rückruf Methode, implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314513"
---
# <a name="to-implement-the-onsample-callback"></a>So implementieren Sie den onsample-Rückruf

Der asynchrone Reader stellt Beispiele für die steuernde Anwendung in der Präsentationszeit-Reihenfolge bereit, indem Aufrufe an die [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) -Rückruf Methode erfolgt. Wenn Sie eine Anwendung mit dem asynchronen Reader erstellen, müssen Sie **onsample** implementieren, um nicht komprimierte Beispiele zu behandeln. Funktionen oder Methoden, die zum Rendering von Inhalten erstellt werden, werden in der Regel innerhalb von " **onsample**" aufgerufen.

Die typische Implementierung des **onsample** -Rückrufs umfasst die folgenden Schritte.

1.  Rufen Sie den Speicherort und die Größe des Puffers ab, der das Beispiel enthält, indem Sie [**inssbuffer:: getbufferandlength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) für den als *psample* übergebenen Puffer aufrufen.
2.  Verzweigen Sie Ihre Logik abhängig von der Ausgabe Nummer. Die Ausgabe Nummer wird als *dwoutputnumber* an **onsample** übermittelt.
3.  Schließen Sie Renderinglogik für jede Ausgabe Nummer ein, die Sie unterstützen möchten. Wenn Sie Beispiele aus mehreren Ausgaben rendern, müssen Sie möglicherweise Ihr Rendering synchronisieren.

Anwendungen, die komprimierte Beispiele aus den ASF-Dateien bereitstellen, müssen die " [**iwmreadercallbackadvanced:: onstreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) "-Rückruf Methode implementieren. **Onstreamsample** funktioniert beinahe identisch mit **onsample**, mit der Ausnahme, dass es komprimierte Stichproben nach streamnummer anstelle von nicht komprimierten Beispielen nach Ausgabe Nummer empfängt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreadercallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**Iwmreadercallbackadvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Verwenden der Rückruf Methoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




