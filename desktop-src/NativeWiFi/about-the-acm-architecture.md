---
description: Informationen zur ACM-Architektur
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Informationen zur ACM-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218199"
---
# <a name="about-the-acm-architecture"></a>Informationen zur ACM-Architektur

Das Auto Configuration Module (ACM) ist die neue drahtlose Konfigurationskomponente für Windows Vista. Windows XP mit Service Pack 3 (SP3) und Wireless LAN API für Windows XP mit Service Pack 2 (SP2) verwenden stattdessen den WZC-Dienst (Wireless Zero Configuration).

Das ACM scannt Netzwerke in regelmäßigen Abständen und verwendet einen iterativen Prozess zum auswählen und verbinden mit dem bevorzugten Netzwerk im Bereich, wenn für dieses Netzwerk eine Schnittstelle für die automatische Verbindung aktiviert ist. Das ACM speichert und ruft auch Netzwerk Profile ab, die ACM, Media Specific Module (MSM), Security und IHV-Einstellungen (Independent Hardware Vendor) enthalten. Diese Netzwerk Profile sind für die automatische Konfiguration vorgesehen.

Die automatische Konfiguration unterstützt sowohl globale als auch Schnittstellen spezifische Einstellungen und Netzwerk Profile. Die globalen Einstellungen und Netzwerk Profile werden konfiguriert, wenn der Computer einer Domäne mit einem Gruppenrichtlinien Objekt (GPO) auf Domänen Ebene oder der Organisationseinheit (OU) in der Active Directory-Hierarchie (AD) hinzugefügt wurde. Diese Gruppenrichtlinien Einstellungen und-Profile sind schreibgeschützt, werden auf jede 802,11-Schnittstelle im System angewendet und haben immer Vorrang vor den einzelnen Schnittstellen-und benutzerspezifischen Einstellungen und Netzwerk Profilen. Die Gruppenrichtlinien Profile werden am Anfang der Liste bevorzugter Netzwerk Profile auf jeder 802,11-Netzwerkschnittstelle platziert.

Die ACM-Architektur ist erweiterbar. IHVs können proprietäre drahtlose Funktionen implementieren, ohne das bereitgestellte Native 802,11-Framework zu ändern. Die verfügbar gemachten IHV-Steuerungsfunktionen und-Strukturen ermöglichen diese Erweiterbarkeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu nativem WiFi](about-native-wifi.md)
</dt> </dl>

 

 



