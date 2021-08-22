---
description: Neues in nativem WiFi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Neues in nativem WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a9430fa2c1645d574f8b4ab851a8cf5ce1407139cfe63a6aabeb3ebfd57abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064860"
---
# <a name="whats-new-in-native-wifi"></a>Neues in nativem WiFi

## <a name="windows-10-version-2004"></a>Windows 10, Version 2004

Weitere Informationen finden Sie unter [Bereitstellen eines Wi-Fi Profils über eine Website.](prov-wifi-profile-via-website.md)

## <a name="windows-10"></a>Windows 10

Unterstützung für Hotspot 2.0 wurde dem [ \_ WLAN-Profilschema](wlan-profileschema-schema.md)hinzugefügt. Hotspot 2.0 ermöglicht die automatische Verbindung mit öffentlichen Wi-Fi Diensten unter Verwendung vorhandener Anmeldeinformationen und der Mitgliedschaft in Dienstanbieternetzwerken. Dienstanbieter geben an, wie Verbindungen mithilfe der neuen Schemaelemente hergestellt werden, um zu beschreiben, welche Netzwerke verwendet werden sollen und wie sie sich bei ihnen authentifizieren. Weitere [](wlan-profileschema-hotspot2-element.md) Informationen finden Sie in der Hotspot2-Elementdokumentation.

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 und Windows Server 2012

Die folgenden Features wurden den Native Wifi-APIs auf Windows 8 und Windows Server 2012 hinzugefügt.

Ein Wi-Fi Direct-Feature, das auf der Entwicklung der Wi-Fi Peer-to-Peer Technical Specification v1.1 durch die Wi-Fi Alliance basiert (siehe Veröffentlichte Spezifikationen der [Wi-Fi Alliance](https://www.wi-fi.org/)). Das Ziel der Wi-Fi Technischen Peer-zu-Peer-Spezifikation besteht darin, eine Lösung für Wi-Fi Gerät-zu-Gerät-Konnektivität bereitzustellen, ohne dass entweder ein Drahtloser Zugriffspunkt (Wireless ACCESS Point, Drahtlos-AP) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.

Die folgenden Funktionen unterstützen das Wi-Fi Direct-Feature.

-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Die folgenden Features wurden den Native Wifi-APIs auf Windows 7 und Windows Server 2008 R2 hinzugefügt.

Das drahtlos gehostete Netzwerk ermöglicht es einem einzelnen physischen Drahtlosadapter, eine Verbindung als Client mit einem Hardwarezugriffspunkt (AP) herzustellen, während gleichzeitig als Software-AP fungiert und anderen drahtlos fähigen Geräten ermöglicht wird, eine Verbindung damit herzustellen.

Die folgenden Funktionen unterstützen das Drahtlose Gehostete Netzwerkfeature.

-   [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**WLANRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

Die folgenden neuen Strukturen, die mit dem drahtlos gehosteten Netzwerk funktionieren.

-   [**WLAN- \_ GEHOSTETE \_ \_ \_ NETZWERKVERBINDUNGSEINSTELLUNGEN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**ÄNDERUNG DES \_ \_ \_ \_ \_ PEERSTATUS \_ VON WLAN-GEHOSTETEN NETZWERKDATEN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**PEERSTATUS \_ DES GEHOSTETEN \_ WLAN-NETZWERKS \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**WLAN \_ HOSTED NETWORK RADIO STATE (FUNKSTATUS DES GEHOSTETEN \_ WLAN-NETZWERKS) \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**WLAN \_ HOSTED NETWORK SECURITY SETTINGS (SICHERHEITSEINSTELLUNGEN FÜR GEHOSTETES \_ WLAN-NETZWERK) \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**\_ZUSTANDSÄNDERUNG DES GEHOSTETEN \_ WLAN-NETZWERKS \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**\_ \_ \_ WLAN– GEHOSTETER NETZWERKSTATUS**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Die folgenden neuen Enumerationen, die mit dem drahtlos gehosteten Netzwerk funktionieren.

-   [**\_BENACHRICHTIGUNGSCODE FÜR GEHOSTETES \_ WLAN-NETZWERK \_ \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**WLAN \_ HOSTED \_ NETWORK \_ OPCODE**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**WLAN \_ HOSTED \_ NETWORK \_ PEER \_ AUTH \_ STATE**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**\_GRUND FÜR WLAN-GEHOSTETES \_ NETZWERK \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**\_WLAN: GEHOSTETER \_ \_ NETZWERKSTATUS**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum drahtlos gehosteten Netzwerk](about-the-wireless-hosted-network.md)
</dt> <dt>

[Verwenden von drahtlos gehosteten Netzwerken und Freigabe von Internetverbindung](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



