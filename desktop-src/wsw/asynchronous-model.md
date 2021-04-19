---
title: Asynchrones Modell
description: Die meisten Vorgänge in der Windows-Webdienste-API können synchron oder asynchron ausgeführt werden.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Asynchrone modellweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341659"
---
# <a name="asynchronous-model"></a><span data-ttu-id="8dc37-106">Asynchrones Modell</span><span class="sxs-lookup"><span data-stu-id="8dc37-106">Asynchronous Model</span></span>

<span data-ttu-id="8dc37-107">Die meisten Vorgänge in der Windows-Webdienste-API können synchron oder asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8dc37-107">Most operations in Windows Web Services API can be performed synchronously or asynchronously.</span></span> <span data-ttu-id="8dc37-108">Um eine Funktion synchron aufzurufen, übergeben Sie einen NULL-Wert für die asynchrone [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="8dc37-108">To call a function synchronously, pass a null value for the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="8dc37-109">Um anzugeben, dass eine Funktion asynchron ausgeführt werden kann, übergeben Sie einen nicht-NULL- **WS- \_ Async- \_ Kontext** an die Funktion.</span><span class="sxs-lookup"><span data-stu-id="8dc37-109">To specify that a function may be performed asynchronously, pass a non-null **WS\_ASYNC\_CONTEXT** to the function.</span></span>

<span data-ttu-id="8dc37-110">Wenn eine Funktion asynchron aufgerufen wird, kann Sie dennoch synchron oder asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8dc37-110">When called asynchronously, a function can nevertheless complete synchronously or asynchronously.</span></span> <span data-ttu-id="8dc37-111">Wenn die Funktion synchron abgeschlossen wird, gibt Sie einen Wert zurück, der den endgültigen Erfolg oder Fehler angibt, und dieser Wert ist immer etwas anderes als **WS \_ S \_ Async** (siehe [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="8dc37-111">If the function completes synchronously, it returns a value that indicates the final success or error, and this value is always something other than **WS\_S\_ASYNC** (See [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span> <span data-ttu-id="8dc37-112">Der Rückgabewert von **WS \_ S \_ Async** gibt jedoch an, dass die Funktion asynchron vollständig ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc37-112">A return value of **WS\_S\_ASYNC**, however, indicates that the function will complete asynchronously.</span></span> <span data-ttu-id="8dc37-113">Wenn die Funktion asynchron abgeschlossen wird, wird ein Rückruf aufgerufen, um den Abschluss des Vorgangs zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="8dc37-113">When the function completes asynchronously, a callback is invoked to signal completion of the operation.</span></span> <span data-ttu-id="8dc37-114">Dieser Rückruf gibt den endgültigen Erfolg oder Fehlerwert an.</span><span class="sxs-lookup"><span data-stu-id="8dc37-114">This callback indicates the final success or error value.</span></span> <span data-ttu-id="8dc37-115">Der Rückruf wird nicht aufgerufen, wenn der Vorgang synchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8dc37-115">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="8dc37-116">Um einen asynchronen Kontext zu erstellen, initialisieren Sie die Felder **Callback** und **callbackstate** der [**Kontext Struktur WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="8dc37-116">To create an asynchronous context, initialize the **callback** and **callbackState** fields of the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="8dc37-117">Das Feld **callbackstate** wird verwendet, um einen Zeiger auf benutzerdefinierte Daten anzugeben, die an die [**WS \_ Async- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) Funktion übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8dc37-117">The **callbackState** field is used to specify a pointer to user-defined data which is passed to the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) function.</span></span>

<span data-ttu-id="8dc37-118">Das folgende Beispiel zeigt, wie Sie eine Funktion asynchron aufrufen, indem Sie einen Zeiger an eine asynchrone [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur übergeben, die den Rückruf und einen Zeiger auf die Zustandsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="8dc37-118">The following example shows calling a function asynchronously by passing a pointer to a [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure that contains the callback and a pointer to the state data.</span></span>

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

<span data-ttu-id="8dc37-119">Die asynchrone [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur wird von der asynchronen Funktion nur für die Dauer des Funktions Aufrufes verwendet (nicht für die Dauer des asynchronen Vorgangs), sodass Sie Sie sicher auf dem Stapel deklarieren können.</span><span class="sxs-lookup"><span data-stu-id="8dc37-119">The [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure is used by the asynchronous function only for the duration of the function call (not for the duration of the asynchronous operation), so you can safely declare it on the stack.</span></span>

<span data-ttu-id="8dc37-120">Wenn andere Parameter Außer der asynchronen [**WS- \_ \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Struktur an eine asynchrone Funktion als Zeiger übergeben werden und die Funktion asynchron abgeschlossen wird, liegt es in der Verantwortung des Aufrufers, die Werte, auf die diese Parameter zeigen, so lange zu speichern, bis der asynchrone Rückruf aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8dc37-120">If any other parameters, besides the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure, are passed to an asynchronous function as pointers and the function completes asynchronously, it is the responsibility of the caller to keep the values pointed to by these parameters alive (not freed) until the asynchronous callback is invoked.</span></span>

<span data-ttu-id="8dc37-121">Es gibt Einschränkungen hinsichtlich der Vorgänge, die ein Rückruf ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="8dc37-121">There are limitations on what operations a callback may perform.</span></span> <span data-ttu-id="8dc37-122">Weitere Informationen zu möglichen Vorgängen finden Sie im [**WS- \_ Rückruf \_ Modell**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span><span class="sxs-lookup"><span data-stu-id="8dc37-122">For more information on possible operations , see the [**WS\_CALLBACK\_MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span></span>

<span data-ttu-id="8dc37-123">Wenn Sie eine asynchrone Funktion implementieren, rufen Sie den Rückruf nicht für denselben Thread auf, der die asynchrone Funktion aufgerufen hat, bevor die asynchrone Funktion an den Aufrufer zurückgegeben wurde, da dadurch das asynchrone Modell gestört wird.</span><span class="sxs-lookup"><span data-stu-id="8dc37-123">When you implement an asynchronous function, do not invoke the callback on the same thread that called the asynchronous function before the asynchronous function has returned to the caller, as this disrupts the asynchronous model.</span></span>

<span data-ttu-id="8dc37-124">Wenn Sie eine Funktion implementieren, die eine Reihe von asynchronen Vorgängen ausführen muss, sollten Sie ggf. die [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) -Hilfsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="8dc37-124">When implementing a function that needs to execute a series of asynchronous operations, consider using the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper function.</span></span>

<span data-ttu-id="8dc37-125">Das [Beispiel für eine asynchrone Funktion](asyncmodelexample.md) zeigt, wie Funktionen implementiert und genutzt werden, die dem asynchronen Modell folgen.</span><span class="sxs-lookup"><span data-stu-id="8dc37-125">The [Asynchronous Function Example](asyncmodelexample.md) shows how to implement and consume functions that follow the asynchronous model.</span></span>

<span data-ttu-id="8dc37-126">Beim Starten eines asynchronen e/a-Vorgangs werden Systemressourcen beansprucht.</span><span class="sxs-lookup"><span data-stu-id="8dc37-126">Starting an asynchronous IO operation consumes system resources.</span></span> <span data-ttu-id="8dc37-127">Wenn genügend e/a-Vorgänge gestartet werden, kann das System nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="8dc37-127">If enough IO operations are started, the system can become unresponsive.</span></span> <span data-ttu-id="8dc37-128">Um dies zu verhindern, muss eine Anwendung die Anzahl der asynchronen Vorgänge, die gestartet werden, einschränken.</span><span class="sxs-lookup"><span data-stu-id="8dc37-128">To prevent this, an application needs to limit the number of asynchronous operations that it starts.</span></span>

<span data-ttu-id="8dc37-129">Das asynchrone Modell verwendet die folgenden API-Elemente.</span><span class="sxs-lookup"><span data-stu-id="8dc37-129">The asynchronous model uses the following API elements.</span></span>

| <span data-ttu-id="8dc37-130">Rückruf</span><span class="sxs-lookup"><span data-stu-id="8dc37-130">Callback</span></span>                                         | <span data-ttu-id="8dc37-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dc37-131">Description</span></span>                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dc37-132">**WS \_ Async- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="8dc37-132">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | <span data-ttu-id="8dc37-133">Der Rückruf Funktionsparameter, der mit dem asynchronen Modell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8dc37-133">The callback function parameter used with the asynchronous model.</span></span>                                                                     |
| [<span data-ttu-id="8dc37-134">**WS \_ Async- \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="8dc37-134">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | <span data-ttu-id="8dc37-135">Wird zusammen mit [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) verwendet, um die nächste Funktion anzugeben, die in einer Reihe von asynchronen Vorgängen aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dc37-135">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |



 



| <span data-ttu-id="8dc37-136">Enumeration</span><span class="sxs-lookup"><span data-stu-id="8dc37-136">Enumeration</span></span>                                      | <span data-ttu-id="8dc37-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8dc37-137">Description</span></span>                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dc37-138">**WS- \_ Rückruf \_ Modell**</span><span class="sxs-lookup"><span data-stu-id="8dc37-138">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | <span data-ttu-id="8dc37-139">Gibt das Threading Verhalten eines Rückrufs an (z. b. einen [**WS \_ Async- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span><span class="sxs-lookup"><span data-stu-id="8dc37-139">Specifies the threading behavior of a callback (for example, a [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span></span> |



 



| <span data-ttu-id="8dc37-140">Funktion</span><span class="sxs-lookup"><span data-stu-id="8dc37-140">Function</span></span>                                 | <span data-ttu-id="8dc37-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dc37-141">Description</span></span>                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dc37-142">**Wsasyncexecute**</span><span class="sxs-lookup"><span data-stu-id="8dc37-142">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | <span data-ttu-id="8dc37-143">Ruft einen benutzerdefinierten Rückruf auf, der einen asynchronen Vorgang initiieren kann und eine Funktion angibt, die aufgerufen werden soll, wenn der asynchrone Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8dc37-143">Invokes a user-defined callback which can initiate an asynchronous operation and indicate a function that should be called when the asynchronous operation has been completed.</span></span> |



 



| <span data-ttu-id="8dc37-144">Struktur</span><span class="sxs-lookup"><span data-stu-id="8dc37-144">Structure</span></span>                                          | <span data-ttu-id="8dc37-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dc37-145">Description</span></span>                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dc37-146">**asynchroner WS- \_ \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="8dc37-146">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | <span data-ttu-id="8dc37-147">Gibt den asynchronen Rückruf und einen Zeiger auf benutzerdefinierte Daten an, die an den asynchronen Rückruf übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8dc37-147">Specifies the asynchronous callback and a pointer to user-defined data, which will be passed to the asynchronous callback.</span></span>            |
| [<span data-ttu-id="8dc37-148">**WS \_ Async- \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="8dc37-148">**WS\_ASYNC\_OPERATION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | <span data-ttu-id="8dc37-149">Wird zusammen mit [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) verwendet, um die nächste Funktion anzugeben, die in einer Reihe von asynchronen Vorgängen aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dc37-149">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |
| [<span data-ttu-id="8dc37-150">**WS- \_ Async- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="8dc37-150">**WS\_ASYNC\_STATE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | <span data-ttu-id="8dc37-151">Wird von [**wsasyncexecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) verwendet, um den Status eines asynchronen Vorgangs zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8dc37-151">Used by [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to manage the state of an asynchronous operation.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="8dc37-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8dc37-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dc37-153">Beispiel für eine asynchrone Funktion</span><span class="sxs-lookup"><span data-stu-id="8dc37-153">Asynchronous Function Example</span></span>](asyncmodelexample.md)
</dt> <dt>

[<span data-ttu-id="8dc37-154">**WS \_ Async- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="8dc37-154">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[<span data-ttu-id="8dc37-155">**asynchroner WS- \_ \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="8dc37-155">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[<span data-ttu-id="8dc37-156">**WS- \_ Rückruf \_ Modell**</span><span class="sxs-lookup"><span data-stu-id="8dc37-156">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[<span data-ttu-id="8dc37-157">**Wsasyncexecute**</span><span class="sxs-lookup"><span data-stu-id="8dc37-157">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




