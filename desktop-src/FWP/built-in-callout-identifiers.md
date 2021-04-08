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
# <a name="built-in-callout-identifiers"></a><span data-ttu-id="92812-104">Integrierte Legenden Bezeichner</span><span class="sxs-lookup"><span data-stu-id="92812-104">Built-in Callout Identifiers</span></span>

<span data-ttu-id="92812-105">Die Bezeichner für die Legenden Funktionen, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="92812-105">The identifiers for the callout functions that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="92812-106">Diese Bezeichner werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="92812-106">These identifiers are defined as follows.</span></span>

<span data-ttu-id="92812-107">Die v4-und V6-Suffixe am Ende der Legenden Bezeichner geben an, ob die Legende dem IPv4-Netzwerk Stapel oder dem IPv6-Netzwerk Stapel entspricht.</span><span class="sxs-lookup"><span data-stu-id="92812-107">The V4 and V6 suffixes at the end of the callout identifiers indicate whether the callout is for the IPv4 network stack or for the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="92812-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**Swpm \_ Callout \_ IPSec \_ Inbound \_ Transport \_ V4/swpm \_ Callout \_ IPSec \_ Inbound \_ Transport \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-109">Mit dieser Option wird überprüft, ob jedes empfangene Paket, das über eine Transportmodus-Sicherheits Zuordnung eingehen soll, sicher ankommt.</span><span class="sxs-lookup"><span data-stu-id="92812-109">Verifies that each received packet that is supposed to arrive over a transport mode security association arrives securely.</span></span>

<span data-ttu-id="92812-110">Diese Legende ist auf der Transportschicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92812-110">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**WPM-Legende \_ \_ IPSec-ausgehende \_ \_ Transport \_ V4/f-Legende \_ IPSec-ausgehenden \_ \_ \_ Transport \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-112">Gibt IPSec den ausgehenden Datenverkehr an, der über Transportmodus-Sicherheits Zuordnungen geschützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="92812-112">Indicates to IPsec the outbound traffic that must be secured over transport mode security associations.</span></span>

<span data-ttu-id="92812-113">Diese Legende ist auf der Transportschicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92812-113">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**WPM-Legende \_ \_ IPSec \_ -Eingangs \_ Tunnel \_ V4/bwpm Legende \_ \_ IPSec- \_ Eingangs \_ Tunnel \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-115">Überprüft, ob jedes empfangene Paket, das über eine Tunnel Modus-Sicherheits Zuordnung eingehen soll, sicher eintrifft.</span><span class="sxs-lookup"><span data-stu-id="92812-115">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="92812-116">Diese Legende ist auf der Transportschicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92812-116">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**WPM-Legenden \_ \_ -IPSec \_ -ausgehender \_ Tunnel \_ V4/f-Legende \_ \_ IPSec- \_ \_ Tunnel \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-118">Gibt IPSec den ausgehenden Datenverkehr an, der über Tunnel Modus-Sicherheits Zuordnungen geschützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="92812-118">Indicates to IPsec the outbound traffic that must be secured over tunnel mode security associations.</span></span>

<span data-ttu-id="92812-119">Diese Legende ist auf der Transportschicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92812-119">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**WPM-Legende \_ \_ IPSec \_ Forward \_ Inbound \_ Tunnel \_ V4/bwpm \_ Callout \_ IPSec \_ Forward \_ Inbound \_ Tunnel \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-121">Überprüft, ob jedes empfangene Paket, das über eine Tunnel Modus-Sicherheits Zuordnung eingehen soll, sicher eintrifft.</span><span class="sxs-lookup"><span data-stu-id="92812-121">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="92812-122">Diese Legende ist auf der Weiterleitungs Ebene anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92812-122">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**WPM-Legende \_ \_ IPSec \_ Forward \_ -ausgehender \_ Tunnel \_ V4/bwpm \_ Callout \_ IPSec \_ Forward \_ Outbound \_ Tunnel \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-124">Gibt IPSec den ausgehenden Datenverkehr an, der über eine Tunnel Modus-Sicherheits Zuordnung geschützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="92812-124">Indicates to IPsec the outbound traffic that must be secured over a tunnel mode security association.</span></span>

<span data-ttu-id="92812-125">Diese Legende ist auf der Weiterleitungs Ebene anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92812-125">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**WPM \_ \_ -Legende IPSec eingehend \_ initiieren \_ von \_ Secure \_ V4/f-Legende \_ \_ IPSec eingehend \_ initiieren von \_ \_ Secure \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-127">Stellt sicher, dass jede eingehende Verbindung, die sicher eintreffen soll, sicher ankommt.</span><span class="sxs-lookup"><span data-stu-id="92812-127">Verifies that each incoming connection that is supposed to arrive secure arrives securely.</span></span>

<span data-ttu-id="92812-128">Diese Legende ist auf der Ebene der ALE-Annahme anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92812-128">This callout is applicable at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**WPM \_ \_ -Legende IPSec \_ -eingehende \_ Tunnel \_ ALE \_ Annahme \_ V4/f-Legende \_ \_ IPSec- \_ eingehende \_ Tunnel \_ ALE \_ akzeptieren \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-130">Ermöglicht die IP-in-IP-Pakete für den IPSec-Tunnel Modus, wenn diese auf der Ebene der ALE-Annahme klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="92812-130">Permits the IPsec tunnel mode IP-in-IP packets when they get classified at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**WPM-Legende \_ \_ IPSec \_ -ALE \_ Connect \_ V4/f-Legende \_ \_ IPSec \_ ALE \_ Verbindung \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V4 / FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-132">Wendet IPSec-richtlinienmodifiziererer auf Client Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="92812-132">Applies IPsec policy modifiers to client applications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**WPM-Legende \_ \_ IPSec \_ DoSP \_ Forward \_ V4/WPM \_ Callout \_ IPSec \_ DoSP \_ Forward \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V4 / FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-134">Signalisiert dem IPSec-DOS-Schutz, dass der Datenverkehr auf potenzielle DOS überprüft werden muss und möglicherweise eine Raten Beschränkung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="92812-134">Signals to IPsec DoS Protection that traffic needs to be verified for potential DoS and may need to be rate limited.</span></span>

> [!Note]  
> <span data-ttu-id="92812-135">Nur in Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92812-135">Available only in Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**\_ \_ WPM-Legende WFP- \_ \_ Transportschicht \_ V4 \_ automatische \_ Drop/WPM-Legende \_ \_ WFP- \_ Transport \_ Schicht \_ V6 \_ Silent \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="92812-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V4\_SILENT\_DROP / FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V6\_SILENT\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-137">Implementiert die Filterung im verborgenen Modus, indem alle eingehenden Pakete, für die TCP keinen Überwachungs Endpunkt hat, automatisch gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="92812-137">Implements stealth-mode filtering by silently dropping all incoming packets for which TCP does not have a listening endpoint.</span></span>

<span data-ttu-id="92812-138">Diese Legende gilt für die eingehende Transport Verwerfungs Schicht.</span><span class="sxs-lookup"><span data-stu-id="92812-138">This callout is applicable at the inbound transport discard layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**WPM-Legende \_ von \_ TCP \_ Chimney \_ Connect \_ Layer \_ V4/f WPM \_ Callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-140">Aktiviert oder deaktiviert die TCP-Chimney-Abladung für jede ausgehende Verbindung.</span><span class="sxs-lookup"><span data-stu-id="92812-140">Enables or disables TCP chimney offload for each outgoing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**F \_ -Callout \_ -TCP \_ \_ -Chimney \_ -Accept \_ -Ebene V4/f \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92812-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-142">Aktiviert oder deaktiviert die TCP-Chimney-Abladung für jede eingehende Verbindung.</span><span class="sxs-lookup"><span data-stu-id="92812-142">Enables or disables TCP chimney offload for each incoming connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**F & # # amp; \_ \_ querset \_ Optionen \_ auth \_ Connect \_ Layer \_ V4/f WPM \_ Callout \_ Set \_ options \_ auth \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-144">Legt klassifiziereroptionen für ausgehende Flows fest.</span><span class="sxs-lookup"><span data-stu-id="92812-144">Sets classify options on outbound flows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**F-Legenden \_ \_ Satz \_ Optionen \_ auth \_ recv \_ Accept \_ Layer \_ V4/f WPM \_ Callout \_ Set \_ options \_ auth \_ recv \_ Accept \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-146">Legt klassifiziereroptionen für eingehende Flows fest.</span><span class="sxs-lookup"><span data-stu-id="92812-146">Sets classify options on inbound flows.</span></span>

> [!Note]  
> <span data-ttu-id="92812-147">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92812-147">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**Abrufbare Authentifizierung für die abrufbare Authentifizierung mit der BPM \_ \_ \_ \_ \_ \_ - \_ \_ \_ \_ \_ \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="92812-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-149">Dieser Bezeichner ist für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="92812-149">This identifier is reserved for internal use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**Der Edge-Over-over-over \_ \_ -down-Monitor \_ \_ \_ \_ v6/f- \_ \_ Legende Teredo- \_ ALE \_ lauscht \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-151">Signalisiert dem Teredo-Dienst, dass eine Anwendung eine Teredo-Adresse benötigt.</span><span class="sxs-lookup"><span data-stu-id="92812-151">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="92812-152">Verwenden Sie für Windows 7 und höher den Windows-Legenden Befehl Edge-out-over-over-Monitor **\_ \_ \_ \_ \_ \_ V6**.</span><span class="sxs-lookup"><span data-stu-id="92812-152">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**F WPM \_ -Legende \_ Edge \_ \_ \_ \_ -Ressourcenzuweisung \_ V6/swpm \_ \_ Legende Teredo \_ ALE- \_ Ressourcen \_ Zuweisung \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-154">Signalisiert dem Teredo-Dienst, dass eine Anwendung eine Teredo-Adresse benötigt.</span><span class="sxs-lookup"><span data-stu-id="92812-154">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="92812-155">Verwenden Sie für Windows 7 und höher die WPM-Legende " **\_ Edge- \_ \_ \_ \_ Ressourcen \_ Zuweisung \_ (Edge**)".</span><span class="sxs-lookup"><span data-stu-id="92812-155">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**\_Swpm-Legende \_ Edge- \_ \_ \_ Ressourcen \_ Zuweisung \_ v4**</span><span class="sxs-lookup"><span data-stu-id="92812-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V4**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-157">Dieser Bezeichner ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="92812-157">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**\_Auschecken der \_ Edge- \_ \_ \_ Edgeausnahme \_**</span><span class="sxs-lookup"><span data-stu-id="92812-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V4**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-159">Dieser Bezeichner ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="92812-159">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**WPM-Legende \_ von \_ TCP \_ \_ -Vorlagen Connect \_ Layer \_ V4/f-Legenden Verbindungs \_ \_ \_ \_ \_ Ebene \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-161">Wendet TCP-Vorlagen Einstellungen für übereinstimmende ausgehende Verbindungen an.</span><span class="sxs-lookup"><span data-stu-id="92812-161">Applies TCP template settings for matching outgoing connections.</span></span>

> [!Note]  
> <span data-ttu-id="92812-162">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92812-162">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92812-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**Von den WPM-Legenden in den \_ \_ TCP \_ \_ -Vorlagen accept \_ Layer \_ V4/f-Legende \_ TCP- \_ \_ Vorlagen \_ akzeptieren \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="92812-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92812-164">Wendet TCP-Vorlagen Einstellungen für eingehende Verbindungen an.</span><span class="sxs-lookup"><span data-stu-id="92812-164">Applies TCP template settings for matching incoming connections.</span></span>

> [!Note]  
> <span data-ttu-id="92812-165">Nur in Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92812-165">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92812-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92812-166">Requirements</span></span>



| <span data-ttu-id="92812-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92812-167">Requirement</span></span> | <span data-ttu-id="92812-168">Wert</span><span class="sxs-lookup"><span data-stu-id="92812-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92812-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92812-169">Minimum supported client</span></span><br/> | <span data-ttu-id="92812-170">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92812-170">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92812-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92812-171">Minimum supported server</span></span><br/> | <span data-ttu-id="92812-172">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92812-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92812-173">Header</span><span class="sxs-lookup"><span data-stu-id="92812-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="92812-174"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="92812-174"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





