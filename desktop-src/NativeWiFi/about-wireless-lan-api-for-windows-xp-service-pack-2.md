---
description: Eine Teilmenge der nativen WiFi-API-Funktionen wird unter Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) unterstützt.
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Native WiFi-API-Unterstützung unter Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346009"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Native WiFi-API-Unterstützung unter Windows XP

Eine Teilmenge der nativen WiFi-API-Funktionen wird unter Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) unterstützt. Diese Funktionalität ist standardmäßig in Windows XP mit SP3 enthalten. In Windows XP mit SP2 kann diese Funktionalität hinzugefügt werden, indem ein Hotfix angewendet wird, der als drahtlose LAN-API für Windows XP mit Service Pack 2 (SP2) bezeichnet wird. Weitere Informationen oder das Herunterladen des Hotfixes finden Sie unter "Entwickler können keine drahtlosen Client Programme erstellen, die drahtlos Profile und Verbindungen über den drahtlos Konfigurations Dienst für drahtlose Daten in Microsoft Windows XP Service Pack 2 (SP2)" in der Hilfe-und Support-Wissensdatenbank unter Verwalten [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

Aufgrund der zugrunde liegenden architektonischen Unterschiede in Windows XP gelten für die native WiFi-API von einige Einschränkungen. Im folgenden finden Sie eine Liste der Einschränkungen:

-   Höchstens eine SSID kann einem Profil zugeordnet werden.
-   Infrastruktur Netzwerke werden immer vor Ad-hoc-Netzwerken in der Profil Liste angezeigt.
-   Profilnamen werden von der SSID abgeleitet und können vom Benutzer nicht auf eine beliebige Zeichenfolge festgelegt werden.
-   PHY-Typen werden nicht unterstützt.
-   PMK-Zwischenspeicherung wird nicht unterstützt.
-   IHV-Erweiterbarkeits Funktionen (Independent Hardware Vendor) werden nicht unterstützt.
-   Profil Berechtigungen werden nicht unterstützt.
-   Es sind nur die WLAN \_ -Benachrichtigungs \_ -ACM \_ -Verbindung und die verbindungsverbindungen mit \_ WLAN- \_ Benachrichtigungs- \_ ACM \_ verfügbar.
-   Globale 802.1 x-und EAPOL-Konfigurationseinstellungen werden nicht unterstützt.

Die folgenden Funktionen werden von Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 unterstützt:

-   [**WLAN- \_ Benachrichtigungs \_ Rückruf**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**Wlanbelegcatememory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**Wlanclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**Wlanconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**Wlandeleteprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**Wlandisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**Wlanenuminterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**Wlanfrememory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**Wlangetavailablenetworklist**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**Wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**Wlangetprofilelist**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**Wlanopenhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**Wlanqueryinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**Wlanreasoncodedestring**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**Wlanregisternotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**Wlanscan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**Wlansetinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**Wlansetprofileeapxmluserdata**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**Wlansetprofilelist**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**Wlansetprofileposition**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[Informationen zu nativem WiFi](about-native-wifi.md)
</dt> </dl>

 

 
