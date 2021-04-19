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
# <a name="receiving-policy-change-events"></a>Empfangen von Richtlinien Änderungs Ereignissen

Die LSA stellt Funktionen bereit, die Sie verwenden können, um Benachrichtigungen zu empfangen, wenn eine Änderung der Richtlinie auf dem lokalen System vorliegt.

Um eine Benachrichtigung zu erhalten, erstellen Sie ein neues Ereignis Objekt, indem Sie die [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) -Funktion aufrufen, und rufen Sie dann die [**lsaregisterpolicychangenotifi-**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) Funktion auf. Die Anwendung kann dann eine wait-Funktion aufrufen, z. b. " [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)", " [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)" oder " [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) ", um auf das Ereignis zu warten. Die wait-Funktion gibt zurück, wenn das Ereignis auftritt oder wenn der Timeout Zeitraum abläuft. In der Regel werden Benachrichtigungs Ereignisse in Multithreadanwendungen verwendet, in denen ein Thread auf ein Ereignis wartet, während andere Threads die Verarbeitung fortsetzen.

Wenn Ihre Anwendung keine Benachrichtigungen mehr empfangen muss, sollte Sie [**lsaunregisterpolicychangenotifizierung**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) aufrufen und dann [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufrufen, um das Ereignis Objekt Handle freizugeben.

Das folgende Beispiel zeigt, wie eine Single Thread-Anwendung Benachrichtigungs Ereignisse empfangen kann, wenn sich die Überwachungsrichtlinie des Systems ändert.


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



Weitere Informationen zu Ereignis Objekten, Wait-Funktionen und der Synchronisierung finden [Sie unter Verwenden von Ereignis Objekten](/windows/desktop/Sync/using-event-objects).

 

 
