---
title: Filterbedingungs-Flags ("f")
description: Die Filter Bedingungs Flags der Windows-Filter Plattform (WFP) werden jeweils durch ein Bitfeld dargestellt.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743152"
---
# <a name="filtering-condition-flags"></a>Filtern von Bedingungs Flags

Die Filter Bedingungs Flags der Windows-Filter Plattform (WFP) werden jeweils durch ein Bitfeld dargestellt.

Diese Flags und die Filter Ebenen, in denen Sie verwendet werden können, werden wie folgt definiert.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ Loopback**
</dt> <dd> <dl> <dt>



Testet, ob der Netzwerk Datenverkehr Loopback-Datenverkehr ist.

Filter Ebenen:

-   WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}
-   WPM- \_ Ebene \_ ausgehende \_ ippacket \_ V {4 \| 6}
-   WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6}
-   Ausgehender Transport der WPM- \_ Schicht \_ \_ \_ V {4 \| 6}
-   WPM- \_ \_ ebenenstream \_ {V4 \| 6}
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   Eingehende ICMP-Fehler in der WPM- \_ Schicht \_ \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   \_ \_ Ausgehender \_ ICMP- \_ Fehler \_ V {4 \| 6} für die WPM-Ebene
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung
-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   F & # amp; \_ \_ \_ \_ \_ 4 \| 6}
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ IPSec- \_ geschützt**
</dt> <dd> <dl> <dt>



Testet, ob der Netzwerk Datenverkehr durch IPSec geschützt ist.

Filter Ebenen:

-   WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}
-   WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung
-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**das Flag der SWP- \_ Bedingung \_ \_ ist \_ reautorisieren.**
</dt> <dd> <dl> <dt>



Testet auf eine Richtlinien Änderung im Gegensatz zu einer neuen Verbindung.

Filter Ebenen:

-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung
-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP \_ - \_ bedingungsflag ist Platzhalter \_ \_ \_ Bindung**
</dt> <dd> <dl> <dt>



Testet, ob die Anwendung beim Binden an eine lokale Netzwerkadresse eine Platzhalter Adresse angegeben hat.

Filter Ebene:

-   F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**das Flag der f \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Testet, ob der lokale Endpunkt, der Datenverkehr sendet und empfängt, ein unformatierten Endpunkt ist.

Filter Ebenen:

-   WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6}
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   Ausgehender Transport der WPM- \_ Schicht \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   Datagramm-Daten der WPM- \_ Ebene \_ \_ \_ {V4 \| 6}
    > [!Note]  
    > Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung
-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ Fragment**
</dt> <dd> <dl> <dt>



Testet, ob die \_ \_ an einen Legenden-Treiber übergebenen Struktur der Netzwerk Puffer Liste ein IP-Paket Fragment ist.

Filter Ebenen:

-   WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}
-   WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6} \_ verwerfen


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**Das \_ Flag der \_ SWP-Bedingung ist eine \_ \_ \_ fragmentgruppe**
</dt> <dd> <dl> <dt>



Testet, ob die \_ \_ an einen Legenden-Treiber übergebenen Struktur der Netzwerk Puffer Liste eine verknüpfte Liste von Paket Fragmenten beschreibt.

Filter Ebene:

-   WPM- \_ Ebene \_ ipforward \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**das Flag für die SWP- \_ Bedingung \_ \_ ist \_ IPSec \_ natt \_ Reclassify.**
</dt> <dd> <dl> <dt>



Gibt an, dass das gleiche Paket auf der Transport Ebene erneut klassifiziert wird, wenn der IPSec-NAT-Shim den Wert des Remoteports übersetzt.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**Flag für die SWP- \_ Bedingung \_ erfordert die ALE- \_ \_ \_ Klassifizierung**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket auf der ALE-Empfangs-/akzep-Ebene neu klassifiziert wird.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**das Flag der SWP- \_ Bedingung \_ ist eine \_ \_ implizite \_ Bindung.**
</dt> <dd> <dl> <dt>



Testet, ob Windows Sockets eine implizite Bindung ausführt.

Nur unter Windows Vista und Windows Server 2008 verfügbar.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**das Flag für die SWP- \_ Bedingung \_ \_ wird wieder \_ zusammengefügt**
</dt> <dd> <dl> <dt>



Testet, ob das Paket neu zusammengefügt wurde.

> [!Note]  
> Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

 

Filter Ebene:

-   WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**SWP-Bedingungs Kennzeichen \_ \_ \_ ist \_ namens- \_ App \_ angegeben**
</dt> <dd> <dl> <dt>



Testet, ob der Name des Peer Computers, mit dem die Anwendung eine Verbindung herstellt, über eine API wie [**wsasetsocketpeertargetname**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) empfangen wurde und nicht über die cacheheuristik abgerufen wird.

> [!Note]  
> Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**das Flag für die SWP- \_ Bedingung \_ \_ ist \_ Promiscuous**
</dt> <dd> <dl> <dt>



Reserviert.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ auth \_ FW**
</dt> <dd> <dl> <dt>



Testet, ob die Verbindung durch End-to-End-Authentifizierung authentifiziert ist, auch wenn die einzelnen Pakete nicht überprüft wurden.

> [!Note]  
> Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**das Flag der SWP- \_ Bedingung \_ \_ ist \_ neu klassifizieren.**
</dt> <dd> <dl> <dt>



Testet, ob die Filter-Engine eine vorherige Bindungs-oder Abhör Anforderung neu klassifiziert.

> [!Note]  
> Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

Filter Ebene:

-   Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}
-   F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**das Flag der SWP- \_ Bedingung \_ ist eine \_ \_ Proxy \_ Verbindung.**
</dt> <dd> <dl> <dt>



Testet, ob die Verbindung einen Proxy verwendet.

> [!Note]  
> Nur unter Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**Das BWP-Bedingungs Kennzeichen \_ \_ ist " \_ \_ appcontainer \_ Loopback".**
</dt> <dd> <dl> <dt>



Testet, ob der Netzwerk Datenverkehr App-Container Loopback-Datenverkehr ist.

> [!Note]  
> Nur unter Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**das Flag der BWP- \_ Bedingung \_ \_ ist \_ kein \_ appcontainer- \_ Loopback.**
</dt> <dd> <dl> <dt>



Testet, ob der Netzwerk Datenverkehr nicht-APP-Container Loopback-Datenverkehr ist.

> [!Note]  
> Nur unter Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**das Flag der SWP- \_ Bedingung \_ \_ ist \_ reserviert.**
</dt> <dd> <dl> <dt>



Reserviert.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**das Flag der SWP- \_ Bedingung \_ ist die \_ \_ \_ Autorisierung der Richtlinie \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die aktuelle Klassifizierung ausgeführt wird, um die Absicht zu berücksichtigen, dass eine umgeleitete Windows Store-App eine Verbindung mit einem angegebenen Host herstellt. Eine solche Klassifizierung enthält die gleichen klassifizierbaren Feldwerte, als ob die APP nie umgeleitet würde. Das-Flag gibt auch an, dass eine zukünftige Klassifizierung aufgerufen wird, um das effektive umgeleitete Ziel abzugleichen. Wenn die APP zur Überprüfung an einen Proxy Dienst umgeleitet wird, bedeutet dies auch, dass für die Proxy Verbindung eine zukünftige Klassifizierung aufgerufen wird. Callout-Treiber sollten diese Klassifizierung im allgemeinen erlauben.

> [!Note]  
> Nur unter Windows 8 und Windows Server 2012 verfügbar.

 

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Die folgenden Flags geben den Grund für die Neuautorisierung einer zuvor autorisierten Verbindung an. Diese Flags und die Filter Ebenen, in denen Sie verwendet werden können, werden wie folgt definiert.

> [!Note]  
> Diese Filterbedingungen sind nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**Änderung der \_ Grundrichtlinie für die \_ erneute Autorisierung der \_ Grundbedingung \_ \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung aufgrund von hinzugefügten oder entfernten Filtern erneut autorisiert wurde.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**Grund für \_ die \_ Neuautorisierung der Grundbedingung für die \_ \_ neue \_ Ankunfts \_ Schnittstelle**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket von einer unbekannten Schnittstelle eingetroffen ist.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**Grund für die erneute \_ \_ Autorisierung der \_ Grundbedingung \_ neuer \_ nexthop- \_ Schnittstelle**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket von einer unbekannten Schnittstelle abweicht.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**Grund für \_ die \_ erneute Autorisierung des \_ Grund Profils der Grundbedingung \_ \_**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket Schnittstellen von mehr als einer Netzwerk Kategorie überschritten hat.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**Grund für \_ die \_ Neuautorisierung der Grundbedingung für die \_ \_ Klassifizierung \_**
</dt> <dd> <dl> <dt>



Gibt an, dass eine zuvor gehaltene Verbindung jetzt zugelassen wird.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**Grund für \_ \_ erneute Autorisierung der Grundbedingungen für \_ \_ IPSec- \_ Eigenschaften \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die IPsec-Eigenschaften geändert wurden oder dass sich die Verbindung von Klartext in eine sichere Verbindung geändert hat.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**Grund für \_ die \_ erneute Autorisierung der Grundbedingung für die Daten \_ \_ \_ Strom Überprüfung \_**
</dt> <dd> <dl> <dt>



Gibt an, dass eine zuvor festgelegte TCP-Verbindung jetzt überprüft wird.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**Grund für \_ die \_ erneute Autorisierung von \_ Grundbedingungen \_ \_ \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die socketeigenschaften festgelegt wurden, nachdem eine Verbindung autorisiert und eingerichtet wurde.

Filter Ebene:

-   WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}
-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**Grund für \_ \_ Neuautorisierung \_ Grund für \_ neuen \_ eingehenden \_ mcast- \_ Bcast \_ Paket**
</dt> <dd> <dl> <dt>



Gibt an, dass neue eingehende Multicast-oder Broadcast Pakete bei Alen recv Accept-aufrufen erneut autorisiert werden \_ \_ .

Filter Ebene:

-   Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung


</dt> </dl> </dd> </dl>

Die folgenden Flags geben socketeigenschaften an, die sich darauf beziehen, ob eine Anwendung Edge-Traversal-Datenverkehr empfangen möchte. Diese Flags und die Filter Ebenen, in denen Sie verwendet werden können, werden wie folgt definiert.

> [!Note]  
> Diese Filterbedingungen sind nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**Flag für die Eigenschaft "SWP \_ Condition \_ Socket" \_ \_ \_ ist \_ System \_ Port \_ RPC**
</dt> <dd> <dl> <dt>



Gibt an, dass die Anwendung mit einem dynamischen RPC-Port kommuniziert.

Filter Ebene:

-   Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}
-   F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**SWP-Eigenschaft für den \_ \_ \_ socketeigenschaft " \_ \_ \_ Edge \_ "**
</dt> <dd> <dl> <dt>



Gibt an, dass die Anwendung edgetraversal-spezifischen Datenverkehr empfangen möchte.

Filter Ebene:

-   Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}
-   F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**SWP-Eigenschaft für das \_ \_ Socket- \_ Eigenschafts \_ Flag " \_ \_ Edge \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die Anwendung keinen Edge-Traversal-spezifischen Datenverkehr empfangen oder verarbeiten möchte.

Filter Ebene:

-   Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}
-   F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Die folgenden Flags geben Verbindungsdetails im Zusammenhang mit der L2-Filterung an.

> [!Note]  
> Diese Filterbedingungen sind nur unter Windows 8 und Windows Server 2012 verfügbar.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**Die f- \_ Bedingung \_ L2 \_ ist \_ natives \_ Ethernet.**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung Native Ethernet ist.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung Wi-Fi ist.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**F WP- \_ Bedingung \_ L2 \_ ist \_ mobiles \_ Breitband**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung ein mobiles Breitband ist.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi Direct- \_ \_ Daten**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung Wi-Fi Direct ist.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**F- \_ Bedingung \_ L2 \_ ist \_ VM2VM**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung zwischen virtuellen Computern besteht.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**Die f- \_ Bedingung \_ L2 \_ ist \_ falsch \_ formatiertes Paket.**
</dt> <dd> <dl> <dt>



Gibt an, dass ein Paket falsch formatiert ist.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**\_ \_ \_ \_ SWP-Bedingung L2 ist IP- \_ \_ fragmentgruppe**
</dt> <dd> <dl> <dt>



Gibt eine IP-Paket fragmentgruppe an.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**SWP- \_ Bedingung \_ L2, \_ Wenn \_ Connector \_ vorhanden ist**
</dt> <dd> <dl> <dt>



Gibt an, dass ein Connector vorhanden ist.

Filter Ebene:

-   fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet
-   fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene
-   \_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

