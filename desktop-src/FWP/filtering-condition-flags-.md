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
# <a name="filtering-condition-flags"></a><span data-ttu-id="35730-103">Filtern von Bedingungs Flags</span><span class="sxs-lookup"><span data-stu-id="35730-103">Filtering Condition Flags</span></span>

<span data-ttu-id="35730-104">Die Filter Bedingungs Flags der Windows-Filter Plattform (WFP) werden jeweils durch ein Bitfeld dargestellt.</span><span class="sxs-lookup"><span data-stu-id="35730-104">The Windows Filtering Platform (WFP) filtering condition flags are each represented by a bitfield.</span></span>

<span data-ttu-id="35730-105">Diese Flags und die Filter Ebenen, in denen Sie verwendet werden können, werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="35730-105">These flags and the filtering layers where they can be used are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="35730-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ Loopback**</span><span class="sxs-lookup"><span data-stu-id="35730-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-107">Testet, ob der Netzwerk Datenverkehr Loopback-Datenverkehr ist.</span><span class="sxs-lookup"><span data-stu-id="35730-107">Tests if the network traffic is loopback traffic.</span></span>

<span data-ttu-id="35730-108">Filter Ebenen:</span><span class="sxs-lookup"><span data-stu-id="35730-108">Filtering layers:</span></span>

-   <span data-ttu-id="35730-109">WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-109">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-110">WPM- \_ Ebene \_ ausgehende \_ ippacket \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-110">FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-111">WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-111">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-112">Ausgehender Transport der WPM- \_ Schicht \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-112">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-113">WPM- \_ \_ ebenenstream \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-113">FWPM\_LAYER\_STREAM\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-114">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-114">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="35730-115">Eingehende ICMP-Fehler in der WPM- \_ Schicht \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-115">FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-116">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-116">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="35730-117">\_ \_ Ausgehender \_ ICMP- \_ Fehler \_ V {4 \| 6} für die WPM-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-117">FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-118">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-118">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="35730-119">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-119">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-120">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-120">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-121">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-121">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="35730-122">F & # amp; \_ \_ \_ \_ \_ 4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-122">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-123">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-123">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ IPSec- \_ geschützt**</span><span class="sxs-lookup"><span data-stu-id="35730-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_SECURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-125">Testet, ob der Netzwerk Datenverkehr durch IPSec geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="35730-125">Tests if the network traffic is protected by IPsec.</span></span>

<span data-ttu-id="35730-126">Filter Ebenen:</span><span class="sxs-lookup"><span data-stu-id="35730-126">Filtering layers:</span></span>

-   <span data-ttu-id="35730-127">WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-127">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-128">WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-128">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-129">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-129">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-130">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-130">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**das Flag der SWP- \_ Bedingung \_ \_ ist \_ reautorisieren.**</span><span class="sxs-lookup"><span data-stu-id="35730-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-132">Testet auf eine Richtlinien Änderung im Gegensatz zu einer neuen Verbindung.</span><span class="sxs-lookup"><span data-stu-id="35730-132">Tests for a policy change as opposed to a new connection.</span></span>

<span data-ttu-id="35730-133">Filter Ebenen:</span><span class="sxs-lookup"><span data-stu-id="35730-133">Filtering layers:</span></span>

-   <span data-ttu-id="35730-134">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-134">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-135">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-135">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP \_ - \_ bedingungsflag ist Platzhalter \_ \_ \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="35730-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-137">Testet, ob die Anwendung beim Binden an eine lokale Netzwerkadresse eine Platzhalter Adresse angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="35730-137">Tests if the application specified a wildcard address when binding to a local network address.</span></span>

<span data-ttu-id="35730-138">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-138">Filtering layer:</span></span>

-   <span data-ttu-id="35730-139">F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-139">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**das Flag der f \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35730-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-141">Testet, ob der lokale Endpunkt, der Datenverkehr sendet und empfängt, ein unformatierten Endpunkt ist.</span><span class="sxs-lookup"><span data-stu-id="35730-141">Tests if the local endpoint that is sending and receiving traffic is a raw endpoint.</span></span>

<span data-ttu-id="35730-142">Filter Ebenen:</span><span class="sxs-lookup"><span data-stu-id="35730-142">Filtering layers:</span></span>

-   <span data-ttu-id="35730-143">WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-143">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-144">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-144">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="35730-145">Ausgehender Transport der WPM- \_ Schicht \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-145">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-146">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-146">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="35730-147">Datagramm-Daten der WPM- \_ Ebene \_ \_ \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-147">FWPM\_LAYER\_DATAGRAM\_DATA\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="35730-148">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-148">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="35730-149">F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-149">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-150">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-150">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-151">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-151">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ Fragment**</span><span class="sxs-lookup"><span data-stu-id="35730-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-153">Testet, ob die \_ \_ an einen Legenden-Treiber übergebenen Struktur der Netzwerk Puffer Liste ein IP-Paket Fragment ist.</span><span class="sxs-lookup"><span data-stu-id="35730-153">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver is an IP packet fragment.</span></span>

<span data-ttu-id="35730-154">Filter Ebenen:</span><span class="sxs-lookup"><span data-stu-id="35730-154">Filtering layers:</span></span>

-   <span data-ttu-id="35730-155">WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-155">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-156">WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6} \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="35730-156">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}\_DISCARD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**Das \_ Flag der \_ SWP-Bedingung ist eine \_ \_ \_ fragmentgruppe**</span><span class="sxs-lookup"><span data-stu-id="35730-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-158">Testet, ob die \_ \_ an einen Legenden-Treiber übergebenen Struktur der Netzwerk Puffer Liste eine verknüpfte Liste von Paket Fragmenten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="35730-158">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver describes a linked list of packet fragments.</span></span>

<span data-ttu-id="35730-159">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-159">Filtering layer:</span></span>

-   <span data-ttu-id="35730-160">WPM- \_ Ebene \_ ipforward \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-160">FWPM\_LAYER\_IPFORWARD\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**das Flag für die SWP- \_ Bedingung \_ \_ ist \_ IPSec \_ natt \_ Reclassify.**</span><span class="sxs-lookup"><span data-stu-id="35730-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_NATT\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-162">Gibt an, dass das gleiche Paket auf der Transport Ebene erneut klassifiziert wird, wenn der IPSec-NAT-Shim den Wert des Remoteports übersetzt.</span><span class="sxs-lookup"><span data-stu-id="35730-162">Indicates that the same packet is being re-classified at the transport layer, when the IPsec NAT shim translates the remote port value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**Flag für die SWP- \_ Bedingung \_ erfordert die ALE- \_ \_ \_ Klassifizierung**</span><span class="sxs-lookup"><span data-stu-id="35730-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**FWP\_CONDITION\_FLAG\_REQUIRES\_ALE\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-164">Gibt an, dass das Paket auf der ALE-Empfangs-/akzep-Ebene neu klassifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="35730-164">Indicates that the packet will be reclassified at the ALE receive/accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**das Flag der SWP- \_ Bedingung \_ ist eine \_ \_ implizite \_ Bindung.**</span><span class="sxs-lookup"><span data-stu-id="35730-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_IMPLICIT\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-166">Testet, ob Windows Sockets eine implizite Bindung ausführt.</span><span class="sxs-lookup"><span data-stu-id="35730-166">Tests if Windows Sockets is performing an implicit bind.</span></span>

<span data-ttu-id="35730-167">Nur unter Windows Vista und Windows Server 2008 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-167">Available only on Windows Vista and Windows Server 2008.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**das Flag für die SWP- \_ Bedingung \_ \_ wird wieder \_ zusammengefügt**</span><span class="sxs-lookup"><span data-stu-id="35730-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**FWP\_CONDITION\_FLAG\_IS\_REASSEMBLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-169">Testet, ob das Paket neu zusammengefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="35730-169">Tests if the packet has been reassembled.</span></span>

> [!Note]  
> <span data-ttu-id="35730-170">Nur unter Windows Server 2008, Windows Vista mit SP1 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-170">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

 

<span data-ttu-id="35730-171">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-171">Filtering layer:</span></span>

-   <span data-ttu-id="35730-172">WPM- \_ Schicht, \_ eingehender \_ ippacket \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-172">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**SWP-Bedingungs Kennzeichen \_ \_ \_ ist \_ namens- \_ App \_ angegeben**</span><span class="sxs-lookup"><span data-stu-id="35730-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**FWP\_CONDITION\_FLAG\_IS\_NAME\_APP\_SPECIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-174">Testet, ob der Name des Peer Computers, mit dem die Anwendung eine Verbindung herstellt, über eine API wie [**wsasetsocketpeertargetname**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) empfangen wurde und nicht über die cacheheuristik abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="35730-174">Tests if the name of the peer machine that the application is expecting to connect to has been received via an API such as [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) and not obtained via the caching heuristics.</span></span>

> [!Note]  
> <span data-ttu-id="35730-175">Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-175">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="35730-176">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-176">Filtering layer:</span></span>

-   <span data-ttu-id="35730-177">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-177">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**das Flag für die SWP- \_ Bedingung \_ \_ ist \_ Promiscuous**</span><span class="sxs-lookup"><span data-stu-id="35730-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**FWP\_CONDITION\_FLAG\_IS\_PROMISCUOUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-179">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="35730-179">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**Flag für die SWP- \_ Bedingung \_ \_ ist \_ auth \_ FW**</span><span class="sxs-lookup"><span data-stu-id="35730-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**FWP\_CONDITION\_FLAG\_IS\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-181">Testet, ob die Verbindung durch End-to-End-Authentifizierung authentifiziert ist, auch wenn die einzelnen Pakete nicht überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="35730-181">Tests if the connection is end-to-end authenticated, even if the individual packets have not been verified.</span></span>

> [!Note]  
> <span data-ttu-id="35730-182">Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-182">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="35730-183">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-183">Filtering layer:</span></span>

-   <span data-ttu-id="35730-184">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-184">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-185">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-185">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**das Flag der SWP- \_ Bedingung \_ \_ ist \_ neu klassifizieren.**</span><span class="sxs-lookup"><span data-stu-id="35730-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-187">Testet, ob die Filter-Engine eine vorherige Bindungs-oder Abhör Anforderung neu klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="35730-187">Tests if the filtering engine is reclassifying a previous bind or listen request.</span></span>

> [!Note]  
> <span data-ttu-id="35730-188">Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-188">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="35730-189">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-189">Filtering layer:</span></span>

-   <span data-ttu-id="35730-190">Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-190">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-191">F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-191">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**das Flag der SWP- \_ Bedingung \_ ist eine \_ \_ Proxy \_ Verbindung.**</span><span class="sxs-lookup"><span data-stu-id="35730-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-193">Testet, ob die Verbindung einen Proxy verwendet.</span><span class="sxs-lookup"><span data-stu-id="35730-193">Tests if the connection uses a proxy.</span></span>

> [!Note]  
> <span data-ttu-id="35730-194">Nur unter Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-194">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**Das BWP-Bedingungs Kennzeichen \_ \_ ist " \_ \_ appcontainer \_ Loopback".**</span><span class="sxs-lookup"><span data-stu-id="35730-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-196">Testet, ob der Netzwerk Datenverkehr App-Container Loopback-Datenverkehr ist.</span><span class="sxs-lookup"><span data-stu-id="35730-196">Tests if the network traffic is app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="35730-197">Nur unter Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-197">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**das Flag der BWP- \_ Bedingung \_ \_ ist \_ kein \_ appcontainer- \_ Loopback.**</span><span class="sxs-lookup"><span data-stu-id="35730-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-199">Testet, ob der Netzwerk Datenverkehr nicht-APP-Container Loopback-Datenverkehr ist.</span><span class="sxs-lookup"><span data-stu-id="35730-199">Tests if the network traffic is non-app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="35730-200">Nur unter Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-200">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**das Flag der SWP- \_ Bedingung \_ \_ ist \_ reserviert.**</span><span class="sxs-lookup"><span data-stu-id="35730-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**FWP\_CONDITION\_FLAG\_IS\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-202">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="35730-202">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**das Flag der SWP- \_ Bedingung \_ ist die \_ \_ \_ Autorisierung der Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="35730-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-204">Gibt an, dass die aktuelle Klassifizierung ausgeführt wird, um die Absicht zu berücksichtigen, dass eine umgeleitete Windows Store-App eine Verbindung mit einem angegebenen Host herstellt.</span><span class="sxs-lookup"><span data-stu-id="35730-204">Indicates that the current classification is being performed to honor the intention of a redirected Windows Store app to connect to a specified host.</span></span> <span data-ttu-id="35730-205">Eine solche Klassifizierung enthält die gleichen klassifizierbaren Feldwerte, als ob die APP nie umgeleitet würde.</span><span class="sxs-lookup"><span data-stu-id="35730-205">Such a classification will contain the same classifiable field values as if the app were never redirected.</span></span> <span data-ttu-id="35730-206">Das-Flag gibt auch an, dass eine zukünftige Klassifizierung aufgerufen wird, um das effektive umgeleitete Ziel abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="35730-206">The flag also indicates that a future classification will be invoked to match the effective redirected destination.</span></span> <span data-ttu-id="35730-207">Wenn die APP zur Überprüfung an einen Proxy Dienst umgeleitet wird, bedeutet dies auch, dass für die Proxy Verbindung eine zukünftige Klassifizierung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="35730-207">If the app is redirected to a proxy service for inspection, it also means a future classification will be invoked on the proxy connection.</span></span> <span data-ttu-id="35730-208">Callout-Treiber sollten diese Klassifizierung im allgemeinen erlauben.</span><span class="sxs-lookup"><span data-stu-id="35730-208">Callout drivers should generally allow this classification.</span></span>

> [!Note]  
> <span data-ttu-id="35730-209">Nur unter Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-209">Available only on Windows 8 and Windows Server 2012.</span></span>

 

<span data-ttu-id="35730-210">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-210">Filtering layer:</span></span>

-   <span data-ttu-id="35730-211">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-211">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="35730-212">Die folgenden Flags geben den Grund für die Neuautorisierung einer zuvor autorisierten Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="35730-212">The following flags specify the reason for reauthorizing a previously authorized connection.</span></span> <span data-ttu-id="35730-213">Diese Flags und die Filter Ebenen, in denen Sie verwendet werden können, werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="35730-213">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="35730-214">Diese Filterbedingungen sind nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-214">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="35730-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**Änderung der \_ Grundrichtlinie für die \_ erneute Autorisierung der \_ Grundbedingung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35730-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-216">Gibt an, dass die Verbindung aufgrund von hinzugefügten oder entfernten Filtern erneut autorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="35730-216">Indicates that the connection was reauthorized due to filters being added or removed.</span></span>

<span data-ttu-id="35730-217">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-217">Filtering layer:</span></span>

-   <span data-ttu-id="35730-218">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-218">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-219">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-219">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**Grund für \_ die \_ Neuautorisierung der Grundbedingung für die \_ \_ neue \_ Ankunfts \_ Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="35730-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_ARRIVAL\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-221">Gibt an, dass das Paket von einer unbekannten Schnittstelle eingetroffen ist.</span><span class="sxs-lookup"><span data-stu-id="35730-221">Indicates that the packet has arrived from an unknown interface.</span></span>

<span data-ttu-id="35730-222">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-222">Filtering layer:</span></span>

-   <span data-ttu-id="35730-223">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-223">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-224">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-224">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**Grund für die erneute \_ \_ Autorisierung der \_ Grundbedingung \_ neuer \_ nexthop- \_ Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="35730-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_NEXTHOP\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-226">Gibt an, dass das Paket von einer unbekannten Schnittstelle abweicht.</span><span class="sxs-lookup"><span data-stu-id="35730-226">Indicates that the packet will be departing from an unknown interface.</span></span>

<span data-ttu-id="35730-227">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-227">Filtering layer:</span></span>

-   <span data-ttu-id="35730-228">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-228">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-229">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-229">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**Grund für \_ die \_ erneute Autorisierung des \_ Grund Profils der Grundbedingung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35730-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_PROFILE\_CROSSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-231">Gibt an, dass das Paket Schnittstellen von mehr als einer Netzwerk Kategorie überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="35730-231">Indicates that the packet has passed through interfaces of more than one network category.</span></span>

<span data-ttu-id="35730-232">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-232">Filtering layer:</span></span>

-   <span data-ttu-id="35730-233">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-233">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-234">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-234">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**Grund für \_ die \_ Neuautorisierung der Grundbedingung für die \_ \_ Klassifizierung \_**</span><span class="sxs-lookup"><span data-stu-id="35730-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_CLASSIFY\_COMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-236">Gibt an, dass eine zuvor gehaltene Verbindung jetzt zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="35730-236">Indicates that a previously held connection is now being allowed to complete.</span></span>

<span data-ttu-id="35730-237">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-237">Filtering layer:</span></span>

-   <span data-ttu-id="35730-238">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-238">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-239">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-239">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**Grund für \_ \_ erneute Autorisierung der Grundbedingungen für \_ \_ IPSec- \_ Eigenschaften \_**</span><span class="sxs-lookup"><span data-stu-id="35730-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_IPSEC\_PROPERTIES\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-241">Gibt an, dass die IPsec-Eigenschaften geändert wurden oder dass sich die Verbindung von Klartext in eine sichere Verbindung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="35730-241">Indicates that IPsec properties have changed, or that the connection has changed from clear text to a secure connection.</span></span>

<span data-ttu-id="35730-242">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-242">Filtering layer:</span></span>

-   <span data-ttu-id="35730-243">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-243">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-244">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-244">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**Grund für \_ die \_ erneute Autorisierung der Grundbedingung für die Daten \_ \_ \_ Strom Überprüfung \_**</span><span class="sxs-lookup"><span data-stu-id="35730-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_MID\_STREAM\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-246">Gibt an, dass eine zuvor festgelegte TCP-Verbindung jetzt überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="35730-246">Indicates that a previously established TCP connection is now being inspected.</span></span>

<span data-ttu-id="35730-247">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-247">Filtering layer:</span></span>

-   <span data-ttu-id="35730-248">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-248">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-249">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-249">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**Grund für \_ die \_ erneute Autorisierung von \_ Grundbedingungen \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35730-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_SOCKET\_PROPERTY\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-251">Gibt an, dass die socketeigenschaften festgelegt wurden, nachdem eine Verbindung autorisiert und eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="35730-251">Indicates that socket properties have been set after a connection was authorized and established.</span></span>

<span data-ttu-id="35730-252">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-252">Filtering layer:</span></span>

-   <span data-ttu-id="35730-253">WPM- \_ Schicht-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-253">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-254">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-254">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**Grund für \_ \_ Neuautorisierung \_ Grund für \_ neuen \_ eingehenden \_ mcast- \_ Bcast \_ Paket**</span><span class="sxs-lookup"><span data-stu-id="35730-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_INBOUND\_MCAST\_BCAST\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-256">Gibt an, dass neue eingehende Multicast-oder Broadcast Pakete bei Alen recv Accept-aufrufen erneut autorisiert werden \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35730-256">Indicates that new inbound multicast or broadcast packets are being re-authorized at ALE\_RECV\_ACCEPT callouts.</span></span>

<span data-ttu-id="35730-257">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-257">Filtering layer:</span></span>

-   <span data-ttu-id="35730-258">Abbild-e-v \_ \_ \_ \_ \_ \_ {4 \| 6} für die-zwpm-Schicht-ALE Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="35730-258">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="35730-259">Die folgenden Flags geben socketeigenschaften an, die sich darauf beziehen, ob eine Anwendung Edge-Traversal-Datenverkehr empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="35730-259">The following flags specify socket properties which are related to whether an application wants to receive Edge Traversal traffic.</span></span> <span data-ttu-id="35730-260">Diese Flags und die Filter Ebenen, in denen Sie verwendet werden können, werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="35730-260">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="35730-261">Diese Filterbedingungen sind nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-261">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="35730-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**Flag für die Eigenschaft "SWP \_ Condition \_ Socket" \_ \_ \_ ist \_ System \_ Port \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="35730-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_IS\_SYSTEM\_PORT\_RPC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-263">Gibt an, dass die Anwendung mit einem dynamischen RPC-Port kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="35730-263">Indicates that the application is communicating with a dynamic RPC port.</span></span>

<span data-ttu-id="35730-264">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-264">Filtering layer:</span></span>

-   <span data-ttu-id="35730-265">Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-265">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-266">F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-266">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**SWP-Eigenschaft für den \_ \_ \_ socketeigenschaft " \_ \_ \_ Edge \_ "**</span><span class="sxs-lookup"><span data-stu-id="35730-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_ALLOW\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-268">Gibt an, dass die Anwendung edgetraversal-spezifischen Datenverkehr empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="35730-268">Indicates that the application wants to receive edge traversal-specific traffic.</span></span>

<span data-ttu-id="35730-269">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-269">Filtering layer:</span></span>

-   <span data-ttu-id="35730-270">Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-270">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-271">F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-271">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**SWP-Eigenschaft für das \_ \_ Socket- \_ Eigenschafts \_ Flag " \_ \_ Edge \_**</span><span class="sxs-lookup"><span data-stu-id="35730-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_DENY\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-273">Gibt an, dass die Anwendung keinen Edge-Traversal-spezifischen Datenverkehr empfangen oder verarbeiten möchte.</span><span class="sxs-lookup"><span data-stu-id="35730-273">Indicates that the application does not want to receive or process edge traversal-specific traffic.</span></span>

<span data-ttu-id="35730-274">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-274">Filtering layer:</span></span>

-   <span data-ttu-id="35730-275">Lwpm \_ Layer \_ ALE \_ auth \_ lauschen \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-275">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="35730-276">F $- \_ \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="35730-276">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="35730-277">Die folgenden Flags geben Verbindungsdetails im Zusammenhang mit der L2-Filterung an.</span><span class="sxs-lookup"><span data-stu-id="35730-277">The following flags specify connection details related to L2 filtering.</span></span>

> [!Note]  
> <span data-ttu-id="35730-278">Diese Filterbedingungen sind nur unter Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35730-278">These filtering conditions are available only on Windows 8 and Windows Server 2012.</span></span>

 

<dl> <dt>

<span data-ttu-id="35730-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**Die f- \_ Bedingung \_ L2 \_ ist \_ natives \_ Ethernet.**</span><span class="sxs-lookup"><span data-stu-id="35730-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-280">Gibt an, dass die Verbindung Native Ethernet ist.</span><span class="sxs-lookup"><span data-stu-id="35730-280">Indicates that the connection is native Ethernet.</span></span>

<span data-ttu-id="35730-281">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-281">Filtering layer:</span></span>

-   <span data-ttu-id="35730-282">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-282">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-283">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-283">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-284">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-284">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-285">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-285">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi**</span><span class="sxs-lookup"><span data-stu-id="35730-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP\_CONDITION\_L2\_IS\_WIFI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-287">Gibt an, dass die Verbindung Wi-Fi ist.</span><span class="sxs-lookup"><span data-stu-id="35730-287">Indicates that the connection is Wi-Fi.</span></span>

<span data-ttu-id="35730-288">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-288">Filtering layer:</span></span>

-   <span data-ttu-id="35730-289">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-289">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-290">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-290">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-291">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-291">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-292">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-292">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**F WP- \_ Bedingung \_ L2 \_ ist \_ mobiles \_ Breitband**</span><span class="sxs-lookup"><span data-stu-id="35730-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-294">Gibt an, dass die Verbindung ein mobiles Breitband ist.</span><span class="sxs-lookup"><span data-stu-id="35730-294">Indicates that the connection is mobile broadband.</span></span>

<span data-ttu-id="35730-295">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-295">Filtering layer:</span></span>

-   <span data-ttu-id="35730-296">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-296">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-297">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-297">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-298">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-298">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-299">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-299">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi Direct- \_ \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="35730-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-301">Gibt an, dass die Verbindung Wi-Fi Direct ist.</span><span class="sxs-lookup"><span data-stu-id="35730-301">Indicates that the connection is Wi-Fi Direct.</span></span>

<span data-ttu-id="35730-302">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-302">Filtering layer:</span></span>

-   <span data-ttu-id="35730-303">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-303">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-304">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-304">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-305">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-305">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-306">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-306">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**F- \_ Bedingung \_ L2 \_ ist \_ VM2VM**</span><span class="sxs-lookup"><span data-stu-id="35730-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP\_CONDITION\_L2\_IS\_VM2VM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-308">Gibt an, dass die Verbindung zwischen virtuellen Computern besteht.</span><span class="sxs-lookup"><span data-stu-id="35730-308">Indicates that the connection is between virtual machines.</span></span>

<span data-ttu-id="35730-309">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-309">Filtering layer:</span></span>

-   <span data-ttu-id="35730-310">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-310">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-311">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-311">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-312">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-312">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-313">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-313">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**Die f- \_ Bedingung \_ L2 \_ ist \_ falsch \_ formatiertes Paket.**</span><span class="sxs-lookup"><span data-stu-id="35730-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-315">Gibt an, dass ein Paket falsch formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="35730-315">Indicates that a packet appears to be malformed.</span></span>

<span data-ttu-id="35730-316">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-316">Filtering layer:</span></span>

-   <span data-ttu-id="35730-317">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-317">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-318">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-318">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-319">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-319">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-320">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-320">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**\_ \_ \_ \_ SWP-Bedingung L2 ist IP- \_ \_ fragmentgruppe**</span><span class="sxs-lookup"><span data-stu-id="35730-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-322">Gibt eine IP-Paket fragmentgruppe an.</span><span class="sxs-lookup"><span data-stu-id="35730-322">Indicates an IP packet fragment group.</span></span>

<span data-ttu-id="35730-323">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-323">Filtering layer:</span></span>

-   <span data-ttu-id="35730-324">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-324">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-325">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-325">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-326">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-326">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-327">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-327">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35730-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**SWP- \_ Bedingung \_ L2, \_ Wenn \_ Connector \_ vorhanden ist**</span><span class="sxs-lookup"><span data-stu-id="35730-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35730-329">Gibt an, dass ein Connector vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35730-329">Indicates that a connector is present.</span></span>

<span data-ttu-id="35730-330">Filter Ebene:</span><span class="sxs-lookup"><span data-stu-id="35730-330">Filtering layer:</span></span>

-   <span data-ttu-id="35730-331">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="35730-331">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-332">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="35730-332">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="35730-333">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-333">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="35730-334">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="35730-334">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35730-335">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35730-335">Requirements</span></span>



| <span data-ttu-id="35730-336">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35730-336">Requirement</span></span> | <span data-ttu-id="35730-337">Wert</span><span class="sxs-lookup"><span data-stu-id="35730-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35730-338">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35730-338">Minimum supported client</span></span><br/> | <span data-ttu-id="35730-339">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35730-339">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35730-340">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35730-340">Minimum supported server</span></span><br/> | <span data-ttu-id="35730-341">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35730-341">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35730-342">Header</span><span class="sxs-lookup"><span data-stu-id="35730-342">Header</span></span><br/>                   | <dl> <span data-ttu-id="35730-343"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="35730-343"><dt>Fwptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35730-344">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35730-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35730-345">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="35730-345">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

