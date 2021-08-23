---
description: Das LSA stellt Funktionen bereit, die Sie verwenden können, um Benachrichtigungen zu erhalten, wenn eine Änderung der Richtlinie auf dem lokalen System vorliegt.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Empfangen von Richtlinienänderungsereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1fc2328d0467dcfe5b6f85b9b8384cf4c8271d35fcda106a61ae5bb068f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005048"
---
# <a name="receiving-policy-change-events"></a>Empfangen von Richtlinienänderungsereignissen

Das LSA stellt Funktionen bereit, die Sie verwenden können, um Benachrichtigungen zu erhalten, wenn eine Änderung der Richtlinie auf dem lokalen System vorliegt.

Um Benachrichtigungen zu erhalten, erstellen Sie ein neues Ereignisobjekt, indem Sie die [**CreateEvent-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) aufrufen und dann die [**LsaRegisterPolicyChangeNotification-Funktion**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) aufrufen. Ihre Anwendung kann dann eine Wait-Funktion wie [**WaitForSingleObject,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)oder [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) aufrufen, um auf das Eintreten des Ereignisses zu warten. Die Wait-Funktion gibt zurück, wenn das Ereignis eintritt oder der Time out-Zeitraum abläuft. In der Regel werden Benachrichtigungsereignisse in Multithreadanwendungen verwendet, in denen ein Thread auf ein Ereignis wartet, während andere Threads die Verarbeitung fortsetzen.

Wenn Ihre Anwendung keine Benachrichtigungen mehr empfangen muss, sollte sie [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) und dann [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufrufen, um das Ereignisobjekthandle frei zu machen.

Das folgende Beispiel zeigt, wie eine Singlethreadanwendung Benachrichtigungsereignisse empfangen kann, wenn sich die Überwachungsrichtlinie des Systems ändert.


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



Weitere Informationen zu Ereignisobjekten, Wartefunktionen und Synchronisierung finden Sie unter [Verwenden von Ereignisobjekten.](/windows/desktop/Sync/using-event-objects)

 

 
