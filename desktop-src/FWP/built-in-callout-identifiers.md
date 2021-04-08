---
title: Integrierte Legenden Bezeichner ("f")
description: Die Bezeichner für die Legenden Funktionen, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt. Diese Bezeichner werden wie folgt definiert.
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
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957138"
---
# <a name="built-in-callout-identifiers"></a>Integrierte Legenden Bezeichner

Die Bezeichner für die Legenden Funktionen, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt. Diese Bezeichner werden wie folgt definiert.

Die v4-und V6-Suffixe am Ende der Legenden Bezeichner geben an, ob die Legende dem IPv4-Netzwerk Stapel oder dem IPv6-Netzwerk Stapel entspricht.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**Swpm \_ Callout \_ IPSec \_ Inbound \_ Transport \_ V4/swpm \_ Callout \_ IPSec \_ Inbound \_ Transport \_ V6** 
</dt> <dd> <dl> <dt>



Mit dieser Option wird überprüft, ob jedes empfangene Paket, das über eine Transportmodus-Sicherheits Zuordnung eingehen soll, sicher ankommt.

Diese Legende ist auf der Transportschicht anwendbar.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**WPM-Legende \_ \_ IPSec-ausgehende \_ \_ Transport \_ V4/f-Legende \_ IPSec-ausgehenden \_ \_ \_ Transport \_ V6** 
</dt> <dd> <dl> <dt>



Gibt IPSec den ausgehenden Datenverkehr an, der über Transportmodus-Sicherheits Zuordnungen geschützt werden muss.

Diese Legende ist auf der Transportschicht anwendbar.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**WPM-Legende \_ \_ IPSec \_ -Eingangs \_ Tunnel \_ V4/bwpm Legende \_ \_ IPSec- \_ Eingangs \_ Tunnel \_ V6** 
</dt> <dd> <dl> <dt>



Überprüft, ob jedes empfangene Paket, das über eine Tunnel Modus-Sicherheits Zuordnung eingehen soll, sicher eintrifft.

Diese Legende ist auf der Transportschicht anwendbar.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**WPM-Legenden \_ \_ -IPSec \_ -ausgehender \_ Tunnel \_ V4/f-Legende \_ \_ IPSec- \_ \_ Tunnel \_ V6** 
</dt> <dd> <dl> <dt>



Gibt IPSec den ausgehenden Datenverkehr an, der über Tunnel Modus-Sicherheits Zuordnungen geschützt werden muss.

Diese Legende ist auf der Transportschicht anwendbar.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**WPM-Legende \_ \_ IPSec \_ Forward \_ Inbound \_ Tunnel \_ V4/bwpm \_ Callout \_ IPSec \_ Forward \_ Inbound \_ Tunnel \_ V6**
</dt> <dd> <dl> <dt>



Überprüft, ob jedes empfangene Paket, das über eine Tunnel Modus-Sicherheits Zuordnung eingehen soll, sicher eintrifft.

Diese Legende ist auf der Weiterleitungs Ebene anwendbar.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**WPM-Legende \_ \_ IPSec \_ Forward \_ -ausgehender \_ Tunnel \_ V4/bwpm \_ Callout \_ IPSec \_ Forward \_ Outbound \_ Tunnel \_ V6**
</dt> <dd> <dl> <dt>



Gibt IPSec den ausgehenden Datenverkehr an, der über eine Tunnel Modus-Sicherheits Zuordnung geschützt werden muss.

Diese Legende ist auf der Weiterleitungs Ebene anwendbar.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**WPM \_ \_ -Legende IPSec eingehend \_ initiieren \_ von \_ Secure \_ V4/f-Legende \_ \_ IPSec eingehend \_ initiieren von \_ \_ Secure \_ V6** 
</dt> <dd> <dl> <dt>



Stellt sicher, dass jede eingehende Verbindung, die sicher eintreffen soll, sicher ankommt.

Diese Legende ist auf der Ebene der ALE-Annahme anwendbar.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**WPM \_ \_ -Legende IPSec \_ -eingehende \_ Tunnel \_ ALE \_ Annahme \_ V4/f-Legende \_ \_ IPSec- \_ eingehende \_ Tunnel \_ ALE \_ akzeptieren \_ V6**
</dt> <dd> <dl> <dt>



Ermöglicht die IP-in-IP-Pakete für den IPSec-Tunnel Modus, wenn diese auf der Ebene der ALE-Annahme klassifiziert werden.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**WPM-Legende \_ \_ IPSec \_ -ALE \_ Connect \_ V4/f-Legende \_ \_ IPSec \_ ALE \_ Verbindung \_ V6**
</dt> <dd> <dl> <dt>



Wendet IPSec-richtlinienmodifiziererer auf Client Anwendungen an.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**WPM-Legende \_ \_ IPSec \_ DoSP \_ Forward \_ V4/WPM \_ Callout \_ IPSec \_ DoSP \_ Forward \_ V6**
</dt> <dd> <dl> <dt>



Signalisiert dem IPSec-DOS-Schutz, dass der Datenverkehr auf potenzielle DOS überprüft werden muss und möglicherweise eine Raten Beschränkung erforderlich ist.

> [!Note]  
> Nur in Windows 7 und Windows Server 2008 R2 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**\_ \_ WPM-Legende WFP- \_ \_ Transportschicht \_ V4 \_ automatische \_ Drop/WPM-Legende \_ \_ WFP- \_ Transport \_ Schicht \_ V6 \_ Silent \_ Drop**
</dt> <dd> <dl> <dt>



Implementiert die Filterung im verborgenen Modus, indem alle eingehenden Pakete, für die TCP keinen Überwachungs Endpunkt hat, automatisch gelöscht werden.

Diese Legende gilt für die eingehende Transport Verwerfungs Schicht.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**WPM-Legende \_ von \_ TCP \_ Chimney \_ Connect \_ Layer \_ V4/f WPM \_ Callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Aktiviert oder deaktiviert die TCP-Chimney-Abladung für jede ausgehende Verbindung.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**F \_ -Callout \_ -TCP \_ \_ -Chimney \_ -Accept \_ -Ebene V4/f \_ \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Aktiviert oder deaktiviert die TCP-Chimney-Abladung für jede eingehende Verbindung.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**F & # # amp; \_ \_ querset \_ Optionen \_ auth \_ Connect \_ Layer \_ V4/f WPM \_ Callout \_ Set \_ options \_ auth \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Legt klassifiziereroptionen für ausgehende Flows fest.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**F-Legenden \_ \_ Satz \_ Optionen \_ auth \_ recv \_ Accept \_ Layer \_ V4/f WPM \_ Callout \_ Set \_ options \_ auth \_ recv \_ Accept \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Legt klassifiziereroptionen für eingehende Flows fest.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**Abrufbare Authentifizierung für die abrufbare Authentifizierung mit der BPM \_ \_ \_ \_ \_ \_ - \_ \_ \_ \_ \_ \_ Authentifizierung**
</dt> <dd> <dl> <dt>



Dieser Bezeichner ist für die interne Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**Der Edge-Over-over-over \_ \_ -down-Monitor \_ \_ \_ \_ v6/f- \_ \_ Legende Teredo- \_ ALE \_ lauscht \_ V6**
</dt> <dd> <dl> <dt>



Signalisiert dem Teredo-Dienst, dass eine Anwendung eine Teredo-Adresse benötigt.

> [!Note]  
> Verwenden Sie für Windows 7 und höher den Windows-Legenden Befehl Edge-out-over-over-Monitor **\_ \_ \_ \_ \_ \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**F WPM \_ -Legende \_ Edge \_ \_ \_ \_ -Ressourcenzuweisung \_ V6/swpm \_ \_ Legende Teredo \_ ALE- \_ Ressourcen \_ Zuweisung \_ V6**
</dt> <dd> <dl> <dt>



Signalisiert dem Teredo-Dienst, dass eine Anwendung eine Teredo-Adresse benötigt.

> [!Note]  
> Verwenden Sie für Windows 7 und höher die WPM-Legende " **\_ Edge- \_ \_ \_ \_ Ressourcen \_ Zuweisung \_ (Edge**)".

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**\_Swpm-Legende \_ Edge- \_ \_ \_ Ressourcen \_ Zuweisung \_ v4** 
</dt> <dd> <dl> <dt>



Dieser Bezeichner ist für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**\_Auschecken der \_ Edge- \_ \_ \_ Edgeausnahme \_**
</dt> <dd> <dl> <dt>



Dieser Bezeichner ist für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**WPM-Legende \_ von \_ TCP \_ \_ -Vorlagen Connect \_ Layer \_ V4/f-Legenden Verbindungs \_ \_ \_ \_ \_ Ebene \_ V6**
</dt> <dd> <dl> <dt>



Wendet TCP-Vorlagen Einstellungen für übereinstimmende ausgehende Verbindungen an.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**Von den WPM-Legenden in den \_ \_ TCP \_ \_ -Vorlagen accept \_ Layer \_ V4/f-Legende \_ TCP- \_ \_ Vorlagen \_ akzeptieren \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Wendet TCP-Vorlagen Einstellungen für eingehende Verbindungen an.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |



 

 





