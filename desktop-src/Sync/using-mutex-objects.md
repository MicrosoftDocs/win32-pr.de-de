---
description: Sie können ein Mutex-Objekt verwenden, um eine freigegebene Ressource vor gleichzeitigem Zugriff durch mehrere Threads oder Prozesse zu schützen.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Verwenden von Mutex-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd68f41319125613e8569e7b343c0b1601a7735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348637"
---
# <a name="using-mutex-objects"></a><span data-ttu-id="e3639-103">Verwenden von Mutex-Objekten</span><span class="sxs-lookup"><span data-stu-id="e3639-103">Using Mutex Objects</span></span>

<span data-ttu-id="e3639-104">Sie können ein [Mutex-Objekt](mutex-objects.md) verwenden, um eine freigegebene Ressource vor gleichzeitigem Zugriff durch mehrere Threads oder Prozesse zu schützen.</span><span class="sxs-lookup"><span data-stu-id="e3639-104">You can use a [mutex object](mutex-objects.md) to protect a shared resource from simultaneous access by multiple threads or processes.</span></span> <span data-ttu-id="e3639-105">Jeder Thread muss auf den Besitz des Mutex warten, bevor er den Code ausführen kann, der auf die freigegebene Ressource zugreift.</span><span class="sxs-lookup"><span data-stu-id="e3639-105">Each thread must wait for ownership of the mutex before it can execute the code that accesses the shared resource.</span></span> <span data-ttu-id="e3639-106">Wenn z. b. mehrere Threads den Zugriff auf eine Datenbank gemeinsam nutzen, können die Threads ein Mutex-Objekt verwenden, um jeweils nur einen Thread zum Schreiben in die Datenbank zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="e3639-106">For example, if several threads share access to a database, the threads can use a mutex object to permit only one thread at a time to write to the database.</span></span>

<span data-ttu-id="e3639-107">Im folgenden Beispiel wird die Funktion " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) " verwendet, um ein Mutex-Objekt und die Funktion " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " zum Erstellen von Arbeitsthreads zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e3639-107">The following example uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create a mutex object and the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create worker threads.</span></span>

<span data-ttu-id="e3639-108">Wenn ein Thread dieses Prozesses in die Datenbank schreibt, fordert er zuerst den Besitz des Mutex mithilfe der [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="e3639-108">When a thread of this process writes to the database, it first requests ownership of the mutex using the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function.</span></span> <span data-ttu-id="e3639-109">Wenn der Thread in den Besitz des Mutex gelangt, schreibt er in die Datenbank und gibt den Besitz des Mutex mithilfe der [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) -Funktion frei.</span><span class="sxs-lookup"><span data-stu-id="e3639-109">If the thread obtains ownership of the mutex, it writes to the database and then releases its ownership of the mutex using the [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) function.</span></span>

<span data-ttu-id="e3639-110">Dieses Beispiel verwendet die strukturierte Ausnahmebehandlung, um sicherzustellen, dass der Thread das Mutex-Objekt ordnungsgemäß freigibt.</span><span class="sxs-lookup"><span data-stu-id="e3639-110">This example uses structured exception handling to ensure that the thread properly releases the mutex object.</span></span> <span data-ttu-id="e3639-111">Der letzte Codeblock wird ausgeführt, unabhängig davon, wie der **\_ \_ try** -Block beendet wird (es sei denn, der **\_ \_ try** -Block enthält einen Aufrufen der [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) -Funktion). **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3639-111">The **\_\_finally** block of code is executed no matter how the **\_\_try** block terminates (unless the **\_\_try** block includes a call to the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function).</span></span> <span data-ttu-id="e3639-112">Dadurch wird verhindert, dass das Mutex-Objekt versehentlich abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="e3639-112">This prevents the mutex object from being abandoned inadvertently.</span></span>

<span data-ttu-id="e3639-113">Wenn ein Mutex abgebrochen wird, hat der Thread, der im Besitz des Mutex war, ihn vor dem Beenden nicht ordnungsgemäß freigegeben.</span><span class="sxs-lookup"><span data-stu-id="e3639-113">If a mutex is abandoned, the thread that owned the mutex did not properly release it before terminating.</span></span> <span data-ttu-id="e3639-114">In diesem Fall ist der Status der freigegebenen Ressource unbestimmt, und die Verwendung des Mutex kann einen potenziell schwerwiegenden Fehler verbergen.</span><span class="sxs-lookup"><span data-stu-id="e3639-114">In this case, the status of the shared resource is indeterminate, and continuing to use the mutex can obscure a potentially serious error.</span></span> <span data-ttu-id="e3639-115">Einige Anwendungen versuchen möglicherweise, die Ressource in einem konsistenten Zustand wiederherzustellen. Dieses Beispiel gibt einfach einen Fehler zurück und beendet die Verwendung des Mutex.</span><span class="sxs-lookup"><span data-stu-id="e3639-115">Some applications might attempt to restore the resource to a consistent state; this example simply returns an error and stops using the mutex.</span></span> <span data-ttu-id="e3639-116">Weitere Informationen finden Sie unter [Mutex Objects](mutex-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e3639-116">For more information, see [Mutex Objects](mutex-objects.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 2

HANDLE ghMutex; 

DWORD WINAPI WriteToDatabase( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a mutex with no initial owner

    ghMutex = CreateMutex( 
        NULL,              // default security attributes
        FALSE,             // initially not owned
        NULL);             // unnamed mutex

    if (ghMutex == NULL) 
    {
        printf("CreateMutex error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) WriteToDatabase, 
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

    // Close thread and mutex handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghMutex);

    return 0;
}

DWORD WINAPI WriteToDatabase( LPVOID lpParam )
{ 
    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwCount=0, dwWaitResult; 

    // Request ownership of mutex.

    while( dwCount < 20 )
    { 
        dwWaitResult = WaitForSingleObject( 
            ghMutex,    // handle to mutex
            INFINITE);  // no time-out interval
 
        switch (dwWaitResult) 
        {
            // The thread got ownership of the mutex
            case WAIT_OBJECT_0: 
                __try { 
                    // TODO: Write to the database
                    printf("Thread %d writing to database...\n", 
                            GetCurrentThreadId());
                    dwCount++;
                } 

                __finally { 
                    // Release ownership of the mutex object
                    if (! ReleaseMutex(ghMutex)) 
                    { 
                        // Handle error.
                    } 
                } 
                break; 

            // The thread got ownership of an abandoned mutex
            // The database is in an indeterminate state
            case WAIT_ABANDONED: 
                return FALSE; 
        }
    }
    return TRUE; 
}
```



 

 
