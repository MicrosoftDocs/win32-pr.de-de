---
description: Mit den folgenden Funktionen werden die Konfigurationseinstellungen für den TCP/IP-Transport auf dem lokalen Computer abgerufen und geändert.
ms.assetid: 5f562470-f3e8-4305-a015-3a84cd09a1eb
title: Funktionen des IP-Hilfsprogramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c8bff21f41c04bb5aecf505b251fbbe2f8bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760477"
---
# <a name="ip-helper-functions"></a><span data-ttu-id="1bc1b-103">IP-Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1bc1b-103">IP Helper functions</span></span>

<span data-ttu-id="1bc1b-104">Mit den folgenden Funktionen werden die Konfigurationseinstellungen für den TCP/IP-Transport auf dem lokalen Computer abgerufen und geändert.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-104">The following functions retrieve and modify configuration settings for the TCP/IP transport on the local computer.</span></span> <span data-ttu-id="1bc1b-105">Die folgende kategorische Auflistung kann helfen, zu bestimmen, welche Sammlung von Funktionen für eine bestimmte Aufgabe am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-105">The following categorical listing can help determine which collection of functions is best suited for a given task.</span></span>

-   [<span data-ttu-id="1bc1b-106">**Getnetworkconnectivityhint**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-106">**GetNetworkConnectivityHint**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhint)
-   [<span data-ttu-id="1bc1b-107">**Getnetworkconnectivityhintforinterface**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-107">**GetNetworkConnectivityHintForInterface**</span></span>](/windows/win32/api/netioapi/nf-netioapi-getnetworkconnectivityhintforinterface)
-   [<span data-ttu-id="1bc1b-108">**Notifynetworkconnectivityhintchange**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-108">**NotifyNetworkConnectivityHintChange**</span></span>](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)

## <a name="adapter-management"></a><span data-ttu-id="1bc1b-109">Adapter Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-109">Adapter management</span></span>

-   [<span data-ttu-id="1bc1b-110">**GetAdapterIndex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-110">**GetAdapterIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadapterindex)
-   [<span data-ttu-id="1bc1b-111">**Getadaptersadressen**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-111">**GetAdaptersAddresses**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)
-   [<span data-ttu-id="1bc1b-112">**Getadaptersinfo**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-112">**GetAdaptersInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)
-   [<span data-ttu-id="1bc1b-113">**Getperadapterinfo**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-113">**GetPerAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)
-   [<span data-ttu-id="1bc1b-114">**Getunidirectionaladapterinfo**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-114">**GetUniDirectionalAdapterInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo)

## <a name="address-resolution-protocol-arp-management"></a><span data-ttu-id="1bc1b-115">Address Resolution Protocol (ARP)-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-115">Address Resolution Protocol (ARP) management</span></span>

-   [<span data-ttu-id="1bc1b-116">**"Kreateipnetentry"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-116">**CreateIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipnetentry)
-   [<span data-ttu-id="1bc1b-117">**"Kreateproxyarpentry"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-117">**CreateProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createproxyarpentry)
-   [<span data-ttu-id="1bc1b-118">**Deleteipnetentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-118">**DeleteIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipnetentry)
-   [<span data-ttu-id="1bc1b-119">**Deleteproxyarpentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-119">**DeleteProxyArpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)
-   [<span data-ttu-id="1bc1b-120">**Flushipnettfähig**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-120">**FlushIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-flushipnettable)
-   [<span data-ttu-id="1bc1b-121">**Getipnettfähig**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-121">**GetIpNetTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipnettable)
-   [<span data-ttu-id="1bc1b-122">**Sendarp**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-122">**SendARP**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-sendarp)
-   [<span data-ttu-id="1bc1b-123">**"-Netentry"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-123">**SetIpNetEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipnetentry)

## <a name="interface-conversion"></a><span data-ttu-id="1bc1b-124">Schnittstellen Konvertierung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-124">Interface conversion</span></span>

-   [<span data-ttu-id="1bc1b-125">**Convertinterfacealiastoluid**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-125">**ConvertInterfaceAliasToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [<span data-ttu-id="1bc1b-126">**Convertinterfaceguidtoluid**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-126">**ConvertInterfaceGuidToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [<span data-ttu-id="1bc1b-127">**Convertinterfakeingedextoluid**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-127">**ConvertInterfaceIndexToLuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [<span data-ttu-id="1bc1b-128">**Convertinterfakeluidesalias**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-128">**ConvertInterfaceLuidToAlias**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoalias)
-   [<span data-ttu-id="1bc1b-129">**Convertinterfakeluidtoguid**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-129">**ConvertInterfaceLuidToGuid**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [<span data-ttu-id="1bc1b-130">**Convertinterfakeluidumindex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-130">**ConvertInterfaceLuidToIndex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [<span data-ttu-id="1bc1b-131">**Convertinterfakeluidtonamea**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-131">**ConvertInterfaceLuidToNameA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [<span data-ttu-id="1bc1b-132">**Convertinterfakeluidtonamew**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-132">**ConvertInterfaceLuidToNameW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [<span data-ttu-id="1bc1b-133">**Convertinterfakenametoluida**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-133">**ConvertInterfaceNameToLuidA**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [<span data-ttu-id="1bc1b-134">**Convertinterfakenametoluidw**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-134">**ConvertInterfaceNameToLuidW**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [<span data-ttu-id="1bc1b-135">**If \_ indextoname**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-135">**if\_indextoname**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_indextoname)
-   [<span data-ttu-id="1bc1b-136">**Wenn \_ nametoindex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-136">**if\_nametoindex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-if_nametoindex)

## <a name="interface-management"></a><span data-ttu-id="1bc1b-137">Schnittstellen Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-137">Interface management</span></span>

-   [<span data-ttu-id="1bc1b-138">**Getfriendlyifindex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-138">**GetFriendlyIfIndex**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)
-   [<span data-ttu-id="1bc1b-139">**Getif-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-139">**GetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getifentry)
-   [<span data-ttu-id="1bc1b-140">**GetIfEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-140">**GetIfEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2)
-   [<span data-ttu-id="1bc1b-141">**GetIfEntry2Ex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-141">**GetIfEntry2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifentry2ex)
-   [<span data-ttu-id="1bc1b-142">**Getifstacktable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-142">**GetIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getifstacktable)
-   [<span data-ttu-id="1bc1b-143">**Getiftbar**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-143">**GetIfTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getiftable)
-   [<span data-ttu-id="1bc1b-144">**GetIfTable2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-144">**GetIfTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2)
-   [<span data-ttu-id="1bc1b-145">**GetIfTable2Ex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-145">**GetIfTable2Ex**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getiftable2ex)
-   [<span data-ttu-id="1bc1b-146">**Getinterfacetten Info**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-146">**GetInterfaceInfo**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)
-   [<span data-ttu-id="1bc1b-147">**Getinvertedifstacktable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-147">**GetInvertedIfStackTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [<span data-ttu-id="1bc1b-148">**Getipinterfaceentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-148">**GetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [<span data-ttu-id="1bc1b-149">**Getipinterfaketable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-149">**GetIpInterfaceTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [<span data-ttu-id="1bc1b-150">**Getnumofintergesichter**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-150">**GetNumberOfInterfaces**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)
-   [<span data-ttu-id="1bc1b-151">**Initializeipinterfaceentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-151">**InitializeIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [<span data-ttu-id="1bc1b-152">**"Eintrag"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-152">**SetIfEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setifentry)
-   [<span data-ttu-id="1bc1b-153">**""-Interfaceentry "**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-153">**SetIpInterfaceEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipinterfaceentry)

## <a name="internet-protocol-ip-and-internet-control-message-protocol-icmp"></a><span data-ttu-id="1bc1b-154">Internetprotokoll (IP) und Internet Control Message Protocol (ICMP)</span><span class="sxs-lookup"><span data-stu-id="1bc1b-154">Internet Protocol (IP) and Internet Control Message Protocol (ICMP)</span></span>

-   [<span data-ttu-id="1bc1b-155">**GetIcmpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-155">**GetIcmpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)
-   [<span data-ttu-id="1bc1b-156">**GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-156">**GetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipstatistics)
-   [<span data-ttu-id="1bc1b-157">**Icmp6CreateFile**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-157">**Icmp6CreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6createfile)
-   [<span data-ttu-id="1bc1b-158">**Icmp6ParseReplies**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-158">**Icmp6ParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6parsereplies)
-   [<span data-ttu-id="1bc1b-159">**Icmp6SendEcho2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-159">**Icmp6SendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmp6sendecho2)
-   [<span data-ttu-id="1bc1b-160">**Icmpclosehandle**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-160">**IcmpCloseHandle**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpclosehandle)
-   [<span data-ttu-id="1bc1b-161">**Icmpkreatefile**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-161">**IcmpCreateFile**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpcreatefile)
-   [<span data-ttu-id="1bc1b-162">**Icmpparamesereplies**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-162">**IcmpParseReplies**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpparsereplies)
-   [<span data-ttu-id="1bc1b-163">**Icmpsendecho**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-163">**IcmpSendEcho**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho)
-   [<span data-ttu-id="1bc1b-164">**IcmpSendEcho2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-164">**IcmpSendEcho2**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2)
-   [<span data-ttu-id="1bc1b-165">**IcmpSendEcho2Ex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-165">**IcmpSendEcho2Ex**</span></span>](/windows/win32/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)
-   [<span data-ttu-id="1bc1b-166">**"Abgleichen"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-166">**SetIpTTL**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipttl)

## <a name="ip-address-management"></a><span data-ttu-id="1bc1b-167">IP-Adressverwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-167">IP address management</span></span>

-   [<span data-ttu-id="1bc1b-168">**Addipaddress**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-168">**AddIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-addipaddress)
-   [<span data-ttu-id="1bc1b-169">**"Kreateanycastipaddressentry"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-169">**CreateAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [<span data-ttu-id="1bc1b-170">**"Kreateunicastipaddressentry"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-170">**CreateUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [<span data-ttu-id="1bc1b-171">**Deleteipaddress**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-171">**DeleteIPAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipaddress)
-   [<span data-ttu-id="1bc1b-172">**Deleteanycastipaddressentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-172">**DeleteAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [<span data-ttu-id="1bc1b-173">**Deleteunicastipaddressentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-173">**DeleteUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [<span data-ttu-id="1bc1b-174">**Getanycastipaddressentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-174">**GetAnycastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [<span data-ttu-id="1bc1b-175">**Getanycastipadresssstable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-175">**GetAnycastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [<span data-ttu-id="1bc1b-176">**Getipaddrtable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-176">**GetIpAddrTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipaddrtable)
-   [<span data-ttu-id="1bc1b-177">**Getmulticastipaddressentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-177">**GetMulticastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [<span data-ttu-id="1bc1b-178">**Getmulticastipadresssstable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-178">**GetMulticastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [<span data-ttu-id="1bc1b-179">**Getunicastipaddressentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-179">**GetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [<span data-ttu-id="1bc1b-180">**Getunicastipadresssstable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-180">**GetUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [<span data-ttu-id="1bc1b-181">**Initializeunicastipaddressentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-181">**InitializeUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [<span data-ttu-id="1bc1b-182">**Ipreleaseaddress**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-182">**IpReleaseAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)
-   [<span data-ttu-id="1bc1b-183">**Iprenewaddress**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-183">**IpRenewAddress**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-iprenewaddress)
-   [<span data-ttu-id="1bc1b-184">**Notifystableunicastipadresssstable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-184">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [<span data-ttu-id="1bc1b-185">**"Setup"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-185">**SetUnicastIpAddressEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setunicastipaddressentry)

## <a name="ip-address-string-conversion"></a><span data-ttu-id="1bc1b-186">Konvertieren von IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="1bc1b-186">IP address string conversion</span></span>

-   [<span data-ttu-id="1bc1b-187">**RtlIpv4AddressToString**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-187">**RtlIpv4AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [<span data-ttu-id="1bc1b-188">**RtlIpv4AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-188">**RtlIpv4AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [<span data-ttu-id="1bc1b-189">**RtlIpv4StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-189">**RtlIpv4StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [<span data-ttu-id="1bc1b-190">**RtlIpv4StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-190">**RtlIpv4StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [<span data-ttu-id="1bc1b-191">**RtlIpv6AddressToString**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-191">**RtlIpv6AddressToString**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [<span data-ttu-id="1bc1b-192">**RtlIpv6AddressToStringEx**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-192">**RtlIpv6AddressToStringEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [<span data-ttu-id="1bc1b-193">**RtlIpv6StringToAddress**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-193">**RtlIpv6StringToAddress**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [<span data-ttu-id="1bc1b-194">**RtlIpv6StringToAddressEx**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-194">**RtlIpv6StringToAddressEx**</span></span>](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

## <a name="ip-neighbor-address-management"></a><span data-ttu-id="1bc1b-195">IP-Nachbar Adressverwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-195">IP neighbor address management</span></span>

-   [<span data-ttu-id="1bc1b-196">**CreateIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-196">**CreateIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipnetentry2)
-   [<span data-ttu-id="1bc1b-197">**DeleteIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-197">**DeleteIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [<span data-ttu-id="1bc1b-198">**FlushIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-198">**FlushIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushipnettable2)
-   [<span data-ttu-id="1bc1b-199">**GetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-199">**GetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnetentry2)
-   [<span data-ttu-id="1bc1b-200">**GetIpNetTable2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-200">**GetIpNetTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipnettable2)
-   [<span data-ttu-id="1bc1b-201">**ResolveIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-201">**ResolveIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [<span data-ttu-id="1bc1b-202">**Resolveneighbor**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-202">**ResolveNeighbor**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [<span data-ttu-id="1bc1b-203">**SetIpNetEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-203">**SetIpNetEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipnetentry2)

## <a name="ip-path-management"></a><span data-ttu-id="1bc1b-204">IP-Pfad Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-204">IP path management</span></span>

-   [<span data-ttu-id="1bc1b-205">**Flushippathtable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-205">**FlushIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-flushippathtable)
-   [<span data-ttu-id="1bc1b-206">**Getippathentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-206">**GetIpPathEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathentry)
-   [<span data-ttu-id="1bc1b-207">**Getippathtable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-207">**GetIpPathTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getippathtable)

## <a name="ip-route-management"></a><span data-ttu-id="1bc1b-208">IP-Routen Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-208">IP route management</span></span>

-   [<span data-ttu-id="1bc1b-209">**"Kreateipforwardentry"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-209">**CreateIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createipforwardentry)
-   [<span data-ttu-id="1bc1b-210">**CreateIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-210">**CreateIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [<span data-ttu-id="1bc1b-211">**Deleteipforwardentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-211">**DeleteIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)
-   [<span data-ttu-id="1bc1b-212">**DeleteIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-212">**DeleteIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [<span data-ttu-id="1bc1b-213">**Enablerouter**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-213">**EnableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-enablerouter)
-   [<span data-ttu-id="1bc1b-214">**Getbestinterface**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-214">**GetBestInterface**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterface)
-   [<span data-ttu-id="1bc1b-215">**Getbestinterfaceex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-215">**GetBestInterfaceEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestinterfaceex)
-   [<span data-ttu-id="1bc1b-216">**Getbestroute**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-216">**GetBestRoute**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getbestroute)
-   [<span data-ttu-id="1bc1b-217">**GetBestRoute2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-217">**GetBestRoute2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getbestroute2)
-   [<span data-ttu-id="1bc1b-218">**GetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-218">**GetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [<span data-ttu-id="1bc1b-219">**Getipforwardtable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-219">**GetIpForwardTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getipforwardtable)
-   [<span data-ttu-id="1bc1b-220">**GetIpForwardTable2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-220">**GetIpForwardTable2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [<span data-ttu-id="1bc1b-221">**Getrttandhopcount**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-221">**GetRTTAndHopCount**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getrttandhopcount)
-   [<span data-ttu-id="1bc1b-222">**Initializeipforwardentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-222">**InitializeIpForwardEntry**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [<span data-ttu-id="1bc1b-223">**"Gtipforwardentry"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-223">**SetIpForwardEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipforwardentry)
-   [<span data-ttu-id="1bc1b-224">**SetIpForwardEntry2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-224">**SetIpForwardEntry2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [<span data-ttu-id="1bc1b-225">**""-Statistik**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-225">**SetIpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatistics)
-   [<span data-ttu-id="1bc1b-226">**"* Tipstatisticsex"*\*</span><span class="sxs-lookup"><span data-stu-id="1bc1b-226">**SetIpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)
-   [<span data-ttu-id="1bc1b-227">**Unenablerouter**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-227">**UnenableRouter**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-unenablerouter)

## <a name="ip-table-memory-management"></a><span data-ttu-id="1bc1b-228">Speicherverwaltung für IP-Tabellen</span><span class="sxs-lookup"><span data-stu-id="1bc1b-228">IP table memory management</span></span>

-   [<span data-ttu-id="1bc1b-229">**Frei wählbar**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-229">**FreeMibTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-freemibtable)

## <a name="ip-utility"></a><span data-ttu-id="1bc1b-230">IP-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="1bc1b-230">IP utility</span></span>

-   [<span data-ttu-id="1bc1b-231">**ConvertIpv4MaskToLength**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-231">**ConvertIpv4MaskToLength**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [<span data-ttu-id="1bc1b-232">**ConvertLengthToIpv4Mask**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-232">**ConvertLengthToIpv4Mask**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [<span data-ttu-id="1bc1b-233">**"Kreatesortedadresssspairs"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-233">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [<span data-ttu-id="1bc1b-234">**Parameeworkstring**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-234">**ParseNetworkString**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

## <a name="network-configuration"></a><span data-ttu-id="1bc1b-235">Netzwerkkonfiguration</span><span class="sxs-lookup"><span data-stu-id="1bc1b-235">Network configuration</span></span>

-   [<span data-ttu-id="1bc1b-236">**Getnetworkparameams**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-236">**GetNetworkParams**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getnetworkparams)

## <a name="notification"></a><span data-ttu-id="1bc1b-237">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-237">Notification</span></span>

-   [<span data-ttu-id="1bc1b-238">**CancelMibChangeNotify2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-238">**CancelMibChangeNotify2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [<span data-ttu-id="1bc1b-239">**Notifyaddrchange**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-239">**NotifyAddrChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyaddrchange)
-   [<span data-ttu-id="1bc1b-240">**Notizyipinterfacechange**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-240">**NotifyIpInterfaceChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [<span data-ttu-id="1bc1b-241">**Notifyroutechange**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-241">**NotifyRouteChange**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-notifyroutechange)
-   [<span data-ttu-id="1bc1b-242">**NotifyRouteChange2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-242">**NotifyRouteChange2**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [<span data-ttu-id="1bc1b-243">**Notifyunicastipadresssschange**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-243">**NotifyUnicastIpAddressChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

## <a name="persistent-port-reservation"></a><span data-ttu-id="1bc1b-244">Persistente Port Reservierung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-244">Persistent port reservation</span></span>

-   [<span data-ttu-id="1bc1b-245">**"Kreatepersistenttcpportreservation"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-245">**CreatePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [<span data-ttu-id="1bc1b-246">**"Kreatepersistentudpportreservation"**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-246">**CreatePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [<span data-ttu-id="1bc1b-247">**Deletepersistenttcpportreservation**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-247">**DeletePersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [<span data-ttu-id="1bc1b-248">**Deletepersistentudpportreservation**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-248">**DeletePersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [<span data-ttu-id="1bc1b-249">**Lookuppersistenttcpportreservation**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-249">**LookupPersistentTcpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [<span data-ttu-id="1bc1b-250">**Lookuppersistentudpportreservation**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-250">**LookupPersistentUdpPortReservation**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="security-health"></a><span data-ttu-id="1bc1b-251">Sicherheitsintegrität</span><span class="sxs-lookup"><span data-stu-id="1bc1b-251">Security health</span></span>

-   <span data-ttu-id="1bc1b-252">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bc1b-252">[**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))</span></span>
-   <span data-ttu-id="1bc1b-253">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bc1b-253">[**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))</span></span>

<span data-ttu-id="1bc1b-254">Diese Funktionen werden nur auf Windows Server 2003 definiert.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-254">These functions are defined only on Windows Server 2003.</span></span>

> [!Note]  
> <span data-ttu-id="1bc1b-255">Diese Funktionen sind unter Windows Vista und Windows Server 2008 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-255">These functions are not available on Windows Vista, nor on Windows Server 2008.</span></span>

## <a name="teredo-ipv6-client-management"></a><span data-ttu-id="1bc1b-256">Teredo-IPv6-Client Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1bc1b-256">Teredo IPv6 client management</span></span>

-   [<span data-ttu-id="1bc1b-257">**Getteredoport**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-257">**GetTeredoPort**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="1bc1b-258">**Notifyteredoportchange**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-258">**NotifyTeredoPortChange**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="1bc1b-259">**Notifystableunicastipadresssstable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-259">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/win32/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

## <a name="transmission-control-protocol-tcp-and-user-datagram-protocol-udp"></a><span data-ttu-id="1bc1b-260">Transmission Control Protocol (TCP) und User Datagram Protocol (UDP)</span><span class="sxs-lookup"><span data-stu-id="1bc1b-260">Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)</span></span>

-   [<span data-ttu-id="1bc1b-261">**Getextende dtcptable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-261">**GetExtendedTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedtcptable)
-   [<span data-ttu-id="1bc1b-262">**Getextendedudptable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-262">**GetExtendedUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getextendedudptable)
-   [<span data-ttu-id="1bc1b-263">**GetOwnerModuleFromTcp6Entry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-263">**GetOwnerModuleFromTcp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [<span data-ttu-id="1bc1b-264">**Getownermodulefromtcpentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-264">**GetOwnerModuleFromTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [<span data-ttu-id="1bc1b-265">**GetOwnerModuleFromUdp6Entry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-265">**GetOwnerModuleFromUdp6Entry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)
-   [<span data-ttu-id="1bc1b-266">**Getownermodulefromudpentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-266">**GetOwnerModuleFromUdpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [<span data-ttu-id="1bc1b-267">**GetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-267">**GetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [<span data-ttu-id="1bc1b-268">**Getpertcpconnectionestats**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-268">**GetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [<span data-ttu-id="1bc1b-269">**GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-269">**GetTcpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)
-   [<span data-ttu-id="1bc1b-270">**Gettcpstatisticsex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-270">**GetTcpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex)
-   [<span data-ttu-id="1bc1b-271">**GetTcpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-271">**GetTcpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcpstatisticsex2)
-   [<span data-ttu-id="1bc1b-272">**GetTcp6Table**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-272">**GetTcp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [<span data-ttu-id="1bc1b-273">**GetTcp6Table2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-273">**GetTcp6Table2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [<span data-ttu-id="1bc1b-274">**GetTcpTable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-274">**GetTcpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable)
-   [<span data-ttu-id="1bc1b-275">**GetTcpTable2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-275">**GetTcpTable2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [<span data-ttu-id="1bc1b-276">**SetPerTcp6ConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-276">**SetPerTcp6ConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [<span data-ttu-id="1bc1b-277">**Setpertcpconnectionestats**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-277">**SetPerTcpConnectionEStats**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)
-   [<span data-ttu-id="1bc1b-278">**Settcpentry**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-278">**SetTcpEntry**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-settcpentry)
-   [<span data-ttu-id="1bc1b-279">**GetUdp6Table**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-279">**GetUdp6Table**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudp6table)
-   [<span data-ttu-id="1bc1b-280">**GetUdpStatistics**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-280">**GetUdpStatistics**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatistics)
-   [<span data-ttu-id="1bc1b-281">**Getudpstatisticsex**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-281">**GetUdpStatisticsEx**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex)
-   [<span data-ttu-id="1bc1b-282">**GetUdpStatisticsEx2**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-282">**GetUdpStatisticsEx2**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudpstatisticsex2)
-   [<span data-ttu-id="1bc1b-283">**Getudptable**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-283">**GetUdpTable**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-getudptable)

## <a name="deprecated-apis"></a><span data-ttu-id="1bc1b-284">Nicht mehr unterstützte APIs</span><span class="sxs-lookup"><span data-stu-id="1bc1b-284">Deprecated APIs</span></span>

> [!Note]  
> <span data-ttu-id="1bc1b-285">Diese Funktionen sind veraltet und werden von Microsoft nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bc1b-285">These functions are deprecated, and are not supported by Microsoft.</span></span>

-   [<span data-ttu-id="1bc1b-286">**"Zuweisung von" "" "".**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-286">**AllocateAndGetTcpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgettcpextablefromstack)
-   [<span data-ttu-id="1bc1b-287">**"Zuweisung von" "" "".**</span><span class="sxs-lookup"><span data-stu-id="1bc1b-287">**AllocateAndGetUdpExTableFromStack**</span></span>](/windows/win32/api/Iphlpapi/nf-iphlpapi-allocateandgetudpextablefromstack)
