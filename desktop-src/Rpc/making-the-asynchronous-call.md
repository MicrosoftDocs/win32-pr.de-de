---
title: Ausführen des asynchronen Aufrufs
description: Bevor ein asynchroner Remoteaufruf ausgeführt werden kann, muss der Client das asynchrone Handle initialisieren. Client- und Serverprogramme verwenden Zeiger auf die RPC \_ ASYNC \_ STATE-Struktur für asynchrone Handles.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Remoteprozeduraufruf RPC , Aufgaben, asynchrone Aufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d8399071cae6ea39aaac3f966e7e799b2c93b32a152048a7d18282b465f929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928376"
---
# <a name="making-the-asynchronous-call"></a>Ausführen des asynchronen Aufrufs

Bevor ein asynchroner Remoteaufruf ausgeführt werden kann, muss der Client das asynchrone Handle initialisieren. Client- und Serverprogramme verwenden Zeiger auf die [**RPC \_ ASYNC \_ STATE-Struktur**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) für asynchrone Handles.

Jeder ausstehende Aufruf muss über ein eigenes eindeutiges asynchrones Handle verfügen. Der Client erstellt das Handle und übergibt es an die [**RpcAsyncInitializeHandle-Funktion.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) Damit der Aufruf ordnungsgemäß abgeschlossen wird, muss der Client sicherstellen, dass der Arbeitsspeicher für das Handle erst freigegeben wird, wenn er die asynchrone Antwort des Servers empfängt. Außerdem muss der Client das Handle erneut initialisieren, bevor ein weiterer Aufruf für ein vorhandenes asynchrones Handle erfolgt. Wenn dies nicht der Fall ist, kann der Clientstub während des Aufrufs eine Ausnahme auslösen. Der Client muss außerdem sicherstellen, dass die Puffer, die er für out-Parameter und in anfing, einer asynchronen Remoteprozedur zugeordnet bleiben, bis er die Antwort vom \[ [](/windows/desktop/Midl/out-idl) \] Server empfangen \[ [](/windows/desktop/Midl/in)  \] hat.

Wenn eine asynchrone Remoteprozedur aufgerufen wird, muss der Client die Methode auswählen, die die RPC-Laufzeitbibliothek verwendet, um sie über den Abschluss des Aufrufs zu benachrichtigen. Der Client kann diese Benachrichtigung auf eine der folgenden Arten empfangen:

-   Ereignis. Der Client kann ein Ereignis angeben, das ausgelöst werden soll, wenn der Aufruf abgeschlossen ist. Weitere Informationen finden Sie unter [Ereignisobjekte.](/windows/desktop/Sync/event-objects)
-   Abrufvorgang Der Client kann [**rpcAsyncGetCallStatus wiederholt aufrufen.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus) Wenn der Rückgabewert ein anderer Wert als RPC \_ S \_ ASYNC \_ CALL PENDING \_ ist, ist der Aufruf abgeschlossen. Diese Methode verwendet mehr CPU-Zeit als die anderen hier beschriebenen Methoden.
-   Apc. Der Client kann einen [asynchronen Prozeduraufruf (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) angeben, der aufgerufen wird, wenn der Aufruf abgeschlossen ist. Den Prototyp der APC-Funktion finden Sie unter [**RPCNOTIFICATION \_ ROUTINE**](/previous-versions/aa375808(v=vs.80)). Der APC wird aufgerufen, dessen Event-Parameter auf RpcCallComplete festgelegt ist. Damit APCs versendet werden können, muss sich der Clientthread in einem wartbaren Wartezustand befindet.

    Wenn das **Feld hThread** im asynchronen Handle auf 0 festgelegt ist, werden die APCs in der Warteschlange des Threads gespeichert, der den asynchronen Aufruf ausgeführt hat. Wenn der Wert ungleich 0 (null) ist, werden die APCs in der Warteschlange für den von m angegebenen Thread gespeichert.

-   Ioc. Der E/A-Abschlussport wird mit den im asynchronen Handle angegebenen Parametern benachrichtigt. Weitere Informationen finden Sie unter [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).
-   Windows Handle. Eine Nachricht wird an das angegebene Fensterhand handle (HWND) gesendet.

Das folgende Codefragment zeigt die wesentlichen Schritte, die erforderlich sind, um ein asynchrones Handle zu initialisieren und es für einen asynchronen Remoteprozeduraufruf zu verwenden.


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



Wie in diesem Beispiel veranschaulicht, kann Ihr Clientprogramm synchrone Remoteprozeduraufrufe ausführen, während ein asynchroner Prozeduraufruf noch aussteht. Dieser Client erstellt ein Ereignisobjekt für die RPC-Laufzeitbibliothek, um es zu benachrichtigen, wenn der asynchrone Aufruf abgeschlossen ist.

> [!Note]  
> Die Abschlussbenachrichtigung wird nicht von einer asynchronen RPC-Routine zurückgegeben, wenn während eines asynchronen Aufrufs eine RPC-Ausnahme ausgelöst wird.

 

 

 