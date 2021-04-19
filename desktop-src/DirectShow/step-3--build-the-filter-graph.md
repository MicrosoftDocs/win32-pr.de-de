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
# <a name="step-3-build-the-filter-graph"></a>Schritt 3: Erstellen des Filter Diagramms

Dieses Thema ist Schritt 3 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.

Der nächste Schritt ist das Erstellen eines Filter Diagramms zum Wiedergeben der Mediendatei.

### <a name="opening-a-media-file"></a>Öffnen einer Mediendatei

Die- `DShowPlayer::OpenFile` Methode öffnet eine Mediendatei für die Wiedergabe. Diese Methode führt Folgendes aus:

1.  Erstellt ein neues (leeres) Filter Diagramm.
2.  Ruft [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) auf, um einen Quell Filter für die angegebene Datei hinzuzufügen.
3.  Rendert die Streams für den Quell Filter.


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



### <a name="creating-the-filter-graph-manager"></a>Erstellen des Filter Graph-Managers

Die- `DShowPlayer::InitializeGraph` Methode erstellt ein neues Filter Diagramm. Diese Methode führt Folgendes aus:

1.  Ruft [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine neue Instanz des [Filter Graph-Managers](filter-graph-manager.md)zu erstellen.
2.  Fragt den Filter Graph-Manager nach den Schnittstellen [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) ab.
3.  Ruft [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) zum Einrichten der Ereignis Benachrichtigung auf. Weitere Informationen finden Sie unter [Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md).


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

Der nächste Schritt besteht darin, den Quell Filter mit einem oder mehreren rendererfiltern zu verbinden.

Die- `DShowPlayer::RenderStreams` Methode führt die folgenden Schritte aus.

1.  Fragt den Filter Graph-Manager nach der [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) -Schnittstelle ab.
2.  Fügt dem Filter Diagramm einen Videorendererfilter hinzu.
3.  Fügt dem Filter Diagramm den [DirectSound-rendererfilter](directsound-renderer-filter.md) hinzu, um die Audiowiedergabe zu unterstützen. Weitere Informationen zum Hinzufügen von Filtern zum Filter Diagramm finden [Sie unter Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md).
4.  Listet die Ausgabe Pins für den Quell Filter auf. Weitere Informationen zum Auflisten von Pins finden Sie unter [Enumerieren von Pins](enumerating-pins.md).
5.  Für jede PIN wird die [**IFilterGraph2:: renderex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) -Methode aufgerufen. Diese Methode verbindet die Ausgabe-PIN mit einem rendererfilter und fügt bei Bedarf zwischen Filter hinzu (z. b. Decoders).
6.  Ruft `CVideoRenderer::FinalizeGraph` auf, um die Initialisierung des Videorenderers abzuschließen.
7.  Entfernt den [DirectSound](directsound-renderer-filter.md) -rendererfilter, wenn dieser Filter nicht mit einem anderen Filter verbunden ist. Dies kann vorkommen, wenn die Quelldatei keinen Audiodatenstrom enthält.


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



Im folgenden finden Sie den Code für die- `RemoveUnconnectedRenderer` Funktion, die im vorherigen Beispiel verwendet wird.


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



### <a name="releasing-the-filter-graph"></a>Freigeben des Filter Diagramms

Wenn die Anwendung beendet wird, muss Sie das Filter Diagramm freigeben, wie im folgenden Code gezeigt.


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

[Audiowiedergabe und Video Wiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Beispiel zur DirectShow-Wiedergabe](directshow-playback-example.md)
</dt> <dt>

[Aufbauen des Filter Diagramms](building-the-filter-graph.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> </dl>

 

 
