---
description: Veranschaulicht die Verwendung grundlegender drahtloser Netzwerk Verwaltungsfunktionen.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Native WiFi-API-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349842"
---
# <a name="native-wifi-api-sample"></a>Native WiFi-API-Beispiel

Ein System eigenes WiFi-API-Beispiel, das die Verwendung grundlegender Drahtlos Netzwerk-Verwaltungsfunktionen veranschaulicht, ist im Microsoft Windows Software Development Kit (SDK) enthalten. Die neueste Version der Windows SDK ist im [Download Center](https://developer.microsoft.com/windows/downloads)verfügbar.

Standardmäßig wird der Native WiFi-Beispiel Quellcode im folgenden Verzeichnis installiert:

**C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ <version number> \\ Samples \\ netds \\ WLAN**

Das Native WiFi-API-Beispiel befindet sich im folgenden Ordner:

**autoConfig**

Das Native WiFi-Beispiel kann unter Windows Vista und höher, Windows XP mit Service Pack 3 (SP3) und Wireless LAN API für Windows XP mit Service Pack 2 (SP2) kompiliert und ausgeführt werden. Einige Features des Beispiels werden unter Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 nicht unterstützt. Eine Liste der Funktionen, die von Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 unterstützt werden, finden Sie [unter Native WiFi-API-Unterstützung unter Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).

Das Native WiFi-Beispiel veranschaulicht, wie die folgenden Aufgaben ausgeführt werden:

-   Listet drahtlose Schnittstellen auf. Weitere Informationen finden Sie unter [**wlanenuminterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Nutzen Sie die Funktionen einer Schnittstelle. Weitere Informationen finden Sie unter [**wlangetinterfakecapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2: * * Diese Funktion wird nicht unterstützt.

-   Abfragen einer Schnittstelle. Weitere Informationen finden Sie unter [**wlanqueryinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Festlegen von Parametern für eine Netzwerkschnittstelle. Weitere Informationen finden Sie unter [**wlansetinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Diese Funktion kann verwendet werden, um das drahtlose Radio zu aktivieren und zu deaktivieren (und damit Drahtlos Netzwerk Konnektivität zu aktivieren oder zu deaktivieren).
-   Suchen Sie nach verfügbaren Drahtlos Netzwerken. Siehe [**wlanscan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Hier finden Sie eine Liste der verfügbaren oder sichtbaren Drahtlos Netzwerke. Weitere Informationen finden Sie unter [**wlangetavailablenetworklist**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Hiermit können Sie ein Profil erstellen, speichern oder löschen. Weitere Informationen finden Sie unter [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)und [**wlandeleteprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Herstellen einer Verbindung mit einem Drahtlos Netzwerk oder Trennen der Verbindung. Weitere Informationen finden Sie unter [**wlanconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) und [**wlandisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von nativem WiFi](using-native-wifi.md)
</dt> <dt>

[Windows Vista-drahtlos-SDK-Forum](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Problembehandlung bei drahtlosen Windows Vista 802,11-Verbindungen](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
