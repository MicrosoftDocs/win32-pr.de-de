---
title: Desktopfenster-Manager
description: Das in Windows Vista eingeführte Feature "Desktop Komposition" hat grundlegend geändert, wie Anwendungen auf dem Bildschirm Pixel anzeigen.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Desktopfenster-Manager (DWM), Informationen zu
- Dwm (Desktopfenster-Manager), Informationen zu
- Desktopfenster-Manager (DWM), Komposition
- Dwm (Desktopfenster-Manager), Komposition
- Desktop Komposition
- Komposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711190"
---
# <a name="desktop-window-manager"></a>Desktopfenster-Manager

Das in Windows Vista eingeführte Feature "Desktop Komposition" hat grundlegend geändert, wie Anwendungen auf dem Bildschirm Pixel anzeigen. Wenn die Desktop Komposition aktiviert ist, werden einzelne Fenster nicht mehr direkt auf den Bildschirm oder das primäre Anzeigegerät gezeichnet, wie dies in früheren Versionen von Windows der Fall war. Stattdessen wird die Zeichenfolge in den Videospeicher, der in einem Desktop Bild gerendert und auf der Anzeige angezeigt wird, zu den Bildschirm Oberflächen umgeleitet.

Die Desktop Komposition wird vom Desktopfenster-Manager (DWM) ausgeführt. Durch die Desktop Komposition ermöglicht DWM visuelle Effekte auf dem Desktop sowie verschiedene Funktionen wie z. b. Glasfenster Rahmen, 3-D-Fenster Übergangs Animationen, Windows Flip-und Windows Flip3D-Unterstützung und Unterstützung für hohe Auflösung.

Der Desktopfenster-Manager wird als Windows-Dienst ausgeführt. Sie kann über das System Steuerungselement "Verwaltung" unter "Dienste" als Desktopfenster-Manager Sitzungs-Manager aktiviert und deaktiviert werden.

Viele der DWM-Features können über die DWM-APIs gesteuert oder von einer Anwendung aufgerufen werden. In der folgenden Dokumentation werden die Features und Anforderungen der DWM-APIs beschrieben.

-   [DWM-Übersichten](desktop-window-manager-overviews.md)
-   [DWM-Beispiel Code](dwm-samples.md)
-   [DWM-Referenz](reference.md)

 

 




