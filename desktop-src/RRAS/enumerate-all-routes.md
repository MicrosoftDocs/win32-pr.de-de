---
title: Alle Routen aufzählen
description: Im folgenden Verfahren werden die Schritte beschrieben, die zum Auflisten von Entitäten verwendet werden, die von der RTMv2-API verwendet werden. Der folgende Beispielcode zeigt, wie alle Routen aufgelistet werden.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c927665cab8d4db492d3a2c5f8e9363fc1fe7be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711340"
---
# <a name="enumerate-all-routes"></a><span data-ttu-id="03453-104">Alle Routen aufzählen</span><span class="sxs-lookup"><span data-stu-id="03453-104">Enumerate All Routes</span></span>

<span data-ttu-id="03453-105">Im folgenden Verfahren werden die Schritte beschrieben, die zum Auflisten von Entitäten verwendet werden, die von der RTMv2-API verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03453-105">The following procedure outlines the steps used to enumerate any of the entities used by the RTMv2 API.</span></span> <span data-ttu-id="03453-106">Der folgende Beispielcode zeigt, wie alle Routen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="03453-106">The sample code that follows shows how to enumerate all routes.</span></span>

<span data-ttu-id="03453-107">**Der grundlegende Prozess für jede Enumeration lautet wie folgt:**</span><span class="sxs-lookup"><span data-stu-id="03453-107">**The basic process for each enumeration is as follows**</span></span>

1.  <span data-ttu-id="03453-108">Starten Sie die-Enumeration, indem Sie ein Handle vom Routing Tabellen-Manager abrufen.</span><span class="sxs-lookup"><span data-stu-id="03453-108">Start the enumeration by obtaining a handle from the routing table manager.</span></span> <span data-ttu-id="03453-109">Aufrufen von [**rtmkreatedestenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**rtmkreaterouteenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) und [**rtmkreatenexthopenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) die Kriterien, die die Art der aufzuzählenden Informationen angeben.</span><span class="sxs-lookup"><span data-stu-id="03453-109">Call [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) and [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) to supply the criteria that specifies the kind of information being enumerated.</span></span> <span data-ttu-id="03453-110">Dieses Kriterium umfasst, ist aber nicht auf eine Reihe von Zielen, eine bestimmte Schnittstelle und die Sichten beschränkt, in denen sich die Informationen befinden.</span><span class="sxs-lookup"><span data-stu-id="03453-110">This criteria includes, but is not limited to a range of destinations, a particular interface, and the views in which the information resides.</span></span>
2.  <span data-ttu-id="03453-111">Aufrufen von [**rtmgetenumdebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**rtmgetenumroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) und [**rtmgetenumnexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) einmal oder mehrmals zum Abrufen von Daten, bis der Routing Tabellen-Manager Fehler \_ keine \_ weiteren Elemente zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="03453-111">Call [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) and [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) one or more times to retrieve data until the routing table manager returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="03453-112">Die Routen-, Ziel-und Next-Hop-Daten werden in der Reihenfolge der Adressinformationen (und die Werte für die Präferenz und Metrik, wenn Routen aufgelistet werden) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03453-112">The route, destination, and next-hop data is returned in order of the address information (and the preference and metric values, if routes are being enumerated).</span></span>
3.  <span data-ttu-id="03453-113">Aufrufen von [**rtmreleasedests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**rtmreleaseroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) und [**rtmreleasenexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) , wenn die mit der-Enumeration verknüpften Handles oder Informationsstrukturen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="03453-113">Call [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) and [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) when the handles or information structures associated with the enumeration are no longer required.</span></span>
4.  <span data-ttu-id="03453-114">Aufrufen von [**rtmdeleteenumhandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) zum Freigeben des enumerationshandles, das beim Erstellen der Enumeration zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="03453-114">Call [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) to release the enumeration handle that was returned when the enumeration was created.</span></span> <span data-ttu-id="03453-115">Diese Funktion wird verwendet, um das Handle für alle Typen von Enumerationen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="03453-115">This function is used to release the handle for all types of enumerations.</span></span>

> [!Note]  
> <span data-ttu-id="03453-116">Routen, die den Status "Hold-Down" aufweisen, werden nur aufgelistet, wenn ein Client mithilfe der RTM- \_ Ansicht \_ Maske beliebige Daten von allen Sichten anfordert \_ .</span><span class="sxs-lookup"><span data-stu-id="03453-116">Routes that are in the hold-down state are only enumerated when a client requests data from all views using RTM\_VIEW\_MASK\_ANY.</span></span>

 

<span data-ttu-id="03453-117">Der folgende Beispielcode zeigt, wie alle Routen in der Routing Tabelle aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="03453-117">The following sample code shows how to enumerate all routes in the routing table.</span></span>


```C++
MaxHandles = RegnProfile.MaxHandlesInEnum;

RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

// Do a "route enumeration" over the whole table
// by passing a NULL DestHandle in this function.

DestHandle = NULL; // Give a valid handle to enumerate over a particular destination

Status = RtmCreateRouteEnum(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST,
                            RTM_ENUM_OWN_ROUTES, // Get only your own routes
                            NULL,
                            0,
                            NULL,
                            0,
                            &EnumHandle2);
if (Status == NO_ERROR)
{
    do
    {
        NumHandles = MaxHandles;

        Status = RtmGetEnumRoutes(RtmRegHandle
                                  EnumHandle2,
                                  &NumHandles,
                                  RouteHandles);

        for (k = 0; k < NumHandles; k++)
        {
            wprintf("Route %d: %p\n", l++, RouteHandles[k]);

            // Get route information using the route's handle
            Status = RtmGetRouteInfo(...RouteHandles[k]...);

            if (Status == NO_ERROR)
            {
                // Do whatever you want with the route info
                //...

                // Release the route information once you are done
                RtmReleaseRouteInfo(...);
            }
        }

        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle2);
}
```



 

 




