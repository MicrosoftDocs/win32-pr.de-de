---
title: Client seitige Dienst Vorgänge
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: Weitere Informationen zu Client seitigen Dienst Vorgängen
keywords:
- Client seitige Service Operations-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd00bfbd832db12a722363bf5b1af8f7298345
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216950"
---
# <a name="client-side-service-operations"></a>Client seitige Dienst Vorgänge

Im folgenden finden Sie das Layout eines Client seitigen Dienst Vorgangs:

-   [WS \_ Dienst \_ Proxy Dienst](ws-service-proxy.md) \* Proxy: der [Dienst Proxy](service-proxy.md) für den-Befehl.
-   [WS \_ Heap](ws-heap.md) \* Heap: ein erforderlicher Heap, der für die Text Serialisierung und Deserialisierung der [WS- \_ Nachricht](ws-message.md)verwendet wird.
-   Dienst Vorgangs Parameter: Parameter für den Dienst Vorgang.
-   [**Callteigenschaften und ihre Anzahl**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): ein Array von Aufrufeigenschaften.
-   Anzahl von [**aufrufseigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : die Anzahl der aufrufseigenschaften.
-   [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Asynchroner Kontext AsyncContext: asynchroner Kontext für die asynchrone Ausführung des Aufrufes.
-   [WS \_ Fehler](ws-error.md) Fehler: Rich Error-Objekt.


### <a name="signature-for-client-side-service-operations"></a>Signatur für Client seitige Dienst Vorgänge

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>Überlegungen zum Arbeitsspeicher für Client seitige Dienst Vorgänge

Der Aufrufen des Dienst Vorgangs nimmt einen [WS- \_ Heap](ws-heap.md) \* als Parameter an. Dies ist ein erforderlicher Parameter, der für die Serialisierung/Deserialisierung von Nachrichten Texten zu Parametern verwendet wird.

Die Anwendung muss [**wsresethap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) abrufen, unabhängig davon, ob der Befehl erfolgreich ausgeführt wurde. Wenn der-Befehl erfolgreich ausgeführt wurde und über ausgehende Parameter verfügt, sollte die Anwendung **wsresethap** sofort nach dem Abschluss mit den ausgehenden Parametern abrufen.

Die Anwendung sollte Arbeitsspeicher für in-und out-Parameter mit [**wsalloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)zuweisen. Der Dienst Proxy muss Sie möglicherweise neu zuordnen, damit die bereitgestellten Zeiger überschrieben werden. Der Versuch, diesen Speicher freizugeben, führt zu einem Absturz der Anwendung.

### <a name="client-side-service-operation-and-ws_heap"></a>Client seitiger Dienst Vorgang und WS- \_ Heap

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

### <a name="error-parameter"></a>Error-Parameter

Die Anwendung sollte immer den Error-Parameter an übergeben:

-   Wenn während des Vorgangs des Dienst Vorgangs ein Fehler auftritt, erhalten Sie umfassende Fehlerinformationen.
-   Das Fault-Objekt wird zurückgegeben, wenn der Dienst einen Fehler zurückgegeben hat. Der Fehler ist im Error-Objekt enthalten. In diesem Fall ist der vom Dienst Vorgang zurückgegebene **HRESULT** -Wert **WS \_ E \_ EndPoint \_ Fault \_** (siehe [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md)).

### <a name="call-properties-for-client-side-service-operations"></a>Ruft Eigenschaften für Client seitige Dienst Vorgänge auf.

Mit den Eigenschaften "Aufrufe" kann eine Anwendung benutzerdefinierte Einstellungen für einen bestimmten-Befehl angeben. Derzeit ist nur eine "Callcenter"-Eigenschaft mit dem Dienstmodell, der [**WS- \_ aufrufsaufrufskennung \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id), verfügbar.

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

### <a name="abandoning-a-call"></a>Abbrechen eines Aufrufes

Häufig ist es wünschenswert, die Ergebnisse eines Aufrufes zu verwerfen, damit das Steuerelement wieder an die Anwendung zurückgibt, sodass der tatsächliche Rückruf Vorgang von der Infrastruktur verarbeitet wird. Der Dienst Proxy stellt diese Funktion über [**wsabandoncallbereit**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).

Beachten Sie, dass das Steuerelement für den Aufrufer möglicherweise nicht sofort zurückgegeben wird. die einzige Garantie, die die Dienst Proxy Laufzeit erteilt, besteht darin, dass es nicht auf den Abschluss eines e/a-gebundenen Vorgangs wartet, bevor er die Steuerung an den Aufrufer zurückgibt

Aufrufe für einen Client seitigen Dienst Vorgang können mithilfe eines Aufrufs von [**wsabandoncallcenter**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)abgebrochen werden. Er nimmt einen Dienst Proxy und eine-ID an. Eine Anrufe-ID wird als Teil einer aufrufseigenschaft für einen Dienst Vorgang angegeben.

Wenn die Aufruf-ID 0 ist, wird der Dienst Proxy alle ausstehenden Aufrufe dieser Instanz verwerfen.

### <a name="call-timeouts"></a>Timeouts aufrufen

Standardmäßig hat ein Dienst Proxy für jeden-Befehl ein Timeout von 30 Sekunden. Das Timeout für einen-Befehl kann von der [**WS \_ - \_ Proxy \_ Eigenschaft \_ Timeout**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) -Dienst Proxy Eigenschaft beim Erstellen eines Dienst Proxys über [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)geändert werden.

Nachdem ein Timeout erreicht wurde, wird der-Rückruf abgebrochen.

### <a name="return-values"></a>Rückgabewerte

Alle **HRESULT** -Erfolgs Werte müssen als Erfolg behandelt werden, und alle Fehler Werte müssen als Fehler behandelt werden. Im folgenden finden Sie einige der **HRESULT** -Werte, die eine Anwendung erwarten kann:

-   **WS \_ S \_ Async**: der-Vorgang wird asynchron abgeschlossen.
-   NoError: der Rückruf wurde erfolgreich abgeschlossen.
-   **WS \_ E- \_ Vorgang \_ abgebrochen**: der-Rückruf wurde abgebrochen. Das Error-Objekt enthält den Grund für den Abbruch.
-   **WS \_ E \_ ungültiger \_ Vorgang**: der Dienst Proxy befindet sich nicht in einem geeigneten Zustand zum Ausführen eines Aufrufens. Überprüfen Sie den Status des Dienst Proxys, um den Status des Dienst Proxys zu ermitteln.

Eine komplette Liste der Rückgabewerte finden Sie unter [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md).

### <a name="code-examples"></a>Codebeispiele

Codebeispiele finden Sie unter:

-   [Callabandon-Beispiel](callabandonexample.md)
-   [**Wsabandoncall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




