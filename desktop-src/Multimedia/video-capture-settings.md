---
title: Video Erfassungs Einstellungen
description: Video Erfassungs Einstellungen
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Captuprojektms-Struktur
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341637"
---
# <a name="video-capture-settings"></a>Video Erfassungs Einstellungen

Die [**captureparms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur enthält die Steuerelement Parameter für das Streaming von Videoaufnahmen. Diese Struktur steuert verschiedene Aspekte des Aufzeichnungsprozesses und ermöglicht Ihnen die Durchführung der folgenden Aufgaben:

-   Geben Sie die Frame Rate an.
-   Geben Sie die Anzahl der zugeordneten Video Puffer an.
-   Deaktivieren und aktivieren Sie die Audioerfassung.
-   Geben Sie das Zeitintervall für die Erfassung an.
-   Geben Sie an, ob während der Erfassung ein MCI-Gerät (VCR oder Videodisk) verwendet wird.
-   Tastatur-oder Maussteuerung zum Beenden des Streamings angeben.
-   Geben Sie den Typ des Videos an, das während der Erfassung angewendet wird.

Sie können die aktuellen Aufzeichnungs Einstellungen innerhalb der [**captuprojektms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur abrufen, indem Sie die [**\_ gatewaycap- \_ Setup Nachricht get \_ Sequence \_**](wm-cap-get-sequence-setup.md) (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) an ein Aufzeichnungs Fenster senden. Sie können eine oder mehrere aktuelle Aufzeichnungs Einstellungen festlegen, indem Sie die entsprechenden Member der **captuprojektstruktur** -Struktur aktualisieren und dann [**die \_ \_ \_ \_ Setup**](wm-cap-set-sequence-setup.md) Nachricht für die WM-Cap-Einrichtung (oder das " [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) "-Makro) und **captuprojektmappenelemente** an ein Aufzeichnungs Fenster senden.

 

 




