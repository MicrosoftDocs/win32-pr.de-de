---
description: Medienereignis Generatoren
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Medienereignis Generatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354912"
---
# <a name="media-event-generators"></a><span data-ttu-id="8b4a9-103">Medienereignis Generatoren</span><span class="sxs-lookup"><span data-stu-id="8b4a9-103">Media Event Generators</span></span>

<span data-ttu-id="8b4a9-104">Media Foundation bietet eine konsistente Methode zum Senden von Ereignissen durch-Objekte.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-104">Media Foundation provides a consistent way for objects to send events.</span></span> <span data-ttu-id="8b4a9-105">Ein Objekt kann Ereignisse verwenden, um den Abschluss einer asynchronen Methode zu signalisieren oder um die Anwendung über eine Änderung des Objekt Zustands zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-105">An object can use events to signal the completion of an asynchronous method, or to notify the application about a change in the object's state.</span></span>

<span data-ttu-id="8b4a9-106">Wenn ein Objekt Ereignisse sendet, wird die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-106">If an object sends events, it exposes the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="8b4a9-107">Wenn das-Objekt ein neues Ereignis sendet, wird das-Ereignis in eine Warteschlange eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-107">Whenever the object sends a new event, the event is placed in a queue.</span></span> <span data-ttu-id="8b4a9-108">Die Anwendung kann das nächste Ereignis aus der Warteschlange anfordern, indem Sie eine der folgenden Methoden aufrufen:</span><span class="sxs-lookup"><span data-stu-id="8b4a9-108">The application can request the next event from the queue by calling one of the following methods:</span></span>

-   [<span data-ttu-id="8b4a9-109">**IMF mediaeventgenerator:: GetEvent**</span><span class="sxs-lookup"><span data-stu-id="8b4a9-109">**IMFMediaEventGenerator::GetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [<span data-ttu-id="8b4a9-110">**IMF mediaeventgenerator:: begingetevent**</span><span class="sxs-lookup"><span data-stu-id="8b4a9-110">**IMFMediaEventGenerator::BeginGetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

<span data-ttu-id="8b4a9-111">Die [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) -Methode ist synchron.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-111">The [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) method is synchronous.</span></span> <span data-ttu-id="8b4a9-112">Wenn ein Ereignis bereits in der Warteschlange vorhanden ist, wird die Methode sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-112">If an event is already in the queue, the method returns immediately.</span></span> <span data-ttu-id="8b4a9-113">Wenn in der Warteschlange kein Ereignis vorhanden ist, schlägt die Methode entweder sofort fehl oder blockiert, bis das nächste Ereignis in die Warteschlange eingereiht wird, je nachdem, welches Flag Sie an **GetEvent** übergeben.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-113">If there is no event in the queue, the method either fails immediately, or blocks until the next event is queued, depending on which flag you pass into **GetEvent**.</span></span>

<span data-ttu-id="8b4a9-114">Die [**begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) -Methode ist asynchron, sodass Sie niemals blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-114">The [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method is asynchronous, so it never blocks.</span></span> <span data-ttu-id="8b4a9-115">Diese Methode nimmt einen Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle an, die von der Anwendung implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-115">This method takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which the application must implement.</span></span> <span data-ttu-id="8b4a9-116">Wenn der Rückruf aufgerufen wird, ruft die Anwendung [**imfmediaeventgenerator:: endgetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) auf, um das Ereignis aus der Warteschlange zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-116">When the callback is invoked, the application calls [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event from the queue.</span></span> <span data-ttu-id="8b4a9-117">Weitere Informationen zu **imfasynccallback** finden Sie unter [asynchrone Rückruf Methoden](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8b4a9-117">For more information about **IMFAsyncCallback**, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="8b4a9-118">Ereignisse werden durch die [**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-118">Events are represented by the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span> <span data-ttu-id="8b4a9-119">Diese Schnittstelle verfügt über die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="8b4a9-119">This interface has the following methods:</span></span>

-   <span data-ttu-id="8b4a9-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Ruft den Ereignistyp ab.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Retrieves the event type.</span></span> <span data-ttu-id="8b4a9-121">Der Ereignistyp gibt an, was geschehen ist, um das Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-121">The event type indicates what happened to trigger the event.</span></span>

-   <span data-ttu-id="8b4a9-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Ruft einen **HRESULT** -Wert ab, der angibt, ob der Vorgang, der das Ereignis ausgelöst hat, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Retrieves an **HRESULT** value, indicating whether the operation that triggered the event was successful.</span></span> <span data-ttu-id="8b4a9-123">Wenn ein Vorgang asynchron fehlschlägt, gibt **GetStatus** einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-123">If an operation fails asynchronously, **GetStatus** returns a failure code.</span></span>

-   <span data-ttu-id="8b4a9-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Ruft eine **PROPVARIANT** ab, die Ereignisdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Retrieves a **PROPVARIANT** that contains event data.</span></span> <span data-ttu-id="8b4a9-125">Die Ereignisdaten hängen vom Ereignistyp ab.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-125">The event data depends on the event type.</span></span> <span data-ttu-id="8b4a9-126">Für einige Ereignisse sind keine Daten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-126">Some events do not have any data.</span></span>

-   <span data-ttu-id="8b4a9-127">[**Getextendedtype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Ruft eine **GUID** ab.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Retrieves a **GUID**.</span></span> <span data-ttu-id="8b4a9-128">Diese Methode gilt für das [meextendedtype-Ereignis](meextendedtype.md)und bietet eine Möglichkeit, benutzerdefinierte Ereignisse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-128">This method applies to the [MEExtendedType Event](meextendedtype.md), and provides a way to define custom events.</span></span>

<span data-ttu-id="8b4a9-129">Außerdem erbt die [**imbomediaevent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Schnittstelle die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-129">The [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface also inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="8b4a9-130">Einige Ereignisse enthalten zusätzliche Informationen als Attribute.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-130">Some events carry additional information as attributes.</span></span>

<span data-ttu-id="8b4a9-131">Eine Liste der Ereignis Typen und der zugehörigen Daten und Attribute finden Sie unter [Media Foundation-Ereignisse](media-foundation-events.md).</span><span class="sxs-lookup"><span data-stu-id="8b4a9-131">For a list of event types and their associated data and attributes, see [Media Foundation Events](media-foundation-events.md).</span></span>

## <a name="implementing-imfmediaeventgenerator"></a><span data-ttu-id="8b4a9-132">Implementieren von IMF mediaeventgenerator</span><span class="sxs-lookup"><span data-stu-id="8b4a9-132">Implementing IMFMediaEventGenerator</span></span>

<span data-ttu-id="8b4a9-133">Wenn Sie eine Plug-in-Komponente für Media Foundation schreiben, z. b. eine benutzerdefinierte Medienquelle oder eine Medien Senke, müssen Sie möglicherweise [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)implementieren.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-133">If you are writing a plug-in component for Media Foundation, such as a custom media source or media sink, you might need to implement [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span></span> <span data-ttu-id="8b4a9-134">Um dies zu vereinfachen, stellt Media Foundation ein Hilfsobjekt bereit, das eine Ereignis Warteschlange implementiert.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-134">To make this easier, Media Foundation provides a helper object that implements an event queue.</span></span> <span data-ttu-id="8b4a9-135">Erstellen Sie die Ereignis Warteschlange, indem Sie die [**mfcreateeventqueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-135">Create the event queue by calling the [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) function.</span></span> <span data-ttu-id="8b4a9-136">Die Ereignis Warteschlange macht die [**IMF mediaeventqueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-136">The event queue exposes the [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) interface.</span></span> <span data-ttu-id="8b4a9-137">In der Implementierung der **imfmediaeventgenerator** -Methoden des-Objekts können Sie die entsprechende-Methode für die Ereignis Warteschlange aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-137">In your object's implementation of the **IMFMediaEventGenerator** methods, call the corresponding method on the event queue.</span></span>

<span data-ttu-id="8b4a9-138">Das Ereignis Warteschlangen Objekt ist Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-138">The event queue object is thread safe.</span></span> <span data-ttu-id="8b4a9-139">Behalten Sie beim Aufrufen von [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) und [**queueevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent)niemals dasselbe kritische Abschnitts Objekt bei, da **GetEvent** ggf. unbegrenzt auf [**queueevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)wartet.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-139">Never hold the same critical section object when calling [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) and [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), because **GetEvent** might block indefinitely waiting for [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span></span> <span data-ttu-id="8b4a9-140">Wenn Sie für beide Methoden denselben kritischen Abschnitt aufbewahren, wird ein Deadlock verursacht.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-140">If you hold the same critical section for both methods, it will cause a deadlock.</span></span>

<span data-ttu-id="8b4a9-141">Bevor Sie die Ereignis Warteschlange freigeben, wenden Sie [**imfmediaeventqueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) an, um die Ressourcen freizugeben, die das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-141">Before releasing the event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) to release the resources that the object holds.</span></span>

<span data-ttu-id="8b4a9-142">Wenn das Objekt ein Ereignis abrufen muss, rufen Sie eine der folgenden Methoden für die Ereignis Warteschlange auf:</span><span class="sxs-lookup"><span data-stu-id="8b4a9-142">When your object needs to raise an event, call one of the following methods on the event queue:</span></span>

-   [<span data-ttu-id="8b4a9-143">**IMF mediaeventqueue:: queueevent**</span><span class="sxs-lookup"><span data-stu-id="8b4a9-143">**IMFMediaEventQueue::QueueEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [<span data-ttu-id="8b4a9-144">**IMF mediaeventqueue:: queueeventparamvar**</span><span class="sxs-lookup"><span data-stu-id="8b4a9-144">**IMFMediaEventQueue::QueueEventParamVar**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [<span data-ttu-id="8b4a9-145">**IMF mediaeventqueue:: queueeventparamunk**</span><span class="sxs-lookup"><span data-stu-id="8b4a9-145">**IMFMediaEventQueue::QueueEventParamUnk**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

<span data-ttu-id="8b4a9-146">Diese Methoden platzieren ein neues Ereignis in der Warteschlange und signalisieren allen Aufrufern, die auf das nächste Ereignis warten.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-146">These methods put a new event on the queue and signal any caller that is waiting for the next event.</span></span>

<span data-ttu-id="8b4a9-147">Der folgende Code zeigt eine Klasse, die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) mithilfe dieses Hilfsobjekts implementiert.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-147">The following code shows a class that implements [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) using this helper object.</span></span> <span data-ttu-id="8b4a9-148">Diese Klasse definiert eine öffentliche **Shutdown** -Methode, die die Ereignis Warteschlange herunterfährt und den Ereignis Warteschlangen Zeiger freigibt.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-148">This class defines a public **Shutdown** method that shuts down the event queue and releases the event queue pointer.</span></span> <span data-ttu-id="8b4a9-149">Dieses Verhalten ist typisch für Medienquellen und Medien senken, die immer über eine **Shutdown** -Methode verfügen.</span><span class="sxs-lookup"><span data-stu-id="8b4a9-149">This behavior would be typical for media sources and media sinks, which always have a **Shutdown** method.</span></span>


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a><span data-ttu-id="8b4a9-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b4a9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b4a9-151">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="8b4a9-151">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



