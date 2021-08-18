---
title: Netzwerkzugriffsschutz
description: Hinweis Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 Network Access Protection (NAP) nicht mehr verfügbar. Dabei handelt es sich um eine Reihe von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Netzwerkzugriffsschutz
- Netzwerkzugriffsschutz,Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e5b5121566c3626ee7a9f2ba5d85efc1bf6cff17b412cd99874ae9b346780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939128"
---
# <a name="network-access-protection"></a>Netzwerkzugriffsschutz

## <a name="purpose"></a>Zweck

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Network Access Protection (NAP) ist ein Satz von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen. Die NAP-Plattform bietet eine integrierte Möglichkeit, den Systemstatus eines Netzwerkclients zu bewerten, der versucht, eine Verbindung mit einem Netzwerk herzustellen oder in einem Netzwerk zu kommunizieren, und den Zugriff des Netzwerkclients so lange zu beschränken, bis die Anforderungen an die Integritätsrichtlinie erfüllt sind.

NAP ist eine erweiterbare Plattform, die eine Infrastruktur und einen API-Satz zum Hinzufügen von Komponenten zum Speichern, Melden, Überprüfen und Korrigieren des Systemstatus eines Computers bietet. Die NAP-Plattform selbst stellt keine Komponenten zum Sammeln und Auswerten von Attributen des Integritätsstatus eines Computers zur Verfügung. Andere Komponenten, die als Systemzustands-Agents (SYSTEM Health Agents, SHAs) und System health validators (SHVs) bezeichnet werden, bieten Netzwerkrichtlinienüberprüfung und Netzwerkrichtlinienkonformität.

## <a name="where-applicable"></a>Anwendungsbereich

NAP ist erweiterbar. Sie kann mit jeder Anbietersoftware zusammenarbeiten, die SHAs und SHVs bietet oder die den veröffentlichten API-Satz erkennt. NAP bietet eine Lösung für die folgenden gängigen Szenarien:

-   Überprüfen Sie die Integrität und den Status von Roaming-Laptops.
-   Stellen Sie die Integrität von Desktopcomputern sicher.
-   Überprüfen Sie die Konformität und Integrität von Computern in Remotebüros.
-   Bestimmen Sie die Integrität von Besuchen von Laptops.
-   Überprüfen Sie die Konformität und Integrität von nicht verwalteten Heimcomputern.

## <a name="developer-audience"></a>Entwicklergruppe

Die NAP-API ist für C/C++-Entwickler konzipiert. Für die NAP-Erzwingungsmethoden sollten Programmierer mit Netzwerkprotokollen und -technologien vertraut sein, z. B. RADIUS (Remote Authentication Dial-in User Service), DHCP (Dynamic Host Configuration Protocol), virtuelle private Netzwerke (VPNs), IEEE 802.1X-Standard für kabelgebundenen und drahtlosen Zugriff und Internetprotokollsicherheit (IPsec).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die NAP-Plattform erfordert NAP-Infrastrukturserver, auf denen Windows Server 2008 oder höher ausgeführt wird, sowie NAP-Clients, auf denen Windows XP mit Service Pack 3 (SP3), Windows Vista oder höher ausgeführt wird. Spezifische Informationen dazu, welche Betriebssysteme ein bestimmtes Programmierelement unterstützen, finden Sie in den Abschnitten Anforderungen der NAP-APIs in der NAP-Referenzdokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                         | Beschreibung                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [Informationen zu NAP](about-nap.md)<br/>         | Allgemeine Informationen zur NAP-API.<br/>                                     |
| [Verwenden von NAP](using-nap.md)<br/>         | Verwendungsbeispiele für die NAP-API.<br/>                                            |
| [NAP-Referenz](nap-reference.md)<br/> | Dokumentation für NAP-Schnittstellen, -Strukturen und andere Codeelemente.<br/> |



 

 

 





