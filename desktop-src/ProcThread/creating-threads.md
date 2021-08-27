---
description: Erfahren Sie, wie Sie mit der CreateThread-Funktion einen neuen Thread für einen Prozess erstellen. Sehen Sie sich ein Codebeispiel an, das seine Verwendung zeigt.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Erstellen von Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dee74cb81c886fe05d07a0970f7d8946d123d92810e6f22dd094e1d8d00466a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081430"
---
# <a name="creating-threads"></a>Erstellen von Threads

Die [**CreateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) erstellt einen neuen Thread für einen Prozess. Der erstellende Thread muss die Startadresse des Codes angeben, der vom neuen Thread ausgeführt werden soll. In der Regel ist die Startadresse der Name einer Funktion, die im Programmcode definiert ist (weitere Informationen finden Sie unter [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))). Diese Funktion akzeptiert einen einzelnen Parameter und gibt einen **DWORD-Wert** zurück. Ein Prozess kann mehrere Threads haben, die gleichzeitig dieselbe Funktion ausführen.

Im Folgenden finden Sie ein einfaches Beispiel, das veranschaulicht, wie ein neuer Thread erstellt wird, der die lokal definierte Funktion ( ) `MyThreadFunction` ausricht.

Der aufrufende Thread verwendet die [**WaitForMultipleObjects-Funktion,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) um persistent zu bleiben, bis alle Arbeitsthreads beendet wurden. Der aufrufende Thread blockiert, während er wartet. Um die Verarbeitung fortzufahren, verwendet ein aufrufende Thread [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) und wartet, bis jeder Arbeitsthread sein Warteobjekt signalisiert. Beachten Sie, dass der Arbeitsthread nicht beendet wird, wenn Sie das Handle vor dem Beenden eines Arbeitsthreads schließen. Das Handle ist jedoch nicht für die Verwendung in nachfolgenden Funktionsaufrufen verfügbar.


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



Die -Funktion vermeidet die Verwendung der C-Laufzeitbibliothek (CRT), da viele ihrer Funktionen nicht threadsicher sind, insbesondere wenn Sie die `MyThreadFunction` Multithread-CRT nicht verwenden. Wenn Sie die CRT in einer Funktion verwenden `ThreadProc` möchten, verwenden Sie stattdessen **\_ die beginthreadex-Funktion.**

Es ist riskant, die Adresse einer lokalen Variablen zu übergeben, wenn der erstellende Thread vor dem neuen Thread beendet wird, da der Zeiger ungültig wird. Übergeben Sie stattdessen entweder einen Zeiger auf dynamisch zugewiesenen Arbeitsspeicher, oder lassen Sie den erstellenden Thread warten, bis der neue Thread beendet wird. Daten können auch mithilfe globaler Variablen vom erstellenden Thread an den neuen Thread übergeben werden. Bei globalen Variablen ist es in der Regel erforderlich, den Zugriff über mehrere Threads zu synchronisieren. Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads.](synchronizing-execution-of-multiple-threads.md)

Der erstellende Thread kann die Argumente für [**CreateThread verwenden,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) um Folgendes anzugeben:

-   Die Sicherheitsattribute für das Handle für den neuen Thread. Diese Sicherheitsattribute enthalten ein Vererbungsflag, das bestimmt, ob das Handle von untergeordneten Prozessen geerbt werden kann. Die Sicherheitsattribute enthalten auch einen Sicherheitsdeskriptor, der vom System verwendet wird, um Zugriffsüberprüfungen für alle nachfolgenden Verwendungen des Handle des Threads durchzuführen, bevor der Zugriff gewährt wird.
-   Die anfängliche Stapelgröße des neuen Threads. Der Stapel des Threads wird automatisch im Arbeitsspeicher des Prozesses zugeordnet. Das System erhöht den Stapel nach Bedarf und gibt ihn frei, wenn der Thread beendet wird. Weitere Informationen finden Sie unter [Threadstapelgröße.](thread-stack-size.md)
-   Ein Erstellungsflag, mit dem Sie den Thread in einem angehaltenen Zustand erstellen können. Wenn der Thread angehalten wird, wird er erst ausgeführt, wenn die [**ResumeThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) aufgerufen wird.

Sie können auch einen Thread erstellen, indem Sie die [**CreateRemoteThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) aufrufen. Diese Funktion wird von Debuggerprozessen verwendet, um einen Thread zu erstellen, der im Adressraum des zu debuggenden Prozesses ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beenden eines Threads](terminating-a-thread.md)
</dt> </dl>

 

 
