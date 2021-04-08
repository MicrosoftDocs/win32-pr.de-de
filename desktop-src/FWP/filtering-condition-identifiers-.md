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
# <a name="filtering-condition-identifiers"></a>Filtern von Bedingungs bezeichlern

Die Filter Bedingungs Bezeichner der Windows-Filter Plattform (WFP) werden jeweils durch eine **GUID** dargestellt. Der Datentyp für den Bedingungs Wert für jede Filterbedingung wird als ein [**\_ \_ Datentyp vom Typ "f**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)" angegeben. Diese Bezeichner und deren Datentypen werden hier definiert.

Die Standardbedingungen werden zuerst aufgeführt, gefolgt von den Bedingungen für den Benutzermodus. Bedingungen werden nach dem unterstützten Betriebssystem gruppiert, sodass Sie leicht erkennen können, welche Bedingungen für ein bestimmtes Betriebssystem unterstützt werden.

> [!Note]  
> Jede der folgenden Filterbedingungen ist nur in einer Teilmenge der WFP-Filter Ebenen verfügbar. Weitere Informationen zur Verfügbarkeit der einzelnen Bedingungen auf einer beliebigen Ebene finden Sie unter [**Filterbedingungen, die auf jeder Filter Ebene verfügbar**](filtering-conditions-available-at-each-filtering-layer.md)sind.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Für Windows 8 und Windows Server 2012 verfügbare Bedingungen</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Mac-Adresse einer bestimmten lokalen Schnittstelle.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Zieladresse eines eingehenden Frames oder die Quelladresse eines ausgehenden Frames.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Quelladresse eines eingehenden Frames oder die Zieladresse eines ausgehenden Frames.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Netzwerk Nutz Last Datentyp von Ethernet v2. (Weitere Informationen finden Sie unter ETHERNET_TYPE_IPV4 usw. in "nettiodef. h".)<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </dl></td>
<td style="text-align: left;">Der 16-Bit-VLAN-Header einschließlich der Felder "vid", "CFI" und "Priority" gemäß 802.1 q-Standard (Weitere Informationen finden Sie unter VLAN_TAG in "netiodef. h" für die Positionen der Bitfields).<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner für das Vswitch-Netzwerk. Kann nicht zusammen mit VLAN_IDs verwendet werden.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des NDIS-Ports.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Medientyp des NDIS-Ports.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/> <strong>Mögliche Werte:</strong> Einer der <strong>NDIS_MEDIUM</strong> Enumerationswerte. (Siehe ntddndis. h.) <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der physische Medientyp des NDIS-Ports.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/> <strong>Mögliche Werte:</strong> Einer der <strong>NDIS_PHYSICAL_MEDIUM</strong> Enumerationswerte. (Siehe ntddndis. h.) <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Eine bitweise OR-Kombination von filterbedingungs-Flags. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>FWP_CONDITION_L2_IS_MOBILE_BROADBAND</li>
<li>FWP_CONDITION_L2_IS_NATIVE_ETHERNET</li>
<li>FWP_CONDITION_L2_IS_WIFI</li>
<li>FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der adrestyp der physischen lokalen Adresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>Dlunicast</li>
<li>Dlmulticast</li>
<li>Dlbroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Adresstyp der physischen Remote Adresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>Dlunicast</li>
<li>Dlmulticast</li>
<li>Dlbroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die physische Quelladresse eines Frames.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die physische Zieladresse eines Frames.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der adreetstyp der physischen Zieladresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>Dlunicast</li>
<li>Dlmulticast</li>
<li>Dlbroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der adreetstyp der physischen Zieladresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Eines der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>Dlunicast</li>
<li>Dlmulticast</li>
<li>Dlbroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Der Quellport des Paket Transports.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Das Feld "ICMP Type", wie in RFC 792 angegeben.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Der Zielport für den Transport des Pakets.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">Das Feld "ICMP-Code", wie in RFC 792 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner einer Vswitch-Instanz.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, ob die Vswitch-Instanz Teil eines externen, internen oder privaten virtuellen Netzwerks ist.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner der Quelle des aktuellen Pakets. (Der Name einer VM-NIC, P-NIC oder V-NIC.)<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner des Ziels des aktuellen Pakets. (Der Name einer VM-NIC, P-NIC oder V-NIC.)<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner der virtuellen Vswitch-Quell Maschine.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner des virtuellen Vswitch-Ziel Computers.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Schnittstellentyp der Quelle des aktuellen Pakets.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>Switchnicsyntheticnic (bei Schnittstellentyp VM-NIC)</li>
<li>Switchnicemulatednic (bei Schnittstellentyp VM-NIC)</li>
<li>Switchnicphysicalnic (bei einem Schnittstellentyp P-NIC)</li>
<li>Switchnicvnic (bei Schnittstellen Typ V-NIC, verbunden mit der Host Partition)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Schnittstellentyp des Ziels des aktuellen Pakets.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>Switchnicsyntheticnic (bei Schnittstellentyp VM-NIC)</li>
<li>Switchnicemulatednic (bei Schnittstellentyp VM-NIC)</li>
<li>Switchnicphysicalnic (bei einem Schnittstellentyp P-NIC)</li>
<li>Switchnicvnic (bei Schnittstellen Typ V-NIC, verbunden mit der Host Partition)</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">Die LUID für die Netzwerkschnittstelle, die der lokalen IP-Adresse zugeordnet ist. <br/> <strong>Datentyp:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Sicherheits-ID (SID) eines App-Containers.<br/> <strong>Datentyp:</strong> FWP_SID<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">Der voll qualifizierte Gerätepfad der Anwendung, z. b &quot; . \device0\hardiskvolume1\program Files\Application.exe&quot; . Wenn eine Verbindung umgeleitet wurde, ist dies der Bezeichner der ursprünglichen app. Andernfalls ist dies identisch mit <strong>FWPM_CONDITION_ALE_APP_ID</strong>.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
</tbody>
</table>





| Für Windows 7, Windows Server 2008 R2 und höher verfügbare Bedingungen                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <dt>**\_ \_ IP- \_ nexthop-Adresse der Bedingung für die IP- \_ Adresse**</dt> </dl>                                             | Die IP-Adresse der Schnittstelle für den nächsten Hop.<br/> **Datentyp:** F/WP- \_ \_ addr- \_ Maske<br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <dt>**\_ \_ IP- \_ \_ Schnittstellen Schnittstellen-Schnittstelle**</dt> </dl>                                       | Die Schnittstelle für den nächsten Hop, von der das Paket abweicht. <br/> **Datentyp:** F \_ UINT64<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <dt>**\_ \_ Dateityp "nexthop \_ - \_ Schnittstellentyp"**</dt> </dl>                                 | Der Schnittstellentyp der Schnittstelle für den nächsten Hop.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <dt>**\_ \_ Dateityp "nexthop \_ - \_ Tunneltyp"**</dt> </dl>                                          | Der Tunneltyp der Schnittstelle für den nächsten Hop.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <dt>**Index für die twpm- \_ Bedingung \_ nexthop- \_ Schnittstelle \_**</dt> </dl>                              | Der Schnittstellen Index der Schnittstelle für den nächsten Hop.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <dt>**Index für die Unterschnittstelle der twpm- \_ Bedingung \_ nexthop \_ \_ \_**</dt> </dl>                 | Der unter Schnittstellen Index der Schnittstelle für den nächsten Hop.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <dt>**\_ursprüngliche Profil-ID der Bedingung für die \_ \_ Profilerstellung \_**</dt> </dl>                                          | Die Netzwerk Kategorie der Ankunfts-oder der nächsten Hop-Schnittstelle, über die der ALE Datenfluss (eingehend oder ausgehend) erstellt wird. <br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <dt>**\_ \_ ID der aktuellen Profil- \_ \_ ID der Bedingung**</dt> </dl>                                             | Die Netzwerk Kategorie der Ankunfts-oder der nächsten Hop-Schnittstelle, über die das aktuelle Paket (eingehend oder ausgehend) erstellt wird. <br/> **Datentyp:** F \_ UInt32<br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <dt>**\_Profil-ID der \_ lokalen \_ Profil erstellungsschnittstelle \_ \_**</dt> </dl>                    | Die Netzwerk Kategorie der Übermittlungs Schnittstelle.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <dt>**Profil-ID für die Profilerstellung für die \_ \_ \_ Benutzeroberfläche \_ \_**</dt> </dl>              | Die Netzwerk Kategorie der Ankunfts Schnittstelle.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <dt>**ID der TPM-Bedingungs \_ \_ \_ Schnittstellen \_ Profil- \_ ID**</dt> </dl>              | Die Netzwerk Kategorie der Schnittstelle für den nächsten Hop.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <dt>**\_ \_ Grund für Neuautorisierung der \_ Grundbedingungen**</dt> </dl>                                              | Der Grund für die Neuautorisierung einer zuvor autorisierten Verbindung.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <dt>**Grund für den \_ Grund für die \_ \_ \_ Grundursache der Grundbedingungen**</dt> </dl>                                                | Der Grund für die Neuautorisierung einer zuvor autorisierten Verbindung, wie z. b. eine erneute Autorisierung der **\_ Grundrichtlinie für die \_ \_ Grund \_ Richtlinie \_** (oder einer der anderen Werte, die unter Filtern von Bedingungs [**Flags**](filtering-condition-flags-.md)aufgeführt sind).<br/> **Datentyp:** F \_ UInt32<br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <dt>**\_ \_ ursprünglicher \_ ICMP- \_ Typ der Datei Bedingung**</dt> </dl>                                             | Der ICMP-Typ, mit dem der Flow erstellt wurde.<br/> **Datentyp:** F \_ UInt16<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <dt>**\_ \_ IP-Adresse der \_ physischen Eingangs \_ \_ Schnittstelle der Bedingung**</dt> </dl>           | Die LUID der physischen Schnittstelle, die der Ankunfts-IP-Adresse zugeordnet ist.<br/> **Datentyp:** F \_ UINT64<br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <dt>**WPM \_ -Bedingung \_ IP \_ Physical \_ nexthop \_ Interface**</dt> </dl>           | Die LUID der physischen Schnittstelle des nächsten Hops.<br/> **Datentyp:** F \_ UINT64<br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <dt>**Quarantäne-Epoche der Bedingung für die Bedingungs \_ \_ Schnittstelle \_ \_**</dt> </dl>                     | Die einer Schnittstelle zugeordnete Epochen Anzahl. Reserviert.<br/> **Datentyp:** F \_ UINT64<br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <dt>**swpm \_ Condition \_ ALE \_ die \_ Firewall \_ - \_ socketeigenschaft**</dt> </dl> | Für die interne Verwendung reserviert. <br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                                              |





| Verfügbare Konstanten für Windows Vista mit SP1, Windows Server 2008 und höher                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <dt>**\_ \_ IP-Ankunfts Schnittstelle der Bedingung für die \_ \_ Benutzeroberfläche**</dt> </dl>                       | Die LUID für die Netzwerkschnittstelle, die der Ankunfts-IP-Adresse zugeordnet ist. <br/> **Datentyp:** F \_ UINT64<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <dt>**Typ der Eingangs \_ Schnittstelle für die \_ \_ Benutzeroberfläche \_**</dt> </dl>                 | Der Typ der Netzwerkschnittstelle für die Ankunft, wie von der Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Die Schnittstellentyp Werte, die in der Header Datei "ipifcons. h" aufgeführt sind.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <dt>"F" **\_ \_ \_ \_ Typ** des Bedingungs Eingangs Tunnels</dt> </dl>                       | Die Kapselungs Methode, die von einem Tunnel verwendet wird, der der Ankunfts Netzwerkschnittstelle zugeordnet ist, wenn der Typmember bei einem \_ \_ typtunnel ist. Der Tunneltyp wird durch die Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Der \_ Typ der Tunneltyp-Enumeration, die in der ifdef. h-Header Datei aufgeführt sind.<br/> **Datentyp:** F \_ UInt32<br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <dt>**Index für die \_ Eingangs \_ Schnittstelle der einstellungsschnittstelle \_ \_**</dt> </dl>              | Der Index der Netzwerkschnittstelle für die Ankunft, wie vom Netzwerk Stapel aufgelistet.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <dt>**Index für die Eingangs \_ subschnittstelle der Bedingung für die \_ \_ unter \_ Schnittstelle \_**</dt> </dl> | Der Index der Netzwerkschnittstelle für die Ankunft, wie vom Netzwerk Stapel aufgelistet. <br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <dt>**\_ \_ Index der lokalen Index- \_ Schnittstelle \_**</dt> </dl>                    | Der Index der Netzwerkschnittstelle, wie vom Netzwerk Stapel aufgelistet. <br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <dt>**\_ \_ lokaler \_ \_ Schnittstellentyp für die Bedingung**</dt> </dl>                       | Der Schnittstellentyp, wie er von der Internet Assigned Names Authority (IANA) definiert wird. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Die Schnittstellentyp Werte, die in der Header Datei "ipifcons. h" aufgeführt sind.<br/> **Datentyp:** F \_ UInt32<br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <dt>**\_ \_ lokaler \_ \_ Tunneltyp der WPM-Bedingung**</dt> </dl>                                | Die Kapselungs Methode, die von einem Tunnel verwendet wird, wenn der Typmember bei einem \_ \_ typtunnel ist. Der Tunneltyp wird durch die Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Der \_ Typ der Tunneltyp-Enumeration, die in der ifdef. h-Header Datei aufgeführt sind.<br/> **Datentyp:** F \_ UInt32 <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Für Windows Vista und höher verfügbare Konstanten</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die lokale IP-Adresse. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK, oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK, oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Remote-IP-Adresse. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK, oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK, oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Quell-IP-Adresse für weitergeleitete Pakete. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK, oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK, oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Ziel-IP-Adresse für weitergeleitete Pakete. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK, oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK, oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ der lokalen IP-Adresse. <br/> <strong>Mögliche Werte:</strong> Eines der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.
<ul>
<li>Nlatunspezifiziert</li>
<li>Nlatunicast</li>
<li>Nlatanycast</li>
<li>Nlatmulticast</li>
<li>Nlatbroadcast</li>
</ul>
<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Ziel-IP-Adressentyp für weitergeleitete Pakete. <br/> <strong>Mögliche Werte:</strong> Eines der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.
<ul>
<li>Nlatunspezifiziert</li>
<li>Nlatunicast</li>
<li>Nlatanycast</li>
<li>Nlatmulticast</li>
<li>Nlatbroadcast</li>
</ul>
<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">Die LUID für die Netzwerkschnittstelle, die der lokalen IP-Adresse zugeordnet ist. <br/> <strong>Datentyp:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Schnittstellentyp, wie er von der Internet Assigned Names Authority (IANA) definiert wird. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> <strong>Mögliche Werte:</strong> Die Schnittstellentyp Werte, die in der Header Datei "ipifcons. h" aufgeführt sind.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Die Kapselungs Methode, die von einem Tunnel verwendet wird, wenn der Typmember IF_TYPE_TUNNEL ist. Der Tunneltyp wird durch die Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>. <br/> <strong>Mögliche Werte:</strong> Die TUNNEL_TYPE Enumerationstyp Werte, die in der ifdef. h-Header Datei aufgeführt sind.<br/> <strong>Datentyp:</strong> FWP_UINT32 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">Die LUID für die Netzwerkschnittstelle, auf der das weitergeleitete Paket versendet werden soll. <br/> <strong>Datentyp:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">Die IP-Protokollnummer, wie in RFC 1700 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des lokalen Transport Protokolls.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Das Feld "ICMP Type", wie in RFC 792 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des Remote Transport Protokolls. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">Das Feld "ICMP-Code", wie in RFC 792 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ der lokalen IP-Adresse, der in das ICMP-Paket eingebettet ist.<br/> <strong>Mögliche Werte:</strong> Eines der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.
<ul>
<li>Nlatunspezifiziert</li>
<li>Nlatunicast</li>
<li>Nlatanycast</li>
<li>Nlatmulticast</li>
<li>Nlatbroadcast</li>
</ul>
<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Remote-IP-Adresse, die in das ICMP-Paket eingebettet ist. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK, oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK, oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">Die IP-Protokollnummer, die in das ICMP-Paket eingebettet ist, wie in RFC 1700 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des lokalen Transport Protokolls, die in das ICMP-Paket eingebettet ist. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des Remote Transport Protokolls, die in das ICMP-Paket eingebettet ist. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Eine bitweise OR-Kombination von filterbedingungs-Flags. <br/> <strong>Mögliche Werte:</strong> Siehe <a href="filtering-condition-flags-.md"> <strong>Filtern</strong> von Bedingungs Flags</a><br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </dl></td>
<td style="text-align: left;">Die Richtung des Datenverkehrs oder Datenflusses. <br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>FWP_DIRECTION_INBOUND</li>
<li>FWP_DIRECTION_OUTBOUND</li>
</ul>
<br/> Für Datagramm-Schichten (FWPM_LAYER_DATAGRAM_DATA_ *) und streampaketschichten (FWPM_LAYER_STREAM_PACKET_*) ist der Wert mit der Richtung des Pakets identisch. <br/> Bei streamschichten (FWPM_LAYER_STREAM_ *) und Datenfluss Ebenen (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*) ist der Wert mit der Verbindungs Richtung identisch. (Wenn z. b. eine lokale Anwendung die Verbindung initiiert, wird für ein <strong></strong> eingehender Paket FWPM_CONDITION_DIRECTION <strong>FWP_DIRECTION_OUTBOUND</strong>festgelegt.) <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der Netzwerkschnittstelle, wie vom Netzwerk Stapel aufgelistet. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der logischen Netzwerkschnittstelle, wie vom Netzwerk Stapel aufgelistet. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der Quell Netzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der logischen Quell Netzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der Zielnetzwerk Schnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der logischen Zielnetzwerk Schnittstelle für weitergeleitete Pakete, wie vom Netzwerk Stapel aufgelistet. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">Der voll qualifizierte Gerätepfad der Anwendung, wie von der <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> -Funktion zurückgegeben. <br/> (Z. b &quot; . \device0\hardiskvolume1\program Files\Application.exe&quot; .)<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifizierung des lokalen Benutzers. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifizierung des Remote Benutzers. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifizierung des Remote Computers. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </dl></td>
<td style="text-align: left;">Der unzulässige oder verweigerte unformatierte Socket-Modus.<br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>SIO_RCVALL</li>
<li>SIO_RCVALL_IGMPMCAST</li>
<li>SIO_RCVALL_MCAST</li>
</ul>
Eine Beschreibung dieser RAW-Socketmodi finden Sie unter der <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> -Funktion.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Für die interne Verwendung reserviert. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;">Für die interne Verwendung reserviert. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
</tbody>
</table>



Die folgenden Konstanten sind nur für den Benutzermodus verfügbar.



| Für Windows 8 und Windows Server 2012 verfügbare benutzermodusbedingungen                                                                                                                       | BESCHREIBUNG                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <dt>**Modus "swpm- \_ Bedingung" \_ \_**</dt> </dl> | Der Modus des Schnellmodus-Filters (qm). Mögliche Werte finden Sie unter [**IPSec- \_ Datenverkehrs \_ Typen**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) .<br/> **Datentyp:** F \_ UInt32<br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Für Windows 7, Windows Server 2008 R2 und höher verfügbare benutzermodusbedingungen</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;">Für die interne Verwendung reserviert.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </dl></td>
<td style="text-align: left;">Der Name des Peers. Beispiel: der DNS-Name des Peers.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identität des Remote Authentifizierungs Prinzipals. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ der IKE-, IKEv2-oder AuthIP-Authentifizierungsmethode. <br/> <strong>Datentyp:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ des Schlüssel gebundenen Moduls.<br/> <strong>Datentyp:</strong> IKEEXT_KEY_MODULE_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </dl></td>
<td style="text-align: left;">Der IPSec-Modus, in dem ein Token abgerufen werden kann.<br/> <strong>Datentyp:</strong> IPSEC_TOKEN_MODE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </dl></td>
<td style="text-align: left;">Der Hauptmodus (mm) oder der Schnellmodus-Richtlinien Anbieter-Kontext Schlüssel der autorisierten Zertifizierungsstelle. Dies ist hilfreich, um den Umfang der Autorisierungs Regel auf SAS zu beschränken, die mit einem angegebenen IPSec-mm-oder-CAS-Richtlinien Schlüssel gebildet<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Die Methode, die verwendet wird, um die Sicherheits Zuordnung zu authentifizieren.<br/>
<blockquote>
[!Note]<br />
Nur unter Windows Server 2008 R2, Windows 7 und höher verfügbar.
</blockquote>
<br/> <strong>Datentyp:</strong> FWP_UINT32 <br/></td>
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
<th style="text-align: left;">Für Windows Vista und höher verfügbare Konstanten</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifizierung des Remote Benutzers.<br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </dl></td>
<td style="text-align: left;">Die UUID der RPC-Schnittstelle. <br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </dl></td>
<td style="text-align: left;">Die Version der RPC-Schnittstelle. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </dl></td>
<td style="text-align: left;">Für die interne Verwendung reserviert. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifizierung der com-Anwendung.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </dl></td>
<td style="text-align: left;">Der Namen der Anwendung.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">Das RPC-Protokoll. <br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>RPC_PROTSEQ_TCP</li>
<li>RPC_PROTSEQ_NMP</li>
<li>RPC_PROTSEQ_LRPC</li>
<li>RPC_PROTSEQ_HTTP</li>
</ul>
<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Authentifizierungstyp. Weitere Informationen zu Authentifizierungsdienst Typen finden Sie unter <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service-Konstanten</strong></a>. <br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </dl></td>
<td style="text-align: left;">Die Authentifizierungsdienst Ebene. Weitere Informationen zu Authentifizierungsdienst Ebenen finden Sie unter <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Konstanten auf Authentifizierungs Ebene</strong></a>. <br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </dl></td>
<td style="text-align: left;">Der Zertifikat basierte SSPI-Verschlüsselungsalgorithmus (Security Service Provider Interface).<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </dl></td>
<td style="text-align: left;">Die Zertifikat basierte SSPI-Verschlüsselungsschlüssel Größe.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">Die lokale IPv4-Adresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK, oder</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">Die lokale IPv6-Adresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK, oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">Die Remote-IPv4-Adresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK, oder</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">Die IPv6-Remote Adresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK, oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <dt><strong>FWPM_CONDITION_PIPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Name des Remote Named Pipe.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </dl></td>
<td style="text-align: left;">Die UUID des Prozesses mit der RPC-Schnittstelle.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </dl></td>
<td style="text-align: left;">Für die interne Verwendung reserviert.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Für die interne Verwendung reserviert.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifizierung des Clients bei Verwendung von RpcProxy.<br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </dl></td>
<td style="text-align: left;">Der Name des RPC-Servers bei Verwendung von RpcProxy.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Der Port auf dem RPC-Server, wenn RpcProxy verwendet wird.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Authentifizierungstyp des RPC-Proxys.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </dl></td>
<td style="text-align: left;">Die SSL-Schlüssellänge (Secure Socket Layer) im Client Zertifikat.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </dl></td>
<td style="text-align: left;">Der Objekt Bezeichner im Client Zertifikat.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ des NET-Ereignisses.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Wenn IP-Adressen im Format "UInt32" im Format "" gespeichert werden \_ oder wenn ein IP-Port im Format "SWP UInt16" gespeichert wird \_ , werden Sie in der Host Reihenfolge und nicht in der Netzwerk Bestellung gespeichert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |
