---
description: Aufgrund der zugrunde liegenden Architekturunterschiede im Betriebssystem unterstützen Windows XP mit Service Pack 3 (SP3) und die Wlan-LAN-API für Windows XP mit Service Pack 2 (SP2) nur eine Teilmenge der Elemente, die im Referenzmaterial WLAN-Profilschema und \_ OneX-Schema beschrieben sind.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Kompatibilität von Drahtlosprofilen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36db0ecea6f85341d904603c99308ec10e79cee20d7567160cd3beee3b13c35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684570"
---
# <a name="wireless-profile-compatibility"></a>Kompatibilität von Drahtlosprofilen

Aufgrund der zugrunde liegenden Architekturunterschiede im Betriebssystem unterstützen Windows XP mit Service Pack 3 (SP3) und die Wlan-LAN-API für Windows XP mit Service Pack 2 (SP2) nur eine Teilmenge der Elemente, die im [Referenzmaterial \_ WLAN-Profilschema](wlan-profileschema-schema.md) und [OneX-Schema](onexschema-schema.md) beschrieben sind.

Alle Profile, die Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2-Anforderungen entsprechen, können auch unter Windows Vista und Windows Server 2008 verwendet werden.

## <a name="wlan_profile-support"></a>UNTERSTÜTZUNG FÜR \_ WLAN-Profile

Die folgenden WLAN-Profilelemente werden in Windows XP mit SP3 oder der Wlan-API für Windows \_ XP mit SP2 nicht unterstützt:

-   Konnektivität (IHV)
-   IHV (WLANProfile)
-   OUI (OUIHeader)
-   phyType (Konnektivität)
-   PMKCacheMode (Sicherheit)
-   PMKCacheSize (Sicherheit)
-   PMKCacheTTL (Sicherheit)
-   preAuthMode (Sicherheit)
-   preAuthThrottle (Sicherheit)
-   Sicherheit (IHV)
-   type (OUIHeader)
-   useMSOneX (IHV)

In der folgenden Tabelle sind WLAN-Profilelemente mit eingeschränkten Werten für Windows XP mit \_ SP3 und die Wlan-LAN-API für Windows XP mit SP2 aufgeführt:



| Element                                                                               | Constraint                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**name (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | Das Name-Element wird ignoriert, wenn das Profil im Profilspeicher gespeichert wird. Der Name des Profils wird automatisch von der SSID des Netzwerks abgeleitet. Bei Infrastrukturnetzwerkprofilen ist der Name des Profils die SSID des Netzwerks. Bei Ad-hoc-Netzwerkprofilen ist der Name des Profils die SSID des Ad-hoc-Netzwerks gefolgt von `-adhoc` . |
| [**protected (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Muss den Wert FALSE haben.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Ist auf ein [**untergeordnetes SSID-Element (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) beschränkt.                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>OneX-Unterstützung

Nur das [**EAPConfig-Element**](onexschema-eapconfig-onex-element.md) wird auf Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 unterstützt. Andere OneX-Elemente, sofern in einem Profil vorhanden, werden ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur nativen WLAN-API](about-the-native-wifi-api.md)
</dt> <dt>

[Native Wifi-API-Unterstützung auf Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



