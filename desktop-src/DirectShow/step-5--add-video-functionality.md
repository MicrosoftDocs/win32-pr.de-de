---
description: Dieses Thema ist Schritt 5 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Schritt 5: Hinzufügen von Videofunktionen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968c35916f90f226305eb987058d14cc7891d250961e2b8a41a1756ec3794b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951779"
---
# <a name="step-5-add-video-functionality"></a>Schritt 5: Hinzufügen von Videofunktionen

Dieses Thema ist Schritt 5 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der vollständige Code wird im Thema [DirectShow Playback Example (DirectShow-Wiedergabebeispiel)](directshow-playback-example.md)gezeigt.

Um sicherzustellen, dass das Video ordnungsgemäß angezeigt wird, muss die Anwendung wie folgt auf [**WM \_ PAINT-,**](../gdi/wm-paint.md) [**WM \_ SIZE-**](../winmsg/wm-size.md)und [**WM \_ DISPLAYCHANGE-Meldungen**](../gdi/wm-displaychange.md) reagieren.

### <a name="handle-wm_paint-messages"></a>Behandeln von WM \_ PAINT-Nachrichten

Wenn die Anwendung eine [**WM \_ PAINT-Nachricht**](../gdi/wm-paint.md) empfängt, muss der Videorenderer möglicherweise den letzten Videoframe neu zeichnen. Rufen Sie für den Filter [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) [**DEN AUFRUF VONVIDEODisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo)auf.


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



Rufen Sie für den [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo)auf.


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



Rufen Sie für den [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo)auf.


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



### <a name="handle-wm_size-messages"></a>Verarbeiten von WM \_ SIZE-Nachrichten

Wenn sich die Größe des Videofensters ändert, benachrichtigen Sie den Videorenderer, um die Größe des Videos zu ändern. Rufen Sie für die EVR [**DEN AUFRUF VONVIDEODisplayControl::SetVideoPosition auf.**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)


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



Rufen Sie für DIE VMR-9 [**IVMRWindowlessControl9::SetVideoPosition auf.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition)


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



Rufen Sie für VMR-7 [**IVMRWindowlessControl::SetVideoPosition auf.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition)


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



### <a name="handle-wm_displaychange-messages"></a>Behandeln von \_ WM-DISPLAYCHANGE-Meldungen

Wenn sich der Anzeigemodus ändert, müssen Sie den Filter VMR-9 oder VMR-7 benachrichtigen. Rufen Sie für VMR-9 [**IVMRWindowlessControl9::D isplayModeChanged auf.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged)


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



Rufen Sie für VMR-7 [**IVMRWindowlessControl::D isplayModeChanged auf.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)


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



Die EVR muss nicht benachrichtigt werden, wenn sich der Anzeigemodus ändert.

Weiter: [Schritt 6: Behandeln Graph Ereignisse](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Beispiel für DirectShow-Wiedergabe](directshow-playback-example.md)
</dt> <dt>

[Verwenden des DirectShow EVR-Filters](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Verwenden des Videomischungsrenderers](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
