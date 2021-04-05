---
title: Verwenden des Ereignis Benachrichtigungs Rückrufs
description: Im folgenden Verfahren werden die Schritte beschrieben, die der Client zum Empfangen von Änderungs Benachrichtigungs Meldungen vom RTM- \_ Ereignis Rückruf verwenden soll \_ . Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.
ms.assetid: e079c585-6457-4c2c-82bd-e95d233c4aa6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a650a762600c254979aaea974379b4021d0d73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037184"
---
# <a name="use-the-event-notification-callback"></a><span data-ttu-id="abcf9-104">Verwenden des Ereignis Benachrichtigungs Rückrufs</span><span class="sxs-lookup"><span data-stu-id="abcf9-104">Use the Event Notification Callback</span></span>

<span data-ttu-id="abcf9-105">Im folgenden Verfahren werden die Schritte beschrieben, die der Client zum Empfangen von Änderungs Benachrichtigungs Meldungen vom RTM- \_ Ereignis Rückruf verwenden soll \_ .</span><span class="sxs-lookup"><span data-stu-id="abcf9-105">The following procedure outlines the steps the client should use to receive change notification messages from the RTM\_EVENT\_CALLBACK.</span></span> <span data-ttu-id="abcf9-106">Der folgende Beispielcode zeigt, wie die Prozedur implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="abcf9-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="abcf9-107">**Abrufen der Änderungs Benachrichtigungs Meldungen**</span><span class="sxs-lookup"><span data-stu-id="abcf9-107">**How to retrieve the change notification messages**</span></span>

1.  <span data-ttu-id="abcf9-108">Rufen Sie [**rtmgetchangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) auf, um einen Satz von Änderungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="abcf9-108">Call [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) to retrieve a set of changes.</span></span>
2.  <span data-ttu-id="abcf9-109">Verarbeiten Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="abcf9-109">Process the changes.</span></span>
3.  <span data-ttu-id="abcf9-110">Geben Sie die Ziele mithilfe von [**rtmreleasechangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)frei.</span><span class="sxs-lookup"><span data-stu-id="abcf9-110">Release the destinations using [**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests).</span></span>
4.  <span data-ttu-id="abcf9-111">Wiederholen Sie die Schritte 1, 2 und 3, bis [**rtmgetchangeddests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) Fehler \_ ohne \_ Weitere Elemente zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="abcf9-111">Repeat steps 1, 2, and 3 until [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="abcf9-112">Der folgende Beispielcode zeigt, wie ein vom Routing Tabellen-Manager empfangener [**RTM- \_ Ereignis \_ Rückruf**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) Rückruf verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="abcf9-112">The following sample code shows how to process an [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback received from the routing table manager.</span></span>


```C++
#include <windows.h>
#include <ras.h>

// Macro to allocate an RTM_DEST_INFO on the stack
#define ALLOC_RTM_DEST_INFO(NumViews, NumInfos)
        (PRTM_DEST_INFO) _alloca(RTM_SIZE_OF_DEST_INFO(NumViews) * NumInfos)

// Routing table manager entity event callback

DWORD
EntityEventCallback (
    IN      RTM_ENTITY_HANDLE               RtmRegHandle,
    IN      RTM_EVENT_TYPE                  EventType,
    IN      PVOID                           Context1,
    IN      PVOID                           Context2
    )
{
    RTM_ENTITY_HANDLE EntityHandle;
    PENTITY_CHARS     EntityChars;
    PRTM_ENTITY_INFO  EntityInfo;
    RTM_NOTIFY_HANDLE NotifyHandle;
    PRTM_DEST_INFO    DestInfos;
    ULONG             DestInfoSize;
    UINT              NumDests;
    UINT              NumViews, i;
    UINT              MaxHandles;
    RTM_ROUTE_HANDLE  RouteHandle;
    PRTM_ROUTE_INFO   RoutePointer;
    DWORD             ChangeFlags;
    DWORD             Status;

    Print("\nEvent callback called for %p :", RtmRegHandle);

    Print("\n\tEntity Event = ");

    Status = ERROR_NOT_SUPPORTED;

    switch (EventType)
    {
    case RTM_ENTITY_REGISTERED:

                // Get the handle and information of the entity that registered
        
        EntityHandle = (RTM_ENTITY_HANDLE) Context1;
        EntityInfo   = (PRTM_ENTITY_INFO)  Context2;

        Print("Registration\n\tEntity Handle = %p\n\tEntity IdInst = %p\n\n",
              EntityHandle,
              EntityInfo->EntityId);

                // Do something if you are interested in the entity
                ;

        Status = NO_ERROR;
        break;

    case RTM_ENTITY_DEREGISTERED:

                // Get the handle and information of the entity that deregistered
        
        EntityHandle = (RTM_ENTITY_HANDLE) Context1;
        EntityInfo   = (PRTM_ENTITY_INFO)  Context2;

        Print("Deregistration\n\tEntity Handle = %p\n\tEntity IdInst = %p\n\n",
               EntityHandle,
              EntityInfo->EntityId);

                // Do something if you are interested in the entity
                ;

        Status = NO_ERROR;
        break;

    case RTM_CHANGE_NOTIFICATION:

        // Get the notification registration on which changes exist and
        // context supplied in RtmRegisterForChangeNotification
        
        NotifyHandle = (RTM_NOTIFY_HANDLE) Context1;

        NotifyContext = (PVOID) Context2; // Unused

        Print("Changes Available\n\tNotify Handle = %p\n\tNotify Context = %p\n\n",
              NotifyHandle,
              NotifyContext);

        MaxHandles = RegnProfile.MaxHandlesInEnum;

        NumViews = RegnProfile.NumberOfViews;

        DestInfoSize = RTM_SIZE_OF_DEST_INFO(NumViews);

                // Get all changes to destinations
        
        DestInfos = ALLOC_RTM_DEST_INFO(NumViews, MaxHandles);

        do
        {
            // Try to get as many as possible in one routing table managercall
            NumDests = MaxHandles;

            Status = RtmGetChangedDests(RtmRegHandle,
                                        NotifyHandle,
                                        &NumDests,
                                        DestInfos);

            ASSERT((Status == NO_ERROR) || (Status == ERROR_NO_MORE_ITEMS));

            DestInfo = (PRTM_DEST_INFO) DestInfos;

            for (i = 0; i < NumDests; i++)
            {
                                // Process the current destination information
                
                // Assuming you asked for unicast view information,
                ASSERT(DestInfo->ViewInfo[0].ViewId == RTM_VIEW_ID_UCAST);

                // Get the best unicast route for the destination.
                NewBestRoute = DestInfo.ViewInfo[0].Route;

                // Do whatever you want with above route
                ...

                // Move to the next changed one
                DestInfo = (PRTM_DEST_INFO) ((PUCHAR)DestInfo + DestInfoSize);
            }

            RtmReleaseChangedDests(RtmRegHandle,
                                   NotifyHandle,
                                   NumDests,
                                   DestInfos);
        }
        while (NumDests > 0);

        Status = NO_ERROR;
        break;

    case RTM_ROUTE_EXPIRED:

                // Get handle and a direct pointer to the route whose timer expired
        
        RouteHandle = (RTM_ROUTE_HANDLE) Context1;

        RoutePointer = (PRTM_ROUTE_INFO) Context2;

        Print("Route Aged Out\n\tRoute Handle = %p\n\tRoute Pointer = %p\n\n",
               RouteHandle,
              RoutePointer);

        // To just let the routing table manager delete the route, return ERROR_NOT_SUPPORTED
        // If you return any other value, the routing table manager assumes that you have
        // handled the time-out condition in callback for route timer expiration
        
        // Suppose we just want to update the metric and leave the route 

        Status = RtmLockRoute(RtmRegHandle,
                              RouteHandle,
                              TRUE,
                              TRUE,
                              NULL);

        // Check(Status, 46);

        if (Status == NO_ERROR)
        {
            // Set the metric to indicate that it is unreachable
            RoutePointer->PrefInfo.Metric = METRIC_UNREACHABLE;

            Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                             RouteHandle,
                                             INFINITE,        // To stay forever
                                             NULL,
                                             0,
                                             NULL,
                                             &ChangeFlags);
            ASSERT(Status == NO_ERROR);
        }

        // If ERROR_NOT_SUPPORTED not returned, release the handle
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);

        Status = NO_ERROR;
        break;
    }

    return Status;
}
```



 

 




