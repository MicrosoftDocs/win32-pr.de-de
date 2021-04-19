---
description: Dieses Thema ist Schritt 3 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Schritt 3: Erstellen des Filter Diagramms'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a770ad823a2578fab88a09cc44a3c7f2be4a4ca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362870"
---
# <a name="step-3-build-the-filter-graph"></a><span data-ttu-id="b7e7c-103">Schritt 3: Erstellen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="b7e7c-103">Step 3: Build the Filter Graph</span></span>

<span data-ttu-id="b7e7c-104">Dieses Thema ist Schritt 3 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b7e7c-104">This topic is step 3 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="b7e7c-105">Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="b7e7c-106">Der nächste Schritt ist das Erstellen eines Filter Diagramms zum Wiedergeben der Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-106">The next step is to build a filter graph to play the media file.</span></span>

### <a name="opening-a-media-file"></a><span data-ttu-id="b7e7c-107">Öffnen einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="b7e7c-107">Opening a Media File</span></span>

<span data-ttu-id="b7e7c-108">Die- `DShowPlayer::OpenFile` Methode öffnet eine Mediendatei für die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-108">The `DShowPlayer::OpenFile` method opens a media file for playback.</span></span> <span data-ttu-id="b7e7c-109">Diese Methode führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="b7e7c-109">This method does the following:</span></span>

1.  <span data-ttu-id="b7e7c-110">Erstellt ein neues (leeres) Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-110">Creates a new (empty) filter graph.</span></span>
2.  <span data-ttu-id="b7e7c-111">Ruft [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) auf, um einen Quell Filter für die angegebene Datei hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-111">Calls [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the specified file.</span></span>
3.  <span data-ttu-id="b7e7c-112">Rendert die Streams für den Quell Filter.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-112">Renders the streams on the source filter.</span></span>


```C++
HRESULT DShowPlayer::OpenFile(PCWSTR pszFileName)
{
    IBaseFilter *pSource = NULL;

    // Create a new filter graph. (This also closes the old one, if any.)
    HRESULT hr = InitializeGraph();
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the source filter to the graph.
    hr = m_pGraph->AddSourceFilter(pszFileName, NULL, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Try to render the streams.
    hr = RenderStreams(pSource);

done:
    if (FAILED(hr))
    {
        TearDownGraph();
    }
    SafeRelease(&pSource);
    return hr;
}
```



### <a name="creating-the-filter-graph-manager"></a><span data-ttu-id="b7e7c-113">Erstellen des Filter Graph-Managers</span><span class="sxs-lookup"><span data-stu-id="b7e7c-113">Creating the Filter Graph Manager</span></span>

<span data-ttu-id="b7e7c-114">Die- `DShowPlayer::InitializeGraph` Methode erstellt ein neues Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-114">The `DShowPlayer::InitializeGraph` method creates a new filter graph.</span></span> <span data-ttu-id="b7e7c-115">Diese Methode führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="b7e7c-115">This method does the following:</span></span>

1.  <span data-ttu-id="b7e7c-116">Ruft [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine neue Instanz des [Filter Graph-Managers](filter-graph-manager.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-116">Calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="b7e7c-117">Fragt den Filter Graph-Manager nach den Schnittstellen [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) ab.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-117">Queries the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>
3.  <span data-ttu-id="b7e7c-118">Ruft [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) zum Einrichten der Ereignis Benachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-118">Calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) to set up event notification.</span></span> <span data-ttu-id="b7e7c-119">Weitere Informationen finden Sie unter [Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b7e7c-119">For more information, see [Event Notification in DirectShow](event-notification-in-directshow.md).</span></span>


```C++
HRESULT DShowPlayer::InitializeGraph()
{
    TearDownGraph();

    // Create the Filter Graph Manager.
    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = STATE_STOPPED;

done:
    return hr;
}
```



### <a name="rendering-the-streams"></a><span data-ttu-id="b7e7c-120">Rendern der Streams</span><span class="sxs-lookup"><span data-stu-id="b7e7c-120">Rendering the Streams</span></span>

<span data-ttu-id="b7e7c-121">Der nächste Schritt besteht darin, den Quell Filter mit einem oder mehreren rendererfiltern zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-121">The next step is to connect the source filter to one or more renderer filters.</span></span>

<span data-ttu-id="b7e7c-122">Die- `DShowPlayer::RenderStreams` Methode führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-122">The `DShowPlayer::RenderStreams` method performs the following steps.</span></span>

1.  <span data-ttu-id="b7e7c-123">Fragt den Filter Graph-Manager nach der [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-123">Queries the Filter Graph Manager for the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface.</span></span>
2.  <span data-ttu-id="b7e7c-124">Fügt dem Filter Diagramm einen Videorendererfilter hinzu.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-124">Adds a video renderer filter to the filter graph.</span></span>
3.  <span data-ttu-id="b7e7c-125">Fügt dem Filter Diagramm den [DirectSound-rendererfilter](directsound-renderer-filter.md) hinzu, um die Audiowiedergabe zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-125">Adds the [DirectSound Renderer Filter](directsound-renderer-filter.md) to the filter graph, to support audio playback.</span></span> <span data-ttu-id="b7e7c-126">Weitere Informationen zum Hinzufügen von Filtern zum Filter Diagramm finden [Sie unter Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="b7e7c-126">For more information about adding filters to the filter graph, see [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>
4.  <span data-ttu-id="b7e7c-127">Listet die Ausgabe Pins für den Quell Filter auf.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-127">Enumerates the output pins on the source filter.</span></span> <span data-ttu-id="b7e7c-128">Weitere Informationen zum Auflisten von Pins finden Sie unter [Enumerieren von Pins](enumerating-pins.md).</span><span class="sxs-lookup"><span data-stu-id="b7e7c-128">For more information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).</span></span>
5.  <span data-ttu-id="b7e7c-129">Für jede PIN wird die [**IFilterGraph2:: renderex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-129">For each pin, calls the [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) method.</span></span> <span data-ttu-id="b7e7c-130">Diese Methode verbindet die Ausgabe-PIN mit einem rendererfilter und fügt bei Bedarf zwischen Filter hinzu (z. b. Decoders).</span><span class="sxs-lookup"><span data-stu-id="b7e7c-130">This method connects the output pin to a renderer filter, adding intermediate filters if needed (such as decoders).</span></span>
6.  <span data-ttu-id="b7e7c-131">Ruft `CVideoRenderer::FinalizeGraph` auf, um die Initialisierung des Videorenderers abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-131">Calls `CVideoRenderer::FinalizeGraph` to finish initializing the video renderer.</span></span>
7.  <span data-ttu-id="b7e7c-132">Entfernt den [DirectSound](directsound-renderer-filter.md) -rendererfilter, wenn dieser Filter nicht mit einem anderen Filter verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-132">Removes the [DirectSound Renderer](directsound-renderer-filter.md) filter if that filter is not connected to another filter.</span></span> <span data-ttu-id="b7e7c-133">Dies kann vorkommen, wenn die Quelldatei keinen Audiodatenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-133">This can occur if the source file does not contain an audio stream.</span></span>


```C++
// Render the streams from a source filter. 

HRESULT DShowPlayer::RenderStreams(IBaseFilter *pSource)
{
    BOOL bRenderedAnyPin = FALSE;

    IFilterGraph2 *pGraph2 = NULL;
    IEnumPins *pEnum = NULL;
    IBaseFilter *pAudioRenderer = NULL;
    HRESULT hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&pGraph2));
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the video renderer to the graph
    hr = CreateVideoRenderer();
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the DSound Renderer to the graph.
    hr = AddFilterByCLSID(m_pGraph, CLSID_DSoundRender, 
        &pAudioRenderer, L"Audio Renderer");
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate the pins on the source filter.
    hr = pSource->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through all the pins
    IPin *pPin;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {           
        // Try to render this pin. 
        // It's OK if we fail some pins, if at least one pin renders.
        HRESULT hr2 = pGraph2->RenderEx(pPin, AM_RENDEREX_RENDERTOEXISTINGRENDERERS, NULL);

        pPin->Release();
        if (SUCCEEDED(hr2))
        {
            bRenderedAnyPin = TRUE;
        }
    }

    hr = m_pVideo->FinalizeGraph(m_pGraph);
    if (FAILED(hr))
    {
        goto done;
    }

    // Remove the audio renderer, if not used.
    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(m_pGraph, pAudioRenderer, &bRemoved);

done:
    SafeRelease(&pEnum);
    SafeRelease(&pAudioRenderer);
    SafeRelease(&pGraph2);

    // If we succeeded to this point, make sure we rendered at least one 
    // stream.
    if (SUCCEEDED(hr))
    {
        if (!bRenderedAnyPin)
        {
            hr = VFW_E_CANNOT_RENDER;
        }
    }
    return hr;
}
```



<span data-ttu-id="b7e7c-134">Im folgenden finden Sie den Code für die- `RemoveUnconnectedRenderer` Funktion, die im vorherigen Beispiel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-134">Here is the code for the `RemoveUnconnectedRenderer` function, which is used in the previous example.</span></span>


```C++
HRESULT RemoveUnconnectedRenderer(IGraphBuilder *pGraph, IBaseFilter *pRenderer, BOOL *pbRemoved)
{
    IPin *pPin = NULL;

    *pbRemoved = FALSE;

    // Look for a connected input pin on the renderer.

    HRESULT hr = FindConnectedPin(pRenderer, PINDIR_INPUT, &pPin);
    SafeRelease(&pPin);

    // If this function succeeds, the renderer is connected, so we don't remove it.
    // If it fails, it means the renderer is not connected to anything, so
    // we remove it.

    if (FAILED(hr))
    {
        hr = pGraph->RemoveFilter(pRenderer);
        *pbRemoved = TRUE;
    }

    return hr;
}
```



### <a name="releasing-the-filter-graph"></a><span data-ttu-id="b7e7c-135">Freigeben des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="b7e7c-135">Releasing the Filter Graph</span></span>

<span data-ttu-id="b7e7c-136">Wenn die Anwendung beendet wird, muss Sie das Filter Diagramm freigeben, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7e7c-136">When the application exits, it must release the filter graph, as shown in the following code.</span></span>


```C++
void DShowPlayer::TearDownGraph()
{
    // Stop sending event messages
    if (m_pEvent)
    {
        m_pEvent->SetNotifyWindow((OAHWND)NULL, NULL, NULL);
    }

    SafeRelease(&m_pGraph);
    SafeRelease(&m_pControl);
    SafeRelease(&m_pEvent);

    delete m_pVideo;
    m_pVideo = NULL;

    m_state = STATE_NO_GRAPH;
}
```



<span data-ttu-id="b7e7c-137">Weiter: [Schritt 4: Hinzufügen des Videorenderers](step-4--add-the-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="b7e7c-137">Next: [Step 4: Add the Video Renderer](step-4--add-the-video-renderer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7e7c-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7e7c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e7c-139">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7e7c-139">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b7e7c-140">Beispiel zur DirectShow-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="b7e7c-140">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="b7e7c-141">Aufbauen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="b7e7c-141">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="b7e7c-142">Allgemeine Graph-Building Techniken</span><span class="sxs-lookup"><span data-stu-id="b7e7c-142">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
