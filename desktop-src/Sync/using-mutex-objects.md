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
# <a name="using-mutex-objects"></a>Verwenden von Mutex-Objekten

Sie können ein [Mutex-Objekt](mutex-objects.md) verwenden, um eine freigegebene Ressource vor gleichzeitigem Zugriff durch mehrere Threads oder Prozesse zu schützen. Jeder Thread muss auf den Besitz des Mutex warten, bevor er den Code ausführen kann, der auf die freigegebene Ressource zugreift. Wenn z. b. mehrere Threads den Zugriff auf eine Datenbank gemeinsam nutzen, können die Threads ein Mutex-Objekt verwenden, um jeweils nur einen Thread zum Schreiben in die Datenbank zuzulassen.

Im folgenden Beispiel wird die Funktion " [**kreatemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) " verwendet, um ein Mutex-Objekt und die Funktion " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " zum Erstellen von Arbeitsthreads zu erstellen.

Wenn ein Thread dieses Prozesses in die Datenbank schreibt, fordert er zuerst den Besitz des Mutex mithilfe der [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) -Funktion an. Wenn der Thread in den Besitz des Mutex gelangt, schreibt er in die Datenbank und gibt den Besitz des Mutex mithilfe der [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) -Funktion frei.

Dieses Beispiel verwendet die strukturierte Ausnahmebehandlung, um sicherzustellen, dass der Thread das Mutex-Objekt ordnungsgemäß freigibt. Der letzte Codeblock wird ausgeführt, unabhängig davon, wie der **\_ \_ try** -Block beendet wird (es sei denn, der **\_ \_ try** -Block enthält einen Aufrufen der [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) -Funktion). **\_ \_** Dadurch wird verhindert, dass das Mutex-Objekt versehentlich abgebrochen wird.

Wenn ein Mutex abgebrochen wird, hat der Thread, der im Besitz des Mutex war, ihn vor dem Beenden nicht ordnungsgemäß freigegeben. In diesem Fall ist der Status der freigegebenen Ressource unbestimmt, und die Verwendung des Mutex kann einen potenziell schwerwiegenden Fehler verbergen. Einige Anwendungen versuchen möglicherweise, die Ressource in einem konsistenten Zustand wiederherzustellen. Dieses Beispiel gibt einfach einen Fehler zurück und beendet die Verwendung des Mutex. Weitere Informationen finden Sie unter [Mutex Objects](mutex-objects.md).


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



 

 
