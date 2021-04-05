---
title: Netzwerkzugriffsschutz
description: Hinweis die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 Network Access Protection (NAP) nicht mehr verfügbar. es handelt sich um eine Gruppe von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Netzwerkzugriffsschutz
- Netzwerk Zugriffsschutz, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709803"
---
# <a name="network-access-protection"></a>Netzwerkzugriffsschutz

## <a name="purpose"></a>Zweck

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der Netzwerk Zugriffsschutz (Network Access Protection, NAP) ist ein Satz von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen. Die NAP-Plattform bietet eine integrierte Möglichkeit, den System Integritäts Status eines Netzwerk Clients auszuwerten, der versucht, eine Verbindung mit einem Netzwerk herzustellen oder in einem Netzwerk zu kommunizieren und den Zugriff auf den Netzwerkclient einzuschränken, bis die Integritäts Richtlinien Anforderungen erfüllt sind.

NAP ist eine erweiterbare Plattform, die eine Infrastruktur und einen API-Satz zum Hinzufügen von Komponenten bereitstellt, die den Systemintegritäts Zustand eines Computers speichern, melden, validieren und korrigieren. Die NAP-Plattform bietet allein keine Komponenten zum ansammeln und Auswerten von Attributen für den Integritäts Zustand eines Computers. Andere Komponenten, die als Systemintegritäts-Agents (SHAs) und System Integritätsprüfungen (SHVs) bezeichnet werden, stellen die Überprüfung der Netzwerk Richtlinie und die Konformität der Netzwerk Richtlinie bereit.

## <a name="where-applicable"></a>Anwendungsbereich

NAP ist als erweiterbar konzipiert. Er kann mit sämtlicher Hersteller Software interagieren, die SHAs und SHVs bereitstellt oder den veröffentlichten API-Satz erkennt. NAP hilft bei der Bereitstellung einer Lösung für die folgenden gängigen Szenarien:

-   Überprüfen Sie die Integrität und den Status von Roaminglaptops.
-   Stellen Sie sicher, dass die Integrität von Desktop Computern besteht.
-   Überprüfen Sie die Konformität und Integrität von Computern in Remote Niederlassungen.
-   Ermitteln der Integrität von Laptops.
-   Überprüfen Sie die Konformität und Integrität nicht verwalteter Heimcomputer.

## <a name="developer-audience"></a>Entwicklergruppe

Die NAP-API ist für C/C++-Entwickler konzipiert. Für die NAP-Erzwingungs Methoden sollten Programmierer mit Netzwerkprotokollen und-Technologien wie z. b. Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration-Protokoll (DHCP), virtuellen privaten Netzwerken (VPNs), dem IEEE 802.1 x-Standard für Kabel-und drahtlos Zugriff und Internet Protokoll Sicherheit (IPSec) vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die NAP-Plattform erfordert NAP-Infrastruktur Server, auf denen Windows Server 2008 oder höher ausgeführt wird, sowie NAP-Clients, auf denen Windows XP mit Service Pack 3 (SP3), Windows Vista oder höher ausgeführt wird. Spezifische Informationen dazu, welche Betriebssysteme ein bestimmtes Programmier Element unterstützen, finden Sie in den Abschnitten zu den Anforderungen der NAP-APIs in der NAP-Referenz Dokumentation.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                         | BESCHREIBUNG                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [Informationen zu NAP](about-nap.md)<br/>         | Allgemeine Informationen zur NAP-API.<br/>                                     |
| [Verwenden von NAP](using-nap.md)<br/>         | Verwendungs Beispiele für die NAP-API.<br/>                                            |
| [NAP-Referenz](nap-reference.md)<br/> | Dokumentation für NAP-Schnittstellen, Strukturen und andere Code Elemente.<br/> |



 

 

 





