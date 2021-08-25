---
title: Übersicht über die Microsoft Agent-Programmierschnittstelle
description: Übersicht über die Microsoft Agent-Programmierschnittstelle
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4dc087064afb0e3beaaf97d987e496239d3fd378461acaf5601927ac6d929
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887920"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Übersicht über die Microsoft Agent-Programmierschnittstelle

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Die Microsoft Agent-API stellt Dienste bereit, die die Anzeige und Animation von animierten Figuren unterstützen. Als OLE Automation-Server (Component Object Model COM) implementiert, ermöglicht Microsoft Agent mehreren Anwendungen, die als Clients oder Clientanwendungen bezeichnet werden, das Gleichzeitige Hosten und Zugreifen auf die Animations-, Eingabe- und \[ \] Ausgabedienste. Ein Client kann eine beliebige Anwendung sein, die eine Verbindung mit den COM-Schnittstellen des Microsoft-Agents herstellt.

Als COM-Server wird Microsoft Agent nur dann automatisch gestartet, wenn eine Clientanwendung die COM-Schnittstellen verwendet und eine Verbindung damit anfängt. Sie wird so lange ausgeführt, bis alle Clients ihre Verbindungen schließen. Wenn keine verbundenen Clients mehr verbleiben, wird Microsoft Agent automatisch beendet.

Obwohl Sie die COM-Schnittstellen von Microsoft Agent direkt aufrufen können, enthält Microsoft Agent auch ein Microsoft ActiveX-Steuerelement. Dieses Steuerelement erleichtert den Zugriff auf die Microsoft Agent-Dienste über Programmiersprachen, die die ActiveX-Schnittstelle unterstützen.

Zusätzlich zur Unterstützung eigenständiger Programme, die für Windows geschrieben wurden, kann der -Agent skriptiert werden, um Webseiten zu unterstützen, vorausgesetzt, dass der Browser die ActiveX unterstützt. Microsoft Internet Explorer bietet Unterstützung für ActiveX sowie Skriptsprachen, die Sie zum Programmieren des -Agents verwenden können. Wenn Sie keine Internet Explorer verwenden, wenden Sie sich an Ihren Anbieter oder Lieferanten, um sich über die Browserunterstützung für ActiveX.

Die folgenden Informationen bieten eine kurze Übersicht über die Programmierschnittstellen für die Microsoft Agent-Software.

-   [Animationsdienste](animation-services.md)
-   [Eingabedienste](input-services.md)
-   [Fenster "Sprachbefehle"](the-voice-commands-window.md)
-   [Ausgabedienste](output-services.md)

 

 




