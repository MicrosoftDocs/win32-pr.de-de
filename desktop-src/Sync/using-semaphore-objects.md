---
description: Im folgenden Beispiel wird ein Semaphor-Objekt verwendet, um die Anzahl der Threads einzuschränken, die eine bestimmte Aufgabe ausführen können.
ms.assetid: 24a5c13c-573a-4fc2-ac19-98188c9eb68a
title: Verwenden von Semaphore-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded28014c7e832ab5bdc96d724d57e314d0cc857
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106371957"
---
# <a name="using-semaphore-objects"></a><span data-ttu-id="3087b-103">Verwenden von Semaphore-Objekten</span><span class="sxs-lookup"><span data-stu-id="3087b-103">Using Semaphore Objects</span></span>

<span data-ttu-id="3087b-104">Im folgenden Beispiel wird ein [Semaphor-Objekt](semaphore-objects.md) verwendet, um die Anzahl der Threads einzuschränken, die eine bestimmte Aufgabe ausführen können.</span><span class="sxs-lookup"><span data-stu-id="3087b-104">The following example uses a [semaphore object](semaphore-objects.md) to limit the number of threads that can perform a particular task.</span></span> <span data-ttu-id="3087b-105">Zuerst wird die Funktion " [**foratesemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) " verwendet, um das Semaphor zu erstellen, und um die anfängliche und die maximale Anzahl anzugeben. Anschließend wird die Funktion mit der Funktion " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " erstellt.</span><span class="sxs-lookup"><span data-stu-id="3087b-105">First, it uses the [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) function to create the semaphore and to specify initial and maximum counts, then it uses the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create the threads.</span></span>

<span data-ttu-id="3087b-106">Bevor ein Thread versucht, die Aufgabe auszuführen, verwendet er die [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion, um zu bestimmen, ob die aktuelle Anzahl des Semaphors dies zulässt.</span><span class="sxs-lookup"><span data-stu-id="3087b-106">Before a thread attempts to perform the task, it uses the [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function to determine whether the semaphore's current count permits it to do so.</span></span> <span data-ttu-id="3087b-107">Der Timeout Parameter der wait-Funktion ist auf 0 (null) festgelegt, sodass die Funktion sofort zurückgegeben wird, wenn sich das Semaphor im nicht signalisierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="3087b-107">The wait function's time-out parameter is set to zero, so the function returns immediately if the semaphore is in the nonsignaled state.</span></span> <span data-ttu-id="3087b-108">**WaitForSingleObject** Dekremente die Anzahl der Semaphore um 1.</span><span class="sxs-lookup"><span data-stu-id="3087b-108">**WaitForSingleObject** decrements the semaphore's count by one.</span></span>

<span data-ttu-id="3087b-109">Wenn ein Thread die Aufgabe abschließt, verwendet er die [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) -Funktion, um die Anzahl der Semaphore zu erhöhen, sodass ein anderer wartender Thread die Aufgabe ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="3087b-109">When a thread completes the task, it uses the [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) function to increment the semaphore's count, thus enabling another waiting thread to perform the task.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define MAX_SEM_COUNT 10
#define THREADCOUNT 12

HANDLE ghSemaphore;

DWORD WINAPI ThreadProc( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a semaphore with initial and max counts of MAX_SEM_COUNT

    ghSemaphore = CreateSemaphore( 
        NULL,           // default security attributes
        MAX_SEM_COUNT,  // initial count
        MAX_SEM_COUNT,  // maximum count
        NULL);          // unnamed semaphore

    if (ghSemaphore == NULL) 
    {
        printf("CreateSemaphore error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) ThreadProc, 
                     NULL,       // no thread function arguments
                     0,          // default creation flags
                     &ThreadID); // receive thread identifier

        if( aThread[i] == NULL )
        {
            printf("CreateThread error: %d\n", GetLastError());
            return 1;
        }
    }

    // Wait for all threads to terminate

    WaitForMultipleObjects(THREADCOUNT, aThread, TRUE, INFINITE);

    // Close thread and semaphore handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghSemaphore);

    return 0;
}

DWORD WINAPI ThreadProc( LPVOID lpParam )
{

    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult; 
    BOOL bContinue=TRUE;

    while(bContinue)
    {
        // Try to enter the semaphore gate.

        dwWaitResult = WaitForSingleObject( 
            ghSemaphore,   // handle to semaphore
            0L);           // zero-second time-out interval

        switch (dwWaitResult) 
        { 
            // The semaphore object was signaled.
            case WAIT_OBJECT_0: 
                // TODO: Perform task
                printf("Thread %d: wait succeeded\n", GetCurrentThreadId());
                bContinue=FALSE;            

                // Simulate thread spending time on task
                Sleep(5);

                // Release the semaphore when task is finished

                if (!ReleaseSemaphore( 
                        ghSemaphore,  // handle to semaphore
                        1,            // increase count by one
                        NULL) )       // not interested in previous count
                {
                    printf("ReleaseSemaphore error: %d\n", GetLastError());
                }
                break; 

            // The semaphore was nonsignaled, so a time-out occurred.
            case WAIT_TIMEOUT: 
                printf("Thread %d: wait timed out\n", GetCurrentThreadId());
                break; 
        }
    }
    return TRUE;
}
```



 

 
