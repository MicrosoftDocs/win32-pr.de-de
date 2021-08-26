---
description: Dieses Thema ist Schritt 4 des Tutorials Audio/Video Playback in DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Schritt 4: Hinzufügen des Videorenderers'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2d73dce5bba34f92c8df59cd9730ef1e25b57b9757039d9bda5c2e4432d734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051410"
---
# <a name="step-4-add-the-video-renderer"></a>Schritt 4: Hinzufügen des Videorenderers

Dieses Thema ist Schritt 4 des Tutorials [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md). Der vollständige Code wird im Thema [DirectShow Playback Example (DirectShow-Wiedergabebeispiel) gezeigt.](directshow-playback-example.md)

DirectShow bietet verschiedene Filter zum Rendern von Videos:

-   [**Erweiterter Videorendererfilter**](enhanced-video-renderer-filter.md) (EVR)
-   [Video mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Video mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)

Weitere Informationen zu den Unterschieden zwischen diesen Filtern finden Sie unter [Auswählen des richtigen Videorenderers.](choosing-the-right-renderer.md)

In diesem Tutorial wird jeder Videorendererfilter von einer Klasse umschlossen, die einige der Unterschiede zwischen ihnen abstrahiert. Diese Klassen werden alle von einer abstrakten Basisklasse mit dem Namen `CVideoRenderer` ableiten. Die Deklaration von wird in Schritt 2: Deklarieren `CVideoRenderer` [von CVideoRenderer und abgeleiteten Klassen gezeigt.](step-2--declare-cvideorenderer-and-derived-classes.md)

Die folgende Methode versucht, jeden Videorenderer nacheinander zu erstellen, beginnend mit der EVR, der VMR-9 und schließlich der VMR-7.


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

Der folgende Code erstellt den EVR-Filter und fügt ihn dem Filterdiagramm hinzu. Die in diesem Beispiel verwendete Funktion wird im Thema Add `AddFilterByCLSID` [a Filter by CLSID (Hinzufügen eines Filters nach CLSID) gezeigt.](add-a-filter-by-clsid.md)


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

1.  Fragt den Filter für die [**BENUTZEROBERFLÄCHEGetService-Schnittstelle**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) ab.
2.  [**RuftGEGETService::GetService auf,**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) um einen Zeiger auf die [**BENUTZEROBERFLÄCHEVideoDisplayControl-Schnittstelle**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) zu erhalten.
3.  Ruft [**DIE VIDEOdisplayControl::SetVideoWindow auf,**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) um das Videofenster zu setzen.
4.  Ruft DEN MODUS 2016332222222666 auf, um den EVR so zu konfigurieren, dass das Seitenverhältnis des Videos erhalten bleibt. [](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode)

Der folgende Code zeigt die `InitializeEVR` -Funktion.


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



Nachdem das Diagramm erstellt wurde, ruft `DShowPlayer::RenderStreams` `CVideoRenderer::FinalizeGraph` auf. Diese Methode führt alle abschließenden Initialisierungen oder Bereinigungen durch. Der folgende Code zeigt die `CEVR` Implementierung dieser Methode.


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



Wenn die EVR nicht mit einem anderen Filter verbunden ist, entfernt diese Methode die EVR aus dem Diagramm. Dies kann auftreten, wenn die Mediendatei keinen Videostream enthält.

### <a name="vmr-9-filter"></a>VMR-9-Filter

Der folgende Code erstellt den Filter VMR-9 und fügt ihn dem Filterdiagramm hinzu.


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



Die `InitWindowlessVMR9` Funktion initialisiert VMR-9 für den fensterlosen Modus. (Weitere Informationen zum fensterlosen Modus finden Sie unter [Fensterloser VMR-Modus.)](vmr-windowless-mode.md) Diese Funktion führt die folgenden Schritte aus.

1.  Fragt den VMR-9-Filter für die [**IVMRFilterConfig9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) ab.
2.  Ruft die [**IVMRFilterConfig9::SetRenderingMode-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) auf, um den fensterlosen Modus zu festlegen.
3.  Fragt den VMR-9-Filter für die [**IVMRWindowlessControl9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) ab.
4.  Ruft die [**IVMRWindowlessControl9::SetVideoClippingWindow-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) auf, um das Videofenster zu festlegen.
5.  Ruft die [**IVMRWindowlessControl9::SetAspectRatioMode-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) auf, um das Video-Seitenverhältnis zu erhalten.

Der folgende Code zeigt die `InitWindowlessVMR9` -Funktion.


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



Die `CVMR9::FinalizeGraph` -Methode überprüft, ob der VMR-9-Filter verbunden ist, und entfernt ihn aus dem Filterdiagramm, falls dies nicht der Dere ist.


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

Die Schritte für den VMR-7-Filter sind nahezu identisch mit denen für VMR-9, mit der Ausnahme, dass stattdessen die VMR-7-Schnittstellen verwendet werden. Der folgende Code erstellt den Filter VMR-7 und fügt ihn dem Filterdiagramm hinzu.


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



Die `InitWindowlessVMR` Funktion initialisiert VMR-7 für den fensterlosen Modus. Diese Funktion führt die folgenden Schritte aus.

1.  Fragt den VMR-7-Filter für die [**IVMRFilterConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) ab.
2.  Ruft die [**IVMRFilterConfig::SetRenderingMode-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) auf, um den fensterlosen Modus zu festlegen.
3.  Fragt den VMR-7-Filter für die [**IVMRWindowlessControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) ab.
4.  Ruft die [**IVMRWindowlessControl::SetVideoClippingWindow-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) auf, um das Videofenster zu festlegen.
5.  Ruft die [**IVMRWindowlessControl::SetAspectRatioMode-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) auf, um das Video-Seitenverhältnis zu erhalten.

Der folgende Code zeigt die `InitWindowlessVMR` -Funktion.


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



Die `CVMR7::FinalizeGraph` -Methode überprüft, ob der VMR-7-Filter verbunden ist, und entfernt ihn aus dem Filterdiagramm, falls dies nicht der Dere ist.


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

[DirectShow-Wiedergabebeispiel](directshow-playback-example.md)
</dt> <dt>

[Verwenden des DirectShow EVR-Filters](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Verwenden des Renderers für das Mischen von Videos](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
