---
description: Dieses Thema ist Schritt 5 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Schritt 5: Hinzufügen von Video Funktionen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f5ccf1ae3ca24a705506bc41620ac53a13d7e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217482"
---
# <a name="step-5-add-video-functionality"></a>Schritt 5: Hinzufügen von Video Funktionen

Dieses Thema ist Schritt 5 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.

Um sicherzustellen, dass das Video ordnungsgemäß angezeigt wird, muss die Anwendung wie folgt auf die Nachrichten [**WM \_ Paint**](../gdi/wm-paint.md), [**WM \_ size**](../winmsg/wm-size.md)und [**WM \_ Display Change**](../gdi/wm-displaychange.md) Antworten.

### <a name="handle-wm_paint-messages"></a>Behandeln von WM-Zeichnungs \_ Meldungen

Wenn die Anwendung eine [**WM- \_**](../gdi/wm-paint.md) Zeichnungs Nachricht empfängt, muss der Videorenderer möglicherweise den letzten Videorahmen neu zeichnen. Für den " [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) "-Filter (EVR), nennen Sie [**imfvideodisplaycontrol:: repaintvideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



Für den [Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), nennen Sie [**IVMRWindowlessControl9:: repaintvideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



Nennen Sie für den [Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) [**ivmrwindowlesscontrol:: repaintvideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a>Behandeln von WM- \_ Größen Meldungen

Wenn sich die Größe des Videofensters ändert, Benachrichtigen Sie den Videorenderer, die Größe des Videos zu ändern. Nennen Sie für den EVR [**imfvideodisplaycontrol:: setvideoposition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



Für VMR-9 wird [**IVMRWindowlessControl9:: setvideoposition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition)aufgerufen.


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



Nennen Sie für VMR-7 [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a>Behandeln von WM \_ Display Change-Nachrichten

Wenn der Anzeigemodus geändert wird, müssen Sie den VMR-9-oder VMR-7-Filter benachrichtigen. Nennen Sie für VMR-9 [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



Nennen Sie für VMR-7 [**ivmrwindowlesscontrol::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



Der EVR muss nicht benachrichtigt werden, wenn der Anzeigemodus geändert wird.

Weiter: [Schritt 6: Behandeln von Diagramm Ereignissen](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiowiedergabe und Video Wiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Beispiel zur DirectShow-Wiedergabe](directshow-playback-example.md)
</dt> <dt>

[Verwenden des DirectShow-EVR-Filters](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Verwenden des Video Mischungs Renderers](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
