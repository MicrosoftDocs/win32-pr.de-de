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
# <a name="creating-threads"></a>Erstellen von Threads

Die Funktion " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " erstellt einen neuen Thread für einen Prozess. Der Erstellungs Thread muss die Startadresse des Codes angeben, den der neue Thread ausführen soll. Die Startadresse ist in der Regel der Name einer im Programmcode definierten Funktion (Weitere Informationen finden Sie unter [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))). Diese Funktion nimmt einen einzelnen Parameter an und gibt einen **DWORD** -Wert zurück. Ein Prozess kann mehrere Threads gleichzeitig dieselbe Funktion ausführen.

Im folgenden finden Sie ein einfaches Beispiel, das veranschaulicht, wie ein neuer Thread erstellt wird, der die lokal definierte Funktion ausführt `MyThreadFunction` .

Der aufrufende Thread verwendet die [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) -Funktion, um beizubehalten, bis alle Arbeitsthreads beendet wurden. Der Aufruf Thread blockiert, während er wartet. um die Verarbeitung fortzusetzen, verwendet ein aufrufenden Thread [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) und wartet, bis jeder Arbeits Thread sein warte Objekt signalisiert. Beachten Sie Folgendes: Wenn Sie das Handle für einen Arbeits Thread vor dem Beenden schließen, wird der Arbeits Thread dadurch nicht beendet. Allerdings steht das Handle nicht für die Verwendung in nachfolgenden Funktionsaufrufen zur Verfügung.


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



Die- `MyThreadFunction` Funktion vermeidet die Verwendung der C-Lauf Zeit Bibliothek (CRT), da viele ihrer Funktionen nicht Thread sicher sind, insbesondere, wenn Sie die multithreadcrt nicht verwenden. Wenn Sie die CRT in einer Funktion verwenden möchten `ThreadProc` , verwenden Sie stattdessen die **\_ beginthreadex** -Funktion.

Es ist riskant, die Adresse einer lokalen Variablen zu übergeben, wenn der erstellende Thread vor dem neuen Thread beendet wird, da der Zeiger ungültig wird. Übergeben Sie stattdessen einen Zeiger auf dynamisch belegten Speicher, oder lassen Sie den Erstellungs Thread warten, bis der neue Thread beendet wird. Daten können auch vom ergebenden Thread an den neuen Thread mithilfe globaler Variablen weitergegeben werden. Bei globalen Variablen ist es normalerweise erforderlich, den Zugriff durch mehrere Threads zu synchronisieren. Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads](synchronizing-execution-of-multiple-threads.md).

Der Erstellungsthread kann die Argumente für " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " verwenden, um Folgendes anzugeben:

-   Die Sicherheits Attribute für das Handle für den neuen Thread. Diese Sicherheits Attribute enthalten ein Vererbungsflag, das bestimmt, ob das Handle von untergeordneten Prozessen geerbt werden kann. Die Sicherheits Attribute enthalten außerdem eine Sicherheits Beschreibung, die das System verwendet, um Zugriffs Überprüfungen für alle nachfolgenden Verwendungen des Thread Handles durchzuführen, bevor der Zugriff gewährt wird.
-   Die anfängliche Stapelgröße des neuen Threads. Der Thread Stapel wird automatisch im Speicherbereich des Prozesses zugeordnet. Das System vergrößert den Stapel bei Bedarf und gibt ihn frei, wenn der Thread beendet wird. Weitere Informationen finden Sie unter [Thread Stapelgröße](thread-stack-size.md).
-   Ein Erstellungsflag, das es Ihnen ermöglicht, den Thread in einem angehaltenen Zustand zu erstellen. Wenn der Thread angehalten wird, wird er erst ausgeführt, wenn die [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) -Funktion aufgerufen wird.

Sie können auch einen Thread erstellen, indem Sie die [**createremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) -Funktion aufrufen. Diese Funktion wird von debuggerprozessen verwendet, um einen Thread zu erstellen, der im Adressraum des Prozesses ausgeführt wird, der gedebuggt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beenden eines Threads](terminating-a-thread.md)
</dt> </dl>

 

 
