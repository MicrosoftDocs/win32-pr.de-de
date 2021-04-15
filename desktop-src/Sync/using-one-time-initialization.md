---
description: In den folgenden Beispielen wird die Verwendung der einmaligen Initialisierungs Funktionen veranschaulicht.
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: Verwenden der One-Time Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f89cbe0e2d3e7c45d4f18863533c8c161037ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529768"
---
# <a name="using-one-time-initialization"></a>Verwenden der One-Time Initialisierung

In den folgenden Beispielen wird die Verwendung der einmaligen Initialisierungs Funktionen veranschaulicht.

## <a name="synchronous-example"></a>Synchrones Beispiel

In diesem Beispiel ist die `g_InitOnce` globale Variable die einmalige Initialisierungs Struktur. Die Initialisierung erfolgt statisch mithilfe von **Init, \_ einmal \_ statischer \_ Init**.

Die- `OpenEventHandleSync` Funktion gibt ein Handle für ein Ereignis zurück, das nur einmal erstellt wird. Die [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) -Funktion wird aufgerufen, um den Initialisierungs Code auszuführen, der in der `InitHandleFunction` Rückruffunktion enthalten ist. Wenn die Rückruffunktion erfolgreich ausgeführt wird, `OpenEventHandleSync` gibt das in *lpContext* zurückgegebene Ereignis Handle zurück. andernfalls wird ein **ungültiger \_ handle- \_ Wert** zurückgegeben.

Die- `InitHandleFunction` Funktion ist die [Rückruffunktion für einmalige Initialisierung](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn). `InitHandleFunction` Ruft die Funktion " [**reateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) " auf, um das Ereignis zu erstellen, und gibt das Ereignis Handle im *lpContext* -Parameter zurück.


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

In diesem Beispiel ist die `g_InitOnce` globale Variable die einmalige Initialisierungs Struktur. Die Initialisierung erfolgt statisch mithilfe von **Init, \_ einmal \_ statischer \_ Init**.

Die- `OpenEventHandleAsync` Funktion gibt ein Handle für ein Ereignis zurück, das nur einmal erstellt wird. `OpenEventHandleAsync` Ruft die [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) -Funktion auf, um den Initialisierungs Status einzugeben.

Wenn der-Befehl erfolgreich ausgeführt wird, prüft der Code den Wert des *fPending* -Parameters, um zu bestimmen, ob das Ereignis erstellt werden soll, oder gibt einfach ein Handle für das von einem anderen Thread erstellte Ereignis zurück. Wenn der Wert für " **false**" lautet *, ist* die Initialisierung bereits abgeschlossen, sodass `OpenEventHandleAsync` das im *lpContext* -Parameter zurückgegebene Ereignis Handle zurückgegeben wird. Andernfalls wird die Funktion " [**-Funktion"**](/windows/win32/api/synchapi/nf-synchapi-createeventa) aufgerufen, um das Ereignis und die [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) -Funktion zu erstellen, um die Initialisierung abzuschließen.

Wenn der [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) -Rückruf erfolgreich ist, `OpenEventHandleAsync` gibt das neue Ereignis Handle zurück. Andernfalls wird das Ereignis Handle geschlossen und [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) mit **Init \_ einmal \_ überprüft \_** , um zu bestimmen, ob die Initialisierung fehlgeschlagen ist oder von einem anderen Thread abgeschlossen wurde.

Wenn die Initialisierung von einem anderen Thread abgeschlossen wurde, `OpenEventHandleAsync` gibt das in *lpContext* zurückgegebene Ereignis Handle zurück. Andernfalls wird ein **ungültiger \_ handle- \_ Wert** zurückgegeben.


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

 

 
