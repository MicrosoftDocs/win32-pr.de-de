---
title: Server seitige Dienst Vorgänge
description: In diesem Abschnitt werden Dienst seitige Dienst Vorgänge beschrieben.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Server seitige Service Operations-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391234"
---
# <a name="server-side-service-operations"></a><span data-ttu-id="19916-106">Server seitige Dienst Vorgänge</span><span class="sxs-lookup"><span data-stu-id="19916-106">Server Side Service Operations</span></span>

<span data-ttu-id="19916-107">In diesem Abschnitt werden Dienst seitige Dienst Vorgänge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19916-107">This section describes service side service operations.</span></span>


<span data-ttu-id="19916-108">Im folgenden finden Sie das Layout eines serverseitigen Dienst Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="19916-108">The following is the layout of a server side service operation</span></span>

-   <span data-ttu-id="19916-109">[ \_ \_ Kontext](ws-operation-context.md) Kontext Kontext des Konstanten WS-Vorgangs \* : der Vorgangs [Kontext](context.md).</span><span class="sxs-lookup"><span data-stu-id="19916-109">const [WS\_OPERATION\_CONTEXT](ws-operation-context.md)\* context: The operation [context](context.md).</span></span>
-   <span data-ttu-id="19916-110">Dienst Vorgangs Parameter: Parameter für den Dienst Vorgang.</span><span class="sxs-lookup"><span data-stu-id="19916-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="19916-111">konstanter [**WS- \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asynchroner Kontext AsyncContext: asynchroner Kontext für die asynchrone Ausführung der Dienst Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="19916-111">const [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)\* asyncContext: Async context for executing the service operations asynchronously.</span></span>
-   <span data-ttu-id="19916-112">[WS \_ Fehler](ws-error.md) \* Fehler: Rich Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="19916-112">[WS\_ERROR](ws-error.md)\* error: Rich error object.</span></span>

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a><span data-ttu-id="19916-113">Fehler-und Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="19916-113">Fault And Error Handling</span></span>

<span data-ttu-id="19916-114">Die Serverseite sollte Fehler verwenden, um Fehlerbedingungen an den Client zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="19916-114">The server side should use faults to deliver error conditions to the client.</span></span> <span data-ttu-id="19916-115">Dies ist möglich, indem ein fehlerhaftes HRESULT zurückgegeben und der Fehler in das Fehler Objekt eingebettet wird.</span><span class="sxs-lookup"><span data-stu-id="19916-115">It can do so by returning a failing HRESULT and embedding the fault in the error object.</span></span>

<span data-ttu-id="19916-116">Wenn der Fehler nicht für das Fehler Objekt festgelegt ist und ein HRESULT-Fehler zurückgegeben wird, versucht die Infrastruktur, einen Fehler an den Client zurückzusenden.</span><span class="sxs-lookup"><span data-stu-id="19916-116">If the fault is not set on the error object and a failure HRESULT is returned, the infrastructure will attempt deliver a fault back to client.</span></span> <span data-ttu-id="19916-117">Die Ebene der Details, die für den Client in einem solchen Fall offengelegt wird, wird von der [**WS- \_ Dienst \_ Eigenschaft \_ Fault \_ Disclosure**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) Service-Eigenschaft auf dem [Dienst Host](service-host.md)gesteuert.</span><span class="sxs-lookup"><span data-stu-id="19916-117">The level of details disclosed to the client in such a case is controlled by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) service property on the [Service Host](service-host.md).</span></span>

## <a name="call-completion"></a><span data-ttu-id="19916-118">Rückruf Abschluss</span><span class="sxs-lookup"><span data-stu-id="19916-118">Call Completion</span></span>

<span data-ttu-id="19916-119">Ein-Rückruf für einen synchronen serverseitigen Dienst Vorgang wird als "Complete" bezeichnet, wenn die Steuerung zurück an den Dienst Host zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="19916-119">A call on a synchronous server side service operation is said to be complete when either it has returned control back to the service host.</span></span> <span data-ttu-id="19916-120">Bei einem asynchronen Dienst Vorgang wird ein-Rückruf als beendet betrachtet, sobald die Rückruf Benachrichtigung von der Dienst Vorgangs Implementierung ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="19916-120">For an asynchronous service operation a call is considered complete once the callback notification is issued by the service operation implementation.</span></span>

## <a name="call-lifetime"></a><span data-ttu-id="19916-121">Lebensdauer von Anrufen</span><span class="sxs-lookup"><span data-stu-id="19916-121">Call Lifetime</span></span>

<span data-ttu-id="19916-122">Beim Implementieren eines serverseitigen Dienst Vorgangs über seine Lebensdauer muss besonders darauf geachtet werden.</span><span class="sxs-lookup"><span data-stu-id="19916-122">Special care should be taken when implementing a server side service operation about its lifetime.</span></span> <span data-ttu-id="19916-123">Die Lebensdauer eines Aufrufes kann sich stark darauf auswirken, wie lange der Dienst Host heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="19916-123">The lifetime of a call can greatly affect how long the service host takes to shutdown.</span></span>

<span data-ttu-id="19916-124">Wenn erwartet wird, dass ein serverseitiger Dienst Vorgang aufgrund eines e/a-gebundenen Vorgangs blockiert wird, wird empfohlen, einen Abbruch Rückruf so zu registrieren, dass er benachrichtigt wird, wenn der Dienst Host abgebrochen wird oder wenn die zugrunde liegende Verbindung vom Client geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="19916-124">If a server side service operation is expected to block because of some IO bound operation, it is recommended that it registers a cancellation callback such that it is notified if when service host is being aborted, or when the underlying connection is closed by the client.</span></span>

## <a name="server-side-service-operations-and-memory-consideration"></a><span data-ttu-id="19916-125">Server seitige Dienst Vorgänge und Arbeitsspeicher Überlegungen</span><span class="sxs-lookup"><span data-stu-id="19916-125">Server side service operations and memory consideration</span></span>

<span data-ttu-id="19916-126">Wenn ein Dienst Vorgang Arbeitsspeicher für die ausgehenden Parameter zuweisen muss, sollte er das [WS- \_ Heap](ws-heap.md) Objekt verwenden, das über den [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="19916-126">If a service operation needs to allocate memory for its outgoing parameters, it should use [WS\_HEAP](ws-heap.md) object available to it through the [WS\_OPERATION\_CONTEXT](ws-operation-context.md).</span></span>

<span data-ttu-id="19916-127">Beispiel: Dienst Vorgang und WS- \_ Heap</span><span class="sxs-lookup"><span data-stu-id="19916-127">Example: Service Operation and WS\_HEAP</span></span>

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a><span data-ttu-id="19916-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="19916-128">Return Values</span></span>

-   <span data-ttu-id="19916-129">WS \_ S Async: der-Vorgang wird asynchron \_ abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="19916-129">WS\_S\_ASYNC: Call will be completed async.</span></span>
-   <span data-ttu-id="19916-130">WS \_ S- \_ Ende: der-Vorgang wurde erfolgreich abgeschlossen, der Server erwartet außerhalb dieses Aufrufes keine [WS- \_ Nachricht](ws-message.md) vom Client.</span><span class="sxs-lookup"><span data-stu-id="19916-130">WS\_S\_END: Call completed successfully, the server is not expecting any [WS\_MESSAGE](ws-message.md) from the client beyond this call.</span></span> <span data-ttu-id="19916-131">Wenn eine andere WS-Nachricht empfangen wird, \_ sollte der Server den Kanal abbrechen.</span><span class="sxs-lookup"><span data-stu-id="19916-131">If another WS\_MESSAGE comes in then the server should abort the channel.</span></span>
-   <span data-ttu-id="19916-132">NoError/alle anderen Erfolgs-HRESULTs: der Rückruf wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="19916-132">NOERROR/All other success HRESULTS: Call completed successfully.</span></span> <span data-ttu-id="19916-133">Beachten Sie, dass die Anwendung für einen erfolgreichen Abschluss des Dienst Vorgangs kein anderes HRESULT-Ergebnis als noError zurückgeben sollte.</span><span class="sxs-lookup"><span data-stu-id="19916-133">Note that it is recommended that the application should not return HRESULT other then NOERROR for successful completion of service operation.</span></span>
-   <span data-ttu-id="19916-134">Alles mit einem Fehler HRESULT: ein Fehler wird an den Client zurückgesendet, wenn ein Fehler in WS- \_ Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="19916-134">Everything with a failure HRESULT: A fault is send back to the client if one is available in WS\_ERROR.</span></span> <span data-ttu-id="19916-135">Andernfalls wird ein generischer Fehler zurück an den Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="19916-135">Otherwise a generic fault is send back to the client.</span></span> <span data-ttu-id="19916-136">Siehe Fehler Diskussion weiter oben.</span><span class="sxs-lookup"><span data-stu-id="19916-136">See fault discussion above.</span></span>

<span data-ttu-id="19916-137">Siehe, [Abbruch des Aufrufes](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="19916-137">See, [Call cancellation](call-cancellation.md).</span></span>

 

 




