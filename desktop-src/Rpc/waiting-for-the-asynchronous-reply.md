---
title: Warten auf die asynchrone Antwort
description: Welche Aktionen der Client durchführt, während er darauf wartet, dass eine Antwort vom Server benachrichtigt wird, hängt vom ausgewählten Benachrichtigungs Mechanismus ab.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- Remote Prozedur Aufruf RPC, Tasks, warten auf asynchrone Antworten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315885"
---
# <a name="waiting-for-the-asynchronous-reply"></a><span data-ttu-id="d4723-104">Warten auf die asynchrone Antwort</span><span class="sxs-lookup"><span data-stu-id="d4723-104">Waiting for the Asynchronous Reply</span></span>

<span data-ttu-id="d4723-105">Welche Aktionen der Client durchführt, während er darauf wartet, dass eine Antwort vom Server benachrichtigt wird, hängt vom ausgewählten Benachrichtigungs Mechanismus ab.</span><span class="sxs-lookup"><span data-stu-id="d4723-105">What the client does while it waits to be notified of a reply from the server depends on the notification mechanism it selects.</span></span>

<span data-ttu-id="d4723-106">Wenn der Client ein Ereignis für die Benachrichtigung verwendet, wird in der Regel die [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion oder die [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d4723-106">If the client uses an event for notification, it will typically call the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function or the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function.</span></span> <span data-ttu-id="d4723-107">Der Client wechselt in einen blockierten Zustand, wenn er eine dieser Funktionen aufruft.</span><span class="sxs-lookup"><span data-stu-id="d4723-107">The client enters a blocked state when it calls either of these functions.</span></span> <span data-ttu-id="d4723-108">Dies ist effizient, da der Client keine CPU-Lauf Zyklen beansprucht, während er blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="d4723-108">This is efficient because the client does not consume CPU run cycles while it is blocked.</span></span>

<span data-ttu-id="d4723-109">Wenn Abruf verwendet wird, um auf seine Ergebnisse zu warten, wechselt das Client Programm in eine Schleife, die die Funktion [**rpcasyncgetcallstatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)wiederholt aufruft.</span><span class="sxs-lookup"><span data-stu-id="d4723-109">When it uses polling to wait for its results, the client program enters a loop that repeatedly calls the function [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="d4723-110">Dies ist eine effiziente Methode, um zu warten, ob das Client Programm in der Abruf Schleife eine andere Verarbeitung durchführt.</span><span class="sxs-lookup"><span data-stu-id="d4723-110">This is an efficient method of waiting if your client program does other processing in the polling loop.</span></span> <span data-ttu-id="d4723-111">Beispielsweise kann die Daten in kleinen Blöcken für einen nachfolgenden asynchronen Remote Prozedur Aufrufvorgang vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="d4723-111">For instance, it can prepare data in small chunks for a subsequent asynchronous remote procedure call.</span></span> <span data-ttu-id="d4723-112">Nachdem jeder Block abgeschlossen ist, kann der Client den ausstehenden asynchronen Remote Prozedur Aufrufs Abfragen, um zu prüfen, ob er abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d4723-112">After each chunk is finished, your client can poll the outstanding asynchronous remote procedure call to see if it is complete.</span></span>

<span data-ttu-id="d4723-113">Das Client Programm kann einen asynchronen Prozedur Aufruf (APC) bereitstellen, bei dem es sich um eine Rückruffunktion handelt, die von der RPC-Lauf Zeit Bibliothek beim Abschluss des asynchronen Remote Prozedur Aufrufs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d4723-113">Your client program can provide an asynchronous procedure call (APC), which is a type of callback function that the RPC run-time library will invoke when the asynchronous remote procedure call completes.</span></span> <span data-ttu-id="d4723-114">Ihr Client Programm muss den Wartezustand "Warnung" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d4723-114">Your client program must be in an alertable wait state.</span></span> <span data-ttu-id="d4723-115">Dies bedeutet in der Regel, dass der Client eine Windows-API-Funktion aufruft, um sich in einen blockierten Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="d4723-115">This typically means that the client calls a Windows API function to put itself in a blocked state.</span></span> <span data-ttu-id="d4723-116">Weitere Informationen finden Sie unter [asynchrone Prozedur Aufrufe](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="d4723-116">For more information, see [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span>

> [!Note]  
> <span data-ttu-id="d4723-117">Die Benachrichtigung über den Abschluss wird von einer asynchronen RPC-Routine nicht zurückgegeben, wenn während eines asynchronen Aufrufs eine RPC-Ausnahme ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="d4723-117">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during a asynchronous call.</span></span>

 

<span data-ttu-id="d4723-118">Wenn Ihr Client Programm einen e/a-Abschlussport verwendet, um Abschluss Benachrichtigungen zu empfangen, muss er die [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d4723-118">If your client program uses an I/O completion port to receive completion notification, it must call the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="d4723-119">Wenn dies der Fall ist, kann es entweder unbegrenzt auf eine Antwort warten oder die andere Verarbeitung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="d4723-119">When it does, it can either wait indefinitely for a response or continue to do other processing.</span></span> <span data-ttu-id="d4723-120">Wenn beim Warten auf eine Antwort andere Verarbeitungsvorgänge durchführt, muss der Abschlussport mit der **GetQueuedCompletionStatus** -Funktion abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="d4723-120">If it does other processing while it waits for a reply, it must poll the completion port with the **GetQueuedCompletionStatus** function.</span></span> <span data-ttu-id="d4723-121">In diesem Fall muss die *dwMilliseconds* in der Regel auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d4723-121">In this case, it typically needs to set the *dwMilliseconds* to zero.</span></span> <span data-ttu-id="d4723-122">Dies bewirkt, dass **GetQueuedCompletionStatus** sofort zurückgegeben wird, auch wenn der asynchrone-Befehl nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d4723-122">This causes **GetQueuedCompletionStatus** to return immediately, even if the asynchronous call has not completed.</span></span>

<span data-ttu-id="d4723-123">Client Programme können auch eine Vervollständigungs Benachrichtigung über die Fenster Nachrichten Warteschlangen empfangen.</span><span class="sxs-lookup"><span data-stu-id="d4723-123">Client programs can also receive completion notification through their window message queues.</span></span> <span data-ttu-id="d4723-124">In diesem Fall wird die Abschluss Nachricht einfach wie jede beliebige Windows-Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d4723-124">In this situation, they simply process the completion message as they would any Windows message.</span></span>

<span data-ttu-id="d4723-125">In einer Multithreadanwendung kann ein asynchroner-Rückruf nur vom Client abgebrochen werden, nachdem der Thread, der den-Befehl ausgelöst hat, erfolgreich vom-Befehl zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d4723-125">In a multithreaded application, an asynchronous call can be canceled by the client only after the thread that originated the call has returned successfully from the call.</span></span> <span data-ttu-id="d4723-126">Dadurch wird sichergestellt, dass der-Vorgang nicht asynchron von einem anderen Thread abgebrochen wird, nachdem er einen synchronen-Befehl nicht</span><span class="sxs-lookup"><span data-stu-id="d4723-126">This ensures that the call is not canceled asynchronously by another thread after it failed a synchronous call.</span></span> <span data-ttu-id="d4723-127">Als Standardübung sollte ein asynchroner Rückruf, der synchron fehlschlägt, nicht asynchron abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="d4723-127">As standard practice, an asynchronous call that fails synchronously should not be canceled asynchronously.</span></span> <span data-ttu-id="d4723-128">Die Client Anwendung muss dieses Verhalten beobachten, wenn Aufrufe für verschiedene Threads ausgegeben und abgebrochen werden können.</span><span class="sxs-lookup"><span data-stu-id="d4723-128">The client application must observe this behavior if calls may be issued and canceled on different threads.</span></span> <span data-ttu-id="d4723-129">Nachdem der-Befehl abgebrochen wurde, muss der Client Code außerdem auf die Abschluss Benachrichtigung warten und den-Vorgang abschließen.</span><span class="sxs-lookup"><span data-stu-id="d4723-129">Also, after the call is canceled, the client code must wait for the completion notification and complete the call.</span></span> <span data-ttu-id="d4723-130">Die Funktion [**rpcasynccancelcallruft**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) einfach die Abschluss Benachrichtigung auf. Es ist kein Ersatz für den Abschluss des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="d4723-130">The [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) function simply rushes the completion notification; it is not a substitute for completing the call.</span></span>

<span data-ttu-id="d4723-131">Das folgende Code Fragment veranschaulicht, wie ein-Client Programm ein Ereignis verwenden kann, um auf eine asynchrone Antwort zu warten.</span><span class="sxs-lookup"><span data-stu-id="d4723-131">The following code fragment illustrates how a client program can use an event to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="d4723-132">Client Programme, die eine APC zum Empfangen von Benachrichtigungen über eine asynchrone Antwort verwenden, versetzen sich in der Regel in einen blockierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="d4723-132">Client programs that use an APC to receive notification of an asynchronous reply typically put themselves into a blocked state.</span></span> <span data-ttu-id="d4723-133">Dies wird im folgenden Code Fragment veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d4723-133">The following code fragment shows this.</span></span>


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="d4723-134">In diesem Fall wechselt das Client Programm in den Standbymodus und beansprucht keine CPU-Zyklen, bis die RPC-Lauf Zeit Bibliothek das APC aufruft (nicht angezeigt).</span><span class="sxs-lookup"><span data-stu-id="d4723-134">In this case, the client program goes to sleep, consuming no CPU cycles, until the RPC run-time library calls the APC (not shown).</span></span>

<span data-ttu-id="d4723-135">Das nächste Beispiel zeigt einen Client, der einen e/a-Abschlussport verwendet, um auf eine asynchrone Antwort zu warten.</span><span class="sxs-lookup"><span data-stu-id="d4723-135">The next example demonstrates a client that uses an I/O completion port to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="d4723-136">Im vorherigen Beispiel wartet der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Aufrufe unbegrenzt, bis der asynchrone Remote Prozedur Aufrufvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d4723-136">In the preceding example, the call to [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) waits indefinitely until the asynchronous remote procedure call completes.</span></span>

<span data-ttu-id="d4723-137">Beim Schreiben von Multithreadanwendungen kommt es zu einem möglichen Problem.</span><span class="sxs-lookup"><span data-stu-id="d4723-137">One potential pitfall occurs when writing multithreaded applications.</span></span> <span data-ttu-id="d4723-138">Wenn ein Thread einen Remote Prozedur Aufruf aufruft und dann beendet wird, bevor er benachrichtigt wird, dass der Sendevorgang abgeschlossen ist, kann der Remote Prozedur Aufruf fehlschlagen, und der Client-Stub kann die Verbindung mit dem Server schließen.</span><span class="sxs-lookup"><span data-stu-id="d4723-138">If a thread invokes a remote procedure call and then terminates before it receives notification that the send completed, the remote procedure call may fail and the client stub may close the connection to the server.</span></span> <span data-ttu-id="d4723-139">Daher sollten Threads, die eine Remote Prozedur aufzurufen, nicht beendet werden, bevor der-Rückruf abgeschlossen oder abgebrochen wird, wenn das Verhalten nicht erwünscht ist.</span><span class="sxs-lookup"><span data-stu-id="d4723-139">Therefore, threads that call a remote procedure should not terminate before the call is completed or canceled when behavior is undesirable.</span></span>

 

 