---
description: Die Funktion "kreatethread" erstellt einen neuen Thread für einen Prozess.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Erstellen von Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545088779bdaff665a8079296014535ab244e821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349853"
---
# <a name="creating-threads"></a><span data-ttu-id="a3eda-103">Erstellen von Threads</span><span class="sxs-lookup"><span data-stu-id="a3eda-103">Creating Threads</span></span>

<span data-ttu-id="a3eda-104">Die Funktion " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " erstellt einen neuen Thread für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="a3eda-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="a3eda-105">Der Erstellungs Thread muss die Startadresse des Codes angeben, den der neue Thread ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="a3eda-105">The creating thread must specify the starting address of the code that the new thread is to execute.</span></span> <span data-ttu-id="a3eda-106">Die Startadresse ist in der Regel der Name einer im Programmcode definierten Funktion (Weitere Informationen finden Sie unter [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="a3eda-106">Typically, the starting address is the name of a function defined in the program code (for more information, see [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span></span> <span data-ttu-id="a3eda-107">Diese Funktion nimmt einen einzelnen Parameter an und gibt einen **DWORD** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3eda-107">This function takes a single parameter and returns a **DWORD** value.</span></span> <span data-ttu-id="a3eda-108">Ein Prozess kann mehrere Threads gleichzeitig dieselbe Funktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3eda-108">A process can have multiple threads simultaneously executing the same function.</span></span>

<span data-ttu-id="a3eda-109">Im folgenden finden Sie ein einfaches Beispiel, das veranschaulicht, wie ein neuer Thread erstellt wird, der die lokal definierte Funktion ausführt `MyThreadFunction` .</span><span class="sxs-lookup"><span data-stu-id="a3eda-109">The following is a simple example that demonstrates how to create a new thread that executes the locally defined function, `MyThreadFunction`.</span></span>

<span data-ttu-id="a3eda-110">Der aufrufende Thread verwendet die [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) -Funktion, um beizubehalten, bis alle Arbeitsthreads beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a3eda-110">The calling thread uses the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to persist until all worker threads have terminated.</span></span> <span data-ttu-id="a3eda-111">Der Aufruf Thread blockiert, während er wartet. um die Verarbeitung fortzusetzen, verwendet ein aufrufenden Thread [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) und wartet, bis jeder Arbeits Thread sein warte Objekt signalisiert.</span><span class="sxs-lookup"><span data-stu-id="a3eda-111">The calling thread blocks while it is waiting; to continue processing, a calling thread would use [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) and wait for each worker thread to signal its wait object.</span></span> <span data-ttu-id="a3eda-112">Beachten Sie Folgendes: Wenn Sie das Handle für einen Arbeits Thread vor dem Beenden schließen, wird der Arbeits Thread dadurch nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="a3eda-112">Note that if you were to close the handle to a worker thread before it terminated, this does not terminate the worker thread.</span></span> <span data-ttu-id="a3eda-113">Allerdings steht das Handle nicht für die Verwendung in nachfolgenden Funktionsaufrufen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a3eda-113">However, the handle will be unavailable for use in subsequent function calls.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

#define MAX_THREADS 3
#define BUF_SIZE 255

DWORD WINAPI MyThreadFunction( LPVOID lpParam );
void ErrorHandler(LPTSTR lpszFunction);

// Sample custom data structure for threads to use.
// This is passed by void pointer so it can be any data type
// that can be passed using a single void pointer (LPVOID).
typedef struct MyData {
    int val1;
    int val2;
} MYDATA, *PMYDATA;


int _tmain()
{
    PMYDATA pDataArray[MAX_THREADS];
    DWORD   dwThreadIdArray[MAX_THREADS];
    HANDLE  hThreadArray[MAX_THREADS]; 

    // Create MAX_THREADS worker threads.

    for( int i=0; i<MAX_THREADS; i++ )
    {
        // Allocate memory for thread data.

        pDataArray[i] = (PMYDATA) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY,
                sizeof(MYDATA));

        if( pDataArray[i] == NULL )
        {
           // If the array allocation fails, the system is out of memory
           // so there is no point in trying to print an error message.
           // Just terminate execution.
            ExitProcess(2);
        }

        // Generate unique data for each thread to work with.

        pDataArray[i]->val1 = i;
        pDataArray[i]->val2 = i+100;

        // Create the thread to begin execution on its own.

        hThreadArray[i] = CreateThread( 
            NULL,                   // default security attributes
            0,                      // use default stack size  
            MyThreadFunction,       // thread function name
            pDataArray[i],          // argument to thread function 
            0,                      // use default creation flags 
            &dwThreadIdArray[i]);   // returns the thread identifier 


        // Check the return value for success.
        // If CreateThread fails, terminate execution. 
        // This will automatically clean up threads and memory. 

        if (hThreadArray[i] == NULL) 
        {
           ErrorHandler(TEXT("CreateThread"));
           ExitProcess(3);
        }
    } // End of main thread creation loop.

    // Wait until all threads have terminated.

    WaitForMultipleObjects(MAX_THREADS, hThreadArray, TRUE, INFINITE);

    // Close all thread handles and free memory allocations.

    for(int i=0; i<MAX_THREADS; i++)
    {
        CloseHandle(hThreadArray[i]);
        if(pDataArray[i] != NULL)
        {
            HeapFree(GetProcessHeap(), 0, pDataArray[i]);
            pDataArray[i] = NULL;    // Ensure address is not reused.
        }
    }

    return 0;
}


DWORD WINAPI MyThreadFunction( LPVOID lpParam ) 
{ 
    HANDLE hStdout;
    PMYDATA pDataArray;

    TCHAR msgBuf[BUF_SIZE];
    size_t cchStringSize;
    DWORD dwChars;

    // Make sure there is a console to receive output results. 

    hStdout = GetStdHandle(STD_OUTPUT_HANDLE);
    if( hStdout == INVALID_HANDLE_VALUE )
        return 1;

    // Cast the parameter to the correct data type.
    // The pointer is known to be valid because 
    // it was checked for NULL before the thread was created.
 
    pDataArray = (PMYDATA)lpParam;

    // Print the parameter values using thread-safe functions.

    StringCchPrintf(msgBuf, BUF_SIZE, TEXT("Parameters = %d, %d\n"), 
        pDataArray->val1, pDataArray->val2); 
    StringCchLength(msgBuf, BUF_SIZE, &cchStringSize);
    WriteConsole(hStdout, msgBuf, (DWORD)cchStringSize, &dwChars, NULL);

    return 0; 
} 



void ErrorHandler(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code.

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message.

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR) lpMsgBuf) + lstrlen((LPCTSTR) lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR) lpDisplayBuf, TEXT("Error"), MB_OK); 

    // Free error-handling buffer allocations.

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}
```



<span data-ttu-id="a3eda-114">Die- `MyThreadFunction` Funktion vermeidet die Verwendung der C-Lauf Zeit Bibliothek (CRT), da viele ihrer Funktionen nicht Thread sicher sind, insbesondere, wenn Sie die multithreadcrt nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3eda-114">The `MyThreadFunction` function avoids the use of the C run-time library (CRT), as many of its functions are not thread-safe, particularly if you are not using the multithreaded CRT.</span></span> <span data-ttu-id="a3eda-115">Wenn Sie die CRT in einer Funktion verwenden möchten `ThreadProc` , verwenden Sie stattdessen die **\_ beginthreadex** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a3eda-115">If you would like to use the CRT in a `ThreadProc` function, use the **\_beginthreadex** function instead.</span></span>

<span data-ttu-id="a3eda-116">Es ist riskant, die Adresse einer lokalen Variablen zu übergeben, wenn der erstellende Thread vor dem neuen Thread beendet wird, da der Zeiger ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="a3eda-116">It is risky to pass the address of a local variable if the creating thread exits before the new thread, because the pointer becomes invalid.</span></span> <span data-ttu-id="a3eda-117">Übergeben Sie stattdessen einen Zeiger auf dynamisch belegten Speicher, oder lassen Sie den Erstellungs Thread warten, bis der neue Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3eda-117">Instead, either pass a pointer to dynamically allocated memory or make the creating thread wait for the new thread to terminate.</span></span> <span data-ttu-id="a3eda-118">Daten können auch vom ergebenden Thread an den neuen Thread mithilfe globaler Variablen weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a3eda-118">Data can also be passed from the creating thread to the new thread using global variables.</span></span> <span data-ttu-id="a3eda-119">Bei globalen Variablen ist es normalerweise erforderlich, den Zugriff durch mehrere Threads zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a3eda-119">With global variables, it is usually necessary to synchronize access by multiple threads.</span></span> <span data-ttu-id="a3eda-120">Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="a3eda-120">For more information about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

<span data-ttu-id="a3eda-121">Der Erstellungsthread kann die Argumente für " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " verwenden, um Folgendes anzugeben:</span><span class="sxs-lookup"><span data-stu-id="a3eda-121">The creating thread can use the arguments to [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to specify the following:</span></span>

-   <span data-ttu-id="a3eda-122">Die Sicherheits Attribute für das Handle für den neuen Thread.</span><span class="sxs-lookup"><span data-stu-id="a3eda-122">The security attributes for the handle to the new thread.</span></span> <span data-ttu-id="a3eda-123">Diese Sicherheits Attribute enthalten ein Vererbungsflag, das bestimmt, ob das Handle von untergeordneten Prozessen geerbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3eda-123">These security attributes include an inheritance flag that determines whether the handle can be inherited by child processes.</span></span> <span data-ttu-id="a3eda-124">Die Sicherheits Attribute enthalten außerdem eine Sicherheits Beschreibung, die das System verwendet, um Zugriffs Überprüfungen für alle nachfolgenden Verwendungen des Thread Handles durchzuführen, bevor der Zugriff gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="a3eda-124">The security attributes also include a security descriptor, which the system uses to perform access checks on all subsequent uses of the thread's handle before access is granted.</span></span>
-   <span data-ttu-id="a3eda-125">Die anfängliche Stapelgröße des neuen Threads.</span><span class="sxs-lookup"><span data-stu-id="a3eda-125">The initial stack size of the new thread.</span></span> <span data-ttu-id="a3eda-126">Der Thread Stapel wird automatisch im Speicherbereich des Prozesses zugeordnet. Das System vergrößert den Stapel bei Bedarf und gibt ihn frei, wenn der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3eda-126">The thread's stack is allocated automatically in the memory space of the process; the system increases the stack as needed and frees it when the thread terminates.</span></span> <span data-ttu-id="a3eda-127">Weitere Informationen finden Sie unter [Thread Stapelgröße](thread-stack-size.md).</span><span class="sxs-lookup"><span data-stu-id="a3eda-127">For more information, see [Thread Stack Size](thread-stack-size.md).</span></span>
-   <span data-ttu-id="a3eda-128">Ein Erstellungsflag, das es Ihnen ermöglicht, den Thread in einem angehaltenen Zustand zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3eda-128">A creation flag that enables you to create the thread in a suspended state.</span></span> <span data-ttu-id="a3eda-129">Wenn der Thread angehalten wird, wird er erst ausgeführt, wenn die [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a3eda-129">When suspended, the thread does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) function is called.</span></span>

<span data-ttu-id="a3eda-130">Sie können auch einen Thread erstellen, indem Sie die [**createremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a3eda-130">You can also create a thread by calling the [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) function.</span></span> <span data-ttu-id="a3eda-131">Diese Funktion wird von debuggerprozessen verwendet, um einen Thread zu erstellen, der im Adressraum des Prozesses ausgeführt wird, der gedebuggt wird.</span><span class="sxs-lookup"><span data-stu-id="a3eda-131">This function is used by debugger processes to create a thread that runs in the address space of the process being debugged.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3eda-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3eda-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3eda-133">Beenden eines Threads</span><span class="sxs-lookup"><span data-stu-id="a3eda-133">Terminating a Thread</span></span>](terminating-a-thread.md)
</dt> </dl>

 

 
