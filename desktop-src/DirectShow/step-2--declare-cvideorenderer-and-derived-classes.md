---
description: Dieses Thema ist Schritt 2 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Schritt 2: Deklarieren von cvideorenderer und abgeleiteten Klassen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362837"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a><span data-ttu-id="b833e-103">Schritt 2: Deklarieren von cvideorenderer und abgeleiteten Klassen</span><span class="sxs-lookup"><span data-stu-id="b833e-103">Step 2: Declare CVideoRenderer and Derived Classes</span></span>

<span data-ttu-id="b833e-104">Dieses Thema ist Schritt 2 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b833e-104">This topic is step 2 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="b833e-105">Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b833e-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="b833e-106">DirectShow bietet verschiedene Filter zum Rendering von Videos:</span><span class="sxs-lookup"><span data-stu-id="b833e-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="b833e-107">[**Erweiterter Videorenderer-Filter**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="b833e-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="b833e-108">[Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="b833e-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="b833e-109">[Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="b833e-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="b833e-110">Weitere Informationen zu den Unterschieden zwischen diesen Filtern finden Sie unter [auswählen des richtigen Videorenderers](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="b833e-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="b833e-111">In diesem Tutorial wird die folgende abstrakte Klasse verwendet, um den Videorenderer-Filter zu umschließen.</span><span class="sxs-lookup"><span data-stu-id="b833e-111">In this tutorial, the following abstract class is used to wrap the video renderer filter.</span></span>


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



<span data-ttu-id="b833e-112">Hinweise:</span><span class="sxs-lookup"><span data-stu-id="b833e-112">Notes:</span></span>

-   <span data-ttu-id="b833e-113">Die- `HasVideo` Methode gibt **true** zurück, wenn der Videorenderer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b833e-113">The `HasVideo` method returns **TRUE** if the video renderer has been created.</span></span>
-   <span data-ttu-id="b833e-114">Die- `AddToGraph` Methode fügt dem Filter Diagramm den Videorenderer hinzu.</span><span class="sxs-lookup"><span data-stu-id="b833e-114">The `AddToGraph` method adds the video renderer to the filter graph.</span></span>
-   <span data-ttu-id="b833e-115">Die `FinalizeGraph` -Methode schließt den Schritt für die Diagramm Bildung ab.</span><span class="sxs-lookup"><span data-stu-id="b833e-115">The `FinalizeGraph` method completes the graph-building step.</span></span>
-   <span data-ttu-id="b833e-116">Die- `UpdateVideoWindow` Methode aktualisiert das Video Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="b833e-116">The `UpdateVideoWindow` method updates the video destination rectangle.</span></span>
-   <span data-ttu-id="b833e-117">Mit der- `Repaint` Methode wird der aktuelle Videoframe neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b833e-117">The `Repaint` method redraws the current video frame.</span></span>
-   <span data-ttu-id="b833e-118">Die `DisplayModeChanged` -Methode behandelt Änderungen im Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="b833e-118">The `DisplayModeChanged` method handles display-mode changes.</span></span>

<span data-ttu-id="b833e-119">Diese Methoden werden weiter unten in diesem Tutorial ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b833e-119">Each of these methods is described in detail later in this tutorial.</span></span>

<span data-ttu-id="b833e-120">Als nächstes deklarieren Sie eine abgeleitete Klasse, um jeden der drei Videorenderer zu umschließen: den EVR, den VMR-9 und den VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b833e-120">Next, declare a derived class to wrap each of the three video renderers: the EVR, the VMR-9, and the VMR-7.</span></span>

### <a name="cevr-class"></a><span data-ttu-id="b833e-121">Cevr-Klasse</span><span class="sxs-lookup"><span data-stu-id="b833e-121">CEVR Class</span></span>

<span data-ttu-id="b833e-122">Die- `CEVR` Klasse verwaltet den EVR.</span><span class="sxs-lookup"><span data-stu-id="b833e-122">The `CEVR` class manages the EVR.</span></span> <span data-ttu-id="b833e-123">Sie enthält einen Zeiger auf die Schnittstellen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) und [**imfvideodisplaycontrol**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) der EVR.</span><span class="sxs-lookup"><span data-stu-id="b833e-123">It contains a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) and [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interfaces of the EVR.</span></span>


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a><span data-ttu-id="b833e-124">CVMR9-Klasse</span><span class="sxs-lookup"><span data-stu-id="b833e-124">CVMR9 Class</span></span>

<span data-ttu-id="b833e-125">Die `CVMR9` -Klasse verwaltet VMR-9.</span><span class="sxs-lookup"><span data-stu-id="b833e-125">The `CVMR9` class manages the VMR-9.</span></span> <span data-ttu-id="b833e-126">Sie enthält einen Zeiger auf die [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b833e-126">It contains a pointer to the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a><span data-ttu-id="b833e-127">CVMR7-Klasse</span><span class="sxs-lookup"><span data-stu-id="b833e-127">CVMR7 Class</span></span>

<span data-ttu-id="b833e-128">Die `CVMR7` -Klasse verwaltet VMR-7.</span><span class="sxs-lookup"><span data-stu-id="b833e-128">The `CVMR7` class manages the VMR-7.</span></span> <span data-ttu-id="b833e-129">Sie enthält einen Zeiger auf die [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b833e-129">It contains a pointer to the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



<span data-ttu-id="b833e-130">Weiter: [Schritt 3: Erstellen des Filter Diagramms](step-3--build-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="b833e-130">Next: [Step 3: Build the Filter Graph](step-3--build-the-filter-graph.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b833e-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b833e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b833e-132">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b833e-132">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b833e-133">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="b833e-133">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="b833e-134">Videorendering</span><span class="sxs-lookup"><span data-stu-id="b833e-134">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
