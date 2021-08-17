---
title: Filtern von Bedingungsbezeichnern (Fwpmu.h)
description: Die Filterbedingungsbezeichner für Windows Filterplattform (WFP) werden jeweils durch eine GUID dargestellt.
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
ms.openlocfilehash: 5d5d1eaf0a86cfdb2cb1051e6ae18f149bcb7934e1de5730857eead42b14917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951239"
---
# <a name="filtering-condition-identifiers"></a>Filtern von Bedingungsbezeichnern

Die Windows Filtering Platform (WFP) Filterbedingungsbezeichner werden jeweils durch eine **GUID** dargestellt. Der Datentyp für den Bedingungswert für jede Filterbedingung wird als [**\_ \_ FWP-DATENTYP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)angegeben. Diese Bezeichner und ihre Datentypen werden hier definiert.

Die Standardbedingungen werden zuerst aufgeführt, gefolgt von den spezifischen Bedingungen für den Benutzermodus. Bedingungen werden nach unterstützten Betriebssystemen gruppiert, sodass Sie leicht erkennen können, welche Bedingungen für ein bestimmtes Betriebssystem unterstützt werden.

> [!Note]  
> Jede der folgenden Filterbedingungen ist nur in einer Teilmenge der WFP-Filterebenen verfügbar. Weitere Informationen zur Verfügbarkeit der einzelnen Bedingungen auf einer beliebigen Ebene finden Sie unter [**Filterbedingungen verfügbar auf jeder Filterebene.**](filtering-conditions-available-at-each-filtering-layer.md)

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Verfügbare Bedingungen für Windows 8 und Windows Server 2012</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die MAC-Adresse einer bestimmten lokalen Schnittstelle.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Zieladresse eines eingehenden Frames oder Quelladresse eines ausgehenden Frames.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Quelladresse eines eingehenden Frames oder Zieladresse eines ausgehenden Frames.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Ethernet V2-Netzwerknutzlastdatentyp. (Siehe ETHERNET_TYPE_IPV4 usw. in netiodef.h.)<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die 16 Bits des VLAN-Headers, einschließlich der Felder VID, CFI und Priority gemäß dem 802.1q-Standard (die Positionen der Bitfelder finden Sie unter VLAN_TAG in netiodef.h).<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner für das vSwitch-Netzwerk. Kann nicht in Verbindung mit VLAN_IDs verwendet werden.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des NDIS-Ports.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Medientyp des NDIS-Ports.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/> <strong>Mögliche Werte:</strong> Jeder der <strong>NDIS_MEDIUM</strong> Enumerationswerte. (Siehe ntddndis.h.) <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der physische Medientyp des NDIS-Ports.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/> <strong>Mögliche Werte:</strong> Jeder der <strong>NDIS_PHYSICAL_MEDIUM</strong> Enumerationswerte. (Siehe ntddndis.h.) <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Ein bitweises OR einer Kombination von Filterbedingungsflags. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/> <strong>Mögliche Werte:  </strong>
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
<td style="text-align: left;">Der Adresstyp der physischen lokalen Adresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Einer der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Adresstyp der physischen Remoteadresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Einer der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
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
<td style="text-align: left;">Der Adresstyp der physischen Zieladresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Einer der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Adresstyp der physischen Zieladresse.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:</strong> Einer der folgenden <strong>DL_ADDRESS_TYPE</strong> Enumerationswerte.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Der Quellport des Pakettransports.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Das FELD ICMP-Typ, wie in RFC 792 angegeben.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Der Zielport des Pakettransports.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">Das ICMP-Codefeld, wie in RFC 792 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner einer vSwitch-Instanz.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, ob die vSwitch-Instanz Teil eines externen, internen oder privaten virtuellen Netzwerks ist.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
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
<td style="text-align: left;">Eindeutiger Bezeichner des virtuellen vSwitch-Quellcomputers.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </dl></td>
<td style="text-align: left;">Eindeutiger Bezeichner des virtuellen vSwitch-Zielcomputers.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Schnittstellentyp der Quelle des aktuellen Pakets.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>SwitchNicSyntheticNic (wenn der Schnittstellentyp VM-NIC ist)</li>
<li>SwitchNicEmulatedNic (wenn der Schnittstellentyp VM-NIC ist)</li>
<li>SwitchNicPhysicalNic (wenn der Schnittstellentyp P-NIC ist)</li>
<li>SwitchNicVNic (wenn der Schnittstellentyp V-NIC ist, mit der Hostpartition verbunden)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Schnittstellentyp des Ziels des aktuellen Pakets.<br/> <strong>Datentyp:</strong> FWP_UINT8<br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>SwitchNicSyntheticNic (wenn der Schnittstellentyp VM-NIC ist)</li>
<li>SwitchNicEmulatedNic (wenn der Schnittstellentyp VM-NIC ist)</li>
<li>SwitchNicPhysicalNic (wenn der Schnittstellentyp P-NIC ist)</li>
<li>SwitchNicVNic (wenn der Schnittstellentyp V-NIC ist, mit der Hostpartition verbunden)</li>
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
<td style="text-align: left;">Der vollqualifizierte Gerätepfad der Anwendung, z. B. &quot; \device0\hardiskvolume1\Program &quot; Files\Application.exe. Wenn eine Verbindung umgeleitet wurde, ist dies der Bezeichner der ursprünglichen App. Andernfalls ist dies identisch mit <strong>FWPM_CONDITION_ALE_APP_ID.</strong><br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
</tbody>
</table>





| Verfügbare Bedingungen für Windows 7, Windows Server 2008 R2 und höher                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <dt>**\_FWPM-BEDINGUNGS-IP \_ \_ NEXTHOP-ADRESSE \_**</dt> </dl>                                             | Die IP-Adresse der Schnittstelle des nächsten Hops.<br/> **Datentyp:** FWP \_ V4 \_ ADDR \_ MASK<br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <dt>**\_FWPM-BEDINGUNGS-IP \_ \_ NEXTHOP-SCHNITTSTELLE \_**</dt> </dl>                                       | Die Schnittstelle des nächsten Hops, über die das Paket übertragen wird. <br/> **Datentyp:** FWP \_ UINT64<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <dt>**\_FWPM-BEDINGUNG \_ NEXTHOP-SCHNITTSTELLENTYP \_ \_**</dt> </dl>                                 | Der Schnittstellentyp der Schnittstelle des nächsten Hops.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <dt>**\_FWPM-BEDINGUNG \_ NEXTHOP \_ TUNNEL \_ TYPE**</dt> </dl>                                          | Der Tunneltyp der Schnittstelle des nächsten Hops.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <dt>**\_FWPM-BEDINGUNG \_ NEXTHOP \_ INTERFACE \_ INDEX**</dt> </dl>                              | Der Schnittstellenindex der Schnittstelle des nächsten Hops.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <dt>**\_FWPM-BEDINGUNG \_ – NÄCHSTERHOP-UNTERSCHNITTSTELLENINDEX \_ \_ \_**</dt> </dl>                 | Der Unterschnittstellenindex der Schnittstelle des nächsten Hops.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <dt>**URSPRÜNGLICHE \_ PROFIL-ID DER FWPM-BEDINGUNG \_ \_ \_**</dt> </dl>                                          | Die Netzwerkkategorie der Eingangs- oder Nächsten-Hop-Schnittstelle, über die der ALE-Datenfluss (eingehend oder ausgehend) erstellt wird. <br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <dt>**AKTUELLE \_ PROFIL-ID DER FWPM-BEDINGUNG \_ \_ \_**</dt> </dl>                                             | Die Netzwerkkategorie der Eingangs- oder Nächsten-Hop-Schnittstelle, über die das aktuelle Paket (eingehend oder ausgehend) erstellt wird. <br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <dt>**PROFIL-ID DER LOKALEN SCHNITTSTELLE FÜR DIE \_ FWPM-BEDINGUNG \_ \_ \_ \_**</dt> </dl>                    | Die Netzwerkkategorie der Übermittlungsschnittstelle.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <dt>**FWPM \_ CONDITION ARRIVAL INTERFACE PROFILE ID (FWPM-BEDINGUNGS-SCHNITTSTELLENPROFIL-ID) \_ \_ \_ \_**</dt> </dl>              | Die Netzwerkkategorie der Ankunftsschnittstelle.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <dt>**\_FWPM-BEDINGUNG \_ NEXTHOP \_ INTERFACE PROFILE \_ \_ ID**</dt> </dl>              | Die Netzwerkkategorie der Schnittstelle des nächsten Hops.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <dt>**FWPM CONDITION REAUTHORIZE REASON (URSACHE FÜR DIE ERNEUTE AUTHENTIFIZIERUNG \_ DER FWPM-BEDINGUNG) \_ \_**</dt> </dl>                                              | Der Grund für die erneute Authentifizierung einer zuvor autorisierten Verbindung.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <dt>**GRUND FÜR DIE ERNEUTE \_ \_ AUTHENTIFIZIERUNG DER FWPM-BEDINGUNG \_ \_**</dt> </dl>                                                | Der Grund für die erneute Authentifizierung einer zuvor autorisierten Verbindung, z. B. **\_ FWP-BEDINGUNG \_ REAUTHORIZE \_ REASON POLICY \_ \_ CHANGE** (oder einer der anderen Unter [**Filterbedingungsflags**](filtering-condition-flags-.md)aufgeführten Werte).<br/> **Datentyp:** FWP \_ UINT32<br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <dt>**\_FWPM-BEDINGUNG \_ URSPRÜNGLICHER \_ ICMP-TYP \_**</dt> </dl>                                             | Der ICMP-Typ, mit dem der Flow erstellt wurde.<br/> **Datentyp:** FWP \_ UINT16<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <dt>**FWPM-BEDINGUNG \_ \_ \_ IP-SCHNITTSTELLE FÜR \_ PHYSISCHE \_ ANKUNFT**</dt> </dl>           | Die LUID der physischen Schnittstelle, die der IP-Adresse der Ankunft zugeordnet ist.<br/> **Datentyp:** FWP \_ UINT64<br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <dt>**FWPM-BEDINGUNG \_ \_ IP PHYSISCHE \_ \_ NEXTHOP-SCHNITTSTELLE \_**</dt> </dl>           | Die LUID der physischen Schnittstelle des nächsten Hops.<br/> **Datentyp:** FWP \_ UINT64<br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <dt>**FWPM \_ CONDITION \_ INTERFACE \_ QUARANTINE \_ EPOCH**</dt> </dl>                     | Die Epochenanzahl, die einer Schnittstelle zugeordnet ist. Reserviert.<br/> **Datentyp:** FWP \_ UINT64<br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <dt>**\_FWPM-BEDINGUNG: \_ \_ ALE-SIO-FIREWALLSOCKETEIGENSCHAFT \_ \_ \_**</dt> </dl> | Für die interne Verwendung reserviert. <br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                                              |





| Für Windows Vista mit SP1, Windows Server 2008 und höher verfügbare Konstanten                                                                                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <dt>**SCHNITTSTELLE FÜR DIE \_ IP-ANKUNFT DER FWPM-BEDINGUNG \_ \_ \_**</dt> </dl>                       | Die LUID für die Netzwerkschnittstelle, die der IP-Adresse der Ankunft zugeordnet ist. <br/> **Datentyp:** FWP \_ UINT64<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <dt>**SCHNITTSTELLENTYP FÜR DIE ANKUNFT \_ DER FWPM-BEDINGUNG \_ \_ \_**</dt> </dl>                 | Der Typ der Ankunftsnetzwerkschnittstelle, wie von der Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Die in der Headerdatei Ipifcons.h aufgeführten Schnittstellentypwerte.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <dt>**FWPM \_ \_BEDINGUNGSTUNNELTYP \_ \_ "ANKUNFT"**</dt> </dl>                       | Die Kapselungsmethode, die von einem Tunnel verwendet wird, der der Ankunftsnetzwerkschnittstelle zugeordnet ist, wenn der Type-Member IF \_ TYPE \_ TUNNEL ist. Der Tunneltyp wird von der Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Die in der Headerdatei Ifdef.h aufgeführten Tunnel \_ TYPE-Enumerationstypwerte.<br/> **Datentyp:** FWP \_ UINT32<br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <dt>**FWPM \_ CONDITION \_ ARRIVAL \_ INTERFACE \_ INDEX**</dt> </dl>              | Der Index der Netzwerkschnittstelle für die Ankunft, wie vom Netzwerkstapel aufzählt.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <dt>**INDEX DER \_ \_ FWPM-BEDINGUNG FÜR \_ DIE ANKUNFT \_ DER \_ UNTERSCHNITTSTELLE**</dt> </dl> | Der Index der Netzwerkschnittstelle für die Ankunft, wie vom Netzwerkstapel aufzählt. <br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <dt>**INDEX DER LOKALEN SCHNITTSTELLE FÜR DIE \_ FWPM-BEDINGUNG \_ \_ \_**</dt> </dl>                    | Der Index der Netzwerkschnittstelle, wie vom Netzwerkstapel aufzählt. <br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <dt>**TYP DER LOKALEN \_ FWPM-BEDINGUNGSSCHNITTSTELLE \_ \_ \_**</dt> </dl>                       | Der Schnittstellentyp, der von der Internet Assigned Names Authority (IANA) definiert wird. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Die in der Headerdatei Ipifcons.h aufgeführten Schnittstellentypwerte.<br/> **Datentyp:** FWP \_ UINT32<br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <dt>**LOKALER \_ \_ FWPM-BEDINGUNGSTUNNELTYP \_ \_**</dt> </dl>                                | Die Kapselungsmethode, die von einem Tunnel verwendet wird, wenn der Type-Member IF \_ TYPE \_ TUNNEL ist. Der Tunneltyp wird von der Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Mögliche Werte:** Die in der Headerdatei Ifdef.h aufgeführten Tunnel \_ TYPE-Enumerationstypwerte.<br/> **Datentyp:** FWP \_ UINT32 <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstanten, die für Windows Vista und höher verfügbar sind</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die lokale IP-Adresse. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Remote-IP-Adresse. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Quell-IP-Adresse für weitergeleitete Pakete. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die IP-Zieladresse für weitergeleitete Pakete. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ der lokalen IP-Adresse. <br/> <strong>Mögliche Werte:</strong> Einer der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Ziel-IP-Adresstyp für weitergeleitete Pakete. <br/> <strong>Mögliche Werte:</strong> Einer der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">Die LUID für die Netzwerkschnittstelle, die der lokalen IP-Adresse zugeordnet ist. <br/> <strong>Datentyp:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Schnittstellentyp, der von der Internet Assigned Names Authority (IANA) definiert wird. Weitere Informationen finden Sie unter [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> <strong>Mögliche Werte:</strong> Die in der Headerdatei Ipifcons.h aufgeführten Schnittstellentypwerte.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Die Kapselungsmethode, die von einem Tunnel verwendet wird, wenn der Type-Member IF_TYPE_TUNNEL. Der Tunneltyp wird von der Internet Assigned Names Authority (IANA) definiert. Weitere Informationen finden Sie unter <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>. <br/> <strong>Mögliche Werte:</strong> Die TUNNEL_TYPE Enumerationstypwerte, die in der Headerdatei Ifdef.h aufgeführt sind.<br/> <strong>Datentyp:</strong> FWP_UINT32 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">Die LUID für die Netzwerkschnittstelle, an die das weitergeleitete Paket gesendet werden soll. <br/> <strong>Datentyp:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">Die IP-Protokollnummer, wie in RFC 1700 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des lokalen Transportprotokolls.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Das IcMP-Typfeld, wie in RFC 792 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des Remotetransportprotokolls. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">Das ICMP-Codefeld, wie in RFC 792 angegeben. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der lokale IP-Adresstyp, der in das ICMP-Paket eingebettet ist.<br/> <strong>Mögliche Werte:</strong> Einer der folgenden <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> Enumerationswerte.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Die Remote-IP-Adresse, die in das ICMP-Paket eingebettet ist. <br/> <strong>Datentyp:</strong> Für eine IPv4-Adresse
<ul>
<li>FWP_V4_ADDR_MASK oder</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Datentyp:</strong> Für eine IPv6-Adresse
<ul>
<li>FWP_V6_ADDR_MASK oder</li>
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
<td style="text-align: left;">Die Portnummer des lokalen Transportprotokolls, die in das ICMP-Paket eingebettet ist. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Die Portnummer des Remotetransportprotokolls, die in das ICMP-Paket eingebettet ist. <br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Ein bitweises OR einer Kombination von Filterbedingungsflags. <br/> <strong>Mögliche Werte:</strong> Weitere Informationen <a href="filtering-condition-flags-.md"> <strong>finden Sie unter Filterbedingungsflags.</strong></a><br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </dl></td>
<td style="text-align: left;">Die Richtung des Datenverkehrs oder Datenflusses. <br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>FWP_DIRECTION_INBOUND</li>
<li>FWP_DIRECTION_OUTBOUND</li>
</ul>
<br/> Für Datagrammebenen (FWPM_LAYER_DATAGRAM_DATA_ ) und *Streampaketebenen (FWPM_LAYER_STREAM_PACKET_)* ist der Wert mit der Richtung des Pakets identisch. <br/> Für Streamebenen (FWPM_LAYER_STREAM_ *) und flow-eingerichtete* Ebenen (FWPM_LAYER_ALE_FLOW_ESTABLISHED_) ist der Wert mit der Richtung der Verbindung identisch. (Wenn z. B. eine lokale Anwendung die Verbindung <strong></strong> initiiert, wurde für ein eingehendes Paket FWPM_CONDITION_DIRECTION auf <strong>FWP_DIRECTION_OUTBOUND.)</strong> <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der Netzwerkschnittstelle, wie vom Netzwerkstapel aufzählt. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der logischen Netzwerkschnittstelle, wie vom Netzwerkstapel aufzählt. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der Quellnetzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerkstapel aufzählt.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der logischen Quellnetzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerkstapel aufzählt. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der Zielnetzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerkstapel aufzählt. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Der Index der logischen Zielnetzwerkschnittstelle für weitergeleitete Pakete, wie vom Netzwerkstapel aufzählt. <br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">Der vollqualifizierte Gerätepfad der Anwendung, wie von der <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0-Funktion</strong></a> zurückgegeben. <br/> (Beispiel: &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .)<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifikation des lokalen Benutzers. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifikation des Remotebenutzers. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifikation des Remotecomputers. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </dl></td>
<td style="text-align: left;">Der unformatierte Socketmodus, der zugelassen oder verweigert wird.<br/> <strong>Mögliche Werte:  </strong>
<ul>
<li>SIO_RCVALL</li>
<li>SIO_RCVALL_IGMPMCAST</li>
<li>SIO_RCVALL_MCAST</li>
</ul>
Eine Beschreibung dieser unformatten Socketmodi finden Sie in der <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl-Funktion.</strong></a><br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
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



| Für Windows 8 und Windows Server 2012 verfügbare Benutzermodusbedingungen                                                                                                                       | Beschreibung                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <dt>**QM-MODUS DER FWPM-BEDINGUNG \_ \_ \_**</dt> </dl> | Der Modus des QM-Filters (Quick Mode). Mögliche Werte finden Sie unter [**\_ IPSEC-DATENVERKEHRSTYP. \_**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type)<br/> **Datentyp:** FWP \_ UINT32<br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Für Windows 7, Windows Server 2008 R2 und höher verfügbare Benutzermodusbedingungen</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;">Für die interne Verwendung reserviert.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </dl></td>
<td style="text-align: left;">Der Name des Peers. Beispielsweise der DNS-Name des Peers.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Die Identität des Remoteauthentifizierungsprinzipals. <br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ der IKE-, IKEv2- oder AuthIP-Authentifizierungsmethode. <br/> <strong>Datentyp:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ des Schlüsselmoduls.<br/> <strong>Datentyp:</strong> IKEEXT_KEY_MODULE_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </dl></td>
<td style="text-align: left;">Der IPsec-Modus, in dem ein Token abgerufen werden kann.<br/> <strong>Datentyp:</strong> IPSEC_TOKEN_MODE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </dl></td>
<td style="text-align: left;">Der Kontextschlüssel des Richtlinienanbieters für den Hauptmodus (MM) oder den Qm-Richtlinienanbieter des zu autorisierenden Sa. Nützlich zum Einschränken des Gültigkeitsbereichs der Autorisierungsregel auf SAs, die mit einem angegebenen IPsec MM- oder QM-Richtlinienschlüssel gebildet wurden.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Die Methode, die zum Authentifizieren der Sicherheitszuordnung verwendet wird.<br/>
<blockquote>
[!Note]<br />
Nur auf Windows Server 2008 R2, Windows 7 und höher verfügbar.
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
<th style="text-align: left;">Verfügbare Konstanten für Windows Vista und höher</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </dl></td>
<td style="text-align: left;">Die Identifikation des Remotebenutzers.<br/> <strong>Datentyp:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
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
<td style="text-align: left;">Die Identifikation der COM-Anwendung.<br/> <strong>Datentyp:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
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
<td style="text-align: left;">Der Authentifizierungsdiensttyp. Weitere Informationen zu Authentifizierungsdiensttypen finden Sie unter <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service-Konstanten.</strong></a> <br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </dl></td>
<td style="text-align: left;">Die Authentifizierungsdienstebene. Weitere Informationen zu Authentifizierungsdienstebenen finden Sie unter <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Konstanten auf Authentifizierungsebene.</strong></a> <br/> <strong>Datentyp:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </dl></td>
<td style="text-align: left;">Der zertifikatbasierte SSPI-Verschlüsselungsalgorithmus (Security Service Provider Interface).<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </dl></td>
<td style="text-align: left;">Die Größe des zertifikatbasierten SSPI-Verschlüsselungsschlüssels.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">Die lokale IPv4-Adresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK oder</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">Die lokale IPv6-Adresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">Die IPv4-Remoteadresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK oder</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">Die IPv6-Remoteadresse. <br/> <strong>Datentyp:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK oder</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <dt><strong>FWPM_CONDITION_PIPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Name der Remote-Named Pipe.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
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
<td style="text-align: left;">Der Port auf dem RPC-Server bei Verwendung von RpcProxy.<br/> <strong>Datentyp:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Rpc-Proxyauthentifizierungsdiensttyp.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </dl></td>
<td style="text-align: left;">Die SSL-Schlüssellänge (Secure Socket Layer) im Clientzertifikat.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </dl></td>
<td style="text-align: left;">Der Objektbezeichner im Clientzertifikat.<br/> <strong>Datentyp:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Der Typ des net-Ereignisses.<br/> <strong>Datentyp:</strong> FWP_UINT32<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Wenn IP-Adressen im FWP-UINT32-Format gespeichert werden oder wenn ein \_ IP-Port im FWP-UINT16-Format gespeichert wird, werden sie in Host- und nicht in Netzwerk \_ reihenfolge gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |
