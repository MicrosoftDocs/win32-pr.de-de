---
title: Hinzufügen und Aktualisieren von Routen mit rtmAddRouteToDest
description: Die Funktion RtmAddRouteToDest wird verwendet, um neue Routen hinzuzufügen und vorhandene Routen für ein Ziel zu aktualisieren. In den folgenden Verfahren werden beide Fälle erläutert. Der folgende Beispielcode zeigt, wie die erste Prozedur implementiert wird.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64032aa5f73019e08bb82405d85ffa5ef85abd0526cf7748ec8881b97ab900e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030600"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Hinzufügen und Aktualisieren von Routen mit rtmAddRouteToDest

Die Funktion [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) wird verwendet, um neue Routen hinzuzufügen und vorhandene Routen für ein Ziel zu aktualisieren. In den folgenden Verfahren werden beide Fälle erläutert. Der folgende Beispielcode zeigt, wie die erste Prozedur implementiert wird.

**Um eine Route hinzuzufügen, muss der Client die folgenden Schritte ausführen:**

1.  Wenn der Client das Handle für den nächsten Hop bereits zwischengespeichert hat, fahren Sie mit Schritt 4 fort.
2.  Erstellen Sie eine [**RTM \_ NEXTHOP \_ INFO-Struktur,**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) und füllen Sie sie mit den entsprechenden Informationen aus.
3.  Fügen Sie der Routingtabelle den nächsten Hop hinzu, indem Sie [**RtmAddNextHop aufrufen.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop) Der Routingtabellen-Manager gibt ein Handle an den nächsten Hop zurück. Wenn der nächste Hop bereits vorhanden ist, fügt die Routingtabelle den nächsten Hop nicht hinzu. Stattdessen wird das Handle an den nächsten Hop zurückgegeben.
4.  Erstellen Sie eine [**RTM \_ ROUTE \_ INFO-Struktur,**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) und füllen Sie sie mit den entsprechenden Informationen aus, einschließlich des vom Routingtabellen-Manager zurückgegebenen Next-Hop-Handles.
5.  Fügen Sie die Route der Routingtabelle hinzu, indem [**Sie RtmAddRouteToDest aufrufen.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) Der Routingtabellen-Manager vergleicht die neue Route mit den Routen, die bereits in der Routingtabelle vorhanden sind. Zwei Routen sind gleich, wenn alle der folgenden Bedingungen erfüllt sind:

    -   Die Route wird demselben Ziel hinzugefügt.
    -   Die Route wird vom gleichen Client hinzugefügt, wie vom **Owner-Member** der [**RTM \_ ROUTE \_ INFO-Struktur**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) angegeben.
    -   Die Route wird vom gleichen Nachbarn angekündigt, der vom **Neighbor-Member** der [**RTM ROUTE \_ \_ INFO-Struktur angegeben**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) wird.

    Wenn die Route vorhanden ist, gibt der Routingtabellen-Manager das Handle an die vorhandene Route zurück. Andernfalls fügt der Routingtabellen-Manager die Route hinzu und gibt das Handle an die neue Route zurück.

    Der Client kann den Parameter *\_ Änderungsflags* auf RTM ROUTE CHANGE NEW festlegen, um den Routingtabellen-Manager anweisen, dem Ziel eine neue Route hinzuzufügen, auch wenn eine andere Route mit demselben Besitzer- und Nachbarfeld \_ \_ vorhanden \_ ist.

    Der Client kann den *Parameter \_ Änderungsflags* auf RTM ROUTE CHANGE FIRST festlegen, um den Routingtabellen-Manager angibt, die erste Route auf dem Ziel zu aktualisieren, das sich im Besitz \_ des Clients \_ \_ befindet. Dieses Update kann ausgeführt werden, wenn eine solche Route vorhanden ist, auch wenn das Nachbarfeld nicht übereinstimmen. Dieses Flag wird von Clients verwendet, die eine einzelne Route pro Ziel verwalten.

**Um eine Route zu aktualisieren, muss der Client die folgenden Schritte ausführen:**

1.  Rufen [**Sie RtmGetRouteInfo mit**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) dem Handle für die Route auf. Das Handle ist entweder ein zuvor vom Client zwischengespeichertes Handle oder wird vom Routingtabellen-Manager von einem Aufruf zurückgegeben, der ein Routenhand handle wie **RtmGetRouteInfo zurückgibt.**
2.  Nehmen Sie die Änderungen an der [**RTM \_ ROUTE \_ INFO-Struktur**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) vor, die vom Routingtabellen-Manager zurückgegeben wird.
3.  Rufen [**Sie RtmAddRouteToDest mit**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) dem Handle für die Route und der geänderten [**RTM-ROUTENINFO-Struktur \_ \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) auf.

Der folgende Beispielcode zeigt, wie Sie einem Ziel eine Route hinzufügen, indem Sie den Routingtabellen-Manager als Vermittler verwenden.


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



 

 




