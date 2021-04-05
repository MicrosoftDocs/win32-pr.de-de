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
# <a name="sending-the-asynchronous-reply"></a>Senden der asynchronen Antwort

Wenn der asynchrone Aufruf abgeschlossen ist, sendet der Server eine Antwort an den Client, indem er die Funktion [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) aufruft und das asynchrone handle übergibt. Dieser-Befehl ist auch dann erforderlich, wenn der asynchrone-Aufrufwert einen void-Rückgabewert und keine \[ out- \] Parameter aufweist. Wenn die Funktion über einen Rückgabewert verfügt, wird Sie als Verweis an **rpcasynccompletecallübergeben**.

Wenn der Server [**rpcasynccompletecallor**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) **rpcasyncabortcallaufruft** oder ein Aufruf abgeschlossen ist, weil eine Ausnahme in der Server-Manager-Routine ausgelöst wurde, zerstört die RPC-Lauf Zeit Bibliothek automatisch das asynchrone Handle des Servers.

> [!Note]  
> Der Server muss die Aktualisierung der \[ in-, out \] -und out-Parameter abschließen, \[ \] bevor **RpcAsyncCompleteCall** aufgerufen wird. An diesen Parametern oder dem asynchronen Handle können nach dem Aufrufen von **RpcAsyncCompleteCall** keine Änderungen vorgenommen werden. Wenn der **RpcAsyncCompleteCall-Funktionsaufruf** fehlschlägt, gibt die RPC-Laufzeit die Parameter frei.

 

Im folgenden Beispiel wird ein einfacher asynchroner Prozedur aufrufsvorgang veranschaulicht.


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



Der Einfachheit halber verarbeitet diese asynchrone Server Routine keine tatsächlichen Daten. Es ist einfach, sich für eine Weile in den Ruhezustand zu versetzen.

> [!Note]  
> Die **rpcasynccompletecallsfunktion** kann entweder auf dem Thread aufgerufen werden, der den Aufruf empfangen hat, oder auf einem beliebigen anderen Thread im Prozess. Wenn alle Daten, die zum Durchführen des Aufrufes erforderlich sind, sofort verfügbar sind, kann der Server Sie in demselben Thread auffüllen und **rpcasynccompletecallin** demselben Thread aufzurufen. Dieser Ansatz spart Kontextwechsel und verbessert die Leistung. Solche Aufrufe werden opportunistisch asynchron aufgerufen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**asynchroner RPC- \_ \_ Status**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**Rpcasynccompletecallcenter**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**Rpcasyncabortcallcenter**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**Rpcservertestcancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




