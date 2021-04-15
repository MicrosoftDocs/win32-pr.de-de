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
# <a name="using-one-time-initialization"></a><span data-ttu-id="f5d22-103">Verwenden der One-Time Initialisierung</span><span class="sxs-lookup"><span data-stu-id="f5d22-103">Using One-Time Initialization</span></span>

<span data-ttu-id="f5d22-104">In den folgenden Beispielen wird die Verwendung der einmaligen Initialisierungs Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f5d22-104">The following examples demonstrate the use of the one-time initialization functions.</span></span>

## <a name="synchronous-example"></a><span data-ttu-id="f5d22-105">Synchrones Beispiel</span><span class="sxs-lookup"><span data-stu-id="f5d22-105">Synchronous Example</span></span>

<span data-ttu-id="f5d22-106">In diesem Beispiel ist die `g_InitOnce` globale Variable die einmalige Initialisierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="f5d22-106">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="f5d22-107">Die Initialisierung erfolgt statisch mithilfe von **Init, \_ einmal \_ statischer \_ Init**.</span><span class="sxs-lookup"><span data-stu-id="f5d22-107">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="f5d22-108">Die- `OpenEventHandleSync` Funktion gibt ein Handle für ein Ereignis zurück, das nur einmal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f5d22-108">The `OpenEventHandleSync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="f5d22-109">Die [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) -Funktion wird aufgerufen, um den Initialisierungs Code auszuführen, der in der `InitHandleFunction` Rückruffunktion enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f5d22-109">It calls the [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) function to execute the initialization code contained in the `InitHandleFunction` callback function.</span></span> <span data-ttu-id="f5d22-110">Wenn die Rückruffunktion erfolgreich ausgeführt wird, `OpenEventHandleSync` gibt das in *lpContext* zurückgegebene Ereignis Handle zurück. andernfalls wird ein **ungültiger \_ handle- \_ Wert** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5d22-110">If the callback function succeeds, `OpenEventHandleSync` returns the event handle returned in *lpContext*; otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="f5d22-111">Die- `InitHandleFunction` Funktion ist die [Rückruffunktion für einmalige Initialisierung](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span><span class="sxs-lookup"><span data-stu-id="f5d22-111">The `InitHandleFunction` function is the [one-time initialization callback function](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span></span> <span data-ttu-id="f5d22-112">`InitHandleFunction` Ruft die Funktion " [**reateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) " auf, um das Ereignis zu erstellen, und gibt das Ereignis Handle im *lpContext* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f5d22-112">`InitHandleFunction` calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and returns the event handle in the *lpContext* parameter.</span></span>


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



## <a name="asynchronous-example"></a><span data-ttu-id="f5d22-113">Asynchrones Beispiel</span><span class="sxs-lookup"><span data-stu-id="f5d22-113">Asynchronous Example</span></span>

<span data-ttu-id="f5d22-114">In diesem Beispiel ist die `g_InitOnce` globale Variable die einmalige Initialisierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="f5d22-114">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="f5d22-115">Die Initialisierung erfolgt statisch mithilfe von **Init, \_ einmal \_ statischer \_ Init**.</span><span class="sxs-lookup"><span data-stu-id="f5d22-115">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="f5d22-116">Die- `OpenEventHandleAsync` Funktion gibt ein Handle für ein Ereignis zurück, das nur einmal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f5d22-116">The `OpenEventHandleAsync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="f5d22-117">`OpenEventHandleAsync` Ruft die [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) -Funktion auf, um den Initialisierungs Status einzugeben.</span><span class="sxs-lookup"><span data-stu-id="f5d22-117">`OpenEventHandleAsync` calls the [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) function to enter the initializing state.</span></span>

<span data-ttu-id="f5d22-118">Wenn der-Befehl erfolgreich ausgeführt wird, prüft der Code den Wert des *fPending* -Parameters, um zu bestimmen, ob das Ereignis erstellt werden soll, oder gibt einfach ein Handle für das von einem anderen Thread erstellte Ereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="f5d22-118">If the call succeeds, the code checks the value of the *fPending* parameter to determine whether to create the event or simply return a handle to the event created by another thread.</span></span> <span data-ttu-id="f5d22-119">Wenn der Wert für " **false**" lautet *, ist* die Initialisierung bereits abgeschlossen, sodass `OpenEventHandleAsync` das im *lpContext* -Parameter zurückgegebene Ereignis Handle zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f5d22-119">If *fPending* is **FALSE**, initialization has already completed so `OpenEventHandleAsync` returns the event handle returned in the *lpContext* parameter.</span></span> <span data-ttu-id="f5d22-120">Andernfalls wird die Funktion " [**-Funktion"**](/windows/win32/api/synchapi/nf-synchapi-createeventa) aufgerufen, um das Ereignis und die [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) -Funktion zu erstellen, um die Initialisierung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f5d22-120">Otherwise, it calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and the [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) function to complete the initialization.</span></span>

<span data-ttu-id="f5d22-121">Wenn der [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) -Rückruf erfolgreich ist, `OpenEventHandleAsync` gibt das neue Ereignis Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="f5d22-121">If the call to [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) succeeds, `OpenEventHandleAsync` returns the new event handle.</span></span> <span data-ttu-id="f5d22-122">Andernfalls wird das Ereignis Handle geschlossen und [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) mit **Init \_ einmal \_ überprüft \_** , um zu bestimmen, ob die Initialisierung fehlgeschlagen ist oder von einem anderen Thread abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f5d22-122">Otherwise, it closes the event handle and calls [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) with **INIT\_ONCE\_CHECK\_ONLY** to determine whether initialization failed or was completed by another thread.</span></span>

<span data-ttu-id="f5d22-123">Wenn die Initialisierung von einem anderen Thread abgeschlossen wurde, `OpenEventHandleAsync` gibt das in *lpContext* zurückgegebene Ereignis Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="f5d22-123">If the initialization was completed by another thread, `OpenEventHandleAsync` returns the event handle returned in *lpContext*.</span></span> <span data-ttu-id="f5d22-124">Andernfalls wird ein **ungültiger \_ handle- \_ Wert** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5d22-124">Otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f5d22-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5d22-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5d22-126">Einmalige Initialisierung</span><span class="sxs-lookup"><span data-stu-id="f5d22-126">One-Time Initialization</span></span>](one-time-initialization.md)
</dt> </dl>

 

 
