---
description: Eine Teilmenge der Native Wifi-API-Funktionalität wird auf Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) unterstützt.
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Native Wifi-API-Unterstützung auf Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc284ed24a6aa6ddb266b410a6233c15e063bf909aa9c82f0afa3dc070c9289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685310"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Native Wifi-API-Unterstützung auf Windows XP

Eine Teilmenge der Native Wifi-API-Funktionalität wird auf Windows XP mit Service Pack 2 (SP2) und Windows XP mit Service Pack 3 (SP3) unterstützt. Diese Funktionalität ist standardmäßig in Windows XP mit SP3 enthalten. In Windows XP mit SP2 kann diese Funktionalität durch Anwenden eines Hotfixes hinzugefügt werden, der als Wlan-API für Windows XP mit Service Pack 2 (SP2) bezeichnet wird. Weitere Informationen oder zum Herunterladen des Hotfixes finden Sie unter "Entwickler können keine Drahtlosclientprogramme erstellen, die Drahtlosprofile und Verbindungen über den Wireless Zero Configuration-Dienst in Microsoft Windows XP Service Pack 2 (SP2)" im Hilfe- und Support-Knowledge Base unter [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) verwalten.

Aufgrund der zugrunde liegenden Architekturunterschiede in Windows XP weist die Native Wifi-API für einige Einschränkungen auf. Im Folgenden finden Sie eine Liste der Einschränkungen:

-   Einem Profil kann höchstens eine SSID zugeordnet werden.
-   Infrastrukturnetzwerke werden immer vor Ad-hoc-Netzwerken in der Profilliste angezeigt.
-   Profilnamen werden von der SSID abgeleitet und können vom Benutzer nicht auf eine beliebige Zeichenfolge festgelegt werden.
-   PHY-Typen werden nicht unterstützt.
-   Das Zwischenspeichern des paarweisen Hauptschlüssels (Pairwise Master Key, PMK) wird nicht unterstützt.
-   Erweiterbarkeitsfunktionen unabhängiger Hardwarehersteller (Independent Hardware Vendor, IHV) werden nicht unterstützt.
-   Profilberechtigungen werden nicht unterstützt.
-   Nur die \_ WLAN-Benachrichtigung \_ \_ acm-Verbindung \_ ist abgeschlossen, und die WLAN-Benachrichtigung \_ \_ acm \_ disconnected notifications ist verfügbar.
-   Globale 802.1X- und EAPOL-Konfigurationseinstellungen werden nicht unterstützt.

Die folgenden Funktionen werden von Windows XP mit SP3 und der Wlan-API für Windows XP mit SP2 unterstützt:

-   [**\_ \_ WLAN-BENACHRICHTIGUNGSRÜCKRUF**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**WLANAllocateMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**WLANCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**WLANVerbindung**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**WLANDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**WlanFreeMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**WLANGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**WlanGetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**WlanOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**WLANRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**WlanSetProfileEapXmlUserData**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**WlanSetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**WlanSetProfilePosition**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[Informationen zu Native Wifi](about-native-wifi.md)
</dt> </dl>

 

 
