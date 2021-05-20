---
description: Stellt die Attribute und Verhaltensweisen eines Netzwerkadapters dar. Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des TCP/IP-Protokolls unterstützen, das vom Netzwerkadapter unabhängig ist.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153573"
---
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="136dd-104">Win32 \_ NetworkAdapterConfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="136dd-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="136dd-105">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkAdapterConfiguration** stellt die Attribute und das Verhalten eines Netzwerkadapters dar.</span><span class="sxs-lookup"><span data-stu-id="136dd-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="136dd-106">Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des TCP/IP-Protokolls unterstützen, das vom Netzwerkadapter unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="136dd-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="136dd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="136dd-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="136dd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="136dd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="136dd-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a><span data-ttu-id="136dd-110">Member</span><span class="sxs-lookup"><span data-stu-id="136dd-110">Members</span></span>

<span data-ttu-id="136dd-111">Die **Win32 \_ NetworkAdapterConfiguration-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="136dd-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="136dd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="136dd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="136dd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="136dd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="136dd-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="136dd-114">Methods</span></span>

<span data-ttu-id="136dd-115">Die **Win32 \_ NetworkAdapterConfiguration-Klasse** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="136dd-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="136dd-116">Methode</span><span class="sxs-lookup"><span data-stu-id="136dd-116">Method</span></span>                                                                                                                       | <span data-ttu-id="136dd-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="136dd-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="136dd-118">**DisableIPSec**</span><span class="sxs-lookup"><span data-stu-id="136dd-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="136dd-119">Deaktiviert IPsec auf diesem TCP/IP-fähigen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="136dd-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="136dd-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="136dd-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="136dd-121">Aktiviert das Dynamic Host Configuration Protocol (DHCP) für den Dienst mit diesem Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="136dd-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="136dd-122">**EnableDNS**</span><span class="sxs-lookup"><span data-stu-id="136dd-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="136dd-123">Aktiviert die Domain Name System (DNS) für den Dienst auf diesem TCP/IP-gebundenen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="136dd-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="136dd-124">**EnableIPFilterSec**</span><span class="sxs-lookup"><span data-stu-id="136dd-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="136dd-125">Aktiviert IPsec global für alle IP-gebundenen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="136dd-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="136dd-126">**EnableIPSec**</span><span class="sxs-lookup"><span data-stu-id="136dd-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="136dd-127">Aktiviert IPsec auf diesem spezifischen TCP/IP-fähigen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="136dd-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="136dd-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="136dd-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="136dd-129">Aktiviert die statische TCP/IP-Adressierung für den Zielnetzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="136dd-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="136dd-130">**EnableWINS**</span><span class="sxs-lookup"><span data-stu-id="136dd-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="136dd-131">Aktiviert TCP/IP-spezifische WINS-Einstellungen, jedoch unabhängig vom Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="136dd-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="136dd-132">**ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="136dd-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="136dd-133">Gibt die IP-Adresse frei, die an einen bestimmten DHCP-fähigen Netzwerkadapter gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="136dd-134">**ReleaseDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="136dd-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="136dd-135">Gibt die IP-Adressen frei, die an alle DHCP-fähigen Netzwerkadapter gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="136dd-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="136dd-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="136dd-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="136dd-137">Erneuert die IP-Adresse auf bestimmten DHCP-fähigen Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="136dd-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="136dd-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="136dd-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="136dd-139">Erneuert die IP-Adressen auf allen DHCP-fähigen Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="136dd-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="136dd-140">**SetArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="136dd-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="136dd-141">Legt die Übertragung von ARP-Abfragen über TCP/IP fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="136dd-142">**SetArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="136dd-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="136dd-143">Ermöglicht Ethernet-Paketen die Verwendung der SNAP-Codierung 802.3.</span><span class="sxs-lookup"><span data-stu-id="136dd-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="136dd-144">**SetDatabasePath**</span><span class="sxs-lookup"><span data-stu-id="136dd-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="136dd-145">Legt den Pfad zu den standardmäßigen Internetdatenbankdateien (HOSTS, LMHOSTS, NETWORKS und PROTOCOLS) fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="136dd-146">**SetDeadGWDetect**</span><span class="sxs-lookup"><span data-stu-id="136dd-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="136dd-147">Aktiviert die Erkennung von toten Gateways.</span><span class="sxs-lookup"><span data-stu-id="136dd-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="136dd-148">**SetDefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="136dd-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="136dd-149">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="136dd-149">Obsolete.</span></span> <span data-ttu-id="136dd-150">Diese Methode legt den Standardwert für den Typ des Diensts (TOS) im Header der ausgehenden IP-Pakete fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="136dd-151">**SetDefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="136dd-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="136dd-152">Legt den Standardwert für die Gültigkeitsdauer (Time to Live, TTL) im Header ausgehender IP-Pakete fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="136dd-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="136dd-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="136dd-154">Legt die DNS-Domäne fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="136dd-155">**SetDNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="136dd-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="136dd-156">Legt die Serversuchreihenfolge als Array von Elementen fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="136dd-157">**SetDNSSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="136dd-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="136dd-158">Legt die Suffixsuchreihenfolge als Array von Elementen fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="136dd-159">**SetDynamicDNSRegistration**</span><span class="sxs-lookup"><span data-stu-id="136dd-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="136dd-160">Gibt die dynamische DNS-Registrierung von IP-Adressen für diesen IP-gebundenen Adapter an.</span><span class="sxs-lookup"><span data-stu-id="136dd-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="136dd-161">**SetForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="136dd-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="136dd-162">Gibt an, wie viel Speicher-IP zum Speichern von Paketdaten in der Routerpaketwarteschlange zuweist.</span><span class="sxs-lookup"><span data-stu-id="136dd-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="136dd-163">**SetGateways**</span><span class="sxs-lookup"><span data-stu-id="136dd-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="136dd-164">Gibt eine Liste von Gateways für das Routing von Paketen an, die für ein anderes Subnetz als das subnetz bestimmt sind, mit dem dieser Adapter verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="136dd-165">**SetIGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="136dd-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="136dd-166">Legt den Umfang fest, in dem das System IP-Multicasting unterstützt und am Internetgruppenverwaltungsprotokoll teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="136dd-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="136dd-167">**SetIPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="136dd-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="136dd-168">Legt die Routingmetrik fest, die diesem IP-gebundenen Adapter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="136dd-169">**SetIPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="136dd-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="136dd-170">Legt die IP-0-Broadcastverwendung fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="136dd-171">**SetIPXFrameTypeNetworkPairs**</span><span class="sxs-lookup"><span data-stu-id="136dd-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="136dd-172">Legt IPX-Netzwerknummer-/Framepaare (Internetworking Packet Exchange) für diesen Netzwerkadapter fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="136dd-173">**SetIPXVirtualNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="136dd-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="136dd-174">Legt die IPX-Netzwerknummer (Internetworking Packet Exchange) auf dem Zielcomputersystem fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="136dd-175">**SetKeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="136dd-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="136dd-176">Legt das Intervall fest, das Keep Alive-Neuübertragungen trennt, bis eine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="136dd-177">**SetKeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="136dd-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="136dd-178">Legt fest, wie oft TCP versucht, durch Senden eines Keep Alive-Pakets zu überprüfen, ob eine Verbindung im Leerlauf weiterhin verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="136dd-179">**SetMTU**</span><span class="sxs-lookup"><span data-stu-id="136dd-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="136dd-180">Legt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="136dd-181">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="136dd-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="136dd-182">**SetNumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="136dd-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="136dd-183">Legt die Anzahl der IP-Paketheader fest, die der Routerpaketwarteschlange zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="136dd-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="136dd-184">**SetPMTUBHDetect**</span><span class="sxs-lookup"><span data-stu-id="136dd-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="136dd-185">Ermöglicht die Erkennung von Black Hole-Routern.</span><span class="sxs-lookup"><span data-stu-id="136dd-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="136dd-186">**SetPMTUDiscovery**</span><span class="sxs-lookup"><span data-stu-id="136dd-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="136dd-187">Aktiviert die Ermittlung der maximalen Übertragungseinheit (Maximum Transmission Unit, MTU).</span><span class="sxs-lookup"><span data-stu-id="136dd-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="136dd-188">**SetTcpipNetbios**</span><span class="sxs-lookup"><span data-stu-id="136dd-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="136dd-189">Legt den Standardvorgang von NetBIOS über TCP/IP fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="136dd-190">**SetTcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="136dd-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="136dd-191">Legt die Anzahl der Versuche fest, mit der TCP eine Verbindungsanforderung vor dem Abbruch erneut überträgt.</span><span class="sxs-lookup"><span data-stu-id="136dd-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="136dd-192">**SetTcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="136dd-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="136dd-193">Legt fest, wie oft TCP ein einzelnes Datensegment erneut überträgt, bevor die Verbindung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="136dd-194">**SetTcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="136dd-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="136dd-195">Legt die maximale Anzahl von Verbindungen fest, die TCP möglicherweise gleichzeitig geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="136dd-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="136dd-196">**SetTcpUseRFC1122RolentPointer**</span><span class="sxs-lookup"><span data-stu-id="136dd-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="136dd-197">Gibt an, ob TCP die RFC 1122-Spezifikation für dringende Daten oder den Modus verwendet, der von BSD-abgeleiteten Systemen (California Software Design) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="136dd-198">**SetTcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="136dd-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="136dd-199">Legt die maximale TCP-Empfangsfenstergröße fest, die vom System angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="136dd-200">**SetWINSServer**</span><span class="sxs-lookup"><span data-stu-id="136dd-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="136dd-201">Legt die primären und sekundären WINDOWS-WINS-Server (Internet Naming Service) auf diesem TCP/IP-gebundenen Netzwerkadapter fest.</span><span class="sxs-lookup"><span data-stu-id="136dd-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="136dd-202">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="136dd-202">Properties</span></span>

<span data-ttu-id="136dd-203">Die **Win32 \_ NetworkAdapterConfiguration-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="136dd-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="136dd-204">**ArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="136dd-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-205">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-207">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")</span><span class="sxs-lookup"><span data-stu-id="136dd-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-208">True gibt an, dass TCP/IP ARP-Abfragen (Address Resolution Protocol) mit aktiviertem Quellrouting in TokenRing-Netzwerken überträgt.</span><span class="sxs-lookup"><span data-stu-id="136dd-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="136dd-209">Standardmäßig (FALSE) fragt ARP zuerst ohne Quellrouting ab und dann erneut, wenn das Quellrouting aktiviert ist, wenn keine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="136dd-210">Das Quellrouting ermöglicht das Routing von Netzwerkpaketen über verschiedene Netzwerktypen hinweg.</span><span class="sxs-lookup"><span data-stu-id="136dd-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-211">**ArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="136dd-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-212">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-214">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpUseEtherSNAP")</span><span class="sxs-lookup"><span data-stu-id="136dd-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-215">True **gibt an,** dass Ethernet-Pakete der IEEE 802.3-Codierung Sub-Network Access Protocol (SNAP) folgen.</span><span class="sxs-lookup"><span data-stu-id="136dd-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="136dd-216">Durch Festlegen dieses Parameters auf 1 wird die Übertragung von Ethernet-Paketen durch TCP/IP mithilfe der SNAP-Codierung 802.3 erzwingt.</span><span class="sxs-lookup"><span data-stu-id="136dd-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="136dd-217">Standardmäßig (FALSE) überträgt der Stapel Pakete im DIX-Ethernet-Format.</span><span class="sxs-lookup"><span data-stu-id="136dd-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="136dd-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="136dd-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-221">Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="136dd-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="136dd-222">Kurze Textbeschreibung des aktuellen Objekts.</span><span class="sxs-lookup"><span data-stu-id="136dd-222">Short textual description of the current object.</span></span>

<span data-ttu-id="136dd-223">Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)</span><span class="sxs-lookup"><span data-stu-id="136dd-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="136dd-224">**Databasepath**</span><span class="sxs-lookup"><span data-stu-id="136dd-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="136dd-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-227">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DatabasePath")</span><span class="sxs-lookup"><span data-stu-id="136dd-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-228">Gültiger Windows-Dateipfad zu Standardmäßigen Internetdatenbankdateien (HOSTS, LMHOSTS, NETWORKS und PROTOCOLS).</span><span class="sxs-lookup"><span data-stu-id="136dd-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="136dd-229">Der Dateipfad wird von der Windows Sockets-Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="136dd-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-230">**DeadGWDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-231">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-233">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDeadGWDetect")</span><span class="sxs-lookup"><span data-stu-id="136dd-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-234">True **gibt an,** dass die Erkennung von toten Gateways auftritt.</span><span class="sxs-lookup"><span data-stu-id="136dd-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="136dd-235">Wenn dieses Feature aktiviert ist, fordert TCP (Transmission Control Protocol) das Internetprotokoll (IP) auf, zu einem Sicherungsgateway zu wechseln, wenn es ein Segment mehrmals erneut überträgt, ohne eine Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="136dd-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="136dd-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-237">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-239">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| DefaultGateway")</span><span class="sxs-lookup"><span data-stu-id="136dd-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-240">Array von IP-Adressen von Standardgateways, die vom Computersystem verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="136dd-241">Beispiel: "192.168.12.1 192.168.46.1"</span><span class="sxs-lookup"><span data-stu-id="136dd-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-242">**DefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="136dd-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-243">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="136dd-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-245">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTOS")</span><span class="sxs-lookup"><span data-stu-id="136dd-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-246">Der Im Header ausgehender IP-Pakete festgelegte Standardwert für den Diensttyp (Type Of Service, TOS).</span><span class="sxs-lookup"><span data-stu-id="136dd-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="136dd-247">Request for Comments (RFC) 791 definiert die Werte.</span><span class="sxs-lookup"><span data-stu-id="136dd-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="136dd-248">Standardwert: 0 (null), Gültiger Bereich: 0 bis 255.</span><span class="sxs-lookup"><span data-stu-id="136dd-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="136dd-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-250">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="136dd-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-252">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTTL")</span><span class="sxs-lookup"><span data-stu-id="136dd-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-253">Der Standardwert für die Gültigkeitsdauer (Time To Live, TTL), der im Header ausgehender IP-Pakete festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="136dd-254">Die Gültigkeitsdauer gibt die Anzahl der Router an, die ein IP-Paket passieren kann, um das Ziel zu erreichen, bevor es verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="136dd-255">Jeder Router dekrementiert die TTL-Anzahl eines Pakets um eins, während es durchläuft, und verwirft die Pakete – wenn die Gültigkeitsdauer 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="136dd-256">Standardwert: 32, gültiger Bereich: 1 bis 255.</span><span class="sxs-lookup"><span data-stu-id="136dd-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-257">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="136dd-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-258">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="136dd-260">Textbeschreibung des aktuellen -Objekts.</span><span class="sxs-lookup"><span data-stu-id="136dd-260">Textual description of the current object.</span></span>

<span data-ttu-id="136dd-261">Diese Eigenschaft wird von [**der \_ CIM-Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="136dd-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="136dd-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-263">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-265">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")</span><span class="sxs-lookup"><span data-stu-id="136dd-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-266">True gibt an, dass der DHCP-Server (Dynamic Host Configuration Protocol) dem Computersystem automatisch eine IP-Adresse zuweist, wenn eine Netzwerkverbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-267">**DHCPLeaseExpires**</span><span class="sxs-lookup"><span data-stu-id="136dd-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-268">Datentyp: **datetime**</span><span class="sxs-lookup"><span data-stu-id="136dd-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-270">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")</span><span class="sxs-lookup"><span data-stu-id="136dd-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-271">Ablaufdatum und -uhrzeit für eine geleaste IP-Adresse, die dem Computer vom DHCP-Server (Dynamic Host Configuration Protocol) zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="136dd-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="136dd-272">Beispiel: 20521201000230.000000000</span><span class="sxs-lookup"><span data-stu-id="136dd-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="136dd-273">**DHCPLeaseObtained**</span><span class="sxs-lookup"><span data-stu-id="136dd-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-274">Datentyp: **datetime**</span><span class="sxs-lookup"><span data-stu-id="136dd-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-276">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")</span><span class="sxs-lookup"><span data-stu-id="136dd-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-277">Datum und Uhrzeit des Leases für die IP-Adresse, die dem Computer vom DHCP-Server (Dynamic Host Configuration Protocol) zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="136dd-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="136dd-278">Beispiel: 19521201000230.000000000</span><span class="sxs-lookup"><span data-stu-id="136dd-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="136dd-279">**DHCPServer**</span><span class="sxs-lookup"><span data-stu-id="136dd-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="136dd-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-282">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")</span><span class="sxs-lookup"><span data-stu-id="136dd-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-283">IP-Adresse des DHCP-Servers (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="136dd-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="136dd-284">Beispiel: "10.55.34.2"</span><span class="sxs-lookup"><span data-stu-id="136dd-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="136dd-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="136dd-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-288">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Domain")</span><span class="sxs-lookup"><span data-stu-id="136dd-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-289">Organisationsname, gefolgt von einem Zeitraum und einer Erweiterung, die den Typ der Organisation angibt, z. B. "microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="136dd-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="136dd-290">Der Name kann eine beliebige Kombination aus den Buchstaben A bis Z, den Ziffern 0 bis 9 und dem Bindestrich (-) sowie dem als Trennzeichen verwendeten Zeitraum (.) sein.</span><span class="sxs-lookup"><span data-stu-id="136dd-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="136dd-291">Beispiel: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="136dd-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-292">**DNSDomainSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="136dd-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-293">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-295">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| SearchList")</span><span class="sxs-lookup"><span data-stu-id="136dd-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-296">Array von DNS-Domänensuffixen, die während der Namensauflösung an das Ende der Hostnamen angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="136dd-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="136dd-297">Beim Versuch, einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) aus einem reinen Hostnamen aufzulösen, fügt das System zuerst den lokalen Domänennamen an.</span><span class="sxs-lookup"><span data-stu-id="136dd-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="136dd-298">Wenn dies nicht erfolgreich ist, verwendet das System die Domänensuffixliste, um zusätzliche FQDNs in der aufgeführten Reihenfolge zu erstellen und dns-Server für jeden abzufragen.</span><span class="sxs-lookup"><span data-stu-id="136dd-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="136dd-299">Beispiel: "samples.microsoft.com example.microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="136dd-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-300">**DNSEnabledForWINSResolution**</span><span class="sxs-lookup"><span data-stu-id="136dd-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-301">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-303">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDNS")</span><span class="sxs-lookup"><span data-stu-id="136dd-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-304">**True** gibt an, dass die Domain Name System (DNS) für die Namensauflösung über die WINS-Auflösung (Internet Naming Service) von Windows aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="136dd-305">Wenn der Name nicht mit DNS aufgelöst werden kann, wird die Namensanforderung zur Auflösung an WINS weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="136dd-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-306">**Dnshostname**</span><span class="sxs-lookup"><span data-stu-id="136dd-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-307">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-309">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Hostname")</span><span class="sxs-lookup"><span data-stu-id="136dd-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-310">Hostname, der verwendet wird, um den lokalen Computer für die Authentifizierung durch einige Hilfsprogramme zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="136dd-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="136dd-311">Andere TCP/IP-basierte Hilfsprogramme können diesen Wert verwenden, um den Namen des lokalen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="136dd-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="136dd-312">Hostnamen werden auf DNS-Servern in einer Tabelle gespeichert, in der Namen IP-Adressen zur Verwendung durch DNS zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="136dd-313">Der Name kann eine beliebige Kombination aus den Buchstaben A bis Z, den Ziffern 0 bis 9 und dem Bindestrich (-) sowie dem Punktzeichen (.) sein, das als Trennzeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="136dd-314">Standardmäßig ist dieser Wert der Name des Microsoft-Netzwerkcomputers, aber der Netzwerkadministrator kann einen anderen Hostnamen zuweisen, ohne dass sich dies auf den Computernamen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="136dd-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="136dd-315">Beispiel: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="136dd-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-316">**DNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="136dd-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-317">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-319">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NameServer")</span><span class="sxs-lookup"><span data-stu-id="136dd-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-320">Array von Server-IP-Adressen, die beim Abfragen von DNS-Servern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="136dd-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-321">**DomainDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-322">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="136dd-324">True **gibt** an, dass die IP-Adressen für diese Verbindung nicht nur unter dem vollständigen DNS-Namen des Computers, sondern auch im DNS unter dem Domänennamen dieser Verbindung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="136dd-325">Der Domänenname dieser Verbindung wird entweder mithilfe der [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)()-Methode festgelegt oder von DSCP zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="136dd-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="136dd-326">Der registrierte Name ist der Hostname des Computers, an den der Domänenname angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-327">**ForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="136dd-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-328">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-330">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="136dd-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-331">Durch IP zugewiesener Arbeitsspeicher zum Speichern von Paketdaten in der Routerpaketwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="136dd-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="136dd-332">Wenn dieser Pufferspeicher gefüllt ist, beginnt der Router damit, Pakete nach dem Zufallsprinzip aus seiner Warteschlange zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="136dd-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="136dd-333">Paketwarteschlangen-Datenpuffer haben eine Länge von 256 Bytes, daher sollte der Wert dieses Parameters ein Vielfaches von 256 sein.</span><span class="sxs-lookup"><span data-stu-id="136dd-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="136dd-334">Mehrere Puffer werden für größere Pakete miteinander verkettet.</span><span class="sxs-lookup"><span data-stu-id="136dd-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="136dd-335">Der IP-Header für ein Paket wird separat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="136dd-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="136dd-336">Dieser Parameter wird ignoriert, und es werden keine Puffer zugeordnet, wenn der IP-Router nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="136dd-337">Die Puffergröße kann von der Netzwerk-MTU bis zu einem Wert reichen, der kleiner als 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="136dd-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="136dd-338">Standardwert: 74240 (1480-Byte-Pakete, gerundet auf ein Vielfaches von 256).</span><span class="sxs-lookup"><span data-stu-id="136dd-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="136dd-339">**FullDNSRegistrationEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-340">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="136dd-342">**True** gibt an, dass die IP-Adressen für diese Verbindung im DNS unter dem vollständigen DNS-Namen des Computers registriert werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="136dd-343">Der vollständige DNS-Name des Computers wird auf der Registerkarte **Netzwerkidentifikation** in der Systemanwendung in Systemsteuerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="136dd-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-344">**GatewayCostMetric**</span><span class="sxs-lookup"><span data-stu-id="136dd-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-345">Datentyp: **uint16-Array**</span><span class="sxs-lookup"><span data-stu-id="136dd-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="136dd-347">Array ganzzahliger Kostenmetrikwerte (im Bereich von 1 bis 9999), die zum Berechnen der schnellsten, zuverlässigsten oder ressourcenintensivsten Routen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="136dd-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="136dd-348">Dieses Argument weist eine 1:1-Entsprechung mit der **DefaultIPGateway-Eigenschaft** auf.</span><span class="sxs-lookup"><span data-stu-id="136dd-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-349">**IGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="136dd-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-350">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="136dd-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-352">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IGMPLevel")</span><span class="sxs-lookup"><span data-stu-id="136dd-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-353">Umfang, in dem das System IP-Multicast unterstützt und am Internet Group Management Protocol (IGMP) teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="136dd-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="136dd-354">Auf Ebene 0 (null) bietet das System keine Multicastunterstützung.</span><span class="sxs-lookup"><span data-stu-id="136dd-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="136dd-355">Auf Ebene 1 kann das System nur IP-Multicastpakete senden.</span><span class="sxs-lookup"><span data-stu-id="136dd-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="136dd-356">Auf Ebene 2 kann das System IP-Multicastpakete senden und vollständig an IGMP teilnehmen, um Multicastpakete zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="136dd-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="136dd-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Kein Multicast** (0)</span><span class="sxs-lookup"><span data-stu-id="136dd-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="136dd-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP-Multicast** (1)</span><span class="sxs-lookup"><span data-stu-id="136dd-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="136dd-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP-& IGMP-Multicast** (2)</span><span class="sxs-lookup"><span data-stu-id="136dd-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="136dd-360">IP und IGMP Multicast (Standard)</span><span class="sxs-lookup"><span data-stu-id="136dd-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="136dd-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="136dd-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-362">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-364">Qualifizierer: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="136dd-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-365">Indexnummer der Konfiguration des Windows-Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="136dd-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="136dd-366">Die Indexnummer wird verwendet, wenn mehrere Konfigurationen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="136dd-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-367">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="136dd-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-368">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="136dd-370">Indexwert, der eine lokale Netzwerkschnittstelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="136dd-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="136dd-371">Der Wert in dieser Eigenschaft entspricht dem Wert in der **InterfaceIndex-Eigenschaft** in der Instanz von [**Win32 \_ IP4RouteTable,**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) der die Netzwerkschnittstelle in der Routentabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="136dd-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-372">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="136dd-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-373">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-375">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip \| IPAddress")</span><span class="sxs-lookup"><span data-stu-id="136dd-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-376">Array aller IP-Adressen, die dem aktuellen Netzwerkadapter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="136dd-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="136dd-377">Diese Eigenschaft kann entweder IPv6-Adressen oder IPv4-Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="136dd-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="136dd-378">Weitere Informationen finden Sie unter [IPv6- und IPv4-Unterstützung in WMI.](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)</span><span class="sxs-lookup"><span data-stu-id="136dd-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="136dd-379">Beispiel-IPv6-Adresse: "2010:836B:4179::836B:4179"</span><span class="sxs-lookup"><span data-stu-id="136dd-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-380">**IPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="136dd-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-381">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="136dd-383">Die Kosten für die Verwendung der konfigurierten Routen für den IP-gebundenen Adapter und der gewichtete Wert für diese Routen in der IP-Routingtabelle.</span><span class="sxs-lookup"><span data-stu-id="136dd-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="136dd-384">Wenn die IP-Routingtabelle mehrere Routen zu einem Ziel enthält, wird die Route mit der niedrigsten Metrik verwendet.</span><span class="sxs-lookup"><span data-stu-id="136dd-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="136dd-385">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="136dd-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-387">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-389">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip")</span><span class="sxs-lookup"><span data-stu-id="136dd-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-390">True **gibt an,** dass TCP/IP gebunden und auf diesem Netzwerkadapter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-391">**IPFilterSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-392">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-394">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="136dd-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-395">**True** gibt an, dass die IP-Portsicherheit global für alle IP-gebundenen Netzwerkadapter aktiviert ist, und die Sicherheitswerte, die einzelnen Netzwerkadaptern zugeordnet sind, sind wirksam.</span><span class="sxs-lookup"><span data-stu-id="136dd-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="136dd-396">Diese Eigenschaft wird in Verbindung mit **IPSecPermitTCPPorts,** **IPSecPermitUDPPorts** und **IPSecPermitIPProtocols** verwendet.</span><span class="sxs-lookup"><span data-stu-id="136dd-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="136dd-397">**False** gibt an, dass die IP-Filtersicherheit für alle Netzwerkadapter deaktiviert ist und den ungefilterten Fluss des gesamten Port- und Protokolldatenverkehrs zulässt.</span><span class="sxs-lookup"><span data-stu-id="136dd-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-398">**IPPortSecurityEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-399">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-401">Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")</span><span class="sxs-lookup"><span data-stu-id="136dd-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-402">**True** gibt an, dass die IP-Portsicherheit global für alle IP-gebundenen Netzwerkadapter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="136dd-403">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="136dd-403">This property is obsolete.</span></span> <span data-ttu-id="136dd-404">Anstelle dieser Eigenschaft sollten Sie **IPFilterSecurityEnabled** verwenden.</span><span class="sxs-lookup"><span data-stu-id="136dd-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-405">**IPSecPermitIPProtocols**</span><span class="sxs-lookup"><span data-stu-id="136dd-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-406">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-408">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| RawIPAllowedProtocols")</span><span class="sxs-lookup"><span data-stu-id="136dd-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-409">Array der Protokolle, die über die IP-Adresse ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="136dd-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="136dd-410">Die Liste der Protokolle wird mithilfe der [**EnableIPSec-Methode**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="136dd-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="136dd-411">Die Liste ist entweder leer oder enthält numerische Werte.</span><span class="sxs-lookup"><span data-stu-id="136dd-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="136dd-412">Der numerische Wert 0 (null) gibt an, dass die Zugriffsberechtigung für alle Protokolle erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="136dd-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="136dd-413">Eine leere Zeichenfolge gibt an, dass keine Protokolle ausgeführt werden dürfen, wenn **IPFilterSecurityEnabled** **TRUE** ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-414">**IPSecPermitTCPPorts**</span><span class="sxs-lookup"><span data-stu-id="136dd-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-415">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-417">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TCPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="136dd-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-418">Array der Ports, denen die Zugriffsberechtigung für TCP erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="136dd-419">Die Liste der Protokolle wird mithilfe der [**EnableIPSec-Methode**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="136dd-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="136dd-420">Die Liste ist entweder leer oder enthält numerische Werte.</span><span class="sxs-lookup"><span data-stu-id="136dd-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="136dd-421">Der numerische Wert 0 (null) gibt an, dass die Zugriffsberechtigung für alle Ports erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="136dd-422">Eine leere Zeichenfolge gibt an, dass keine Zugriffsberechtigung für Ports erteilt wird, **wenn IPFilterSecurityEnabled** **true ist.**</span><span class="sxs-lookup"><span data-stu-id="136dd-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-423">**IPSecPermitUDPPorts**</span><span class="sxs-lookup"><span data-stu-id="136dd-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-424">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-426">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UDPAllowedPorts")</span><span class="sxs-lookup"><span data-stu-id="136dd-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-427">Array der Ports, denen die UDP-Zugriffsberechtigung (User Datagram Protocol) erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="136dd-428">Die Liste der Protokolle wird mithilfe der [**EnableIPSec-Methode**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="136dd-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="136dd-429">Die Liste ist entweder leer oder enthält numerische Werte.</span><span class="sxs-lookup"><span data-stu-id="136dd-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="136dd-430">Der numerische Wert 0 (null) gibt an, dass die Zugriffsberechtigung für alle Ports erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="136dd-431">Eine leere Zeichenfolge gibt an, dass keine Zugriffsberechtigung für Ports erteilt wird, **wenn IPFilterSecurityEnabled** **true ist.**</span><span class="sxs-lookup"><span data-stu-id="136dd-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="136dd-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-433">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-435">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| SubnetMask")</span><span class="sxs-lookup"><span data-stu-id="136dd-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-436">Array aller Subnetzmasken, die dem aktuellen Netzwerkadapter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="136dd-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="136dd-437">Beispiel: "255.255.0.0"</span><span class="sxs-lookup"><span data-stu-id="136dd-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-438">**IPUseZeroBroadcast**</span><span class="sxs-lookup"><span data-stu-id="136dd-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-439">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-441">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UseZeroBroadcast")</span><span class="sxs-lookup"><span data-stu-id="136dd-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-442">True gibt an, dass IP-Nullen-Broadcasts verwendet werden (0.0.0.0), und das System verwendet Eins-Broadcasts (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="136dd-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="136dd-443">Computersysteme verwenden in der Regel Eins-Broadcasts, aber die von BSD-Implementierungen abgeleiteten Verwenden Nullen-Broadcasts.</span><span class="sxs-lookup"><span data-stu-id="136dd-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="136dd-444">Systeme, die nicht dieselben Broadcasts verwenden, können nicht im selben Netzwerk zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="136dd-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="136dd-445">Der Standardwert ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="136dd-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-446">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="136dd-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-447">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-449">Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS")</span><span class="sxs-lookup"><span data-stu-id="136dd-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-450">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="136dd-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-451">**IPXEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-452">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-454">Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="136dd-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-455">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="136dd-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-456">**IPXFrameType**</span><span class="sxs-lookup"><span data-stu-id="136dd-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-457">Datentyp: **uint32-Array**</span><span class="sxs-lookup"><span data-stu-id="136dd-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-459">Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| PktType")</span><span class="sxs-lookup"><span data-stu-id="136dd-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-460">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="136dd-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="136dd-461">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="136dd-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="136dd-462">**Ethernet 802.3** (1)</span><span class="sxs-lookup"><span data-stu-id="136dd-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="136dd-463">**Ethernet 802.2** (2)</span><span class="sxs-lookup"><span data-stu-id="136dd-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="136dd-464">**Ethernet-SNAP** (3)</span><span class="sxs-lookup"><span data-stu-id="136dd-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="136dd-465">**AUTO** (255)</span><span class="sxs-lookup"><span data-stu-id="136dd-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="136dd-466">**IPXMediaType**</span><span class="sxs-lookup"><span data-stu-id="136dd-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-467">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-469">Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| MediaType")</span><span class="sxs-lookup"><span data-stu-id="136dd-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-470">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="136dd-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="136dd-471">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="136dd-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="136dd-472">**Tokenring** (2)</span><span class="sxs-lookup"><span data-stu-id="136dd-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="136dd-473">**FDDI** (3)</span><span class="sxs-lookup"><span data-stu-id="136dd-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="136dd-474">**ARCNET** (8)</span><span class="sxs-lookup"><span data-stu-id="136dd-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="136dd-475">**IPXNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="136dd-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-476">Datentyp: **Zeichenfolgenarray**</span><span class="sxs-lookup"><span data-stu-id="136dd-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="136dd-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-478">Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| NetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="136dd-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-479">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="136dd-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-480">**IPXVirtualNetNumber**</span><span class="sxs-lookup"><span data-stu-id="136dd-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="136dd-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-483">Qualifizierer: [**VERALTET**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| VirtualNetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="136dd-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-484">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="136dd-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="136dd-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-486">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-488">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="136dd-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-489">Intervall, das Keep Alive-Neuübertragungen trennt, bis eine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="136dd-490">Nachdem eine Antwort empfangen wurde, wird die Verzögerung bis zur nächsten Keep Alive-Übertragung wieder durch den Wert von **KeepAliveTime** gesteuert.</span><span class="sxs-lookup"><span data-stu-id="136dd-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="136dd-491">Die Verbindung wird abgebrochen, nachdem die Anzahl der von **TcpMaxDataRetransmissions angegebenen Neuübertragungen** nicht mehr beantwortet wurde.</span><span class="sxs-lookup"><span data-stu-id="136dd-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="136dd-492">Standardwert: 1000, Gültiger Bereich: 1 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="136dd-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="136dd-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-494">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-496">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="136dd-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-497">Die **KeepAliveTime-Eigenschaft** gibt an, wie oft tcp versucht, zu überprüfen, ob eine Leerlaufverbindung noch intakt ist, indem ein Keep Alive-Paket gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="136dd-498">Ein erreichbares Remotesystem bestätigt die Keep-Alive-Übertragung.</span><span class="sxs-lookup"><span data-stu-id="136dd-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="136dd-499">Keep Alive-Pakete werden standardmäßig nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="136dd-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="136dd-500">Dieses Feature kann in einer Verbindung von einer Anwendung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="136dd-501">Standardwert: 7.200.000 (zwei Stunden).</span><span class="sxs-lookup"><span data-stu-id="136dd-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="136dd-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="136dd-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-503">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-505">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Geräteeingabe- \| und -ausgabefunktionen \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="136dd-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-506">Mac-Adresse (Media Access Control) des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="136dd-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="136dd-507">Eine MAC-Adresse wird vom Hersteller zugewiesen, um den Netzwerkadapter eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="136dd-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="136dd-508">Beispiel: "00:80:C7:8F:6C:96"</span><span class="sxs-lookup"><span data-stu-id="136dd-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-509">**MTU**</span><span class="sxs-lookup"><span data-stu-id="136dd-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-510">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-511">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-512">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="136dd-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-513">Überschreibt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="136dd-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="136dd-514">Die MTU ist die maximale Paketgröße (einschließlich des Transportheaders), die der Transport über das zugrunde liegende Netzwerk überträgt.</span><span class="sxs-lookup"><span data-stu-id="136dd-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="136dd-515">Das IP-Datagramm kann mehrere Pakete umfassen.</span><span class="sxs-lookup"><span data-stu-id="136dd-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="136dd-516">Der Bereich dieses Werts umfasst die mindeste Paketgröße (68) bis zur MTU, die vom zugrunde liegenden Netzwerk unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-517">**NumForwardPackets**</span><span class="sxs-lookup"><span data-stu-id="136dd-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-518">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-520">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NumForwardPackets")</span><span class="sxs-lookup"><span data-stu-id="136dd-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-521">Anzahl der IP-Paketheader, die der Routerpaketwarteschlange zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="136dd-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="136dd-522">Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="136dd-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="136dd-523">Dieser Wert sollte mindestens so groß sein wie der **ForwardBufferMemory-Wert** dividiert durch die maximale IP-Datengröße der mit dem Router verbundenen Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="136dd-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="136dd-524">Er sollte nicht größer als der **ForwardBufferMemory-Wert** dividiert durch 256 sein, da mindestens 256 Bytes Vorwärtspufferspeicher für jedes Paket verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="136dd-525">Die optimale Anzahl von Forward-Paketen für eine bestimmte **ForwardBufferMemory-Größe** hängt vom Typ des Datenverkehrs im Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="136dd-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="136dd-526">Sie liegt zwischen diesen beiden Werten.</span><span class="sxs-lookup"><span data-stu-id="136dd-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="136dd-527">Wenn der Router nicht aktiviert ist, wird dieser Parameter ignoriert, und es werden keine Header zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="136dd-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="136dd-528">Standardwert: 50, Gültiger Bereich: 1 – 0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="136dd-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-529">**PMTUBHDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-530">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-531">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-532">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUBHDetect")</span><span class="sxs-lookup"><span data-stu-id="136dd-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-533">True **gibt an,** dass die Erkennung von Routern mit schwarzer Lücke erfolgt, während TCP den Pfad der maximalen Übertragungseinheit entdeckt.</span><span class="sxs-lookup"><span data-stu-id="136dd-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="136dd-534">Ein Router mit schwarzer Lücke gibt keine ICMP-Zielnachrichten zurück, die nicht erreichbar sind, wenn ein IP-Datagramm fragmentiert werden muss, wenn das Bit Nicht fragmentieren festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="136dd-535">TCP hängt vom Empfang dieser Nachrichten ab, um die Pfad-MTU-Ermittlung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="136dd-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="136dd-536">Wenn dieses Feature aktiviert ist, versucht TCP, Segmente zu senden, ohne dass das Bit "Nicht fragmentieren" festgelegt ist, wenn mehrere Neuübertragungen eines Segments nicht bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="136dd-537">Wenn das Segment als Ergebnis bestätigt wird, wird der MSS verringert, und das Bit Nicht fragmentieren wird in zukünftigen Paketen für die Verbindung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="136dd-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="136dd-538">Durch die Aktivierung der Erkennung schwarzer Löcher erhöht sich die maximale Anzahl von Neuübertragungen, die für ein bestimmtes Segment ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="136dd-539">Der Standardwert dieser Eigenschaft ist **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="136dd-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-540">**PMTUDiscoveryEnabled**</span><span class="sxs-lookup"><span data-stu-id="136dd-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-541">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-543">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUDiscovery")</span><span class="sxs-lookup"><span data-stu-id="136dd-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-544">True gibt an, dass der Pfad der maximalen Übertragungseinheit (Maximum Transmission Unit, MTU) über den Pfad zu einem Remotehost ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="136dd-545">Indem der MTU-Pfad entdeckt und TCP-Segmente auf diese Größe beschränkt werden, kann TCP die Fragmentierung an Routern entlang des Pfads beseitigen, die Netzwerke mit unterschiedlichen MTUs verbinden.</span><span class="sxs-lookup"><span data-stu-id="136dd-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="136dd-546">Fragmentierung wirkt sich negativ auf TCP-Durchsatz und Netzwerküberlastung aus.</span><span class="sxs-lookup"><span data-stu-id="136dd-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="136dd-547">Wenn Sie diesen Parameter auf **FALSE** festlegen, wird eine MTU von 576 Bytes für alle Verbindungen verwendet, die nicht mit Computern im lokalen Subnetz verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="136dd-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="136dd-548">Der Standardwert ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="136dd-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-549">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="136dd-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-550">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-551">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-552">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="136dd-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-553">Dienstname des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="136dd-553">Service name of the network adapter.</span></span> <span data-ttu-id="136dd-554">Dieser Name ist in der Regel kürzer als der vollständige Produktname.</span><span class="sxs-lookup"><span data-stu-id="136dd-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="136dd-555">Beispiel: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="136dd-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="136dd-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="136dd-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-557">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-558">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-559">Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="136dd-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="136dd-560">Bezeichner, unter dem das aktuelle Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="136dd-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="136dd-561">Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)</span><span class="sxs-lookup"><span data-stu-id="136dd-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="136dd-562">**TcpipNetbiosOptions**</span><span class="sxs-lookup"><span data-stu-id="136dd-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-563">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-564">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="136dd-565">Bitmap der möglichen Einstellungen im Zusammenhang mit NetBIOS über TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="136dd-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="136dd-566">Werte werden in der folgenden Liste identifiziert.</span><span class="sxs-lookup"><span data-stu-id="136dd-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="136dd-567">**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="136dd-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="136dd-568">**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="136dd-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="136dd-569">**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="136dd-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="136dd-570">**TcpMaxConnectRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="136dd-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-571">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-572">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-573">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxConnectRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="136dd-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-574">Gibt an, wie oft TCP versucht, eine Connect-Anforderung erneut zu übertragen, bevor die Verbindung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="136dd-575">Das anfängliche Timeout für die Neuübertragung beträgt 3 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="136dd-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="136dd-576">Das Neuübertragungs-Timeout verdoppelt sich für jeden Versuch.</span><span class="sxs-lookup"><span data-stu-id="136dd-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="136dd-577">Standardwert: 3, Gültiger Bereich: 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="136dd-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="136dd-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-579">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-580">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-581">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="136dd-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-582">Gibt an, wie oft TCP ein einzelnes Datensegment (Nichtverbindungssegment) erneut überträgt, bevor die Verbindung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="136dd-583">Das Timeout für die Neuübertragung verdoppelt sich mit jeder nachfolgenden Neuübertragung für eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="136dd-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="136dd-584">Standardwert: 5, Gültiger Bereich: 0 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="136dd-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-585">**Tcpnumconnections**</span><span class="sxs-lookup"><span data-stu-id="136dd-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-586">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="136dd-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-587">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-588">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpNumConnections")</span><span class="sxs-lookup"><span data-stu-id="136dd-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-589">Maximale Anzahl von Verbindungen, die TCP gleichzeitig geöffnet haben kann.</span><span class="sxs-lookup"><span data-stu-id="136dd-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="136dd-590">Standard: 0xFFFFFE, Gültiger Bereich: 0 – 0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="136dd-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-591">**TcpUseRFC1122RolentPointer**</span><span class="sxs-lookup"><span data-stu-id="136dd-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-592">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-593">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-594">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ Tcpip-Parameter \\ \| TcpUseRFC1122PinentPointer")</span><span class="sxs-lookup"><span data-stu-id="136dd-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-595">True gibt an, dass TCP die RFC 1122-Spezifikation für dringende Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="136dd-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="136dd-596">False  (Standard) gibt an, dass TCP den Modus verwendet, der von BSD-abgeleiteten Systemen (California Software Design) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="136dd-597">Die beiden Mechanismen interpretieren den dringenden Zeiger unterschiedlich und sind nicht interoperabel.</span><span class="sxs-lookup"><span data-stu-id="136dd-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="136dd-598">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="136dd-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="136dd-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-600">Datentyp: **uint16**</span><span class="sxs-lookup"><span data-stu-id="136dd-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-601">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-602">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="136dd-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-603">Maximale TCP-Empfangsfenstergröße, die vom System angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="136dd-604">Das Empfangsfenster gibt die Anzahl der Bytes an, die ein Absender übertragen kann, ohne eine Bestätigung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="136dd-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="136dd-605">Im Allgemeinen verbessern größere Empfangsfenster die Leistung gegenüber Netzwerken mit hoher Verzögerung und hoher Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="136dd-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="136dd-606">Aus Effizienzgründen sollte das Empfangsfenster ein gerades Vielfaches der maximalen TCP-Segmentgröße (MSS) sein.</span><span class="sxs-lookup"><span data-stu-id="136dd-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="136dd-607">Standardeinstellung: Viermal so groß wie die maximale TCP-Datengröße oder sogar ein Vielfaches der TCP-Datengröße, aufgerundet auf das nächste Vielfache von 8192.</span><span class="sxs-lookup"><span data-stu-id="136dd-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="136dd-608">Ethernet-Netzwerke sind standardmäßig auf 8760 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="136dd-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="136dd-609">Gültiger Bereich: 0 bis 65535.</span><span class="sxs-lookup"><span data-stu-id="136dd-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="136dd-610">Windows Vista: Diese Eigenschaft greifen auf den Registrierungseintrag zu, der in der aktuellen Implementierung des `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` Betriebssystems nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="136dd-611">**WINSEnableLMHostsLookup**</span><span class="sxs-lookup"><span data-stu-id="136dd-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-612">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="136dd-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-613">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-614">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableLMHOSTS")</span><span class="sxs-lookup"><span data-stu-id="136dd-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-615">True **gibt an,** dass lokale Nachschlagedateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="136dd-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="136dd-616">Suchdateien enthalten eine Zuordnung von IP-Adressen zu Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="136dd-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="136dd-617">Wenn sie auf dem lokalen System vorhanden sind, finden Sie sie unter \\ %SystemRoot%-System32-Treiber \\ \\ usw.</span><span class="sxs-lookup"><span data-stu-id="136dd-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-618">**WINSHostLookupFile**</span><span class="sxs-lookup"><span data-stu-id="136dd-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-619">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="136dd-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-620">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-621">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers \\ \\ etc \\ \\ lmhosts")</span><span class="sxs-lookup"><span data-stu-id="136dd-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-622">Pfad zu einer WINS-Nachschlagedatei auf dem lokalen System.</span><span class="sxs-lookup"><span data-stu-id="136dd-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="136dd-623">Diese Datei enthält eine Zuordnung von IP-Adressen zu Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="136dd-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="136dd-624">Wenn die in dieser Eigenschaft angegebene Datei gefunden wird, wird sie in den Ordner %SystemRoot% \\ system32 drivers etc des \\ lokalen Systems \\ kopiert.</span><span class="sxs-lookup"><span data-stu-id="136dd-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="136dd-625">Nur gültig, wenn die **WINSEnableLMHostsLookup-Eigenschaft** **TRUE ist.**</span><span class="sxs-lookup"><span data-stu-id="136dd-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-626">**WINSPrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="136dd-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-627">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="136dd-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-628">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-629">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="136dd-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-630">IP-Adresse für den primären WINS-Server.</span><span class="sxs-lookup"><span data-stu-id="136dd-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-631">**WINSScopeID**</span><span class="sxs-lookup"><span data-stu-id="136dd-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-632">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-633">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-634">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ScopeID")</span><span class="sxs-lookup"><span data-stu-id="136dd-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-635">Der Wert wird am Ende des NetBIOS-Namens angefügt, der eine Gruppe von Computersystemen isoliert, die nur miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="136dd-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="136dd-636">Sie wird für alle NetBIOS-Transaktionen über TCP/IP-Kommunikation von diesem Computersystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="136dd-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="136dd-637">Computer, die mit identischen Bereichsbezeichnern konfiguriert sind, können mit diesem Computer kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="136dd-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="136dd-638">TCP/IP-Clients mit unterschiedlichen Bereichsbezeichnern ignorieren Pakete von Computern mit dieser Bereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="136dd-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="136dd-639">Nur gültig, wenn die [**EnableWINS-Methode**](enablewins-method-in-class-win32-networkadapterconfiguration.md) erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="136dd-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="136dd-640">**WINSSecondaryServer**</span><span class="sxs-lookup"><span data-stu-id="136dd-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="136dd-641">Datentyp: **String**</span><span class="sxs-lookup"><span data-stu-id="136dd-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="136dd-642">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="136dd-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="136dd-643">Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Geräteeingabe- \| und -ausgabefunktionen \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="136dd-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="136dd-644">IP-Adresse für den sekundären WINS-Server.</span><span class="sxs-lookup"><span data-stu-id="136dd-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="136dd-645">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="136dd-645">Remarks</span></span>

<span data-ttu-id="136dd-646">Die **Win32 \_ NetworkAdapterConfiguration-Klasse** wird von [**der \_ CIM-Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="136dd-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="136dd-647">Beispiele</span><span class="sxs-lookup"><span data-stu-id="136dd-647">Examples</span></span>

<span data-ttu-id="136dd-648">Im VBScript-Codebeispiel für [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) im TechNet-Katalog wird die **Win32 \_ NetworkAdapterConfiguration-Klasse** verwendet, um Netzwerkkonfigurationsinformationen von einer Reihe von Remotecomputern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="136dd-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="136dd-649">Das [PowerShell-Beispiel Get-ComputerInfo – Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) im TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ NetworkAdapterConfiguration,** um Informationen zu einem lokalen oder Remotesystem anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="136dd-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="136dd-650">Der folgende PowerShell-Code ruft die Konfigurationseinstellungen für den Microsoft ISTAP-Adapter ab.</span><span class="sxs-lookup"><span data-stu-id="136dd-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="136dd-651">Im folgenden \# C-Beispiel werden die Beschreibung und die Indexnummer aller Netzwerkadapter-Konfigurationsinstanzen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="136dd-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="136dd-652">Beachten Sie, dass in diesem C-Beispiel der \# [Namespace Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) verwendet wird, der im Allgemeinen effizienter skaliert wird als die WMI-Klassen des [System.Management-Namespace.](/dotnet/api/system.management)</span><span class="sxs-lookup"><span data-stu-id="136dd-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



<span data-ttu-id="136dd-653">Im folgenden \# C-Beispiel werden die Beschreibung und Indexnummer aller Netzwerkadapter-Konfigurationsinstanzen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="136dd-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="136dd-654">Beachten Sie, dass in \# diesem C-Beispiel der ursprüngliche [System.Management-Namespace](/dotnet/api/system.management) verwendet wird, der von [Microsoft.Management.Infrastructure ersetzt wurde.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="136dd-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



<span data-ttu-id="136dd-655">Im folgenden Beispiel werden Informationen aus der **Win32 \_ NetworkAdapterConfiguration-Klasse** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="136dd-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a><span data-ttu-id="136dd-656">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="136dd-656">Requirements</span></span>



| <span data-ttu-id="136dd-657">Anforderung</span><span class="sxs-lookup"><span data-stu-id="136dd-657">Requirement</span></span> | <span data-ttu-id="136dd-658">Wert</span><span class="sxs-lookup"><span data-stu-id="136dd-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="136dd-659">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="136dd-659">Minimum supported client</span></span><br/> | <span data-ttu-id="136dd-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="136dd-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="136dd-661">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="136dd-661">Minimum supported server</span></span><br/> | <span data-ttu-id="136dd-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="136dd-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="136dd-663">Namespace</span><span class="sxs-lookup"><span data-stu-id="136dd-663">Namespace</span></span><br/>                | <span data-ttu-id="136dd-664">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="136dd-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="136dd-665">MOF</span><span class="sxs-lookup"><span data-stu-id="136dd-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="136dd-666"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="136dd-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="136dd-667">DLL</span><span class="sxs-lookup"><span data-stu-id="136dd-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="136dd-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="136dd-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="136dd-669">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="136dd-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136dd-670">**\_CIM-Einstellung**</span><span class="sxs-lookup"><span data-stu-id="136dd-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="136dd-671">Hardwareklassen des Computersystems</span><span class="sxs-lookup"><span data-stu-id="136dd-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="136dd-672">WMI-Aufgaben: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="136dd-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="136dd-673">WMI-Aufgaben: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="136dd-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="136dd-674">IPv6- und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="136dd-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
