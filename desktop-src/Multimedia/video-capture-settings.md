---
title: Video capture Einstellungen
description: Video capture Einstellungen
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- CAPTUREPARMS-Struktur
- WM_CAP_GET_SEQUENCE_SETUP Nachricht
- capCaptureGetSetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP-Nachricht
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50eb26170c8b1594d288cec903ef0c05867a24db2d5a89a6ad60f66eef4fd0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135588"
---
# <a name="video-capture-settings"></a>Video capture Einstellungen

Die [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) enthält die Steuerungsparameter für das Streaming von Videoaufnahmen. Diese Struktur steuert verschiedene Aspekte des Erfassungsprozesses und ermöglicht Ihnen die Ausführung der folgenden Aufgaben:

-   Geben Sie die Bildfrequenz an.
-   Geben Sie die Anzahl der zugeordneten Videopuffer an.
-   Deaktivieren und aktivieren Sie die Audioaufnahme.
-   Geben Sie das Zeitintervall für die Erfassung an.
-   Geben Sie an, ob ein MCI-Gerät (VCR oder videodisc) während der Erfassung verwendet wird.
-   Geben Sie das Tastatur- oder Maussteuersteuersystem zum Beenden des Streamings an.
-   Geben Sie den Typ der Videover mittelung an, die während der Erfassung angewendet wird.

Sie können die aktuellen Erfassungseinstellungen innerhalb der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) abrufen, indem Sie die [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder das [**CapCaptureGetSetup-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) an ein Erfassungsfenster senden. Sie können eine oder mehrere aktuelle Erfassungseinstellungen festlegen, indem Sie die entsprechenden Member der **CAPTUREPARMS-Struktur** aktualisieren und dann die [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder das [**capCaptureSetSetup-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) und **CAPTUREPARMS** an ein Erfassungsfenster senden.

 

 




