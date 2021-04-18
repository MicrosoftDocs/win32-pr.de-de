---
title: Hinzufügen und Aktualisieren von Routen mithilfe von rtmaddroutededest
description: Die Funktion rtmaddroutededest wird zum Hinzufügen neuer Routen und zum Aktualisieren vorhandener Routen für ein Ziel verwendet. In den folgenden Verfahren werden beide Fälle erläutert. Der folgende Beispielcode zeigt, wie die erste Prozedur implementiert wird.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3594aee054e6815094834bedbc1aae158fc4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338998"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a><span data-ttu-id="f102e-105">Hinzufügen und Aktualisieren von Routen mithilfe von rtmaddroutededest</span><span class="sxs-lookup"><span data-stu-id="f102e-105">Add and Update Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="f102e-106">Die Funktion [**rtmaddroutededest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) wird zum Hinzufügen neuer Routen und zum Aktualisieren vorhandener Routen für ein Ziel verwendet.</span><span class="sxs-lookup"><span data-stu-id="f102e-106">The function [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) is used to add new routes and update existing routes for a destination.</span></span> <span data-ttu-id="f102e-107">In den folgenden Verfahren werden beide Fälle erläutert.</span><span class="sxs-lookup"><span data-stu-id="f102e-107">The following procedures explain both cases.</span></span> <span data-ttu-id="f102e-108">Der folgende Beispielcode zeigt, wie die erste Prozedur implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="f102e-108">The sample code that follows shows how to implement the first procedure.</span></span>

<span data-ttu-id="f102e-109">**Zum Hinzufügen einer Route sollte der Client die folgenden Schritte ausführen:**</span><span class="sxs-lookup"><span data-stu-id="f102e-109">**To add a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="f102e-110">Wenn der Client den nächsten Hop-handle bereits zwischengespeichert hat, fahren Sie mit Schritt 4 fort.</span><span class="sxs-lookup"><span data-stu-id="f102e-110">If the client has already cached the next-hop handle, go to step 4.</span></span>
2.  <span data-ttu-id="f102e-111">Erstellen Sie eine [**RTM- \_ nexthop \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) -Informationsstruktur, und füllen Sie Sie mit den entsprechenden Informationen aus.</span><span class="sxs-lookup"><span data-stu-id="f102e-111">Create an [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure and fill it with the appropriate information.</span></span>
3.  <span data-ttu-id="f102e-112">Fügen Sie der Routing Tabelle den nächsten Hop hinzu, indem Sie [**rtmaddnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f102e-112">Add the next hop to the routing table by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="f102e-113">Der Routing Tabellen-Manager gibt ein Handle für den nächsten Hop zurück.</span><span class="sxs-lookup"><span data-stu-id="f102e-113">The routing table manager returns a handle to the next hop.</span></span> <span data-ttu-id="f102e-114">Wenn der nächste Hop bereits vorhanden ist, fügt die Routing Tabelle den nächsten Hop nicht hinzu. Stattdessen wird das Handle an den nächsten Hop zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f102e-114">If the next hop already exists, the routing table does not add the next hop; instead it returns the handle to the next hop.</span></span>
4.  <span data-ttu-id="f102e-115">Erstellen Sie eine [**RTM- \_ Routen \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Informationsstruktur, und füllen Sie Sie mit den entsprechenden Informationen aus, einschließlich des Handles für den nächsten Hop, der vom Routing Tabellen-Manager zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f102e-115">Create an [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure and fill it with the appropriate information, including the next-hop handle returned by the routing table manager.</span></span>
5.  <span data-ttu-id="f102e-116">Fügen Sie der Routing Tabelle die Route hinzu, indem Sie [**rtmaddroutetodest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f102e-116">Add the route to the routing table by calling [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span></span> <span data-ttu-id="f102e-117">Der Routing Tabellen-Manager vergleicht die neue Route mit den Routen, die bereits in der Routing Tabelle vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f102e-117">The routing table manager compares the new route to the routes that are already in the routing table.</span></span> <span data-ttu-id="f102e-118">Zwei Routen sind gleich, wenn alle der folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="f102e-118">Two routes are equal if all of the following conditions are true:</span></span>

    -   <span data-ttu-id="f102e-119">Die Route wird dem gleichen Ziel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f102e-119">The route is being added to the same destination.</span></span>
    -   <span data-ttu-id="f102e-120">Die Route wird durch denselben Client hinzugefügt, der vom **Besitzer** Mitglied der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f102e-120">The route is being added by the same client as specified by the **Owner** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>
    -   <span data-ttu-id="f102e-121">Die Route wird durch denselben Nachbar angekündigt, der vom **Nachbar** Mitglied der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f102e-121">The route is advertised by the same neighbor as specified by the **Neighbor** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

    <span data-ttu-id="f102e-122">Wenn die Route vorhanden ist, gibt der Routing Tabellen-Manager das Handle an die vorhandene Route zurück.</span><span class="sxs-lookup"><span data-stu-id="f102e-122">If the route exists, the routing table manager returns the handle to the existing route.</span></span> <span data-ttu-id="f102e-123">Andernfalls fügt der Routing Tabellen-Manager die Route hinzu und gibt das Handle an die neue Route zurück.</span><span class="sxs-lookup"><span data-stu-id="f102e-123">Otherwise, the routing table manager adds the route and returns the handle to the new route.</span></span>

    <span data-ttu-id="f102e-124">Der Client kann den *\_ änderungsflags* -Parameter auf RTM- \_ Routen \_ Änderung neu festlegen, \_ um den Routing Tabellen-Manager anzuweisen, eine neue Route zum Ziel hinzuzufügen, selbst wenn eine andere Route mit demselben Besitzer-und Nachbarfeld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f102e-124">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_NEW to instruct the routing table manager to add a new route on the destination, even if another route with the same owner and neighbor fields exists.</span></span>

    <span data-ttu-id="f102e-125">Der Client kann den *\_ änderungsflags* -Parameter zuerst auf die RTM- \_ Routen \_ Änderung festlegen \_ , um dem Routing Tabellen-Manager mitzuteilen, dass die erste Route auf dem Ziel des Clients aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f102e-125">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_FIRST to tell the routing table manager to update the first route on the destination owned by the client.</span></span> <span data-ttu-id="f102e-126">Dieses Update kann ausgeführt werden, wenn eine solche Route vorhanden ist, auch wenn das Nachbarfeld nicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="f102e-126">This update can be performed if such a route exists, even if the neighbor field does not match.</span></span> <span data-ttu-id="f102e-127">Dieses Flag wird von Clients verwendet, die eine einzelne Route pro Ziel verwalten.</span><span class="sxs-lookup"><span data-stu-id="f102e-127">This flag is used by clients that maintain a single route per destination.</span></span>

<span data-ttu-id="f102e-128">**Um eine Route zu aktualisieren, muss der Client die folgenden Schritte ausführen:**</span><span class="sxs-lookup"><span data-stu-id="f102e-128">**To update a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="f102e-129">Aufrufen von [**rtmgetrouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) mit dem Handle der Route.</span><span class="sxs-lookup"><span data-stu-id="f102e-129">Call [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) with the handle to the route.</span></span> <span data-ttu-id="f102e-130">Das Handle ist entweder zuvor vom Client zwischengespeichert oder wurde vom Routing Tabellen-Manager von einem-Ausdruck zurückgegeben, der ein Routen handle wie **rtmgetrouteinfo** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f102e-130">The handle is either one previously cached by the client, or returned by the routing table manager from a call that returns a route handle such as **RtmGetRouteInfo**.</span></span>
2.  <span data-ttu-id="f102e-131">Nehmen Sie die Änderungen an der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur vor, die vom Routing Tabellen-Manager zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f102e-131">Make the changes to the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure that is returned by the routing table manager.</span></span>
3.  <span data-ttu-id="f102e-132">Nennen Sie [**rtmaddroutetodest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) mit dem Handle für die Route und die geänderte RTM-Weiterleitungs [**\_ \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f102e-132">Call [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) with the handle to the route and the changed [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

<span data-ttu-id="f102e-133">Der folgende Beispielcode zeigt, wie Sie eine Route zu einem Ziel hinzufügen, indem Sie den Routing Tabellen-Manager als Vermittler verwenden.</span><span class="sxs-lookup"><span data-stu-id="f102e-133">The following sample code shows how to add a route to a destination using the routing table manager as an intermediary.</span></span>


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




