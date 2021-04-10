---
title: Server seitige asynchrone Pipe-Verarbeitung
description: Die Manager-Routine einer asynchronen Funktion empfängt immer das asynchrone Handle als ersten Parameter.
ms.assetid: ddf9c319-6c4d-4de1-ab29-0ef9b76531ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b0f11372090f1fd181c0d7272aa1446e5e3d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039099"
---
# <a name="server-side-asynchronous-pipe-handling"></a>Server seitige asynchrone Pipe-Verarbeitung

Die Manager-Routine einer asynchronen Funktion empfängt immer das asynchrone Handle als ersten Parameter. Der Server verwendet dieses Handle zum Senden der Antwort und zum Senden der ausgehenden Pipe-Daten, sobald diese verfügbar sind. Das Handle bleibt gültig, bis [**rpcasynccompletecalldarauf**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) aufgerufen wird, der Aufruf von [**rpcasyncabortcallcenter**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)abgebrochen wird oder eine Ausnahme in der Manager-Routine auftritt. Die Anwendung muss alle Zeiger der obersten Ebene für die \[ **out** - \] und in- \[ **, out** -Parameter nachverfolgen \] , um Sie vor Abschluss des Aufrufes zu aktualisieren. Die Anwendung muss außerdem die \[ [**in**](/windows/desktop/Midl/in) \] -und Out- \[ [](/windows/desktop/Midl/out-idl) \] Pipes verfolgen.

Der Server sendet asynchrone pipedaten auf die gleiche Weise wie der Client. Weitere Informationen finden Sie unter [Client seitige asynchrone Pipe-Verarbeitung](client-side-asynchronous-pipe-handling.md).

Der Server empfängt asynchrone pipedaten auf die gleiche Weise wie der Client. Wenn der Empfangs Mechanismus asynchrone Prozedur Aufrufe (APCs) ist, muss der Server ein Thread handle (in pAsync->u. APC. hThread) angeben und das asynchrone Handle mit der Lauf Zeit Bibliothek registrieren.

## <a name="example"></a>Beispiel

In diesem Beispiel behandelt die Server-Manager-Routine myasyncpipefunc den Remote Prozedur Aufrufe vom Client.


```C++
typedef struct 
{
    PRPC_ASYNC_STATE pAsync;
    ASYNC_INTPIPE *inpipe;
    ASYNC_INTPIPE *outpipe;
    int i;
    int *b;
    int PipeBuffer[ASYNC_CHUNK_SIZE];
} PIPE_CALL_COOKIE;
 
void MyAsyncPipeFunc(
    IN PRPC_ASYNC_STATE pAsync,
    IN RPC_BINDING_HANDLE hBinding,
    IN int a,
    IN ASYNC_INTPIPE *inpipe,
    OUT ASYNC_INTPIPE *outpipe,
    OUT int *b)
{
    unsigned long ThreadIdentifier;
    HANDLE HandleToThread;
    PIPE_CALL_COOKIE *PipeCallCookie;
 
    PipeCallCookie = new PIPE_CALL_COOKIE;
    PipeCallCookie->pAsync = pAsync;
    PipeCallCookie->inpipe = inpipe;
    PipeCallCookie->outpipe = outpipe;
    PipeCallCookie->b = b;
 
    pAsync->u.APC.hThread = 0;
    pAsync->u.APC.hThread = CreateThread(
                                0, DefaultThreadStackSize,
                                (LPTHREAD_START_ROUTINE)   
                                ThreadProcPipes,
                                PipeCallCookie, 0,
                                &ThreadIdentifier);
}// endMyAsyncPipeFunc
 
//Sending pipe data
//This APC routine is called when a pipe send completes, 
//or when an asynchronous call completes. 
 
//This thread routine receives pipe data, processes the call, 
//sends the reply back to the client, and 
//completes the asynchronous call.
 
void ThreadProcPipes(IN PIPE_CALL_COOKIE  *Cookie)
{
    int *ptr ;
    int  n ;
    int retval ;
 
    while (pAsync->u.APC.hThread == 0)
    {
        Sleep(10);
    }
 
    pAsync->Flags = RPC_C_NOTIFY_ON_SEND_COMPLETE;
    pAsync->UserInfo = (void *) PipeCallCookie;
    pAsync->NotificationType = RpcNotificationTypeApc;
    pAsync->u.APC.NotificationRoutine = MyAsyncPipeAPCRoutine;
    pAsync->u.APC.hThread = HandleToThread;
 
    RpcAsyncRegisterHandle(pAsync);
 
    while (!fDone)
    {
        Cookie->inpipe->pull(
            Cookie->inpipe.state,
            (int *) Cookie->PipeBuffer,
            ASYNC_CHUNK_SIZE,
            &num_elements);
        switch (Status)
        {
            case RPC_S_ASYNC_CALL_PENDING:
                if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
                {
                    RpcRaiseException(APP_ERROR) ;
                }
            break;
 
            case RPC_S_OK:
                if (num_elements == 0)
                {
                    fDone = 1;
                }
                else
                {
                    // process the received data
                }
            break;
 
            default:
                fDone = 1;
            break;
        }
    }
 
    Cookie->i = 1;
    Cookie->outpipe->push(
        Cookie->outpipe.state,
        0,
        Cookie->PipeBuffer,
        ASYNC_CHUNK_SIZE) ;
 
    while (Cookie->i < ASYNC_NUM_CHUNKS+1)
    {
        if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
        {
            RpcRaiseException (APP_ERROR);
        }
    }
    // sending non pipe reply
    *(Cookie->b) = 10;
    Status = RpcAsyncCompleteCall (Cookie->pAsync, &retval);
}
 
void MyAsyncPipeAPCRoutine (
    IN PRPC_ASYNC_STATE pAsync,
    IN void *Context,
    IN unsigned int Flags)
{
    PIPE_CALL_COOKIE *Cookie = (PIPE_CALL_COOKIE *) pAsync->UserInfo;
 
    if (Flags & RPC_ASYNC_PIPE_SEND_COMPLETE)
    {
        if (Cookie->i & ASYNC_NUM_CHUNKS)
        {
            Cookie->outpipe->push(
                Cookie->outpipe.state,
                0,
                (int *) Cookie->PipeBuffer,
                ASYNC_CHUNK_SIZE);
            Cookie->i++ ;
        }
        else
        {
            pAsync->Flags = 0;
            Cookie->outpipe->push(Cookie->outpipe.state, 0, 0, 0);
            Cookie->i++;
        }
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipes](pipes.md)
</dt> <dt>

[Asynchrone Mittell](/windows/desktop/Midl/async)
</dt> <dt>

[Server seitiges asynchrones RPC](server-side-asynchronous-rpc.md)
</dt> </dl>

 

 