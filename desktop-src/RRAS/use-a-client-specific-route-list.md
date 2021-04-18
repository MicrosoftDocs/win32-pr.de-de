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
# <a name="use-a-client-specific-route-list"></a>Client-Specific Routenliste verwenden

In den folgenden Verfahren werden die Schritte zum Verwenden der Client spezifischen Routenlisten erläutert. Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.

**Um dieses Feature verwenden zu können, muss ein Client die folgenden Schritte ausführen:**

1.  Rufen Sie [**rtmkreateroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) auf, um ein Handle vom Routing Tabellen-Manager zu erhalten.
2.  Ruft [**rtminsertinroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) immer dann auf, wenn der Client eine Route zu dieser Liste hinzufügen muss.
3.  Wenn der Client die Liste nicht mehr benötigt, sollte er [**rtmdeleteroutelist**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) aufrufen, um die Liste zu entfernen.

**Wenn der Client die Routen in der Liste auflisten muss, muss der Client die folgenden Schritte ausführen:**

1.  Rufen Sie [**rtmkreateroutelistenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) auf, um ein enumerationshandle aus dem Routing Tabellen-Manager abzurufen.
2.  Rufen Sie [**rtmgetlistenumroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) auf, um die Handles für die Routen in der Liste zu erhalten.
3.  Wenden Sie [**rtmreleaseroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) an, um die Handles freizugeben, wenn Sie nicht mehr benötigt werden.

Der folgende Beispielcode zeigt, wie eine Client spezifische Routenliste erstellt und verwendet wird.


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



 

 




