---
title: Clientseitige Dienstvorgänge
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: Weitere Informationen finden Sie unter Clientseitige Dienstvorgänge.
keywords:
- Clientseitige Dienstvorgänge Webdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73ccbb0c742d0be09570b0959c9c1a663d7f4d0f054cc88070d842ac6d954ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657300"
---
# <a name="client-side-service-operations"></a>Clientseitige Dienstvorgänge

Im Folgenden finden Sie das Layout eines clientseitigen Dienstvorgang:

-   [WS \_ SERVICE \_ PROXY](ws-service-proxy.md) \* serviceProxy: Der [Dienstproxy](service-proxy.md) für den Aufruf.
-   [WS \_ ](ws-heap.md) \* HEAP-Heap: Ein erforderlicher Heap, der für die Serialisierung und Deserialisierung von [WS \_ MESSAGE verwendet wird.](ws-message.md)
-   Dienstbetriebsparameter: Parameter für den Dienstvorgang.
-   [**Aufrufeigenschaften und ihre Anzahl:**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)Ein Array von Aufrufeigenschaften.
-   [**Anzahl**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) der Aufrufeigenschaften: Die Anzahl der Aufrufeigenschaften.
-   [**WS \_ ASYNC \_ CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: asynchroner Kontext zum asynchronen Ausführen des Aufrufs.
-   [WS \_ FEHLERfehler:](ws-error.md) Umfangreiches Fehlerobjekt.


### <a name="signature-for-client-side-service-operations"></a>Signatur für clientseitige Dienstvorgänge

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>Überlegungen zum Arbeitsspeicher für clientseitige Dienstvorgänge

Beim Aufruf des Dienstvorgang wird ein [ \_ WS-HEAP](ws-heap.md) \* als Parameter verwendet. Dies ist ein erforderlicher Parameter, der für die Serialisierung/Deserialisierung von Nachrichtentexten in Parameter verwendet wird.

Die Anwendung muss [**WsResetHeap aufrufen,**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) unabhängig davon, ob der Aufruf erfolgreich war. Wenn der Aufruf erfolgreich war und über ausgehende Parameter verfügt, sollte die Anwendung **WsResetHeap** sofort aufrufen, nachdem er mit den ausgehenden Parametern abgeschlossen wurde.

Die Anwendung sollte mit WsAlloc Arbeitsspeicher für in- und [**out-Parameter zuweisen.**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) Der Dienstproxy muss sie möglicherweise neu zufinden, damit bereitgestellte Zeiger überschrieben werden. Ein Versuch, solchen Arbeitsspeicher frei zu geben, verursacht einen Absturz der Anwendung.

### <a name="client-side-service-operation-and-ws_heap"></a>Clientseitiger Dienstvorgang und \_ WS-HEAP

``` syntax
HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessReceipt(orderReceipt);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderMemo, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessMemo(orderMemo);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
```

### <a name="error-parameter"></a>Fehlerparameter

Die Anwendung sollte den Fehlerparameter immer an Folgenden übergeben:

-   Rufen Sie umfassende Fehlerinformationen ab, wenn während des Dienstvorgangaufrufs ein Fehler auftritt.
-   Get the fault object if the service returned a fault. (Das Fehlerobjekt wird zurückgegeben, wenn der Dienst einen Fehler zurückgegeben hat.) Der Fehler ist im Fehlerobjekt enthalten. In diesem Fall ist der vom Dienstvorgang zurückgegebene **HRESULT-Wert** **WS E ENDPOINT FAULT \_ \_ \_ \_ RECEIVED** (siehe Windows [Webdienste-Rückgabewerte).](windows-web-services-return-values.md)

### <a name="call-properties-for-client-side-service-operations"></a>Aufrufeigenschaften für clientseitige Dienstvorgänge

Aufrufeigenschaften ermöglichen es einer Anwendung, benutzerdefinierte Einstellungen für einen bestimmten Aufruf anzugeben. Derzeit ist nur eine Aufrufeigenschaft mit dem Dienstmodell [**verfügbar: WS \_ CALL PROPERTY CALL \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

``` syntax
WS_CALL_PROPERTY callProperties[1] = {0};
callProperties[0].id = WS_CALL_PROPERTY_CALL_ID;
callProperties[0].value = 5;

HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt,  callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;
//:
//:
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderReceipt, callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;

//:
//:
//:
// On a separate thread 
// In this case both the calls belong to call group 5, and will abandon as a result of the call to WsAbandonCall. 
hr = WsAbandonCall(serviceProxy, 5, error);
```

### <a name="abandoning-a-call"></a>Verabbruch eines Anrufs

Häufig ist es wünschenswert, die Ergebnisse eines Aufrufs aufzugeben, um das Steuerelement an die Anwendung zurückzugeben, damit die tatsächliche Aufrufvervollständigung von der Infrastruktur verarbeitet wird. Der Dienstproxy stellt diese Möglichkeit über [**WsAbproxynCall zur Verfügung.**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

Beachten Sie, dass das Steuerelement an den Aufrufer möglicherweise nicht sofort zurück gegeben wird. Die einzige Garantie, die die Dienstproxylaufzeit bietet, ist, dass sie nicht auf den Abschluss eines E/A-gebundenen Vorgangs warten würde, bevor sie die Kontrolle an den Aufrufer zurückgibt.

Aufrufe für einen clientseitigen Dienstvorgang können durch einen Aufruf von [**WsAbcall abgebrochen werden.**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall) Es werden ein Dienstproxy und eine Anruf-ID verwendet. Eine Aufruf-ID wird als Teil einer Aufrufeigenschaften für einen Dienstvorgang angegeben.

Wenn die Aufruf-ID 0 ist, verläss der Dienstproxy alle ausstehenden Aufrufe in dieser Instanz.

### <a name="call-timeouts"></a>Timeouts für Aufrufe

Standardmäßig ist für einen Dienstproxy für jeden Aufruf ein Timeout von 30 Sekunden festgelegt. Das Timeout für einen Aufruf kann durch die [**WS \_ PROXY PROPERTY \_ CALL \_ \_ TIMEOUT-Dienstproxyeigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) geändert werden, wenn ein Dienstproxy über [**WsCreateServiceProxy erstellt wird.**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)

Nach Erreichen eines Timeouts wird der Aufruf abgebrochen.

### <a name="return-values"></a>Rückgabewerte

Alle **erfolgreichen HRESULT-Werte** müssen als erfolgreich behandelt werden, und alle Fehlerwerte müssen als Fehler behandelt werden. Im Folgenden finden Sie einige **der HRESULT-Werte,** die eine Anwendung erwarten kann:

-   **WS \_ S \_ ASYNC:** Der Aufruf wird asynchron abgeschlossen.
-   NOERROR: Der Aufruf wurde erfolgreich abgeschlossen.
-   **WS \_ E \_ OPERATION \_ ABANDONED**: Der Aufruf wurde abgebrochen. Das Fehlerobjekt enthält den Grund für den Abbruch.
-   **WS \_ E \_ \_ UNGÜLTIGER VORGANG:** Der Dienstproxy befindet sich nicht in einem geeigneten Zustand, um einen Aufruf zu führen. Überprüfen Sie den Dienstproxystatus, um den Status des Dienstproxys zu finden.

Eine vollständige Liste der Rückgabewerte finden Sie unter Windows [Webdienste-Rückgabewerte.](windows-web-services-return-values.md)

### <a name="code-examples"></a>Codebeispiele

Codebeispiele finden Sie in den folgenden Themen:

-   [CallAbillenExample](callabandonexample.md)
-   [**WsAbcall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




