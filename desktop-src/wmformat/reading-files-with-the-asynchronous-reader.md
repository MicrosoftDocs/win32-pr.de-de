---
title: Lesen von Dateien mit dem asynchronen Reader
description: Lesen von Dateien mit dem asynchronen Reader
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Medienformat-SDK, Lesen von Dateien
- Windows Medienformat-SDK, asynchrone Reader
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- asynchrone Reader,IWMReaderCallback-Schnittstelle
- IWMReaderCallback, asynchrone Reader
- asynchrone Reader,Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea24a8f09cff8fe3e4a1f1cfb383f5569e968200bbbe6f25f2c8f225b3c18f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084507"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Lesen von Dateien mit dem asynchronen Reader

Der asynchrone Reader liest den Inhalt aus ASF-Dateien mithilfe mehrerer Threads und asynchroner Aufrufe. Die vom asynchronen Reader unterstützten Features eignen sich gut für Anwendungen, die Inhalte für Endbenutzer rendern.

Die grundlegendsten Funktionen des Readerobjekts können in die folgenden Schritte aufgeschlüsselt werden. In diesen Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media Format SDK schreiben.

1.  Die Anwendung implementiert die [**IWMReaderCallback-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) um Nachrichten vom Reader zu verarbeiten. Dies umfasst zwei Rückrufmethoden: **OnStatus**, das Nachrichten empfängt, die sich auf den Status verschiedener Aspekte des Readers bezieht, und **OnSample**, das unkomprimierte Beispiele vom Reader empfängt.
2.  Die Anwendung übergibt den Namen einer zu lesenden Datei an den Reader. Wenn der Reader die Datei öffnet, weist er jedem Stream eine Ausgabenummer zu. Wenn die Datei gegenseitigen Ausschluss verwendet, weist der Reader eine einzelne Ausgabe für alle sich gegenseitig ausschließenden Streams zu.
3.  Die Anwendung ruft Informationen zur Konfiguration der verschiedenen Ausgaben vom Reader ab. Die gesammelten Informationen ermöglichen der Anwendung das ordnungsgemäße Rendern von Medienbeispielen.
4.  Die Anwendung weist den Leser an, mit dem Lesen von Daten aus der Datei zu beginnen. Der Reader beginnt damit, unkomprimierte Beispiele in Puffern, die in Pufferobjekten umschlossen sind, nach und nach an den **OnSample-Rückruf** zu übertragen. Die vom Reader bereitgestellten Beispiele befinden sich in der Reihenfolge der Präsentationszeit. Der Reader wird weiterhin Stichproben bereitstellen, bis er von der Anwendung beendet wird oder bis das Ende der Datei erreicht ist.
5.  Die Anwendung ist für das Rendern von Daten verantwortlich, nachdem sie vom Reader übermittelt wurden. Das Windows Media Format SDK stellt keine Renderingroutinen bereit. In der Regel verwenden Anwendungen andere SDKs zum Rendern von Daten, z. B. das Microsoft DirectX® SDK oder die Multimediafunktionen des Microsoft Windows Platform SDK.
6.  Wenn das Lesen abgeschlossen ist, weist die Anwendung den Reader an, die Datei zu schließen.

Diese Schritte werden unter anderem in der AudioPlayer-Beispielanwendung veranschaulicht. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

Der Reader unterstützt auch erweiterte Funktionen. Der Reader ermöglicht Folgendes:

-   Anhalten der Wiedergabe einer Datei.
-   Abrufen von Readerleistungsstatistiken.
-   Steuern der Streamauswahl für sich gegenseitig ausschließende Streams.
-   Manuelles Zuordnen von Puffern für die Ausgabe.
-   Geben Sie Ihre eigene Uhr an.
-   Rufen Sie den Status von Dateivorgängen ab (Pufferung, Download oder Speichern).
-   Öffnen Sie eine Datei mithilfe der COM-Standardschnittstelle **IStream**.
-   Suchen Sie nach bestimmten Punkten in einer ASF-Datei.
-   Liest Profildaten aus dem Header der Datei.

In den folgenden Abschnitten wird die Verwendung des Readerobjekts ausführlich beschrieben.

-   [So implementieren Sie Readernachrichten im OnStatus-Rückruf](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [So implementieren Sie den OnSample-Rückruf](to-implement-the-onsample-callback.md)
-   [So erstellen Sie einen Reader und öffnen eine Datei](to-create-a-reader-and-open-a-file.md)
-   [So rufen Sie Medienbeispiele mit dem asynchronen Reader ab](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [So suchen Sie nach Zeit mithilfe des asynchronen Readers](to-seek-by-time-using-the-asynchronous-reader.md)
-   [So suchen Sie nach Framenummer mithilfe des asynchronen Readers](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [So suchen Sie mithilfe des asynchronen Readers nach SMPTE-Zeitcode](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [So suchen Sie nach Markern](to-seek-to-markers.md)
-   [So halten Sie die Wiedergabe an oder beenden sie](to-pause-or-stop-playback.md)
-   [So erhalten Sie Leseleistungsstatistiken](to-get-reader-performance-statistics.md)
-   [So verwenden Sie die manuelle Streamauswahl](to-use-manual-stream-selection.md)
-   [So stellen Sie komprimierte Beispiele mit dem asynchronen Reader zur Verfügung](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> </dl>

 

 




