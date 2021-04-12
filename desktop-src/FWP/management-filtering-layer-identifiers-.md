---
title: Filtern von ebenenbezeichgern ("f")
description: WFP API Management filtert ebenenbezeichnerkonstanten.
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
ms.openlocfilehash: 7766a147939b107ab173d927d90019c23cc6efb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105441"
---
# <a name="filtering-layer-identifiers"></a>Filtern von ebenenbezeichgern

Die ebenenids der Windows-Filter Plattform (WFP) werden jeweils durch eine GUID dargestellt. Diese Bezeichner werden wie folgt definiert.

Die v4-und V6-Suffixe am Ende der ebenenids geben an, ob sich die Ebene im IPv4-Netzwerk Stapel oder im IPv6-Netzwerk Stapel befindet.

<dl> <dt>

<span id="FWPM_LAYER_INBOUND_IPPACKET_V4___FWPM_LAYER_INBOUND_IPPACKET_V6"></span><span id="fwpm_layer_inbound_ippacket_v4___fwpm_layer_inbound_ippacket_v6"></span>**WPM- \_ Schicht \_ eingehender \_ ippacket \_ V4/bwpm- \_ Schicht \_ eingehender \_ ippacket \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad, wenn der IP-Header eines empfangenen Pakets analysiert wurde, aber bevor eine IP-Header Verarbeitung stattfindet. Es ist keine IPSec-Entschlüsselung oder-Neuzuweisung aufgetreten.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_inbound_ippacket_v4_discard___fwpm_layer_inbound_ippacket_v6_discard"></span>**WPM \_ -Schicht \_ eingehender \_ ippacket \_ V4 \_ verwerfen/bwpm- \_ Schicht \_ eingehender \_ ippacket \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener Pakete, die auf der Netzwerkebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4___FWPM_LAYER_OUTBOUND_IPPACKET_V6"></span><span id="fwpm_layer_outbound_ippacket_v4___fwpm_layer_outbound_ippacket_v6"></span>**WPM- \_ Ebene ausgehend von \_ \_ ippacket \_ V4/bwpm- \_ Schicht ausgehende \_ \_ ippacket \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Sende Pfad, kurz bevor das gesendete Paket für die Fragmentierung ausgewertet wird. Die gesamte IP-Header Verarbeitung ist vollständig, und alle Erweiterungs Header sind vorhanden. Alle IPSec-Authentifizierung und-Verschlüsselung sind bereits aufgetreten.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_outbound_ippacket_v4_discard___fwpm_layer_outbound_ippacket_v6_discard"></span>**WPM- \_ Ebene ausgehend von \_ \_ ippacket \_ V4 \_ verwerfen/WPM- \_ Schicht \_ ausgehende \_ ippacket \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im sendepfad zum Überprüfen aller gesendeten Pakete, die auf der Netzwerkebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPFORWARD_V4___FWPM_LAYER_IPFORWARD_V6"></span><span id="fwpm_layer_ipforward_v4___fwpm_layer_ipforward_v6"></span>**WPM \_ -Schicht \_ ipforward \_ V4/bwpm- \_ Schicht \_ ipforward \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Weiterleitungs Pfad an dem Punkt, an dem ein empfangenes Paket weitergeleitet wird.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPFORWARD_V4_DISCARD___FWPM_LAYER_IPFORWARD_V6_DISCARD"></span><span id="fwpm_layer_ipforward_v4_discard___fwpm_layer_ipforward_v6_discard"></span>**WPM \_ -Schicht \_ ipforward \_ V4 \_ Verwerfungs-/WPM- \_ Schicht- \_ ipforward \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Weiterleitungs Pfad zum Überprüfen von weitergeleiteten Paketen, die auf der Weiterleitungs Ebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_TRANSPORT_V4___FWPM_LAYER_INBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_inbound_transport_v4___fwpm_layer_inbound_transport_v6"></span>**WPM \_ -Schicht \_ eingehender \_ Transport \_ V4/bwpm- \_ Schicht \_ eingehender \_ Transport \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad, unmittelbar nachdem der Transport Header eines empfangenen Pakets vom Netzwerk Stapel auf der Transport Ebene analysiert wurde, jedoch bevor die Verarbeitung der Transportschicht erfolgt ist.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_inbound_transport_v4_discard___fwpm_layer_inbound_transport_v6_discard"></span>**WPM \_ -Schicht \_ eingehender \_ Transport \_ V4 \_ verwerfen/WPM- \_ Schicht \_ eingehender \_ Transport \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener Pakete, die auf der Transport Ebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4___FWPM_LAYER_OUTBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_outbound_transport_v4___fwpm_layer_outbound_transport_v6"></span>**Ausgehender Transport der WPM-Schicht für ausgehenden \_ \_ \_ Transport \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im sendepfad, wenn ein gesendetes Paket zur Verarbeitung an die Netzwerkschicht, aber erst nach der Verarbeitung der Netzwerkschicht an die Netzwerkschicht übermittelt wurde. Diese Filter Ebene befindet sich am oberen Rand der Netzwerkschicht anstatt am unteren Rand der Transport Ebene, sodass alle Pakete, die von Drittanbietern oder als unformatierte Pakete gesendet werden, auf dieser Ebene gefiltert werden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_outbound_transport_v4_discard___fwpm_layer_outbound_transport_v6_discard"></span>**Ausgehender Transport der WPM \_ -Schicht, \_ \_ \_ V4 \_ verwerfen/WPM- \_ Schicht- \_ \_ Transport \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im sendepfad zum Überprüfen aller gesendeten Pakete, die auf der Transport Ebene verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_STREAM_V4___FWPM_LAYER_STREAM_V6"></span><span id="fwpm_layer_stream_v4___fwpm_layer_stream_v6"></span>**BPM \_ -Layer \_ \_ -Stream V4/bwpm- \_ \_ ebenenstream \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Stream-Daten Pfad. Diese Ebene ermöglicht die Untersuchung von Netzwerkdaten pro Datenstrom. Auf der streamschicht sind die Netzwerkdaten bidirektional.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_STREAM_V4_DISCARD___FWPM_LAYER_STREAM_V6_DISCARD"></span><span id="fwpm_layer_stream_v4_discard___fwpm_layer_stream_v6_discard"></span>**BPM \_ -Layer \_ \_ -Stream \_ V4 verwerfen/WPM \_ - \_ ebenenstream \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Stream-Daten Pfad zum Überprüfen von Datenstrom Daten, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_DATAGRAM_DATA_V4___FWPM_LAYER_DATAGRAM_DATA_V6"></span><span id="fwpm_layer_datagram_data_v4___fwpm_layer_datagram_data_v6"></span>**\_ \_ Datagramm-Datagramm-Daten (Datagramm) der WPM \_ \_ - \_ \_ \_ \_ Ebene**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Datagramm-Datenpfad. Diese Ebene ermöglicht die Untersuchung von Netzwerkdaten pro Datagramm-Basis. Die Netzwerkdaten auf der datagrammebene sind bidirektional.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD___FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD"></span><span id="fwpm_layer_datagram_data_v4_discard___fwpm_layer_datagram_data_v6_discard"></span>**\_ \_ Datagramm-Datagramm \_ \_ \_ - \_ \_ \_ \_ Datagrammdaten \_**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Datagramm-Datenpfad zum Überprüfen von Datagrammen, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4___FWPM_LAYER_INBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_inbound_icmp_error_v4___fwpm_layer_inbound_icmp_error_v6"></span>**WPM- \_ Schicht \_ eingehender \_ ICMP \_ \_ -Fehler V4/WPM- \_ Schicht \_ eingehender \_ ICMP- \_ Fehler \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener ICMP-Fehlermeldungen für das Transportprotokoll.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_inbound_icmp_error_v4_discard___fwpm_layer_inbound_icmp_error_v6_discard"></span>**WPM \_ -Schicht \_ eingehender \_ ICMP \_ \_ -Fehler V4 \_ verwerfen/WPM- \_ Schicht \_ eingehender \_ ICMP- \_ Fehler \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener ICMP-Fehlermeldungen, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_outbound_icmp_error_v4___fwpm_layer_outbound_icmp_error_v6"></span>**\_ \_ Ausgehender \_ ICMP \_ \_ -Fehler V4/WPM-Layer-ausgehende \_ \_ \_ ICMP- \_ Fehler \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im sendepfad zum Überprüfen empfangener ICMP-Fehlermeldungen für das Transportprotokoll.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_outbound_icmp_error_v4_discard___fwpm_layer_outbound_icmp_error_v6_discard"></span>**\_ \_ Ausgehender \_ ICMP \_ \_ -Fehler V4 \_ verwerfen/WPM-Ebene Ausgeh \_ Ende \_ \_ ICMP- \_ Fehler \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im sendepfad zum Überprüfen empfangener ICMP-Fehlermeldungen, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_layer_ale_resource_assignment_v4___fwpm_layer_ale_resource_assignment_v6"></span>**F/a \_ -Ebene der \_ \_ Ressourcen \_ Zuweisung \_ V4/bwpm \_ Schicht- \_ \_ Ressourcen \_ Zuweisung \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das autorialisieren von Transport Port Zuweisungen, Bindungs Anforderungen, Anforderungen im Anforderungs Modus und Anforderungen im RAW-Modus.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD"></span><span id="fwpm_layer_ale_resource_assignment_v4_discard___fwpm_layer_ale_resource_assignment_v6_discard"></span>**F-Ressourcenzuweisung der swpm \_ -Schicht, \_ \_ \_ \_ V4 \_ verwerfen/swpm \_ Schicht- \_ \_ Ressourcen \_ Zuweisung \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das Überprüfen der folgenden verworfenen Elemente: Transport Port Zuweisungen, Bindungs Anforderungen, Anforderungen im Anforderungs Modus und Anforderungen im RAW-Modus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4___FWPM_LAYER_ALE_AUTH_LISTEN_V6"></span><span id="fwpm_layer_ale_auth_listen_v4___fwpm_layer_ale_auth_listen_v6"></span>**Lwpm \_ Layer \_ ALE \_ auth \_ hört \_ V4/bwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das autorialisieren von TCP-lausch Anforderungen.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD___FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_listen_v4_discard___fwpm_layer_ale_auth_listen_v6_discard"></span>**BPM \_ -Layer \_ \_ -der-Authentifizierung \_ hört \_ V4 \_ -Verwerfungs-/BB-ebenenauthentifizierung \_ \_ \_ \_ \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Untersuchung von TCP-lausch Anforderungen, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6"></span><span id="fwpm_layer_ale_auth_recv_accept_v4___fwpm_layer_ale_auth_recv_accept_v6"></span>**BPM \_ -Schicht \_ \_ -e \_ -v akzeptieren Version \_ \_ V4/bwpm \_ Schicht \_ ALE Authentifizierung \_ \_ \_ akzeptieren \_**
</dt> <dd> <dl> <dt>



Diese Filterungs Ebene ermöglicht das autorialisieren von Accept-Anforderungen für eingehende TCP-Verbindungen sowie das Autorisierungs eingehender nicht-TCP-Datenverkehr basierend auf dem ersten empfangenen Paket.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_recv_accept_v4_discard___fwpm_layer_ale_auth_recv_accept_v6_discard"></span>**BPM \_ -Schicht \_ \_ -e/a \_ \_ \_ \_ - \_ \_ \_ \_ \_ \_ \_ vorlagenauthentifizierung akzeptieren, Version 9 verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das Überprüfen von Accept-Anforderungen für eingehende TCP-Verbindungen, die verworfen wurden, sowie das Überprüfen von Autorisierungen für eingehenden nicht-TCP-Datenverkehr, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4___FWPM_LAYER_ALE_AUTH_CONNECT_V6"></span><span id="fwpm_layer_ale_auth_connect_v4___fwpm_layer_ale_auth_connect_v6"></span>**Bwpm \_ Layer \_ ALE Authentifizierung \_ \_ Connect \_ V4/bwpm \_ Layer \_ ALE \_ auth \_ Connect \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das autorialisieren von Connect-Anforderungen für ausgehende TCP-Verbindungen sowie das autorialisieren von nicht-TCP-Datenverkehr basierend auf dem ersten gesendeten Paket.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_connect_v4_discard___fwpm_layer_ale_auth_connect_v6_discard"></span>**Bwpm \_ Layer \_ ALE Authentifizierung \_ \_ Connect \_ V4 \_ verwerfen/bwpm \_ Layer \_ ALE \_ auth \_ Connect \_ V6 \_ verwerfen**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Überprüfung von Verbindungsanforderungen für ausgehende TCP-Verbindungen, die verworfen wurden, sowie das Überprüfen von Autorisierungen für ausgehenden nicht-TCP-Datenverkehr, die verworfen wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6"></span><span id="fwpm_layer_ale_flow_established_v4___fwpm_layer_ale_flow_established_v6"></span>**F-der \_ -Schicht-Fluss der Ebene der \_ \_ \_ \_ V4-/bwpm- \_ Schicht, \_ \_ \_ festgelegte \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Benachrichtigung, wann eine TCP-Verbindung hergestellt wurde oder wann nicht-TCP-Datenverkehr autorisiert wurde.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD"></span><span id="fwpm_layer_ale_flow_established_v4_discard___fwpm_layer_ale_flow_established_v6_discard"></span>**Auf der Ebene der schwpm \_ \_ \_ -Ebene \_ festgelegtes \_ V4 \_ -verwerfen/bwpm-Schicht-ALE-Daten \_ \_ \_ Fluss \_ \_ \_**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht es, zu überprüfen, wann eine festgelegte TCP-Verbindung auf der durch den Flow eingerichteten Ebene verworfen wurde, und wenn der autorisierte nicht-TCP-Datenverkehr auf der durch Flow eingerichteten Ebene verworfen wurde.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_inbound_mac_frame_ethernet"></span>**fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad, nachdem die Mac-ebenenverarbeitung (802,3) stattgefunden hat, aber bevor der Frame von der framingebene verarbeitet wird. Dies ist die Ebene nach dem systemeigenen, in der alle Frames wie Ethernet-Frames aussehen.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_outbound_mac_frame_ethernet"></span>**\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im sendepfad, nachdem die Verarbeitung der Rahmen Ebene aufgetreten ist, aber bevor der Frame von der Mac-Ebene (802,3) verarbeitet wird. Dies ist die Ebene nach dem systemeigenen, in der alle Frames wie Ethernet-Frames aussehen.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_inbound_mac_frame_native"></span>**fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Empfangs Pfad, nachdem die Verarbeitung der Mac-Schicht stattgefunden hat, aber bevor der Frame von der frageebene verarbeitet wird. Dies ist die erste Ebene, nachdem der Miniport den Frame an NDIS übermittelt hat.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_outbound_mac_frame_native"></span>**\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im sendepfad, nachdem die Verarbeitung der Rahmen Ebene aufgetreten ist, aber bevor der Frame von der Mac-Ebene (Native 802,11) verarbeitet wird. Dies ist die erste Ebene, nachdem der Miniport den Frame an NDIS übermittelt hat.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_ingress_vswitch_ethernet"></span>**fwpm- \_ Schicht \_ Ingress \_ vSwitch \_ Ethernet**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Vswitch-Eingangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_EGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_egress_vswitch_ethernet"></span>**fwpm- \_ Schicht, \_ ausgehender \_ vSwitch \_ Ethernet**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Vswitch-Ausgangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_ingress_vswitch_transport_v4___fwpm_layer_ingress_vswitch_transport_v6"></span>**Fwpm- \_ Schicht \_ Eingangs \_ -vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht Eingangs- \_ \_ vSwitch- \_ Transport \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Vswitch-Eingangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet. Diese Ebene ermöglicht Filterbedingungen auf Transport Ebene, um das Filtern von Datenverkehr zu unterstützen.

Wenn sich ein vswitchport im pvlan-oder trunk Modus befindet, werden Filter auf dieser Ebene umgangen, sodass der Datenverkehr ohne Filterung durchlaufen werden kann.

Wenn IPv4 auf dem Host deinstalliert wird, werden die Pakete in dieser Ebene gelöscht.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_egress_vswitch_transport_v4___fwpm_layer_egress_vswitch_transport_v6"></span>**Fwpm- \_ Schicht \_ ausgehender \_ vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht \_ ausgehender \_ vSwitch- \_ Transport \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene befindet sich im Vswitch-Ausgangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet. Diese Ebene ermöglicht Filterbedingungen auf Transport Ebene, um das Filtern von Datenverkehr zu unterstützen.

Wenn sich ein vswitchport im pvlan-oder trunk Modus befindet, werden Filter auf dieser Ebene umgangen, sodass der Datenverkehr ohne Filterung durchlaufen werden kann.

Wenn IPv4 auf dem Host deinstalliert wird, werden die Pakete in dieser Ebene gelöscht.

> [!Note]  
> Nur in Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPSEC_KM_DEMUX_V4___FWPM_LAYER_IPSEC_KM_DEMUX_V6"></span><span id="fwpm_layer_ipsec_km_demux_v4___fwpm_layer_ipsec_km_demux_v6"></span>**WPM- \_ Schicht \_ IPSec \_ km \_ \_ -Version V4/- \_ Ebene \_ IPSec km-Version \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene wird verwendet, um zu bestimmen, welche Schlüssel-Module aufgerufen werden, wenn das lokale System der Initiator ist. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IPSEC_V4___FWPM_LAYER_IPSEC_V6"></span><span id="fwpm_layer_ipsec_v4___fwpm_layer_ipsec_v6"></span>**WPM \_ -Schicht \_ IPSec \_ V4/WPM- \_ Schicht \_ IPSec \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht es dem Schlüssel Bindungs Modul, beim Aushandeln von Schnellmodus-Sicherheits Zuordnungen Schnellmodus-Richtlinien Informationen zu suchen. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_IKEEXT_V4___FWPM_LAYER_IKEEXT_V6"></span><span id="fwpm_layer_ikeext_v4___fwpm_layer_ikeext_v6"></span>**WPM \_ -Schicht \_ IKEEXT \_ V4/bwpm \_ Schicht \_ IKEEXT \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht es den IKE-und authentifizierten IP-Modulen, beim Aushandeln von hauptmodussicherheits-Zuordnungen hauptmodusrichtlinieninformationen zu suchen. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_UM"></span><span id="fwpm_layer_rpc_um"></span>**WPM- \_ Schicht- \_ RPC- \_ um**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Überprüfung der im Benutzermodus verfügbaren RPC-Datenfelder. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_EPMAP"></span><span id="fwpm_layer_rpc_epmap"></span>**\_ \_ RPC- \_ EPMAP der WPM-Ebene**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Überprüfung der RPC-Datenfelder, die während der Endpunkt Auflösung im Benutzermodus verfügbar sind. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_EP_ADD"></span><span id="fwpm_layer_rpc_ep_add"></span>**WPM- \_ Schicht- \_ RPC \_ EP- \_ Add**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das Überprüfen der RPC-Datenfelder, die im Benutzermodus verfügbar sind, wenn ein neuer Endpunkt hinzugefügt wird. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_PROXY_CONN"></span><span id="fwpm_layer_rpc_proxy_conn"></span>**WPM- \_ Schicht- \_ RPC- \_ Proxy \_ conn**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Überprüfung der RpcProxy-Verbindungsanforderungen. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_RPC_PROXY_IF"></span><span id="fwpm_layer_rpc_proxy_if"></span>**WPM- \_ Schicht- \_ RPC- \_ Proxy \_ if**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Überprüfung der für RpcProxy-Verbindungen verwendeten Schnittstelle. Dabei handelt es sich um eine Filter Ebene im Benutzermodus.


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_KM_AUTHORIZATION"></span><span id="fwpm_layer_km_authorization"></span>**Autorisierung für die Authentifizierung mit der \_ Ebene \_ km \_**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Autorisierungs Einrichtung von Sicherheits Zuordnungen.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_NAME_RESOLUTION_CACHE_V4___FWPM_LAYER_NAME_RESOLUTION_CACHE_V6"></span><span id="fwpm_layer_name_resolution_cache_v4___fwpm_layer_name_resolution_cache_v6"></span>**Auflösung der swpm \_ \_ -Ebenenname \_ \_ -Auflösung Cache \_ V4/swpm- \_ \_ Ebenenname- \_ \_ Cache \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Abfrage der Namen, die vor kurzem vom System aufgelöst wurden.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_RESOURCE_RELEASE_V4___FWPM_LAYER_ALE_RESOURCE_RELEASE_V6"></span><span id="fwpm_layer_ale_resource_release_v4___fwpm_layer_ale_resource_release_v6"></span>**Swpm \_ Layer \_ ALE \_ \_ -Ressourcen Release \_ V4/f \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das Freigeben von Ressourcen, die zuvor zugewiesen wurden.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4___FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6"></span><span id="fwpm_layer_ale_endpoint_closure_v4___fwpm_layer_ale_endpoint_closure_v6"></span>**F/a \_ \_ \_ \_ -Endpunkt Schließung \_ \_ \_ \_ \_ \_ der swpm-Schicht**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht das Nachverfolgen der Deaktivierung des verbundenen TCP-Flows oder der UDP-Sockets.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_CONNECT_REDIRECT_V4___FWPM_LAYER_ALE_CONNECT_REDIRECT_V6"></span><span id="fwpm_layer_ale_connect_redirect_v4___fwpm_layer_ale_connect_redirect_v6"></span>**F & # amp; \_ quer-Layer \_ \_ \_ -Connect \_ -Umleitung V4/bwpm \_ Schicht- \_ \_ Verbindungs \_ Umleitung \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Änderung von Adressen und Ports auf der Bindungs \_ Ebene der Umleitung.

Für TCP können die lokale Adresse und/oder der lokale Port sowie die Remote Adresse und/oder der Remoteport geändert werden.

Für UDP können die lokale Adresse und/oder der lokale Port geändert werden.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_ALE_BIND_REDIRECT_V4___FWPM_LAYER_ALE_BIND_REDIRECT_V6"></span><span id="fwpm_layer_ale_bind_redirect_v4___fwpm_layer_ale_bind_redirect_v6"></span>**F/a \_ \_ -Layer \_ \_ -Bind \_ -Umleitung V4-/b-ebenenbindung \_ \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Änderung von BIND ()-und Connect ()-aufrufen sowie die Auswahl von Host Routen.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_LAYER_STREAM_PACKET_V4___FWPM_LAYER_STREAM_PACKET_V6"></span><span id="fwpm_layer_stream_packet_v4___fwpm_layer_stream_packet_v6"></span>**F & # amp; amp; amp; amp \_ \_ \_ \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Diese Filter Ebene ermöglicht die Überprüfung von TCP-Paketen einschließlich Hand Shake-und Fluss Steuerungs Austausch.

Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese filterebenenbezeichner werden auch als Bezeichner für die Verwaltung von ebenenbezeichlern bezeichnet. Die WFP-API enthält auch eine Reihe von [Lauf Zeit filterebenenbezeichlern](/windows-hardware/drivers/network/management-filtering-layer-identifiers), die im Windows-Treiberkit (WDK) dokumentiert sind. Ebenenidentifizierer für die Lauf Zeit Filterung sind LUIDs und daher kleiner, nur 64 Bits im Vergleich zu den Verwaltungs ebenenbezeichern der Verwaltung, die 128 Bits groß sind.

Ebenenbezeichner für die Verwaltung und Lauf Zeit Filterung auf die gleichen Ebenen.

Bezeichner für die verwaltungfilterebenenkennung werden von Funktionen verwendet, die mit der Basis Filter-Engine (BFE) über den Benutzermodus oder den Kernel Modus (z. b. [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)) interagieren.

Ebenenbezeichner für die Lauf Zeit Filterung werden von Funktionen verwendet, die mit der Filter-Engine aus dem Kernel Modus interagieren (z. b. [FwpsFlowAssociateContext0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsflowassociatecontext0), [FwpsStreamInjectAsync0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsstreaminjectasync0)), und in Datenstrukturen, die direkt aus dem Kernel stammen (z. b. " [**swpm \_ net \_ Event \_ klassifizieren" \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ALE Ebenen](ale-layers.md)
</dt> <dt>

[WFP-Architektur](windows-filtering-platform-architecture-overview.md)
</dt> </dl>

