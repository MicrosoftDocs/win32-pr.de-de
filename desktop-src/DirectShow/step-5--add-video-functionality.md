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
# <a name="step-5-add-video-functionality"></a><span data-ttu-id="042d7-103">Schritt 5: Hinzufügen von Video Funktionen</span><span class="sxs-lookup"><span data-stu-id="042d7-103">Step 5: Add Video Functionality</span></span>

<span data-ttu-id="042d7-104">Dieses Thema ist Schritt 5 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="042d7-104">This topic is step 5 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="042d7-105">Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="042d7-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="042d7-106">Um sicherzustellen, dass das Video ordnungsgemäß angezeigt wird, muss die Anwendung wie folgt auf die Nachrichten [**WM \_ Paint**](../gdi/wm-paint.md), [**WM \_ size**](../winmsg/wm-size.md)und [**WM \_ Display Change**](../gdi/wm-displaychange.md) Antworten.</span><span class="sxs-lookup"><span data-stu-id="042d7-106">To ensure that video displays correctly, the application must respond to [**WM\_PAINT**](../gdi/wm-paint.md), [**WM\_SIZE**](../winmsg/wm-size.md), and [**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md) messages as follows.</span></span>

### <a name="handle-wm_paint-messages"></a><span data-ttu-id="042d7-107">Behandeln von WM-Zeichnungs \_ Meldungen</span><span class="sxs-lookup"><span data-stu-id="042d7-107">Handle WM\_PAINT Messages</span></span>

<span data-ttu-id="042d7-108">Wenn die Anwendung eine [**WM- \_**](../gdi/wm-paint.md) Zeichnungs Nachricht empfängt, muss der Videorenderer möglicherweise den letzten Videorahmen neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="042d7-108">When the application receives a [**WM\_PAINT**](../gdi/wm-paint.md) message, the video renderer might need to redraw the last video frame.</span></span> <span data-ttu-id="042d7-109">Für den " [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) "-Filter (EVR), nennen Sie [**imfvideodisplaycontrol:: repaintvideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="042d7-109">For the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter, call [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>


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



<span data-ttu-id="042d7-110">Für den [Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), nennen Sie [**IVMRWindowlessControl9:: repaintvideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="042d7-110">For the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span>


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



<span data-ttu-id="042d7-111">Nennen Sie für den [Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) [**ivmrwindowlesscontrol:: repaintvideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="042d7-111">For the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7), call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span>


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



### <a name="handle-wm_size-messages"></a><span data-ttu-id="042d7-112">Behandeln von WM- \_ Größen Meldungen</span><span class="sxs-lookup"><span data-stu-id="042d7-112">Handle WM\_SIZE Messages</span></span>

<span data-ttu-id="042d7-113">Wenn sich die Größe des Videofensters ändert, Benachrichtigen Sie den Videorenderer, die Größe des Videos zu ändern.</span><span class="sxs-lookup"><span data-stu-id="042d7-113">If the size of the video window changes, notify the video renderer to resize the video.</span></span> <span data-ttu-id="042d7-114">Nennen Sie für den EVR [**imfvideodisplaycontrol:: setvideoposition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="042d7-114">For the EVR, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>


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



<span data-ttu-id="042d7-115">Für VMR-9 wird [**IVMRWindowlessControl9:: setvideoposition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="042d7-115">For the VMR-9, call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span></span>


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



<span data-ttu-id="042d7-116">Nennen Sie für VMR-7 [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="042d7-116">For the VMR-7, call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span></span>


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



### <a name="handle-wm_displaychange-messages"></a><span data-ttu-id="042d7-117">Behandeln von WM \_ Display Change-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="042d7-117">Handle WM\_DISPLAYCHANGE Messages</span></span>

<span data-ttu-id="042d7-118">Wenn der Anzeigemodus geändert wird, müssen Sie den VMR-9-oder VMR-7-Filter benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="042d7-118">If the display mode changes, you must notify the VMR-9 or VMR-7 filter.</span></span> <span data-ttu-id="042d7-119">Nennen Sie für VMR-9 [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="042d7-119">For the VMR-9, call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span>


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



<span data-ttu-id="042d7-120">Nennen Sie für VMR-7 [**ivmrwindowlesscontrol::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="042d7-120">For the VMR-7, call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span>


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



<span data-ttu-id="042d7-121">Der EVR muss nicht benachrichtigt werden, wenn der Anzeigemodus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="042d7-121">The EVR does not need to be notified when the display mode changes.</span></span>

<span data-ttu-id="042d7-122">Weiter: [Schritt 6: Behandeln von Diagramm Ereignissen](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="042d7-122">Next: [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="042d7-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="042d7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="042d7-124">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="042d7-124">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="042d7-125">Beispiel zur DirectShow-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="042d7-125">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="042d7-126">Verwenden des DirectShow-EVR-Filters</span><span class="sxs-lookup"><span data-stu-id="042d7-126">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="042d7-127">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="042d7-127">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
