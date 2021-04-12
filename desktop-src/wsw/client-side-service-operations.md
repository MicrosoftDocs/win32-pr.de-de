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
# <a name="client-side-service-operations"></a><span data-ttu-id="95897-106">Client seitige Dienst Vorgänge</span><span class="sxs-lookup"><span data-stu-id="95897-106">Client-side Service Operations</span></span>

<span data-ttu-id="95897-107">Im folgenden finden Sie das Layout eines Client seitigen Dienst Vorgangs:</span><span class="sxs-lookup"><span data-stu-id="95897-107">The following is the layout of a client-side service operation:</span></span>

-   <span data-ttu-id="95897-108">[WS \_ Dienst \_ Proxy Dienst](ws-service-proxy.md) \* Proxy: der [Dienst Proxy](service-proxy.md) für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="95897-108">[WS\_SERVICE\_PROXY](ws-service-proxy.md)\* serviceProxy: The [service proxy](service-proxy.md) for the call.</span></span>
-   <span data-ttu-id="95897-109">[WS \_ Heap](ws-heap.md) \* Heap: ein erforderlicher Heap, der für die Text Serialisierung und Deserialisierung der [WS- \_ Nachricht](ws-message.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95897-109">[WS\_HEAP](ws-heap.md)\* heap: A required heap used for body serialization and deserialization of the [WS\_MESSAGE](ws-message.md).</span></span>
-   <span data-ttu-id="95897-110">Dienst Vorgangs Parameter: Parameter für den Dienst Vorgang.</span><span class="sxs-lookup"><span data-stu-id="95897-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="95897-111">[**Callteigenschaften und ihre Anzahl**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): ein Array von Aufrufeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95897-111">[**Call Properties and their count**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): An array of call properties.</span></span>
-   <span data-ttu-id="95897-112">Anzahl von [**aufrufseigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : die Anzahl der aufrufseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95897-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) property count: The count of call properties.</span></span>
-   <span data-ttu-id="95897-113">[**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Asynchroner Kontext AsyncContext: asynchroner Kontext für die asynchrone Ausführung des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="95897-113">[**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: Async context for executing the call asynchronously.</span></span>
-   <span data-ttu-id="95897-114">[WS \_ Fehler](ws-error.md) Fehler: Rich Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95897-114">[WS\_ERROR](ws-error.md) error: Rich error object.</span></span>


### <a name="signature-for-client-side-service-operations"></a><span data-ttu-id="95897-115">Signatur für Client seitige Dienst Vorgänge</span><span class="sxs-lookup"><span data-stu-id="95897-115">Signature for Client-side Service Operations</span></span>

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a><span data-ttu-id="95897-116">Überlegungen zum Arbeitsspeicher für Client seitige Dienst Vorgänge</span><span class="sxs-lookup"><span data-stu-id="95897-116">Memory Considerations for Client-side Service Operations</span></span>

<span data-ttu-id="95897-117">Der Aufrufen des Dienst Vorgangs nimmt einen [WS- \_ Heap](ws-heap.md) \* als Parameter an.</span><span class="sxs-lookup"><span data-stu-id="95897-117">The call to the service operation takes a [WS\_HEAP](ws-heap.md)\* as parameter.</span></span> <span data-ttu-id="95897-118">Dies ist ein erforderlicher Parameter, der für die Serialisierung/Deserialisierung von Nachrichten Texten zu Parametern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95897-118">This is a required parameter used for serialization/deserialization of message bodies to parameters.</span></span>

<span data-ttu-id="95897-119">Die Anwendung muss [**wsresethap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) abrufen, unabhängig davon, ob der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="95897-119">The application must call [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) whether the call succeeded or not.</span></span> <span data-ttu-id="95897-120">Wenn der-Befehl erfolgreich ausgeführt wurde und über ausgehende Parameter verfügt, sollte die Anwendung **wsresethap** sofort nach dem Abschluss mit den ausgehenden Parametern abrufen.</span><span class="sxs-lookup"><span data-stu-id="95897-120">If the call succeeded and it has outgoing parameters, the application should call **WsResetHeap** immediately after it is finished with the outgoing parameters.</span></span>

<span data-ttu-id="95897-121">Die Anwendung sollte Arbeitsspeicher für in-und out-Parameter mit [**wsalloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)zuweisen.</span><span class="sxs-lookup"><span data-stu-id="95897-121">The application should allocate memory for in and out parameters with [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span></span> <span data-ttu-id="95897-122">Der Dienst Proxy muss Sie möglicherweise neu zuordnen, damit die bereitgestellten Zeiger überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="95897-122">The service proxy may need to reallocate them so provided pointers will be overwritten.</span></span> <span data-ttu-id="95897-123">Der Versuch, diesen Speicher freizugeben, führt zu einem Absturz der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="95897-123">An attempt to free such memory will cause the application to crash.</span></span>

### <a name="client-side-service-operation-and-ws_heap"></a><span data-ttu-id="95897-124">Client seitiger Dienst Vorgang und WS- \_ Heap</span><span class="sxs-lookup"><span data-stu-id="95897-124">Client-side Service Operation and WS\_HEAP</span></span>

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

### <a name="error-parameter"></a><span data-ttu-id="95897-125">Error-Parameter</span><span class="sxs-lookup"><span data-stu-id="95897-125">Error parameter</span></span>

<span data-ttu-id="95897-126">Die Anwendung sollte immer den Error-Parameter an übergeben:</span><span class="sxs-lookup"><span data-stu-id="95897-126">The application should always pass in the error parameter to:</span></span>

-   <span data-ttu-id="95897-127">Wenn während des Vorgangs des Dienst Vorgangs ein Fehler auftritt, erhalten Sie umfassende Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="95897-127">Get rich error information if a failure occurs during the service operation call.</span></span>
-   <span data-ttu-id="95897-128">Das Fault-Objekt wird zurückgegeben, wenn der Dienst einen Fehler zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="95897-128">Get the fault object if the service returned back a fault.</span></span> <span data-ttu-id="95897-129">Der Fehler ist im Error-Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="95897-129">The fault is contained in the error object.</span></span> <span data-ttu-id="95897-130">In diesem Fall ist der vom Dienst Vorgang zurückgegebene **HRESULT** -Wert **WS \_ E \_ EndPoint \_ Fault \_** (siehe [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="95897-130">In this case, the **HRESULT** value returned from the service operation is **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** (see [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span>

### <a name="call-properties-for-client-side-service-operations"></a><span data-ttu-id="95897-131">Ruft Eigenschaften für Client seitige Dienst Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="95897-131">Call Properties for Client-side Service Operations</span></span>

<span data-ttu-id="95897-132">Mit den Eigenschaften "Aufrufe" kann eine Anwendung benutzerdefinierte Einstellungen für einen bestimmten-Befehl angeben.</span><span class="sxs-lookup"><span data-stu-id="95897-132">Call properties allow an application to specify custom settings for a given call.</span></span> <span data-ttu-id="95897-133">Derzeit ist nur eine "Callcenter"-Eigenschaft mit dem Dienstmodell, der [**WS- \_ aufrufsaufrufskennung \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id), verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95897-133">Currently, only one call property is available with the service model, [**WS\_CALL\_PROPERTY\_CALL\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span></span>

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

### <a name="abandoning-a-call"></a><span data-ttu-id="95897-134">Abbrechen eines Aufrufes</span><span class="sxs-lookup"><span data-stu-id="95897-134">Abandoning a Call</span></span>

<span data-ttu-id="95897-135">Häufig ist es wünschenswert, die Ergebnisse eines Aufrufes zu verwerfen, damit das Steuerelement wieder an die Anwendung zurückgibt, sodass der tatsächliche Rückruf Vorgang von der Infrastruktur verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="95897-135">It is often desirable to abandon the results of a call in order to relinquish the control back to the application, such that the actual call completion is handled by the infrastructure.</span></span> <span data-ttu-id="95897-136">Der Dienst Proxy stellt diese Funktion über [**wsabandoncallbereit**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="95897-136">Service proxy provides this facility through [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span>

<span data-ttu-id="95897-137">Beachten Sie, dass das Steuerelement für den Aufrufer möglicherweise nicht sofort zurückgegeben wird. die einzige Garantie, die die Dienst Proxy Laufzeit erteilt, besteht darin, dass es nicht auf den Abschluss eines e/a-gebundenen Vorgangs wartet, bevor er die Steuerung an den Aufrufer zurückgibt</span><span class="sxs-lookup"><span data-stu-id="95897-137">Note that the control to the caller may not be given back immediately, the only guarantee that the service proxy runtime gives is that it would not wait for any I/O bound operation to complete before it gives control back to the caller.</span></span>

<span data-ttu-id="95897-138">Aufrufe für einen Client seitigen Dienst Vorgang können mithilfe eines Aufrufs von [**wsabandoncallcenter**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="95897-138">Calls on a client side service operation can be abandoned by means of a call to [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span> <span data-ttu-id="95897-139">Er nimmt einen Dienst Proxy und eine-ID an. Eine Anrufe-ID wird als Teil einer aufrufseigenschaft für einen Dienst Vorgang angegeben.</span><span class="sxs-lookup"><span data-stu-id="95897-139">It takes a service proxy and a call id. A call Id is given as part of a call properties on a service operation.</span></span>

<span data-ttu-id="95897-140">Wenn die Aufruf-ID 0 ist, wird der Dienst Proxy alle ausstehenden Aufrufe dieser Instanz verwerfen.</span><span class="sxs-lookup"><span data-stu-id="95897-140">If the call Id is 0, then the service proxy will abandon all pending calls at that instance.</span></span>

### <a name="call-timeouts"></a><span data-ttu-id="95897-141">Timeouts aufrufen</span><span class="sxs-lookup"><span data-stu-id="95897-141">Call Timeouts</span></span>

<span data-ttu-id="95897-142">Standardmäßig hat ein Dienst Proxy für jeden-Befehl ein Timeout von 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="95897-142">By default a service proxy has a 30 second timeout for every call.</span></span> <span data-ttu-id="95897-143">Das Timeout für einen-Befehl kann von der [**WS \_ - \_ Proxy \_ Eigenschaft \_ Timeout**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) -Dienst Proxy Eigenschaft beim Erstellen eines Dienst Proxys über [**wscreateserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="95897-143">The timeout on a call can be changed by [**WS\_PROXY\_PROPERTY\_CALL\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) service proxy property when creating a service proxy through [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span></span>

<span data-ttu-id="95897-144">Nachdem ein Timeout erreicht wurde, wird der-Rückruf abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="95897-144">After a timeout is reached, the call is abandoned.</span></span>

### <a name="return-values"></a><span data-ttu-id="95897-145">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="95897-145">Return Values</span></span>

<span data-ttu-id="95897-146">Alle **HRESULT** -Erfolgs Werte müssen als Erfolg behandelt werden, und alle Fehler Werte müssen als Fehler behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="95897-146">All success **HRESULT** values must be treated as success, and all failure values must be treated as failures.</span></span> <span data-ttu-id="95897-147">Im folgenden finden Sie einige der **HRESULT** -Werte, die eine Anwendung erwarten kann:</span><span class="sxs-lookup"><span data-stu-id="95897-147">The following are some of the **HRESULT** values that an application can expect:</span></span>

-   <span data-ttu-id="95897-148">**WS \_ S \_ Async**: der-Vorgang wird asynchron abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="95897-148">**WS\_S\_ASYNC**: Call will be completed asynchronously.</span></span>
-   <span data-ttu-id="95897-149">NoError: der Rückruf wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="95897-149">NOERROR: Call completed successfully.</span></span>
-   <span data-ttu-id="95897-150">**WS \_ E- \_ Vorgang \_ abgebrochen**: der-Rückruf wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="95897-150">**WS\_E\_OPERATION\_ABANDONED**: The call has been abandoned.</span></span> <span data-ttu-id="95897-151">Das Error-Objekt enthält den Grund für den Abbruch.</span><span class="sxs-lookup"><span data-stu-id="95897-151">The error object contains the reason for abandon.</span></span>
-   <span data-ttu-id="95897-152">**WS \_ E \_ ungültiger \_ Vorgang**: der Dienst Proxy befindet sich nicht in einem geeigneten Zustand zum Ausführen eines Aufrufens. Überprüfen Sie den Status des Dienst Proxys, um den Status des Dienst Proxys zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="95897-152">**WS\_E\_INVALID\_OPERATION**: The service proxy is not in an appropriate state to make a call, check the service proxy state to figure out the state of the service proxy.</span></span>

<span data-ttu-id="95897-153">Eine komplette Liste der Rückgabewerte finden Sie unter [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="95897-153">For a complete list of return values, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

### <a name="code-examples"></a><span data-ttu-id="95897-154">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="95897-154">Code Examples</span></span>

<span data-ttu-id="95897-155">Codebeispiele finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="95897-155">For code examples, see the following:</span></span>

-   [<span data-ttu-id="95897-156">Callabandon-Beispiel</span><span class="sxs-lookup"><span data-stu-id="95897-156">CallAbandonExample</span></span>](callabandonexample.md)
-   [<span data-ttu-id="95897-157">**Wsabandoncall**</span><span class="sxs-lookup"><span data-stu-id="95897-157">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




