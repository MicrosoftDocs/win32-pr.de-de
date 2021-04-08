---
title: Filtern von Bedingungs bezeichlern ("f")
description: Die Filter Bedingungs Bezeichner der Windows-Filter Plattform (WFP) werden jeweils durch eine GUID dargestellt.
ms.assetid: 4f0b970a-e511-4107-8023-22a8775905b9
topic_type:
- apiref
api_name:
- FWPM_CONDITION_INTERFACE_MAC_ADDRESS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS
- FWPM_CONDITION_MAC_REMOTE_ADDRESS
- FWPM_CONDITION_ETHER_TYPE
- FWPM_CONDITION_VLAN_ID
- FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID
- FWPM_CONDITION_NDIS_PORT
- FWPM_CONDITION_NDIS_MEDIA_TYPE
- FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE
- FWPM_CONDITION_L2_FLAGS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_SOURCE_ADDRESS
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS
- FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_SOURCE_PORT
- FWPM_CONDITION_VSWITCH_ICMP_TYPE
- FWPM_CONDITION_IP_DESTINATION_PORT
- FWPM_CONDITION_VSWITCH_ICMP_CODE
- FWPM_CONDITION_VSWITCH_ID
- FWPM_CONDITION_VSWITCH_NETWORK_TYPE
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_SOURCE_VM_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE
- FWPM_CONDITION_INTERFACE
- FWPM_CONDITION_ALE_PACKAGE_ID
- FWPM_CONDITION_ALE_ORIGINAL_APP_ID
- FWPM_CONDITION_IP_NEXTHOP_ADDRESS
- FWPM_CONDITION_IP_NEXTHOP_INTERFACE
- FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE
- FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE
- FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX
- FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ORIGINAL_PROFILE_ID
- FWPM_CONDITION_CURRENT_PROFILE_ID
- FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID
- FWPM_CONDITION_REAUTHORIZE_REASON
- FWPM_CONDITION_ALE_REAUTH_REASON
- FWPM_CONDITION_ORIGINAL_ICMP_TYPE
- FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE
- FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE
- FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH
- FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY
- FWPM_CONDITION_IP_ARRIVAL_INTERFACE
- FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE
- FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE
- FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX
- FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_TYPE
- FWPM_CONDITION_LOCAL_TUNNEL_TYPE
- FWPM_CONDITION_IP_LOCAL_ADDRESS
- FWPM_CONDITION_IP_REMOTE_ADDRESS
- FWPM_CONDITION_IP_SOURCE_ADDRESS
- FWPM_CONDITION_IP_DESTINATION_ADDRESS
- FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_LOCAL_INTERFACE
- FWPM_CONDITION_INTERFACE_TYPE
- FWPM_CONDITION_TUNNEL_TYPE
- FWPM_CONDITION_IP_FORWARD_INTERFACE
- FWPM_CONDITION_IP_PROTOCOL
- FWPM_CONDITION_IP_LOCAL_PORT
- FWPM_CONDITION_ICMP_TYPE
- FWPM_CONDITION_IP_REMOTE_PORT
- FWPM_CONDITION_ICMP_CODE
- FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS
- FWPM_CONDITION_EMBEDDED_PROTOCOL
- FWPM_CONDITION_EMBEDDED_LOCAL_PORT
- FWPM_CONDITION_EMBEDDED_REMOTE_PORT
- FWPM_CONDITION_FLAGS
- FWPM_CONDITION_DIRECTION
- FWPM_CONDITION_INTERFACE_INDEX
- FWPM_CONDITION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ALE_APP_ID
- FWPM_CONDITION_ALE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_MACHINE_ID
- FWPM_CONDITION_ALE_PROMISCUOUS_MODE
- FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT
- FWPM_CONDITION_ALE_NAP_CONTEXT
- FWPM_CONDITION_QM_MODE
- FWPM_CONDITION_KM_AUTH_NAP_CONTEXT
- FWPM_CONDITION_PEER_NAME
- FWPM_CONDITION_REMOTE_ID
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_KM_TYPE
- FWPM_CONDITION_KM_MODE
- FWPM_CONDITION_IPSEC_POLICY_KEY
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_REMOTE_USER_TOKEN
- FWPM_CONDITION_RPC_IF_UUID
- FWPM_CONDITION_RPC_IF_VERSION
- FWPM_CONDITION_RPC_IF_FLAG
- FWPM_CONDITION_DCOM_APP_ID
- FWPM_CONDITION_IMAGE_NAME
- FWPM_CONDITION_RPC_PROTOCOL
- FWPM_CONDITION_RPC_AUTH_TYPE
- FWPM_CONDITION_RPC_AUTH_LEVEL
- FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM
- FWPM_CONDITION_SEC_KEY_SIZE
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V4
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V6
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V4
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V6
- FWPM_CONDITION_PIPE
- FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID
- FWPM_CONDITION_RPC_EP_VALUE
- FWPM_CONDITION_RPC_EP_FLAGS
- FWPM_CONDITION_CLIENT_TOKEN
- FWPM_CONDITION_RPC_SERVER_NAME
- FWPM_CONDITION_RPC_SERVER_PORT
- FWPM_CONDITION_RPC_PROXY_AUTH_TYPE
- FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH
- FWPM_CONDITION_CLIENT_CERT_OID
- FWPM_CONDITION_NET_EVENT_TYPE
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617946e5708bb982f96edcad155bcbf2509596dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739848"
---
# <a name="filtering-condition-identifiers"></a><span data-ttu-id="b49b4-103">Filtern von Bedingungs bezeichlern</span><span class="sxs-lookup"><span data-stu-id="b49b4-103">Filtering Condition Identifiers</span></span>

<span data-ttu-id="b49b4-104">Die Filter Bedingungs Bezeichner der Windows-Filter Plattform (WFP) werden jeweils durch eine **GUID** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b49b4-104">The Windows Filtering Platform (WFP) filtering condition identifiers are each represented by a **GUID**.</span></span> <span data-ttu-id="b49b4-105">Der Datentyp für den Bedingungs Wert für jede Filterbedingung wird als ein [**\_ \_ Datentyp vom Typ "f**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-105">The data type for the condition value for each filtering condition is specified as an [**FWP\_DATA\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="b49b4-106">Diese Bezeichner und deren Datentypen werden hier definiert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-106">These identifiers and their data types are defined here.</span></span>

<span data-ttu-id="b49b4-107">Die Standardbedingungen werden zuerst aufgeführt, gefolgt von den Bedingungen für den Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="b49b4-107">The standard conditions are listed first, followed by the conditions specific to user mode.</span></span> <span data-ttu-id="b49b4-108">Bedingungen werden nach dem unterstützten Betriebssystem gruppiert, sodass Sie leicht erkennen können, welche Bedingungen für ein bestimmtes Betriebssystem unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b49b4-108">Conditions are grouped by supported operating system, so that you can easily tell which conditions are supported for a given OS.</span></span>

> [!Note]  
> <span data-ttu-id="b49b4-109">Jede der folgenden Filterbedingungen ist nur in einer Teilmenge der WFP-Filter Ebenen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b49b4-109">Each of the following filtering conditions is available only at a subset of the WFP filtering layers.</span></span> <span data-ttu-id="b49b4-110">Weitere Informationen zur Verfügbarkeit der einzelnen Bedingungen auf einer beliebigen Ebene finden Sie unter [**Filterbedingungen, die auf jeder Filter Ebene verfügbar**](filtering-conditions-available-at-each-filtering-layer.md)sind.</span><span class="sxs-lookup"><span data-stu-id="b49b4-110">For more information on each condition's availability at any given layer, see [**Filtering Conditions Available at Each Filtering Layer**](filtering-conditions-available-at-each-filtering-layer.md).</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b49b4-111">Für Windows 8 und Windows Server 2012 verfügbare Bedingungen</span><span class="sxs-lookup"><span data-stu-id="b49b4-111">Conditions available for Windows 8 and Windows Server 2012</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b49b4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49b4-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <span data-ttu-id="b49b4-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-114">Die Mac-Adresse einer bestimmten lokalen Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b49b4-114">The MAC address of a particular local interface.</span></span><br/> <span data-ttu-id="b49b4-115"><strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-115"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <span data-ttu-id="b49b4-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-117">Die Zieladresse eines eingehenden Frames oder die Quelladresse eines ausgehenden Frames.</span><span class="sxs-lookup"><span data-stu-id="b49b4-117">Destination address of an inbound frame, or source address of an outbound frame.</span></span><br/> <span data-ttu-id="b49b4-118"><strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-118"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <span data-ttu-id="b49b4-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-120">Die Quelladresse eines eingehenden Frames oder die Zieladresse eines ausgehenden Frames.</span><span class="sxs-lookup"><span data-stu-id="b49b4-120">Source address of an inbound frame, or destination address of an outbound frame.</span></span><br/> <span data-ttu-id="b49b4-121"><strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-121"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <span data-ttu-id="b49b4-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-123">Der Netzwerk Nutz Last Datentyp von Ethernet v2.</span><span class="sxs-lookup"><span data-stu-id="b49b4-123">The Ethernet V2 network payload data type.</span></span> <span data-ttu-id="b49b4-124">(Weitere Informationen finden Sie unter ETHERNET_TYPE_IPV4 usw. in "nettiodef. h".)</span><span class="sxs-lookup"><span data-stu-id="b49b4-124">(See ETHERNET_TYPE_IPV4, etc. in netiodef.h.)</span></span><br/> <span data-ttu-id="b49b4-125"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-125"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <span data-ttu-id="b49b4-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-127">Der 16-Bit-VLAN-Header einschließlich der Felder "vid", "CFI" und "Priority" gemäß 802.1 q-Standard (Weitere Informationen finden Sie unter VLAN_TAG in "netiodef. h" für die Positionen der Bitfields).</span><span class="sxs-lookup"><span data-stu-id="b49b4-127">The 16-bits of VLAN header including the VID, CFI, and Priority fields as per the 802.1q standard (see VLAN_TAG in netiodef.h for the positions of the bitfields).</span></span><br/> <span data-ttu-id="b49b4-128"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-128"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <span data-ttu-id="b49b4-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-130">Eindeutiger Bezeichner für das Vswitch-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b49b4-130">Unique identifier for the vSwitch network.</span></span> <span data-ttu-id="b49b4-131">Kann nicht zusammen mit VLAN_IDs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b49b4-131">Cannot be used in conjunction with VLAN_IDs.</span></span><br/> <span data-ttu-id="b49b4-132"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-132"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <span data-ttu-id="b49b4-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-134">Die Portnummer des NDIS-Ports.</span><span class="sxs-lookup"><span data-stu-id="b49b4-134">The port number of the NDIS port.</span></span><br/> <span data-ttu-id="b49b4-135"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-135"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <span data-ttu-id="b49b4-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-137">Der Medientyp des NDIS-Ports.</span><span class="sxs-lookup"><span data-stu-id="b49b4-137">The media type of the NDIS port.</span></span><br/> <span data-ttu-id="b49b4-138"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-138"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="b49b4-139"><strong>Mögliche Werte:</strong> Einer der <strong>NDIS_MEDIUM</strong> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-139"><strong>Possible values:</strong> Any of the <strong>NDIS_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="b49b4-140">(Siehe ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="b49b4-140">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <span data-ttu-id="b49b4-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-142">Der physische Medientyp des NDIS-Ports.</span><span class="sxs-lookup"><span data-stu-id="b49b4-142">The physical media type of the NDIS port.</span></span><br/> <span data-ttu-id="b49b4-143"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-143"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="b49b4-144"><strong>Mögliche Werte:</strong> Einer der <strong>NDIS_PHYSICAL_MEDIUM</strong> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-144"><strong>Possible values:</strong> Any of the <strong>NDIS_PHYSICAL_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="b49b4-145">(Siehe ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="b49b4-145">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <span data-ttu-id="b49b4-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-147">Eine bitweise OR-Kombination von filterbedingungs-Flags.</span><span class="sxs-lookup"><span data-stu-id="b49b4-147">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="b49b4-148"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-148"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="b49b4-149"><strong>Mögliche Werte:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-149"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span><span class="sxs-lookup"><span data-stu-id="b49b4-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span></span></li>
<li><span data-ttu-id="b49b4-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="b49b4-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span></span></li>
<li><span data-ttu-id="b49b4-152">FWP_CONDITION_L2_IS_WIFI</span><span class="sxs-lookup"><span data-stu-id="b49b4-152">FWP_CONDITION_L2_IS_WIFI</span></span></li>
<li><span data-ttu-id="b49b4-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span><span class="sxs-lookup"><span data-stu-id="b49b4-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <span data-ttu-id="b49b4-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-155">Der adrestyp der physischen lokalen Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-155">The address type of the physical local address.</span></span><br/> <span data-ttu-id="b49b4-156"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-156"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="b49b4-157"><strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-157"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="b49b4-158">Dlunicast</span><span class="sxs-lookup"><span data-stu-id="b49b4-158">DlUnicast</span></span></li>
<li><span data-ttu-id="b49b4-159">Dlmulticast</span><span class="sxs-lookup"><span data-stu-id="b49b4-159">DlMulticast</span></span></li>
<li><span data-ttu-id="b49b4-160">Dlbroadcast</span><span class="sxs-lookup"><span data-stu-id="b49b4-160">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <span data-ttu-id="b49b4-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-162">Der Adresstyp der physischen Remote Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-162">The address type of the physical remote address.</span></span><br/> <span data-ttu-id="b49b4-163"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-163"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="b49b4-164"><strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-164"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="b49b4-165">Dlunicast</span><span class="sxs-lookup"><span data-stu-id="b49b4-165">DlUnicast</span></span></li>
<li><span data-ttu-id="b49b4-166">Dlmulticast</span><span class="sxs-lookup"><span data-stu-id="b49b4-166">DlMulticast</span></span></li>
<li><span data-ttu-id="b49b4-167">Dlbroadcast</span><span class="sxs-lookup"><span data-stu-id="b49b4-167">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <span data-ttu-id="b49b4-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-169">Die physische Quelladresse eines Frames.</span><span class="sxs-lookup"><span data-stu-id="b49b4-169">The physical source address of a frame.</span></span><br/> <span data-ttu-id="b49b4-170"><strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-170"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <span data-ttu-id="b49b4-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-172">Die physische Zieladresse eines Frames.</span><span class="sxs-lookup"><span data-stu-id="b49b4-172">The physical destination address of a frame.</span></span><br/> <span data-ttu-id="b49b4-173"><strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-173"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <span data-ttu-id="b49b4-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-175">Der adreetstyp der physischen Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-175">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="b49b4-176"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-176"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="b49b4-177"><strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-177"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="b49b4-178">Dlunicast</span><span class="sxs-lookup"><span data-stu-id="b49b4-178">DlUnicast</span></span></li>
<li><span data-ttu-id="b49b4-179">Dlmulticast</span><span class="sxs-lookup"><span data-stu-id="b49b4-179">DlMulticast</span></span></li>
<li><span data-ttu-id="b49b4-180">Dlbroadcast</span><span class="sxs-lookup"><span data-stu-id="b49b4-180">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <span data-ttu-id="b49b4-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-182">Der adreetstyp der physischen Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-182">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="b49b4-183"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-183"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="b49b4-184"><strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-184"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="b49b4-185">Dlunicast</span><span class="sxs-lookup"><span data-stu-id="b49b4-185">DlUnicast</span></span></li>
<li><span data-ttu-id="b49b4-186">Dlmulticast</span><span class="sxs-lookup"><span data-stu-id="b49b4-186">DlMulticast</span></span></li>
<li><span data-ttu-id="b49b4-187">Dlbroadcast</span><span class="sxs-lookup"><span data-stu-id="b49b4-187">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <span data-ttu-id="b49b4-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-189">Der Quellport des Paket Transports.</span><span class="sxs-lookup"><span data-stu-id="b49b4-189">The source port of the packet's transport.</span></span><br/> <span data-ttu-id="b49b4-190"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-190"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <span data-ttu-id="b49b4-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-192">Das Feld "ICMP Type", wie in RFC 792 angegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-192">The ICMP type field, as specified in RFC 792.</span></span><br/> <span data-ttu-id="b49b4-193"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-193"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <span data-ttu-id="b49b4-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-195">Der Zielport für den Transport des Pakets.</span><span class="sxs-lookup"><span data-stu-id="b49b4-195">The destination port of the packet's transport.</span></span><br/> <span data-ttu-id="b49b4-196"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-196"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <span data-ttu-id="b49b4-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-198">Das Feld "ICMP-Code", wie in RFC 792 angegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-198">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="b49b4-199"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-199"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <span data-ttu-id="b49b4-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-201">Eindeutiger Bezeichner einer Vswitch-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b49b4-201">Unique identifier of an vSwitch instance.</span></span><br/> <span data-ttu-id="b49b4-202"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-202"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <span data-ttu-id="b49b4-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-204">Gibt an, ob die Vswitch-Instanz Teil eines externen, internen oder privaten virtuellen Netzwerks ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-204">Specifies whether the vSwitch instance is part of an external, internal, or private virtual network.</span></span><br/> <span data-ttu-id="b49b4-205"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-205"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <span data-ttu-id="b49b4-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-207">Eindeutiger Bezeichner der Quelle des aktuellen Pakets.</span><span class="sxs-lookup"><span data-stu-id="b49b4-207">Unique identifier of the source of the current packet.</span></span> <span data-ttu-id="b49b4-208">(Der Name einer VM-NIC, P-NIC oder V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="b49b4-208">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="b49b4-209"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-209"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <span data-ttu-id="b49b4-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-211">Eindeutiger Bezeichner des Ziels des aktuellen Pakets.</span><span class="sxs-lookup"><span data-stu-id="b49b4-211">Unique identifier of the destination of the current packet.</span></span> <span data-ttu-id="b49b4-212">(Der Name einer VM-NIC, P-NIC oder V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="b49b4-212">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="b49b4-213"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-213"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <span data-ttu-id="b49b4-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-215">Eindeutiger Bezeichner der virtuellen Vswitch-Quell Maschine.</span><span class="sxs-lookup"><span data-stu-id="b49b4-215">Unique identifier of the vSwitch source virtual machine.</span></span><br/> <span data-ttu-id="b49b4-216"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-216"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <span data-ttu-id="b49b4-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-218">Eindeutiger Bezeichner des virtuellen Vswitch-Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-218">Unique identifier of the vSwitch destination virtual machine.</span></span><br/> <span data-ttu-id="b49b4-219"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-219"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <span data-ttu-id="b49b4-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-221">Der Schnittstellentyp der Quelle des aktuellen Pakets.</span><span class="sxs-lookup"><span data-stu-id="b49b4-221">Interface type of the source of the current packet.</span></span><br/> <span data-ttu-id="b49b4-222"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-222"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="b49b4-223"><strong>Mögliche Werte:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-223"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-224">Switchnicsyntheticnic (bei Schnittstellentyp VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="b49b4-224">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="b49b4-225">Switchnicemulatednic (bei Schnittstellentyp VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="b49b4-225">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="b49b4-226">Switchnicphysicalnic (bei einem Schnittstellentyp P-NIC)</span><span class="sxs-lookup"><span data-stu-id="b49b4-226">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="b49b4-227">Switchnicvnic (bei Schnittstellen Typ V-NIC, verbunden mit der Host Partition)</span><span class="sxs-lookup"><span data-stu-id="b49b4-227">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <span data-ttu-id="b49b4-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-229">Der Schnittstellentyp des Ziels des aktuellen Pakets.</span><span class="sxs-lookup"><span data-stu-id="b49b4-229">Interface type of the destination of the current packet.</span></span><br/> <span data-ttu-id="b49b4-230"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-230"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="b49b4-231"><strong>Mögliche Werte:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-231"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-232">Switchnicsyntheticnic (bei Schnittstellentyp VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="b49b4-232">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="b49b4-233">Switchnicemulatednic (bei Schnittstellentyp VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="b49b4-233">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="b49b4-234">Switchnicphysicalnic (bei einem Schnittstellentyp P-NIC)</span><span class="sxs-lookup"><span data-stu-id="b49b4-234">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="b49b4-235">Switchnicvnic (bei Schnittstellen Typ V-NIC, verbunden mit der Host Partition)</span><span class="sxs-lookup"><span data-stu-id="b49b4-235">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <span data-ttu-id="b49b4-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-237">Die LUID für die Netzwerkschnittstelle, die der lokalen IP-Adresse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-237">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="b49b4-238"><strong>Datentyp:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-238"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <span data-ttu-id="b49b4-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-240">Die Sicherheits-ID (SID) eines App-Containers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-240">The security identifier (SID) of an app container.</span></span><br/> <span data-ttu-id="b49b4-241"><strong>Datentyp:</strong> FWP_SID</span><span class="sxs-lookup"><span data-stu-id="b49b4-241"><strong>Data type:</strong> FWP_SID</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <span data-ttu-id="b49b4-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-243">Der voll qualifizierte Gerätepfad der Anwendung, z. b &quot; . \device0\hardiskvolume1\program Files\Application.exe&quot; .</span><span class="sxs-lookup"><span data-stu-id="b49b4-243">The fully qualified device path of the application, such as &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.</span></span> <span data-ttu-id="b49b4-244">Wenn eine Verbindung umgeleitet wurde, ist dies der Bezeichner der ursprünglichen app. Andernfalls ist dies identisch mit <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span><span class="sxs-lookup"><span data-stu-id="b49b4-244">When a connection has been redirected, this will be the identifier of the originating app; otherwise this will be the same as <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span></span><br/> <span data-ttu-id="b49b4-245"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-245"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
</tbody>
</table>





| <span data-ttu-id="b49b4-246">Für Windows 7, Windows Server 2008 R2 und höher verfügbare Bedingungen</span><span class="sxs-lookup"><span data-stu-id="b49b4-246">Conditions available for Windows 7, Windows Server 2008 R2, and later</span></span>                                                                                                                                                                                                    | <span data-ttu-id="b49b4-247">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49b4-247">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <span data-ttu-id="b49b4-248"><dt>**\_ \_ IP- \_ nexthop-Adresse der Bedingung für die IP- \_ Adresse**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-248"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_ADDRESS**</dt></span></span> </dl>                                             | <span data-ttu-id="b49b4-249">Die IP-Adresse der Schnittstelle für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b49b4-249">The IP address of the next-hop interface.</span></span><br/> <span data-ttu-id="b49b4-250">**Datentyp:** F/WP- \_ \_ addr- \_ Maske</span><span class="sxs-lookup"><span data-stu-id="b49b4-250">**Data type:** FWP\_V4\_ADDR\_MASK</span></span><br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <span data-ttu-id="b49b4-251"><dt>**\_ \_ IP- \_ \_ Schnittstellen Schnittstellen-Schnittstelle**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-251"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>                                       | <span data-ttu-id="b49b4-252">Die Schnittstelle für den nächsten Hop, von der das Paket abweicht.</span><span class="sxs-lookup"><span data-stu-id="b49b4-252">The next-hop interface from which the packet will be departing.</span></span> <br/> <span data-ttu-id="b49b4-253">**Datentyp:** F \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-253">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <span data-ttu-id="b49b4-254"><dt>**\_ \_ Dateityp "nexthop \_ - \_ Schnittstellentyp"**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-254"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_TYPE**</dt></span></span> </dl>                                 | <span data-ttu-id="b49b4-255">Der Schnittstellentyp der Schnittstelle für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b49b4-255">The interface type of the next-hop interface.</span></span><br/> <span data-ttu-id="b49b4-256">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-256">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <span data-ttu-id="b49b4-257"><dt>**\_ \_ Dateityp "nexthop \_ - \_ Tunneltyp"**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-257"><dt>**FWPM\_CONDITION\_NEXTHOP\_TUNNEL\_TYPE**</dt></span></span> </dl>                                          | <span data-ttu-id="b49b4-258">Der Tunneltyp der Schnittstelle für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b49b4-258">The tunnel type of the next-hop interface.</span></span><br/> <span data-ttu-id="b49b4-259">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-259">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <span data-ttu-id="b49b4-260"><dt>**Index für die twpm- \_ Bedingung \_ nexthop- \_ Schnittstelle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-260"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_INDEX**</dt></span></span> </dl>                              | <span data-ttu-id="b49b4-261">Der Schnittstellen Index der Schnittstelle für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b49b4-261">The interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="b49b4-262">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-262">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <span data-ttu-id="b49b4-263"><dt>**Index für die Unterschnittstelle der twpm- \_ Bedingung \_ nexthop \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-263"><dt>**FWPM\_CONDITION\_NEXTHOP\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl>                 | <span data-ttu-id="b49b4-264">Der unter Schnittstellen Index der Schnittstelle für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b49b4-264">The sub-interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="b49b4-265">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-265">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <span data-ttu-id="b49b4-266"><dt>**\_ursprüngliche Profil-ID der Bedingung für die \_ \_ Profilerstellung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-266"><dt>**FWPM\_CONDITION\_ORIGINAL\_PROFILE\_ID**</dt></span></span> </dl>                                          | <span data-ttu-id="b49b4-267">Die Netzwerk Kategorie der Ankunfts-oder der nächsten Hop-Schnittstelle, über die der ALE Datenfluss (eingehend oder ausgehend) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b49b4-267">The network category of the arrival or next-hop interface through which the ALE flow (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="b49b4-268">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-268">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <span data-ttu-id="b49b4-269"><dt>**\_ \_ ID der aktuellen Profil- \_ \_ ID der Bedingung**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-269"><dt>**FWPM\_CONDITION\_CURRENT\_PROFILE\_ID**</dt></span></span> </dl>                                             | <span data-ttu-id="b49b4-270">Die Netzwerk Kategorie der Ankunfts-oder der nächsten Hop-Schnittstelle, über die das aktuelle Paket (eingehend oder ausgehend) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b49b4-270">The network category of the arrival or next-hop interface through which the current packet (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="b49b4-271">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-271">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <span data-ttu-id="b49b4-272"><dt>**\_Profil-ID der \_ lokalen \_ Profil erstellungsschnittstelle \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-272"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>                    | <span data-ttu-id="b49b4-273">Die Netzwerk Kategorie der Übermittlungs Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b49b4-273">The network category of the delivery interface.</span></span><br/> <span data-ttu-id="b49b4-274">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-274">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <span data-ttu-id="b49b4-275"><dt>**Profil-ID für die Profilerstellung für die \_ \_ \_ Benutzeroberfläche \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-275"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="b49b4-276">Die Netzwerk Kategorie der Ankunfts Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b49b4-276">The network category of the arrival interface.</span></span><br/> <span data-ttu-id="b49b4-277">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-277">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <span data-ttu-id="b49b4-278"><dt>**ID der TPM-Bedingungs \_ \_ \_ Schnittstellen \_ Profil- \_ ID**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-278"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="b49b4-279">Die Netzwerk Kategorie der Schnittstelle für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b49b4-279">The network category of the next-hop interface.</span></span><br/> <span data-ttu-id="b49b4-280">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-280">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <span data-ttu-id="b49b4-281"><dt>**\_ \_ Grund für Neuautorisierung der \_ Grundbedingungen**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-281"><dt>**FWPM\_CONDITION\_REAUTHORIZE\_REASON**</dt></span></span> </dl>                                              | <span data-ttu-id="b49b4-282">Der Grund für die Neuautorisierung einer zuvor autorisierten Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b49b4-282">The reason for reauthorizing a previously authorized connection.</span></span><br/> <span data-ttu-id="b49b4-283">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-283">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <span data-ttu-id="b49b4-284"><dt>**Grund für den \_ Grund für die \_ \_ \_ Grundursache der Grundbedingungen**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-284"><dt>**FWPM\_CONDITION\_ALE\_REAUTH\_REASON**</dt></span></span> </dl>                                                | <span data-ttu-id="b49b4-285">Der Grund für die Neuautorisierung einer zuvor autorisierten Verbindung, wie z. b. eine erneute Autorisierung der **\_ Grundrichtlinie für die \_ \_ Grund \_ Richtlinie \_** (oder einer der anderen Werte, die unter Filtern von Bedingungs [**Flags**](filtering-condition-flags-.md)aufgeführt sind).</span><span class="sxs-lookup"><span data-stu-id="b49b4-285">The reason for reauthorizing a previously authorized connection, such as **FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE** (or one of the other values listed in [**Filtering Condition Flags**](filtering-condition-flags-.md)).</span></span><br/> <span data-ttu-id="b49b4-286">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-286">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <span data-ttu-id="b49b4-287"><dt>**\_ \_ ursprünglicher \_ ICMP- \_ Typ der Datei Bedingung**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-287"><dt>**FWPM\_CONDITION\_ORIGINAL\_ICMP\_TYPE**</dt></span></span> </dl>                                             | <span data-ttu-id="b49b4-288">Der ICMP-Typ, mit dem der Flow erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b49b4-288">The ICMP type with which the flow was created.</span></span><br/> <span data-ttu-id="b49b4-289">**Datentyp:** F \_ UInt16</span><span class="sxs-lookup"><span data-stu-id="b49b4-289">**Data type:** FWP\_UINT16</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <span data-ttu-id="b49b4-290"><dt>**\_ \_ IP-Adresse der \_ physischen Eingangs \_ \_ Schnittstelle der Bedingung**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-290"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="b49b4-291">Die LUID der physischen Schnittstelle, die der Ankunfts-IP-Adresse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-291">The LUID of the physical interface associated with the arrival IP address.</span></span><br/> <span data-ttu-id="b49b4-292">**Datentyp:** F \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-292">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <span data-ttu-id="b49b4-293"><dt>**WPM \_ -Bedingung \_ IP \_ Physical \_ nexthop \_ Interface**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-293"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="b49b4-294">Die LUID der physischen Schnittstelle des nächsten Hops.</span><span class="sxs-lookup"><span data-stu-id="b49b4-294">The LUID of the physical interface of the next hop.</span></span><br/> <span data-ttu-id="b49b4-295">**Datentyp:** F \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-295">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <span data-ttu-id="b49b4-296"><dt>**Quarantäne-Epoche der Bedingung für die Bedingungs \_ \_ Schnittstelle \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-296"><dt>**FWPM\_CONDITION\_INTERFACE\_QUARANTINE\_EPOCH**</dt></span></span> </dl>                     | <span data-ttu-id="b49b4-297">Die einer Schnittstelle zugeordnete Epochen Anzahl.</span><span class="sxs-lookup"><span data-stu-id="b49b4-297">The epoch count associated with an interface.</span></span> <span data-ttu-id="b49b4-298">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-298">Reserved.</span></span><br/> <span data-ttu-id="b49b4-299">**Datentyp:** F \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-299">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <span data-ttu-id="b49b4-300"><dt>**swpm \_ Condition \_ ALE \_ die \_ Firewall \_ - \_ socketeigenschaft**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-300"><dt>**FWPM\_CONDITION\_ALE\_SIO\_FIREWALL\_SOCKET\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="b49b4-301">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-301">Reserved for internal use.</span></span> <br/> <span data-ttu-id="b49b4-302">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-302">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                              |





| <span data-ttu-id="b49b4-303">Verfügbare Konstanten für Windows Vista mit SP1, Windows Server 2008 und höher</span><span class="sxs-lookup"><span data-stu-id="b49b4-303">Constants available for Windows Vista with SP1, Windows Server 2008, and later</span></span>                                                                                                                                                                           | <span data-ttu-id="b49b4-304">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49b4-304">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <span data-ttu-id="b49b4-305"><dt>**\_ \_ IP-Ankunfts Schnittstelle der Bedingung für die \_ \_ Benutzeroberfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-305"><dt>**FWPM\_CONDITION\_IP\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>                       | <span data-ttu-id="b49b4-306">Die LUID für die Netzwerkschnittstelle, die der Ankunfts-IP-Adresse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-306">The LUID for the network interface associated with the arrival IP address.</span></span> <br/> <span data-ttu-id="b49b4-307">**Datentyp:** F \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-307">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <span data-ttu-id="b49b4-308"><dt>**Typ der Eingangs \_ Schnittstelle für die \_ \_ Benutzeroberfläche \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-308"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                 | <span data-ttu-id="b49b4-309">Der Typ der Netzwerkschnittstelle für die Ankunft, wie von der Internet Assigned Names Authority (IANA) definiert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-309">The type of the arrival network interface as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="b49b4-310">Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="b49b4-310">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="b49b4-311">**Mögliche Werte:** Die Schnittstellentyp Werte, die in der Header Datei "ipifcons. h" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b49b4-311">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="b49b4-312">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-312">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <span data-ttu-id="b49b4-313"><dt>"F" **\_ \_ \_ \_ Typ** des Bedingungs Eingangs Tunnels</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-313"><dt> **FWPM\_CONDITION\_ARRIVAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="b49b4-314">Die Kapselungs Methode, die von einem Tunnel verwendet wird, der der Ankunfts Netzwerkschnittstelle zugeordnet ist, wenn der Typmember bei einem \_ \_ typtunnel ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-314">The encapsulation method used by a tunnel associated with the arrival network interface if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="b49b4-315">Der Tunneltyp wird durch die Internet Assigned Names Authority (IANA) definiert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-315">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="b49b4-316">Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="b49b4-316">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="b49b4-317">**Mögliche Werte:** Der \_ Typ der Tunneltyp-Enumeration, die in der ifdef. h-Header Datei aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b49b4-317">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="b49b4-318">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-318">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <span data-ttu-id="b49b4-319"><dt>**Index für die \_ Eingangs \_ Schnittstelle der einstellungsschnittstelle \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-319"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_INDEX**</dt></span></span> </dl>              | <span data-ttu-id="b49b4-320">Der Index der Netzwerkschnittstelle für die Ankunft, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-320">The index of the arrival network interface, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="b49b4-321">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-321">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <span data-ttu-id="b49b4-322"><dt>**Index für die Eingangs \_ subschnittstelle der Bedingung für die \_ \_ unter \_ Schnittstelle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-322"><dt>**FWPM\_CONDITION\_ARRIVAL\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl> | <span data-ttu-id="b49b4-323">Der Index der Netzwerkschnittstelle für die Ankunft, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-323">The index of the arrival network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="b49b4-324">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-324">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <span data-ttu-id="b49b4-325"><dt>**\_ \_ Index der lokalen Index- \_ Schnittstelle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-325"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_INDEX**</dt></span></span> </dl>                    | <span data-ttu-id="b49b4-326">Der Index der Netzwerkschnittstelle, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-326">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="b49b4-327">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-327">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <span data-ttu-id="b49b4-328"><dt>**\_ \_ lokaler \_ \_ Schnittstellentyp für die Bedingung**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-328"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="b49b4-329">Der Schnittstellentyp, wie er von der Internet Assigned Names Authority (IANA) definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b49b4-329">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="b49b4-330">Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="b49b4-330">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="b49b4-331">**Mögliche Werte:** Die Schnittstellentyp Werte, die in der Header Datei "ipifcons. h" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b49b4-331">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="b49b4-332">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-332">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <span data-ttu-id="b49b4-333"><dt>**\_ \_ lokaler \_ \_ Tunneltyp der WPM-Bedingung**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-333"><dt>**FWPM\_CONDITION\_LOCAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                                | <span data-ttu-id="b49b4-334">Die Kapselungs Methode, die von einem Tunnel verwendet wird, wenn der Typmember bei einem \_ \_ typtunnel ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-334">The encapsulation method used by a tunnel if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="b49b4-335">Der Tunneltyp wird durch die Internet Assigned Names Authority (IANA) definiert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-335">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="b49b4-336">Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="b49b4-336">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="b49b4-337">**Mögliche Werte:** Der \_ Typ der Tunneltyp-Enumeration, die in der ifdef. h-Header Datei aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b49b4-337">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="b49b4-338">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-338">**Data type:** FWP\_UINT32</span></span> <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b49b4-339">Für Windows Vista und höher verfügbare Konstanten</span><span class="sxs-lookup"><span data-stu-id="b49b4-339">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b49b4-340">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49b4-340">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <span data-ttu-id="b49b4-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-342">Die lokale IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-342">The local IP address.</span></span> <br/> <span data-ttu-id="b49b4-343"><strong>Datentyp:</strong> Für eine IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-343"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-344">FWP_V4_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-344">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-345">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-345">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-346"><strong>Datentyp:</strong> Für eine IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-346"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-347">FWP_V6_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-347">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-348">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-348">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <span data-ttu-id="b49b4-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-350">Die Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-350">The remote IP address.</span></span> <br/> <span data-ttu-id="b49b4-351"><strong>Datentyp:</strong> Für eine IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-351"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-352">FWP_V4_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-352">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-353">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-353">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-354"><strong>Datentyp:</strong> Für eine IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-354"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-355">FWP_V6_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-355">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-356">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-356">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <span data-ttu-id="b49b4-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-358">Die Quell-IP-Adresse für weitergeleitete Pakete.</span><span class="sxs-lookup"><span data-stu-id="b49b4-358">The source IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="b49b4-359"><strong>Datentyp:</strong> Für eine IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-359"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-360">FWP_V4_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-360">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-361">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-361">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-362"><strong>Datentyp:</strong> Für eine IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-362"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-363">FWP_V6_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-363">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-364">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-364">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <span data-ttu-id="b49b4-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-366">Die Ziel-IP-Adresse für weitergeleitete Pakete.</span><span class="sxs-lookup"><span data-stu-id="b49b4-366">The destination IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="b49b4-367"><strong>Datentyp:</strong> Für eine IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-367"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-368">FWP_V4_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-368">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-369">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-369">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-370"><strong>Datentyp:</strong> Für eine IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-370"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-371">FWP_V6_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-371">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-372">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-372">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <span data-ttu-id="b49b4-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-374">Der Typ der lokalen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-374">The local IP address type.</span></span> <br/> <span data-ttu-id="b49b4-375"><strong>Mögliche Werte:</strong> Eines der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-375"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="b49b4-376">Nlatunspezifiziert</span><span class="sxs-lookup"><span data-stu-id="b49b4-376">NlatUnspecified</span></span></li>
<li><span data-ttu-id="b49b4-377">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b49b4-377">NlatUnicast</span></span></li>
<li><span data-ttu-id="b49b4-378">Nlatanycast</span><span class="sxs-lookup"><span data-stu-id="b49b4-378">NlatAnycast</span></span></li>
<li><span data-ttu-id="b49b4-379">Nlatmulticast</span><span class="sxs-lookup"><span data-stu-id="b49b4-379">NlatMulticast</span></span></li>
<li><span data-ttu-id="b49b4-380">Nlatbroadcast</span><span class="sxs-lookup"><span data-stu-id="b49b4-380">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-381"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-381"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <span data-ttu-id="b49b4-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-383">Der Ziel-IP-Adressentyp für weitergeleitete Pakete.</span><span class="sxs-lookup"><span data-stu-id="b49b4-383">The destination IP address type for forwarded packets.</span></span> <br/> <span data-ttu-id="b49b4-384"><strong>Mögliche Werte:</strong> Eines der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-384"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="b49b4-385">Nlatunspezifiziert</span><span class="sxs-lookup"><span data-stu-id="b49b4-385">NlatUnspecified</span></span></li>
<li><span data-ttu-id="b49b4-386">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b49b4-386">NlatUnicast</span></span></li>
<li><span data-ttu-id="b49b4-387">Nlatanycast</span><span class="sxs-lookup"><span data-stu-id="b49b4-387">NlatAnycast</span></span></li>
<li><span data-ttu-id="b49b4-388">Nlatmulticast</span><span class="sxs-lookup"><span data-stu-id="b49b4-388">NlatMulticast</span></span></li>
<li><span data-ttu-id="b49b4-389">Nlatbroadcast</span><span class="sxs-lookup"><span data-stu-id="b49b4-389">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-390"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-390"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <span data-ttu-id="b49b4-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-392">Die LUID für die Netzwerkschnittstelle, die der lokalen IP-Adresse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-392">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="b49b4-393"><strong>Datentyp:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-393"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <span data-ttu-id="b49b4-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-395">Der Schnittstellentyp, wie er von der Internet Assigned Names Authority (IANA) definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b49b4-395">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="b49b4-396">Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="b49b4-396">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="b49b4-397"><strong>Mögliche Werte:</strong> Die Schnittstellentyp Werte, die in der Header Datei "ipifcons. h" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b49b4-397"><strong>Possible values:</strong> The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="b49b4-398"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-398"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <span data-ttu-id="b49b4-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-400">Die Kapselungs Methode, die von einem Tunnel verwendet wird, wenn der Typmember IF_TYPE_TUNNEL ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-400">The encapsulation method used by a tunnel if the Type member is IF_TYPE_TUNNEL.</span></span> <span data-ttu-id="b49b4-401">Der Tunneltyp wird durch die Internet Assigned Names Authority (IANA) definiert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-401">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="b49b4-402">Weitere Informationen finden Sie unter <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span><span class="sxs-lookup"><span data-stu-id="b49b4-402">For more information, see <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span></span> <br/> <span data-ttu-id="b49b4-403"><strong>Mögliche Werte:</strong> Die TUNNEL_TYPE Enumerationstyp Werte, die in der ifdef. h-Header Datei aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b49b4-403"><strong>Possible values:</strong> The TUNNEL_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="b49b4-404"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-404"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <span data-ttu-id="b49b4-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-406">Die LUID für die Netzwerkschnittstelle, auf der das weitergeleitete Paket versendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b49b4-406">The LUID for the network interface on which the packet being forwarded is to be sent out.</span></span> <br/> <span data-ttu-id="b49b4-407"><strong>Datentyp:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="b49b4-407"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <span data-ttu-id="b49b4-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-409">Die IP-Protokollnummer, wie in RFC 1700 angegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-409">The IP protocol number, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="b49b4-410"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-410"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <span data-ttu-id="b49b4-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-412">Die Portnummer des lokalen Transport Protokolls.</span><span class="sxs-lookup"><span data-stu-id="b49b4-412">The local transport protocol port number.</span></span><br/> <span data-ttu-id="b49b4-413"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-413"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <span data-ttu-id="b49b4-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-415">Das Feld "ICMP Type", wie in RFC 792 angegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-415">The ICMP type field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="b49b4-416"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-416"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <span data-ttu-id="b49b4-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-418">Die Portnummer des Remote Transport Protokolls.</span><span class="sxs-lookup"><span data-stu-id="b49b4-418">The remote transport protocol port number.</span></span> <br/> <span data-ttu-id="b49b4-419"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-419"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <span data-ttu-id="b49b4-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-421">Das Feld "ICMP-Code", wie in RFC 792 angegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-421">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="b49b4-422"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-422"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <span data-ttu-id="b49b4-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-424">Der Typ der lokalen IP-Adresse, der in das ICMP-Paket eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-424">The local IP address type that is embedded in the ICMP packet.</span></span><br/> <span data-ttu-id="b49b4-425"><strong>Mögliche Werte:</strong> Eines der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.</span><span class="sxs-lookup"><span data-stu-id="b49b4-425"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="b49b4-426">Nlatunspezifiziert</span><span class="sxs-lookup"><span data-stu-id="b49b4-426">NlatUnspecified</span></span></li>
<li><span data-ttu-id="b49b4-427">Nlatunicast</span><span class="sxs-lookup"><span data-stu-id="b49b4-427">NlatUnicast</span></span></li>
<li><span data-ttu-id="b49b4-428">Nlatanycast</span><span class="sxs-lookup"><span data-stu-id="b49b4-428">NlatAnycast</span></span></li>
<li><span data-ttu-id="b49b4-429">Nlatmulticast</span><span class="sxs-lookup"><span data-stu-id="b49b4-429">NlatMulticast</span></span></li>
<li><span data-ttu-id="b49b4-430">Nlatbroadcast</span><span class="sxs-lookup"><span data-stu-id="b49b4-430">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-431"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-431"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <span data-ttu-id="b49b4-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-433">Die Remote-IP-Adresse, die in das ICMP-Paket eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-433">The remote IP address that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="b49b4-434"><strong>Datentyp:</strong> Für eine IPv4-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-434"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-435">FWP_V4_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-435">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-436">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-436">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-437"><strong>Datentyp:</strong> Für eine IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="b49b4-437"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="b49b4-438">FWP_V6_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-438">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-439">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-439">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <span data-ttu-id="b49b4-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-441">Die IP-Protokollnummer, die in das ICMP-Paket eingebettet ist, wie in RFC 1700 angegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-441">The IP protocol number that is embedded in the ICMP packet, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="b49b4-442"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-442"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <span data-ttu-id="b49b4-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-444">Die Portnummer des lokalen Transport Protokolls, die in das ICMP-Paket eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-444">The local transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="b49b4-445"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-445"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <span data-ttu-id="b49b4-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-447">Die Portnummer des Remote Transport Protokolls, die in das ICMP-Paket eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="b49b4-447">The remote transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="b49b4-448"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-448"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <span data-ttu-id="b49b4-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-450">Eine bitweise OR-Kombination von filterbedingungs-Flags.</span><span class="sxs-lookup"><span data-stu-id="b49b4-450">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="b49b4-451"><strong>Mögliche Werte:</strong> Siehe <a href="filtering-condition-flags-.md"> <strong>Filtern</strong> von Bedingungs Flags</a></span><span class="sxs-lookup"><span data-stu-id="b49b4-451"><strong>Possible values:</strong> See <a href="filtering-condition-flags-.md"><strong>Filtering Condition Flags</strong></a></span></span><br/> <span data-ttu-id="b49b4-452"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-452"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <span data-ttu-id="b49b4-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-454">Die Richtung des Datenverkehrs oder Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="b49b4-454">The direction of the traffic or data flow.</span></span> <br/> <span data-ttu-id="b49b4-455"><strong>Mögliche Werte:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-455"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-456">FWP_DIRECTION_INBOUND</span><span class="sxs-lookup"><span data-stu-id="b49b4-456">FWP_DIRECTION_INBOUND</span></span></li>
<li><span data-ttu-id="b49b4-457">FWP_DIRECTION_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="b49b4-457">FWP_DIRECTION_OUTBOUND</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-458">Für Datagramm-Schichten (FWPM_LAYER_DATAGRAM_DATA_ *) und streampaketschichten (FWPM_LAYER_STREAM_PACKET_*) ist der Wert mit der Richtung des Pakets identisch.</span><span class="sxs-lookup"><span data-stu-id="b49b4-458">For datagram layers (FWPM_LAYER_DATAGRAM_DATA_ *) and stream packet layers (FWPM_LAYER_STREAM_PACKET_*), the value will be the same as the direction of the packet.</span></span> <br/> <span data-ttu-id="b49b4-459">Bei streamschichten (FWPM_LAYER_STREAM_ *) und Datenfluss Ebenen (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*) ist der Wert mit der Verbindungs Richtung identisch.</span><span class="sxs-lookup"><span data-stu-id="b49b4-459">For stream layers (FWPM_LAYER_STREAM_ *) and flow established layers (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), the value will be the same as direction of the connection.</span></span> <span data-ttu-id="b49b4-460">(Wenn z. b. eine lokale Anwendung die Verbindung initiiert, wird für ein <strong></strong> eingehender Paket FWPM_CONDITION_DIRECTION <strong>FWP_DIRECTION_OUTBOUND</strong>festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="b49b4-460">(For example, when a local application initiates the connection, an inbound packet has <strong>FWPM_CONDITION_DIRECTION</strong> set to <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span></span> <br/> <span data-ttu-id="b49b4-461"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-461"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <span data-ttu-id="b49b4-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-463">Der Index der Netzwerkschnittstelle, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-463">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="b49b4-464"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-464"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <span data-ttu-id="b49b4-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-466">Der Index der logischen Netzwerkschnittstelle, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-466">The index of the logical network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="b49b4-467"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-467"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <span data-ttu-id="b49b4-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-469">Der Index der Quell Netzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-469">The index of the source network interface for forwarded packets, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="b49b4-470"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-470"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <span data-ttu-id="b49b4-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-472">Der Index der logischen Quell Netzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-472">The index of the source logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="b49b4-473"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-473"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <span data-ttu-id="b49b4-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-475">Der Index der Zielnetzwerk Schnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-475">The index of the destination network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="b49b4-476"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-476"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <span data-ttu-id="b49b4-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-478">Der Index der logischen Zielnetzwerk Schnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b49b4-478">The index of the destination logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="b49b4-479"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-479"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <span data-ttu-id="b49b4-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-481">Der voll qualifizierte Gerätepfad der Anwendung, wie von der <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b49b4-481">The fully qualified device path of the application, as returned by the <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> function.</span></span> <br/> <span data-ttu-id="b49b4-482">(Z. b &quot; . \device0\hardiskvolume1\program Files\Application.exe&quot; .)</span><span class="sxs-lookup"><span data-stu-id="b49b4-482">(For example, &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.)</span></span><br/> <span data-ttu-id="b49b4-483"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-483"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <span data-ttu-id="b49b4-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-485">Die Identifizierung des lokalen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-485">The identification of the local user.</span></span> <br/> <span data-ttu-id="b49b4-486"><strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-486"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <span data-ttu-id="b49b4-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-488">Die Identifizierung des Remote Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-488">The identification of the remote user.</span></span> <br/> <span data-ttu-id="b49b4-489"><strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-489"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <span data-ttu-id="b49b4-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-491">Die Identifizierung des Remote Computers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-491">The identification of the remote machine.</span></span> <br/> <span data-ttu-id="b49b4-492"><strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-492"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <span data-ttu-id="b49b4-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-494">Der unzulässige oder verweigerte unformatierte Socket-Modus.</span><span class="sxs-lookup"><span data-stu-id="b49b4-494">The raw socket mode that is allowed or denied.</span></span><br/> <span data-ttu-id="b49b4-495"><strong>Mögliche Werte:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-495"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-496">SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="b49b4-496">SIO_RCVALL</span></span></li>
<li><span data-ttu-id="b49b4-497">SIO_RCVALL_IGMPMCAST</span><span class="sxs-lookup"><span data-stu-id="b49b4-497">SIO_RCVALL_IGMPMCAST</span></span></li>
<li><span data-ttu-id="b49b4-498">SIO_RCVALL_MCAST</span><span class="sxs-lookup"><span data-stu-id="b49b4-498">SIO_RCVALL_MCAST</span></span></li>
</ul>
<span data-ttu-id="b49b4-499">Eine Beschreibung dieser RAW-Socketmodi finden Sie unter der <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b49b4-499">For a description of these raw socket modes, see the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> function.</span></span><br/> <span data-ttu-id="b49b4-500"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-500"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <span data-ttu-id="b49b4-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-502">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-502">Reserved for internal use.</span></span> <br/> <span data-ttu-id="b49b4-503"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-503"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <span data-ttu-id="b49b4-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-505">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-505">Reserved for internal use.</span></span> <br/> <span data-ttu-id="b49b4-506"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-506"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b49b4-507">Die folgenden Konstanten sind nur für den Benutzermodus verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b49b4-507">The following constants are available for user mode only.</span></span>



| <span data-ttu-id="b49b4-508">Für Windows 8 und Windows Server 2012 verfügbare benutzermodusbedingungen</span><span class="sxs-lookup"><span data-stu-id="b49b4-508">User-mode conditions available for Windows 8 and Windows Server 2012</span></span>                                                                                                                       | <span data-ttu-id="b49b4-509">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49b4-509">Description</span></span>                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <span data-ttu-id="b49b4-510"><dt>**Modus "swpm- \_ Bedingung" \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-510"><dt>**FWPM\_CONDITION\_QM\_MODE**</dt></span></span> </dl> | <span data-ttu-id="b49b4-511">Der Modus des Schnellmodus-Filters (qm).</span><span class="sxs-lookup"><span data-stu-id="b49b4-511">The mode of the quick mode (QM) filter.</span></span> <span data-ttu-id="b49b4-512">Mögliche Werte finden Sie unter [**IPSec- \_ Datenverkehrs \_ Typen**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) .</span><span class="sxs-lookup"><span data-stu-id="b49b4-512">See [**IPSEC\_TRAFFIC\_TYPE**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) for possible values.</span></span><br/> <span data-ttu-id="b49b4-513">**Datentyp:** F \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="b49b4-513">**Data type:** FWP\_UINT32</span></span><br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b49b4-514">Für Windows 7, Windows Server 2008 R2 und höher verfügbare benutzermodusbedingungen</span><span class="sxs-lookup"><span data-stu-id="b49b4-514">User-mode conditions available for Windows 7, Windows Server 2008 R2, and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b49b4-515">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49b4-515">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <span data-ttu-id="b49b4-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-517">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-517">Reserved for internal use.</span></span><br/> <span data-ttu-id="b49b4-518"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-518"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <span data-ttu-id="b49b4-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-520">Der Name des Peers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-520">The name of the peer.</span></span> <span data-ttu-id="b49b4-521">Beispiel: der DNS-Name des Peers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-521">For example, the peer's DNS name.</span></span><br/> <span data-ttu-id="b49b4-522"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-522"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <span data-ttu-id="b49b4-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-524">Die Identität des Remote Authentifizierungs Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="b49b4-524">The identity of the remote authentication principal.</span></span> <br/> <span data-ttu-id="b49b4-525"><strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-525"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="b49b4-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-527">Der Typ der IKE-, IKEv2-oder AuthIP-Authentifizierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="b49b4-527">The type of IKE, IKEv2, or AuthIP authentication method.</span></span> <br/> <span data-ttu-id="b49b4-528"><strong>Datentyp:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-528"><strong>Data type:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <span data-ttu-id="b49b4-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-530">Der Typ des Schlüssel gebundenen Moduls.</span><span class="sxs-lookup"><span data-stu-id="b49b4-530">The type of keying module.</span></span><br/> <span data-ttu-id="b49b4-531"><strong>Datentyp:</strong> IKEEXT_KEY_MODULE_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-531"><strong>Data type:</strong> IKEEXT_KEY_MODULE_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <span data-ttu-id="b49b4-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-533">Der IPSec-Modus, in dem ein Token abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b49b4-533">The IPsec mode in which a token can be obtained.</span></span><br/> <span data-ttu-id="b49b4-534"><strong>Datentyp:</strong> IPSEC_TOKEN_MODE</span><span class="sxs-lookup"><span data-stu-id="b49b4-534"><strong>Data type:</strong> IPSEC_TOKEN_MODE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <span data-ttu-id="b49b4-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-536">Der Hauptmodus (mm) oder der Schnellmodus-Richtlinien Anbieter-Kontext Schlüssel der autorisierten Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="b49b4-536">The main mode (MM) or quick mode (QM) policy provider context key of the SA being authorized.</span></span> <span data-ttu-id="b49b4-537">Dies ist hilfreich, um den Umfang der Autorisierungs Regel auf SAS zu beschränken, die mit einem angegebenen IPSec-mm-oder-CAS-Richtlinien Schlüssel gebildet</span><span class="sxs-lookup"><span data-stu-id="b49b4-537">Useful for restricting the scope of the authorization rule to SAs formed using a specified IPsec MM or QM policy key.</span></span><br/> <span data-ttu-id="b49b4-538"><strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-538"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="b49b4-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-540">Die Methode, die verwendet wird, um die Sicherheits Zuordnung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="b49b4-540">The method used to authenticate the security association.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b49b4-541">Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b49b4-541">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="b49b4-542"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-542"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
</tbody>
</table>





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b49b4-543">Für Windows Vista und höher verfügbare Konstanten</span><span class="sxs-lookup"><span data-stu-id="b49b4-543">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b49b4-544">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49b4-544">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <span data-ttu-id="b49b4-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-546">Die Identifizierung des Remote Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b49b4-546">The identification of the remote user.</span></span><br/> <span data-ttu-id="b49b4-547"><strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-547"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <span data-ttu-id="b49b4-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-549">Die UUID der RPC-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b49b4-549">The UUID of the RPC interface.</span></span> <br/> <span data-ttu-id="b49b4-550"><strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-550"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <span data-ttu-id="b49b4-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-552">Die Version der RPC-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b49b4-552">The version of the RPC interface.</span></span> <br/> <span data-ttu-id="b49b4-553"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-553"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <span data-ttu-id="b49b4-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-555">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-555">Reserved for internal use.</span></span> <br/> <span data-ttu-id="b49b4-556"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-556"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <span data-ttu-id="b49b4-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-558">Die Identifizierung der com-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b49b4-558">The identification of the COM application.</span></span><br/> <span data-ttu-id="b49b4-559"><strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-559"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <span data-ttu-id="b49b4-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-561">Der Namen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b49b4-561">The name of the application.</span></span><br/> <span data-ttu-id="b49b4-562"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-562"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <span data-ttu-id="b49b4-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-564">Das RPC-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="b49b4-564">The RPC protocol.</span></span> <br/> <span data-ttu-id="b49b4-565"><strong>Mögliche Werte:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-565"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-566">RPC_PROTSEQ_TCP</span><span class="sxs-lookup"><span data-stu-id="b49b4-566">RPC_PROTSEQ_TCP</span></span></li>
<li><span data-ttu-id="b49b4-567">RPC_PROTSEQ_NMP</span><span class="sxs-lookup"><span data-stu-id="b49b4-567">RPC_PROTSEQ_NMP</span></span></li>
<li><span data-ttu-id="b49b4-568">RPC_PROTSEQ_LRPC</span><span class="sxs-lookup"><span data-stu-id="b49b4-568">RPC_PROTSEQ_LRPC</span></span></li>
<li><span data-ttu-id="b49b4-569">RPC_PROTSEQ_HTTP</span><span class="sxs-lookup"><span data-stu-id="b49b4-569">RPC_PROTSEQ_HTTP</span></span></li>
</ul>
<br/> <span data-ttu-id="b49b4-570"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-570"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <span data-ttu-id="b49b4-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-572">Der Authentifizierungstyp.</span><span class="sxs-lookup"><span data-stu-id="b49b4-572">The authentication service type.</span></span> <span data-ttu-id="b49b4-573">Weitere Informationen zu Authentifizierungsdienst Typen finden Sie unter <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service-Konstanten</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b49b4-573">For more information about authentication service types, see <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service Constants</strong></a>.</span></span> <br/> <span data-ttu-id="b49b4-574"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-574"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <span data-ttu-id="b49b4-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-576">Die Authentifizierungsdienst Ebene.</span><span class="sxs-lookup"><span data-stu-id="b49b4-576">The authentication service level.</span></span> <span data-ttu-id="b49b4-577">Weitere Informationen zu Authentifizierungsdienst Ebenen finden Sie unter <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Konstanten auf Authentifizierungs Ebene</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b49b4-577">For more information about authentication service levels, see <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Authentication-Level Constants</strong></a>.</span></span> <br/> <span data-ttu-id="b49b4-578"><strong>Datentyp:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="b49b4-578"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <span data-ttu-id="b49b4-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-580">Der Zertifikat basierte SSPI-Verschlüsselungsalgorithmus (Security Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="b49b4-580">The certificate based Security Service Provider Interface (SSPI) encryption algorithm.</span></span><br/> <span data-ttu-id="b49b4-581"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-581"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <span data-ttu-id="b49b4-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-583">Die Zertifikat basierte SSPI-Verschlüsselungsschlüssel Größe.</span><span class="sxs-lookup"><span data-stu-id="b49b4-583">The certificate based SSPI encryption key size.</span></span><br/> <span data-ttu-id="b49b4-584"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-584"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <span data-ttu-id="b49b4-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-586">Die lokale IPv4-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-586">The local IPv4 address.</span></span> <br/> <span data-ttu-id="b49b4-587"><strong>Datentyp:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-587"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-588">FWP_V4_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-588">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-589">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-589">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <span data-ttu-id="b49b4-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-591">Die lokale IPv6-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-591">The local IPv6 address.</span></span> <br/> <span data-ttu-id="b49b4-592"><strong>Datentyp:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-592"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-593">FWP_V6_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-593">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-594">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-594">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <span data-ttu-id="b49b4-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-596">Die Remote-IPv4-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-596">The remote IPv4 address.</span></span> <br/> <span data-ttu-id="b49b4-597"><strong>Datentyp:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-597"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-598">FWP_V4_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-598">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-599">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-599">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <span data-ttu-id="b49b4-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-601">Die IPv6-Remote Adresse.</span><span class="sxs-lookup"><span data-stu-id="b49b4-601">The remote IPv6 address.</span></span> <br/> <span data-ttu-id="b49b4-602"><strong>Datentyp:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="b49b4-602"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="b49b4-603">FWP_V6_ADDR_MASK, oder</span><span class="sxs-lookup"><span data-stu-id="b49b4-603">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="b49b4-604">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-604">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <span data-ttu-id="b49b4-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-606">Der Name des Remote Named Pipe.</span><span class="sxs-lookup"><span data-stu-id="b49b4-606">The name of the remote named pipe.</span></span><br/> <span data-ttu-id="b49b4-607"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-607"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <span data-ttu-id="b49b4-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-609">Die UUID des Prozesses mit der RPC-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b49b4-609">The UUID of the process with the RPC interface.</span></span><br/> <span data-ttu-id="b49b4-610"><strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-610"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <span data-ttu-id="b49b4-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-612">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-612">Reserved for internal use.</span></span><br/> <span data-ttu-id="b49b4-613"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-613"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <span data-ttu-id="b49b4-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-615">Für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b49b4-615">Reserved for internal use.</span></span><br/> <span data-ttu-id="b49b4-616"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-616"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <span data-ttu-id="b49b4-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-618">Die Identifizierung des Clients bei Verwendung von RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="b49b4-618">The identification of the client when using RpcProxy.</span></span><br/> <span data-ttu-id="b49b4-619"><strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-619"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <span data-ttu-id="b49b4-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-621">Der Name des RPC-Servers bei Verwendung von RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="b49b4-621">The name of the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="b49b4-622"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-622"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <span data-ttu-id="b49b4-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-624">Der Port auf dem RPC-Server, wenn RpcProxy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b49b4-624">The port on the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="b49b4-625"><strong>Datentyp:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="b49b4-625"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <span data-ttu-id="b49b4-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-627">Der Authentifizierungstyp des RPC-Proxys.</span><span class="sxs-lookup"><span data-stu-id="b49b4-627">The RPC proxy authentication service type.</span></span><br/> <span data-ttu-id="b49b4-628"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-628"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <span data-ttu-id="b49b4-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-630">Die SSL-Schlüssellänge (Secure Socket Layer) im Client Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="b49b4-630">The Secure Socket Layer (SSL) key length in the client certificate.</span></span><br/> <span data-ttu-id="b49b4-631"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-631"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <span data-ttu-id="b49b4-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-633">Der Objekt Bezeichner im Client Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="b49b4-633">The object identifier in the client certificate.</span></span><br/> <span data-ttu-id="b49b4-634"><strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="b49b4-634"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <span data-ttu-id="b49b4-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b49b4-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b49b4-636">Der Typ des NET-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="b49b4-636">The type of net event.</span></span><br/> <span data-ttu-id="b49b4-637"><strong>Datentyp:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="b49b4-637"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="b49b4-638">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b49b4-638">Remarks</span></span>

<span data-ttu-id="b49b4-639">Wenn IP-Adressen im Format "UInt32" im Format "" gespeichert werden \_ oder wenn ein IP-Port im Format "SWP UInt16" gespeichert wird \_ , werden Sie in der Host Reihenfolge und nicht in der Netzwerk Bestellung gespeichert</span><span class="sxs-lookup"><span data-stu-id="b49b4-639">When IP addresses are stored in FWP\_UINT32 format or when an IP port is stored in FWP\_UINT16 format, they are stored in host-order, not network-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49b4-640">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b49b4-640">Requirements</span></span>



| <span data-ttu-id="b49b4-641">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b49b4-641">Requirement</span></span> | <span data-ttu-id="b49b4-642">Wert</span><span class="sxs-lookup"><span data-stu-id="b49b4-642">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b49b4-643">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b49b4-643">Minimum supported client</span></span><br/> | <span data-ttu-id="b49b4-644">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b49b4-644">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b49b4-645">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b49b4-645">Minimum supported server</span></span><br/> | <span data-ttu-id="b49b4-646">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b49b4-646">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b49b4-647">Header</span><span class="sxs-lookup"><span data-stu-id="b49b4-647">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49b4-648"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="b49b4-648"><dt>Fwpmu.h</dt></span></span> </dl> |
