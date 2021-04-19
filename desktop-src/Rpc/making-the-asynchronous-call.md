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
# <a name="making-the-asynchronous-call"></a>Ausführen des asynchronen Aufrufes

Bevor ein asynchroner Remote-Befehl durchgeführt werden kann, muss der Client das asynchrone handle initialisieren. Client-und Serverprogramme verwenden Zeiger auf die [**RPC- \_ Async- \_ Zustands**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) Struktur für asynchrone Handles.

Jeder ausstehende-Rückruf muss über ein eigenes, eindeutiges asynchrones handle verfügen. Der Client erstellt das Handle und übergibt es an die Funktion [**rpcasyncinitializehandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) . Damit der-Befehl ordnungsgemäß ausgeführt wird, muss der Client sicherstellen, dass der Arbeitsspeicher für das Handle erst freigegeben wird, wenn die asynchrone Antwort des Servers empfangen wird. Bevor ein anderer asynchroner Handle aufgerufen wird, muss der Client das Handle erneut initialisieren. Wenn dies nicht der Fall ist, kann der Clientstub eine Ausnahme während des Aufrufes auslösen. Außerdem muss der Client sicherstellen, dass die Puffer, die er für \[ [**out**](/windows/desktop/Midl/out-idl) \] -Parameter und \[ [**in**](/windows/desktop/Midl/in)- **out** - \] Parameter für eine asynchrone Remote Prozedur bereitstellt, zugewiesen bleiben, bis er die Antwort vom Server empfangen hat.

Wenn eine asynchrone Remote Prozedur aufgerufen wird, muss der Client die Methode auswählen, die von der RPC-Lauf Zeit Bibliothek verwendet wird, um Sie über den Abschluss des Aufrufs zu benachrichtigen. Der Client kann diese Benachrichtigung auf eine der folgenden Arten empfangen:

-   Veranstalter. Der Client kann ein Ereignis angeben, das bei Abschluss des Aufrufes ausgelöst werden soll. Weitere Informationen finden Sie unter [Event Objects](/windows/desktop/Sync/event-objects).
-   Abrufvorgang Der Client kann [**rpcasyncgetcallstatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)wiederholt aufrufen. Wenn der Rückgabewert etwas anderes als der RPC-asynchrone \_ \_ \_ Aufruf steht \_ aus, ist der Aufruf abgeschlossen. Diese Methode verwendet mehr CPU-Zeit als die anderen hier beschriebenen Methoden.
-   APC: Der Client kann einen [asynchronen Prozedur Aufruf (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) angeben, der aufgerufen wird, wenn der Aufruf abgeschlossen wird. Informationen zum Prototyp der APC-Funktion finden Sie unter [**rpcnotification- \_ Routine**](/previous-versions/aa375808(v=vs.80)). Der APC wird aufgerufen, wenn der Ereignis Parameter auf rpccallcomplete festgelegt ist. Damit APCs gesendet werden, muss sich der Client Thread in einem wartewartewartestatus befinden.

    Wenn das **hThread** -Feld im asynchronen Handle auf 0 festgelegt ist, werden die APCs auf dem Thread in die Warteschlange eingereiht, der den asynchronen-Befehl durchgeführt hat. Wenn Sie ungleich NULL ist, werden die APCs in den durch m angegebenen Thread eingereiht.

-   Bucht. Der e/a-Abschlussport wird mit den im asynchronen handle angegebenen Parametern benachrichtigt. Weitere Informationen finden Sie unter " [**kreateiocompletionport**](/windows/desktop/FileIO/createiocompletionport)".
-   Windows-handle. Eine Nachricht wird an das angegebene Fenster Handle (HWND) gesendet.

Das folgende Code Fragment zeigt die wesentlichen Schritte, die erforderlich sind, um ein asynchrones Handle zu initialisieren und dieses zum Ausführen eines asynchronen Remote Prozedur Aufrufes zu verwenden.


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



Wie in diesem Beispiel veranschaulicht, kann Ihr Client Programm synchrone Remote Prozedur Aufrufe ausführen, während ein asynchroner Prozedur Aufruf noch aussteht. Dieser Client erstellt ein Ereignis Objekt für die RPC-Lauf Zeit Bibliothek, das verwendet wird, um es zu benachrichtigen, wenn der asynchrone Aufruf abgeschlossen wird.

> [!Note]  
> Die Benachrichtigung über den Abschluss wird von einer asynchronen RPC-Routine nicht zurückgegeben, wenn während eines asynchronen Aufrufs eine RPC-Ausnahme ausgelöst wird.

 

 

 