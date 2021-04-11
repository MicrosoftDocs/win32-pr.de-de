---
description: Stellt die Attribute und Verhalten eines Netzwerkadapters dar. Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des vom Netzwerkadapter unabhängigen TCP/IP-Protokolls unterstützen.
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
ms.openlocfilehash: 2bccbe7fc44e75c2448d2eda800fe3c14cd13a9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127469"
---
# <a name="win32_networkadapterconfiguration-class"></a><span data-ttu-id="fd2bb-104">Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="fd2bb-104">Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="fd2bb-105">Die **Win32 \_ networkadapterconfiguration** - [WMI-Klasse](../wmisdk/retrieving-a-class.md)stellt die Attribute und Verhalten eines Netzwerkadapters dar.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-105">The **Win32\_NetworkAdapterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md)represents the attributes and behaviors of a network adapter.</span></span> <span data-ttu-id="fd2bb-106">Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des vom Netzwerkadapter unabhängigen TCP/IP-Protokolls unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-106">This class includes extra properties and methods that support the management of the TCP/IP protocol that are independent from the network adapter.</span></span>

<span data-ttu-id="fd2bb-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fd2bb-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2bb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd2bb-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="fd2bb-110">Member</span><span class="sxs-lookup"><span data-stu-id="fd2bb-110">Members</span></span>

<span data-ttu-id="fd2bb-111">Die **Win32 \_ networkadapterconfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fd2bb-111">The **Win32\_NetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="fd2bb-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="fd2bb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd2bb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd2bb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fd2bb-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="fd2bb-114">Methods</span></span>

<span data-ttu-id="fd2bb-115">Die **Win32 \_ networkadapterconfiguration** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-115">The **Win32\_NetworkAdapterConfiguration** class has these methods.</span></span>



| <span data-ttu-id="fd2bb-116">Methode</span><span class="sxs-lookup"><span data-stu-id="fd2bb-116">Method</span></span>                                                                                                                       | <span data-ttu-id="fd2bb-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd2bb-117">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd2bb-118">**DisableIPSec**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-118">**DisableIPSec**</span></span>](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="fd2bb-119">Deaktiviert IPSec auf diesem TCP/IP-fähigen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-119">Disables IPsec on this TCP/IP-enabled network adapter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="fd2bb-120">**EnableDHCP**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-120">**EnableDHCP**</span></span>](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="fd2bb-121">Aktiviert das Dynamic Host Configuration-Protokoll (DHCP) für den Dienst mit diesem Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-121">Enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span><br/>                                              |
| [<span data-ttu-id="fd2bb-122">**EnableDNS**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-122">**EnableDNS**</span></span>](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | <span data-ttu-id="fd2bb-123">Aktiviert die Domain Name System (DNS) für den Dienst auf diesem TCP/IP-gebundenen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-123">Enables the Domain Name System (DNS) for service on this TCP/IP-bound network adapter.</span></span><br/>                                                     |
| [<span data-ttu-id="fd2bb-124">**EnableIPFilterSec**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-124">**EnableIPFilterSec**</span></span>](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="fd2bb-125">Aktiviert IPSec Global über alle IP-gebundenen Netzwerkadapter hinweg.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-125">Enables IPsec globally across all IP-bound network adapters.</span></span><br/>                                                                               |
| [<span data-ttu-id="fd2bb-126">**EnableIPSec**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-126">**EnableIPSec**</span></span>](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="fd2bb-127">Aktiviert IPSec auf diesem speziellen TCP/IP-fähigen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-127">Enables IPsec on this specific TCP/IP-enabled network adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="fd2bb-128">**EnableStatic**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-128">**EnableStatic**</span></span>](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="fd2bb-129">Aktiviert die statische TCP/IP-Adressierung für den Zielnetzwerk Adapter.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-129">Enables static TCP/IP addressing for the target network adapter.</span></span><br/>                                                                           |
| [<span data-ttu-id="fd2bb-130">**EnableWINS**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-130">**EnableWINS**</span></span>](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | <span data-ttu-id="fd2bb-131">Aktiviert WINS-Einstellungen, die für TCP/IP spezifisch sind, aber unabhängig vom Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-131">Enables WINS settings specific to TCP/IP, but independent of the network adapter.</span></span><br/>                                                          |
| [<span data-ttu-id="fd2bb-132">**ReleaseDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-132">**ReleaseDHCPLease**</span></span>](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="fd2bb-133">Gibt die IP-Adresse frei, die an einen bestimmten DHCP-fähigen Netzwerkadapter gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-133">Releases the IP address bound to a specific DHCP-enabled network adapter.</span></span><br/>                                                                  |
| [<span data-ttu-id="fd2bb-134">**ReleaseDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-134">**ReleaseDHCPLeaseAll**</span></span>](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | <span data-ttu-id="fd2bb-135">Gibt die IP-Adressen frei, die an alle DHCP-fähigen Netzwerkadapter gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-135">Releases the IP addresses bound to all DHCP-enabled network adapters.</span></span><br/>                                                                      |
| [<span data-ttu-id="fd2bb-136">**RenewDHCPLease**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-136">**RenewDHCPLease**</span></span>](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | <span data-ttu-id="fd2bb-137">Erneuert die IP-Adresse auf bestimmten DHCP-fähigen Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-137">Renews the IP address on specific DHCP-enabled network adapters.</span></span><br/>                                                                           |
| [<span data-ttu-id="fd2bb-138">**RenewDHCPLeaseAll**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-138">**RenewDHCPLeaseAll**</span></span>](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | <span data-ttu-id="fd2bb-139">Erneuert die IP-Adressen auf allen DHCP-fähigen Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-139">Renews the IP addresses on all DHCP-enabled network adapters.</span></span><br/>                                                                              |
| [<span data-ttu-id="fd2bb-140">**"Starpalwayssourceroute"**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-140">**SetArpAlwaysSourceRoute**</span></span>](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="fd2bb-141">Legt die Übertragung von ARP-Abfragen durch TCP/IP fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-141">Sets the transmission of ARP queries by the TCP/IP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="fd2bb-142">**SetArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-142">**SetArpUseEtherSNAP**</span></span>](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | <span data-ttu-id="fd2bb-143">Ermöglicht Ethernet-Paketen die Verwendung der 802,3-Snap-Codierung.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-143">Enables Ethernet packets to use 802.3 SNAP encoding.</span></span><br/>                                                                                       |
| [<span data-ttu-id="fd2bb-144">**SetDatabasePath**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-144">**SetDatabasePath**</span></span>](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="fd2bb-145">Legt den Pfad zu den standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke und Protokolle) fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-145">Sets the path to the standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span><br/>                                           |
| [<span data-ttu-id="fd2bb-146">**Setdeadgwdetect**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-146">**SetDeadGWDetect**</span></span>](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="fd2bb-147">Ermöglicht die Erkennung von deadlockgateways.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-147">Enables dead gateway detection.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="fd2bb-148">**Setdefaulttos**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-148">**SetDefaultTOS**</span></span>](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="fd2bb-149">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-149">Obsolete.</span></span> <span data-ttu-id="fd2bb-150">Diese Methode legt den Standardtyp des Dienst Werts (TOS) im Header von ausgehenden IP-Paketen fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-150">This method sets the default Type of Service (TOS) value in the header of outgoing IP packets.</span></span><br/>                                   |
| [<span data-ttu-id="fd2bb-151">**Setdefaultttl**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-151">**SetDefaultTTL**</span></span>](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="fd2bb-152">Legt den Standardwert für die Gültigkeitsdauer (Time to Live, TTL) im Header von ausgehenden IP-Paketen fest</span><span class="sxs-lookup"><span data-stu-id="fd2bb-152">Sets the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span><br/>                                                            |
| [<span data-ttu-id="fd2bb-153">**SetDNSDomain**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-153">**SetDNSDomain**</span></span>](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="fd2bb-154">Legt die DNS-Domäne fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-154">Sets the DNS domain.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="fd2bb-155">**SetDNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-155">**SetDNSServerSearchOrder**</span></span>](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="fd2bb-156">Legt die Server Such Reihenfolge als Array von-Elementen fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-156">Sets the server search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fd2bb-157">**SetDNSSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-157">**SetDNSSuffixSearchOrder**</span></span>](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | <span data-ttu-id="fd2bb-158">Legt die Suffixsuchreihenfolge als Array von-Elementen fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-158">Sets the suffix search order as an array of elements.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fd2bb-159">**SetDynamicDNSRegistration**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-159">**SetDynamicDNSRegistration**</span></span>](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | <span data-ttu-id="fd2bb-160">Gibt die dynamische DNS-Registrierung von IP-Adressen für diesen IP-gebundenen Adapter an.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-160">Indicates dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span><br/>                                                              |
| [<span data-ttu-id="fd2bb-161">**SetForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-161">**SetForwardBufferMemory**</span></span>](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | <span data-ttu-id="fd2bb-162">Gibt an, wie viel Arbeitsspeicher-IP zugewiesen wird, um Paketdaten in der Routerpaketwarteschlange</span><span class="sxs-lookup"><span data-stu-id="fd2bb-162">Specifies how much memory IP allocates to store packet data in the router packet queue.</span></span><br/>                                                    |
| [<span data-ttu-id="fd2bb-163">**SetGateways**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-163">**SetGateways**</span></span>](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | <span data-ttu-id="fd2bb-164">Gibt eine Liste von Gateways für das Routing von Paketen an, die für ein anderes Subnetz bestimmt sind als das, mit dem dieser Adapter verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-164">Specifies a list of gateways for routing packets destined for a different subnet than the one this adapter is connected to.</span></span><br/>                |
| [<span data-ttu-id="fd2bb-165">**Setigmplevel**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-165">**SetIGMPLevel**</span></span>](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | <span data-ttu-id="fd2bb-166">Legt den Umfang fest, in dem das System IP-Multicasting unterstützt und am Internet Group Management-Protokoll teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-166">Sets the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span><br/>                   |
| [<span data-ttu-id="fd2bb-167">**"Abkconnectionmetric"**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-167">**SetIPConnectionMetric**</span></span>](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="fd2bb-168">Legt die Routing Metrik fest, die diesem IP-gebundenen Adapter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-168">Sets the routing metric associated with this IP-bound adapter.</span></span><br/>                                                                             |
| [<span data-ttu-id="fd2bb-169">**"S"**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-169">**SetIPUseZeroBroadcast**</span></span>](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | <span data-ttu-id="fd2bb-170">Legt die Verwendung von IP Zero Broadcast fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-170">Sets IP zero broadcast usage.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="fd2bb-171">**"Setxframetypetworkpair"**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-171">**SetIPXFrameTypeNetworkPairs**</span></span>](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | <span data-ttu-id="fd2bb-172">Legt die IPX-Netzwerk Nummer/-Frame Paare für diesen Netzwerkadapter fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-172">Sets Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span><br/>                                            |
| [<span data-ttu-id="fd2bb-173">**"Stipxvirtualnetworknumber"**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-173">**SetIPXVirtualNetworkNumber**</span></span>](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | <span data-ttu-id="fd2bb-174">Legt die virtuelle IPX-Netzwerk Nummer (Internetworking Packet Exchange) auf dem Zielcomputer System fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-174">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span><br/>                                       |
| [<span data-ttu-id="fd2bb-175">**Setkeepaliveingeterval**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-175">**SetKeepAliveInterval**</span></span>](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="fd2bb-176">Legt das Intervall zum Trennen von Keep-Alive-Neuübertragungen fest, bis eine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-176">Sets the interval separating Keep Alive Retransmissions until a response is received.</span></span><br/>                                                      |
| [<span data-ttu-id="fd2bb-177">**Setkeepalivetime**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-177">**SetKeepAliveTime**</span></span>](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="fd2bb-178">Legt fest, wie oft TCP überprüft, ob eine Verbindung im Leerlauf noch verfügbar ist, indem ein Keep-Alive-Paket gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-178">Sets how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span><br/>                           |
| [<span data-ttu-id="fd2bb-179">**"Ab-TU"**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-179">**SetMTU**</span></span>](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | <span data-ttu-id="fd2bb-180">Legt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-180">Sets the default Maximum Transmission Unit (MTU) for a network interface.</span></span><br/> <span data-ttu-id="fd2bb-181">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-181">This method is not supported.</span></span><br/>                         |
| [<span data-ttu-id="fd2bb-182">**Setnumforwardpakete**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-182">**SetNumForwardPackets**</span></span>](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="fd2bb-183">Legt die Anzahl der der Routerpaketwarteschlange zugeordneten IP-Paket Header fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-183">Sets the number of IP packet headers allocated for the router packet queue.</span></span><br/>                                                                |
| [<span data-ttu-id="fd2bb-184">**SetPMTUBHDetect**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-184">**SetPMTUBHDetect**</span></span>](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="fd2bb-185">Ermöglicht die Erkennung von Black-Hole-Routern.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-185">Enables detection of Black Hole routers.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="fd2bb-186">**SetPMTUDiscovery**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-186">**SetPMTUDiscovery**</span></span>](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="fd2bb-187">Ermöglicht die Ermittlung von maximalen Übertragungs Einheiten (MTU).</span><span class="sxs-lookup"><span data-stu-id="fd2bb-187">Enables Maximum Transmission Unit (MTU) discovery.</span></span><br/>                                                                                         |
| [<span data-ttu-id="fd2bb-188">**SetTcpipNetbios**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-188">**SetTcpipNetbios**</span></span>](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | <span data-ttu-id="fd2bb-189">Legt den Standard Vorgang von NetBIOS über TCP/IP fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-189">Sets the default operation of NetBIOS over TCP/IP.</span></span><br/>                                                                                         |
| [<span data-ttu-id="fd2bb-190">**Settcpmaxconnectretransmissions**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-190">**SetTcpMaxConnectRetransmissions**</span></span>](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | <span data-ttu-id="fd2bb-191">Legt fest, wie viele Versuche TCP eine Verbindungsanforderung erneut übermittelt, bevor Sie abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-191">Sets the number of attempts TCP will retransmit a connect request before aborting.</span></span><br/>                                                         |
| [<span data-ttu-id="fd2bb-192">**SetTcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-192">**SetTcpMaxDataRetransmissions**</span></span>](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | <span data-ttu-id="fd2bb-193">Legt fest, wie oft TCP ein einzelnes Daten Segment erneut überträgt, bevor die Verbindung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-193">Sets the number of times TCP will retransmit an individual data segment before aborting the connection.</span></span><br/>                                    |
| [<span data-ttu-id="fd2bb-194">**SetTcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-194">**SetTcpNumConnections**</span></span>](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | <span data-ttu-id="fd2bb-195">Legt die maximale Anzahl von Verbindungen fest, die von TCP gleichzeitig geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-195">Sets the maximum number of connections that TCP may have open simultaneously.</span></span><br/>                                                              |
| [<span data-ttu-id="fd2bb-196">**SetTcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-196">**SetTcpUseRFC1122UrgentPointer**</span></span>](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | <span data-ttu-id="fd2bb-197">Gibt an, ob TCP die RFC 1122-Spezifikation für dringende Daten oder den Modus verwendet, der von den von Berkeley (Berkeley Software Design) abgeleiteten Systemen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-197">Specifies whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span><br/> |
| [<span data-ttu-id="fd2bb-198">**Settcpwindowsize**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-198">**SetTcpWindowSize**</span></span>](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | <span data-ttu-id="fd2bb-199">Legt die maximale TCP-Empfangs Fenstergröße fest, die vom System bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-199">Sets the maximum TCP Receive Window size offered by the system.</span></span><br/>                                                                            |
| [<span data-ttu-id="fd2bb-200">**SetWINSServer**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-200">**SetWINSServer**</span></span>](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | <span data-ttu-id="fd2bb-201">Legt die primären und sekundären WINS-Server (Windows Internet Naming Service) auf diesem TCP/IP-gebundenen Netzwerkadapter fest.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-201">Sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="fd2bb-202">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd2bb-202">Properties</span></span>

<span data-ttu-id="fd2bb-203">Die **Win32 \_ networkadapterconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-203">The **Win32\_NetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd2bb-204">**ArpAlwaysSourceRoute**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-204">**ArpAlwaysSourceRoute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-205">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-207">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpAlwaysSourceRoute")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-208">**True** gibt an, dass TCP/IP-ARP-Abfragen (Address Resolution Protocol) mit aktiviertem Quell Routing in Tokenringnetzwerken überträgt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-208">If **TRUE**, TCP/IP transmits Address Resolution Protocol (ARP) queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="fd2bb-209">In der Standardeinstellung (false) werden ARP zuerst ohne Quell Routing abgefragt, und es wird dann erneut versucht, das Quell Routing zu aktivieren, wenn keine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-209">By default (FALSE), ARP first queries without source routing, and then retries with source routing enabled if no reply is received.</span></span> <span data-ttu-id="fd2bb-210">Das Quell Routing ermöglicht das Routing von Netzwerk Paketen über verschiedene Arten von Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-210">Source routing allows the routing of network packets across different types of networks.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-211">**ArpUseEtherSNAP**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-211">**ArpUseEtherSNAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-212">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-214">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ArpUseEtherSNAP")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-214">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ArpUseEtherSNAP")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-215">**True** gibt an, dass Ethernet-Pakete die IEEE 802,3-Snap-Codierung (Sub-Network Access Protocol) befolgen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-215">If **TRUE**, Ethernet packets follow the IEEE 802.3 Sub-Network Access Protocol (SNAP) encoding.</span></span> <span data-ttu-id="fd2bb-216">Wenn dieser Parameter auf 1 festgelegt wird, wird TCP/IP zum Übertragen von Ethernet-Paketen mithilfe der 802,3-Snap-Codierung</span><span class="sxs-lookup"><span data-stu-id="fd2bb-216">Setting this parameter to 1 forces TCP/IP to transmit Ethernet packets by using 802.3 SNAP encoding.</span></span> <span data-ttu-id="fd2bb-217">Standardmäßig (false) überträgt der Stapel Pakete im Dix Ethernet-Format.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-217">By default (FALSE), the stack transmits packets in DIX Ethernet format.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-221">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-221">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-222">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-222">Short textual description of the current object.</span></span>

<span data-ttu-id="fd2bb-223">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-223">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-224">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-224">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-227">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DatabasePath")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-227">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DatabasePath")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-228">Gültiger Windows-Dateipfad zu standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke und Protokolle).</span><span class="sxs-lookup"><span data-stu-id="fd2bb-228">Valid Windows file path to standard Internet database files (HOSTS, LMHOSTS, NETWORKS, and PROTOCOLS).</span></span> <span data-ttu-id="fd2bb-229">Der Dateipfad wird von der Windows Sockets-Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-229">The file path is used by the Windows Sockets interface.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-230">**DeadGWDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-230">**DeadGWDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-233">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableDeadGWDetect")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDeadGWDetect")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-234">**True** gibt an, dass die Erkennung von deadlockgateways erfolgt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-234">If **TRUE**, dead gateway detection occurs.</span></span> <span data-ttu-id="fd2bb-235">Wenn diese Funktion aktiviert ist, fordert das Transmission Control Protocol (TCP) das Internet Protokoll (IP) auf, um zu einem Sicherungs Gateway zu wechseln, wenn ein Segment mehrmals neu übermittelt wird, ohne dass eine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-235">With this feature enabled, Transmission Control Protocol (TCP) asks Internet Protocol (IP) to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-236">**DefaultIPGateway**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-236">**DefaultIPGateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-237">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-239">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| DefaultGateway")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|DefaultGateway")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-240">Array von IP-Adressen von Standard Gateways, die vom Computersystem verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-240">Array of IP addresses of default gateways that the computer system uses.</span></span>

<span data-ttu-id="fd2bb-241">Beispiel: "192.168.12.1 192.168.46.1"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-241">Example: "192.168.12.1 192.168.46.1"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-242">**DefaultTOS**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-242">**DefaultTOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-243">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-243">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-245">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTOS")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTOS")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-246">Der Standardwert für den Diensttyp (TOS), der im Header der ausgehenden IP-Pakete festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-246">Default Type Of Service (TOS) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="fd2bb-247">Request for Comments (RFC) 791 definiert die Werte.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-247">Request for Comments (RFC) 791 defines the values.</span></span> <span data-ttu-id="fd2bb-248">Standardwert: 0 (null), gültiger Bereich: 0-255.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-248">Default: 0 (zero), Valid Range: 0 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-249">**DefaultTTL**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-249">**DefaultTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-250">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-250">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-252">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTTL")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|DefaultTTL")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-253">Der Standardwert für die Gültigkeitsdauer (TTL), der im Header der ausgehenden IP-Pakete festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="fd2bb-253">Default Time To Live (TTL) value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="fd2bb-254">Die Gültigkeitsdauer gibt an, wie viele Router ein IP-Paket durchlaufen kann, um das Ziel zu erreichen, bevor es verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-254">The TTL specifies the number of routers an IP packet can pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="fd2bb-255">Jeder Router dekrementierungen um die TTL-Anzahl eines Pakets beim durchlaufen und verwirft die Pakete – wenn die Gültigkeitsdauer 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-255">Each router decrements by one the TTL count of a packet as it passes through and discards the packets—if the TTL is 0 (zero).</span></span> <span data-ttu-id="fd2bb-256">Standardwert: 32, gültiger Bereich: 1-255.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-256">Default: 32, Valid Range: 1 - 255.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-257">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-260">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-260">Textual description of the current object.</span></span>

<span data-ttu-id="fd2bb-261">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-261">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-262">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-262">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-263">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-263">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-265">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|EnableDHCP")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-266">**True** gibt an, dass der DHCP-Server (Dynamic Host Configuration Protocol) beim Herstellen einer Netzwerkverbindung dem Computersystem automatisch eine IP-Adresse zuweist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-266">If **TRUE**, the dynamic host configuration protocol (DHCP) server automatically assigns an IP address to the computer system when establishing a network connection.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-267">**Dhcpleaseabläuft**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-267">**DHCPLeaseExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-268">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-268">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-270">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| leaseterminatestime")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseTerminatesTime")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-271">Ablaufdatum und-Uhrzeit für eine geleast-IP-Adresse, die dem Computer vom DHCP-Server (Dynamic Host Configuration-Protokoll) zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-271">Expiration date and time for a leased IP address that was assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="fd2bb-272">Beispiel: 20521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="fd2bb-272">Example: 20521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-273">**Dhcpleasebezogen**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-273">**DHCPLeaseObtained**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-274">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-274">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-276">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| leaseobtainedtime")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|LeaseObtainedTime")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-277">Datum und Uhrzeit, zu der die Lease für die IP-Adresse abgerufen wurde, die dem Computer vom DHCP-Server (Dynamic Host Configuration Protocol) zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-277">Date and time the lease was obtained for the IP address assigned to the computer by the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="fd2bb-278">Beispiel: 19521201000230,000000000</span><span class="sxs-lookup"><span data-stu-id="fd2bb-278">Example: 19521201000230.000000000</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-279">**Dhcpserver ein**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-279">**DHCPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-282">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| DHCPServer")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-282">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\|DhcpServer")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-283">Die IP-Adresse des DHCP-Servers (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="fd2bb-283">IP address of the dynamic host configuration protocol (DHCP) server.</span></span>

<span data-ttu-id="fd2bb-284">Beispiel: "10.55.34.2"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-284">Example: "10.55.34.2"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-285">**DNSDomain**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-285">**DNSDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-288">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Domain")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-289">Organisationsname, gefolgt von einem Zeitraum und einer Erweiterung, die den Typ der Organisation angibt, z. b. "Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="fd2bb-289">Organization name followed by a period and an extension that indicates the type of organization, such as "microsoft.com".</span></span> <span data-ttu-id="fd2bb-290">Der Name kann eine beliebige Kombination der Buchstaben A bis Z, die Ziffern 0 bis 9 und der Bindestrich (-) sowie das Zeichen (.) sein, das als Trennzeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-290">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span>

<span data-ttu-id="fd2bb-291">Beispiel: "Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-291">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-292">**DNSDomainSuffixSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-292">**DNSDomainSuffixSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-293">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-295">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| SEARCHLIST")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|SearchList")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-296">Array von DNS-Domänen Suffixen, das während der Namensauflösung an das Ende der Hostnamen angehängt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-296">Array of DNS domain suffixes to be appended to the end of host names during name resolution.</span></span> <span data-ttu-id="fd2bb-297">Wenn Sie versuchen, einen vollständig qualifizierten Domänen Namen (FQDN) aus einem reinen Host Namen aufzulösen, fügt das System zuerst den lokalen Domänen Namen an.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-297">When attempting to resolve a fully qualified domain name (FQDN) from a host-only name, the system will first append the local domain name.</span></span> <span data-ttu-id="fd2bb-298">Wenn dies nicht erfolgreich ist, verwendet das System die Liste der Domänen Suffixe, um zusätzliche FQDNs in der aufgeführten Reihenfolge zu erstellen und die DNS-Server für jede zu Abfragen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-298">If this is not successful, the system will use the domain suffix list to create additional FQDNs in the order listed and query DNS servers for each.</span></span>

<span data-ttu-id="fd2bb-299">Beispiel: "Samples.Microsoft.com example.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-299">Example: "samples.microsoft.com example.microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-300">**DNSEnabledForWINSResolution**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-300">**DNSEnabledForWINSResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-301">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-303">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableDNS")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableDNS")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-304">**True** gibt an, dass die Domain Name System (DNS) für die Namensauflösung über die WINS-Auflösung (Windows Internet Naming Service) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-304">If **TRUE**, the Domain Name System (DNS) is enabled for name resolution over Windows Internet Naming Service (WINS) resolution.</span></span> <span data-ttu-id="fd2bb-305">Wenn der Name nicht mit DNS aufgelöst werden kann, wird die namens Anforderung zur Auflösung an WINS weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-305">If the name cannot be resolved using DNS, the name request is forwarded to WINS for resolution.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-306">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-306">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-309">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Hostname")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|Hostname")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-310">Der Hostname, der zum Identifizieren des lokalen Computers für die Authentifizierung durch einige Hilfsprogramme verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-310">Host name used to identify the local computer for authentication by some utilities.</span></span> <span data-ttu-id="fd2bb-311">Andere auf TCP/IP basierende Hilfsprogramme können diesen Wert verwenden, um den Namen des lokalen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-311">Other TCP/IP-based utilities can use this value to acquire the name of the local computer.</span></span> <span data-ttu-id="fd2bb-312">Hostnamen werden auf DNS-Servern in einer Tabelle gespeichert, die Namen zu IP-Adressen für die Verwendung durch DNS zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-312">Host names are stored on DNS servers in a table that maps names to IP addresses for use by DNS.</span></span> <span data-ttu-id="fd2bb-313">Der Name kann eine beliebige Kombination der Buchstaben A bis Z, die Ziffern 0 bis 9 und der Bindestrich (-) sowie das Zeichen (.) sein, das als Trennzeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-313">The name can be any combination of the letters A through Z, the numerals 0 through 9, and the hyphen (-), plus the period (.) character used as a separator.</span></span> <span data-ttu-id="fd2bb-314">Standardmäßig ist dieser Wert der Computername des Microsoft-Netzwerks, aber der Netzwerkadministrator kann einen anderen Hostnamen zuweisen, ohne dass sich dies auf den Computernamen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-314">By default, this value is the Microsoft networking computer name, but the network administrator can assign another host name without affecting the computer name.</span></span>

<span data-ttu-id="fd2bb-315">Beispiel: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-315">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-316">**DNSServerSearchOrder**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-316">**DNSServerSearchOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-317">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-319">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Nameserver")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NameServer")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-320">Array von Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-320">Array of server IP addresses to be used in querying for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-321">**Domaindnsregistrationaktiviert**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-321">**DomainDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-322">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-324">Wenn der Wert **true** ist, werden die IP-Adressen für diese Verbindung in DNS unter dem Domänen Namen dieser Verbindung registriert, zusätzlich zur Registrierung unter dem vollständigen DNS-Namen des Computers.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-324">If **TRUE**, the IP addresses for this connection are registered in DNS under the domain name of this connection in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="fd2bb-325">Der Domänen Name dieser Verbindung wird entweder mit der [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)()-Methode festgelegt oder von DSCP zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-325">The domain name of this connection is either set using the [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)() method or assigned by DSCP.</span></span> <span data-ttu-id="fd2bb-326">Der registrierte Name ist der Hostname des Computers, dem der Domänen Name angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-326">The registered name is the host name of the computer with the domain name appended.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-327">**ForwardBufferMemory**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-327">**ForwardBufferMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-328">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-330">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-331">Von IP zugewiesener Arbeitsspeicher zum Speichern von Paketdaten in der Routerpaketwarteschlange</span><span class="sxs-lookup"><span data-stu-id="fd2bb-331">Memory allocated by IP to store packet data in the router packet queue.</span></span> <span data-ttu-id="fd2bb-332">Wenn dieser Pufferbereich ausgefüllt ist, beginnt der Router, Pakete zufällig aus der Warteschlange zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-332">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span> <span data-ttu-id="fd2bb-333">Der Datenpuffer der Paket Warteschlange beträgt 256 Bytes, daher sollte der Wert dieses Parameters ein Vielfaches von 256 sein.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-333">Packet queue data buffers are 256 bytes in length, so the value of this parameter should be a multiple of 256.</span></span> <span data-ttu-id="fd2bb-334">Mehrere Puffer werden für größere Pakete miteinander verkettet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-334">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="fd2bb-335">Der IP-Header für ein Paket wird separat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-335">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="fd2bb-336">Dieser Parameter wird ignoriert, und es werden keine Puffer zugewiesen, wenn der IP-Router nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-336">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="fd2bb-337">Die Puffergröße kann zwischen der Netzwerk-MTU und einem Wert kleiner als 0xffffffff liegen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-337">The buffer size can range from the network MTU to a value smaller than 0xFFFFFFFF.</span></span> <span data-ttu-id="fd2bb-338">Standardwert: 74240 (50 1480-Byte-Pakete, gerundet auf ein Vielfaches von 256).</span><span class="sxs-lookup"><span data-stu-id="fd2bb-338">Default: 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-339">**Fulldnsregistrationaktivierte**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-339">**FullDNSRegistrationEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-340">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-342">**True** gibt an, dass die IP-Adressen für diese Verbindung in DNS unter dem vollständigen DNS-Namen des Computers registriert sind.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-342">If **TRUE**, the IP addresses for this connection are registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="fd2bb-343">Der vollständige DNS-Name des Computers wird auf der Registerkarte **Netzwerk Identifizierung** in der System Anwendung in der System Steuerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-343">The full DNS name of the computer is displayed on the **Network Identification** tab in the System application in Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-344">**GatewayCostMetric**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-344">**GatewayCostMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-345">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-347">Array von ganzzahligen Kosten Metrik Werten (im Bereich von 1 bis 9999), die zum Berechnen der schnellsten, zuverlässigsten oder am wenigsten ressourcenintensiven Routen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-347">Array of integer cost metric values (ranging from 1 to 9999) to be used in calculating the fastest, most reliable, or least resource-intensive routes.</span></span> <span data-ttu-id="fd2bb-348">Dieses Argument weist eine eins-zu-eins-Entsprechung mit der **DefaultIPGateway** -Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-348">This argument has a one-to-one correspondence with the **DefaultIPGateway** property.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-349">**IGMPLevel**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-349">**IGMPLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-350">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-352">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| IGMPLevel")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-352">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IGMPLevel")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-353">Der Umfang, in dem das System IP-Multicast unterstützt und am IGMP (Internet Group Management Protocol) teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-353">Extent to which the system supports IP multicast and participates in the Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="fd2bb-354">Auf Ebene 0 (null) stellt das System keine Multicast Unterstützung bereit.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-354">At level 0 (zero), the system provides no multicast support.</span></span> <span data-ttu-id="fd2bb-355">Auf Ebene 1 kann das System nur IP-Multicast Pakete senden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-355">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="fd2bb-356">Auf Ebene 2 kann das System IP-Multicast Pakete senden und für den Empfang von Multicast Paketen vollständig an IGMP teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-356">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="fd2bb-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Kein Multicast** (0)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-357"><span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="fd2bb-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP-Multicast** (1)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-358"><span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="fd2bb-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP-& IGMP-Multicast** (2)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-359"><span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP & IGMP multicast** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd2bb-360">IP-und IGMP-Multicast (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-360">IP and IGMP Multicast (default)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd2bb-361">**Index**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-361">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-362">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-364">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-364">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-365">Index Nummer der Windows-Netzwerkadapter Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-365">Index number of the Windows network adapter configuration.</span></span> <span data-ttu-id="fd2bb-366">Die Indexnummer wird verwendet, wenn mehr als eine Konfiguration verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-366">The index number is used when there is more than one configuration available.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-367">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-367">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-368">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-370">Indexwert, der eine lokale Netzwerkschnittstelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-370">Index value that uniquely identifies a local network interface.</span></span> <span data-ttu-id="fd2bb-371">Der Wert in dieser Eigenschaft ist identisch mit dem Wert in der **interfakeindex** -Eigenschaft in der Instanz von [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) , die die Netzwerkschnittstelle in der Routing Tabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-371">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-372">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-372">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-373">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-373">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-375">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip \| IPAddress")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip\|IPAddress")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-376">Array mit allen IP-Adressen, die dem aktuellen Netzwerkadapter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-376">Array of all of the IP addresses associated with the current network adapter.</span></span> <span data-ttu-id="fd2bb-377">Diese Eigenschaft kann entweder IPv6-Adressen oder IPv4-Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-377">This property can contain either IPv6 addresses or IPv4 addresses.</span></span> <span data-ttu-id="fd2bb-378">Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fd2bb-378">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="fd2bb-379">Beispiel für eine IPv6-Adresse: "2010:836b: 4179:: 836b: 4179"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-379">Example IPv6 address: "2010:836B:4179::836B:4179"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-380">**IPConnectionMetric**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-380">**IPConnectionMetric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-381">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-383">Die Kosten für die Verwendung der konfigurierten Routen für den IP-gebundenen Adapter und sind der gewichtete Wert für diese Routen in der IP-Routing Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-383">Cost of using the configured routes for the IP bound adapter and is the weighted value for those routes in the IP routing table.</span></span> <span data-ttu-id="fd2bb-384">Wenn mehrere Routen zu einem Ziel in der IP-Routing Tabelle vorhanden sind, wird die Route mit der niedrigsten Metrik verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-384">If there are multiple routes to a destination in the IP routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="fd2bb-385">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-385">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-386">**IPEnabled**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-386">**IPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-387">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-389">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\\\\Tcpip")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-390">**True** gibt an, dass TCP/IP auf diesem Netzwerkadapter gebunden und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-390">If **TRUE**, TCP/IP is bound and enabled on this network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-391">**Ipfiltersecurityaktiviert**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-391">**IPFilterSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-392">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-392">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-394">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ipfiltersecurityaktivierte")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-395">Bei " **true**" wird die IP-Port Sicherheit Global über alle IP-gebundenen Netzwerkadapter hinweg aktiviert, und die Sicherheitswerte, die den einzelnen Netzwerkadaptern zugeordnet sind, sind wirksam.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-395">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters and the security values associated with individual network adapters are in effect.</span></span> <span data-ttu-id="fd2bb-396">Diese Eigenschaft wird in Verbindung mit **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts** und **ipsecperentschärpprotokolls** verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-396">This property is used in conjunction with **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts**, and **IPSecPermitIPProtocols**.</span></span> <span data-ttu-id="fd2bb-397">Bei " **false**" wird die IP-Filter Sicherheit auf allen Netzwerkadaptern deaktiviert und ermöglicht, dass der gesamte Port-und Protokoll Datenverkehr ungefiltert erfolgt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-397">If **FALSE**, IP filter security is disabled across all network adapters and allows all port and protocol traffic to flow unfiltered.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-398">**Ipportsecurityaktivierte**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-398">**IPPortSecurityEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-399">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-399">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-401">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ networkadapterconfiguration \| ipfiltersecurityaktivierte")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-401">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration\|IPFilterSecurityEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-402">**True** gibt an, dass die IP-Port Sicherheit Global über alle IP-gebundenen Netzwerkadapter hinweg aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-402">If **TRUE**, IP port security is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="fd2bb-403">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-403">This property is obsolete.</span></span> <span data-ttu-id="fd2bb-404">Anstelle dieser Eigenschaft sollten Sie **ipfiltersecurityaktivierte** verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-404">In place of this property, you should use **IPFilterSecurityEnabled**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-405">**Ipsecperentschärpprotokolle**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-405">**IPSecPermitIPProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-406">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-406">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-408">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| rawipallowedprotokolls")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|RawIPAllowedProtocols")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-409">Array der Protokolle, die über die IP ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-409">Array of the protocols permitted to run over the IP.</span></span> <span data-ttu-id="fd2bb-410">Die Liste der Protokolle wird mithilfe der [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) -Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-410">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="fd2bb-411">Die Liste ist entweder leer oder enthält numerische Werte.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-411">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="fd2bb-412">Ein numerischer Wert von 0 (null) gibt an, dass für alle Protokolle die Zugriffsberechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-412">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="fd2bb-413">Eine leere Zeichenfolge gibt an, dass keine Protokolle ausgeführt werden dürfen, wenn **ipfiltersecurityaktivitrue** ist. </span><span class="sxs-lookup"><span data-stu-id="fd2bb-413">An empty string indicates that no protocols are permitted to run when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-414">**IPSecPermitTCPPorts**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-414">**IPSecPermitTCPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-415">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-417">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| tcpallowedports")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TCPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-418">Array der Ports, denen die Zugriffsberechtigung für TCP erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-418">Array of the ports that will be granted access permission for TCP.</span></span> <span data-ttu-id="fd2bb-419">Die Liste der Protokolle wird mithilfe der [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) -Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-419">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="fd2bb-420">Die Liste ist entweder leer oder enthält numerische Werte.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-420">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="fd2bb-421">Ein numerischer Wert von 0 (null) gibt an, dass für alle Ports die Zugriffsberechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-421">A numeric value of 0 (zero)indicates access permission is granted for all ports.</span></span> <span data-ttu-id="fd2bb-422">Eine leere Zeichenfolge gibt an, dass keinen Ports die Zugriffsberechtigung erteilt wird, wenn **ipfiltersecurityaktivitrue** ist. </span><span class="sxs-lookup"><span data-stu-id="fd2bb-422">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-423">**IPSecPermitUDPPorts**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-423">**IPSecPermitUDPPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-424">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-426">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| udpallowedports")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UDPAllowedPorts")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-427">Array der Ports, dem die UDP (User Datagram Protocol)-Zugriffsberechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-427">Array of the ports that will be granted User Datagram Protocol (UDP) access permission.</span></span> <span data-ttu-id="fd2bb-428">Die Liste der Protokolle wird mithilfe der [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) -Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-428">The list of protocols is defined using the [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span> <span data-ttu-id="fd2bb-429">Die Liste ist entweder leer oder enthält numerische Werte.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-429">The list will either be empty or contain numeric values.</span></span> <span data-ttu-id="fd2bb-430">Ein numerischer Wert von 0 (null) gibt an, dass für alle Ports die Zugriffsberechtigung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-430">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="fd2bb-431">Eine leere Zeichenfolge gibt an, dass keinen Ports die Zugriffsberechtigung erteilt wird, wenn **ipfiltersecurityaktivitrue** ist. </span><span class="sxs-lookup"><span data-stu-id="fd2bb-431">An empty string indicates that no ports are granted access permission when **IPFilterSecurityEnabled** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-432">**IPSubnet**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-432">**IPSubnet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-433">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-433">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-435">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| Subnetmask")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Parameters\|SubnetMask")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-436">Array aller Subnetzmasken, die dem aktuellen Netzwerkadapter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-436">Array of all of the subnet masks associated with the current network adapter.</span></span>

<span data-ttu-id="fd2bb-437">Beispiel: "255.255.0.0"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-437">Example: "255.255.0.0"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-438">**Ipuabzerobroadcast**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-438">**IPUseZeroBroadcast**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-439">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-441">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| UseZeroBroadcast")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|UseZeroBroadcast")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-442">**True** gibt an, dass IP-Nullen-Übertragungen verwendet werden (0.0.0.0), und das System verwendet Übertragungen (255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="fd2bb-442">If **TRUE**, IP zeros-broadcasts are used (0.0.0.0), and the system uses ones-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="fd2bb-443">Computer Systeme verwenden normalerweise solche-Sendungen, aber von BSD-Implementierungen abgeleitete, verwenden Nullen-Sendungen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-443">Computer systems generally use ones-broadcasts, but those derived from BSD implementations use zeros-broadcasts.</span></span> <span data-ttu-id="fd2bb-444">Systeme, die nicht die gleichen Übertragungen verwenden, werden nicht im selben Netzwerk zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-444">Systems that do not use that same broadcasts will not interoperate on the same network.</span></span> <span data-ttu-id="fd2bb-445">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-445">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-446">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-446">**IPXAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-447">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-449">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ Address")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-449">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Sockets Version 2\|[**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt)\|IPX\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-450">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-450">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-451">**Ipxaktiviert**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-451">**IPXEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-452">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-454">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-454">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-455">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-455">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-456">**IPXFrameType**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-456">**IPXFrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-457">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-457">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-459">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| PktType")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-459">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|PktType")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-460">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-460">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="fd2bb-461">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-461">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="fd2bb-462">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-462">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="fd2bb-463">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-463">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="fd2bb-464">**Ethernet-Snap** (3)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-464">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="fd2bb-465">**Auto** (255)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-465">**AUTO** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd2bb-466">**IPXMediaType**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-466">**IPXMediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-467">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-469">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| MediaType")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-469">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-470">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-470">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="fd2bb-471">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-471">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="fd2bb-472">**TokenRing** (2)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-472">**Token ring** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="fd2bb-473">" **F** " (3)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-473">**FDDI** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="fd2bb-474">**ARCNET** (8)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-474">**ARCNET** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd2bb-475">**IPXNetworkNumber**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-475">**IPXNetworkNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-476">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="fd2bb-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-478">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| NetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-478">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|NetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-479">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-479">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-480">**IPXVirtualNetNumber**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-480">**IPXVirtualNetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-483">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| VirtualNetworkNumber")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-483">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\nwlnkipx\\\\Parameters\|VirtualNetworkNumber")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-484">Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-484">The Internetwork Packet Exchange (IPX) technology is no longer supported and this property does not contain useful data.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-485">**KeepAliveInterval**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-485">**KeepAliveInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-486">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-488">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-489">Intervall zum Trennen von Keep-Alive-reübertragungen, bis eine Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-489">Interval separating Keep Alive Retransmissions until a response is received.</span></span> <span data-ttu-id="fd2bb-490">Nachdem eine Antwort empfangen wurde, wird die Verzögerung bis zur nächsten Keep-Alive-Übertragung wieder durch den Wert von **KeepAliveTime** gesteuert.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-490">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of **KeepAliveTime**.</span></span> <span data-ttu-id="fd2bb-491">Die Verbindung wird abgebrochen, nachdem die Anzahl der von **TcpMaxDataRetransmissions** angegebenen Neuübertragungen nicht mehr offengelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-491">The connection will be aborted after the number of retransmissions specified by **TcpMaxDataRetransmissions** have gone unanswered.</span></span> <span data-ttu-id="fd2bb-492">Standardwert: 1000, gültiger Bereich: 1-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-492">Default: 1000, Valid Range: 1 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-493">**KeepAliveTime**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-493">**KeepAliveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-494">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-494">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-496">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-497">Die **KeepAliveTime** -Eigenschaft gibt an, wie oft TCP versucht, zu überprüfen, ob eine Verbindung im Leerlauf noch intakt ist, indem ein Keep-Alive-Paket gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-497">The **KeepAliveTime** property indicates how often the TCP attempts to verify that an idle connection is still intact by sending a Keep Alive Packet.</span></span> <span data-ttu-id="fd2bb-498">Ein Remote System, das erreichbar ist, bestätigt die Keep-Alive-Übertragung.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-498">A remote system that is reachable will acknowledge the keep alive transmission.</span></span> <span data-ttu-id="fd2bb-499">Keep-Alive-Pakete werden standardmäßig nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-499">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="fd2bb-500">Diese Funktion kann in einer Verbindung von einer Anwendung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-500">This feature may be enabled in a connection by an application.</span></span> <span data-ttu-id="fd2bb-501">Standardwert: 7,2 Millionen (zwei Stunden).</span><span class="sxs-lookup"><span data-stu-id="fd2bb-501">Default: 7,200,000 (two hours).</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-502">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-502">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-503">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-505">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-505">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-506">Media Access Control (Mac)-Adresse des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-506">Media Access Control (MAC) address of the network adapter.</span></span> <span data-ttu-id="fd2bb-507">Eine Mac-Adresse wird vom Hersteller zugewiesen, um den Netzwerkadapter eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-507">A MAC address is assigned by the manufacturer to uniquely identify the network adapter.</span></span>

<span data-ttu-id="fd2bb-508">Beispiel: "00:80: C7:8F: 6C: 96"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-508">Example: "00:80:C7:8F:6C:96"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-509">**MTU**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-509">**MTU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-510">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-510">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-511">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-512">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-512">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-513">Überschreibt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-513">Overrides the default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="fd2bb-514">Die MTU ist die maximale Paketgröße (einschließlich der Transport Kopfzeile), die vom Transport über das zugrunde liegende Netzwerk übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-514">The MTU is the maximum packet size (including the transport header) that the transport will transmit over the underlying network.</span></span> <span data-ttu-id="fd2bb-515">Das IP-Datagramm kann mehrere Pakete umfassen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-515">The IP datagram can span multiple packets.</span></span> <span data-ttu-id="fd2bb-516">Der Bereich dieses Werts umfasst die minimale Paketgröße (68) für die MTU, die vom zugrunde liegenden Netzwerk unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-516">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-517">**Numforwardpakete**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-517">**NumForwardPackets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-518">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-520">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| numforwardpakete")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|NumForwardPackets")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-521">Anzahl der IP-Paket Header, die der Routerpaketwarteschlange zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="fd2bb-521">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="fd2bb-522">Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-522">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span> <span data-ttu-id="fd2bb-523">Dieser Wert muss mindestens so groß sein wie der **ForwardBufferMemory** -Wert, dividiert durch die maximale IP-Datengröße der mit dem Router verbundenen Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-523">This value should be at least as large as the **ForwardBufferMemory** value divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="fd2bb-524">Der Wert darf nicht größer sein als der **ForwardBufferMemory** -Wert dividiert durch 256, da für jedes Paket mindestens 256 Bytes an vorwärts Puffer Arbeitsspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-524">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are used for each packet.</span></span> <span data-ttu-id="fd2bb-525">Die optimale Anzahl von vorwärts Paketen für eine bestimmte **ForwardBufferMemory** -Größe hängt von der Art des Datenverkehrs im Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-525">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic on the network.</span></span> <span data-ttu-id="fd2bb-526">Sie liegt zwischen diesen beiden Werten.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-526">It will be somewhere between these two values.</span></span> <span data-ttu-id="fd2bb-527">Wenn der Router nicht aktiviert ist, wird dieser Parameter ignoriert, und es werden keine Header zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-527">If the router is not enabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="fd2bb-528">Standardwert: 50, gültiger Bereich: 1-0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-528">Default: 50, Valid Range: 1 - 0xFFFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-529">**PMTUBHDetectEnabled**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-529">**PMTUBHDetectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-530">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-530">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-531">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-532">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUBHDetect")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-532">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUBHDetect")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-533">**True** gibt an, dass die Erkennung von Black-Hole-Routern erfolgt, während TCP den Pfad der maximalen Übertragungseinheit ermittelt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-533">If **TRUE**, detection of black hole routers occurs while TCP discovers the path of the Maximum Transmission Unit.</span></span> <span data-ttu-id="fd2bb-534">Ein schwarzer Loch Router gibt keine nicht erreichbaren ICMP-Ziele zurück, wenn er ein IP-Datagramm mit dem Bitsatz "nicht Fragment" fragmentieren muss.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-534">A black hole router does not return ICMP Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="fd2bb-535">TCP ist davon abhängig, dass diese Nachrichten zum Durchführen der MTU-Ermittlung empfangen werden</span><span class="sxs-lookup"><span data-stu-id="fd2bb-535">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span> <span data-ttu-id="fd2bb-536">Wenn diese Funktion aktiviert ist, versucht TCP, Segmente ohne das Bit "nicht Fragment" zu senden, wenn mehrere Neuübertragungen eines Segments nicht bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-536">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="fd2bb-537">Wenn das Segment als Ergebnis bestätigt wird, wird der MSS verringert, und das Bit "nicht Fragment" wird in zukünftigen Paketen der Verbindung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-537">If the segment is acknowledged as a result, the MSS will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="fd2bb-538">Das Aktivieren der Black Hole-Erkennung erhöht die maximale Anzahl von erneuten Übertragungen, die für ein bestimmtes Segment ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-538">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span> <span data-ttu-id="fd2bb-539">Der Standardwert dieser Eigenschaft ist **false**.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-539">The default value of this property is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-540">**Pmtudiscoveryaktivierte**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-540">**PMTUDiscoveryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-541">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-542">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-543">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUDiscovery")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-543">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnablePMTUDiscovery")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-544">Wenn der Wert **true** ist, wird der Wert für die maximale Übertragungseinheit (MTU) über dem Pfad zu einem Remote Host erkannt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-544">If **TRUE**, the Maximum Transmission Unit (MTU) path is discovered over the path to a remote host.</span></span> <span data-ttu-id="fd2bb-545">Wenn Sie den MTU-Pfad ermitteln und TCP-Segmente auf diese Größe beschränken, kann TCP die Fragmentierung auf Routern entlang des Pfads eliminieren, der Netzwerke mit verschiedenen MTUs verbindet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-545">By discovering the MTU path and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="fd2bb-546">Die Fragmentierung beeinträchtigt den TCP-Durchsatz und die Überlastung des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-546">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="fd2bb-547">Wenn Sie diesen Parameter auf **false** festlegen, wird eine MTU von 576 Bytes für alle Verbindungen verwendet, die nicht zu Computern im lokalen Subnetz gehören.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-547">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet.</span></span> <span data-ttu-id="fd2bb-548">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="fd2bb-548">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-549">**Service Name**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-549">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-550">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-551">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-552">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Network Cards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-552">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-553">Der Dienst Name des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-553">Service name of the network adapter.</span></span> <span data-ttu-id="fd2bb-554">Dieser Name ist in der Regel kürzer als der vollständige Produktname.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-554">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="fd2bb-555">Beispiel: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="fd2bb-555">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-556">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-556">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-557">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-558">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-559">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-559">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-560">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-560">Identifier by which the current object is known.</span></span>

<span data-ttu-id="fd2bb-561">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-561">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-562">**TcpipNetbiosOptions**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-562">**TcpipNetbiosOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-563">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-564">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-565">Bitmap der möglichen Einstellungen im Zusammenhang mit NetBIOS über TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-565">Bitmap of the possible settings related to NetBIOS over TCP/IP.</span></span> <span data-ttu-id="fd2bb-566">Werte werden in der folgenden Liste angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-566">Values are identified in the following list.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="fd2bb-567">**Enablenetbiosviadhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-567">**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="fd2bb-568">**Enablenetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-568">**EnableNetbios** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="fd2bb-569">**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-569">**DisableNetbios** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd2bb-570">**Tcpmaxconnectretransmissions**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-570">**TcpMaxConnectRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-571">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-571">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-572">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-573">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| tcpmaxconnectretransmissions")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-573">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxConnectRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-574">Gibt an, wie oft TCP versucht, eine Verbindungsanforderung erneut zu übertragen, bevor die Verbindung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-574">Number of times TCP attempts to retransmit a Connect Request before terminating the connection.</span></span> <span data-ttu-id="fd2bb-575">Der anfängliche Neuübertragungs Timeout beträgt 3 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-575">The initial retransmission timeout is 3 seconds.</span></span> <span data-ttu-id="fd2bb-576">Das Timeout für die erneute Übertragung verdoppelt sich für jeden Versuch.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-576">The retransmission timeout doubles for each attempt.</span></span> <span data-ttu-id="fd2bb-577">Standardwert: 3, gültiger Bereich: 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-577">Default: 3, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-578">**TcpMaxDataRetransmissions**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-578">**TcpMaxDataRetransmissions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-579">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-579">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-580">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-581">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpMaxDataRetransmissions")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-582">Gibt an, wie oft TCP ein einzelnes Daten Segment (nonconnect-Segment) erneut überträgt, bevor die Verbindung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-582">Number of times TCP retransmits an individual data segment (nonconnect segment) before terminating the connection.</span></span> <span data-ttu-id="fd2bb-583">Das Timeout für die erneute Übertragung verdoppelt sich mit jeder nachfolgenden erneuten Übertragung für eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-583">The retransmission timeout doubles with each successive retransmission on a connection.</span></span> <span data-ttu-id="fd2bb-584">Standardwert: 5, gültiger Bereich: 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-584">Default: 5, Valid Range: 0 - 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-585">**TcpNumConnections**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-585">**TcpNumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-586">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-586">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-587">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-587">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-588">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpNumConnections")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-588">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpNumConnections")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-589">Maximale Anzahl von Verbindungen, die von TCP gleichzeitig geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-589">Maximum number of connections that TCP can have open simultaneously.</span></span> <span data-ttu-id="fd2bb-590">Standard: 0xfffffe, gültiger Bereich: 0-0xfffffe.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-590">Default: 0xFFFFFE, Valid Range: 0 - 0xFFFFFE.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-591">**TcpUseRFC1122UrgentPointer**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-591">**TcpUseRFC1122UrgentPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-592">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-592">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-593">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-594">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-594">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpUseRFC1122UrgentPointer")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-595">**True** gibt an, dass TCP die Spezifikation RFC 1122 für dringende Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-595">If **TRUE**, TCP uses the RFC 1122 specification for urgent data.</span></span> <span data-ttu-id="fd2bb-596">Der Standardwert **false** gibt an, dass TCP den von den von Berkeley Software Design (BSD) abgeleiteten Systemen verwendeten Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-596">If **FALSE** (default), TCP uses the mode used by Berkeley Software Design (BSD) derived systems.</span></span> <span data-ttu-id="fd2bb-597">Die beiden Mechanismen interpretieren den dringenden Zeiger anders und sind nicht interoperabel.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-597">The two mechanisms interpret the urgent pointer differently and are not interoperable.</span></span> <span data-ttu-id="fd2bb-598">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-598">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-599">**TcpWindowSize**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-599">**TcpWindowSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-600">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-600">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-601">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-602">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-602">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-603">Maximale TCP-Empfangs Fenstergröße, die vom System bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-603">Maximum TCP Receive Window size offered by the system.</span></span> <span data-ttu-id="fd2bb-604">Das Empfangs Fenster gibt die Anzahl der Bytes an, die ein Absender übertragen kann, ohne eine Bestätigung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-604">The Receive Window specifies the number of bytes a sender may transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="fd2bb-605">Im allgemeinen verbessern größere empfangende Fenster die Leistung bei Netzwerken mit hoher Verzögerung und hoher Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-605">In general, larger receiving windows will improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="fd2bb-606">Aus Effizienzgründen sollte das empfangende Fenster ein gleich Vielfaches der maximalen TCP-Segment Größe (MSS) sein.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-606">For efficiency, the receiving window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span> <span data-ttu-id="fd2bb-607">Standardwert: viermal die maximale TCP-Datengröße oder ein gleichmäßiges Vielfaches der TCP-Datengröße, das auf das nächste Vielfache von 8192 aufgerundet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-607">Default: Four times the maximum TCP data size or an even multiple of TCP data size rounded up to the nearest multiple of 8192.</span></span> <span data-ttu-id="fd2bb-608">Ethernet-Netzwerke werden standardmäßig auf 8760 eingestellt.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-608">Ethernet networks default to 8760.</span></span> <span data-ttu-id="fd2bb-609">Gültiger Bereich: 0-65535.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-609">Valid range: 0 - 65535.</span></span>

> [!Note]  
> <span data-ttu-id="fd2bb-610">Windows Vista: Diese Eigenschaft greift `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` auf den Registrierungs Eintrag zu, der nicht in der aktuellen Implementierung des Betriebssystems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-610">Windows Vista: This property accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

</dd> <dt>

<span data-ttu-id="fd2bb-611">**WINSEnableLMHostsLookup**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-611">**WINSEnableLMHostsLookup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-612">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-612">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-613">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-613">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-614">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| enablelmhosts")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-614">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|EnableLMHOSTS")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-615">**True** gibt an, dass lokale Suchdateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-615">If **TRUE**, local lookup files are used.</span></span> <span data-ttu-id="fd2bb-616">Suchdateien enthalten eine Zuordnung von IP-Adressen zu Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-616">Lookup files will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="fd2bb-617">Wenn Sie auf dem lokalen System vorhanden sind, werden Sie in% SystemRoot% \\ system32 \\ Drivers \\ usw. gefunden.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-617">If they exist on the local system, they will be found in %SystemRoot%\\system32\\drivers\\etc.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-618">**WINSHostLookupFile**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-618">**WINSHostLookupFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-619">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-620">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-621">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ Drivers \\ \\ usw \\ \\ Lmhosts")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-621">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)\|\\\\drivers\\\\etc\\\\lmhosts")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-622">Pfad zu einer WINS-Suche-Datei auf dem lokalen System.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-622">Path to a WINS lookup file on the local system.</span></span> <span data-ttu-id="fd2bb-623">Diese Datei enthält eine Zuordnung von IP-Adressen zu Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-623">This file will contain a map of IP addresses to host names.</span></span> <span data-ttu-id="fd2bb-624">Wenn die in dieser Eigenschaft angegebene Datei gefunden wird, wird Sie in den Ordner% systemroot% \\ system32 \\ Drivers \\ usw. des lokalen Systems kopiert.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-624">If the file specified in this property is found, it will be copied to the %SystemRoot%\\system32\\drivers\\etc folder of the local system.</span></span> <span data-ttu-id="fd2bb-625">Nur gültig, wenn die **WINSEnableLMHostsLookup** -Eigenschaft auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-625">Valid only if the **WINSEnableLMHostsLookup** property is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-626">**WINSPrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-626">**WINSPrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-627">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-627">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-628">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-629">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-629">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-630">Die IP-Adresse für den primären WINS-Server.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-630">IP address for the primary WINS server.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-631">**WINSScopeID**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-631">**WINSScopeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-632">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-632">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-633">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-634">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ScopeId")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-634">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\Tcpip\\\\Parameters\|ScopeID")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-635">Der am Ende des NetBIOS-Namens angefügte Wert, der eine Gruppe von Computersystemen isoliert, die miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-635">Value appended to the end of the NetBIOS name that isolates a group of computer systems communicating with only each other.</span></span> <span data-ttu-id="fd2bb-636">Sie wird für alle NetBIOS-Transaktionen über die TCP/IP-Kommunikation von diesem Computersystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-636">It is used for all NetBIOS transactions over TCP/IP communications from that computer system.</span></span> <span data-ttu-id="fd2bb-637">Computer, die mit identischen Bereichs Bezeichners konfiguriert sind, können mit diesem Computer kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-637">Computers configured with identical scope identifiers are able to communicate with this computer.</span></span> <span data-ttu-id="fd2bb-638">TCP/IP-Clients mit unterschiedlichen Bereichs Bezeichnern ignorieren Pakete von Computern mit diesem Bereichs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-638">TCP/IP clients with different scope identifiers disregard packets from computers with this scope identifier.</span></span> <span data-ttu-id="fd2bb-639">Nur gültig, wenn die [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) -Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-639">Valid only when the [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) method executes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="fd2bb-640">**WINSSecondaryServer**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-640">**WINSSecondaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd2bb-641">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-642">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd2bb-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd2bb-643">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="fd2bb-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="fd2bb-644">Die IP-Adresse für den sekundären WINS-Server.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-644">IP address for the secondary WINS server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd2bb-645">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd2bb-645">Remarks</span></span>

<span data-ttu-id="fd2bb-646">Die **Win32- \_ networkadapterconfiguration** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-646">The **Win32\_NetworkAdapterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fd2bb-647">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd2bb-647">Examples</span></span>

<span data-ttu-id="fd2bb-648">Das Codebeispiel für den [WMI-Informations](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) Abruf im VBScript-Code in der TechNet Gallery verwendet die **Win32 \_ networkadapterconfiguration** -Klasse, um Informationen zur Netzwerkkonfiguration von einer Reihe von Remote Computern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-648">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_NetworkAdapterConfiguration** class to retrieve network configuration information from a number of remote computers.</span></span>

<span data-ttu-id="fd2bb-649">Das PowerShell [-Beispiel Get-ComputerInfo-Query Computer Info from Local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ networkadapterconfiguration**, um Informationen über ein lokales oder Remote System anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-649">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapterConfiguration**, to display information about a local or remote system.</span></span>

<span data-ttu-id="fd2bb-650">Der folgende PowerShell-Code Ruft die Konfigurationseinstellungen für den Microsoft istap-Adapter ab.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-650">The following PowerShell code retrieves the configuration settings for the Microsoft ISTAP Adapter.</span></span>


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



<span data-ttu-id="fd2bb-651">Das folgende C \# -Beispiel ruft die Beschreibung und die Indexnummer aller Netzwerkadapter-Konfigurations Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-651">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="fd2bb-652">Beachten Sie, dass in diesem C- \# Beispiel der [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace verwendet wird, der im Allgemeinen effizienter skaliert als die WMI-Klassen des [System. Management](/dotnet/api/system.management) -Namespace.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-652">Note that this C\# sample uses the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, which generally scales more efficiently than the [System.Management](/dotnet/api/system.management) namespace WMI classes.</span></span>


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



<span data-ttu-id="fd2bb-653">Das folgende C \# -Beispiel ruft die Beschreibung und die Indexnummer aller Netzwerkadapter-Konfigurations Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-653">The following C\# sample retrieves the description and index number of all network adapter configuration instances.</span></span> <span data-ttu-id="fd2bb-654">Beachten Sie, dass in diesem C- \# Beispiel der ursprüngliche [System. Management](/dotnet/api/system.management) -Namespace verwendet wird, der von [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-654">Note that this C\# sample uses the original [System.Management](/dotnet/api/system.management) namespace, which has been superceded by [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)).</span></span>


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



<span data-ttu-id="fd2bb-655">Im folgenden Beispiel werden Informationen aus der **Win32 \_ networkadapterconfiguration** -Klasse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-655">The following example retrieves information from the **Win32\_NetworkAdapterConfiguration** class.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fd2bb-656">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd2bb-656">Requirements</span></span>



| <span data-ttu-id="fd2bb-657">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd2bb-657">Requirement</span></span> | <span data-ttu-id="fd2bb-658">Wert</span><span class="sxs-lookup"><span data-stu-id="fd2bb-658">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2bb-659">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-659">Minimum supported client</span></span><br/> | <span data-ttu-id="fd2bb-660">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd2bb-660">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd2bb-661">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-661">Minimum supported server</span></span><br/> | <span data-ttu-id="fd2bb-662">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd2bb-662">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd2bb-663">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd2bb-663">Namespace</span></span><br/>                | <span data-ttu-id="fd2bb-664">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fd2bb-664">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd2bb-665">MOF</span><span class="sxs-lookup"><span data-stu-id="fd2bb-665">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd2bb-666"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fd2bb-666"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd2bb-667">DLL</span><span class="sxs-lookup"><span data-stu-id="fd2bb-667">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd2bb-668"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd2bb-668"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd2bb-669">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd2bb-669">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2bb-670">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="fd2bb-670">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="fd2bb-671">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="fd2bb-671">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="fd2bb-672">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="fd2bb-672">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="fd2bb-673">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="fd2bb-673">WMI Tasks: Accounts and Domains</span></span>](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[<span data-ttu-id="fd2bb-674">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="fd2bb-674">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
