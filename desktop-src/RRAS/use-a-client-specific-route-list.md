---
title: Client-Specific Routenliste verwenden
description: In den folgenden Verfahren werden die Schritte zum Verwenden der Client spezifischen Routenlisten erläutert. Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.
ms.assetid: aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cfa893bda9e850527c7ebe35590dbe2d08a490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341263"
---
# <a name="use-a-client-specific-route-list"></a><span data-ttu-id="795c4-104">Client-Specific Routenliste verwenden</span><span class="sxs-lookup"><span data-stu-id="795c4-104">Use a Client-Specific Route List</span></span>

<span data-ttu-id="795c4-105">In den folgenden Verfahren werden die Schritte zum Verwenden der Client spezifischen Routenlisten erläutert.</span><span class="sxs-lookup"><span data-stu-id="795c4-105">The following procedures outlines the steps to use the client-specific route lists.</span></span> <span data-ttu-id="795c4-106">Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="795c4-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="795c4-107">**Um dieses Feature verwenden zu können, muss ein Client die folgenden Schritte ausführen:**</span><span class="sxs-lookup"><span data-stu-id="795c4-107">**To use this feature, a client should take the following steps**</span></span>

1.  <span data-ttu-id="795c4-108">Rufen Sie [**rtmkreateroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) auf, um ein Handle vom Routing Tabellen-Manager zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="795c4-108">Call [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) to obtain a handle from the routing table manager.</span></span>
2.  <span data-ttu-id="795c4-109">Ruft [**rtminsertinroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) immer dann auf, wenn der Client eine Route zu dieser Liste hinzufügen muss.</span><span class="sxs-lookup"><span data-stu-id="795c4-109">Call [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) whenever the client must add a route to this list.</span></span>
3.  <span data-ttu-id="795c4-110">Wenn der Client die Liste nicht mehr benötigt, sollte er [**rtmdeleteroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) aufrufen, um die Liste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="795c4-110">When the client no longer requires the list, it should call [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) to remove the list.</span></span>

<span data-ttu-id="795c4-111">**Wenn der Client die Routen in der Liste auflisten muss, muss der Client die folgenden Schritte ausführen:**</span><span class="sxs-lookup"><span data-stu-id="795c4-111">**If the client must enumerate the routes on the list, the client should take the following steps**</span></span>

1.  <span data-ttu-id="795c4-112">Rufen Sie [**rtmkreateroutelistenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) auf, um ein enumerationshandle aus dem Routing Tabellen-Manager abzurufen.</span><span class="sxs-lookup"><span data-stu-id="795c4-112">Call [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) to obtain an enumeration handle from the routing table manager.</span></span>
2.  <span data-ttu-id="795c4-113">Rufen Sie [**rtmgetlistenumroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) auf, um die Handles für die Routen in der Liste zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="795c4-113">Call [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) to obtain the handles to the routes in the list.</span></span>
3.  <span data-ttu-id="795c4-114">Wenden Sie [**rtmreleaseroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) an, um die Handles freizugeben, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="795c4-114">Call [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) to release the handles when no longer required.</span></span>

<span data-ttu-id="795c4-115">Der folgende Beispielcode zeigt, wie eine Client spezifische Routenliste erstellt und verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795c4-115">The following sample code shows how to create and use a client-specific route list.</span></span>


```C++
HANDLE RouteListHandle1;
HANDLE RouteListHandle2;

// Create two entity-specific lists to add routes to

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle1);
// Check Status
//...

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle2);
// Check Status
//...

// Assume you have added a bunch of routes
// by calling RtmAddRouteToDest many times
// with 'RouteListHandle1' specified similar to
// Status = RtmAddRouteToDest(RtmRegHandle,
//                            ...
//                            RouteListHandle1,
//                            ...
//                            &ChangeFlags);

// Enumerate routes in RouteListHandle1 list

// Create an enumeration on the route list

Status = RtmCreateRouteListEnum(RtmRegHandle,
                                RouteListHandle1,
                                &EnumHandle);

if (Status == NO_ERROR)
{
        // Allocate space on the top of the stack
        
    MaxHandles = RegnProfile.MaxHandlesInEnum;

    RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

    // Note how the termination condition is different
    // from other enumerations - the call to the function
    // RtmGetListEnumRoutes always returns NO_ERROR
    // Quit when you get fewer handles than requested
    
    do
    {
                // Get next set of routes from the list enumeration
        
        NumHandles = MaxHandles;

        Status = RtmGetListEnumRoutes(RtmRegHandle,
                                      EnumHandle,
                                      &NumHandles,
                                      RouteHandles);

        for (i = 0; i < NumHandles; i++)
        {
            Print("Route Handle %5lu: %p\n", i, RouteHandles[i]);
        }

        // Move all these routes to another route list
        // They are automatically removed from the old one
        
        Status = RtmInsertInRouteList(RtmRegHandle,
                                      RouteListHandle2,
                                      NumHandles,
                                      RouteHandles);
        // Check Status...
        
                // Release the routes that have been enumerated
        
        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (NumHandles == MaxHandles);

    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}

// Destroy all the entity-specific route lists 
// after removing all routes from these lists;
// the routes themselves are not deleted

Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle1);
ASSERT(Status == NO_ERROR);


Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle2);
ASSERT(Status == NO_ERROR);
```



 

 




