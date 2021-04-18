---
description: Im folgenden Beispiel wird ein Timer erstellt, der nach einer Verzögerung von 10 Sekunden signalisiert wird.
ms.assetid: 3c84c2ad-6bac-4f14-a633-51d4529314af
title: Verwenden von wanutzbaren Timer-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a23b0d9f6ab74df325be81eb9236bffe6a0c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352622"
---
# <a name="using-waitable-timer-objects"></a><span data-ttu-id="a411a-103">Verwenden von wanutzbaren Timer-Objekten</span><span class="sxs-lookup"><span data-stu-id="a411a-103">Using Waitable Timer Objects</span></span>

<span data-ttu-id="a411a-104">Im folgenden Beispiel wird ein Timer erstellt, der nach einer Verzögerung von 10 Sekunden signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a411a-104">The following example creates a timer that will be signaled after a 10 second delay.</span></span> <span data-ttu-id="a411a-105">Zuerst verwendet der Code die Funktion " [**kreatewaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) ", um ein [wanutzbares](waitable-timer-objects.md)Zeit Geber Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a411a-105">First, the code uses the [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function to create a [waitable timer object](waitable-timer-objects.md).</span></span> <span data-ttu-id="a411a-106">Anschließend wird der Timer mithilfe der [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) -Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a411a-106">Then it uses the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function to set the timer.</span></span> <span data-ttu-id="a411a-107">Der Code verwendet die [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) -Funktion, um zu bestimmen, wann der Timer signalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a411a-107">The code uses the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function to determine when the timer has been signaled.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

int main()
{
    HANDLE hTimer = NULL;
    LARGE_INTEGER liDueTime;

    liDueTime.QuadPart = -100000000LL;

    // Create an unnamed waitable timer.
    hTimer = CreateWaitableTimer(NULL, TRUE, NULL);
    if (NULL == hTimer)
    {
        printf("CreateWaitableTimer failed (%d)\n", GetLastError());
        return 1;
    }

    printf("Waiting for 10 seconds...\n");

    // Set a timer to wait for 10 seconds.
    if (!SetWaitableTimer(hTimer, &liDueTime, 0, NULL, NULL, 0))
    {
        printf("SetWaitableTimer failed (%d)\n", GetLastError());
        return 2;
    }

    // Wait for the timer.

    if (WaitForSingleObject(hTimer, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());
    else printf("Timer was signaled.\n");

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="a411a-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a411a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a411a-109">Verwenden von wanutzbaren Timern mit einem asynchronen Prozedur aufrutor</span><span class="sxs-lookup"><span data-stu-id="a411a-109">Using Waitable Timers with an Asynchronous Procedure Call</span></span>](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
