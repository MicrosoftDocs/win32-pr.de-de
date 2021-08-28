---
description: Informationen zur ACM-Architektur
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Informationen zur ACM-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d75b6b365970c34174facd035ddf38c625e3e4fac72f011e612998c46e9bee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065176"
---
# <a name="about-the-acm-architecture"></a>Informationen zur ACM-Architektur

Das Automatische Konfigurationsmodul (Auto Configuration Module, ACM) ist die neue drahtlose Konfigurationskomponente für Windows Vista. Windows XP mit Service Pack 3 (SP3) und Wlan-LAN-API für Windows XP mit Service Pack 2 (SP2) verwenden stattdessen den WZC-Dienst (Wireless Zero Configuration).

Der ACM scannt Netzwerke in regelmäßigen Abständen und verwendet einen iterativen Prozess, um das bevorzugte Netzwerk im Bereich auszuwählen und eine Verbindung herzustellen, wenn für dieses Netzwerk eine Schnittstelle für die automatische Verbindung aktiviert ist. Der ACM speichert und ruft auch Netzwerkprofile ab, die Einstellungen für ACM, Media Specific Module (MSM), Sicherheit und unabhängige Hardwareanbieter (Independent Hardware Vendor, IHV) enthalten. Diese Netzwerkprofile sind für die automatische Konfiguration.

Die automatische Konfiguration unterstützt sowohl globale als auch schnittstellenspezifische Einstellungen und Netzwerkprofile. Die globalen Einstellungen und Netzwerkprofile werden konfiguriert, wenn der Computer einer Domäne mit einem Gruppenrichtlinienobjekt (Group Policy Object, GPO) entweder auf Domänenebene oder organisationseinheitsebene in der Active Directory-Hierarchie (AD) beigetreten ist. Diese Gruppenrichtlinieneinstellungen und -profile sind schreibgeschützt, werden auf jede 802.11-Schnittstelle im System angewendet und haben immer Vorrang vor den Einstellungen und Netzwerkprofilen pro Schnittstelle und Benutzer. Die Gruppenrichtlinienprofile werden auf jeder 802.11-Netzwerkschnittstelle ganz oben in der Liste der bevorzugten Netzwerkprofile platziert.

Die ACM-Architektur ist erweiterbar. IHVs können proprietäre Drahtlosfunktionen implementieren, ohne das bereitgestellte native Framework 802.11 zu ändern. Die verfügbar gemachten IHV-Steuerelementfunktionen und -Strukturen ermöglichen diese Erweiterbarkeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu nativem WLAN](about-native-wifi.md)
</dt> </dl>

 

 



