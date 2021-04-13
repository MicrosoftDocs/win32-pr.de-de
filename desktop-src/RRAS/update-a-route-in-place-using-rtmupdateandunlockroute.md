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
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="db52c-104">Direktes Aktualisieren einer Route mithilfe von rtmupdateandunlockroute</span><span class="sxs-lookup"><span data-stu-id="db52c-104">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="db52c-105">Im folgenden Verfahren werden die Schritte beschrieben, die zum Aktualisieren einer Route vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="db52c-105">The following procedure outlines the steps used to update a route in place.</span></span> <span data-ttu-id="db52c-106">Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="db52c-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="db52c-107">**Um eine Route zu aktualisieren, muss der Client die folgenden Schritte ausführen:**</span><span class="sxs-lookup"><span data-stu-id="db52c-107">**To update a route in place, the client should take the following steps**</span></span>

1.  <span data-ttu-id="db52c-108">Sperren Sie die Route durch Aufrufen von [**rtmlockroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span><span class="sxs-lookup"><span data-stu-id="db52c-108">Lock the route by calling [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span></span> <span data-ttu-id="db52c-109">Derzeit sperrt diese Funktion das Ziel der Route.</span><span class="sxs-lookup"><span data-stu-id="db52c-109">Currently, this function actually locks the route's destination.</span></span> <span data-ttu-id="db52c-110">Der Routing Tabellen-Manager gibt einen Zeiger auf die Route zurück.</span><span class="sxs-lookup"><span data-stu-id="db52c-110">The routing table manager returns a pointer to the route.</span></span>
2.  <span data-ttu-id="db52c-111">Verwenden Sie den Zeiger auf die [**RTM-Weiterleitungs \_ \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur des Routing Tabellen-Managers, die Sie in Schritt 1 erhalten haben, um die erforderlichen Änderungen an der Route vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="db52c-111">Use the pointer to the routing table manager's [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure, obtained in step 1, to make the necessary changes to the route.</span></span> <span data-ttu-id="db52c-112">Nur bestimmte Mitglieder der RTM-Weiterleitungs **\_ \_ Informations** Struktur können beim direkten aktualisieren geändert werden.</span><span class="sxs-lookup"><span data-stu-id="db52c-112">Only certain members of the **RTM\_ROUTE\_INFO** structure can be modified when updating in place.</span></span> <span data-ttu-id="db52c-113">Diese Member lauten: **Nachbar**, **prefinfo**, **entityspecificinfo**, **belongstoviews** und **nexthopslist**.</span><span class="sxs-lookup"><span data-stu-id="db52c-113">These members are: **Neighbour**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews**, and **NextHopsList**.</span></span>
    > [!Note]  
    > <span data-ttu-id="db52c-114">Wenn der Client dem **Nachbar** -oder dem **nexthopslist** -Member Informationen hinzufügt, muss der Client [**rtmreferencehandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) abrufen, um explizit den Verweis Zähler zu erhöhen, den der Routing Tabellen-Manager im Next-Hop-Objekt speichert.</span><span class="sxs-lookup"><span data-stu-id="db52c-114">If the client adds information to either the **Neighbour** or **NextHopsList** members, the client must call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) to explicitly increment the reference count that the routing table manager keeps on the next-hop object.</span></span> <span data-ttu-id="db52c-115">Auch wenn der Client Informationen aus dem **nexthopslist** -Member entfernt, muss der Client [**rtmreleasenexthops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) aufzurufen, um den Verweis Zähler zu verringern.</span><span class="sxs-lookup"><span data-stu-id="db52c-115">Similarly, if the client removes information from the **NextHopsList** member, the client must call [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) to decrement the reference count.</span></span>

     

3.  <span data-ttu-id="db52c-116">Nennen Sie [**rtmupdateandunlockroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) , um den Routing Tabellen-Manager zu benachrichtigen, dass eine Änderung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="db52c-116">Call [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) to notify the routing table manager that a change has taken place.</span></span> <span data-ttu-id="db52c-117">Der Routing Tabellen-Manager führt einen Commit für die Änderungen aus, aktualisiert das Ziel, um die neuen Informationen widerzuspiegeln, und entsperrt dann die Route.</span><span class="sxs-lookup"><span data-stu-id="db52c-117">The routing table manager commits the changes, updates the destination to reflect the new information, and then unlocks the route.</span></span>

<span data-ttu-id="db52c-118">Der folgende Beispielcode zeigt, wie Sie eine Route direkt mithilfe eines Zeigers auf die eigentlichen Routeninformationen in der Routing Tabelle aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db52c-118">The following sample code shows how to update a route directly, using a pointer to the actual route information in the routing table.</span></span>


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



 

 




