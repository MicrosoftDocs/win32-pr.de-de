---
title: Senden der asynchronen Antwort
description: Wenn der asynchrone Aufruf abgeschlossen ist, sendet der Server eine Antwort an den Client, indem er die RpcAsyncCompleteCall-Funktion aufruft und ihr das asynchrone Handle über gibt.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdcaf4db4a27a49a8025596668893518c6b6c577a0d81d91189a44ec81df4de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925578"
---
# <a name="sending-the-asynchronous-reply"></a>Senden der asynchronen Antwort

Wenn der asynchrone Aufruf abgeschlossen ist, sendet der Server eine Antwort an den Client, indem er die [**RpcAsyncCompleteCall-Funktion**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) aufruft und ihr das asynchrone Handle über gibt. Dieser Aufruf ist auch dann erforderlich, wenn der asynchrone Aufruf über einen void-Rückgabewert und keine \[ out-Parameter \] verfügt. Wenn die Funktion über einen Rückgabewert verfügt, wird sie als Verweis an **RpcAsyncCompleteCall übergeben.**

Wenn der Server [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) oder **RpcAsyncAbortCall** aufruft oder ein Aufruf abgeschlossen wird, weil eine Ausnahme in der Server-Manager-Routine ausgelöst wurde, zerstört die RPC-Laufzeitbibliothek automatisch das asynchrone Handle des Servers.

> [!Note]  
> Der Server muss die Aktualisierung der \[ Parameter in, out und out beenden, \] bevor \[ \] **RpcAsyncCompleteCall aufgerufen wird.** Nach dem Aufruf von **RpcAsyncCompleteCall** können keine Änderungen an diesen Parametern oder am asynchronen Handle vorgenommen werden. Wenn der **RpcAsyncCompleteCall-Funktionsaufruf** fehlschlägt, gibt die RPC-Laufzeit die Parameter frei.

 

Im folgenden Beispiel wird ein einfacher asynchroner Prozeduraufruf veranschaulicht.


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



Der Einfachheit halber werden von dieser asynchronen Serverroutine keine tatsächlichen Daten verarbeiten. Sie versetzt sich einfach eine Weile in den Ruhezustand.

> [!Note]  
> Die **RpcAsyncCompleteCall-Funktion** kann entweder für den Thread, der den Aufruf empfangen hat, oder für einen anderen Thread im Prozess aufgerufen werden. Wenn alle daten, die zum Abschließen des Aufrufs erforderlich sind, sofort verfügbar sind, kann der Server sie im selben Thread ausfüllen und **rpcAsyncCompleteCall** im gleichen Thread aufrufen. Dieser Ansatz spart Kontextwechsel und verbessert die Leistung. Solche Aufrufe werden als "asynchron" bezeichnet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_RPC-ASYNCHRONER \_ ZUSTAND**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




