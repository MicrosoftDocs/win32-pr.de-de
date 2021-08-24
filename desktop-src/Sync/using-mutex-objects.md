---
description: Sie können ein Mutexobjekt verwenden, um eine freigegebene Ressource vor dem gleichzeitigen Zugriff durch mehrere Threads oder Prozesse zu schützen.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Verwenden von Mutex-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c629d90e1cd811c62f62e1151cee4c3e2af77b84133e142fcfe7f93a35b2e5bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739260"
---
# <a name="using-mutex-objects"></a>Verwenden von Mutex-Objekten

Sie können ein [Mutexobjekt](mutex-objects.md) verwenden, um eine freigegebene Ressource vor dem gleichzeitigen Zugriff durch mehrere Threads oder Prozesse zu schützen. Jeder Thread muss auf den Besitz des Mutex warten, bevor er den Code ausführen kann, der auf die freigegebene Ressource zugreift. Wenn z. B. mehrere Threads den Zugriff auf eine Datenbank gemeinsam nutzen, können die Threads ein Mutex-Objekt verwenden, um jeweils nur einem Thread das Schreiben in die Datenbank zu gestatten.

Im folgenden Beispiel wird die [**CreateMutex-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) verwendet, um ein Mutex-Objekt zu erstellen, und die [**CreateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) zum Erstellen von Arbeitsthreads.

Wenn ein Thread dieses Prozesses in die Datenbank schreibt, fordert er zunächst den Besitz des Mutex mithilfe der [**WaitForSingleObject-Funktion**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) an. Wenn der Thread den Besitz des Mutex erhält, schreibt er in die Datenbank und gibt dann den Besitz des Mutex mithilfe der [**ReleaseMutex-Funktion**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) frei.

In diesem Beispiel wird die strukturierte Ausnahmebehandlung verwendet, um sicherzustellen, dass der Thread das Mutex-Objekt ordnungsgemäß freigibt. Der **\_ \_ finally-Codeblock** wird unabhängig davon ausgeführt, wie der **\_ \_ try-Block** beendet wird (es sei denn, der **\_ \_ try-Block** enthält einen Aufruf der [**TerminateThread-Funktion).**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) Dadurch wird verhindert, dass das Mutex-Objekt versehentlich abgebrochen wird.

Wenn ein Mutex abgebrochen wird, hat der Thread, der den Mutex besitzt, ihn vor dem Beenden nicht ordnungsgemäß freigeben. In diesem Fall ist der Status der freigegebenen Ressource unbestimmt, und die weitere Verwendung des Mutex kann einen potenziell schwerwiegenden Fehler verbergen. Einige Anwendungen versuchen möglicherweise, die Ressource in einem konsistenten Zustand wiederherzustellen. Dieses Beispiel gibt einfach einen Fehler zurück und beendet die Verwendung des Mutex. Weitere Informationen finden Sie unter [Mutex-Objekte.](mutex-objects.md)


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



 

 
