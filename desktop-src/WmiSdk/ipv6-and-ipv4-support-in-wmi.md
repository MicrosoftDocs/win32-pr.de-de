---
description: WMI-IP-Routen Anbieter und Netzwerk Klassen stellen Daten für IPv4-Adressen bereit. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: IPv6-und IPv4-Unterstützung in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363246"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a><span data-ttu-id="707c5-104">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="707c5-104">IPv6 and IPv4 Support in WMI</span></span>

<span data-ttu-id="707c5-105">WMI [-IP-Routen Anbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) und Netzwerk Klassen stellen Daten für IPv4-Adressen bereit.</span><span class="sxs-lookup"><span data-stu-id="707c5-105">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="707c5-106">Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.</span><span class="sxs-lookup"><span data-stu-id="707c5-106">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span>

## <a name="wmi-ip-data"></a><span data-ttu-id="707c5-107">WMI-IP-Daten</span><span class="sxs-lookup"><span data-stu-id="707c5-107">WMI IP Data</span></span>

<span data-ttu-id="707c5-108">Die folgenden Klassen stellen nur IPv4-Daten bereit:</span><span class="sxs-lookup"><span data-stu-id="707c5-108">The following classes supply only IPv4 data:</span></span>

-   [<span data-ttu-id="707c5-109">**Win32- \_ IP4RouteTable**</span><span class="sxs-lookup"><span data-stu-id="707c5-109">**Win32\_IP4RouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [<span data-ttu-id="707c5-110">**Win32- \_ IP4PersistedRouteTable**</span><span class="sxs-lookup"><span data-stu-id="707c5-110">**Win32\_IP4PersistedRouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [<span data-ttu-id="707c5-111">**Win32- \_ IP4RouteTableEvent**</span><span class="sxs-lookup"><span data-stu-id="707c5-111">**Win32\_IP4RouteTableEvent**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [<span data-ttu-id="707c5-112">**Win32- \_ activeroute**</span><span class="sxs-lookup"><span data-stu-id="707c5-112">**Win32\_ActiveRoute**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [<span data-ttu-id="707c5-113">**Win32- \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="707c5-113">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)

<span data-ttu-id="707c5-114">Die folgenden Klassen stellen Daten sowohl für IPv4 als auch für IPv6 bereit.</span><span class="sxs-lookup"><span data-stu-id="707c5-114">The following classes supply data for both IPv4 and IPv6.</span></span>

-   [<span data-ttu-id="707c5-115">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="707c5-115">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    <span data-ttu-id="707c5-116">Die **ipaddess** -Eigenschaft enthält die IPv6-Adresse des Computers in einem IPv6-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="707c5-116">The **IpAddess** property contains the IPv6 address of the computer in an IPv6 network.</span></span>

-   [<span data-ttu-id="707c5-117">**Win32 \_ Pingstatus**</span><span class="sxs-lookup"><span data-stu-id="707c5-117">**Win32\_PingStatus**</span></span>](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    <span data-ttu-id="707c5-118">[**Win32 \_ Pingstatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) kann Daten für IPv4-oder IPv6-Adressen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="707c5-118">[**Win32\_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) can return data for either IPv4 or IPv6 addresses.</span></span>

## <a name="ipv4-and-ipv6-connections-to-wmi"></a><span data-ttu-id="707c5-119">IPv4-und IPv6-Verbindungen mit WMI</span><span class="sxs-lookup"><span data-stu-id="707c5-119">IPv4 and IPv6 Connections to WMI</span></span>

<span data-ttu-id="707c5-120">Beim Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer muss auf dem Bereitstellungs Zielcomputer die gleiche IP-Software wie der Computer ausgeführt werden, der die Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="707c5-120">When connecting to a WMI namespace on a remote computer, the target computer must be running the same IP software as the connecting computer.</span></span> <span data-ttu-id="707c5-121">Beispielsweise kann ein Computer, auf dem IPv4 ausgeführt wird, keine Verbindung mit einem Computer herstellen, auf dem IPv6 ausgeführt wird. Dies gilt auch, wenn versucht wird, einen Computernamen im Aufruf von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**Swap-Locator. ConnectServer**](swbemlocator-connectserver.md)oder mithilfe der `winmgmts` monikerverbindung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="707c5-121">For example, a computer running IPv4 cannot connect to a computer running IPv6, even if the connection is attempted by using a computer name in the call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), or by using the `winmgmts` moniker connection.</span></span> <span data-ttu-id="707c5-122">Das Gegenteil gilt auch: ein Computer, auf dem nur IPv6 ausgeführt wird, kann keine Verbindung mit einem Computer herstellen, der nur IPv4 ausgeführt</span><span class="sxs-lookup"><span data-stu-id="707c5-122">The reverse is also true: a computer running only IPv6 cannot connect to a computer running only IPv4.</span></span>

<span data-ttu-id="707c5-123">Wenn auf dem Bereitstellungs Zielcomputer sowohl IPv4 als auch IPv6 ausgeführt wird, kann eine Verbindung von einem Computer hergestellt werden, auf dem entweder eine IP-Software ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="707c5-123">If the target computer is running both IPv4 and IPv6, then a connection can be made from a computer running either IP software.</span></span> <span data-ttu-id="707c5-124">Ein Computername oder eine IP-Adresse im IPv4-oder IPv6-Format kann in der Verbindung mit einem WMI-Namespace bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="707c5-124">A computer name or an IP address in either IPv4 or IPv6 format can be supplied in the connection to a WMI namespace.</span></span>

<span data-ttu-id="707c5-125">Ein Computer, auf dem sowohl IPv4 als auch IPv6 ausgeführt wird und der eine Verbindung mit einem Zielcomputer herstellt, auf dem nur IPv4 oder IPv6 ausgeführt wird, muss eine IP-Adresse im entsprechenden Format für die IP-Software des Ziel Computers</span><span class="sxs-lookup"><span data-stu-id="707c5-125">A computer that runs both IPv4 and IPv6 and connects to a target computer running only IPv4 or only IPv6 must supply an IP address in the appropriate format for the target computer IP software.</span></span>

## <a name="related-topics"></a><span data-ttu-id="707c5-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="707c5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="707c5-127">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="707c5-127">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
