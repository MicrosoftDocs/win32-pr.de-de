---
title: So implementieren Sie den OnSample-Rückruf
description: So implementieren Sie den OnSample-Rückruf
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), Implementieren des OnStatus-Rückrufs
- ASF (Advanced Systems Format),Implementieren des OnStatus-Rückrufs
- Advanced Systems Format (ASF), OnStatus-Rückruf
- ASF (Advanced Systems Format), OnStatus-Rückruf
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- asynchrone Reader, Implementieren des OnStatus-Rückrufs
- OnStatus-Rückrufmethode, Implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00523ae28ec14feefb8249ff86a2b1600629c84cb245eb627b59b619a28a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027288"
---
# <a name="to-implement-the-onsample-callback"></a>So implementieren Sie den OnSample-Rückruf

Der asynchrone Reader übermittelt Beispiele in der Reihenfolge der Präsentationszeit an die steuernde Anwendung, indem er Aufrufe der [**Rückrufmethode IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) vornimmt. Wenn Sie eine Anwendung mit dem asynchronen Reader erstellen, müssen Sie **OnSample** implementieren, um nicht komprimierte Beispiele zu behandeln. In der Regel werden Funktionen oder Methoden, die zum Rendern von Inhalten erstellt wurden, in **OnSample** aufgerufen.

Die typische Implementierung des **OnSample-Rückrufs** umfasst die folgenden Schritte.

1.  Rufen Sie die Position und Größe des Puffers ab, der das Beispiel enthält, indem [**Sie INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) für den Puffer aufrufen, der als *pSample* übergeben wird.
2.  Verzweigen Sie Ihre Logik abhängig von der Ausgabenummer. Die Ausgabenummer wird als *dwOutputNumber* an **OnSample** übergeben.
3.  Fügen Sie Renderinglogik für jede Ausgabenummer ein, die Sie unterstützen möchten. Wenn Sie Beispiele aus mehreren Ausgaben rendern, müssen Sie das Rendering möglicherweise synchronisieren.

Anwendungen, die komprimierte Beispiele aus ASF-Dateien bereitstellen, müssen die [**Rückrufmethode IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) implementieren. **OnStreamSample** funktioniert fast identisch mit **OnSample,** mit der Ausnahme, dass komprimierte Stichproben nach Streamnummer anstelle von unkomprimierten Stichproben nach Ausgabenummer empfangen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReaderCallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**IWMReaderCallbackErweiterte Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Verwenden der Rückrufmethoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




