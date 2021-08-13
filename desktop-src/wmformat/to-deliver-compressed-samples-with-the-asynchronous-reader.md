---
title: So stellen Sie komprimierte Beispiele mit dem asynchronen Reader zur Verfügung
description: So stellen Sie komprimierte Beispiele mit dem asynchronen Reader zur Verfügung
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), Bereitstellen komprimierter Beispiele
- ASF (Advanced Systems Format), Bereitstellen komprimierter Beispiele
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- Advanced Systems Format (ASF), komprimierte Beispiele
- ASF (Advanced Systems Format), komprimierte Beispiele
- asynchrone Reader,Bereitstellen komprimierter Beispiele
- asynchrone Reader,komprimierte Beispiele
- Komprimierte Beispiele, Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9199fb1deefdd3c7408bc9039639bd723b06c380c03d249c9c71a1d792c1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699930"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>So stellen Sie komprimierte Beispiele mit dem asynchronen Reader zur Verfügung

Der asynchrone Reader kann komprimierte Beispiele aus Streams in ASF-Dateien liefern. Anwendungen liefern in der Regel komprimierte Beispiele, wenn sie einen Stream aus einer Datei in eine andere kopieren. Es ist nicht ratsam, Daten erneut zu komprimieren, die aus einem komprimierten Datenstrom rekonstruiert wurden, da daten während des Codierungsprozesses verloren gehen. Digitale Medien, die mehr als einmal komprimiert wurden, verringern die Qualität deutlich.

Das Windows Media Format SDK stellt keine Methoden zum Decodieren von Daten bereit, nachdem sie aus einer ASF-Datei extrahiert wurden. Wenn Sie komprimierte Beispiele erhalten und diese später dekomprimieren möchten, müssen Sie dafür Ihren eigenen Code bereitstellen. Eine Möglichkeit, diese Einschränkung zu umgehen, besteht im Schreiben der komprimierten Beispiele in eine neue ASF-Datei und dem anschließenden erneuten Lesen in normale, unkomprimierte Beispiele.

Führen Sie die folgenden Schritte aus, um komprimierte Beispiele mit dem asynchronen Reader zu erhalten.

1.  Implementieren Sie [**den IWMReaderCallbackAdvanced::OnStreamSample-Rückruf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) Dieser Rückruf ist in der Funktion im Grunde identisch mit [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) mit der Ausnahme, dass er Stichproben nach Streamnummer liefert und die Beispiele weiterhin komprimiert sind.
2.  Rufen Sie vor beginn der Wiedergabe einen Zeiger auf die [**IWMReaderAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) des Readerobjekts ab, indem Sie **IWMReader::QueryInterface aufrufen.**
3.  Konfigurieren Sie den Reader so, dass komprimierte Beispiele für den gewünschten Stream übermittelt werden, indem [**Sie IWMReaderAdvanced::SetReceiveStreamSamples aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)
4.  Wiederholen Sie Schritt 3 für jeden Stream, für den eine komprimierte Beispielbereitstellung gewünscht ist.

> [!Note]  
> Bildstreams sind für die Übermittlung komprimierter Datenströme ungültig. Wenn Sie einen Bilddatenstrom aus einer Datei in eine andere kopieren, funktioniert er in der neuen Datei nicht. Um einen Bilddatenstrom aus einer Datei in eine Datei zu kopieren, rufen Sie die Bilddatenstrombeispiele nach Ausgabenummer ab und fügen sie in die neue Datei ein, als würde ein neuer Bilddatenstrom enthalten sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReaderCallbackAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




