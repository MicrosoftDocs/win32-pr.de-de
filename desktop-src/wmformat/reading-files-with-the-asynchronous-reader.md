---
title: Lesen von Dateien mit dem asynchronen Reader
description: Lesen von Dateien mit dem asynchronen Reader
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media-Format-SDK, Lesen von Dateien
- SDK für den Windows Media-Format, asynchrone Leser
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- asynchrone Reader, iwmreadercallback-Schnittstelle
- Iwmreadercallback, asynchrone Reader
- asynchrone Leser, Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389851"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Lesen von Dateien mit dem asynchronen Reader

Der asynchrone Reader liest den Inhalt aus den ASF-Dateien mit mehreren Threads und asynchronen Aufrufen. Die Funktionen, die vom asynchronen Reader unterstützt werden, eignen sich gut für Anwendungen, die Inhalte für Endbenutzer darstellen.

Die grundlegende Funktionalität des Reader-Objekts kann in die folgenden Schritte aufgeteilt werden. In den folgenden Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media-Format-SDK schreiben.

1.  Die Anwendung implementiert die [**iwmreadercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) -Schnittstelle zum Verarbeiten von Nachrichten vom Reader. Dies schließt zwei Rückruf Methoden ein: **OnStatus**, das Nachrichten im Zusammenhang mit dem Status verschiedener Aspekte von Reader und **onsample** empfängt, die nicht komprimierte Beispiele vom Reader empfangen.
2.  Die Anwendung übergibt an den Reader den Namen einer zu lesenden Datei. Wenn der Reader die Datei öffnet, wird jedem Stream eine Ausgabe Nummer zugewiesen. Wenn die Datei einen gegenseitigen Ausschluss verwendet, weist der Reader eine einzelne Ausgabe für alle sich gegenseitig ausschließenden Streams zu.
3.  Die Anwendung ruft Informationen zur Konfiguration der verschiedenen Ausgaben des Readers ab. Die gesammelten Informationen ermöglichen der Anwendung das ordnungsgemäße Rendering von Medien Beispielen.
4.  Die Anwendung weist den Reader an, mit dem Lesen von Daten aus der Datei zu beginnen. Der Reader beginnt mit der Bereitstellung von nicht komprimierten Beispielen für den **onsample** -Rückruf nacheinander in Puffern, die in Puffer Objekten eingebunden sind. Die vom Reader gelieferten Beispiele sind in der Präsentationszeit sortiert. Der Reader liefert weiterhin Beispiele, bis die Anwendung beendet wird oder bis das Ende der Datei erreicht ist.
5.  Die Anwendung ist für das Rendern von Daten verantwortlich, nachdem Sie vom Reader zugestellt wurde. Das Windows Media-Format-SDK stellt keine renderingroutinen bereit. In der Regel verwenden Anwendungen andere SDKs zum Rendering von Daten, wie z. b. das Microsoft DirectX® SDK oder die Multimedia-Funktionen des Microsoft Windows Platform SDK.
6.  Wenn der Lesevorgang abgeschlossen ist, weist die Anwendung den Reader an, die Datei zu schließen.

Diese Schritte werden unter anderem in der Audioplayer-Beispielanwendung veranschaulicht. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

Der Reader unterstützt auch erweiterte Funktionen. Der Reader ermöglicht Ihnen Folgendes:

-   Hält die Wiedergabe einer Datei an.
-   Abrufen von Leistungsstatistiken für Reader.
-   Steuern der Streamauswahl für sich gegenseitig ausschließende Streams.
-   Puffer für Ausgabe manuell zuordnen.
-   Geben Sie eine eigene Uhr an.
-   Abrufen des Status von Datei Vorgängen (Pufferung, herunterladen oder speichern).
-   Öffnen Sie eine Datei mit der Standard-COM-Schnittstelle **IStream**.
-   Suchen Sie nach bestimmten Punkten in einer ASF-Datei.
-   Liest Profildaten aus dem Header der Datei.

In den folgenden Abschnitten wird die Verwendung des Reader-Objekts ausführlich beschrieben.

-   [So implementieren Sie readernachrichten im OnStatus-Rückruf](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [So implementieren Sie den onsample-Rückruf](to-implement-the-onsample-callback.md)
-   [So erstellen Sie einen Reader und öffnen eine Datei](to-create-a-reader-and-open-a-file.md)
-   [So rufen Sie Medien Beispiele mit dem asynchronen Reader ab](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [So suchen Sie nach Zeit mithilfe des asynchronen Readers](to-seek-by-time-using-the-asynchronous-reader.md)
-   [So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [So suchen Sie Marker](to-seek-to-markers.md)
-   [Anhalten oder Anhalten der Wiedergabe](to-pause-or-stop-playback.md)
-   [So erhalten Sie Leistungsstatistiken für Leser](to-get-reader-performance-statistics.md)
-   [So verwenden Sie die manuelle Datenstrom Auswahl](to-use-manual-stream-selection.md)
-   [So liefern Sie komprimierte Beispiele mit dem asynchronen Reader](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> </dl>

 

 




