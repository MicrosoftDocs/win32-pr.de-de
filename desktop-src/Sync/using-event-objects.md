---
description: Anwendungen können Ereignisobjekte in einer Reihe von Situationen verwenden, um einen wartenden Thread über das Auftreten eines Ereignisses zu benachrichtigen.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Verwenden von Ereignisobjekten (Synchronisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8466ca1104a4d8e6ddaaed3e0618bea3db68bd1954aaf3b859f66fb93a3aac79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765331"
---
# <a name="using-event-objects-synchronization"></a>Verwenden von Ereignisobjekten (Synchronisierung)

Anwendungen können [Ereignisobjekte](event-objects.md) in einer Reihe von Situationen verwenden, um einen wartenden Thread über das Auftreten eines Ereignisses zu benachrichtigen. Beispielsweise verwenden überlappende E/A-Vorgänge für Dateien, Named Pipes und Kommunikationsgeräte ein Ereignisobjekt, um ihren Abschluss zu signalisieren. Weitere Informationen zur Verwendung von Ereignisobjekten in überlappende E/A-Vorgänge finden Sie unter [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).

Im folgenden Beispiel werden Ereignisobjekte verwendet, um zu verhindern, dass mehrere Threads aus einem Shared Memory-Puffer lesen, während ein Masterthread in diesen Puffer schreibt. Zunächst verwendet der Masterthread die [**CreateEvent-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-createeventa) um ein Ereignisobjekt mit manueller Zurücksetzung zu erstellen, dessen Anfangszustand nicht signalisiert ist. Anschließend werden mehrere Readerthreads erstellt. Der Masterthread führt einen Schreibvorgang aus und legt dann das Ereignisobjekt auf den signalisierten Zustand fest, wenn das Schreiben abgeschlossen ist.

Bevor ein Lesevorgang gestartet wird, verwendet jeder Readerthread [**WaitForSingleObject,**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) um zu warten, bis das Ereignisobjekt für manuelles Zurücksetzen signalisiert wird. Wenn **WaitForSingleObject** zurückgegeben wird, gibt dies an, dass der Hauptthread bereit ist, mit dem Lesevorgang zu beginnen.


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 4 

HANDLE ghWriteEvent; 
HANDLE ghThreads[THREADCOUNT];

DWORD WINAPI ThreadProc(LPVOID);

void CreateEventsAndThreads(void) 
{
    int i; 
    DWORD dwThreadID; 

    // Create a manual-reset event object. The write thread sets this
    // object to the signaled state when it finishes writing to a 
    // shared buffer. 

    ghWriteEvent = CreateEvent( 
        NULL,               // default security attributes
        TRUE,               // manual-reset event
        FALSE,              // initial state is nonsignaled
        TEXT("WriteEvent")  // object name
        ); 

    if (ghWriteEvent == NULL) 
    { 
        printf("CreateEvent failed (%d)\n", GetLastError());
        return;
    }

    // Create multiple threads to read from the buffer.

    for(i = 0; i < THREADCOUNT; i++) 
    {
        // TODO: More complex scenarios may require use of a parameter
        //   to the thread procedure, such as an event per thread to  
        //   be used for synchronization.
        ghThreads[i] = CreateThread(
            NULL,              // default security
            0,                 // default stack size
            ThreadProc,        // name of the thread function
            NULL,              // no thread parameters
            0,                 // default startup flags
            &dwThreadID); 

        if (ghThreads[i] == NULL) 
        {
            printf("CreateThread failed (%d)\n", GetLastError());
            return;
        }
    }
}

void WriteToBuffer(VOID) 
{
    // TODO: Write to the shared buffer.
    
    printf("Main thread writing to the shared buffer...\n");

    // Set ghWriteEvent to signaled

    if (! SetEvent(ghWriteEvent) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return;
    }
}

void CloseEvents()
{
    // Close all event handles (currently, only one global handle).
    
    CloseHandle(ghWriteEvent);
}

int main( void )
{
    DWORD dwWaitResult;

    // TODO: Create the shared buffer

    // Create events and THREADCOUNT threads to read from the buffer

    CreateEventsAndThreads();

    // At this point, the reader threads have started and are most
    // likely waiting for the global event to be signaled. However, 
    // it is safe to write to the buffer because the event is a 
    // manual-reset event.
    
    WriteToBuffer();

    printf("Main thread waiting for threads to exit...\n");

    // The handle for each thread is signaled when the thread is
    // terminated.
    dwWaitResult = WaitForMultipleObjects(
        THREADCOUNT,   // number of handles in array
        ghThreads,     // array of thread handles
        TRUE,          // wait until all are signaled
        INFINITE);

    switch (dwWaitResult) 
    {
        // All thread objects were signaled
        case WAIT_OBJECT_0: 
            printf("All threads ended, cleaning up for application exit...\n");
            break;

        // An error occurred
        default: 
            printf("WaitForMultipleObjects failed (%d)\n", GetLastError());
            return 1;
    } 
            
    // Close the events to clean up

    CloseEvents();

    return 0;
}

DWORD WINAPI ThreadProc(LPVOID lpParam) 
{
    // lpParam not used in this example.
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult;

    printf("Thread %d waiting for write event...\n", GetCurrentThreadId());
    
    dwWaitResult = WaitForSingleObject( 
        ghWriteEvent, // event handle
        INFINITE);    // indefinite wait

    switch (dwWaitResult) 
    {
        // Event object was signaled
        case WAIT_OBJECT_0: 
            //
            // TODO: Read from the shared buffer
            //
            printf("Thread %d reading from buffer\n", 
                   GetCurrentThreadId());
            break; 

        // An error occurred
        default: 
            printf("Wait error (%d)\n", GetLastError()); 
            return 0; 
    }

    // Now that we are done reading the buffer, we could use another
    // event to signal that this thread is no longer reading. This
    // example simply uses the thread handle for synchronization (the
    // handle is signaled when the thread terminates.)

    printf("Thread %d exiting\n", GetCurrentThreadId());
    return 1;
}

```



 

 
