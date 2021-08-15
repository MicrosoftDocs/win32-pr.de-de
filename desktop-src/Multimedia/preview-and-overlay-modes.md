---
title: Vorschau- und Überlagerungsmodi
description: Vorschau- und Überlagerungsmodi
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW Meldung
- capPreview-Makro
- WM_CAP_SET_PREVIEWRATE Meldung
- capPreviewRate-Makro
- WM_CAP_SET_SCALE Meldung
- capPreviewScale-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9359b1380c5d6efe049bc4bea52a08a92f880af5d35558f4e65e21070f20c0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372369"
---
# <a name="preview-and-overlay-modes"></a>Vorschau- und Überlagerungsmodi

Ein Erfassungstreiber kann zwei Methoden zum Anzeigen eines eingehenden Videostreams implementieren: den Vorschaumodus und den Überlagerungsmodus. Wenn ein Erfassungstreiber beide Methoden implementiert, kann der Benutzer auswählen, welche Methode verwendet werden soll.

Der Vorschaumodus überträgt digitalisierte Frames von der Erfassungshardware an den Systemspeicher und zeigt dann die digitalisierten Frames im Erfassungsfenster mithilfe von GDI-Funktionen (Graphics Device Interface) an. Anwendungen können die Vorschaurate verringern, wenn das übergeordnete Fenster den Fokus verliert, und die Vorschaurate erhöhen, wenn das übergeordnete Fenster den Fokus erhält. Diese Aktion verbessert die allgemeine Reaktionsfähigkeit des Systems, da der Vorschauvorgang prozessorintensiv ist.

Es gibt drei Meldungen, um den Vorschauvorgang zu steuern.

-   Verwenden Sie die [**WM \_ CAP SET \_ \_ PREVIEW-Meldung,**](wm-cap-set-preview.md) um den Vorschaumodus zu aktivieren oder zu deaktivieren, indem Sie (oder das [**CapPreview-Makro)**](/windows/desktop/api/Vfw/nf-vfw-cappreview) an ein Erfassungsfenster senden.
-   Verwenden Sie die [**WM \_ CAP SET \_ \_ PREVIEWRATE-Meldung**](wm-cap-set-previewrate.md) (oder das [**CapPreviewRate-Makro),**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) um die Rate festzulegen, mit der Frames im Vorschaumodus angezeigt werden.
-   Verwenden Sie die [**WM \_ CAP SET \_ \_ SCALE-Nachricht**](wm-cap-set-scale.md) (oder das [**CapPreviewScale-Makro),**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) um die Skalierung des Vorschauvideos zu aktivieren oder zu deaktivieren.

Wenn Vorschau und Skalierung aktiviert sind, wird der erfasste Videoframe auf die Dimensionen des Erfassungsfensters gestreckt. Durch aktivieren des Vorschaumodus wird der Überlagerungsmodus automatisch deaktiviert.

Der Überlagerungsmodus ist eine Hardwarefunktion, die den Inhalt des Erfassungspuffers auf dem Monitor anzeigt, ohne CPU-Ressourcen zu verwenden. Sie können den Überlagerungsmodus aktivieren und deaktivieren, indem Sie die [**WM \_ CAP SET \_ \_ OVERLAY-Nachricht**](wm-cap-set-overlay.md) (oder das [**capOverlay-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) an ein Erfassungsfenster senden. Durch aktivieren des Überlagerungsmodus wird der Vorschaumodus automatisch deaktiviert.

Sie können auch die Bildlaufposition des Videoframes im Clientbereich des Erfassungsfensters für den Vorschau- oder Überlagerungsmodus festlegen, indem Sie die [**WM \_ CAP SET \_ \_ SCROLL-Nachricht**](wm-cap-set-scroll.md) (oder das [**CapSetScrollPos-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) an ein Erfassungsfenster senden.

 

 




