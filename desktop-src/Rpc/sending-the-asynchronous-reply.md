---
title: Senden der asynchronen Antwort
description: Wenn der asynchrone Aufruf abgeschlossen ist, sendet der Server eine Antwort an den Client, indem er die Funktion RpcAsyncCompleteCall aufruft und das asynchrone handle übergibt.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037413"
---
# <a name="sending-the-asynchronous-reply"></a><span data-ttu-id="4da09-103">Senden der asynchronen Antwort</span><span class="sxs-lookup"><span data-stu-id="4da09-103">Sending the Asynchronous Reply</span></span>

<span data-ttu-id="4da09-104">Wenn der asynchrone Aufruf abgeschlossen ist, sendet der Server eine Antwort an den Client, indem er die Funktion [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) aufruft und das asynchrone handle übergibt.</span><span class="sxs-lookup"><span data-stu-id="4da09-104">When the asynchronous call is complete, the server sends a reply to the client by calling the [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) function and passing it the asynchronous handle.</span></span> <span data-ttu-id="4da09-105">Dieser-Befehl ist auch dann erforderlich, wenn der asynchrone-Aufrufwert einen void-Rückgabewert und keine \[ out- \] Parameter aufweist.</span><span class="sxs-lookup"><span data-stu-id="4da09-105">This call is necessary even if the asynchronous call has a void return value and no \[out\] parameters.</span></span> <span data-ttu-id="4da09-106">Wenn die Funktion über einen Rückgabewert verfügt, wird Sie als Verweis an **rpcasynccompletecallübergeben**.</span><span class="sxs-lookup"><span data-stu-id="4da09-106">If the function has a return value, it is passed by reference to **RpcAsyncCompleteCall**.</span></span>

<span data-ttu-id="4da09-107">Wenn der Server [**rpcasynccompletecallor**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) **rpcasyncabortcallaufruft** oder ein Aufruf abgeschlossen ist, weil eine Ausnahme in der Server-Manager-Routine ausgelöst wurde, zerstört die RPC-Lauf Zeit Bibliothek automatisch das asynchrone Handle des Servers.</span><span class="sxs-lookup"><span data-stu-id="4da09-107">When the server calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) or **RpcAsyncAbortCall**, or a call completes because an exception was raised in the server-manager routine, the RPC run-time library automatically destroys the server's asynchronous handle.</span></span>

> [!Note]  
> <span data-ttu-id="4da09-108">Der Server muss die Aktualisierung der \[ in-, out \] -und out-Parameter abschließen, \[ \] bevor **RpcAsyncCompleteCall** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4da09-108">The server must finish updating the \[in, out\] and \[out\] parameters before calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="4da09-109">An diesen Parametern oder dem asynchronen Handle können nach dem Aufrufen von **RpcAsyncCompleteCall** keine Änderungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="4da09-109">No changes can be made to those parameters or to the asynchronous handle after calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="4da09-110">Wenn der **RpcAsyncCompleteCall-Funktionsaufruf** fehlschlägt, gibt die RPC-Laufzeit die Parameter frei.</span><span class="sxs-lookup"><span data-stu-id="4da09-110">If the **RpcAsyncCompleteCall** function call fails, the RPC runtime frees the parameters.</span></span>

 

<span data-ttu-id="4da09-111">Im folgenden Beispiel wird ein einfacher asynchroner Prozedur aufrufsvorgang veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4da09-111">The following example demonstrates a simple asynchronous procedure call.</span></span>


```C++
#define DEFAULT_ASYNC_DELAY 20;
#define ASYNC_CANCEL_CHECK 100;

void AsyncFunc(IN PRPC_ASYNC_STATE pAsync,
               IN RPC_BINDING_HANDLE hBinding,
               IN OUT unsigned long nAsychDelay)
{
    int nReply = 1;
    RPC_STATUS status;
    unsigned long nTmpAsychDelay;
    int i;
 
    if (nAsychDelay < 0){
        nAsychDelay = DEFAULT_ASYNC_DELAY;
    }else if (nAsychDelay < 100){
        nAsychDelay = 100;
    }

    // We only call RpcServerTestCancel if the call
    // takes longer than ASYNC_CANCEL_CHECK ms
    if(nAsychDelay > ASYNC_CANCEL_CHECK){
        
        nTmpAsychDelay = nAsychDelay/100;
 
        for (i = 0; i < 100; i++){
            Sleep(nTmpAsychDelay);
 
            if (i%5 == 0){
                fprintf(stderr, 
                        "\rRunning AsyncFunc (%lu ms) (%d%c) ... ",
                        nAsychDelay, i+5, PERCENT);
 
                status = 
                    RpcServerTestCancel(
                        RpcAsyncGetCallHandle(pAsync));
                if (status == RPC_S_OK){
                    fprintf(stderr, 
                            "\nAsyncFunc has been canceled!!!\n");
                    break;
                }else if (status != RPC_S_CALL_IN_PROGRESS){
                    printf(
                        "RpcAsyncInitializeHandle returned 0x%x\n", 
                        status);
                    exit(status); 
                }
            }
        }
    }else{
        Sleep(nAsychDelay);
    }
 
    printf("\nCalling RpcAsyncCompleteCall\n");
    status = RpcAsyncCompleteCall(pAsync, &nReply);
    printf("RpcAsyncCompleteCall returned 0x%x\n", status);
    if (status){
        exit(status);
    }
}
```



<span data-ttu-id="4da09-112">Der Einfachheit halber verarbeitet diese asynchrone Server Routine keine tatsächlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="4da09-112">For the sake of simplicity, this asynchronous server routine does not process actual data.</span></span> <span data-ttu-id="4da09-113">Es ist einfach, sich für eine Weile in den Ruhezustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="4da09-113">It simply puts itself to sleep for awhile.</span></span>

> [!Note]  
> <span data-ttu-id="4da09-114">Die **rpcasynccompletecallsfunktion** kann entweder auf dem Thread aufgerufen werden, der den Aufruf empfangen hat, oder auf einem beliebigen anderen Thread im Prozess.</span><span class="sxs-lookup"><span data-stu-id="4da09-114">The **RpcAsyncCompleteCall** function can be called either on the thread that received the call, or on any other thread in the process.</span></span> <span data-ttu-id="4da09-115">Wenn alle Daten, die zum Durchführen des Aufrufes erforderlich sind, sofort verfügbar sind, kann der Server Sie in demselben Thread auffüllen und **rpcasynccompletecallin** demselben Thread aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4da09-115">If all the data necessary to complete the call are readily available, the server may fill them in on the same thread, and call the **RpcAsyncCompleteCall** on the same thread.</span></span> <span data-ttu-id="4da09-116">Dieser Ansatz spart Kontextwechsel und verbessert die Leistung.</span><span class="sxs-lookup"><span data-stu-id="4da09-116">This approach saves some context switching and improves performance.</span></span> <span data-ttu-id="4da09-117">Solche Aufrufe werden opportunistisch asynchron aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4da09-117">Such calls are called opportunistically asynchronous.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4da09-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4da09-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da09-119">**asynchroner RPC- \_ \_ Status**</span><span class="sxs-lookup"><span data-stu-id="4da09-119">**RPC\_ASYNC\_STATE**</span></span>](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[<span data-ttu-id="4da09-120">**Rpcasynccompletecallcenter**</span><span class="sxs-lookup"><span data-stu-id="4da09-120">**RpcAsyncCompleteCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[<span data-ttu-id="4da09-121">**Rpcasyncabortcallcenter**</span><span class="sxs-lookup"><span data-stu-id="4da09-121">**RpcAsyncAbortCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[<span data-ttu-id="4da09-122">**Rpcservertestcancel**</span><span class="sxs-lookup"><span data-stu-id="4da09-122">**RpcServerTestCancel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




