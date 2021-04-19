---
description: Dieses Thema ist Schritt 4 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Schritt 4: Hinzufügen des Videorenderers'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353230"
---
# <a name="step-4-add-the-video-renderer"></a><span data-ttu-id="b78f5-103">Schritt 4: Hinzufügen des Videorenderers</span><span class="sxs-lookup"><span data-stu-id="b78f5-103">Step 4: Add the Video Renderer</span></span>

<span data-ttu-id="b78f5-104">Dieses Thema ist Schritt 4 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b78f5-104">This topic is step 4 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="b78f5-105">Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b78f5-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="b78f5-106">DirectShow bietet verschiedene Filter zum Rendering von Videos:</span><span class="sxs-lookup"><span data-stu-id="b78f5-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="b78f5-107">[**Erweiterter Videorenderer-Filter**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="b78f5-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="b78f5-108">[Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="b78f5-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="b78f5-109">[Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="b78f5-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="b78f5-110">Weitere Informationen zu den Unterschieden zwischen diesen Filtern finden Sie unter [auswählen des richtigen Videorenderers](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="b78f5-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="b78f5-111">In diesem Tutorial wird jeder Videorendererfilter von einer Klasse umschließt, die einige der Unterschiede zwischen Ihnen abstrahiert.</span><span class="sxs-lookup"><span data-stu-id="b78f5-111">In this tutorial, each video renderer filter is wrapped by a class that abstracts some of the differences between them.</span></span> <span data-ttu-id="b78f5-112">Diese Klassen werden von einer abstrakten Basisklasse mit dem Namen abgeleitet `CVideoRenderer` .</span><span class="sxs-lookup"><span data-stu-id="b78f5-112">These classes all derive from an abstract base class named `CVideoRenderer`.</span></span> <span data-ttu-id="b78f5-113">Die Deklaration von `CVideoRenderer` wird in [Schritt 2: Declare cvideorenderer und abgeleitete Klassen](step-2--declare-cvideorenderer-and-derived-classes.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b78f5-113">The declaration of `CVideoRenderer` is shown in [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

<span data-ttu-id="b78f5-114">Mit der folgenden Methode wird versucht, jeden Videorenderer zu erstellen, beginnend mit dem EVR, dann mit VMR-9 und schließlich mit VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b78f5-114">The following method tries to create each video renderer in turn, starting with the EVR, then the VMR-9, and finally the VMR-7.</span></span>


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a><span data-ttu-id="b78f5-115">EVR-Filter</span><span class="sxs-lookup"><span data-stu-id="b78f5-115">EVR Filter</span></span>

<span data-ttu-id="b78f5-116">Mit dem folgenden Code wird der EVR-Filter erstellt und dem Filter Diagramm hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b78f5-116">The following code creates the EVR filter and adds it to the filter graph.</span></span> <span data-ttu-id="b78f5-117">Die Funktion, die `AddFilterByCLSID` in diesem Beispiel verwendet wird, finden [Sie im Thema Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="b78f5-117">The function `AddFilterByCLSID` used in this example is shown in the topic [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



<span data-ttu-id="b78f5-118">Die `InitializeEVR` Funktion initialisiert den EVR-Filter.</span><span class="sxs-lookup"><span data-stu-id="b78f5-118">The `InitializeEVR` function initializes the EVR filter.</span></span> <span data-ttu-id="b78f5-119">Diese Funktion führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b78f5-119">This function performs the following steps.</span></span>

1.  <span data-ttu-id="b78f5-120">Fragt den Filter für die [**IMF GetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="b78f5-120">Queries the filter for the [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="b78f5-121">Ruft [**imfgetservice:: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) auf, um einen Zeiger auf die [**imfvideodisplaycontrol**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b78f5-121">Calls [**IMFGetService::GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span>
3.  <span data-ttu-id="b78f5-122">Ruft [**imfvideodisplaycontrol:: setvideowindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) auf, um das Videofenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b78f5-122">Calls [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) to set the video window.</span></span>
4.  <span data-ttu-id="b78f5-123">Ruft [**imfvideodisplaycontrol:: setaspectratiomode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) auf, um den EVR so zu konfigurieren, dass das Seitenverhältnis des Videos beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="b78f5-123">Calls [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) to configure the EVR to preserve the video aspect ratio.</span></span>

<span data-ttu-id="b78f5-124">Der folgende Code zeigt die- `InitializeEVR` Funktion.</span><span class="sxs-lookup"><span data-stu-id="b78f5-124">The following code shows the `InitializeEVR` function.</span></span>


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



<span data-ttu-id="b78f5-125">Nachdem das Diagramm erstellt wurde, ruft die auf `DShowPlayer::RenderStreams` `CVideoRenderer::FinalizeGraph` .</span><span class="sxs-lookup"><span data-stu-id="b78f5-125">After the graph is built, the `DShowPlayer::RenderStreams` calls `CVideoRenderer::FinalizeGraph`.</span></span> <span data-ttu-id="b78f5-126">Diese Methode führt jede abschließende Initialisierung oder Bereinigung durch.</span><span class="sxs-lookup"><span data-stu-id="b78f5-126">This method performs any final initialization or cleanup.</span></span> <span data-ttu-id="b78f5-127">Der folgende Code zeigt die `CEVR` Implementierung dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="b78f5-127">The following code shows the `CEVR` implementation of this method.</span></span>


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



<span data-ttu-id="b78f5-128">Wenn der EVR nicht mit einem anderen Filter verbunden ist, entfernt diese Methode den EVR aus dem Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b78f5-128">If the EVR is not connected to any other filter, this method removes the EVR from the graph.</span></span> <span data-ttu-id="b78f5-129">Dies kann vorkommen, wenn die Mediendatei keinen Videostream enthält.</span><span class="sxs-lookup"><span data-stu-id="b78f5-129">This can occur if the media file does not contain a video stream.</span></span>

### <a name="vmr-9-filter"></a><span data-ttu-id="b78f5-130">VMR-9-Filter</span><span class="sxs-lookup"><span data-stu-id="b78f5-130">VMR-9 Filter</span></span>

<span data-ttu-id="b78f5-131">Mit dem folgenden Code wird der VMR-9-Filter erstellt und dem Filter Diagramm hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b78f5-131">The following code creates the VMR-9 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="b78f5-132">Die `InitWindowlessVMR9` -Funktion initialisiert VMR-9 für den fensterlosen Modus.</span><span class="sxs-lookup"><span data-stu-id="b78f5-132">The `InitWindowlessVMR9` function initializes the VMR-9 for windowless mode.</span></span> <span data-ttu-id="b78f5-133">(Weitere Informationen über den fensterlosen Modus finden Sie unter [VMR-Modus](vmr-windowless-mode.md)für Windows-los.) Diese Funktion führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b78f5-133">(For more information about windowless mode, see [VMR Windowless Mode](vmr-windowless-mode.md).) This function performs the following steps.</span></span>

1.  <span data-ttu-id="b78f5-134">Fragt den VMR-9-Filter für die [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="b78f5-134">Queries the VMR-9 filter for the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) interface.</span></span>
2.  <span data-ttu-id="b78f5-135">Ruft die [**IVMRFilterConfig9:: setrenderingmode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) -Methode auf, um den fensterlosen Modus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b78f5-135">Calls the [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="b78f5-136">Fragt den VMR-9-Filter für die [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="b78f5-136">Queries the VMR-9 filter for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
4.  <span data-ttu-id="b78f5-137">Ruft die [**IVMRWindowlessControl9:: setvideoclippingwindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) -Methode auf, um das Videofenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b78f5-137">Calls the [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="b78f5-138">Ruft die [**IVMRWindowlessControl9:: setaspectratiomode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) -Methode auf, um das Videoseiten Verhältnis beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="b78f5-138">Calls the [**IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="b78f5-139">Der folgende Code zeigt die- `InitWindowlessVMR9` Funktion.</span><span class="sxs-lookup"><span data-stu-id="b78f5-139">The following code shows the `InitWindowlessVMR9` function.</span></span>


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="b78f5-140">Die `CVMR9::FinalizeGraph` -Methode überprüft, ob der VMR-9-Filter verbunden ist, und entfernt andernfalls den Filter aus dem Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b78f5-140">The `CVMR9::FinalizeGraph` method checks if the VMR-9 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a><span data-ttu-id="b78f5-141">VMR-7-Filter</span><span class="sxs-lookup"><span data-stu-id="b78f5-141">VMR-7 Filter</span></span>

<span data-ttu-id="b78f5-142">Die Schritte für den VMR-7-Filter sind fast identisch mit denen für VMR-9, mit dem Unterschied, dass stattdessen die VMR-7-Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b78f5-142">The steps for the VMR-7 filter are nearly identical to those for the VMR-9, except the VMR-7 interfaces are used instead.</span></span> <span data-ttu-id="b78f5-143">Mit dem folgenden Code wird der VMR-7-Filter erstellt und dem Filter Diagramm hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b78f5-143">The following code creates the VMR-7 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="b78f5-144">Die `InitWindowlessVMR` -Funktion initialisiert VMR-7 für den fensterlosen Modus.</span><span class="sxs-lookup"><span data-stu-id="b78f5-144">The `InitWindowlessVMR` function initializes the VMR-7 for windowless mode.</span></span> <span data-ttu-id="b78f5-145">Diese Funktion führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b78f5-145">This function performs the following steps.</span></span>

1.  <span data-ttu-id="b78f5-146">Fragt den VMR-7-Filter für die [**ivmrfilterconfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="b78f5-146">Queries the VMR-7 filter for the [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) interface.</span></span>
2.  <span data-ttu-id="b78f5-147">Ruft die [**ivmrfilterconfig:: setrenderingmode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) -Methode auf, um den fensterlosen Modus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b78f5-147">Calls the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="b78f5-148">Fragt den VMR-7-Filter für die [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="b78f5-148">Queries the VMR-7 filter for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
4.  <span data-ttu-id="b78f5-149">Ruft die [**ivmrwindowlesscontrol:: setvideoclippingwindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) -Methode auf, um das Videofenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b78f5-149">Calls the [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="b78f5-150">Ruft die [**ivmrwindowlesscontrol:: setaspectratiomode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) -Methode auf, um das Videoseiten Verhältnis beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="b78f5-150">Calls the [**IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="b78f5-151">Der folgende Code zeigt die- `InitWindowlessVMR` Funktion.</span><span class="sxs-lookup"><span data-stu-id="b78f5-151">The following code shows the `InitWindowlessVMR` function.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="b78f5-152">Die `CVMR7::FinalizeGraph` -Methode überprüft, ob der VMR-7-Filter verbunden ist, und entfernt andernfalls den Filter aus dem Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b78f5-152">The `CVMR7::FinalizeGraph` method checks if the VMR-7 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b78f5-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b78f5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b78f5-154">Beispiel zur DirectShow-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="b78f5-154">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="b78f5-155">Verwenden des DirectShow-EVR-Filters</span><span class="sxs-lookup"><span data-stu-id="b78f5-155">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="b78f5-156">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="b78f5-156">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
