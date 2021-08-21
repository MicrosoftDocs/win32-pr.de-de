---
title: Filterbedingungsflags (Fwptypes.h)
description: Die Windows Filterungsbedingungsflags der Filterplattform (WFP) werden jeweils durch ein Bitfeld dargestellt.
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
ms.openlocfilehash: 5a43ae080a9ef1c17baa262cc1154f9ae89a837f0ec6f6919d80c22376f3b995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150893"
---
# <a name="filtering-condition-flags"></a>Filterbedingungsflags

Die Windows Filterungsbedingungsflags der Filterplattform (WFP) werden jeweils durch ein Bitfeld dargestellt.

Diese Flags und die Filterebenen, in denen sie verwendet werden können, werden wie folgt definiert.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ LOOPBACK**
</dt> <dd> <dl> <dt>



Testet, ob es sich bei dem Netzwerkdatenverkehr um Loopbackdatenverkehr handelt.

Filterebenen:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   AUSGEHENDES \_ \_ \_ IPPACKET \_ V{4 \| 6} für FWPM LAYER
-   FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ STREAM \_ {V4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   FWPM \_ LAYER \_ INBOUND \_ ICMP ERROR \_ \_ V{4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   FWPM \_ LAYER \_ OUTBOUND \_ ICMP ERROR \_ \_ V{4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V{4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ \_ IPSEC-GESCHÜTZT**
</dt> <dd> <dl> <dt>



Testet, ob der Netzwerkdatenverkehr durch IPsec geschützt ist.

Filterebenen:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ \_ WIRD ERNEUT AUTORISIERT**
</dt> <dd> <dl> <dt>



Testet eine Richtlinienänderung im Gegensatz zu einer neuen Verbindung.

Filterebenen:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ \_ PLATZHALTERBINDUNG**
</dt> <dd> <dl> <dt>



Testet, ob die Anwendung bei der Bindung an eine lokale Netzwerkadresse eine Platzhalteradresse angegeben hat.

Filterebene:

-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ ROHEN \_ ENDPUNKT**
</dt> <dd> <dl> <dt>



Testet, ob der lokale Endpunkt, der Datenverkehr sendet und empfängt, ein roher Endpunkt ist.

Filterebenen:

-   FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   FWPM \_ LAYER \_ DATAGRAM DATA \_ \_ {V4 \| 6}
    > [!Note]  
    > Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

     

-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ FRAGMENT**
</dt> <dd> <dl> <dt>



Testet, ob die an einen Callouttreiber übergebene NET \_ BUFFER \_ LIST-Struktur ein IP-Paketfragment ist.

Filterebenen:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}
-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6} \_ DISCARD


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ \_ FRAGMENTGRUPPE**
</dt> <dd> <dl> <dt>



Testet, ob die an einen Callouttreiber übergebene NET BUFFER LIST-Struktur eine verknüpfte \_ \_ Liste von Paketfragmenten beschreibt.

Filterebene:

-   FWPM \_ LAYER \_ IPFORWARD \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ IPSEC \_ NATT \_ RECLASSIFY**
</dt> <dd> <dl> <dt>



Gibt an, dass das gleiche Paket auf der Transportebene neu klassifiziert wird, wenn der IPsec NAT-Shim den Remoteportwert übersetzt.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ ERFORDERT \_ ALE \_ CLASSIFY**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket auf der ALE-Empfangs-/Annahmeebene neu klassifiziert wird.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ IMPLIZITE \_ BINDUNG**
</dt> <dd> <dl> <dt>



Testet, Windows Sockets eine implizite Bindung ausführen.

Nur unter Windows Vista und Windows Server 2008 verfügbar.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ \_ WIRD NEU ZUSAMMENGESTELLT**
</dt> <dd> <dl> <dt>



Testet, ob das Paket neu zusammengestellt wurde.

> [!Note]  
> Nur auf Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.

 

Filterebene:

-   FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**\_ \_ FWP-BEDINGUNGSFLAG IST NAME APP \_ \_ \_ \_ SPECIFIED**
</dt> <dd> <dl> <dt>



Testet, ob der Name des Peercomputers, mit dem die Anwendung eine Verbindung herstellen soll, über eine API wie [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) empfangen und nicht über die Cachehuristik erhalten wurde.

> [!Note]  
> Nur auf Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ \_ IST PROMISCUOUS**
</dt> <dd> <dl> <dt>



Reserviert.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ AUTH \_ FW**
</dt> <dd> <dl> <dt>



Testet, ob die Verbindung end-to-end authentifiziert ist, auch wenn die einzelnen Pakete nicht überprüft wurden.

> [!Note]  
> Nur auf Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ RECLASSIFY**
</dt> <dd> <dl> <dt>



Testet, ob die Filter-Engine eine vorherige Bindungs- oder Lauschanforderung neu klassifiziert.

> [!Note]  
> Nur auf Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ \_ PROXYVERBINDUNG**
</dt> <dd> <dl> <dt>



Testet, ob die Verbindung einen Proxy verwendet.

> [!Note]  
> Nur auf Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ APPCONTAINER \_ LOOPBACK**
</dt> <dd> <dl> <dt>



Testet, ob es sich bei dem Netzwerkdatenverkehr um App-Container-Loopbackdatenverkehr handelt.

> [!Note]  
> Nur auf Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST NICHT \_ \_ APPCONTAINER \_ LOOPBACK**
</dt> <dd> <dl> <dt>



Testet, ob der Netzwerkdatenverkehr ein Loopbackdatenverkehr ohne App-Container ist.

> [!Note]  
> Nur auf Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ IST \_ RESERVIERT**
</dt> <dd> <dl> <dt>



Reserviert.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**\_ \_ FWP-BEDINGUNGSFLAG \_ WIRD RICHTLINIEN \_ \_ \_ AUTORISIERT.**
</dt> <dd> <dl> <dt>



Gibt an, dass die aktuelle Klassifizierung ausgeführt wird, um die Absicht einer umgeleiteten Windows Store App zum Herstellen einer Verbindung mit einem angegebenen Host zu erkennen. Eine solche Klassifizierung enthält dieselben klassifizierbaren Feldwerte, als ob die App nie umgeleitet würde. Das Flag gibt auch an, dass eine zukünftige Klassifizierung aufgerufen wird, um mit dem effektiven umgeleiteten Ziel übereinzuordnen. Wenn die App zur Überprüfung an einen Proxydienst umgeleitet wird, bedeutet dies auch, dass eine zukünftige Klassifizierung für die Proxyverbindung aufgerufen wird. Callout-Treiber sollten diese Klassifizierung im Allgemeinen zulassen.

> [!Note]  
> Nur auf Windows 8 und Windows Server 2012.

 

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Die folgenden Flags geben den Grund für die erneute Authentifizierung einer zuvor autorisierten Verbindung an. Diese Flags und die Filterebenen, in denen sie verwendet werden können, werden wie folgt definiert.

> [!Note]  
> Diese Filterbedingungen sind nur auf Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**ÄNDERUNG DER RICHTLINIE FÜR \_ \_ DIE ERNEUTE AUTHENTIFIZIERUNG DER FWP-BEDINGUNG \_ \_ \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung erneut autorisiert wurde, weil Filter hinzugefügt oder entfernt wurden.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**\_ \_ FWP-BEDINGUNG: NEUAUTORISIEREN DES \_ \_ GRUNDS FÜR \_ NEUE \_ ANKUNFTSSCHNITTSTELLE**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket von einer unbekannten Schnittstelle empfangen wurde.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**\_FWP-BEDINGUNG: GRUND NEU \_ \_ AUTORISIEREN \_ NEUE \_ NEXTHOP-SCHNITTSTELLE \_**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket von einer unbekannten Schnittstelle entfernt wird.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**\_FWP-BEDINGUNG: \_ ERNEUTES AUTORISIEREN DER \_ \_ \_ GRUNDPROFILÜBERQUERUNG**
</dt> <dd> <dl> <dt>



Gibt an, dass das Paket Schnittstellen von mehr als einer Netzwerkkategorie übergeben hat.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**\_FWP-BEDINGUNG: \_ NEUAUTORISIEREN DER \_ URSACHE \_ KLASSIFIZIEREN DER \_ VERVOLLSTÄNDIGUNG**
</dt> <dd> <dl> <dt>



Gibt an, dass eine zuvor gehaltene Verbindung jetzt abgeschlossen werden darf.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**GEÄNDERTE IPSEC-EIGENSCHAFTEN \_ DER FWP-BEDINGUNG \_ ZUM \_ \_ ERNEUTEN \_ AUTORISIEREN DER \_ URSACHE**
</dt> <dd> <dl> <dt>



Gibt an, dass sich die IPsec-Eigenschaften geändert haben oder dass die Verbindung von Klartext in eine sichere Verbindung geändert wurde.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**\_FWP-BEDINGUNG: URSACHE BEI DER \_ \_ \_ STREAMÜBERPRÜFUNG ERNEUT \_ \_ AUTORISIEREN**
</dt> <dd> <dl> <dt>



Gibt an, dass eine zuvor hergestellte TCP-Verbindung jetzt überprüft wird.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**GEÄNDERTE SOCKETEIGENSCHAFT FÜR DIE \_ \_ FWP-BEDINGUNG \_ "GRUND \_ NEU \_ \_ AUTORISIEREN"**
</dt> <dd> <dl> <dt>



Gibt an, dass Socketeigenschaften festgelegt wurden, nachdem eine Verbindung autorisiert und hergestellt wurde.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**\_ \_ FWP-BEDINGUNG: URSACHE FÜR NEUES \_ \_ \_ EINGEHENDES \_ \_ MCAST-BCAST-PAKET ERNEUT \_ AUTORISIEREN**
</dt> <dd> <dl> <dt>



Gibt an, dass neue eingehende Multicast- oder Broadcastpakete bei ALE \_ RECV \_ ACCEPT-Rückrufen erneut autorisiert werden.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Die folgenden Flags geben Socketeigenschaften an, die sich darauf bezieht, ob eine Anwendung Edge-Traversaldatenverkehr empfangen möchte. Diese Flags und die Filterebenen, in denen sie verwendet werden können, werden wie folgt definiert.

> [!Note]  
> Diese Filterbedingungen sind nur auf Windows Server 2008 R2, Windows 7 und höher verfügbar.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**\_ \_ FWP-BEDINGUNGSSOCKET-EIGENSCHAFTENFLAG \_ \_ IST \_ \_ \_ SYSTEMPORT-RPC \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die Anwendung mit einem dynamischen RPC-Port kommuniziert.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_ \_ FWP-BEDINGUNGSSOCKET-EIGENSCHAFTENFLAG \_ \_ \_ \_ \_ EDGEDATENVERKEHR ZULASSEN**
</dt> <dd> <dl> <dt>



Gibt an, dass die Anwendung edgedurchlaufspezifischen Datenverkehr empfangen möchte.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_ \_ FWP-BEDINGUNGSSOCKET-EIGENSCHAFTENFLAG \_ \_ \_ \_ \_ EDGEDATENVERKEHR VERWEIGERN**
</dt> <dd> <dl> <dt>



Gibt an, dass die Anwendung edgedurchlaufspezifischen Datenverkehr nicht empfangen oder verarbeiten möchte.

Filterebene:

-   FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Die folgenden Flags geben Verbindungsdetails im Zusammenhang mit der L2-Filterung an.

> [!Note]  
> Diese Filterbedingungen sind nur auf Windows 8 und Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP-BEDINGUNG \_ \_ L2 \_ IST \_ SYSTEMEIGENES \_ ETHERNET**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung systemeigenes Ethernet ist.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP-BEDINGUNG \_ \_ L2 \_ IS \_ WIFI**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung WLAN ist.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP-BEDINGUNG \_ \_ L2 \_ IST \_ MOBILES BREITBAND \_**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung ein mobiles Breitband ist.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP-BEDINGUNG \_ \_ \_ L2: DIREKTE \_ \_ \_ WLAN-DATEN**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung direkt Wi-Fi ist.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP-BEDINGUNG \_ \_ L2 \_ IST \_ VM2VM**
</dt> <dd> <dl> <dt>



Gibt an, dass die Verbindung zwischen virtuellen Computern besteht.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**\_FWP-BEDINGUNG \_ L2 \_ IST FALSCH \_ FORMATIERTES \_ PAKET**
</dt> <dd> <dl> <dt>



Gibt an, dass ein Paket anscheinend falsch formatiert ist.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP-BEDINGUNG \_ \_ L2 \_ IST \_ \_ IP-FRAGMENTGRUPPE \_**
</dt> <dd> <dl> <dt>



Gibt eine IP-Paketfragmentgruppe an.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP-BEDINGUNG \_ \_ L2, \_ FALLS CONNECTOR \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>



Gibt an, dass ein Connector vorhanden ist.

Filterebene:

-   EINGEHENDES \_ \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Fwptypes.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

