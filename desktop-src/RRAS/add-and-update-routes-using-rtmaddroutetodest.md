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
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Hinzufügen und Aktualisieren von Routen mithilfe von rtmaddroutededest

Die Funktion [**rtmaddroutededest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) wird zum Hinzufügen neuer Routen und zum Aktualisieren vorhandener Routen für ein Ziel verwendet. In den folgenden Verfahren werden beide Fälle erläutert. Der folgende Beispielcode zeigt, wie die erste Prozedur implementiert wird.

**Zum Hinzufügen einer Route sollte der Client die folgenden Schritte ausführen:**

1.  Wenn der Client den nächsten Hop-handle bereits zwischengespeichert hat, fahren Sie mit Schritt 4 fort.
2.  Erstellen Sie eine [**RTM- \_ nexthop \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) -Informationsstruktur, und füllen Sie Sie mit den entsprechenden Informationen aus.
3.  Fügen Sie der Routing Tabelle den nächsten Hop hinzu, indem Sie [**rtmaddnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)aufrufen. Der Routing Tabellen-Manager gibt ein Handle für den nächsten Hop zurück. Wenn der nächste Hop bereits vorhanden ist, fügt die Routing Tabelle den nächsten Hop nicht hinzu. Stattdessen wird das Handle an den nächsten Hop zurückgegeben.
4.  Erstellen Sie eine [**RTM- \_ Routen \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Informationsstruktur, und füllen Sie Sie mit den entsprechenden Informationen aus, einschließlich des Handles für den nächsten Hop, der vom Routing Tabellen-Manager zurückgegeben wird.
5.  Fügen Sie der Routing Tabelle die Route hinzu, indem Sie [**rtmaddroutetodest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)aufrufen. Der Routing Tabellen-Manager vergleicht die neue Route mit den Routen, die bereits in der Routing Tabelle vorhanden sind. Zwei Routen sind gleich, wenn alle der folgenden Bedingungen zutreffen:

    -   Die Route wird dem gleichen Ziel hinzugefügt.
    -   Die Route wird durch denselben Client hinzugefügt, der vom **Besitzer** Mitglied der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur angegeben wird.
    -   Die Route wird durch denselben Nachbar angekündigt, der vom **Nachbar** Mitglied der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur angegeben wird.

    Wenn die Route vorhanden ist, gibt der Routing Tabellen-Manager das Handle an die vorhandene Route zurück. Andernfalls fügt der Routing Tabellen-Manager die Route hinzu und gibt das Handle an die neue Route zurück.

    Der Client kann den *\_ änderungsflags* -Parameter auf RTM- \_ Routen \_ Änderung neu festlegen, \_ um den Routing Tabellen-Manager anzuweisen, eine neue Route zum Ziel hinzuzufügen, selbst wenn eine andere Route mit demselben Besitzer-und Nachbarfeld vorhanden ist.

    Der Client kann den *\_ änderungsflags* -Parameter zuerst auf die RTM- \_ Routen \_ Änderung festlegen \_ , um dem Routing Tabellen-Manager mitzuteilen, dass die erste Route auf dem Ziel des Clients aktualisiert werden soll. Dieses Update kann ausgeführt werden, wenn eine solche Route vorhanden ist, auch wenn das Nachbarfeld nicht entspricht. Dieses Flag wird von Clients verwendet, die eine einzelne Route pro Ziel verwalten.

**Um eine Route zu aktualisieren, muss der Client die folgenden Schritte ausführen:**

1.  Aufrufen von [**rtmgetrouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) mit dem Handle der Route. Das Handle ist entweder zuvor vom Client zwischengespeichert oder wurde vom Routing Tabellen-Manager von einem-Ausdruck zurückgegeben, der ein Routen handle wie **rtmgetrouteinfo** zurückgibt.
2.  Nehmen Sie die Änderungen an der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur vor, die vom Routing Tabellen-Manager zurückgegeben wird.
3.  Nennen Sie [**rtmaddroutetodest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) mit dem Handle für die Route und die geänderte RTM-Weiterleitungs [**\_ \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur.

Der folgende Beispielcode zeigt, wie Sie eine Route zu einem Ziel hinzufügen, indem Sie den Routing Tabellen-Manager als Vermittler verwenden.


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



 

 




