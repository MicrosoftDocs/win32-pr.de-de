---
description: Die folgenden Beispiele veranschaulichen die Verwendung der einmaligen Initialisierungsfunktionen.
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: Verwenden One-Time Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98da686f17c2c089524949b5465f64d50166e8f705ceddcc73cc7dd972f9961f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959129"
---
# <a name="using-one-time-initialization"></a>Verwenden One-Time Initialisierung

Die folgenden Beispiele veranschaulichen die Verwendung der einmaligen Initialisierungsfunktionen.

## <a name="synchronous-example"></a>Synchrones Beispiel

In diesem Beispiel ist die `g_InitOnce` globale Variable die Einmalige Initialisierungsstruktur. Sie wird statisch **mitHILFE von INIT \_ ONCE STATIC \_ \_ INIT initialisiert.**

Die `OpenEventHandleSync` Funktion gibt ein Handle für ein Ereignis zurück, das nur einmal erstellt wird. Sie ruft die [**InitOnceExecuteOnce-Funktion**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) auf, um den initialisierungscode auszuführen, der in der `InitHandleFunction` Rückruffunktion enthalten ist. Wenn die Rückruffunktion erfolgreich ist, wird das in lpContext zurückgegebene Ereignishand handle `OpenEventHandleSync` zurückgegeben. Andernfalls wird **INVALID HANDLE VALUE \_ \_ zurückgegeben.** 

Die `InitHandleFunction` -Funktion ist [die Rückruffunktion für die einmalige Initialisierung.](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) `InitHandleFunction` ruft die [**CreateEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createeventa) auf, um das Ereignis zu erstellen, und gibt das Ereignishand handle im *lpContext-Parameter* zurück.


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Initialization callback function 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        
    PVOID Parameter,            
    PVOID *lpContext);           

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleSync()
{
  PVOID lpContext;
  BOOL  bStatus;
  
  // Execute the initialization callback function 
  bStatus = InitOnceExecuteOnce(&g_InitOnce,          // One-time initialization structure
                                InitHandleFunction,   // Pointer to initialization callback function
                                NULL,                 // Optional parameter to callback function (not used)
                                &lpContext);          // Receives pointer to event object stored in g_InitOnce

  // InitOnceExecuteOnce function succeeded. Return event object.
  if (bStatus)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return (INVALID_HANDLE_VALUE);
  }
}

// Initialization callback function that creates the event object 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        // Pointer to one-time initialization structure        
    PVOID Parameter,            // Optional parameter passed by InitOnceExecuteOnce            
    PVOID *lpContext)           // Receives pointer to event object           
{
  HANDLE hEvent;

  // Create event object
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return FALSE;
  }
  // Event object creation succeeded.
  else
  {
    *lpContext = hEvent;
    return TRUE;
  }
}
```



## <a name="asynchronous-example"></a>Asynchrones Beispiel

In diesem Beispiel ist die `g_InitOnce` globale Variable die Einmalige Initialisierungsstruktur. Sie wird statisch **mitHILFE von INIT \_ ONCE STATIC \_ \_ INIT initialisiert.**

Die `OpenEventHandleAsync` Funktion gibt ein Handle für ein Ereignis zurück, das nur einmal erstellt wird. `OpenEventHandleAsync` ruft die [**InitOnceBeginInitialize-Funktion auf,**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) um in den Initialisierungszustand zu gelangen.

Wenn der Aufruf erfolgreich ist, überprüft der Code den Wert des *fPending-Parameters,* um zu bestimmen, ob das Ereignis erstellt oder einfach ein Handle an das von einem anderen Thread erstellte Ereignis zurückgibt. Wenn *fPending* **auf FALSE festgelegt ist,** wurde die Initialisierung bereits abgeschlossen, sodass das im lpContext-Parameter zurückgegebene `OpenEventHandleAsync` *Ereignishand* handle zurückgibt. Andernfalls wird die [**CreateEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createeventa) aufgerufen, um das Ereignis zu erstellen, und die [**InitOnceComplete-Funktion**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) zum Abschließen der Initialisierung.

Wenn der Aufruf von [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) erfolgreich ist, `OpenEventHandleAsync` gibt das neue Ereignishandl zurück. Andernfalls wird das Ereignishand handle geschlossen und [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) mit **INIT \_ ONCE CHECK \_ \_ ONLY** aufgerufen, um zu ermitteln, ob die Initialisierung fehlgeschlagen ist oder von einem anderen Thread abgeschlossen wurde.

Wenn die Initialisierung von einem anderen Thread abgeschlossen wurde, gibt das in lpContext zurückgegebene `OpenEventHandleAsync` *Ereignishand handle zurück.* Andernfalls wird INVALID **\_ HANDLE VALUE \_ zurückgegeben.**


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleAsync()
{
  PVOID  lpContext;
  BOOL   fStatus;
  BOOL   fPending;
  HANDLE hEvent;
  
  // Begin one-time initialization
  fStatus = InitOnceBeginInitialize(&g_InitOnce,       // Pointer to one-time initialization structure
                                    INIT_ONCE_ASYNC,   // Asynchronous one-time initialization
                                    &fPending,         // Receives initialization status
                                    &lpContext);       // Receives pointer to data in g_InitOnce  

  // InitOnceBeginInitialize function failed.
  if (!fStatus)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Initialization has already completed and lpContext contains event object.
  if (!fPending)
  {
    return (HANDLE)lpContext;
  }

  // Create event object for one-time initialization.
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Complete one-time initialization.
  fStatus = InitOnceComplete(&g_InitOnce,             // Pointer to one-time initialization structure
                             INIT_ONCE_ASYNC,         // Asynchronous initialization
                             (PVOID)hEvent);          // Pointer to event object to be stored in g_InitOnce

  // InitOnceComplete function succeeded. Return event object.
  if (fStatus)
  {
    return hEvent;
  }
  
  // Initialization has already completed. Free the local event.
  CloseHandle(hEvent);


  // Retrieve the final context data.
  fStatus = InitOnceBeginInitialize(&g_InitOnce,            // Pointer to one-time initialization structure
                                    INIT_ONCE_CHECK_ONLY,   // Check whether initialization is complete
                                    &fPending,              // Receives initialization status
                                    &lpContext);            // Receives pointer to event object in g_InitOnce
  
  // Initialization is complete. Return handle.
  if (fStatus && !fPending)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return INVALID_HANDLE_VALUE;
  }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einmalige Initialisierung](one-time-initialization.md)
</dt> </dl>

 

 
