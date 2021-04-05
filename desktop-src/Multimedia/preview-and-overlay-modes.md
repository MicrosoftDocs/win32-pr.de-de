---
title: Vorschau-und Überlagerungs Modi
description: Vorschau-und Überlagerungs Modi
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW Meldung
- cappreview-Makro
- WM_CAP_SET_PREVIEWRATE Meldung
- cappreviewrate-Makro
- WM_CAP_SET_SCALE Meldung
- cappreviewscale-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947603"
---
# <a name="preview-and-overlay-modes"></a>Vorschau-und Überlagerungs Modi

Ein Erfassungs Treiber kann zwei Methoden zum Anzeigen eines eingehenden Videodaten Stroms implementieren: Vorschaumodus und Überlagerungs Modus. Wenn ein Aufzeichnungs Treiber beide Methoden implementiert, kann der Benutzer auswählen, welche Methode verwendet werden soll.

Der Vorschaumodus überträgt digitalisierte Frames von der Aufzeichnungs Hardware in den Systemspeicher und zeigt dann die digitalisierten Frames im Erfassungsfenster mithilfe von Funktionen der Graphics Device Interface (GDI) an. Anwendungen können die Vorschau Rate verringern, wenn das übergeordnete Fenster den Fokus verliert, und die Vorschau Rate erhöhen, wenn das übergeordnete Fenster den Fokus erhält. Durch diese Aktion wird die allgemeine Reaktionsfähigkeit des Systems verbessert, da der Vorschau Vorgang Prozessor intensiv ist.

Es gibt drei Nachrichten, um den Vorschauvorgang zu steuern.

-   Verwenden Sie die Vorschau Nachricht der [**WM- \_ Ober \_ \_ Grenze**](wm-cap-set-preview.md) , um den Vorschaumodus zu aktivieren oder zu deaktivieren, indem Sie das-(oder das [**cappreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) -Makro) an ein Aufzeichnungs Fenster senden
-   Verwenden Sie die " [**WM \_ Cap \_ Set \_ previewrate**](wm-cap-set-previewrate.md) "-Meldung (oder das " [**cappreviewrate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) "-Makro), um die Rate festzulegen, mit der Frames im Vorschaumodus angezeigt werden
-   Verwenden Sie die " [**WM \_ Cap \_ Set \_ Scale**](wm-cap-set-scale.md) "-Nachricht (oder das [**cappreviewscale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) -Makro), um die Skalierung des Vorschau Videos zu aktivieren oder zu deaktivieren.

Wenn Vorschau und Skalierung aktiviert sind, wird der erfasste Videoframe auf die Abmessungen des Aufzeichnungs Fensters gestreckt. Durch Aktivieren des Vorschaumodus wird der Überlagerungs Modus automatisch deaktiviert.

Der Überlagerungs Modus ist eine Hardware Funktion, die den Inhalt des Aufzeichnungs Puffers auf dem Monitor anzeigt, ohne CPU-Ressourcen zu verwenden. Sie können den Überlagerungs Modus aktivieren und deaktivieren, indem Sie die WM-Cap-über [**\_ \_ \_ Lagerungs**](wm-cap-set-overlay.md) Nachricht (oder das [**capoverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) -Makro) an ein Aufzeichnungs Fenster senden. Durch Aktivieren des Überlagerungs Modus wird der Vorschaumodus automatisch deaktiviert.

Sie können auch die Bild Lauf Position des Video Rahmens im Client Bereich des Aufzeichnungs Fensters für den Vorschaumodus oder den Überlagerungs Modus festlegen, indem Sie die WM-Cap-Abbild [**\_ \_ \_ scrollnachricht**](wm-cap-set-scroll.md) (oder das [**capsetscrollpos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) -Makro) an ein Erfassungsfenster senden.

 

 




