---
description: Dieses Thema ist Schritt 5 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Schritt 5: Behandeln von Medien Sitzungs Ereignissen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357157"
---
# <a name="step-5-handle-media-session-events"></a><span data-ttu-id="92cfb-103">Schritt 5: Behandeln von Medien Sitzungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="92cfb-103">Step 5: Handle Media Session Events</span></span>

<span data-ttu-id="92cfb-104">Dieses Thema ist Schritt 5 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="92cfb-104">This topic is step 5 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="92cfb-105">Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92cfb-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="92cfb-106">Hintergrundinformationen zu diesem Thema finden Sie unter [Medienereignis Generatoren](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="92cfb-106">For background on this topic, read [Media Event Generators](media-event-generators.md).</span></span> <span data-ttu-id="92cfb-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="92cfb-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="92cfb-108">Sitzungs Ereignisse werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="92cfb-108">Getting Session Events</span></span>](#getting-session-events)
-   [<span data-ttu-id="92cfb-109">Mesessiontopologystatus</span><span class="sxs-lookup"><span data-stu-id="92cfb-109">MESessionTopologyStatus</span></span>](#mesessiontopologystatus)
-   [<span data-ttu-id="92cfb-110">Meendof Presentation</span><span class="sxs-lookup"><span data-stu-id="92cfb-110">MEEndOfPresentation</span></span>](#meendofpresentation)
-   [<span data-ttu-id="92cfb-111">Menewpresentation</span><span class="sxs-lookup"><span data-stu-id="92cfb-111">MENewPresentation</span></span>](#menewpresentation)
-   [<span data-ttu-id="92cfb-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92cfb-112">Related topics</span></span>](#related-topics)

## <a name="getting-session-events"></a><span data-ttu-id="92cfb-113">Sitzungs Ereignisse werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="92cfb-113">Getting Session Events</span></span>

<span data-ttu-id="92cfb-114">Um Ereignisse aus der Medien Sitzung zu erhalten, ruft das cplayer-Objekt die [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) -Methode auf, wie in [Schritt 4: Erstellen der Medien Sitzung](step-4--create-the-media-session.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="92cfb-114">To get events from the Media Session, the CPlayer object calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method, as shown in [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span> <span data-ttu-id="92cfb-115">Diese Methode ist asynchron und bedeutet, dass Sie sofort an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="92cfb-115">This method is asynchronous, meaning it returns to the caller immediately.</span></span> <span data-ttu-id="92cfb-116">Wenn das nächste Sitzungs Ereignis auftritt, ruft die Medien Sitzung die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode des cplayer-Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="92cfb-116">When the next session event occurs, the Media Session calls the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the CPlayer object.</span></span>

<span data-ttu-id="92cfb-117">Beachten Sie, dass der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem Arbeits Thread, nicht vom Anwendungs Thread aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="92cfb-117">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) gets called from a worker thread, not from the application thread.</span></span> <span data-ttu-id="92cfb-118">Daher **muss die** Implementierung des Aufrufs multithreadsicher sein.</span><span class="sxs-lookup"><span data-stu-id="92cfb-118">Therefore, the implementation of **Invoke** must be multithread-safe.</span></span> <span data-ttu-id="92cfb-119">Ein Ansatz besteht darin, die Elementdaten mit einem kritischen Abschnitt zu schützen.</span><span class="sxs-lookup"><span data-stu-id="92cfb-119">One approach would be to protect the member data with a critical section.</span></span> <span data-ttu-id="92cfb-120">Die- `CPlayer` Klasse zeigt jedoch einen alternativen Ansatz:</span><span class="sxs-lookup"><span data-stu-id="92cfb-120">However, the `CPlayer` class shows an alternative approach:</span></span>

1.  <span data-ttu-id="92cfb-121">In der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode stellt das cplayer-Objekt eine **WM \_ App \_ Player- \_ Ereignis** Meldung an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="92cfb-121">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the CPlayer object posts a **WM\_APP\_PLAYER\_EVENT** message to the application.</span></span> <span data-ttu-id="92cfb-122">Der Message-Parameter ist ein [**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="92cfb-122">The message parameter is an [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
2.  <span data-ttu-id="92cfb-123">Die Anwendung empfängt die **WM \_ App \_ Player- \_ Ereignis** Meldung.</span><span class="sxs-lookup"><span data-stu-id="92cfb-123">The application receives the **WM\_APP\_PLAYER\_EVENT** message.</span></span>
3.  <span data-ttu-id="92cfb-124">Die Anwendung ruft die- `CPlayer::HandleEvent` Methode auf und übergibt den [**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="92cfb-124">The application calls the `CPlayer::HandleEvent` method, passing in the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
4.  <span data-ttu-id="92cfb-125">Die- `HandleEvent` Methode antwortet auf das-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="92cfb-125">The `HandleEvent` method responds to the event.</span></span>

<span data-ttu-id="92cfb-126">Der folgende Code zeigt die Methode zum [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :</span><span class="sxs-lookup"><span data-stu-id="92cfb-126">The following code shows the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method:</span></span>


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



<span data-ttu-id="92cfb-127">Die [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="92cfb-127">The [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method performs the following steps:</span></span>

1.  <span data-ttu-id="92cfb-128">Zum Abrufen des Ereignisses muss [**imfmediaeventgenerator:: endgetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92cfb-128">Call [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event.</span></span> <span data-ttu-id="92cfb-129">Diese Methode gibt einen Zeiger auf die [**imfmediaevent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="92cfb-129">This method returns a pointer to the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span>
2.  <span data-ttu-id="92cfb-130">Wenn Sie [**imfmediaevent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) aufrufen, um den Ereignis Code abzurufen.</span><span class="sxs-lookup"><span data-stu-id="92cfb-130">Call [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event code.</span></span>
3.  <span data-ttu-id="92cfb-131">Wenn der Ereignis Code [mesessionclosed](mesessionclosed.md)ist, wird SetEvent aufgerufen, um *das \_ m hcloseevent* -Ereignis festzulegen.</span><span class="sxs-lookup"><span data-stu-id="92cfb-131">If the event code is [MESessionClosed](mesessionclosed.md), call SetEvent to set the *m\_hCloseEvent* event.</span></span> <span data-ttu-id="92cfb-132">Der Grund für diesen Schritt wird in [Schritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md)und auch in den Code Kommentaren erläutert.</span><span class="sxs-lookup"><span data-stu-id="92cfb-132">The reason for this step is explained in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md), and also in the code comments.</span></span>
4.  <span data-ttu-id="92cfb-133">Für alle anderen Ereignis Codes müssen Sie [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) aufrufen, um das nächste Ereignis anzufordern.</span><span class="sxs-lookup"><span data-stu-id="92cfb-133">For all other event codes, call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) to request the next event.</span></span>
5.  <span data-ttu-id="92cfb-134">Hiermit wird eine **WM \_ App Player- \_ \_ Ereignis** Meldung im Fenster gepostet.</span><span class="sxs-lookup"><span data-stu-id="92cfb-134">Post a **WM\_APP\_PLAYER\_EVENT** message to the window.</span></span>

<span data-ttu-id="92cfb-135">Der folgende Code zeigt die Methode "Lenker Ereignis", die aufgerufen wird, wenn die Anwendung die Ereignismeldung " **WM \_ App \_ Player \_** " empfängt:</span><span class="sxs-lookup"><span data-stu-id="92cfb-135">The following code shows the HandleEvent method, which is called when the application receives the **WM\_APP\_PLAYER\_EVENT** message:</span></span>


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



<span data-ttu-id="92cfb-136">Diese Methode ruft [**imfmediaevent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) auf, um den Ereignistyp und [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) zu erhalten, um den Erfolg des Fehlercodes zu erhalten, der dem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92cfb-136">This method calls [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event type and [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the success of failure code associated with the event.</span></span> <span data-ttu-id="92cfb-137">Die nächste Aktion, die ausgeführt wird, hängt vom Ereignis Code ab.</span><span class="sxs-lookup"><span data-stu-id="92cfb-137">The next action taken depends on the event code.</span></span>

## <a name="mesessiontopologystatus"></a><span data-ttu-id="92cfb-138">Mesessiontopologystatus</span><span class="sxs-lookup"><span data-stu-id="92cfb-138">MESessionTopologyStatus</span></span>

<span data-ttu-id="92cfb-139">Das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) signalisiert eine Änderung des Status der Topologie.</span><span class="sxs-lookup"><span data-stu-id="92cfb-139">The [MESessionTopologyStatus](mesessiontopologystatus.md) event signals a change in the status of the topology.</span></span> <span data-ttu-id="92cfb-140">Das [**MF- \_ Ereignis \_ topologiestatusattribut \_**](mf-event-topology-status-attribute.md) des Ereignis Objekts enthält den Status.</span><span class="sxs-lookup"><span data-stu-id="92cfb-140">The [**MF\_EVENT\_TOPOLOGY\_STATUS**](mf-event-topology-status-attribute.md) attribute of the event object contains the status.</span></span> <span data-ttu-id="92cfb-141">In diesem Beispiel ist der einzige relevante Wert " **MF \_ topostatus \_ Ready**", was darauf hinweist, dass die Wiedergabe bereit ist.</span><span class="sxs-lookup"><span data-stu-id="92cfb-141">For this example, the only value of interest is **MF\_TOPOSTATUS\_READY**, which indicates that playback is ready to start.</span></span>


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



<span data-ttu-id="92cfb-142">Die- `CPlayer::StartPlayback` Methode wird in [Schritt 6: Wiedergabe von Steuer](step-6--control-playback.md)Elementen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92cfb-142">The `CPlayer::StartPlayback` method is shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

<span data-ttu-id="92cfb-143">In diesem Beispiel wird auch [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufgerufen, um die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle vom [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="92cfb-143">This example also calls [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface from the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="92cfb-144">Diese Schnittstelle ist erforderlich, um das Neuzeichnen und die Größe des Videofensters zu verarbeiten, das auch in [Schritt 6: Wiedergabe von Steuer](step-6--control-playback.md)Elementen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="92cfb-144">This interface is needed to handle repainting and resizing the video window, also shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

## <a name="meendofpresentation"></a><span data-ttu-id="92cfb-145">Meendof Presentation</span><span class="sxs-lookup"><span data-stu-id="92cfb-145">MEEndOfPresentation</span></span>

<span data-ttu-id="92cfb-146">Das [meendof Presentation](meendofpresentation.md) -Ereignis signalisiert, dass die Wiedergabe das Ende der Datei erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="92cfb-146">The [MEEndOfPresentation](meendofpresentation.md) event signals that playback has reached the end of the file.</span></span> <span data-ttu-id="92cfb-147">Die Medien Sitzung wechselt automatisch wieder in den Zustand "beendet".</span><span class="sxs-lookup"><span data-stu-id="92cfb-147">The Media Session automatically switches back to the stopped state.</span></span>


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a><span data-ttu-id="92cfb-148">Menewpresentation</span><span class="sxs-lookup"><span data-stu-id="92cfb-148">MENewPresentation</span></span>

<span data-ttu-id="92cfb-149">Das [menewpresentation](menewpresentation.md) -Ereignis signalisiert den Anfang einer neuen Präsentation.</span><span class="sxs-lookup"><span data-stu-id="92cfb-149">The [MENewPresentation](menewpresentation.md) event signals the start of a new presentation.</span></span> <span data-ttu-id="92cfb-150">Bei den Ereignisdaten handelt es sich um einen [**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Zeiger für die neue Präsentation.</span><span class="sxs-lookup"><span data-stu-id="92cfb-150">The event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer for the new presentation.</span></span>

<span data-ttu-id="92cfb-151">In vielen Fällen wird dieses Ereignis überhaupt nicht empfangen.</span><span class="sxs-lookup"><span data-stu-id="92cfb-151">In many cases, you will not receive this event at all.</span></span> <span data-ttu-id="92cfb-152">Verwenden Sie in diesem Fall den [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Zeiger zum Erstellen einer neuen Wiedergabe Topologie, wie in [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="92cfb-152">If you do, use the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer to create a new playback topology, as shown in [Step 3: Open a Media File](step-3--open-a-media-file.md).</span></span> <span data-ttu-id="92cfb-153">Stellen Sie dann die neue Topologie in die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="92cfb-153">Then queue the new topology on the Media Session.</span></span>


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



<span data-ttu-id="92cfb-154">Nächstes: [Schritt 6: Wiedergabe von Steuer](step-6--control-playback.md) Elementen</span><span class="sxs-lookup"><span data-stu-id="92cfb-154">Next: [Step 6: Control Playback](step-6--control-playback.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="92cfb-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92cfb-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92cfb-156">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="92cfb-156">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="92cfb-157">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92cfb-157">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



