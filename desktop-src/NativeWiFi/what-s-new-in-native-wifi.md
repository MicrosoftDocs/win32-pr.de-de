---
description: Neues in nativem WiFi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Neues in nativem WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347293"
---
# <a name="whats-new-in-native-wifi"></a>Neues in nativem WiFi

## <a name="windows-10-version-2004"></a>Windows 10, Version 2004

Weitere Informationen finden Sie unter [Bereitstellen eines Wi-Fi Profils über eine Website](prov-wifi-profile-via-website.md).

## <a name="windows-10"></a>Windows 10

Die Unterstützung für Hotspot 2,0 wurde dem [WLAN- \_ Profil Schema](wlan-profileschema-schema.md)hinzugefügt. Hotspot 2,0 ermöglicht die automatische Verbindung mit öffentlichen Wi-Fi Diensten unter Verwendung vorhandener Anmelde Informationen und der Mitgliedschaft in Dienstanbieter Netzwerken. Dienstanbieter geben an, wie Verbindungen mithilfe der neuen Schema Elemente hergestellt werden, um zu beschreiben, welche Netzwerke verwendet werden sollen und wie Sie sich bei Ihnen authentifizieren. Weitere Informationen finden Sie in der Dokumentation zum [**Hotspot2**](wlan-profileschema-hotspot2-element.md) -Element.

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 und Windows Server 2012

Die folgenden Features wurden den nativen WiFi-APIs unter Windows 8 und Windows Server 2012 hinzugefügt.

Eine Wi-Fi Direct-Funktion, die auf der Entwicklung der Wi-Fi Peer-to-Peer Technical Specification v 1.1 von der Wi-Fi Alliance basiert (siehe [veröffentlichte Wi-Fi Alliance-Spezifikationen](https://www.wi-fi.org/)). Das Ziel der Wi-Fi Peer-to-Peer-technischen Spezifikation besteht darin, eine Lösung für die Wi-Fi Geräte-zu-Gerät-Konnektivität bereitzustellen, ohne dass entweder ein drahtloser Zugriffspunkt (drahtlos Zugriffspunkt) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.

Die folgenden Funktionen unterstützen die Wi-Fi Direct-Funktion.

-   [**Rückruf für das Beenden der WFD- \_ \_ Sitzung \_ \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WF-cancelopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WF-CloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WF-CloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WF-openhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WF-openlegacysession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WF-startopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WF dupdatedevicevisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Die folgenden Features wurden den nativen WiFi-APIs unter Windows 7 und Windows Server 2008 R2 hinzugefügt.

Das drahtlos gehostete Netzwerk ermöglicht einem einzelnen physischen drahtlosen Adapter das Herstellen einer Verbindung als Client mit einem Hardware Zugriffspunkt (AP), während gleichzeitig ein Software-AP-Gerät fungiert, das anderen drahtlos fähigen Geräten das Herstellen einer Verbindung ermöglicht.

Die folgenden Funktionen unterstützen das Feature für drahtlos gehostete Netzwerke.

-   [**Wlanhustednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**Wlanhustednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**Wlanhustednetworkinitsettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**Wlanhustednetworkqueryproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**Wlanhustednetworkquerysecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**Wlanhustednetworkquerystatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**Wlanhustednetworkrefreshsecuritysettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**Wlanhustednetworksetproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**Wlanhustednetworksetsecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**Wlanhustednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**Wlanhustednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**Wlanregistervirtualstationnotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

Die folgenden neuen Strukturen, die mit einem drahtlos gehosteten Netzwerk funktionieren.

-   [**WLAN- \_ gehostete \_ Netzwerk \_ Verbindungs \_ Einstellungen**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**vom WLAN \_ gehosteter \_ Netzwerk \_ \_ datenpeer- \_ Status \_ Änderung**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**Status des WLAN- \_ gehosteten \_ Netzwerks \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**Funk Status des WLAN- \_ gehosteten \_ Netzwerks \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**vom WLAN \_ gehostete \_ Netzwerk \_ Sicherheits \_ Einstellungen**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**vom WLAN \_ gehostete \_ Netzwerk \_ Status \_ Änderungen**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**Status des WLAN- \_ gehosteten \_ Netzwerks \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Die folgenden neuen Enumerationen, die mit einem drahtlos gehosteten Netzwerk funktionieren.

-   [**über WLAN \_ gehosteter \_ Netzwerk \_ Benachrichtigungs \_ Code**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**WLAN- \_ gehosteter \_ Netzwerk- \_ Opcode**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**\_vom WLAN gehosteter \_ netzwerkpeer-Authentifizierungs \_ \_ \_ Status**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**Grund für WLAN- \_ gehostete \_ Netzwerke \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**WLAN- \_ gehosteter \_ Netzwerk \_ Status**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum drahtlos gehosteten Netzwerk](about-the-wireless-hosted-network.md)
</dt> <dt>

[Verwenden von drahtlos gehosteter Netzwerk-und Internet Verbindungs Freigabe](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



