---
title: Desktopfenster-Manager
description: Die in Vista Windows eingeführte Desktopkompositionsfunktion hat sich grundlegend geändert, wie Anwendungen Pixel auf dem Bildschirm anzeigen.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Desktopfenster-Manager (DWM), Informationen
- DWM (Desktopfenster-Manager),about
- Desktopfenster-Manager (DWM), Komposition
- DWM (Desktopfenster-Manager),Composition
- Desktopkomposition
- Komposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8259be171f225cc955546314febdff5395a47318499b830ee855bc8b985b025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456040"
---
# <a name="desktop-window-manager"></a>Desktopfenster-Manager

Die in Vista Windows eingeführte Desktopkompositionsfunktion hat sich grundlegend geändert, wie Anwendungen Pixel auf dem Bildschirm anzeigen. Wenn die Desktopkomposition aktiviert ist, zeichnen einzelne Fenster nicht mehr direkt auf den Bildschirm oder das primäre Anzeigegerät, wie in früheren Versionen von Windows. Stattdessen wird ihre Zeichnung an Offscreenoberflächen im Videospeicher umgeleitet, die dann in ein Desktopbild gerendert und auf der Anzeige angezeigt werden.

Die Desktopkomposition wird vom Desktopfenster-Manager (DWM) ausgeführt. Durch die Desktopkomposition ermöglicht DWM visuelle Effekte auf dem Desktop sowie verschiedene Features wie Fensterrahmen, 3D-Fensterübergangsanimationen, Windows Flip und Windows Flip3D sowie Unterstützung für hohe Auflösung.

Der Desktopfenster-Manager wird als Windows ausgeführt. Sie kann über das Element Verwaltung Systemsteuerung unter Dienste als Desktopfenster-Manager Sitzungs-Manager aktiviert und deaktiviert werden.

Viele der DWM-Features können von einer Anwendung über die DWM-APIs gesteuert oder aufgerufen werden. In der folgenden Dokumentation werden die Features und Anforderungen der DWM-APIs beschrieben.

-   [DWM-Übersichten](desktop-window-manager-overviews.md)
-   [DWM-Beispielcode](dwm-samples.md)
-   [DWM-Referenz](reference.md)

 

 




