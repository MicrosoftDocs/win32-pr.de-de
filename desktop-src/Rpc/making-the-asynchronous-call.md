---
title: Ausführen des asynchronen Aufrufes
description: Bevor ein asynchroner Remote-Befehl durchgeführt werden kann, muss der Client das asynchrone handle initialisieren. Client-und Serverprogramme verwenden Zeiger auf die RPC- \_ Async- \_ Zustands Struktur für asynchrone Handles.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Ausführen von asynchronen Aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338077"
---
# <a name="making-the-asynchronous-call"></a><span data-ttu-id="4fe55-105">Ausführen des asynchronen Aufrufes</span><span class="sxs-lookup"><span data-stu-id="4fe55-105">Making the Asynchronous Call</span></span>

<span data-ttu-id="4fe55-106">Bevor ein asynchroner Remote-Befehl durchgeführt werden kann, muss der Client das asynchrone handle initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4fe55-106">Before it can make an asynchronous remote call, the client must initialize the asynchronous handle.</span></span> <span data-ttu-id="4fe55-107">Client-und Serverprogramme verwenden Zeiger auf die [**RPC- \_ Async- \_ Zustands**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) Struktur für asynchrone Handles.</span><span class="sxs-lookup"><span data-stu-id="4fe55-107">Client and server programs use pointers to the [**RPC\_ASYNC\_STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) structure for asynchronous handles.</span></span>

<span data-ttu-id="4fe55-108">Jeder ausstehende-Rückruf muss über ein eigenes, eindeutiges asynchrones handle verfügen.</span><span class="sxs-lookup"><span data-stu-id="4fe55-108">Every outstanding call must have its own unique asynchronous handle.</span></span> <span data-ttu-id="4fe55-109">Der Client erstellt das Handle und übergibt es an die Funktion [**rpcasyncinitializehandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) .</span><span class="sxs-lookup"><span data-stu-id="4fe55-109">The client creates the handle and passes it to the [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) function.</span></span> <span data-ttu-id="4fe55-110">Damit der-Befehl ordnungsgemäß ausgeführt wird, muss der Client sicherstellen, dass der Arbeitsspeicher für das Handle erst freigegeben wird, wenn die asynchrone Antwort des Servers empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="4fe55-110">For the call to complete correctly, the client must ensure that the memory for the handle is not released until it receives the server's asynchronous reply.</span></span> <span data-ttu-id="4fe55-111">Bevor ein anderer asynchroner Handle aufgerufen wird, muss der Client das Handle erneut initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4fe55-111">Also, before making another call on an existing asynchronous handle, the client must reinitialize the handle.</span></span> <span data-ttu-id="4fe55-112">Wenn dies nicht der Fall ist, kann der Clientstub eine Ausnahme während des Aufrufes auslösen.</span><span class="sxs-lookup"><span data-stu-id="4fe55-112">Failure to do this can cause the client stub to raise an exception during the call.</span></span> <span data-ttu-id="4fe55-113">Außerdem muss der Client sicherstellen, dass die Puffer, die er für \[ [**out**](/windows/desktop/Midl/out-idl) \] -Parameter und \[ [**in**](/windows/desktop/Midl/in)- **out** - \] Parameter für eine asynchrone Remote Prozedur bereitstellt, zugewiesen bleiben, bis er die Antwort vom Server empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="4fe55-113">The client must also ensure that the buffers it supplies for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters and \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to an asynchronous remote procedure remain allocated until it has received the reply from the server.</span></span>

<span data-ttu-id="4fe55-114">Wenn eine asynchrone Remote Prozedur aufgerufen wird, muss der Client die Methode auswählen, die von der RPC-Lauf Zeit Bibliothek verwendet wird, um Sie über den Abschluss des Aufrufs zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="4fe55-114">When it invokes an asynchronous remote procedure, the client must select the method that the RPC run-time library will use to notify it of the call's completion.</span></span> <span data-ttu-id="4fe55-115">Der Client kann diese Benachrichtigung auf eine der folgenden Arten empfangen:</span><span class="sxs-lookup"><span data-stu-id="4fe55-115">The client can receive this notification in any one of the following ways:</span></span>

-   <span data-ttu-id="4fe55-116">Veranstalter.</span><span class="sxs-lookup"><span data-stu-id="4fe55-116">Event.</span></span> <span data-ttu-id="4fe55-117">Der Client kann ein Ereignis angeben, das bei Abschluss des Aufrufes ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fe55-117">The client can specify an event to be fired when the call has completed.</span></span> <span data-ttu-id="4fe55-118">Weitere Informationen finden Sie unter [Event Objects](/windows/desktop/Sync/event-objects).</span><span class="sxs-lookup"><span data-stu-id="4fe55-118">For details, see [Event Objects](/windows/desktop/Sync/event-objects).</span></span>
-   <span data-ttu-id="4fe55-119">Abrufvorgang</span><span class="sxs-lookup"><span data-stu-id="4fe55-119">Polling.</span></span> <span data-ttu-id="4fe55-120">Der Client kann [**rpcasyncgetcallstatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)wiederholt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4fe55-120">The client can repeatedly call [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="4fe55-121">Wenn der Rückgabewert etwas anderes als der RPC-asynchrone \_ \_ \_ Aufruf steht \_ aus, ist der Aufruf abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4fe55-121">If the return value is anything other than RPC\_S\_ASYNC\_CALL\_PENDING, the call is complete.</span></span> <span data-ttu-id="4fe55-122">Diese Methode verwendet mehr CPU-Zeit als die anderen hier beschriebenen Methoden.</span><span class="sxs-lookup"><span data-stu-id="4fe55-122">This method uses more CPU time than the other methods described here.</span></span>
-   <span data-ttu-id="4fe55-123">APC:</span><span class="sxs-lookup"><span data-stu-id="4fe55-123">APC.</span></span> <span data-ttu-id="4fe55-124">Der Client kann einen [asynchronen Prozedur Aufruf (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) angeben, der aufgerufen wird, wenn der Aufruf abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4fe55-124">The client can specify an [asynchronous procedure call (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) that gets called when the call completes.</span></span> <span data-ttu-id="4fe55-125">Informationen zum Prototyp der APC-Funktion finden Sie unter [**rpcnotification- \_ Routine**](/previous-versions/aa375808(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="4fe55-125">For the prototype of the APC function, see [**RPCNOTIFICATION\_ROUTINE**](/previous-versions/aa375808(v=vs.80)).</span></span> <span data-ttu-id="4fe55-126">Der APC wird aufgerufen, wenn der Ereignis Parameter auf rpccallcomplete festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4fe55-126">The APC is called with its Event parameter set to RpcCallComplete.</span></span> <span data-ttu-id="4fe55-127">Damit APCs gesendet werden, muss sich der Client Thread in einem wartewartewartestatus befinden.</span><span class="sxs-lookup"><span data-stu-id="4fe55-127">For APCs to get dispatched, the client thread must be in an alertable wait state.</span></span>

    <span data-ttu-id="4fe55-128">Wenn das **hThread** -Feld im asynchronen Handle auf 0 festgelegt ist, werden die APCs auf dem Thread in die Warteschlange eingereiht, der den asynchronen-Befehl durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="4fe55-128">If the **hThread** field in the asynchronous handle is set to 0, the APCs are queued on the thread that made the asynchronous call.</span></span> <span data-ttu-id="4fe55-129">Wenn Sie ungleich NULL ist, werden die APCs in den durch m angegebenen Thread eingereiht.</span><span class="sxs-lookup"><span data-stu-id="4fe55-129">If it is nonzero, the APCs are queued on the thread specified by m.</span></span>

-   <span data-ttu-id="4fe55-130">Bucht.</span><span class="sxs-lookup"><span data-stu-id="4fe55-130">IOC.</span></span> <span data-ttu-id="4fe55-131">Der e/a-Abschlussport wird mit den im asynchronen handle angegebenen Parametern benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="4fe55-131">The I/O completion port is notified with the parameters specified in the asynchronous handle.</span></span> <span data-ttu-id="4fe55-132">Weitere Informationen finden Sie unter " [**kreateiocompletionport**](/windows/desktop/FileIO/createiocompletionport)".</span><span class="sxs-lookup"><span data-stu-id="4fe55-132">For more information, see [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span></span>
-   <span data-ttu-id="4fe55-133">Windows-handle.</span><span class="sxs-lookup"><span data-stu-id="4fe55-133">Windows handle.</span></span> <span data-ttu-id="4fe55-134">Eine Nachricht wird an das angegebene Fenster Handle (HWND) gesendet.</span><span class="sxs-lookup"><span data-stu-id="4fe55-134">A message is posted to the specified window handle (HWND).</span></span>

<span data-ttu-id="4fe55-135">Das folgende Code Fragment zeigt die wesentlichen Schritte, die erforderlich sind, um ein asynchrones Handle zu initialisieren und dieses zum Ausführen eines asynchronen Remote Prozedur Aufrufes zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fe55-135">The following code fragment shows the essential steps required for initializing an asynchronous handle and using it to make an asynchronous remote procedure call.</span></span>


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



<span data-ttu-id="4fe55-136">Wie in diesem Beispiel veranschaulicht, kann Ihr Client Programm synchrone Remote Prozedur Aufrufe ausführen, während ein asynchroner Prozedur Aufruf noch aussteht.</span><span class="sxs-lookup"><span data-stu-id="4fe55-136">As this example demonstrates, your client program can execute synchronous remote procedure calls while an asynchronous procedure call is still pending.</span></span> <span data-ttu-id="4fe55-137">Dieser Client erstellt ein Ereignis Objekt für die RPC-Lauf Zeit Bibliothek, das verwendet wird, um es zu benachrichtigen, wenn der asynchrone Aufruf abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4fe55-137">This client creates an event object for the RPC run-time library to use to notify it when the asynchronous call completes.</span></span>

> [!Note]  
> <span data-ttu-id="4fe55-138">Die Benachrichtigung über den Abschluss wird von einer asynchronen RPC-Routine nicht zurückgegeben, wenn während eines asynchronen Aufrufs eine RPC-Ausnahme ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4fe55-138">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during an asynchronous call.</span></span>

 

 

 