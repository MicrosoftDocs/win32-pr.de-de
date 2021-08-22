---
description: Dieses Thema ist Schritt 3 des Tutorials Audio/Video Playback in DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Schritt 3: Erstellen des Filter-Graph'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4903e08b19e15721c8b62f130261bb4d05fcd94d544380b2e501f56d60704d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072504"
---
# <a name="step-3-build-the-filter-graph"></a>Schritt 3: Erstellen des Filter-Graph

Dieses Thema ist Schritt 3 des Tutorials [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md). Der vollständige Code wird im Thema [DirectShow Playback Example (DirectShow-Wiedergabebeispiel) gezeigt.](directshow-playback-example.md)

Der nächste Schritt besteht im Erstellen eines Filterdiagramms zur Wiedergabe der Mediendatei.

### <a name="opening-a-media-file"></a>Öffnen einer Mediendatei

Die `DShowPlayer::OpenFile` -Methode öffnet eine Mediendatei für die Wiedergabe. Diese Methode führt Folgendes aus:

1.  Erstellt ein neues (leeres) Filterdiagramm.
2.  Ruft [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) auf, um einen Quellfilter für die angegebene Datei hinzuzufügen.
3.  Rendert die Streams im Quellfilter.


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



### <a name="creating-the-filter-graph-manager"></a>Erstellen des Filter-Graph-Managers

Die `DShowPlayer::InitializeGraph` -Methode erstellt ein neues Filterdiagramm. Diese Methode führt Folgendes aus:

1.  Ruft [**CoCreateInstance auf,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um eine neue Instanz von Filter Graph [Manager zu erstellen.](filter-graph-manager.md)
2.  Fragt den Filter Graph Manager für die [**Schnittstellen IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) ab.
3.  Ruft [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) auf, um ereignisbenachrichtigungen zu einrichten. Weitere Informationen finden Sie unter [Ereignisbenachrichtigung in DirectShow.](event-notification-in-directshow.md)


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



### <a name="rendering-the-streams"></a>Rendern der Streams

Der nächste Schritt besteht im Verbinden des Quellfilters mit einem oder mehr Rendererfiltern.

Die `DShowPlayer::RenderStreams` -Methode führt die folgenden Schritte aus.

1.  Fragt den Filter-Graph-Manager für die [**IFilterGraph2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) ab.
2.  Fügt dem Filterdiagramm einen Videorendererfilter hinzu.
3.  Fügt dem [Filterdiagramm den DirectSound-Rendererfilter](directsound-renderer-filter.md) hinzu, um die Audiowiedergabe zu unterstützen. Weitere Informationen zum Hinzufügen von Filtern zum Filterdiagramm finden Sie unter [Hinzufügen eines Filters nach CLSID.](add-a-filter-by-clsid.md)
4.  Listet die Ausgabepins im Quellfilter auf. Weitere Informationen zum Aufzählen von Stecknadeln finden Sie unter [Aufzählen von Stecknadeln.](enumerating-pins.md)
5.  Ruft für jeden Pin die [**IFilterGraph2::RenderEx-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) auf. Diese Methode verbindet den Ausgabepin mit einem Rendererfilter und fügt bei Bedarf Zwischenfilter hinzu (z. B. Decoder).
6.  Ruft `CVideoRenderer::FinalizeGraph` auf, um die Initialisierung des Videorenderers zu beenden.
7.  Entfernt den [DirectSound-Rendererfilter,](directsound-renderer-filter.md) wenn dieser Filter nicht mit einem anderen Filter verbunden ist. Dies kann auftreten, wenn die Quelldatei keinen Audiostream enthält.


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



Hier ist der Code für die `RemoveUnconnectedRenderer` Funktion, die im vorherigen Beispiel verwendet wird.


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



### <a name="releasing-the-filter-graph"></a>Freigeben des Filterfilters Graph

Wenn die Anwendung beendet wird, muss sie das Filterdiagramm wie im folgenden Code gezeigt frei geben.


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



Weiter: [Schritt 4: Hinzufügen des Videorenderers](step-4--add-the-video-renderer.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow-Wiedergabebeispiel](directshow-playback-example.md)
</dt> <dt>

[Erstellen des Graph](building-the-filter-graph.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> </dl>

 

 
