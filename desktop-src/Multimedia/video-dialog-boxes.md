---
title: Dialogfelder "Video"
description: Dialogfelder "Video"
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE Meldung
- capDlgVideoSource-Makro
- WM_CAP_DLG_VIDEOFORMAT Meldung
- capDlgVideoFormat-Makro
- WM_CAP_DLG_VIDEODISPLAY Meldung
- capDlgVideoDisplay-Makro
- WM_CAP_DLG_VIDEOCOMPRESSION Meldung
- capDlgVideoCompression-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93674b8ed4e6f6ff594013cc27825aea601cc005fc082ca8a8954b661c1f4317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135558"
---
# <a name="video-dialog-boxes"></a>Dialogfelder "Video"

Jeder Erfassungstreiber kann bis zu vier Dialogfelder bereitstellen, um Aspekte der Videodigitalisierung und des Aufzeichnungsprozesses zu steuern und Komprimierungsattribute zu definieren, die zum Verringern der Größe der Videodaten verwendet werden. Der Inhalt dieser Dialogfelder wird vom Videoaufnahmetreiber definiert.

Das Dialogfeld Videoquelle steuert die Auswahl von Videoeingabekanälen und -parametern, die sich auf das Videobild auswirken, das im Framepuffer digitalisiert wird. Dieses Dialogfeld listet die Signaltypen auf, die die Videoquelle mit der Erfassungskarte verbinden (in der Regel SVHS und zusammengesetzte Eingaben) und stellt Steuerelemente zum Ändern von Farbton, Kontrast oder Sättigung bereit. Wenn das Dialogfeld von einem Videoaufnahmetreiber unterstützt wird, können Sie es mithilfe der [**WM \_ CAP \_ DLG \_ VIDEOSOURCE-Nachricht**](wm-cap-dlg-videosource.md) (oder des Makros [**capDlgVideoSource)**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) anzeigen und aktualisieren.

Das Dialogfeld Videoformat steuert die Auswahl der Dimension und Bildtiefe des digitalisierten Videorahmens sowie die Komprimierungsoptionen des aufgezeichneten Videos. Wenn das Dialogfeld von einem Videoaufnahmetreiber unterstützt wird, können Sie es mithilfe der [**WM \_ CAP \_ DLG \_ VIDEOFORMAT-Nachricht**](wm-cap-dlg-videoformat.md) (oder des Makros [**capDlgVideoFormat)**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) anzeigen und aktualisieren.

Das Dialogfeld Videoanzeige steuert die Darstellung des Videos auf dem Monitor während der Erfassung. Die Steuerelemente in diesem Dialogfeld haben keine Auswirkungen auf die digitalisierten Videodaten, können sich jedoch auf die Darstellung des digitalisierten Signals auswirken. Erfassungsgeräte, die Overlay unterstützen, können beispielsweise das Ändern von Farbton und Sättigung, Schlüsselfarbe oder Ausrichtung der Überlagerung ermöglichen. Wenn das Dialogfeld von einem Videoaufnahmetreiber unterstützt wird, können Sie es mithilfe der [**WM \_ CAP \_ DLG \_ VIDEODISPLAY-Meldung**](wm-cap-dlg-videodisplay.md) (oder des Makros [**capDlgVideoDisplay)**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) anzeigen und aktualisieren.

Im Dialogfeld Videokomprimierung werden die Attribute für die Videokomprimierung nach der Erfassung gesteuert. Wenn das Dialogfeld von einem Videoaufnahmetreiber unterstützt wird, können Sie es mithilfe der [**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION-Meldung**](wm-cap-dlg-videocompression.md) (oder des Makros [**capDlgVideoCompression)**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) anzeigen und aktualisieren.

 

 




