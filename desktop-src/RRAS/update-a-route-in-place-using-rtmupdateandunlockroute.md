---
title: Direktes Aktualisieren einer Route mithilfe von rtmupdateandunlockroute
description: Im folgenden Verfahren werden die Schritte beschrieben, die zum Aktualisieren einer Route vorhanden sind. Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388476"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a>Direktes Aktualisieren einer Route mithilfe von rtmupdateandunlockroute

Im folgenden Verfahren werden die Schritte beschrieben, die zum Aktualisieren einer Route vorhanden sind. Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.

**Um eine Route zu aktualisieren, muss der Client die folgenden Schritte ausführen:**

1.  Sperren Sie die Route durch Aufrufen von [**rtmlockroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute). Derzeit sperrt diese Funktion das Ziel der Route. Der Routing Tabellen-Manager gibt einen Zeiger auf die Route zurück.
2.  Verwenden Sie den Zeiger auf die [**RTM-Weiterleitungs \_ \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur des Routing Tabellen-Managers, die Sie in Schritt 1 erhalten haben, um die erforderlichen Änderungen an der Route vorzunehmen. Nur bestimmte Mitglieder der RTM-Weiterleitungs **\_ \_ Informations** Struktur können beim direkten aktualisieren geändert werden. Diese Member lauten: **Nachbar**, **prefinfo**, **entityspecificinfo**, **belongstoviews** und **nexthopslist**.
    > [!Note]  
    > Wenn der Client dem **Nachbar** -oder dem **nexthopslist** -Member Informationen hinzufügt, muss der Client [**rtmreferencehandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) abrufen, um explizit den Verweis Zähler zu erhöhen, den der Routing Tabellen-Manager im Next-Hop-Objekt speichert. Auch wenn der Client Informationen aus dem **nexthopslist** -Member entfernt, muss der Client [**rtmreleasenexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) aufzurufen, um den Verweis Zähler zu verringern.

     

3.  Nennen Sie [**rtmupdateandunlockroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) , um den Routing Tabellen-Manager zu benachrichtigen, dass eine Änderung vorgenommen wurde. Der Routing Tabellen-Manager führt einen Commit für die Änderungen aus, aktualisiert das Ziel, um die neuen Informationen widerzuspiegeln, und entsperrt dann die Route.

Der folgende Beispielcode zeigt, wie Sie eine Route direkt mithilfe eines Zeigers auf die eigentlichen Routeninformationen in der Routing Tabelle aktualisieren.


```C++
Status = RtmLockRoute(RtmRegHandle,
                      RouteHandle,
                      TRUE,
                      TRUE,
                      &RoutePointer);

if (Status == NO_ERROR)
{
        // Update route parameters in place (i.e., directly on 
// the routing table manager's copy)
    
    // Update the metric and views of the route
    RoutePointer->PrefInfo.Metric = 16;

    // Change the views so that the route belongs to only the multicast view
    RoutePointer->BelongsToViews = RTM_VIEW_MASK_MCAST;

    // Set the entity-specific information to X
    RoutePointer->EntitySpecificInfo = X;

    // Note that the following manipulation of
    // next-hop references is not needed when
    // using RtmAddRouteToDest, as it is done
    // by the routing table manager automatically
    
    // Change next hop from NextHop1 to NextHop2
    NextHop1 = RoutePointer->NextHopsList.NextHop[0];

    // Explicitly dereference the old next hop
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHop1);

    RoutePointer->NextHopsList.NextHop[0] = NextHop2;

    // Explicitly reference next hop being added
    RtmReferenceHandles(RtmRegHandle, 1, &NextHop2);

    // Call the routing table manager to indicate that route information
    // has changed, and that its position might
    // have to be rearranged and the corresponding destination
    // needs to be updated to reflect this change.
    
    Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                     RouteHandle,
                                     INFINITE, // Keep forever
                                     NULL,
                                     0,
                                     NULL,
                                     &ChangeFlags);
    ASSERT(Status == NO_ERROR);
}
```



 

 




