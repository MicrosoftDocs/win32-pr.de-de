---
title: Video Dialogfelder
description: Video Dialogfelder
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE Meldung
- capdlgvideosource-Makro
- WM_CAP_DLG_VIDEOFORMAT Meldung
- capdlgvideoformat-Makro
- WM_CAP_DLG_VIDEODISPLAY Meldung
- capdlgvideodisplay-Makro
- WM_CAP_DLG_VIDEOCOMPRESSION Meldung
- capdlgvideocompression-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339797"
---
# <a name="video-dialog-boxes"></a>Video Dialogfelder

Jeder Aufzeichnungs Treiber kann bis zu vier Dialogfelder bereitstellen, um Aspekte der Video Digitalisierung und des Aufzeichnungs Vorgangs zu steuern und Komprimierungs Attribute zu definieren, die zum Verringern der Größe der Videodaten verwendet werden. Der Inhalt dieser Dialogfelder wird vom Video Erfassungs Treiber definiert.

Im Dialogfeld Videoquelle wird die Auswahl von Videoeingabe Kanälen und-Parametern gesteuert, die sich auf das im Frame Puffer zu Digitalisier Ende Video Bild auswirken. In diesem Dialogfeld werden die Signaltypen aufgelistet, die die Videoquelle mit der aufzeichnungskarte verbinden (in der Regel SVHS und zusammengesetzte Eingaben) und Steuerelemente bereitstellen, um Farbton, Kontrast oder Sättigung zu ändern. Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mithilfe der WM- [**\_ Cap- \_ DLG- \_ videosource**](wm-cap-dlg-videosource.md) -Nachricht (oder des " [**capdlgvideosource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) "-Makros) anzeigen und aktualisieren.

Im Dialogfeld Video Format wird die Auswahl der digitalisierten Video Frame Dimensionen und der Bild-und Komprimierungs Optionen des aufgezeichneten Videos gesteuert. Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mit der Meldung " [**WM \_ Cap \_ DLG \_ Videoformat**](wm-cap-dlg-videoformat.md) " (oder dem Makro " [**capdlgvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ") anzeigen und aktualisieren.

Im Dialogfeld Videoanzeige wird die Darstellung des Videos auf dem Monitor während der Erfassung gesteuert. Die Steuerelemente in diesem Dialogfeld wirken sich nicht auf die digitalisierten Videodaten aus, Sie können sich jedoch auf die Darstellung des digitalisierten Signals auswirken. Beispielsweise können Erfassungsgeräte, die Overlay unterstützen, das Ändern von Farbton, Sättigung, Schlüsselfarbe oder Ausrichtung der Überlagerung ermöglichen. Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mithilfe der WM- [**\_ Cap- \_ DLG- \_ Videodisplay**](wm-cap-dlg-videodisplay.md) -Nachricht (oder des " [**capdlgvideodisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) "-Makros) anzeigen und aktualisieren.

Im Dialogfeld Video Komprimierung werden die Attribute für die Video Komprimierung nach der Erfassung gesteuert. Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mithilfe der WM- [**\_ Cap- \_ DLG- \_ Video Komprimierungs**](wm-cap-dlg-videocompression.md) Nachricht (oder mit dem [**capdlgvideocompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) -Makro) anzeigen und aktualisieren.

 

 




