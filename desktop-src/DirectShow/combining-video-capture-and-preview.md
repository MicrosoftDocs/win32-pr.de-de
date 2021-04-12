---
description: Kombinieren von Video Erfassung und Vorschau
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Kombinieren von Video Erfassung und Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481174"
---
# <a name="combining-video-capture-and-preview"></a>Kombinieren von Video Erfassung und Vorschau

In den vorherigen Abschnitten wird beschrieben, wie Videos in verschiedenen Dateiformaten aufgezeichnet werden. Im Abschnitt [Vorschau Video](previewing-video.md) wird beschrieben, wie ein Live Vorschau Diagramm erstellt wird. Viele Anwendungen müssen jedoch beide gleichzeitig ausführen. Um ein kombiniertes Vorschau-und Datei Schreib Diagramm zu erstellen, führen Sie einfach zwei Aufrufe von [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)aus:


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



In diesem Code verbirgt der Erfassungs Diagramm-Generator einige Details:

-   Wenn der Erfassungs Filter eine Vorschau-PIN oder eine Videoport-PIN sowie eine Aufzeichnungs-Pin aufweist, rendert die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode einfach beide Pins, wie in der folgenden Abbildung dargestellt.

    ![Erfassungs-und Vorschau Diagramm](images/vidcap04.png)

-   Wenn der Filter nur über eine Erfassungs-Pin verfügt, verwendet der Erfassungs Diagramm-Generator den [Smart Tee](smart-tee-filter.md) -Filter, um den Erfassungsdaten Strom aufzuteilen. Die folgende Abbildung zeigt das Diagramm mit einem intelligenten Tee.

    ![Erfassung und Vorschau des Diagramms mit Smart Tee Filter](images/vidcap05.png)

Der Smart Tee-Filter verfügt über eine Erfassungs-PIN und eine Vorschau-PIN. Er nimmt einen einzelnen Videostream aus dem Erfassungs Filter und teilt ihn in zwei Streams auf: einen für die Erfassung und einen für die Vorschau. Um den Durchsatz auf der Erfassungs-Pin aufrechtzuerhalten, löscht die Vorschau-Pin Frames nach Bedarf. Außerdem werden die Zeitstempel aus den einzelnen Stichproben entfernt, bevor Sie bereitgestellt werden, aus den im Thema [DirectShow-Video Erfassungs Filtern](directshow-video-capture-filters.md)beschriebenen Gründen.

Obwohl der intelligente Tee den Stream teilt, werden die Videodaten nicht physisch dupliziert. Stattdessen werden benutzerdefinierte Medien Beispiel Objekte verwendet, die die Puffer gemeinsam verwenden. Die Beispiele sind als "schreibgeschützt" gekennzeichnet, um sicherzustellen, dass downstreamfilter nicht auf die Daten schreiben.

Wenn das Erfassungs Diagramm über ein Vorschaufenster verfügt, kann es passieren, dass der Filter Graph-Manager das gesamte Diagramm, einschließlich des Erfassungsdaten Stroms, beendet:

-   Sperren des Computers.
-   Drücken von STRG + ALT + ENTF auf einem Computer, der Mitglied einer Domäne ist.
-   Ausführen einer Vollbild-Direct3D-Anwendung, z. b. eines Spiels oder Bildschirmschoners.
-   Wechseln von Monitoren oder Ändern der Bildschirmauflösung.
-   Ausführen eines Programms, das dazu führt, dass Windows ein Dialogfeld für die Benutzerkontensteuerung (UAC) anzeigt. (Windows Vista oder höher)
-   Ausführen eines Vollbild-DOS-Fensters.

Diese Ereignisse können die Erfassungs Sitzung unterbrechen und möglicherweise zu Datenverlusten führen. (Dies geschieht intern: der Videorenderer verliert die Direct3D-oder DirectDraw-Ressourcen, die er benötigt. Beim Wiederherstellen dieser Ressourcen muss der Videorenderer erneut eine Verbindung mit dem upstreamfilter herstellen, wodurch der Filter Graph-Manager das Diagramm beendet.)

Es gibt zwei mögliche Lösungen für dieses Problem:

-   Schließen Sie keinen Vorschau Datenstrom ein. Beachten Sie jedoch, dass die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode automatisch ein Vorschaufenster hinzufügt, wenn das Erfassungsgerät über eine Videoport-Pin verfügt. Siehe [Video Port Pins in file Capture](video-port-pins-in-file-capture.md).
-   Verwenden Sie die streampufferengine, um den Vorschau Datenstrom in einem anderen Prozess an ein Diagramm zu senden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



