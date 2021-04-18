---
description: Aufrufen von asynchronen Methoden
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Aufrufen von asynchronen Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524643"
---
# <a name="calling-asynchronous-methods"></a><span data-ttu-id="394ee-103">Aufrufen von asynchronen Methoden</span><span class="sxs-lookup"><span data-stu-id="394ee-103">Calling Asynchronous Methods</span></span>

<span data-ttu-id="394ee-104">In Media Foundation werden viele Vorgänge asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="394ee-104">In Media Foundation, many operations are performed asynchronously.</span></span> <span data-ttu-id="394ee-105">Asynchrone Vorgänge können die Leistung verbessern, da Sie den aufrufenden Thread nicht blockieren.</span><span class="sxs-lookup"><span data-stu-id="394ee-105">Asynchronous operations can improve performance, because they do not block the calling thread.</span></span> <span data-ttu-id="394ee-106">Ein asynchroner Vorgang in Media Foundation wird durch ein paar von Methoden definiert, wobei die Benennungs Konvention **BEGIN...** und **End....**</span><span class="sxs-lookup"><span data-stu-id="394ee-106">An asynchronous operation in Media Foundation is defined by a pair of methods with the naming convention **Begin...** and **End....**.</span></span> <span data-ttu-id="394ee-107">Zusammen definieren diese beiden Methoden einen asynchronen Lesevorgang für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="394ee-107">Together, these two methods define an asynchronous read operation on the stream.</span></span>

<span data-ttu-id="394ee-108">Um einen asynchronen Vorgang zu starten, müssen Sie die **Begin** -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="394ee-108">To start an asynchronous operation, call the **Begin** method.</span></span> <span data-ttu-id="394ee-109">Die **Begin** -Methode enthält immer mindestens zwei Parameter:</span><span class="sxs-lookup"><span data-stu-id="394ee-109">The **Begin** method always contains at least two parameters:</span></span>

-   <span data-ttu-id="394ee-110">Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="394ee-110">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="394ee-111">Die Anwendung muss diese Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="394ee-111">The application must implement this interface.</span></span>
-   <span data-ttu-id="394ee-112">Ein Zeiger auf ein optionales Zustands Objekt.</span><span class="sxs-lookup"><span data-stu-id="394ee-112">A pointer to an optional state object.</span></span>

<span data-ttu-id="394ee-113">Die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle benachrichtigt die Anwendung, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="394ee-113">The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface notifies the application when the operation is completed.</span></span> <span data-ttu-id="394ee-114">Ein Beispiel für die Implementierung dieser Schnittstelle finden Sie unter [Implementieren des asynchronen Rückrufs](implementing-the-asynchronous-callback.md).</span><span class="sxs-lookup"><span data-stu-id="394ee-114">For an example of how to implement this interface, see [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md).</span></span> <span data-ttu-id="394ee-115">Das Zustands Objekt ist optional.</span><span class="sxs-lookup"><span data-stu-id="394ee-115">The state object is optional.</span></span> <span data-ttu-id="394ee-116">Wenn angegeben, muss die **IUnknown** -Schnittstelle implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="394ee-116">If specified, it must implement the **IUnknown** interface.</span></span> <span data-ttu-id="394ee-117">Sie können das State-Objekt verwenden, um alle Zustandsinformationen zu speichern, die von Ihrem Rückruf benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="394ee-117">You can use the state object to store any state information that is needed by your callback.</span></span> <span data-ttu-id="394ee-118">Wenn Sie keine Zustandsinformationen benötigen, können Sie diesen Parameter auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="394ee-118">If you do not need state information, you can set this parameter to **NULL**.</span></span> <span data-ttu-id="394ee-119">Die **Begin** -Methode kann zusätzliche Parameter enthalten, die für diese Methode spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="394ee-119">The **Begin** method might contain additional parameters that are specific to that method.</span></span>

<span data-ttu-id="394ee-120">Wenn die **Begin** -Methode einen Fehlercode zurückgibt, bedeutet dies, dass der Vorgang sofort fehlgeschlagen ist und der Rückruf nicht aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="394ee-120">If the **Begin** method returns a failure code, it means the operation has failed immediately, and the callback will not be invoked.</span></span> <span data-ttu-id="394ee-121">Wenn die **Begin** -Methode erfolgreich ist, bedeutet dies, dass der Vorgang aussteht und der Rückruf aufgerufen wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="394ee-121">If the **Begin** method succeeds, it means the operation is pending, and the callback will be invoked when the operation completes.</span></span>

<span data-ttu-id="394ee-122">Die [**IMF Bytestream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) -Methode startet z. b. einen asynchronen Lesevorgang für einen Bytestream:</span><span class="sxs-lookup"><span data-stu-id="394ee-122">For example, the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) method starts an asynchronous read operation on a byte stream:</span></span>


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



<span data-ttu-id="394ee-123">Die Rückruf Methode ist [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="394ee-123">The callback method is [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="394ee-124">Er verfügt über einen einzelnen Parameter, *pasynkresult*, der ein Zeiger auf die [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="394ee-124">It has a single parameter, *pAsyncResult*, which is a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="394ee-125">Um den asynchronen Vorgang abzuschließen, nennen Sie die **End** -Methode, die mit der asynchronen **Begin** -Methode übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="394ee-125">To complete the asynchronous operation, call the **End** method that matches the asynchronous **Begin** method.</span></span> <span data-ttu-id="394ee-126">Die **End** -Methode nimmt immer einen **imfasynkresult** -Zeiger an.</span><span class="sxs-lookup"><span data-stu-id="394ee-126">The **End** method always takes an **IMFAsyncResult** pointer.</span></span> <span data-ttu-id="394ee-127">Übergeben Sie immer denselben Zeiger, den Sie in der **Aufruf** Methode erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="394ee-127">Always pass in the same pointer that you received in the **Invoke** method.</span></span> <span data-ttu-id="394ee-128">Der asynchrone Vorgang ist erst abgeschlossen, wenn Sie die **End** -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="394ee-128">The asynchronous operation is not complete until you call the **End** method.</span></span> <span data-ttu-id="394ee-129">Sie können die **End** **-Methode innerhalb der Aufruf** Methode aufrufen, oder Sie können Sie von einem anderen Thread aus aufrufen.</span><span class="sxs-lookup"><span data-stu-id="394ee-129">You may call the **End** method from inside the **Invoke** method, or you can call it from another thread.</span></span>

<span data-ttu-id="394ee-130">Um z. b. [**imfbytestream:: BeginRead für einen Bytestream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) abzuschließen, nennen Sie [**imfbytestream:: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span><span class="sxs-lookup"><span data-stu-id="394ee-130">For example, to complete the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) on a byte stream, call [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span></span>


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



<span data-ttu-id="394ee-131">Der Rückgabewert der **End** -Methode gibt den Status des asynchronen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="394ee-131">The return value of the **End** method indicates the status of the asynchronous operation.</span></span> <span data-ttu-id="394ee-132">In den meisten Fällen führt die Anwendung nach Abschluss des asynchronen Vorgangs einige Aufgaben aus, ob Sie erfolgreich abgeschlossen wurde oder nicht.</span><span class="sxs-lookup"><span data-stu-id="394ee-132">In most cases, your application will perform some work after the asynchronous operation completes, whether it completes successfully or not.</span></span> <span data-ttu-id="394ee-133">Sie haben mehrere Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="394ee-133">You have several options:</span></span>

-   <span data-ttu-id="394ee-134">Führen Sie die Arbeit innerhalb der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode aus.</span><span class="sxs-lookup"><span data-stu-id="394ee-134">Do the work inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="394ee-135">Diese Vorgehensweise ist akzeptabel, wenn Ihre Anwendung den aufrufenden Thread niemals blockiert oder auf etwas in der **Aufruf** Methode wartet.</span><span class="sxs-lookup"><span data-stu-id="394ee-135">This approach is acceptable as long as your application never blocks the calling thread or waits for anything inside the **Invoke** method.</span></span> <span data-ttu-id="394ee-136">Wenn Sie den aufrufenden Thread blockieren, kann die streamingpipeline blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="394ee-136">If you block the calling thread, you might block the streaming pipeline.</span></span> <span data-ttu-id="394ee-137">Beispielsweise können Sie einige Zustandsvariablen aktualisieren, aber keinen synchronen Lesevorgang ausführen oder auf ein Mutex-Objekt warten.</span><span class="sxs-lookup"><span data-stu-id="394ee-137">For example, you might update some state variables, but do not perform a synchronous read operation or wait on a mutex object.</span></span>
-   <span data-ttu-id="394ee-138">Legen Sie in der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode ein Ereignis fest, und geben Sie sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="394ee-138">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, set an event and return immediately.</span></span> <span data-ttu-id="394ee-139">Der Aufruf Thread der Anwendung wartet auf das Ereignis und führt die Arbeit aus, wenn das Ereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="394ee-139">The application's calling thread waits for the event and does the work when the event is signaled.</span></span>
-   <span data-ttu-id="394ee-140">Stellen Sie in der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode eine private Fenster Meldung in Ihrem Anwendungsfenster bereit, und geben Sie sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="394ee-140">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, post a private window message to your application window and return immediately.</span></span> <span data-ttu-id="394ee-141">Die Anwendung führt die Verarbeitung in der Nachrichten Schleife durch.</span><span class="sxs-lookup"><span data-stu-id="394ee-141">The application does the work on its message loop.</span></span> <span data-ttu-id="394ee-142">(Stellen Sie sicher, dass Sie die Nachricht senden, indem Sie **PostMessage** und nicht **SendMessage** aufrufen, da **SendMessage** den Rückruf Thread blockieren kann.)</span><span class="sxs-lookup"><span data-stu-id="394ee-142">(Make sure to post the message by calling **PostMessage**, not **SendMessage**, because **SendMessage** can block the callback thread.)</span></span>

<span data-ttu-id="394ee-143">Beachten Sie, dass [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem anderen Thread aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="394ee-143">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from another thread.</span></span> <span data-ttu-id="394ee-144">Ihre Anwendung ist dafür verantwortlich, sicherzustellen, dass jede im **Aufruf** ausgeführte Arbeit Thread sicher ist.</span><span class="sxs-lookup"><span data-stu-id="394ee-144">Your application is responsible for ensuring that any work performed inside **Invoke** is thread-safe.</span></span>

<span data-ttu-id="394ee-145">Der Thread, der " [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) " aufruft, trifft standardmäßig keine Annahmen über das Verhalten Ihres Rückruf Objekts.</span><span class="sxs-lookup"><span data-stu-id="394ee-145">By default, the thread that calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) makes no assumptions about the behavior of your callback object.</span></span> <span data-ttu-id="394ee-146">Optional können Sie die [**imfasynccallback:: GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) -Methode implementieren, um Informationen zu ihrer Rückruf Implementierung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="394ee-146">Optionally, you can implement the [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) method to return information about your callback implementation.</span></span> <span data-ttu-id="394ee-147">Andernfalls kann diese Methode **E \_ notimpl** zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="394ee-147">Otherwise, this method can return **E\_NOTIMPL**:</span></span>


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



<span data-ttu-id="394ee-148">Wenn Sie in der **Begin** -Methode ein Zustands Objekt angegeben haben, können Sie es aus der Rückruf Methode abrufen, indem Sie [**imfasyncresult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="394ee-148">If you specified a state object in the **Begin** method, you can retrieve it from inside your callback method by calling [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>

## <a name="related-topics"></a><span data-ttu-id="394ee-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="394ee-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="394ee-150">Asynchrone Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="394ee-150">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



