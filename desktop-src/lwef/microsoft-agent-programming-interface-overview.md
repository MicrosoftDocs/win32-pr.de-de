---
title: Übersicht über die Microsoft Agent-Programmierschnittstelle
description: Übersicht über die Microsoft Agent-Programmierschnittstelle
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856215"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Übersicht über die Microsoft Agent-Programmierschnittstelle

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Microsoft-Agent-API bietet Dienste, die die Anzeige und Animation von animierten Zeichen unterstützen. Der Microsoft-Agent wird als OLE-Automatisierungsserver (Component Object Model \[ com \] ) implementiert und ermöglicht, dass mehrere Anwendungen, so genannte Clients oder Client Anwendungen, gleichzeitig auf die Animation, die Eingabe und die Ausgabe Dienste zugreifen und darauf zugreifen können. Ein Client kann eine beliebige Anwendung sein, die eine Verbindung mit den COM-Schnittstellen des Microsoft-Agents herstellt.

Als com-Server wird der Microsoft-Agent automatisch gestartet, wenn eine Client Anwendung die COM-Schnittstellen und Anforderungen zum Herstellen einer Verbindung verwendet. Sie wird weiterhin ausgeführt, bis alle Clients ihre Verbindungen schließen. Wenn keine verbundenen Clients vorhanden sind, wird der Microsoft-Agent automatisch beendet.

Obwohl Sie die COM-Schnittstellen des Microsoft-Agents direkt abrufen können, enthält der Microsoft-Agent auch ein Microsoft ActiveX-Steuerelement. Dieses Steuerelement erleichtert den Zugriff auf die Dienste von Microsoft Agent von Programmiersprachen, die die ActiveX-Steuerelement Schnittstelle unterstützen.

Zusätzlich zur Unterstützung eigenständiger Programme, die für Windows geschrieben wurden, kann der-Agent für die Unterstützung von Webseiten erstellt werden, vorausgesetzt, der Browser unterstützt die ActiveX-Schnittstelle. Microsoft Internet Explorer bietet Unterstützung für ActiveX und Skriptsprachen, die Sie zum Programmieren von-Agents verwenden können. Wenn Sie nicht Internet Explorer verwenden, wenden Sie sich an Ihren Hersteller oder Lieferanten über die Unterstützung von ActiveX im Browser.

Die folgenden Informationen bieten eine kurze Übersicht über die Programmierschnittstellen für die Microsoft-Agent-Software.

-   [Animations Dienste](animation-services.md)
-   [Eingabe Dienste](input-services.md)
-   [Das Fenster "Sprachbefehle"](the-voice-commands-window.md)
-   [Ausgabe Dienste](output-services.md)

 

 




