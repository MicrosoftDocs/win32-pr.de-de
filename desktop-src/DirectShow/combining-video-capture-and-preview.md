---
description: Kombinieren von Videoaufnahme und Vorschau
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Kombinieren von Videoaufnahme und Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1894e9431cbfa9e7bbbd0ef0bcec48021055350030b54ffd2f3e2729db81c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084325"
---
# <a name="combining-video-capture-and-preview"></a>Kombinieren von Videoaufnahme und Vorschau

In den vorherigen Abschnitten wird beschrieben, wie Videos in verschiedenen Dateiformaten erfasst werden. Im Abschnitt [Videovorschau](previewing-video.md) wird beschrieben, wie Sie einen Livevorschaugraphen erstellen. Viele Anwendungen müssen jedoch beides gleichzeitig durchführen. Um einen kombinierten Vorschau- und Dateischreibgraphen zu erstellen, führen Sie einfach zwei Aufrufe von [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)aus:


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



In diesem Code werden im Capture Graph Builder einige Details ausgeblendet:

-   Wenn der Erfassungsfilter über einen Vorschauanschluss oder einen Videoportanschluss sowie einen Aufnahmeanschluss verfügt, rendert die [**RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) einfach beide Stecknadeln, wie in der folgenden Abbildung dargestellt.

    ![Erfassungs- und Vorschaudiagramm](images/vidcap04.png)

-   Wenn der Filter nur über einen Erfassungspin verfügt, verwendet der Capture Graph Builder den [Smart Tee-Filter,](smart-tee-filter.md) um den Erfassungsstream aufzuteilen. Die folgende Abbildung zeigt das Diagramm mit einem Smart Tee.

    ![Erfassen und Anzeigen eines Diagramms mit Smart Tee-Filter](images/vidcap05.png)

Der Smart Tee-Filter verfügt über einen Erfassungspin und einen Vorschaupin. Es nimmt einen einzelnen Videostream aus dem Erfassungsfilter und teilt ihn in zwei Streams auf: einen für die Erfassung und einen für die Vorschau. Um den Durchsatz für den Erfassungspin beizubehalten, löscht der Vorschaupin Frames nach Bedarf. Aus den im Thema [DirectShow Video Capture Filters](directshow-video-capture-filters.md)erläuterten Gründen entfernt es auch die Zeitstempel aus jedem Beispiel, bevor es geliefert wird.

Obwohl Smart Tee den Stream teilt, werden die Videodaten nicht physisch dupliziert. Stattdessen werden benutzerdefinierte Medienbeispielobjekte verwendet, die die Puffer gemeinsam nutzen. Die Beispiele sind als "schreibgeschützt" gekennzeichnet, um sicherzustellen, dass Downstreamfilter nicht in die Daten schreiben.

Wenn Ihr Erfassungsdiagramm über ein Vorschaufenster verfügt, kann dies dazu führen, dass der Filter Graph Manager das gesamte Diagramm einschließlich des Erfassungsstreams beendet:

-   Sperren des Computers.
-   Drücken Sie STRG+ALT+DELETE auf einem Computer, der Mitglied einer Domäne ist.
-   Ausführen einer Direct3D-Vollbildanwendung, z. B. eines Spiels oder bildschirmschoner.
-   Wechseln von Monitoren oder Ändern der Anzeigeauflösung.
-   Ausführen eines Programms, das bewirkt, dass Windows ein Dialogfeld für die Benutzerkontensteuerung (User Account Control, UAC) anzeigt. (Windows Vista oder höher.)
-   Ausführen eines Vollbild-DOS-Fensters.

Jedes dieser Ereignisse kann die Aufzeichnungssitzung unterbrechen und möglicherweise zu Datenverlusten führen. (Dies geschieht intern: Der Videorenderer verliert die benötigten Direct3D- oder DirectDraw-Ressourcen. Beim Wiederherstellen dieser Ressourcen muss der Videorenderer erneut eine Verbindung mit dem Upstreamfilter herstellen, sodass der Filter Graph Manager das Diagramm beendet.)

Es gibt zwei mögliche Lösungen für dieses Problem:

-   Schließen Sie keinen Vorschaustream ein. Beachten Sie jedoch, dass die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) automatisch ein Vorschaufenster hinzufügt, wenn das Erfassungsgerät über einen Videoportanschluss verfügt. Weitere Informationen finden Sie [unter Videoport-Pins in File Capture](video-port-pins-in-file-capture.md).
-   Verwenden Sie die Streampuffer-Engine, um den Vorschaudatenstrom in einem anderen Prozess an ein Diagramm zu senden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



