---
description: Veranschaulicht die Verwendung grundlegender Funktionen für die Drahtlose Netzwerkverwaltung.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Beispiel für die Native Wifi-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed28fadcd73eb4b3e632702078280ddba55d683c66decfdf03bc948182c52d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801060"
---
# <a name="native-wifi-api-sample"></a>Beispiel für die Native Wifi-API

Im Microsoft Windows Software Development Kit (SDK) ist ein Native Wifi-API-Beispiel enthalten, das die Verwendung grundlegender Funktionen für die Drahtlose Netzwerkverwaltung veranschaulicht. Die neueste Version des Windows SDK ist im [Download Center](https://developer.microsoft.com/windows/downloads)verfügbar.

Standardmäßig wird der Native Wifi-Beispielquellcode im folgenden Verzeichnis installiert:

**C: \\ Programme \\ Microsoft SDKs Windows Samples \\ \\ <version number> \\ \\ NetDs \\ WLAN**

Das Native Wifi-API-Beispiel befindet sich im folgenden Ordner:

**Autoconfig**

Das Native Wifi-Beispiel kann kompiliert und auf Windows Vista und höher, Windows XP mit Service Pack 3 (SP3) und der WLAN-API für Windows XP mit Service Pack 2 (SP2) ausgeführt werden. Einige Features des Beispiels werden auf Windows XP mit SP3 und der Wlan-API für Windows XP mit SP2 nicht unterstützt. Eine Liste der Funktionen, die von Windows XP mit SP3 und der Wlan-API für Windows XP mit SP2 unterstützt werden, finden Sie unter [Native Wifi-API-Unterstützung auf Windows XP.](about-wireless-lan-api-for-windows-xp-service-pack-2.md)

Das Native Wifi-Beispiel veranschaulicht, wie die folgenden Aufgaben ausgeführt werden:

-   Aufzählen von Funkschnittstellen. Weitere Informationen finden Sie unter [**WlanEnumInterfaces.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   Abrufen der Funktionen einer Schnittstelle. Weitere Informationen finden Sie unter [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    **Windows XP mit SP3 und Wlan-API für Windows XP mit SP2: ** Dieses Feature wird nicht unterstützt.

-   Abfragen einer Schnittstelle. Weitere Informationen finden Sie [**unter WlanQueryInterface.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   Legen Sie Parameter für eine Netzwerkschnittstelle fest. Weitere Informationen finden Sie unter [**WlanSetInterface.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface) Diese Funktion kann verwendet werden, um das Funkgerät zu aktivieren und zu deaktivieren (und daher die Drahtlosnetzwerkkonnektivität zu aktivieren oder zu deaktivieren).
-   Suchen Sie nach verfügbaren Drahtlosnetzwerken. Weitere Informationen finden Sie [**unter WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Abrufen der Liste der verfügbaren oder sichtbaren Drahtlosnetzwerke. Siehe [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Abrufen, Speichern oder Löschen eines Profils. Weitere Informationen finden Sie unter [**WlanGetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)und [**WlanDeleteProfile.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   Verbinden zu einem drahtlos verbundenen Netzwerk, oder trennen Sie es von diesem. Weitere Informationen finden Sie unter [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) und [**WlanDisconnect.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von nativem WLAN](using-native-wifi.md)
</dt> <dt>

[Windows Vista Wireless SDK-Forum](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Problembehandlung bei Windows Vista 802.11-Drahtlosverbindungen](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
