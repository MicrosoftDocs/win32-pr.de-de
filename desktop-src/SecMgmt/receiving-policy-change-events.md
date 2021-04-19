---
description: Die LSA stellt Funktionen bereit, die Sie verwenden können, um Benachrichtigungen zu empfangen, wenn eine Änderung der Richtlinie auf dem lokalen System vorliegt.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Empfangen von Richtlinien Änderungs Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345036"
---
# <a name="receiving-policy-change-events"></a><span data-ttu-id="62cb3-103">Empfangen von Richtlinien Änderungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="62cb3-103">Receiving Policy Change Events</span></span>

<span data-ttu-id="62cb3-104">Die LSA stellt Funktionen bereit, die Sie verwenden können, um Benachrichtigungen zu empfangen, wenn eine Änderung der Richtlinie auf dem lokalen System vorliegt.</span><span class="sxs-lookup"><span data-stu-id="62cb3-104">The LSA provides functions you can use to receive notification when there is a change in policy on the local system.</span></span>

<span data-ttu-id="62cb3-105">Um eine Benachrichtigung zu erhalten, erstellen Sie ein neues Ereignis Objekt, indem Sie die [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) -Funktion aufrufen, und rufen Sie dann die [**lsaregisterpolicychangenotifi-**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="62cb3-105">To receive notification, create a new event object by calling the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function, and then call the [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) function.</span></span> <span data-ttu-id="62cb3-106">Die Anwendung kann dann eine wait-Funktion aufrufen, z. b. " [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)", " [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)" oder " [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) ", um auf das Ereignis zu warten.</span><span class="sxs-lookup"><span data-stu-id="62cb3-106">Your application can then call a wait function such as [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), or [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the event to occur.</span></span> <span data-ttu-id="62cb3-107">Die wait-Funktion gibt zurück, wenn das Ereignis auftritt oder wenn der Timeout Zeitraum abläuft.</span><span class="sxs-lookup"><span data-stu-id="62cb3-107">The wait function returns when the event occurs, or when the time-out period expires.</span></span> <span data-ttu-id="62cb3-108">In der Regel werden Benachrichtigungs Ereignisse in Multithreadanwendungen verwendet, in denen ein Thread auf ein Ereignis wartet, während andere Threads die Verarbeitung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="62cb3-108">Typically, notification events are used in multithreaded applications, in which one thread waits for an event, while other threads continue processing.</span></span>

<span data-ttu-id="62cb3-109">Wenn Ihre Anwendung keine Benachrichtigungen mehr empfangen muss, sollte Sie [**lsaunregisterpolicychangenotifizierung**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) aufrufen und dann [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufrufen, um das Ereignis Objekt Handle freizugeben.</span><span class="sxs-lookup"><span data-stu-id="62cb3-109">When your application no longer needs to receive notifications, it should call [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) and then call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to free the event object handle.</span></span>

<span data-ttu-id="62cb3-110">Das folgende Beispiel zeigt, wie eine Single Thread-Anwendung Benachrichtigungs Ereignisse empfangen kann, wenn sich die Überwachungsrichtlinie des Systems ändert.</span><span class="sxs-lookup"><span data-stu-id="62cb3-110">The following example shows how a single-threaded application can receive notification events when the system's auditing policy changes.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void WaitForPolicyChanges()
{
  HANDLE hEvent;
  NTSTATUS ntsResult;
  DWORD dwResult;

  // Create an event object.
  hEvent = CreateEvent( 
    NULL,  // child processes cannot inherit 
    FALSE, // automatically reset event
    FALSE, // start as a nonsignaled event
    NULL   // do not need a name
  );

  // Check that the event was created.
  if (hEvent == NULL) 
  {
    wprintf(L"Event object creation failed: %d\n",GetLastError());
    return;
  }
  // Register to receive auditing policy change notifications.
  ntsResult = LsaRegisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );
  if (STATUS_SUCCESS != ntsResult)
  {
    wprintf(L"LsaRegisterPolicyChangeNotification failed.\n");
    CloseHandle(hEvent);
    return;
  }

  // Wait for the event to be triggered.
  dwResult = WaitForSingleObject( 
    hEvent, // handle to the event object
    300000  // time-out interval, in milliseconds
  );

  // The wait function returned.
  if (dwResult == WAIT_OBJECT_0)
  {  // received the notification signal
    wprintf(L"Notification received.\n");
  } 
  else 
  {  // received a time-out or error
    wprintf(L"Notification was not received.\n");
  }
  // Unregister for notification.
  LsaUnregisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );

  // Free the event handle.
  CloseHandle(hEvent);
}
```



<span data-ttu-id="62cb3-111">Weitere Informationen zu Ereignis Objekten, Wait-Funktionen und der Synchronisierung finden [Sie unter Verwenden von Ereignis Objekten](/windows/desktop/Sync/using-event-objects).</span><span class="sxs-lookup"><span data-stu-id="62cb3-111">For more information about event objects, wait functions, and synchronization, see [Using Event Objects](/windows/desktop/Sync/using-event-objects).</span></span>

 

 
