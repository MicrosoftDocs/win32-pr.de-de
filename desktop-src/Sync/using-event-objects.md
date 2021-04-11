---
description: Anwendungen können Ereignis Objekte in einer Reihe von Situationen verwenden, um einen wartenden Thread über das Auftreten eines Ereignisses zu benachrichtigen.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Verwenden von Ereignis Objekten (Synchronisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c0c7ee5f58b8359e989b19ffc9c016dd1a6593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865403"
---
# <a name="using-event-objects-synchronization"></a>Verwenden von Ereignis Objekten (Synchronisierung)

Anwendungen können [Ereignis Objekte](event-objects.md) in einer Reihe von Situationen verwenden, um einen wartenden Thread über das Auftreten eines Ereignisses zu benachrichtigen. Beispielsweise wird bei überlappenden e/a-Vorgängen für Dateien, Named Pipes und Kommunikationsgeräte ein Ereignis Objekt verwendet, um den Abschluss zu signalisieren. Weitere Informationen zur Verwendung von Ereignis Objekten in überlappenden e/a-Vorgängen finden Sie unter [Synchronisierung und überlappende Eingabe und Ausgabe](synchronization-and-overlapped-input-and-output.md).

Im folgenden Beispiel werden Ereignis Objekte verwendet, um zu verhindern, dass mehrere Threads aus einem freigegebenen Speicherpuffer lesen, während ein Master Thread in diesen Puffer schreibt. Zuerst verwendet der Master Thread die Funktion " [**forateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) ", um ein Ereignis Objekt für manuelles Zurücksetzen zu erstellen, dessen ursprünglicher Zustand nicht signalisiert ist. Anschließend werden mehrere Lesethreads erstellt. Der Master Thread führt einen Schreibvorgang aus und legt dann das Ereignis Objekt auf den signalisierten Zustand fest, wenn der Schreibvorgang abgeschlossen ist.

Vor dem Starten eines Lesevorgangs verwendet jeder Lesethread [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) , um zu warten, bis das Ereignis Objekt für manuelles Zurücksetzen signalisiert wird. Wenn **WaitForSingleObject** zurückgibt, gibt dies an, dass der Haupt Thread bereit ist, damit er mit dem Lesevorgang beginnen kann.


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



 

 
