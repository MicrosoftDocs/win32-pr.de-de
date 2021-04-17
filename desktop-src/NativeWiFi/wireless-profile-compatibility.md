---
description: Aufgrund der zugrunde liegenden architektonischen Unterschiede im Betriebssystem unterstützen Windows XP mit Service Pack 3 (SP3) und die Wireless LAN-API für Windows XP mit Service Pack 2 (SP2) nur eine Teilmenge der Elemente, die im WLAN \_ -Profil Schema und im Onex-Schema Referenzmaterial beschrieben sind.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Kompatibilität von drahtlos Profilen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529240"
---
# <a name="wireless-profile-compatibility"></a>Kompatibilität von drahtlos Profilen

Aufgrund der zugrunde liegenden architektonischen Unterschiede im Betriebssystem unterstützen Windows XP mit Service Pack 3 (SP3) und die Wireless LAN-API für Windows XP mit Service Pack 2 (SP2) nur eine Teilmenge der Elemente, die im [WLAN- \_ Profil Schema](wlan-profileschema-schema.md) und im [Onex-Schema](onexschema-schema.md) Referenzmaterial beschrieben sind.

Alle Profile, die den Anforderungen Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2 entsprechen, können auch unter Windows Vista und Windows Server 2008 verwendet werden.

## <a name="wlan_profile-support"></a>WLAN- \_ Profil Unterstützung

Die folgenden WLAN- \_ Profil Elemente werden in Windows XP mit SP3 oder der Wireless LAN-API für Windows XP mit SP2 nicht unterstützt:

-   Konnektivität (IHV)
-   IHV (wlanprofile)
-   OUI (ouiheader)
-   phytype (Konnektivität)
-   Pmkcachemode (Sicherheit)
-   Pmkcachesize (Sicherheit)
-   Pmkcachettl (Sicherheit)
-   preauthmode (Sicherheit)
-   preauththrottle (Sicherheit)
-   Sicherheit (IHV)
-   Type (ouiheader)
-   usemsonex (IHV)

In der folgenden Tabelle sind die WLAN \_ -Profil Elemente mit eingeschränkten Werten für Windows XP mit SP3 und die drahtlose LAN-API für Windows XP mit SP2 aufgeführt:



| Element                                                                               | Constraint                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Name (wlanprofile)**](wlan-profileschema-name-wlanprofile-element.md)             | Das Name-Element wird ignoriert, wenn das Profil im Profil Speicher gespeichert wird. Der Name des Profils wird automatisch von der SSID des Netzwerks abgeleitet. Bei Infrastrukturnetzwerk Profilen ist der Name des Profils die SSID des Netzwerks. Bei Ad-hoc-Netzwerk Profilen ist der Name des Profils die SSID des Ad-hoc-Netzwerks gefolgt von `-adhoc` . |
| [**geschützt (sharedkey)**](wlan-profileschema-protected-sharedkey-element.md)       | Muss den Wert false aufweisen.                                                                                                                                                                                                                                                                                                                                      |
| [**Ssidconfig (wlanprofile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Beschränkt auf ein untergeordnetes [**SSID-Element (ssidconfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Onex-Unterstützung

Nur das [**eapconfig**](onexschema-eapconfig-onex-element.md) -Element wird unter Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 unterstützt. Andere Onex-Elemente, sofern Sie in einem Profil vorhanden sind, werden ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur nativen WiFi-API](about-the-native-wifi-api.md)
</dt> <dt>

[Native WiFi-API-Unterstützung unter Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



