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
# <a name="filtering-layer-identifiers"></a><span data-ttu-id="be877-103">Filtern von ebenenbezeichgern</span><span class="sxs-lookup"><span data-stu-id="be877-103">Filtering Layer Identifiers</span></span>

<span data-ttu-id="be877-104">Die ebenenids der Windows-Filter Plattform (WFP) werden jeweils durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="be877-104">The Windows Filtering Platform (WFP) layer identifiers are each represented by a GUID.</span></span> <span data-ttu-id="be877-105">Diese Bezeichner werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="be877-105">These identifiers are defined as follows.</span></span>

<span data-ttu-id="be877-106">Die v4-und V6-Suffixe am Ende der ebenenids geben an, ob sich die Ebene im IPv4-Netzwerk Stapel oder im IPv6-Netzwerk Stapel befindet.</span><span class="sxs-lookup"><span data-stu-id="be877-106">The V4 and V6 suffixes at the end of the layer identifiers indicate whether the layer is located in the IPv4 network stack or in the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="be877-107"><span id="FWPM_LAYER_INBOUND_IPPACKET_V4___FWPM_LAYER_INBOUND_IPPACKET_V6"></span><span id="fwpm_layer_inbound_ippacket_v4___fwpm_layer_inbound_ippacket_v6"></span>**WPM- \_ Schicht \_ eingehender \_ ippacket \_ V4/bwpm- \_ Schicht \_ eingehender \_ ippacket \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-107"><span id="FWPM_LAYER_INBOUND_IPPACKET_V4___FWPM_LAYER_INBOUND_IPPACKET_V6"></span><span id="fwpm_layer_inbound_ippacket_v4___fwpm_layer_inbound_ippacket_v6"></span>**FWPM\_LAYER\_INBOUND\_IPPACKET\_V4 / FWPM\_LAYER\_INBOUND\_IPPACKET\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-108">Diese Filter Ebene befindet sich im Empfangs Pfad, wenn der IP-Header eines empfangenen Pakets analysiert wurde, aber bevor eine IP-Header Verarbeitung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="be877-108">This filtering layer is located in the receive path just after the IP header of a received packet has been parsed but before any IP header processing takes place.</span></span> <span data-ttu-id="be877-109">Es ist keine IPSec-Entschlüsselung oder-Neuzuweisung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="be877-109">No IPsec decryption or reassembly has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-110"><span id="FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_inbound_ippacket_v4_discard___fwpm_layer_inbound_ippacket_v6_discard"></span>**WPM \_ -Schicht \_ eingehender \_ ippacket \_ V4 \_ verwerfen/bwpm- \_ Schicht \_ eingehender \_ ippacket \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-110"><span id="FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_inbound_ippacket_v4_discard___fwpm_layer_inbound_ippacket_v6_discard"></span>**FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD / FWPM\_LAYER\_INBOUND\_IPPACKET\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-111">Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener Pakete, die auf der Netzwerkebene verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-111">This filtering layer is located in the receive path for inspecting any received packets that have been discarded at the network layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-112"><span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4___FWPM_LAYER_OUTBOUND_IPPACKET_V6"></span><span id="fwpm_layer_outbound_ippacket_v4___fwpm_layer_outbound_ippacket_v6"></span>**WPM- \_ Ebene ausgehend von \_ \_ ippacket \_ V4/bwpm- \_ Schicht ausgehende \_ \_ ippacket \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-112"><span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4___FWPM_LAYER_OUTBOUND_IPPACKET_V6"></span><span id="fwpm_layer_outbound_ippacket_v4___fwpm_layer_outbound_ippacket_v6"></span>**FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4 / FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-113">Diese Filter Ebene befindet sich im Sende Pfad, kurz bevor das gesendete Paket für die Fragmentierung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="be877-113">This filtering layer is located in the send path just before the sent packet is evaluated for fragmentation.</span></span> <span data-ttu-id="be877-114">Die gesamte IP-Header Verarbeitung ist vollständig, und alle Erweiterungs Header sind vorhanden.</span><span class="sxs-lookup"><span data-stu-id="be877-114">All IP header processing is complete and all extension headers are in place.</span></span> <span data-ttu-id="be877-115">Alle IPSec-Authentifizierung und-Verschlüsselung sind bereits aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="be877-115">Any IPsec authentication and encryption has already occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-116"><span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_outbound_ippacket_v4_discard___fwpm_layer_outbound_ippacket_v6_discard"></span>**WPM- \_ Ebene ausgehend von \_ \_ ippacket \_ V4 \_ verwerfen/WPM- \_ Schicht \_ ausgehende \_ ippacket \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-116"><span id="FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD___FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD"></span><span id="fwpm_layer_outbound_ippacket_v4_discard___fwpm_layer_outbound_ippacket_v6_discard"></span>**FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4\_DISCARD / FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-117">Diese Filter Ebene befindet sich im sendepfad zum Überprüfen aller gesendeten Pakete, die auf der Netzwerkebene verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-117">This filtering layer is located in the send path for inspecting any sent packets that have been discarded at the network layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-118"><span id="FWPM_LAYER_IPFORWARD_V4___FWPM_LAYER_IPFORWARD_V6"></span><span id="fwpm_layer_ipforward_v4___fwpm_layer_ipforward_v6"></span>**WPM \_ -Schicht \_ ipforward \_ V4/bwpm- \_ Schicht \_ ipforward \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-118"><span id="FWPM_LAYER_IPFORWARD_V4___FWPM_LAYER_IPFORWARD_V6"></span><span id="fwpm_layer_ipforward_v4___fwpm_layer_ipforward_v6"></span>**FWPM\_LAYER\_IPFORWARD\_V4 / FWPM\_LAYER\_IPFORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-119">Diese Filter Ebene befindet sich im Weiterleitungs Pfad an dem Punkt, an dem ein empfangenes Paket weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="be877-119">This filtering layer is located in the forwarding path at the point where a received packet is forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-120"><span id="FWPM_LAYER_IPFORWARD_V4_DISCARD___FWPM_LAYER_IPFORWARD_V6_DISCARD"></span><span id="fwpm_layer_ipforward_v4_discard___fwpm_layer_ipforward_v6_discard"></span>**WPM \_ -Schicht \_ ipforward \_ V4 \_ Verwerfungs-/WPM- \_ Schicht- \_ ipforward \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-120"><span id="FWPM_LAYER_IPFORWARD_V4_DISCARD___FWPM_LAYER_IPFORWARD_V6_DISCARD"></span><span id="fwpm_layer_ipforward_v4_discard___fwpm_layer_ipforward_v6_discard"></span>**FWPM\_LAYER\_IPFORWARD\_V4\_DISCARD / FWPM\_LAYER\_IPFORWARD\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-121">Diese Filter Ebene befindet sich im Weiterleitungs Pfad zum Überprüfen von weitergeleiteten Paketen, die auf der Weiterleitungs Ebene verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-121">This filtering layer is located in the forwarding path for inspecting any forwarded packets that have been discarded at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-122"><span id="FWPM_LAYER_INBOUND_TRANSPORT_V4___FWPM_LAYER_INBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_inbound_transport_v4___fwpm_layer_inbound_transport_v6"></span>**WPM \_ -Schicht \_ eingehender \_ Transport \_ V4/bwpm- \_ Schicht \_ eingehender \_ Transport \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-122"><span id="FWPM_LAYER_INBOUND_TRANSPORT_V4___FWPM_LAYER_INBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_inbound_transport_v4___fwpm_layer_inbound_transport_v6"></span>**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4 / FWPM\_LAYER\_INBOUND\_TRANSPORT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-123">Diese Filter Ebene befindet sich im Empfangs Pfad, unmittelbar nachdem der Transport Header eines empfangenen Pakets vom Netzwerk Stapel auf der Transport Ebene analysiert wurde, jedoch bevor die Verarbeitung der Transportschicht erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="be877-123">This filtering layer is located in the receive path just after a received packet's transport header has been parsed by the network stack at the transport layer, but before any transport layer processing takes place.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-124"><span id="FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_inbound_transport_v4_discard___fwpm_layer_inbound_transport_v6_discard"></span>**WPM \_ -Schicht \_ eingehender \_ Transport \_ V4 \_ verwerfen/WPM- \_ Schicht \_ eingehender \_ Transport \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-124"><span id="FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_inbound_transport_v4_discard___fwpm_layer_inbound_transport_v6_discard"></span>**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD / FWPM\_LAYER\_INBOUND\_TRANSPORT\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-125">Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener Pakete, die auf der Transport Ebene verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-125">This filtering layer is located in the receive path for inspecting any received packets that have been discarded at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-126"><span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4___FWPM_LAYER_OUTBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_outbound_transport_v4___fwpm_layer_outbound_transport_v6"></span>**Ausgehender Transport der WPM-Schicht für ausgehenden \_ \_ \_ Transport \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be877-126"><span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4___FWPM_LAYER_OUTBOUND_TRANSPORT_V6"></span><span id="fwpm_layer_outbound_transport_v4___fwpm_layer_outbound_transport_v6"></span>**FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-127">Diese Filter Ebene befindet sich im sendepfad, wenn ein gesendetes Paket zur Verarbeitung an die Netzwerkschicht, aber erst nach der Verarbeitung der Netzwerkschicht an die Netzwerkschicht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="be877-127">This filtering layer is located in the send path just after a sent packet has been passed to the network layer for processing but before any network layer processing takes place.</span></span> <span data-ttu-id="be877-128">Diese Filter Ebene befindet sich am oberen Rand der Netzwerkschicht anstatt am unteren Rand der Transport Ebene, sodass alle Pakete, die von Drittanbietern oder als unformatierte Pakete gesendet werden, auf dieser Ebene gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="be877-128">This filtering layer is located at the top of the network layer instead of at the bottom of the transport layer so that any packets that are sent by third-party transports or as raw packets are filtered at this layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-129"><span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_outbound_transport_v4_discard___fwpm_layer_outbound_transport_v6_discard"></span>**Ausgehender Transport der WPM \_ -Schicht, \_ \_ \_ V4 \_ verwerfen/WPM- \_ Schicht- \_ \_ Transport \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-129"><span id="FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD___FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD"></span><span id="fwpm_layer_outbound_transport_v4_discard___fwpm_layer_outbound_transport_v6_discard"></span>**FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4\_DISCARD / FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-130">Diese Filter Ebene befindet sich im sendepfad zum Überprüfen aller gesendeten Pakete, die auf der Transport Ebene verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-130">This filtering layer is located in the send path for inspecting any sent packets that have been discarded at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-131"><span id="FWPM_LAYER_STREAM_V4___FWPM_LAYER_STREAM_V6"></span><span id="fwpm_layer_stream_v4___fwpm_layer_stream_v6"></span>**BPM \_ -Layer \_ \_ -Stream V4/bwpm- \_ \_ ebenenstream \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-131"><span id="FWPM_LAYER_STREAM_V4___FWPM_LAYER_STREAM_V6"></span><span id="fwpm_layer_stream_v4___fwpm_layer_stream_v6"></span>**FWPM\_LAYER\_STREAM\_V4 / FWPM\_LAYER\_STREAM\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-132">Diese Filter Ebene befindet sich im Stream-Daten Pfad.</span><span class="sxs-lookup"><span data-stu-id="be877-132">This filtering layer is located in the stream data path.</span></span> <span data-ttu-id="be877-133">Diese Ebene ermöglicht die Untersuchung von Netzwerkdaten pro Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="be877-133">This layer allows for inspecting network data on a per stream basis.</span></span> <span data-ttu-id="be877-134">Auf der streamschicht sind die Netzwerkdaten bidirektional.</span><span class="sxs-lookup"><span data-stu-id="be877-134">At the stream layer, the network data is bidirectional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-135"><span id="FWPM_LAYER_STREAM_V4_DISCARD___FWPM_LAYER_STREAM_V6_DISCARD"></span><span id="fwpm_layer_stream_v4_discard___fwpm_layer_stream_v6_discard"></span>**BPM \_ -Layer \_ \_ -Stream \_ V4 verwerfen/WPM \_ - \_ ebenenstream \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-135"><span id="FWPM_LAYER_STREAM_V4_DISCARD___FWPM_LAYER_STREAM_V6_DISCARD"></span><span id="fwpm_layer_stream_v4_discard___fwpm_layer_stream_v6_discard"></span>**FWPM\_LAYER\_STREAM\_V4\_DISCARD / FWPM\_LAYER\_STREAM\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-136">Diese Filter Ebene befindet sich im Stream-Daten Pfad zum Überprüfen von Datenstrom Daten, die verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-136">This filtering layer is located in the stream data path for inspecting any stream data that has been discarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-137"><span id="FWPM_LAYER_DATAGRAM_DATA_V4___FWPM_LAYER_DATAGRAM_DATA_V6"></span><span id="fwpm_layer_datagram_data_v4___fwpm_layer_datagram_data_v6"></span>**\_ \_ Datagramm-Datagramm-Daten (Datagramm) der WPM \_ \_ - \_ \_ \_ \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="be877-137"><span id="FWPM_LAYER_DATAGRAM_DATA_V4___FWPM_LAYER_DATAGRAM_DATA_V6"></span><span id="fwpm_layer_datagram_data_v4___fwpm_layer_datagram_data_v6"></span>**FWPM\_LAYER\_DATAGRAM\_DATA\_V4 / FWPM\_LAYER\_DATAGRAM\_DATA\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-138">Diese Filter Ebene befindet sich im Datagramm-Datenpfad.</span><span class="sxs-lookup"><span data-stu-id="be877-138">This filtering layer is located in the datagram data path.</span></span> <span data-ttu-id="be877-139">Diese Ebene ermöglicht die Untersuchung von Netzwerkdaten pro Datagramm-Basis.</span><span class="sxs-lookup"><span data-stu-id="be877-139">This layer allows for inspecting network data on a per datagram basis.</span></span> <span data-ttu-id="be877-140">Die Netzwerkdaten auf der datagrammebene sind bidirektional.</span><span class="sxs-lookup"><span data-stu-id="be877-140">At the datagram layer, the network data is bidirectional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-141"><span id="FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD___FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD"></span><span id="fwpm_layer_datagram_data_v4_discard___fwpm_layer_datagram_data_v6_discard"></span>**\_ \_ Datagramm-Datagramm \_ \_ \_ - \_ \_ \_ \_ Datagrammdaten \_**</span><span class="sxs-lookup"><span data-stu-id="be877-141"><span id="FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD___FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD"></span><span id="fwpm_layer_datagram_data_v4_discard___fwpm_layer_datagram_data_v6_discard"></span>**FWPM\_LAYER\_DATAGRAM\_DATA\_V4\_DISCARD / FWPM\_LAYER\_DATAGRAM\_DATA\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-142">Diese Filter Ebene befindet sich im Datagramm-Datenpfad zum Überprüfen von Datagrammen, die verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-142">This filtering layer is located in the datagram data path for inspecting any datagrams that have been discarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-143"><span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4___FWPM_LAYER_INBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_inbound_icmp_error_v4___fwpm_layer_inbound_icmp_error_v6"></span>**WPM- \_ Schicht \_ eingehender \_ ICMP \_ \_ -Fehler V4/WPM- \_ Schicht \_ eingehender \_ ICMP- \_ Fehler \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-143"><span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4___FWPM_LAYER_INBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_inbound_icmp_error_v4___fwpm_layer_inbound_icmp_error_v6"></span>**FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V4 / FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-144">Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener ICMP-Fehlermeldungen für das Transportprotokoll.</span><span class="sxs-lookup"><span data-stu-id="be877-144">This filtering layer is located in the receive path for inspecting received ICMP error messages for the transport protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-145"><span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_inbound_icmp_error_v4_discard___fwpm_layer_inbound_icmp_error_v6_discard"></span>**WPM \_ -Schicht \_ eingehender \_ ICMP \_ \_ -Fehler V4 \_ verwerfen/WPM- \_ Schicht \_ eingehender \_ ICMP- \_ Fehler \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-145"><span id="FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_inbound_icmp_error_v4_discard___fwpm_layer_inbound_icmp_error_v6_discard"></span>**FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V4\_DISCARD / FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-146">Diese Filter Ebene befindet sich im Empfangs Pfad zum Überprüfen empfangener ICMP-Fehlermeldungen, die verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-146">This filtering layer is located in the receive path for inspecting received ICMP error messages that have been discarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-147"><span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_outbound_icmp_error_v4___fwpm_layer_outbound_icmp_error_v6"></span>**\_ \_ Ausgehender \_ ICMP \_ \_ -Fehler V4/WPM-Layer-ausgehende \_ \_ \_ ICMP- \_ Fehler \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-147"><span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6"></span><span id="fwpm_layer_outbound_icmp_error_v4___fwpm_layer_outbound_icmp_error_v6"></span>**FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4 / FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-148">Diese Filter Ebene befindet sich im sendepfad zum Überprüfen empfangener ICMP-Fehlermeldungen für das Transportprotokoll.</span><span class="sxs-lookup"><span data-stu-id="be877-148">This filtering layer is located in the send path for inspecting received ICMP error messages for the transport protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-149"><span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_outbound_icmp_error_v4_discard___fwpm_layer_outbound_icmp_error_v6_discard"></span>**\_ \_ Ausgehender \_ ICMP \_ \_ -Fehler V4 \_ verwerfen/WPM-Ebene Ausgeh \_ Ende \_ \_ ICMP- \_ Fehler \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-149"><span id="FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD___FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD"></span><span id="fwpm_layer_outbound_icmp_error_v4_discard___fwpm_layer_outbound_icmp_error_v6_discard"></span>**FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4\_DISCARD / FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-150">Diese Filter Ebene befindet sich im sendepfad zum Überprüfen empfangener ICMP-Fehlermeldungen, die verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-150">This filtering layer is located in the send path for inspecting received ICMP error messages that have been discarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-151"><span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_layer_ale_resource_assignment_v4___fwpm_layer_ale_resource_assignment_v6"></span>**F/a \_ -Ebene der \_ \_ Ressourcen \_ Zuweisung \_ V4/bwpm \_ Schicht- \_ \_ Ressourcen \_ Zuweisung \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-151"><span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_layer_ale_resource_assignment_v4___fwpm_layer_ale_resource_assignment_v6"></span>**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4 / FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-152">Diese Filter Ebene ermöglicht das autorialisieren von Transport Port Zuweisungen, Bindungs Anforderungen, Anforderungen im Anforderungs Modus und Anforderungen im RAW-Modus.</span><span class="sxs-lookup"><span data-stu-id="be877-152">This filtering layer allows for authorizing transport port assignments, bind requests, promiscuous mode requests, and raw mode requests.</span></span>

<span data-ttu-id="be877-153">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-153">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-154"><span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD"></span><span id="fwpm_layer_ale_resource_assignment_v4_discard___fwpm_layer_ale_resource_assignment_v6_discard"></span>**F-Ressourcenzuweisung der swpm \_ -Schicht, \_ \_ \_ \_ V4 \_ verwerfen/swpm \_ Schicht- \_ \_ Ressourcen \_ Zuweisung \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-154"><span id="FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD___FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD"></span><span id="fwpm_layer_ale_resource_assignment_v4_discard___fwpm_layer_ale_resource_assignment_v6_discard"></span>**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4\_DISCARD / FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-155">Diese Filter Ebene ermöglicht das Überprüfen der folgenden verworfenen Elemente: Transport Port Zuweisungen, Bindungs Anforderungen, Anforderungen im Anforderungs Modus und Anforderungen im RAW-Modus.</span><span class="sxs-lookup"><span data-stu-id="be877-155">This filtering layer allows for inspecting the following discarded items: transport port assignments, bind requests, promiscuous mode requests, and raw mode requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-156"><span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4___FWPM_LAYER_ALE_AUTH_LISTEN_V6"></span><span id="fwpm_layer_ale_auth_listen_v4___fwpm_layer_ale_auth_listen_v6"></span>**Lwpm \_ Layer \_ ALE \_ auth \_ hört \_ V4/bwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-156"><span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4___FWPM_LAYER_ALE_AUTH_LISTEN_V6"></span><span id="fwpm_layer_ale_auth_listen_v4___fwpm_layer_ale_auth_listen_v6"></span>**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4 / FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-157">Diese Filter Ebene ermöglicht das autorialisieren von TCP-lausch Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="be877-157">This filtering layer allows for authorizing TCP listen requests.</span></span>

<span data-ttu-id="be877-158">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-158">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-159"><span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD___FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_listen_v4_discard___fwpm_layer_ale_auth_listen_v6_discard"></span>**BPM \_ -Layer \_ \_ -der-Authentifizierung \_ hört \_ V4 \_ -Verwerfungs-/BB-ebenenauthentifizierung \_ \_ \_ \_ \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-159"><span id="FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD___FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_listen_v4_discard___fwpm_layer_ale_auth_listen_v6_discard"></span>**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4\_DISCARD / FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-160">Diese Filter Ebene ermöglicht die Untersuchung von TCP-lausch Anforderungen, die verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-160">This filtering layer allows for inspecting TCP listen requests that have been discarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-161"><span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6"></span><span id="fwpm_layer_ale_auth_recv_accept_v4___fwpm_layer_ale_auth_recv_accept_v6"></span>**BPM \_ -Schicht \_ \_ -e \_ -v akzeptieren Version \_ \_ V4/bwpm \_ Schicht \_ ALE Authentifizierung \_ \_ \_ akzeptieren \_**</span><span class="sxs-lookup"><span data-stu-id="be877-161"><span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6"></span><span id="fwpm_layer_ale_auth_recv_accept_v4___fwpm_layer_ale_auth_recv_accept_v6"></span>**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4 / FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-162">Diese Filterungs Ebene ermöglicht das autorialisieren von Accept-Anforderungen für eingehende TCP-Verbindungen sowie das Autorisierungs eingehender nicht-TCP-Datenverkehr basierend auf dem ersten empfangenen Paket.</span><span class="sxs-lookup"><span data-stu-id="be877-162">This filtering layer allows for authorizing accept requests for incoming TCP connections, as well as authorizing incoming non-TCP traffic based on the first packet received.</span></span>

<span data-ttu-id="be877-163">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-163">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-164"><span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_recv_accept_v4_discard___fwpm_layer_ale_auth_recv_accept_v6_discard"></span>**BPM \_ -Schicht \_ \_ -e/a \_ \_ \_ \_ - \_ \_ \_ \_ \_ \_ \_ vorlagenauthentifizierung akzeptieren, Version 9 verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-164"><span id="FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_recv_accept_v4_discard___fwpm_layer_ale_auth_recv_accept_v6_discard"></span>**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD / FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-165">Diese Filter Ebene ermöglicht das Überprüfen von Accept-Anforderungen für eingehende TCP-Verbindungen, die verworfen wurden, sowie das Überprüfen von Autorisierungen für eingehenden nicht-TCP-Datenverkehr, die verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-165">This filtering layer allows for inspecting accept requests for incoming TCP connections that have been discarded, as well as inspecting authorizations for incoming non-TCP traffic that have been discarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-166"><span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4___FWPM_LAYER_ALE_AUTH_CONNECT_V6"></span><span id="fwpm_layer_ale_auth_connect_v4___fwpm_layer_ale_auth_connect_v6"></span>**Bwpm \_ Layer \_ ALE Authentifizierung \_ \_ Connect \_ V4/bwpm \_ Layer \_ ALE \_ auth \_ Connect \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-166"><span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4___FWPM_LAYER_ALE_AUTH_CONNECT_V6"></span><span id="fwpm_layer_ale_auth_connect_v4___fwpm_layer_ale_auth_connect_v6"></span>**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4 / FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-167">Diese Filter Ebene ermöglicht das autorialisieren von Connect-Anforderungen für ausgehende TCP-Verbindungen sowie das autorialisieren von nicht-TCP-Datenverkehr basierend auf dem ersten gesendeten Paket.</span><span class="sxs-lookup"><span data-stu-id="be877-167">This filtering layer allows for authorizing connect requests for outgoing TCP connections, as well as authorizing outgoing non-TCP traffic based on the first packet sent.</span></span>

<span data-ttu-id="be877-168">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-168">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-169"><span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_connect_v4_discard___fwpm_layer_ale_auth_connect_v6_discard"></span>**Bwpm \_ Layer \_ ALE Authentifizierung \_ \_ Connect \_ V4 \_ verwerfen/bwpm \_ Layer \_ ALE \_ auth \_ Connect \_ V6 \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="be877-169"><span id="FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD___FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD"></span><span id="fwpm_layer_ale_auth_connect_v4_discard___fwpm_layer_ale_auth_connect_v6_discard"></span>**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4\_DISCARD / FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-170">Diese Filter Ebene ermöglicht die Überprüfung von Verbindungsanforderungen für ausgehende TCP-Verbindungen, die verworfen wurden, sowie das Überprüfen von Autorisierungen für ausgehenden nicht-TCP-Datenverkehr, die verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-170">This filtering layer allows for inspecting connect requests for outgoing TCP connections that have been discarded, as well as inspecting authorizations for outgoing non-TCP traffic that have been discarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-171"><span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6"></span><span id="fwpm_layer_ale_flow_established_v4___fwpm_layer_ale_flow_established_v6"></span>**F-der \_ -Schicht-Fluss der Ebene der \_ \_ \_ \_ V4-/bwpm- \_ Schicht, \_ \_ \_ festgelegte \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-171"><span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6"></span><span id="fwpm_layer_ale_flow_established_v4___fwpm_layer_ale_flow_established_v6"></span>**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4 / FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-172">Diese Filter Ebene ermöglicht die Benachrichtigung, wann eine TCP-Verbindung hergestellt wurde oder wann nicht-TCP-Datenverkehr autorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="be877-172">This filtering layer allows for notification of when a TCP connection has been established, or when non-TCP traffic has been authorized.</span></span>

<span data-ttu-id="be877-173">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-173">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-174"><span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD"></span><span id="fwpm_layer_ale_flow_established_v4_discard___fwpm_layer_ale_flow_established_v6_discard"></span>**Auf der Ebene der schwpm \_ \_ \_ -Ebene \_ festgelegtes \_ V4 \_ -verwerfen/bwpm-Schicht-ALE-Daten \_ \_ \_ Fluss \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be877-174"><span id="FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD___FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD"></span><span id="fwpm_layer_ale_flow_established_v4_discard___fwpm_layer_ale_flow_established_v6_discard"></span>**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4\_DISCARD / FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V6\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-175">Diese Filter Ebene ermöglicht es, zu überprüfen, wann eine festgelegte TCP-Verbindung auf der durch den Flow eingerichteten Ebene verworfen wurde, und wenn der autorisierte nicht-TCP-Datenverkehr auf der durch Flow eingerichteten Ebene verworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="be877-175">This filtering layer allows for inspecting when an established TCP connection has been discarded at the flow established layer, as well as when authorized non-TCP traffic has been discarded at the flow established layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-176"><span id="FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_inbound_mac_frame_ethernet"></span>**fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet**</span><span class="sxs-lookup"><span data-stu-id="be877-176"><span id="FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_inbound_mac_frame_ethernet"></span>**FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-177">Diese Filter Ebene befindet sich im Empfangs Pfad, nachdem die Mac-ebenenverarbeitung (802,3) stattgefunden hat, aber bevor der Frame von der framingebene verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="be877-177">This filtering layer is located in the receive path after the MAC (802.3) layer processing has occurred but before the frame is processed by the framing layer.</span></span> <span data-ttu-id="be877-178">Dies ist die Ebene nach dem systemeigenen, in der alle Frames wie Ethernet-Frames aussehen.</span><span class="sxs-lookup"><span data-stu-id="be877-178">This is the layer after native in which all frames look like Ethernet frames.</span></span>

> [!Note]  
> <span data-ttu-id="be877-179">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-179">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-180"><span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_outbound_mac_frame_ethernet"></span>**\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene**</span><span class="sxs-lookup"><span data-stu-id="be877-180"><span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET"></span><span id="fwpm_layer_outbound_mac_frame_ethernet"></span>**FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-181">Diese Filter Ebene befindet sich im sendepfad, nachdem die Verarbeitung der Rahmen Ebene aufgetreten ist, aber bevor der Frame von der Mac-Ebene (802,3) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="be877-181">This filtering layer is located in the send path after the framing layer processing has occurred but before the frame is processed by the MAC (802.3) layer.</span></span> <span data-ttu-id="be877-182">Dies ist die Ebene nach dem systemeigenen, in der alle Frames wie Ethernet-Frames aussehen.</span><span class="sxs-lookup"><span data-stu-id="be877-182">This is the layer after native in which all frames look like Ethernet frames.</span></span>

> [!Note]  
> <span data-ttu-id="be877-183">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-183">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-184"><span id="FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_inbound_mac_frame_native"></span>**fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_**</span><span class="sxs-lookup"><span data-stu-id="be877-184"><span id="FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_inbound_mac_frame_native"></span>**FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-185">Diese Filter Ebene befindet sich im Empfangs Pfad, nachdem die Verarbeitung der Mac-Schicht stattgefunden hat, aber bevor der Frame von der frageebene verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="be877-185">This filtering layer is located in the receive path after the MAC layer processing has occurred but before the frame is processed by the framing layer.</span></span> <span data-ttu-id="be877-186">Dies ist die erste Ebene, nachdem der Miniport den Frame an NDIS übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="be877-186">It is the first layer after the Miniport delivers the frame to NDIS.</span></span>

> [!Note]  
> <span data-ttu-id="be877-187">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-187">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-188"><span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_outbound_mac_frame_native"></span>**\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene**</span><span class="sxs-lookup"><span data-stu-id="be877-188"><span id="FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE"></span><span id="fwpm_layer_outbound_mac_frame_native"></span>**FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-189">Diese Filter Ebene befindet sich im sendepfad, nachdem die Verarbeitung der Rahmen Ebene aufgetreten ist, aber bevor der Frame von der Mac-Ebene (Native 802,11) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="be877-189">This filtering layer is located in the send path after the framing layer processing has occurred but before the frame is processed by the MAC (Native 802.11) layer.</span></span> <span data-ttu-id="be877-190">Dies ist die erste Ebene, nachdem der Miniport den Frame an NDIS übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="be877-190">It is the first layer after the Miniport delivers the frame to NDIS.</span></span>

> [!Note]  
> <span data-ttu-id="be877-191">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-191">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-192"><span id="FWPM_LAYER_INGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_ingress_vswitch_ethernet"></span>**fwpm- \_ Schicht \_ Ingress \_ vSwitch \_ Ethernet**</span><span class="sxs-lookup"><span data-stu-id="be877-192"><span id="FWPM_LAYER_INGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_ingress_vswitch_ethernet"></span>**FWPM\_LAYER\_INGRESS\_VSWITCH\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-193">Diese Filter Ebene befindet sich im Vswitch-Eingangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="be877-193">This filtering layer is located in the vSwitch ingress path just after the MAC header has been parsed, but before any MAC header processing takes place.</span></span>

> [!Note]  
> <span data-ttu-id="be877-194">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-194">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-195"><span id="FWPM_LAYER_EGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_egress_vswitch_ethernet"></span>**fwpm- \_ Schicht, \_ ausgehender \_ vSwitch \_ Ethernet**</span><span class="sxs-lookup"><span data-stu-id="be877-195"><span id="FWPM_LAYER_EGRESS_VSWITCH_ETHERNET"></span><span id="fwpm_layer_egress_vswitch_ethernet"></span>**FWPM\_LAYER\_EGRESS\_VSWITCH\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-196">Diese Filter Ebene befindet sich im Vswitch-Ausgangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="be877-196">This filtering layer is located in the vSwitch egress path just after the MAC header has been parsed, but before any MAC header processing takes place.</span></span>

> [!Note]  
> <span data-ttu-id="be877-197">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-197">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-198"><span id="FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_ingress_vswitch_transport_v4___fwpm_layer_ingress_vswitch_transport_v6"></span>**Fwpm- \_ Schicht \_ Eingangs \_ -vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht Eingangs- \_ \_ vSwitch- \_ Transport \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-198"><span id="FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_ingress_vswitch_transport_v4___fwpm_layer_ingress_vswitch_transport_v6"></span>**FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-199">Diese Filter Ebene befindet sich im Vswitch-Eingangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="be877-199">This filtering layer is located in the vSwitch ingress path just after the MAC header has been parsed, but before any MAC header processing takes place.</span></span> <span data-ttu-id="be877-200">Diese Ebene ermöglicht Filterbedingungen auf Transport Ebene, um das Filtern von Datenverkehr zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="be877-200">This layer allows for TRANSPORT level filtering conditions to aid in filtering traffic.</span></span>

<span data-ttu-id="be877-201">Wenn sich ein vswitchport im pvlan-oder trunk Modus befindet, werden Filter auf dieser Ebene umgangen, sodass der Datenverkehr ohne Filterung durchlaufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="be877-201">If a vSwitchPort is in PVLAN or trunk mode, filters at this layer will be bypassed, letting the traffic flow through without any filtering.</span></span>

<span data-ttu-id="be877-202">Wenn IPv4 auf dem Host deinstalliert wird, werden die Pakete in dieser Ebene gelöscht.</span><span class="sxs-lookup"><span data-stu-id="be877-202">If IPv4 is uninstalled in the host, filters in this layer will cause packets to be dropped.</span></span>

> [!Note]  
> <span data-ttu-id="be877-203">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-203">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-204"><span id="FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_egress_vswitch_transport_v4___fwpm_layer_egress_vswitch_transport_v6"></span>**Fwpm- \_ Schicht \_ ausgehender \_ vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht \_ ausgehender \_ vSwitch- \_ Transport \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-204"><span id="FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4___FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V6"></span><span id="fwpm_layer_egress_vswitch_transport_v4___fwpm_layer_egress_vswitch_transport_v6"></span>**FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-205">Diese Filter Ebene befindet sich im Vswitch-Ausgangs Pfad, unmittelbar nachdem der Mac-Header analysiert wurde, aber bevor eine Mac-Header Verarbeitung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="be877-205">This filtering layer is located in the vSwitch egress path just after the MAC header has been parsed, but before any MAC header processing takes place.</span></span> <span data-ttu-id="be877-206">Diese Ebene ermöglicht Filterbedingungen auf Transport Ebene, um das Filtern von Datenverkehr zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="be877-206">This layer allows for TRANSPORT level filtering conditions to aid in filtering traffic.</span></span>

<span data-ttu-id="be877-207">Wenn sich ein vswitchport im pvlan-oder trunk Modus befindet, werden Filter auf dieser Ebene umgangen, sodass der Datenverkehr ohne Filterung durchlaufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="be877-207">If a vSwitchPort is in PVLAN or trunk mode, filters at this layer will be bypassed, letting the traffic flow through without any filtering.</span></span>

<span data-ttu-id="be877-208">Wenn IPv4 auf dem Host deinstalliert wird, werden die Pakete in dieser Ebene gelöscht.</span><span class="sxs-lookup"><span data-stu-id="be877-208">If IPv4 is uninstalled in the host, filters in this layer will cause packets to be dropped.</span></span>

> [!Note]  
> <span data-ttu-id="be877-209">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be877-209">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-210"><span id="FWPM_LAYER_IPSEC_KM_DEMUX_V4___FWPM_LAYER_IPSEC_KM_DEMUX_V6"></span><span id="fwpm_layer_ipsec_km_demux_v4___fwpm_layer_ipsec_km_demux_v6"></span>**WPM- \_ Schicht \_ IPSec \_ km \_ \_ -Version V4/- \_ Ebene \_ IPSec km-Version \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-210"><span id="FWPM_LAYER_IPSEC_KM_DEMUX_V4___FWPM_LAYER_IPSEC_KM_DEMUX_V6"></span><span id="fwpm_layer_ipsec_km_demux_v4___fwpm_layer_ipsec_km_demux_v6"></span>**FWPM\_LAYER\_IPSEC\_KM\_DEMUX\_V4 / FWPM\_LAYER\_IPSEC\_KM\_DEMUX\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-211">Diese Filter Ebene wird verwendet, um zu bestimmen, welche Schlüssel-Module aufgerufen werden, wenn das lokale System der Initiator ist.</span><span class="sxs-lookup"><span data-stu-id="be877-211">This filtering layer is used to determine which keying modules are invoked when the local system is the initiator.</span></span> <span data-ttu-id="be877-212">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-212">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-213"><span id="FWPM_LAYER_IPSEC_V4___FWPM_LAYER_IPSEC_V6"></span><span id="fwpm_layer_ipsec_v4___fwpm_layer_ipsec_v6"></span>**WPM \_ -Schicht \_ IPSec \_ V4/WPM- \_ Schicht \_ IPSec \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-213"><span id="FWPM_LAYER_IPSEC_V4___FWPM_LAYER_IPSEC_V6"></span><span id="fwpm_layer_ipsec_v4___fwpm_layer_ipsec_v6"></span>**FWPM\_LAYER\_IPSEC\_V4 / FWPM\_LAYER\_IPSEC\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-214">Diese Filter Ebene ermöglicht es dem Schlüssel Bindungs Modul, beim Aushandeln von Schnellmodus-Sicherheits Zuordnungen Schnellmodus-Richtlinien Informationen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="be877-214">This filtering layer allows the keying module to look up quick-mode policy information when negotiating quick-mode security associations.</span></span> <span data-ttu-id="be877-215">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-215">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-216"><span id="FWPM_LAYER_IKEEXT_V4___FWPM_LAYER_IKEEXT_V6"></span><span id="fwpm_layer_ikeext_v4___fwpm_layer_ikeext_v6"></span>**WPM \_ -Schicht \_ IKEEXT \_ V4/bwpm \_ Schicht \_ IKEEXT \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-216"><span id="FWPM_LAYER_IKEEXT_V4___FWPM_LAYER_IKEEXT_V6"></span><span id="fwpm_layer_ikeext_v4___fwpm_layer_ikeext_v6"></span>**FWPM\_LAYER\_IKEEXT\_V4 / FWPM\_LAYER\_IKEEXT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-217">Diese Filter Ebene ermöglicht es den IKE-und authentifizierten IP-Modulen, beim Aushandeln von hauptmodussicherheits-Zuordnungen hauptmodusrichtlinieninformationen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="be877-217">This filtering layer allows the IKE and authenticated IP modules to look up main-mode policy information when negotiating main-mode security associations.</span></span> <span data-ttu-id="be877-218">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-218">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-219"><span id="FWPM_LAYER_RPC_UM"></span><span id="fwpm_layer_rpc_um"></span>**WPM- \_ Schicht- \_ RPC- \_ um**</span><span class="sxs-lookup"><span data-stu-id="be877-219"><span id="FWPM_LAYER_RPC_UM"></span><span id="fwpm_layer_rpc_um"></span>**FWPM\_LAYER\_RPC\_UM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-220">Diese Filter Ebene ermöglicht die Überprüfung der im Benutzermodus verfügbaren RPC-Datenfelder.</span><span class="sxs-lookup"><span data-stu-id="be877-220">This filtering layer allows for inspecting the RPC data fields that are available in user mode.</span></span> <span data-ttu-id="be877-221">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-221">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-222"><span id="FWPM_LAYER_RPC_EPMAP"></span><span id="fwpm_layer_rpc_epmap"></span>**\_ \_ RPC- \_ EPMAP der WPM-Ebene**</span><span class="sxs-lookup"><span data-stu-id="be877-222"><span id="FWPM_LAYER_RPC_EPMAP"></span><span id="fwpm_layer_rpc_epmap"></span>**FWPM\_LAYER\_RPC\_EPMAP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-223">Diese Filter Ebene ermöglicht die Überprüfung der RPC-Datenfelder, die während der Endpunkt Auflösung im Benutzermodus verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="be877-223">This filtering layer allows for inspecting the RPC data fields that are available in user mode during endpoint resolution.</span></span> <span data-ttu-id="be877-224">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-224">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-225"><span id="FWPM_LAYER_RPC_EP_ADD"></span><span id="fwpm_layer_rpc_ep_add"></span>**WPM- \_ Schicht- \_ RPC \_ EP- \_ Add**</span><span class="sxs-lookup"><span data-stu-id="be877-225"><span id="FWPM_LAYER_RPC_EP_ADD"></span><span id="fwpm_layer_rpc_ep_add"></span>**FWPM\_LAYER\_RPC\_EP\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-226">Diese Filter Ebene ermöglicht das Überprüfen der RPC-Datenfelder, die im Benutzermodus verfügbar sind, wenn ein neuer Endpunkt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="be877-226">This filtering layer allows for inspecting the RPC data fields that are available in user mode when a new endpoint is added.</span></span> <span data-ttu-id="be877-227">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-227">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-228"><span id="FWPM_LAYER_RPC_PROXY_CONN"></span><span id="fwpm_layer_rpc_proxy_conn"></span>**WPM- \_ Schicht- \_ RPC- \_ Proxy \_ conn**</span><span class="sxs-lookup"><span data-stu-id="be877-228"><span id="FWPM_LAYER_RPC_PROXY_CONN"></span><span id="fwpm_layer_rpc_proxy_conn"></span>**FWPM\_LAYER\_RPC\_PROXY\_CONN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-229">Diese Filter Ebene ermöglicht die Überprüfung der RpcProxy-Verbindungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="be877-229">This filtering layer allows for inspecting the RpcProxy connection requests.</span></span> <span data-ttu-id="be877-230">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-230">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-231"><span id="FWPM_LAYER_RPC_PROXY_IF"></span><span id="fwpm_layer_rpc_proxy_if"></span>**WPM- \_ Schicht- \_ RPC- \_ Proxy \_ if**</span><span class="sxs-lookup"><span data-stu-id="be877-231"><span id="FWPM_LAYER_RPC_PROXY_IF"></span><span id="fwpm_layer_rpc_proxy_if"></span>**FWPM\_LAYER\_RPC\_PROXY\_IF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-232">Diese Filter Ebene ermöglicht die Überprüfung der für RpcProxy-Verbindungen verwendeten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="be877-232">This filtering layer allows for inspecting the interface used for RpcProxy connections.</span></span> <span data-ttu-id="be877-233">Dabei handelt es sich um eine Filter Ebene im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="be877-233">This is a user-mode filtering layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-234"><span id="FWPM_LAYER_KM_AUTHORIZATION"></span><span id="fwpm_layer_km_authorization"></span>**Autorisierung für die Authentifizierung mit der \_ Ebene \_ km \_**</span><span class="sxs-lookup"><span data-stu-id="be877-234"><span id="FWPM_LAYER_KM_AUTHORIZATION"></span><span id="fwpm_layer_km_authorization"></span>**FWPM\_LAYER\_KM\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-235">Diese Filter Ebene ermöglicht die Autorisierungs Einrichtung von Sicherheits Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="be877-235">This filtering layer allows for authorizing security association establishment.</span></span>

<span data-ttu-id="be877-236">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-236">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-237"><span id="FWPM_LAYER_NAME_RESOLUTION_CACHE_V4___FWPM_LAYER_NAME_RESOLUTION_CACHE_V6"></span><span id="fwpm_layer_name_resolution_cache_v4___fwpm_layer_name_resolution_cache_v6"></span>**Auflösung der swpm \_ \_ -Ebenenname \_ \_ -Auflösung Cache \_ V4/swpm- \_ \_ Ebenenname- \_ \_ Cache \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-237"><span id="FWPM_LAYER_NAME_RESOLUTION_CACHE_V4___FWPM_LAYER_NAME_RESOLUTION_CACHE_V6"></span><span id="fwpm_layer_name_resolution_cache_v4___fwpm_layer_name_resolution_cache_v6"></span>**FWPM\_LAYER\_NAME\_RESOLUTION\_CACHE\_V4 / FWPM\_LAYER\_NAME\_RESOLUTION\_CACHE\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-238">Diese Filter Ebene ermöglicht die Abfrage der Namen, die vor kurzem vom System aufgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-238">This filtering layer allows for querying the names recently resolved by the system.</span></span>

<span data-ttu-id="be877-239">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-239">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-240"><span id="FWPM_LAYER_ALE_RESOURCE_RELEASE_V4___FWPM_LAYER_ALE_RESOURCE_RELEASE_V6"></span><span id="fwpm_layer_ale_resource_release_v4___fwpm_layer_ale_resource_release_v6"></span>**Swpm \_ Layer \_ ALE \_ \_ -Ressourcen Release \_ V4/f \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be877-240"><span id="FWPM_LAYER_ALE_RESOURCE_RELEASE_V4___FWPM_LAYER_ALE_RESOURCE_RELEASE_V6"></span><span id="fwpm_layer_ale_resource_release_v4___fwpm_layer_ale_resource_release_v6"></span>**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V4 / FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-241">Diese Filter Ebene ermöglicht das Freigeben von Ressourcen, die zuvor zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="be877-241">This filtering layer allows for resources previously allocated to be released.</span></span>

<span data-ttu-id="be877-242">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-242">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-243"><span id="FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4___FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6"></span><span id="fwpm_layer_ale_endpoint_closure_v4___fwpm_layer_ale_endpoint_closure_v6"></span>**F/a \_ \_ \_ \_ -Endpunkt Schließung \_ \_ \_ \_ \_ \_ der swpm-Schicht**</span><span class="sxs-lookup"><span data-stu-id="be877-243"><span id="FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4___FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6"></span><span id="fwpm_layer_ale_endpoint_closure_v4___fwpm_layer_ale_endpoint_closure_v6"></span>**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V4 / FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-244">Diese Filter Ebene ermöglicht das Nachverfolgen der Deaktivierung des verbundenen TCP-Flows oder der UDP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="be877-244">This filtering layer allows for tracking de-activation of connected TCP flow or UDP sockets.</span></span>

<span data-ttu-id="be877-245">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-245">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-246"><span id="FWPM_LAYER_ALE_CONNECT_REDIRECT_V4___FWPM_LAYER_ALE_CONNECT_REDIRECT_V6"></span><span id="fwpm_layer_ale_connect_redirect_v4___fwpm_layer_ale_connect_redirect_v6"></span>**F & # amp; \_ quer-Layer \_ \_ \_ -Connect \_ -Umleitung V4/bwpm \_ Schicht- \_ \_ Verbindungs \_ Umleitung \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-246"><span id="FWPM_LAYER_ALE_CONNECT_REDIRECT_V4___FWPM_LAYER_ALE_CONNECT_REDIRECT_V6"></span><span id="fwpm_layer_ale_connect_redirect_v4___fwpm_layer_ale_connect_redirect_v6"></span>**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 / FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-247">Diese Filter Ebene ermöglicht die Änderung von Adressen und Ports auf der Bindungs \_ Ebene der Umleitung.</span><span class="sxs-lookup"><span data-stu-id="be877-247">This filtering layer allows for modification of addresses and ports at the bind\_redirect layer.</span></span>

<span data-ttu-id="be877-248">Für TCP können die lokale Adresse und/oder der lokale Port sowie die Remote Adresse und/oder der Remoteport geändert werden.</span><span class="sxs-lookup"><span data-stu-id="be877-248">For TCP, the local address and/or local port as well as the remote address and/or remote port can be modified.</span></span>

<span data-ttu-id="be877-249">Für UDP können die lokale Adresse und/oder der lokale Port geändert werden.</span><span class="sxs-lookup"><span data-stu-id="be877-249">For UDP, the local address and/or local port can be modified.</span></span>

<span data-ttu-id="be877-250">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-250">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-251"><span id="FWPM_LAYER_ALE_BIND_REDIRECT_V4___FWPM_LAYER_ALE_BIND_REDIRECT_V6"></span><span id="fwpm_layer_ale_bind_redirect_v4___fwpm_layer_ale_bind_redirect_v6"></span>**F/a \_ \_ -Layer \_ \_ -Bind \_ -Umleitung V4-/b-ebenenbindung \_ \_ \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="be877-251"><span id="FWPM_LAYER_ALE_BIND_REDIRECT_V4___FWPM_LAYER_ALE_BIND_REDIRECT_V6"></span><span id="fwpm_layer_ale_bind_redirect_v4___fwpm_layer_ale_bind_redirect_v6"></span>**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 / FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-252">Diese Filter Ebene ermöglicht die Änderung von BIND ()-und Connect ()-aufrufen sowie die Auswahl von Host Routen.</span><span class="sxs-lookup"><span data-stu-id="be877-252">This filtering layer allows for modification of bind() and connect() calls and selection of host routes.</span></span>

<span data-ttu-id="be877-253">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-253">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be877-254"><span id="FWPM_LAYER_STREAM_PACKET_V4___FWPM_LAYER_STREAM_PACKET_V6"></span><span id="fwpm_layer_stream_packet_v4___fwpm_layer_stream_packet_v6"></span>**F & # amp; amp; amp; amp \_ \_ \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be877-254"><span id="FWPM_LAYER_STREAM_PACKET_V4___FWPM_LAYER_STREAM_PACKET_V6"></span><span id="fwpm_layer_stream_packet_v4___fwpm_layer_stream_packet_v6"></span>**FWPM\_LAYER\_STREAM\_PACKET\_V4 / FWPM\_LAYER\_STREAM\_PACKET\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be877-255">Diese Filter Ebene ermöglicht die Überprüfung von TCP-Paketen einschließlich Hand Shake-und Fluss Steuerungs Austausch.</span><span class="sxs-lookup"><span data-stu-id="be877-255">This filtering layer allows for inspection of TCP packets including handshake and flow control exchanges.</span></span>

<span data-ttu-id="be877-256">Weitere Informationen finden Sie unter [ALE Ebenen](ale-layers.md) .</span><span class="sxs-lookup"><span data-stu-id="be877-256">See [ALE Layers](ale-layers.md) for more information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be877-257">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be877-257">Remarks</span></span>

<span data-ttu-id="be877-258">Diese filterebenenbezeichner werden auch als Bezeichner für die Verwaltung von ebenenbezeichlern bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="be877-258">These filtering layer identifiers are also referred to as management filtering layer identifiers.</span></span> <span data-ttu-id="be877-259">Die WFP-API enthält auch eine Reihe von [Lauf Zeit filterebenenbezeichlern](/windows-hardware/drivers/network/management-filtering-layer-identifiers), die im Windows-Treiberkit (WDK) dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="be877-259">WFP API also contains a set of [run-time filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers), documented in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="be877-260">Ebenenidentifizierer für die Lauf Zeit Filterung sind LUIDs und daher kleiner, nur 64 Bits im Vergleich zu den Verwaltungs ebenenbezeichern der Verwaltung, die 128 Bits groß sind.</span><span class="sxs-lookup"><span data-stu-id="be877-260">Run-time filtering layer identifiers are LUIDs, and therefore are smaller, only 64 bits in size, compared to the management filtering layer identifiers, which are 128 bits in size.</span></span>

<span data-ttu-id="be877-261">Ebenenbezeichner für die Verwaltung und Lauf Zeit Filterung auf die gleichen Ebenen.</span><span class="sxs-lookup"><span data-stu-id="be877-261">Management filtering layer identifiers and run-time filtering layer identifiers point to the same layers.</span></span>

<span data-ttu-id="be877-262">Bezeichner für die verwaltungfilterebenenkennung werden von Funktionen verwendet, die mit der Basis Filter-Engine (BFE) über den Benutzermodus oder den Kernel Modus (z. b. [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)) interagieren.</span><span class="sxs-lookup"><span data-stu-id="be877-262">Management filtering layer identifiers are used by functions that interact with the Base Filtering Engine (BFE) from either user mode or kernel mode (for example, [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)).</span></span>

<span data-ttu-id="be877-263">Ebenenbezeichner für die Lauf Zeit Filterung werden von Funktionen verwendet, die mit der Filter-Engine aus dem Kernel Modus interagieren (z. b. [FwpsFlowAssociateContext0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsflowassociatecontext0), [FwpsStreamInjectAsync0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsstreaminjectasync0)), und in Datenstrukturen, die direkt aus dem Kernel stammen (z. b. " [**swpm \_ net \_ Event \_ klassifizieren" \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0)).</span><span class="sxs-lookup"><span data-stu-id="be877-263">Run-time filtering layer identifiers are used by functions that interact with the filter engine from kernel mode only (for example, [FwpsFlowAssociateContext0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsflowassociatecontext0), [FwpsStreamInjectAsync0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpsstreaminjectasync0)), and in data structures that come directly from the kernel (for example, [**FWPM\_NET\_EVENT\_CLASSIFY\_DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0)).</span></span>

## <a name="requirements"></a><span data-ttu-id="be877-264">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be877-264">Requirements</span></span>



| <span data-ttu-id="be877-265">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be877-265">Requirement</span></span> | <span data-ttu-id="be877-266">Wert</span><span class="sxs-lookup"><span data-stu-id="be877-266">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be877-267">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be877-267">Minimum supported client</span></span><br/> | <span data-ttu-id="be877-268">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be877-268">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="be877-269">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be877-269">Minimum supported server</span></span><br/> | <span data-ttu-id="be877-270">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be877-270">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be877-271">Header</span><span class="sxs-lookup"><span data-stu-id="be877-271">Header</span></span><br/>                   | <dl> <span data-ttu-id="be877-272"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="be877-272"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be877-273">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be877-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be877-274">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="be877-274">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="be877-275">WFP-Architektur</span><span class="sxs-lookup"><span data-stu-id="be877-275">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> </dl>

