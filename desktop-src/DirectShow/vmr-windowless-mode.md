---
description: Fensterloser VMR-Modus
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Fensterloser VMR-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344369"
---
# <a name="vmr-windowless-mode"></a><span data-ttu-id="4a791-103">Fensterloser VMR-Modus</span><span class="sxs-lookup"><span data-stu-id="4a791-103">VMR Windowless Mode</span></span>

<span data-ttu-id="4a791-104">Der fensterlose Modus ist die bevorzugte Methode für Anwendungen zum renderingvideo in einem Anwendungsfenster.</span><span class="sxs-lookup"><span data-stu-id="4a791-104">Windowless mode is the preferred way for applications to render video inside an application window.</span></span> <span data-ttu-id="4a791-105">Im fensterlosen Modus lädt der Video Mischungs-Renderer seine Fenster-Manager-Komponente nicht und unterstützt daher nicht die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -oder [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4a791-105">In windowless mode, the Video Mixing Renderer does not load its Window Manager component, and therefore does not support the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) or [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interfaces.</span></span> <span data-ttu-id="4a791-106">Stattdessen stellt die Anwendung das Wiedergabe Fenster bereit und legt ein Ziel Rechteck im Client Bereich fest, damit das Video vom VMR gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a791-106">Instead, the application provides the playback window and sets a destination rectangle in the client area for the VMR to draw the video.</span></span> <span data-ttu-id="4a791-107">VMR verwendet ein DirectDraw-clipperobjekt, um sicherzustellen, dass das Video auf das Fenster der Anwendung zugeschnitten und nicht in anderen Fenstern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4a791-107">The VMR uses a DirectDraw clipper object to ensure that the video is clipped to the application's window and does not appear on any other windows.</span></span> <span data-ttu-id="4a791-108">Der VMR unterstützt das Fenster der Anwendung nicht oder installiert keine System-/prozesshooks.</span><span class="sxs-lookup"><span data-stu-id="4a791-108">The VMR does not subclass the application's window or install any system/process hooks.</span></span>

<span data-ttu-id="4a791-109">Im fensterlosen Modus lautet die Sequenz von Ereignissen während der Verbindung und der Übergang in den Ausführungs Status wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4a791-109">In windowless mode, the sequence of events during connection and transition to the run state is as follows:</span></span>

-   <span data-ttu-id="4a791-110">Der upstreamfilter schlägt einen Medientyp vor, den VMR entweder akzeptiert oder ablehnt.</span><span class="sxs-lookup"><span data-stu-id="4a791-110">The upstream filter proposes a media type, which the VMR either accepts or rejects.</span></span>
-   <span data-ttu-id="4a791-111">Wenn der Medientyp akzeptiert wird, ruft VMR den "zuordcator-Presenter" auf, um eine DirectDraw-Oberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a791-111">If the media type is accepted, the VMR calls the allocator-presenter to obtain a DirectDraw surface.</span></span> <span data-ttu-id="4a791-112">Wenn die Oberfläche erfolgreich erstellt wurde, sind die Pins Connect und VMR bereit für den Übergang in den Ausführungs Status.</span><span class="sxs-lookup"><span data-stu-id="4a791-112">If the surface is created successfully, the pins connect and the VMR is ready to transition into the run state.</span></span>
-   <span data-ttu-id="4a791-113">Wenn das Filter Diagramm ausgeführt wird, ruft der Decoder **GetBuffer** auf, um ein Medien Beispiel aus der Zuweisung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a791-113">When the filter graph runs, the decoder calls **GetBuffer** to get a media sample from the allocator.</span></span> <span data-ttu-id="4a791-114">VMR fragt den Zuweiser-Presenter ab, um sicherzustellen, dass die Pixel Tiefe, die Rechteck Größe und andere Parameter auf der DirectDraw-Oberfläche mit dem eingehenden Video kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="4a791-114">The VMR queries the allocator-presenter to ensure that the pixel depth, rectangle size, and other parameters on its DirectDraw surface are compatible with the incoming video.</span></span> <span data-ttu-id="4a791-115">Wenn Sie kompatibel sind, gibt der VMR die DirectDraw-Oberfläche an den Decoder zurück.</span><span class="sxs-lookup"><span data-stu-id="4a791-115">If they are compatible, the VMR returns the DirectDraw surface to the decoder.</span></span> <span data-ttu-id="4a791-116">Nachdem der Decoder in die-Oberfläche decodiert wurde, überprüft die Kern Synchronisierungs Einheit von VMR die Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="4a791-116">After the decoder has decoded into the surface, the VMR's Core Synchronization Unit validates the time stamps.</span></span> <span data-ttu-id="4a791-117">Diese Einheit blockiert den **Empfangs** Aufruf, bis die Präsentationszeit erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="4a791-117">This unit blocks the **Receive** call until the presentation time arrives.</span></span> <span data-ttu-id="4a791-118">An diesem Punkt ruft der VMR " **presentimage** " auf dem "zuordcator-Presenter" auf, der die Oberfläche auf der Grafikkarte darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a791-118">At that point, the VMR calls **PresentImage** on the allocator-presenter, which presents the surface to the graphics card.</span></span>

<span data-ttu-id="4a791-119">Die folgende Abbildung zeigt VMR im fensterlosen Modus mit mehreren Eingabedaten strömen.</span><span class="sxs-lookup"><span data-stu-id="4a791-119">The following illustration shows the VMR in windowless mode with multiple input streams.</span></span>

![VMR im fensterlosen Modus](images/vmr-windowless-mult-streams.png)

<span data-ttu-id="4a791-121">**Konfigurieren von VMR-7 für den fensterlosen Modus**</span><span class="sxs-lookup"><span data-stu-id="4a791-121">**Configuring the VMR-7 for Windowless Mode**</span></span>

<span data-ttu-id="4a791-122">Um VMR-7 für den fensterlosen Modus zu konfigurieren, führen Sie die folgenden Schritte aus, bevor Sie eine der VMR-Eingabe Pins verbinden:</span><span class="sxs-lookup"><span data-stu-id="4a791-122">To configure the VMR-7 for windowless mode, perform all of the following steps before connecting any of the VMR's input pins:</span></span>

1.  <span data-ttu-id="4a791-123">Erstellen Sie den Filter, und fügen Sie ihn dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="4a791-123">Create the filter and add it to the graph.</span></span>
2.  <span data-ttu-id="4a791-124">Wenden Sie die [**ivmrfilterconfig:: setrenderingmode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) -Methode mit dem Windows-Flag "vmrmode" an \_ .</span><span class="sxs-lookup"><span data-stu-id="4a791-124">Call the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method with the VMRMode\_Windowless flag.</span></span>
3.  <span data-ttu-id="4a791-125">Optional können Sie den VMR für mehrere Eingabedaten Ströme konfigurieren, indem Sie [**ivmrfilterconfig:: setnumofstreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4a791-125">Optionally, configure the VMR for multiple input streams by calling [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="4a791-126">VMR erstellt eine Eingabe-PIN für jeden Stream.</span><span class="sxs-lookup"><span data-stu-id="4a791-126">The VMR creates an input pin for each stream.</span></span> <span data-ttu-id="4a791-127">Verwenden Sie die [**ivmrmixercontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) -Schnittstelle, um die Z-Reihenfolge und andere Parameter für den Stream festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4a791-127">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface to set the Z-order and other parameters for the stream.</span></span> <span data-ttu-id="4a791-128">Weitere Informationen finden Sie unter [VMR mit mehreren Streams (Mischungs Modus)](vmr-with-multiple-streams--mixing-mode.md).</span><span class="sxs-lookup"><span data-stu-id="4a791-128">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span>

    <span data-ttu-id="4a791-129">Wenn Sie **setnumofstreams** nicht aufrufen, wird VMR-7 standardmäßig auf eine Eingabe-PIN festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a791-129">If you do not call **SetNumberOfStreams**, the VMR-7 defaults to one input pin.</span></span> <span data-ttu-id="4a791-130">Nachdem die Eingabe Pins verbunden sind, kann die Anzahl der Pins nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4a791-130">After the input pins are connected, the number of pins cannot be changed.</span></span>

4.  <span data-ttu-id="4a791-131">Aufrufen von [**ivmrwindowlesscontrol:: setvideoclippingwindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) zum Angeben des Fensters, in dem das gerenderte Video angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4a791-131">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) to specify the window in which the rendered video will appear.</span></span>

<span data-ttu-id="4a791-132">Nachdem Sie diese Schritte abgeschlossen haben, können Sie die Eingabe Pins des VMR-Filters verbinden.</span><span class="sxs-lookup"><span data-stu-id="4a791-132">Once these steps are completed, you can connect the VMR filter's input pins.</span></span> <span data-ttu-id="4a791-133">Es gibt verschiedene Möglichkeiten, das Diagramm zu erstellen, z. b. das direkte Verbinden von Pins, die Verwendung von intelligenten Verbindungsmethoden wie [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)oder die Verwendung der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode des Capture Graph-Generators.</span><span class="sxs-lookup"><span data-stu-id="4a791-133">There are various ways to build the graph, such as connecting pins directly, using Intelligent Connect methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), or using the Capture Graph Builder's [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="4a791-134">Weitere Informationen finden Sie unter [Allgemeine Graph-Building Techniken](general-graph-building-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="4a791-134">For more information, see [General Graph-Building Techniques](general-graph-building-techniques.md).</span></span>

<span data-ttu-id="4a791-135">Um die Position des Videos innerhalb des Anwendungsfensters festzulegen, können Sie die [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4a791-135">To set the position of the video within the application window, call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method.</span></span> <span data-ttu-id="4a791-136">Die [**ivmrwindowlesscontrol:: getnativevideosize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) -Methode gibt die systemeigene Videogröße zurück.</span><span class="sxs-lookup"><span data-stu-id="4a791-136">The [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method returns the native video size.</span></span> <span data-ttu-id="4a791-137">Während der Wiedergabe sollte die Anwendung den VMR der folgenden Windows-Meldungen Benachrichtigen:</span><span class="sxs-lookup"><span data-stu-id="4a791-137">During playback, the application should notify the VMR of the following Windows messages:</span></span>

-   <span data-ttu-id="4a791-138">WM \_ Paint: nennen Sie [**ivmrwindowlesscontrol:: repaintvideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) , um das Bild neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4a791-138">WM\_PAINT: Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) to repaint the image.</span></span>
-   <span data-ttu-id="4a791-139">WM \_ displaychange: der Befehl [**ivmrwindowlesscontrol::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="4a791-139">WM\_DISPLAYCHANGE: Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="4a791-140">VMR führt alle Aktionen aus, die erforderlich sind, um das Video mit der neuen Auflösung oder Farbtiefe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a791-140">The VMR takes any actions that are needed to display the video at the new resolution or color depth.</span></span>
-   <span data-ttu-id="4a791-141">WM \_ size: berechnet die Position des Videos neu und ruft [**setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) bei Bedarf erneut auf.</span><span class="sxs-lookup"><span data-stu-id="4a791-141">WM\_SIZE: Recalculate the position of the video and call [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) again if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="4a791-142">MFC-Anwendungen müssen einen leeren "WM \_ erasebkgnd"-Nachrichten Handler definieren, oder der Videoanzeige Bereich wird nicht ordnungsgemäß neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4a791-142">MFC applications must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="4a791-143">**Konfigurieren von VMR-9 für den fensterlosen Modus**</span><span class="sxs-lookup"><span data-stu-id="4a791-143">**Configuring the VMR-9 for Windowless Mode**</span></span>

<span data-ttu-id="4a791-144">Verwenden Sie zum Konfigurieren von VMR-9 für den fensterlosen Modus die für VMR-7 beschriebenen Schritte für den fensterlosen Modus, aber verwenden Sie die Schnittstellen [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) und [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="4a791-144">To configure the VMR-9 for windowless mode, use the steps described for the VMR-7 for Windowless mode, but use the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) and [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interfaces.</span></span> <span data-ttu-id="4a791-145">Der einzige bedeutende Unterschied besteht darin, dass VMR-9 standardmäßig vier Eingabe Pins erstellt, anstelle einer Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="4a791-145">The only significant difference is that the VMR-9 creates four input pins by default, rather than one input pin.</span></span> <span data-ttu-id="4a791-146">Daher müssen Sie **setnumofstreams** nur aufrufen, wenn Sie mehr als vier Videostreams mischen.</span><span class="sxs-lookup"><span data-stu-id="4a791-146">Therefore, you only need to call **SetNumberOfStreams** if you are mixing more than four video streams.</span></span>

<span data-ttu-id="4a791-147">**Beispiel Code**</span><span class="sxs-lookup"><span data-stu-id="4a791-147">**Example Code**</span></span>

<span data-ttu-id="4a791-148">Der folgende Code zeigt, wie ein VMR-7-Filter erstellt, dem DirectShow-Filter Diagramm hinzugefügt und anschließend der VMR in den fensterlosen Modus versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="4a791-148">The following code shows how to create a VMR-7 filter, add it to the DirectShow filter graph, and then put the VMR into windowless mode.</span></span> <span data-ttu-id="4a791-149">Verwenden Sie für VMR-9 CLSID \_ VideoMixingRenderer9 in **cokreateinstance** und die entsprechenden VMR-9-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4a791-149">For the VMR-9, use CLSID\_VideoMixingRenderer9 in **CoCreateInstance** and the corresponding VMR-9 interfaces.</span></span>


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4a791-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a791-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a791-151">Verwenden des fensterlosen Modus</span><span class="sxs-lookup"><span data-stu-id="4a791-151">Using Windowless Mode</span></span>](using-windowless-mode.md)
</dt> </dl>

 

 



