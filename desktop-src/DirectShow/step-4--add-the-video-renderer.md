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
# <a name="step-4-add-the-video-renderer"></a>Schritt 4: Hinzufügen des Videorenderers

Dieses Thema ist Schritt 4 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.

DirectShow bietet verschiedene Filter zum Rendering von Videos:

-   [**Erweiterter Videorenderer-Filter**](enhanced-video-renderer-filter.md) (EVR)
-   [Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)

Weitere Informationen zu den Unterschieden zwischen diesen Filtern finden Sie unter [auswählen des richtigen Videorenderers](choosing-the-right-renderer.md).

In diesem Tutorial wird jeder Videorendererfilter von einer Klasse umschließt, die einige der Unterschiede zwischen Ihnen abstrahiert. Diese Klassen werden von einer abstrakten Basisklasse mit dem Namen abgeleitet `CVideoRenderer` . Die Deklaration von `CVideoRenderer` wird in [Schritt 2: Declare cvideorenderer und abgeleitete Klassen](step-2--declare-cvideorenderer-and-derived-classes.md)gezeigt.

Mit der folgenden Methode wird versucht, jeden Videorenderer zu erstellen, beginnend mit dem EVR, dann mit VMR-9 und schließlich mit VMR-7.


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



### <a name="evr-filter"></a>EVR-Filter

Mit dem folgenden Code wird der EVR-Filter erstellt und dem Filter Diagramm hinzugefügt. Die Funktion, die `AddFilterByCLSID` in diesem Beispiel verwendet wird, finden [Sie im Thema Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md).


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



Die `InitializeEVR` Funktion initialisiert den EVR-Filter. Diese Funktion führt die folgenden Schritte aus.

1.  Fragt den Filter für die [**IMF GetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle ab.
2.  Ruft [**imfgetservice:: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) auf, um einen Zeiger auf die [**imfvideodisplaycontrol**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle zu erhalten.
3.  Ruft [**imfvideodisplaycontrol:: setvideowindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) auf, um das Videofenster festzulegen.
4.  Ruft [**imfvideodisplaycontrol:: setaspectratiomode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) auf, um den EVR so zu konfigurieren, dass das Seitenverhältnis des Videos beibehalten wird.

Der folgende Code zeigt die- `InitializeEVR` Funktion.


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



Nachdem das Diagramm erstellt wurde, ruft die auf `DShowPlayer::RenderStreams` `CVideoRenderer::FinalizeGraph` . Diese Methode führt jede abschließende Initialisierung oder Bereinigung durch. Der folgende Code zeigt die `CEVR` Implementierung dieser Methode.


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



Wenn der EVR nicht mit einem anderen Filter verbunden ist, entfernt diese Methode den EVR aus dem Diagramm. Dies kann vorkommen, wenn die Mediendatei keinen Videostream enthält.

### <a name="vmr-9-filter"></a>VMR-9-Filter

Mit dem folgenden Code wird der VMR-9-Filter erstellt und dem Filter Diagramm hinzugefügt.


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



Die `InitWindowlessVMR9` -Funktion initialisiert VMR-9 für den fensterlosen Modus. (Weitere Informationen über den fensterlosen Modus finden Sie unter [VMR-Modus](vmr-windowless-mode.md)für Windows-los.) Diese Funktion führt die folgenden Schritte aus.

1.  Fragt den VMR-9-Filter für die [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) -Schnittstelle ab.
2.  Ruft die [**IVMRFilterConfig9:: setrenderingmode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) -Methode auf, um den fensterlosen Modus festzulegen.
3.  Fragt den VMR-9-Filter für die [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) -Schnittstelle ab.
4.  Ruft die [**IVMRWindowlessControl9:: setvideoclippingwindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) -Methode auf, um das Videofenster festzulegen.
5.  Ruft die [**IVMRWindowlessControl9:: setaspectratiomode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) -Methode auf, um das Videoseiten Verhältnis beizubehalten.

Der folgende Code zeigt die- `InitWindowlessVMR9` Funktion.


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



Die `CVMR9::FinalizeGraph` -Methode überprüft, ob der VMR-9-Filter verbunden ist, und entfernt andernfalls den Filter aus dem Filter Diagramm.


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



### <a name="vmr-7-filter"></a>VMR-7-Filter

Die Schritte für den VMR-7-Filter sind fast identisch mit denen für VMR-9, mit dem Unterschied, dass stattdessen die VMR-7-Schnittstellen verwendet werden. Mit dem folgenden Code wird der VMR-7-Filter erstellt und dem Filter Diagramm hinzugefügt.


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



Die `InitWindowlessVMR` -Funktion initialisiert VMR-7 für den fensterlosen Modus. Diese Funktion führt die folgenden Schritte aus.

1.  Fragt den VMR-7-Filter für die [**ivmrfilterconfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) -Schnittstelle ab.
2.  Ruft die [**ivmrfilterconfig:: setrenderingmode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) -Methode auf, um den fensterlosen Modus festzulegen.
3.  Fragt den VMR-7-Filter für die [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle ab.
4.  Ruft die [**ivmrwindowlesscontrol:: setvideoclippingwindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) -Methode auf, um das Videofenster festzulegen.
5.  Ruft die [**ivmrwindowlesscontrol:: setaspectratiomode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) -Methode auf, um das Videoseiten Verhältnis beizubehalten.

Der folgende Code zeigt die- `InitWindowlessVMR` Funktion.


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



Die `CVMR7::FinalizeGraph` -Methode überprüft, ob der VMR-7-Filter verbunden ist, und entfernt andernfalls den Filter aus dem Filter Diagramm.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel zur DirectShow-Wiedergabe](directshow-playback-example.md)
</dt> <dt>

[Verwenden des DirectShow-EVR-Filters](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Verwenden des Video Mischungs Renderers](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
