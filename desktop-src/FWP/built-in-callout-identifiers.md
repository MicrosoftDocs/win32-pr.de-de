---
title: Integrierte Aufrufbezeichner (Fwpmu.h)
description: Die Bezeichner für die Calloutfunktionen, die in die Windows Filterplattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt. Diese Bezeichner werden wie folgt definiert.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d430f44e6e72f575d5e2ff0fd30681c04e81892f0438f0508be994d53c1643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151426"
---
# <a name="built-in-callout-identifiers"></a>Integrierte Aufrufbezeichner

Die Bezeichner für die Calloutfunktionen, die in die Windows Filterplattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt. Diese Bezeichner werden wie folgt definiert.

Die Suffixe V4 und V6 am Ende der Aufrufbezeichner geben an, ob die Aufrufliste für den IPv4-Netzwerkstapel oder für den IPv6-Netzwerkstapel gilt.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V6** 
</dt> <dd> <dl> <dt>



Überprüft, ob jedes empfangene Paket, das über eine Transportmodus-Sicherheitszuordnung empfangen werden soll, sicher eintrifft.

Diese Aufrufe gelten für die Transportebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TRANSPORT \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V6** 
</dt> <dd> <dl> <dt>



Gibt IPsec den ausgehenden Datenverkehr an, der über Sicherheitszuordnungen des Transportmodus gesichert werden muss.

Diese Aufrufe gelten für die Transportebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TUNNEL \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TUNNEL \_ \_ V6** 
</dt> <dd> <dl> <dt>



Überprüft, ob jedes empfangene Paket, das über eine Tunnelmodus-Sicherheitszuordnung empfangen werden soll, sicher eintrifft.

Diese Aufrufe gelten für die Transportebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TUNNEL \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TUNNEL \_ \_ V6** 
</dt> <dd> <dl> <dt>



Gibt an, dass der ausgehende Datenverkehr, der über Tunnelmodus-Sicherheitszuordnungen geschützt werden muss, IPsec anzeigt.

Diese Aufrufe gelten für die Transportebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD \_ INBOUND TUNNEL \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC FORWARD \_ \_ INBOUND TUNNEL \_ \_ V6**
</dt> <dd> <dl> <dt>



Überprüft, ob jedes empfangene Paket, das über eine Tunnelmodus-Sicherheitszuordnung empfangen werden soll, sicher eintrifft.

Diese Aufrufe gelten für die Weiterleitungsebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD \_ OUTBOUND TUNNEL \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC FORWARD \_ \_ OUTBOUND TUNNEL \_ \_ V6**
</dt> <dd> <dl> <dt>



Gibt an, dass für IPsec der ausgehende Datenverkehr angegeben wird, der über eine Sicherheitszuordnung im Tunnelmodus gesichert werden muss.

Diese Aufrufe gelten für die Weiterleitungsebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ INITIATE SECURE \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND INITIATE SECURE \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Überprüft, ob jede eingehende Verbindung, die sicher empfangen werden soll, sicher eintrifft.

Diese Aufrufe gelten für die ALE-Accept-Ebene.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TUNNEL \_ ALE ACCEPT \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TUNNEL \_ \_ ALE ACCEPT \_ \_ V6**
</dt> <dd> <dl> <dt>



Lässt ip-in-IP-Pakete im IPsec-Tunnelmodus zu, wenn sie auf der ALE-Accept-Ebene klassifiziert werden.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ ALE \_ CONNECT \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ ALE CONNECT \_ \_ V6**
</dt> <dd> <dl> <dt>



Wendet IPsec-Richtlinienmodifizierer auf Clientanwendungen an.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ DOSP \_ FORWARD \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ DOSP FORWARD \_ \_ V6**
</dt> <dd> <dl> <dt>



Signalisiert IPsec DoS Protection, dass der Datenverkehr auf potenzielle DoS überprüft werden muss und möglicherweise eingeschränkt werden muss.

> [!Note]  
> Nur in Windows 7 und Windows Server 2008 R2 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ CALLOUT \_ WFP \_ TRANSPORT LAYER \_ \_ V4 SILENT DROP \_ \_ /FWPM \_ CALLOUT \_ WFP TRANSPORT LAYER \_ \_ \_ V6 SILENT \_ \_ DROP**
</dt> <dd> <dl> <dt>



Implementiert die Filterung im geschütztem Modus, indem alle eingehenden Pakete, für die TCP keinen lauschenden Endpunkt hat, im Hintergrund gelöscht werden.

Diese Aufrufe gelten für die Ebene für eingehende Transportrückwürfe.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP \_ ÄHLNEY \_ CONNECT LAYER \_ \_ V4/FWPM \_ CALLOUT TCP \_ \_ ÄHLNEY \_ CONNECT LAYER \_ \_ V6**
</dt> <dd> <dl> <dt>



Aktiviert oder deaktiviert die TCP-Auslagerung für jede ausgehende Verbindung.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP \_ SPRECHWEISE \_ ANNEHMEN DER EBENE \_ \_ V4/FWPM-CALLOUT \_ \_ \_ TCP-CHORNEY \_ AKZEPTIEREN EBENE \_ \_ V6**
</dt> <dd> <dl> <dt>



Aktiviert oder deaktiviert die TCP-Auslagerung für jede eingehende Verbindung.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH CONNECT LAYER \_ \_ \_ V4/FWPM \_ CALLOUT SET OPTIONS \_ \_ \_ AUTH CONNECT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Legt Klassifikationsoptionen für ausgehende Datenflüsse fest.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH \_ RECV ACCEPT LAYER \_ \_ \_ V4/FWPM \_ CALLOUT SET OPTIONS \_ \_ \_ AUTH \_ RECV ACCEPT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Legt Klassifikationsoptionen für eingehende Datenflüsse fest.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ RESERVED \_ AUTH CONNECT LAYER \_ \_ \_ V4/FWPM \_ CALLOUT RESERVED \_ \_ AUTH CONNECT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Dieser Bezeichner ist für die interne Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE LISTEN \_ \_ V6/FWPM \_ CALLOUT \_ TEREDO \_ ALE LISTEN \_ \_ V6**
</dt> <dd> <dl> <dt>



Signalisiert dem Teredo-Dienst, dass eine Anwendung eine Teredo-Adresse erfordert.

> [!Note]  
> Verwenden Sie für Windows 7 und höher **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V6/FWPM \_ CALLOUT \_ TEREDO \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Signalisiert dem Teredo-Dienst, dass eine Anwendung eine Teredo-Adresse erfordert.

> [!Note]  
> Verwenden Sie für Windows 7 und höher **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ RESOURCE \_ ASSIGNMENT \_ V4** 
</dt> <dd> <dl> <dt>



Dieser Bezeichner ist für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V4**
</dt> <dd> <dl> <dt>



Dieser Bezeichner ist für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP TEMPLATES CONNECT LAYER \_ \_ \_ \_ V4/FWPM \_ CALLOUT TCP TEMPLATES CONNECT \_ LAYER \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Wendet TCP-Vorlageneinstellungen für den Abgleich ausgehender Verbindungen an.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**TCP-VORLAGEN FÜR \_ FWPM-AUFRUFE \_ AKZEPTIEREN \_ EBENE \_ \_ \_ V4/FWPM-RÜCKRUF \_ \_ \_ TCP-VORLAGEN \_ AKZEPTIEREN EBENE \_ \_ V6**
</dt> <dd> <dl> <dt>



Wendet TCP-Vorlageneinstellungen für den Abgleich eingehender Verbindungen an.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





