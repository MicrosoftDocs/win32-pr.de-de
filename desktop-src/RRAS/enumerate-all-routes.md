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
# <a name="enumerate-all-routes"></a>Alle Routen aufzählen

Im folgenden Verfahren werden die Schritte beschrieben, die zum Auflisten von Entitäten verwendet werden, die von der RTMv2-API verwendet werden. Der folgende Beispielcode zeigt, wie alle Routen aufgelistet werden.

**Der grundlegende Prozess für jede Enumeration lautet wie folgt:**

1.  Starten Sie die-Enumeration, indem Sie ein Handle vom Routing Tabellen-Manager abrufen. Aufrufen von [**rtmkreatedestenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**rtmkreaterouteenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) und [**rtmkreatenexthopenum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) die Kriterien, die die Art der aufzuzählenden Informationen angeben. Dieses Kriterium umfasst, ist aber nicht auf eine Reihe von Zielen, eine bestimmte Schnittstelle und die Sichten beschränkt, in denen sich die Informationen befinden.
2.  Aufrufen von [**rtmgetenumdebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**rtmgetenumroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) und [**rtmgetenumnexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) einmal oder mehrmals zum Abrufen von Daten, bis der Routing Tabellen-Manager Fehler \_ keine \_ weiteren Elemente zurückgibt \_ . Die Routen-, Ziel-und Next-Hop-Daten werden in der Reihenfolge der Adressinformationen (und die Werte für die Präferenz und Metrik, wenn Routen aufgelistet werden) zurückgegeben.
3.  Aufrufen von [**rtmreleasedests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**rtmreleaseroutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) und [**rtmreleasenexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) , wenn die mit der-Enumeration verknüpften Handles oder Informationsstrukturen nicht mehr benötigt werden.
4.  Aufrufen von [**rtmdeleteenumhandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) zum Freigeben des enumerationshandles, das beim Erstellen der Enumeration zurückgegeben wurde. Diese Funktion wird verwendet, um das Handle für alle Typen von Enumerationen freizugeben.

> [!Note]  
> Routen, die den Status "Hold-Down" aufweisen, werden nur aufgelistet, wenn ein Client mithilfe der RTM- \_ Ansicht \_ Maske beliebige Daten von allen Sichten anfordert \_ .

 

Der folgende Beispielcode zeigt, wie alle Routen in der Routing Tabelle aufgelistet werden.


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



 

 




