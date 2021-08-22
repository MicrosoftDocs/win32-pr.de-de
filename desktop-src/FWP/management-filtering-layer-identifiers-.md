---
title: Filtern von Ebenenbezeichnern (Fwpmu.h)
description: WFP API Management filtert Ebenenbezeichnerkonstatoren.
ms.assetid: 3b2daef1-558b-4e3a-a98a-f4dfa80a29c0
topic_type:
- apiref
api_name:
- FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V6
- FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V6
- FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V6
- FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6_DISCARD
- FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V6
- FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6
- FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V6
- FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6_DISCARD
- FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V6
- FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD
- FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6
- FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6
- FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD
- FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V6
- FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD
- FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6
- FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD
- FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V6
- FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD
- FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6
- FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD
- FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET
- FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET
- FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE
- FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE
- FWPM_LAYER_INGRESS_VSWITCH_ETHERNET
- FWPM_LAYER_EGRESS_VSWITCH_ETHERNET
- FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6
- FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V6
- FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6
- FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6
- FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6
- FWPM_LAYER_RPC_UM
- FWPM_LAYER_RPC_EPMAP
- FWPM_LAYER_RPC_EP_ADD
- FWPM_LAYER_RPC_PROXY_CONN
- FWPM_LAYER_RPC_PROXY_IF
- FWPM_LAYER_KM_AUTHORIZATION
- FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6
- FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6
- FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6
- FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT_V6
- FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT_V6
- FWPM_LAYER_STREAM_PACKET_V4 / FWPM_LAYER_STREAM_PACKET_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d1d6d8e4987fd60d3b3ff0fea73c615f75444e76ed6ebdf3c95110564ef6c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068890"
---
# <a name="filtering-layer-identifiers"></a>Filtern von Ebenenbezeichnern

Die Windows-Ebenenbezeichner der Filterplattform (WFP) werden jeweils durch eine GUID dargestellt. Diese Bezeichner werden wie folgt definiert.

Die Suffixe V4 und V6 am Ende der Ebenenbezeichner geben an, ob sich die Ebene im IPv4-Netzwerkstapel oder im IPv6-Netzwerkstapel befindet.

<dl> <dt>

<span id="FWPM_LAYER_INBOUND_IPPACKET_V4___FWPM_LAYER_INBOUND_IPPACKET_V6"></span><span id="fwpm_layer_inbound_ippacket_v4___fwpm_layer_inbound_ippacket_v6"></span>**EINGEHENDES \_ \_ \_ IPPACKET \_ V4/EINGEHENDES \_ \_ \_ IPPACKET \_ V6 DER FWPM-SCHICHT**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad, direkt nachdem der IP-Header eines empfangenen Pakets analysiert wurde, aber bevor eine IP-Headerverarbeitung stattfindet. Es ist keine IPsec-Entschlüsselung oder -Neuassembly aufgetreten.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_inbound_ippacket_v4_discard___fwpm_layer_inbound_ippacket_v6_discard"></span>**FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4 \_ DISCARD/FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad, um alle empfangenen Pakete zu überprüfen, die auf der Netzwerkebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4___FWPM_LAYER_OUTBOUND_IPPACKET_V6"></span><span id="fwpm_layer_outbound_ippacket_v4___fwpm_layer_outbound_ippacket_v6"></span>**AUSGEHENDE \_ \_ \_ IPPACKET \_ V4-/FWPM-SCHICHT \_ \_ AUSGEHENDE \_ IPPACKET V6 DER FWPM-SCHICHT \_**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad, kurz bevor das gesendete Paket auf Fragmentierung ausgewertet wird. Die gesamte IP-Headerverarbeitung ist abgeschlossen, und alle Erweiterungsheader sind bereits enthalten. IPsec-Authentifizierung und -Verschlüsselung sind bereits erfolgt.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_outbound_ippacket_v4_discard___fwpm_layer_outbound_ippacket_v6_discard"></span>**FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4 \_ DISCARD/FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad, um alle gesendeten Pakete zu überprüfen, die auf der Netzwerkebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPFORWARD_V4___FWPM_LAYER_IPFORWARD_V6"></span><span id="fwpm_layer_ipforward_v4___fwpm_layer_ipforward_v6"></span>**FWPM \_ LAYER \_ IPFORWARD \_ V4/FWPM \_ LAYER \_ IPFORWARD \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Weiterleitungspfad an dem Punkt, an dem ein empfangenes Paket weitergeleitet wird.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPFORWARD_V4_DISCARD___FWPM_LAYER_IPFORWARD_V6_DISCARD"></span><span id="fwpm_layer_ipforward_v4_discard___fwpm_layer_ipforward_v6_discard"></span>**FWPM \_ LAYER \_ IPFORWARD \_ V4 \_ DISCARD/FWPM \_ LAYER \_ IPFORWARD \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Weiterleitungspfad, um weitergeleitete Pakete zu überprüfen, die auf der Weiterleitungsebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_TRANSPORT_V4___FWPM_LAYER_INBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_inbound_transport_v4___fwpm_layer_inbound_transport_v6"></span>**FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4/FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad, direkt nachdem der Transportheader eines empfangenen Pakets vom Netzwerkstapel auf der Transportebene analysiert wurde, aber bevor eine Transportschichtverarbeitung stattfindet.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_inbound_transport_v4_discard___fwpm_layer_inbound_transport_v6_discard"></span>**FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad, um alle empfangenen Pakete zu überprüfen, die auf der Transportebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4___FWPM_LAYER_OUTBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_outbound_transport_v4___fwpm_layer_outbound_transport_v6"></span>**FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V4/FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad, direkt nachdem ein gesendetes Paket zur Verarbeitung an die Netzwerkschicht übergeben wurde, aber bevor eine Verarbeitung auf Netzwerkebene stattfindet. Diese Filterebene befindet sich am oberen Rand der Netzwerkebene und nicht am unteren Rand der Transportschicht, sodass alle Pakete, die von Transporten von Drittanbietern oder als Rohpakete gesendet werden, auf dieser Ebene gefiltert werden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_outbound_transport_v4_discard___fwpm_layer_outbound_transport_v6_discard"></span>**FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad, um alle gesendeten Pakete zu überprüfen, die auf der Transportebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_STREAM_V4___FWPM_LAYER_STREAM_V6"></span><span id="fwpm_layer_stream_v4___fwpm_layer_stream_v6"></span>**FWPM \_ LAYER \_ STREAM \_ V4/FWPM \_ LAYER STREAM \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Datenstrompfad. Auf dieser Ebene können Netzwerkdaten pro Datenstrom überprüft werden. Auf der Streamebene sind die Netzwerkdaten bidirektional.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_STREAM_V4_DISCARD___FWPM_LAYER_STREAM_V6_DISCARD"></span><span id="fwpm_layer_stream_v4_discard___fwpm_layer_stream_v6_discard"></span>**FWPM \_ LAYER \_ STREAM \_ V4 \_ DISCARD/FWPM \_ LAYER STREAM \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Datenstrompfad zum Überprüfen von Datenstromdaten, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_DATAGRAM_DATA_V4___FWPM_LAYER_DATAGRAM_DATA_V6"></span><span id="fwpm_layer_datagram_data_v4___fwpm_layer_datagram_data_v6"></span>**\_DATAGRAMMDATEN DER FWPM-SCHICHT \_ \_ \_ V4/FWPM-SCHICHT \_ \_ DATAGRAM DATA \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Datagrammdatenpfad. Auf dieser Ebene können Netzwerkdaten pro Datagramm überprüft werden. Auf der Datagrammebene sind die Netzwerkdaten bidirektional.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD___FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD"></span><span id="fwpm_layer_datagram_data_v4_discard___fwpm_layer_datagram_data_v6_discard"></span>**FWPM \_ LAYER \_ DATAGRAM DATA \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ DATAGRAM DATA \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Datenpfad des Datagramms, um alle verworfenen Datagramme zu überprüfen.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4___FWPM_LAYER_INBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_inbound_icmp_error_v4___fwpm_layer_inbound_icmp_error_v6"></span>**FWPM \_ LAYER \_ INBOUND \_ ICMP ERROR \_ \_ V4/FWPM \_ LAYER \_ INBOUND \_ ICMP ERROR \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad zum Überprüfen empfangener ICMP-Fehlermeldungen für das Transportprotokoll.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_inbound_icmp_error_v4_discard___fwpm_layer_inbound_icmp_error_v6_discard"></span>**FWPM \_ LAYER \_ INBOUND \_ ICMP ERROR \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ INBOUND \_ ICMP ERROR \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad zum Überprüfen empfangener ICMP-Fehlermeldungen, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_outbound_icmp_error_v4___fwpm_layer_outbound_icmp_error_v6"></span>**FWPM \_ LAYER \_ OUTBOUND \_ ICMP ERROR \_ \_ V4/FWPM \_ LAYER \_ OUTBOUND \_ ICMP ERROR \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad zum Überprüfen empfangener ICMP-Fehlermeldungen für das Transportprotokoll.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_outbound_icmp_error_v4_discard___fwpm_layer_outbound_icmp_error_v6_discard"></span>**FWPM \_ LAYER \_ OUTBOUND \_ ICMP ERROR \_ \_ V4 DISCARD \_ /FWPM \_ LAYER \_ OUTBOUND \_ ICMP ERROR \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad zum Überprüfen empfangener ICMP-Fehlermeldungen, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_layer_ale_resource_assignment_v4___fwpm_layer_ale_resource_assignment_v6"></span>**RESSOURCENZUWEISUNG DER \_ FWPM-SCHICHT \_ \_ \_ \_ ALE V4/FWPM-SCHICHT \_ \_ \_ ALE-RESSOURCENZUWEISUNG \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Autorisierung von Transportportzuweisungen, Bindungsanforderungen, Anforderungen im promiscuous-Modus und Anforderungen im Rohmodus.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD"></span><span id="fwpm_layer_ale_resource_assignment_v4_discard___fwpm_layer_ale_resource_assignment_v6_discard"></span>**FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung der folgenden verworfenen Elemente: Transportportzuweisungen, Bindungsanforderungen, Anforderungen im promiscuous-Modus und Anforderungen im Rohmodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4___FWPM_LAYER_ALE_AUTH_LISTEN_V6"></span><span id="fwpm_layer_ale_auth_listen_v4___fwpm_layer_ale_auth_listen_v6"></span>**FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V4/FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht das Autorisieren von TCP-Lauschenanforderungen.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD___FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_listen_v4_discard___fwpm_layer_ale_auth_listen_v6_discard"></span>**FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung von TCP-Lauschenanforderungen, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6"></span><span id="fwpm_layer_ale_auth_recv_accept_v4___fwpm_layer_ale_auth_recv_accept_v6"></span>**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V4/FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht das Autorisieren von Annahmeanforderungen für eingehende TCP-Verbindungen sowie das Autorisieren von eingehendem Nicht-TCP-Datenverkehr basierend auf dem ersten empfangenen Paket.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_recv_accept_v4_discard___fwpm_layer_ale_auth_recv_accept_v6_discard"></span>**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V4 DISCARD \_ /FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung von Accept-Anforderungen für eingehende TCP-Verbindungen, die verworfen wurden, sowie die Überprüfung von Autorisierungen für eingehenden Nicht-TCP-Datenverkehr, der verworfen wurde.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4___FWPM_LAYER_ALE_AUTH_CONNECT_V6"></span><span id="fwpm_layer_ale_auth_connect_v4___fwpm_layer_ale_auth_connect_v6"></span>**FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V4/FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht das Autorisieren von Verbindungsanforderungen für ausgehende TCP-Verbindungen sowie das Autorisieren von ausgehenden Nicht-TCP-Datenverkehr basierend auf dem ersten gesendeten Paket.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_connect_v4_discard___fwpm_layer_ale_auth_connect_v6_discard"></span>**FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Untersuchung von Verbindungsanforderungen für ausgehende TCP-Verbindungen, die verworfen wurden, sowie die Überprüfung von Autorisierungen für ausgehenden Nicht-TCP-Datenverkehr, der verworfen wurde.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6"></span><span id="fwpm_layer_ale_flow_established_v4___fwpm_layer_ale_flow_established_v6"></span>**FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V4/FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Benachrichtigung, wenn eine TCP-Verbindung hergestellt wurde oder wenn Nicht-TCP-Datenverkehr autorisiert wurde.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD"></span><span id="fwpm_layer_ale_flow_established_v4_discard___fwpm_layer_ale_flow_established_v6_discard"></span>**FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V4 \_ DISCARD/FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V6 \_ DISCARD**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung, wann eine hergestellte TCP-Verbindung auf der eingerichteten Datenflussebene verworfen wurde und wenn autorisierter Nicht-TCP-Datenverkehr auf der eingerichteten Flussebene verworfen wurde.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_inbound_mac_frame_ethernet"></span>**EINGEHENDES \_ MAC-FRAME-ETHERNET AUF FWPM-EBENE \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad, nachdem die Verarbeitung der MAC-Schicht (802.3) erfolgt ist, aber bevor der Frame von der Rahmenebene verarbeitet wird. Dies ist die Ebene nach der systemeigenen , in der alle Frames wie Ethernetframes aussehen.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_outbound_mac_frame_ethernet"></span>**FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ ETHERNET**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad, nachdem die Verarbeitung der Rahmenebene erfolgt ist, aber bevor der Frame von der MAC-Ebene (802.3) verarbeitet wird. Dies ist die Ebene nach der systemeigenen , in der alle Frames wie Ethernetframes aussehen.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_inbound_mac_frame_native"></span>**FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Empfangspfad, nachdem die VERARBEITUNG der MAC-Ebene erfolgt ist, aber bevor der Frame von der Rahmenebene verarbeitet wird. Dies ist die erste Ebene, nachdem der Miniport den Frame an NDIS übergibt.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_outbound_mac_frame_native"></span>**FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im Sendepfad, nachdem die Verarbeitung der Rahmenebene erfolgt ist, aber bevor der Frame von der MAC-Ebene (Native 802.11) verarbeitet wird. Dies ist die erste Ebene, nachdem der Miniport den Frame an NDIS übergibt.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_ingress_vswitch_ethernet"></span>**FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ ETHERNET**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im vSwitch-Ingress-Pfad, direkt nachdem der MAC-Header analysiert wurde, aber bevor eine MAC-Headerverarbeitung stattfindet.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_EGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_egress_vswitch_ethernet"></span>**AUSGEHENDES \_ \_ \_ VSWITCH-ETHERNET AUF FWPM-EBENE \_**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im ausgehenden vSwitch-Pfad, direkt nachdem der MAC-Header analysiert wurde, aber bevor eine MAC-Headerverarbeitung stattfindet.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_ingress_vswitch_transport_v4___fwpm_layer_ingress_vswitch_transport_v6"></span>**FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ TRANSPORT \_ V4/FWPM \_ LAYER \_ INGRESS \_ VSWITCH \_ TRANSPORT \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im vSwitch-Ingress-Pfad, direkt nachdem der MAC-Header analysiert wurde, aber bevor eine MAC-Headerverarbeitung stattfindet. Diese Ebene ermöglicht Filterbedingungen auf TRANSPORT-Ebene, um das Filtern des Datenverkehrs zu verbessern.

Wenn sich ein vSwitchPort im PVLAN- oder Trunkmodus befindet, werden Filter auf dieser Ebene umgangen, damit der Datenverkehr ohne Filterung fließen kann.

Wenn IPv4 auf dem Host deinstalliert wird, führen Filter auf dieser Ebene dazu, dass Pakete gelöscht werden.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_egress_vswitch_transport_v4___fwpm_layer_egress_vswitch_transport_v6"></span>**FWPM \_ LAYER \_ EGRESS \_ VSWITCH \_ TRANSPORT \_ V4/FWPM \_ LAYER \_ EGRESS \_ VSWITCH \_ TRANSPORT \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene befindet sich im ausgehenden vSwitch-Pfad, direkt nachdem der MAC-Header analysiert wurde, aber bevor eine MAC-Headerverarbeitung stattfindet. Diese Ebene ermöglicht Filterbedingungen auf TRANSPORT-Ebene, um das Filtern des Datenverkehrs zu verbessern.

Wenn sich ein vSwitchPort im PVLAN- oder Trunkmodus befindet, werden Filter auf dieser Ebene umgangen, damit der Datenverkehr ohne Filterung fließen kann.

Wenn IPv4 auf dem Host deinstalliert wird, führen Filter auf dieser Ebene dazu, dass Pakete gelöscht werden.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPSEC_KM_DEMUX_V4___FWPM_LAYER_IPSEC_KM_DEMUX_V6"></span><span id="fwpm_layer_ipsec_km_demux_v4___fwpm_layer_ipsec_km_demux_v6"></span>**FWPM \_ LAYER \_ IPSEC KM \_ \_ DEMUX \_ V4/FWPM \_ LAYER \_ IPSEC KM \_ \_ DEMUX \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene wird verwendet, um zu bestimmen, welche Schlüsselmodulen aufgerufen werden, wenn das lokale System der Initiator ist. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPSEC_V4___FWPM_LAYER_IPSEC_V6"></span><span id="fwpm_layer_ipsec_v4___fwpm_layer_ipsec_v6"></span>**FWPM \_ LAYER \_ IPSEC \_ V4/FWPM \_ LAYER \_ IPSEC \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht es dem Schlüsselmodul, Beim Aushandeln von Sicherheitszuordnungen im Schnellmodus Richtlinieninformationen im Schnellmodus zu suchen. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IKEEXT_V4___FWPM_LAYER_IKEEXT_V6"></span><span id="fwpm_layer_ikeext_v4___fwpm_layer_ikeext_v6"></span>**FWPM \_ LAYER \_ IKEEXT \_ V4/FWPM \_ LAYER \_ IKEEXT \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht es den IKE- und authentifizierten IP-Modulen, beim Aushandeln von Sicherheitszuordnungen im Hauptmodus Richtlinieninformationen im Hauptmodus zu suchen. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_UM"></span><span id="fwpm_layer_rpc_um"></span>**RPC-UM \_ AUF FWPM-EBENE \_ \_**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung der RPC-Datenfelder, die im Benutzermodus verfügbar sind. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_EPMAP"></span><span id="fwpm_layer_rpc_epmap"></span>**\_RPC-EPMAP DER FWPM-EBENE \_ \_**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung der RPC-Datenfelder, die während der Endpunktauflösung im Benutzermodus verfügbar sind. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_EP_ADD"></span><span id="fwpm_layer_rpc_ep_add"></span>**RPC-EP-ADD \_ AUF FWPM-EBENE \_ \_ \_**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung der RPC-Datenfelder, die im Benutzermodus verfügbar sind, wenn ein neuer Endpunkt hinzugefügt wird. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_PROXY_CONN"></span><span id="fwpm_layer_rpc_proxy_conn"></span>**RPC-PROXYKONN AUF FWPM-EBENE \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung der RpcProxy-Verbindungsanforderungen. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_PROXY_IF"></span><span id="fwpm_layer_rpc_proxy_if"></span>**RPC-PROXY \_ AUF FWPM-EBENE, \_ \_ \_ WENN**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung der Schnittstelle, die für RpcProxy-Verbindungen verwendet wird. Dies ist eine Filterebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_KM_AUTHORIZATION"></span><span id="fwpm_layer_km_authorization"></span>**KM-AUTORISIERUNG \_ AUF FWPM-EBENE \_ \_**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Autorisierung der Einrichtung von Sicherheitsverbunden.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_NAME_RESOLUTION_CACHE_V4___FWPM_LAYER_NAME_RESOLUTION_CACHE_V6"></span><span id="fwpm_layer_name_resolution_cache_v4___fwpm_layer_name_resolution_cache_v6"></span>**FWPM \_ LAYER NAME RESOLUTION CACHE \_ \_ \_ \_ V4/FWPM \_ LAYER NAME RESOLUTION CACHE \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht das Abfragen der Namen, die vor Kurzem vom System aufgelöst wurden.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_RESOURCE_RELEASE_V4___FWPM_LAYER_ALE_RESOURCE_RELEASE_V6"></span><span id="fwpm_layer_ale_resource_release_v4___fwpm_layer_ale_resource_release_v6"></span>**FWPM \_ LAYER \_ ALE RESOURCE RELEASE \_ \_ \_ V4/FWPM \_ LAYER \_ ALE RESOURCE RELEASE \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Mit dieser Filterebene können ressourcen, die zuvor zugeordnet wurden, freigegeben werden.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4___FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6"></span><span id="fwpm_layer_ale_endpoint_closure_v4___fwpm_layer_ale_endpoint_closure_v6"></span>**FWPM \_ LAYER \_ ALE ENDPOINT CLOSURE \_ \_ \_ V4/FWPM \_ LAYER \_ ALE ENDPOINT CLOSURE \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Nachverfolgung der Deaktivierung der Aktivierung verbundener TCP-Datenflüsse oder UDP-Sockets.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_CONNECT_REDIRECT_V4___FWPM_LAYER_ALE_CONNECT_REDIRECT_V6"></span><span id="fwpm_layer_ale_connect_redirect_v4___fwpm_layer_ale_connect_redirect_v6"></span>**FWPM \_ LAYER \_ ALE CONNECT REDIRECT \_ \_ \_ V4/FWPM \_ LAYER \_ ALE CONNECT REDIRECT \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Änderung von Adressen und Ports auf der \_ Bindungsumleitungsebene.

Für TCP können die lokale Adresse und/oder der lokale Port sowie die Remoteadresse und/oder der Remoteport geändert werden.

Für UDP kann die lokale Adresse und/oder der lokale Port geändert werden.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_BIND_REDIRECT_V4___FWPM_LAYER_ALE_BIND_REDIRECT_V6"></span><span id="fwpm_layer_ale_bind_redirect_v4___fwpm_layer_ale_bind_redirect_v6"></span>**FWPM \_ LAYER \_ ALE BIND REDIRECT \_ \_ \_ V4/FWPM \_ LAYER \_ ALE BIND REDIRECT \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Änderung von bind()- und connect()-Aufrufen sowie die Auswahl von Hostrouten.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_STREAM_PACKET_V4___FWPM_LAYER_STREAM_PACKET_V6"></span><span id="fwpm_layer_stream_packet_v4___fwpm_layer_stream_packet_v6"></span>**FWPM \_ LAYER STREAM PACKET \_ \_ \_ V4/FWPM \_ LAYER STREAM PACKET \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filterebene ermöglicht die Überprüfung von TCP-Paketen, einschließlich Handshake- und Flusssteuerungsaustausch.

Weitere [Informationen finden Sie unter ALE-Ebenen.](ale-layers.md)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Filterebenenbezeichner werden auch als Bezeichner der Verwaltungsfilterebene bezeichnet. Die WFP-API enthält auch eine Reihe von [Laufzeitfilterebenenbezeichnern,](/windows-hardware/drivers/network/management-filtering-layer-identifiers)die im Windows Driver Kit (WDK) dokumentiert sind. Laufzeitfilterebenenbezeichner sind LUIDs und daher kleiner, nur 64 Bit groß, im Vergleich zu den Bezeichnern der Verwaltungsfilterebene mit einer Größe von 128 Bits.

Bezeichner der Verwaltungsfilterebene und Laufzeitfilterebenenbezeichner zeigen auf die gleichen Ebenen.

Bezeichner der Verwaltungsfilterebene werden von Funktionen verwendet, die entweder über den Benutzermodus oder den Kernelmodus (z. B. [**FwpmFilterAdd0)**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)mit der Basisfilter-Engine (BFE) interagieren.

Laufzeitfilterebenenbezeichner werden von Funktionen verwendet, die nur aus dem Kernelmodus mit der Filter-Engine interagieren (z. B. [FwpsFlowAssociateContext0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsflowassociatecontext0), [FwpsStreamInjectAsync0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsstreaminjectasync0)) und in Datenstrukturen, die direkt aus dem Kernel stammen (z. B. [**FWPM \_ NET EVENT CLASSIFY \_ \_ \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ALE-Ebenen](ale-layers.md)
</dt> <dt>

[WFP-Architektur](windows-filtering-platform-architecture-overview.md)
</dt> </dl>

