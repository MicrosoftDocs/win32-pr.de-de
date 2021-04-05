---
title: Informationen zu NAP
description: Informationen zu NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707824"
---
# <a name="about-nap"></a>Informationen zu NAP

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der Netzwerk Zugriffsschutz (Network Access Protection, NAP) soll Administratoren dabei helfen, die Integrität der Computer im Netzwerk beizubehalten, die wiederum die Gesamt Integrität des Netzwerks aufrechterhalten. Es ist nicht zum Sichern eines Netzwerks vor böswilligen Benutzern vorgesehen. Wenn ein Computer beispielsweise über die gesamte Software und Konfigurationen verfügt, die für die Netzwerk Zugriffs Richtlinie erforderlich sind, wird der Computer als fehlerfrei oder kompatibel eingestuft und erhält den entsprechenden Zugriff auf das Netzwerk. NAP verhindert nicht, dass ein autorisierter Benutzer mit einem kompatiblen Computer ein schädliches Programm in das Netzwerk hochladen oder ein anderes ungeeignetes Verhalten einbindet.

Um den Zugriff auf ein Netzwerk zu schützen, muss eine Netzwerkinfrastruktur die folgenden Funktionsbereiche bereitstellen:

-   Integritäts Überprüfung: bestimmt, ob die Computer den System Integritäts Anforderungen entsprechen.
-   Netzwerk Einschränkung: schränkt den Zugriff auf das Netzwerk oder die Kommunikation für Clients ein, die nicht den System Integritäts Anforderungen entsprechen.
-   Wiederherstellung: Stellt erforderliche Updates bereit, damit der Computer seinen nicht kompatiblen Integritäts Status korrigieren kann.
-   Fortlaufende Konformität: ermöglicht den Zugriff auf das Netzwerk, solange der Computer des Benutzers die Integritäts Richtlinien Anforderungen erfüllt.

Windows XP mit Service Pack 3 (SP3), Windows Vista und Windows Server 2008 stellen NAP-Erzwingungs Methoden für die DHCP-Adress Konfiguration (Dynamic Host Configuration Protocol), RAS-basierte VPN (Virtual Private Network)-Verbindungen, IEEE 802.1 x-authentifizierte Kabel-und Drahtlos Verbindungen und IPSec-basierte (Internet Protocol Security) Kommunikation bereit. Die NAP-Plattform unterstützt zusätzlich eine Architektur, durch die Integritäts Überprüfung, Netzwerk Einschränkung, Wiederherstellung und fortlaufende Konformität von zusätzlichen Komponenten unterstützt werden, die von Drittanbietern oder von Microsoft bereitgestellt werden können.

Die NAP-Plattform umfasst die folgenden Komponenten:

-   [NAP-Client Architektur](nap-client-architecture.md)
-   [Server seitige NAP-Architektur](nap-server-side-architecture.md)
-   [Kommunikation zwischen NAP-Client und Server seitiger Komponente](nap-client-and-server-side-component-communication.md)

Der NAP-Client erfordert Windows Vista, Windows XP mit SP3 oder Windows Server 2008. Der NAP-Integritäts Richtlinien Server und NAP-Erzwingungs Punkte für DHCP-, VPN-und IPsec-Erzwingung erfordern Windows Server 2008.

 

 




