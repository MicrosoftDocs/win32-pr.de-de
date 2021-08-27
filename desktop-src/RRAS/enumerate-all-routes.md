---
title: Aufzählen aller Routen
description: Das folgende Verfahren beschreibt die Schritte zum Aufzählen aller Entitäten, die von der RTMv2-API verwendet werden. Der folgende Beispielcode zeigt, wie alle Routen aufzählt werden.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f8707c7cf78f274fedaca3fb4882ae36dbd569ab5fa1260ec3b6cb663aced3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101850"
---
# <a name="enumerate-all-routes"></a>Aufzählen aller Routen

Das folgende Verfahren beschreibt die Schritte zum Aufzählen aller Entitäten, die von der RTMv2-API verwendet werden. Der folgende Beispielcode zeigt, wie alle Routen aufzählt werden.

**Der grundlegende Prozess für jede Enumeration lautet wie folgt:**

1.  Starten Sie die -Enumeration, indem Sie ein Handle vom Routingtabellen-Manager abrufen. Rufen [**Sie RtmCreateDestEnum,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum) [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) und [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) auf, um die Kriterien zur Angabe der Art der aufzählten Informationen zu geben. Diese Kriterien umfassen unter anderem einen Bereich von Zielen, eine bestimmte Schnittstelle und die Ansichten, in denen sich die Informationen befinden.
2.  Rufen [**Sie RtmGetEnumDests,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests) [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) und [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) mindestens einmal auf, um Daten abzurufen, bis der Routingtabellen-Manager ERROR NO MORE ITEMS zurückgibt. \_ \_ \_ Die Routen-, Ziel- und Nächsten-Hop-Daten werden in der Reihenfolge der Adressinformationen (und der Einstellungs- und Metrikwerte, wenn Routen aufzählt werden) zurückgegeben.
3.  Rufen [**Sie RtmReleaseDests,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) und [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) auf, wenn die der Enumeration zugeordneten Handles oder Informationsstrukturen nicht mehr benötigt werden.
4.  Rufen [**Sie RtmDeleteEnumHandle auf,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) um das Enumerationshandle frei zu geben, das beim Erstellen der Enumeration zurückgegeben wurde. Diese Funktion wird verwendet, um das Handle für alle Enumerationstypen frei zu geben.

> [!Note]  
> Routen, die sich im zurückhaltenden Zustand befinden, werden nur aufzählt, wenn ein Client Daten aus allen Ansichten mit RTM \_ VIEW MASK ANY an \_ \_ fordert.

 

Der folgende Beispielcode zeigt, wie sie alle Routen in der Routingtabelle aufzählen.


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



 

 




