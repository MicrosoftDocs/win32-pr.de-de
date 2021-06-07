---
description: Im folgenden Beispiel wird eine Timerroutine erstellt, die von einem Thread aus einer Timerwarteschlange nach einer Verzögerung von 10 Sekunden ausgeführt wird.
ms.assetid: 779156fe-f825-452b-acbe-e2cb189e24d2
title: Verwenden von Timerwarteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d084a03eb25301f94361c1e7ca6b76dd9fee269
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549932"
---
# <a name="using-timer-queues"></a>Verwenden von Timerwarteschlangen

Im folgenden Beispiel wird eine Timerroutine erstellt, die von einem Thread aus einer [Timerwarteschlange](timer-queues.md) nach einer Verzögerung von 10 Sekunden ausgeführt wird. Zunächst verwendet der Code die [**CreateEvent-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-createeventa) um ein Ereignisobjekt zu erstellen, das signalisiert wird, wenn der Timerwarteschlangenthread abgeschlossen ist. Anschließend wird mithilfe der [**Funktionen CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) bzw. [**CreateTimerQueueTimer eine Timerwarteschlange**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) und ein Timer-Queue-Timer erstellt. Der Code verwendet die [**WaitForSingleObject-Funktion,**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) um zu bestimmen, wann die Timerroutine abgeschlossen wurde. Abschließend ruft der Code [**DeleteTimerQueue auf, um**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue) die Bereinigung zu bereinigen.

Weitere Informationen zur Timerroutine finden Sie unter [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).


```C++
#include <windows.h>
#include <stdio.h>

HANDLE gDoneEvent;

VOID CALLBACK TimerRoutine(PVOID lpParam, BOOLEAN TimerOrWaitFired)
{
    if (lpParam == NULL)
    {
        printf("TimerRoutine lpParam is NULL\n");
    }
    else
    {
        // lpParam points to the argument; in this case it is an int

        printf("Timer routine called. Parameter is %d.\n", 
                *(int*)lpParam);
        if(TimerOrWaitFired)
        {
            printf("The wait timed out.\n");
        }
        else
        {
            printf("The wait event was signaled.\n");
        }
    }

    SetEvent(gDoneEvent);
}

int main()
{
    HANDLE hTimer = NULL;
    HANDLE hTimerQueue = NULL;
    int arg = 123;

    // Use an event object to track the TimerRoutine execution
    gDoneEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == gDoneEvent)
    {
        printf("CreateEvent failed (%d)\n", GetLastError());
        return 1;
    }

    // Create the timer queue.
    hTimerQueue = CreateTimerQueue();
    if (NULL == hTimerQueue)
    {
        printf("CreateTimerQueue failed (%d)\n", GetLastError());
        return 2;
    }

    // Set a timer to call the timer routine in 10 seconds.
    if (!CreateTimerQueueTimer( &hTimer, hTimerQueue, 
            (WAITORTIMERCALLBACK)TimerRoutine, &arg , 10000, 0, 0))
    {
        printf("CreateTimerQueueTimer failed (%d)\n", GetLastError());
        return 3;
    }

    // TODO: Do other useful work here 

    printf("Call timer routine in 10 seconds...\n");

    // Wait for the timer-queue thread to complete using an event 
    // object. The thread will signal the event at that time.

    if (WaitForSingleObject(gDoneEvent, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());

    CloseHandle(gDoneEvent);

    // Delete all timers in the timer queue.
    if (!DeleteTimerQueue(hTimerQueue))
        printf("DeleteTimerQueue failed (%d)\n", GetLastError());

    return 0;
}
```



 

 
