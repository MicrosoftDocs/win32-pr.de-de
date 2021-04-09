---
description: Verwenden des fensterlosen Modus
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Verwenden des fensterlosen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866448"
---
# <a name="using-windowless-mode"></a><span data-ttu-id="0bef5-103">Verwenden des fensterlosen Modus</span><span class="sxs-lookup"><span data-stu-id="0bef5-103">Using Windowless Mode</span></span>

<span data-ttu-id="0bef5-104">Sowohl der [Video Mischungs Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) als auch der [Video Mischungs Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) unterstützen den *fensterlosen Modus*, der eine bedeutende Verbesserung gegenüber der [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="0bef5-104">Both the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) support *windowless mode*, which represents a major improvement over the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="0bef5-105">In diesem Thema werden die Unterschiede zwischen dem fensterlosen Modus und dem Fenstermodus sowie die Verwendung des fensterlosen Modus beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0bef5-105">This topic describes the differences between windowless mode and windowed mode, and how to use windowless mode.</span></span>

<span data-ttu-id="0bef5-106">Um Abwärtskompatibilität mit vorhandenen Anwendungen zu erhalten, wird für VMR standardmäßig der Fenster-Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="0bef5-106">To remain backward-compatible with existing applications, the VMR defaults to windowed mode.</span></span> <span data-ttu-id="0bef5-107">Im Fenstermodus erstellt der Renderer ein eigenes Fenster, um das Video anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0bef5-107">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="0bef5-108">In der Regel legt die Anwendung das Videofenster als untergeordnetes Element des Anwendungsfensters fest.</span><span class="sxs-lookup"><span data-stu-id="0bef5-108">Typically the application sets the video window to be a child of the application window.</span></span> <span data-ttu-id="0bef5-109">Das vorhanden sein eines separaten Videofensters verursacht jedoch einige Probleme:</span><span class="sxs-lookup"><span data-stu-id="0bef5-109">The existence of a separate video window causes some problems, however:</span></span>

-   <span data-ttu-id="0bef5-110">Am wichtigsten ist, dass es zu Deadlocks kommen kann, wenn zwischen Threads Fenster Meldungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bef5-110">Most importantly, there is a potential for deadlocks if window messages are sent between threads.</span></span>
-   <span data-ttu-id="0bef5-111">Der Filter Graph-Manager muss bestimmte Fenster Meldungen, z. b \_ . WM Paint, an den Videorenderer weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="0bef5-111">The Filter Graph Manager must forward certain window messages, such as WM\_PAINT, to the Video Renderer.</span></span> <span data-ttu-id="0bef5-112">Die Anwendung muss die Implementierung von [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) des Filter Diagramms (und nicht die des Videorenderers) verwenden, damit der Filter Graph-Manager den korrekten internen Zustand beibehält.</span><span class="sxs-lookup"><span data-stu-id="0bef5-112">The application must use the Filter Graph Manager's implementation of [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (and not the Video Renderer's), so that the Filter Graph Manager maintains the correct internal state.</span></span>
-   <span data-ttu-id="0bef5-113">Um Maus-oder Tastatur Ereignisse aus dem Videofenster zu empfangen, muss die Anwendung eine *Nachrichten Ableitung* festlegen, sodass das Videofenster diese Nachrichten an die Anwendung weiterleiten kann.</span><span class="sxs-lookup"><span data-stu-id="0bef5-113">To receive mouse or keyboard events from the video window, the application must set a *message drain*, causing the video window to forward these messages to the application.</span></span>
-   <span data-ttu-id="0bef5-114">Um clippingprobleme zu vermeiden, muss das Videofenster über die richtigen Fenster Stile verfügen.</span><span class="sxs-lookup"><span data-stu-id="0bef5-114">To prevent clipping problems, the video window must have the right window styles.</span></span>

<span data-ttu-id="0bef5-115">Der fensterlose Modus vermeidet diese Probleme, indem der VMR direkt im Client Bereich des Anwendungsfensters gezeichnet wird. dabei wird DirectDraw zum Ausschneiden des Video Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="0bef5-115">Windowless mode avoids these problems by having the VMR draw directly on the application window's client area, using DirectDraw to clip the video rectangle.</span></span> <span data-ttu-id="0bef5-116">Der fensterlose Modus verringert die Wahrscheinlichkeit von Deadlocks erheblich.</span><span class="sxs-lookup"><span data-stu-id="0bef5-116">Windowless mode significantly reduces the chance of deadlocks.</span></span> <span data-ttu-id="0bef5-117">Außerdem muss die Anwendung das Besitzer Fenster oder die Fenster Stile nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="0bef5-117">Also, the application does not have to set the owner window or the window styles.</span></span> <span data-ttu-id="0bef5-118">Wenn sich VMR im fensterlosen Modus befindet, wird die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle nicht einmal verfügbar gemacht, da Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0bef5-118">In fact, when the VMR is in windowless mode, it does not even expose the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, which is no longer needed.</span></span>

<span data-ttu-id="0bef5-119">Um den fensterlosen Modus zu verwenden, müssen Sie den VMR explizit konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0bef5-119">To use windowless mode, you must explicitly configure the VMR.</span></span> <span data-ttu-id="0bef5-120">Sie werden jedoch feststellen, dass flexibler und einfacher zu verwenden ist als der Fenstermodus.</span><span class="sxs-lookup"><span data-stu-id="0bef5-120">However, you will find that is more flexible and easier to use than windowed mode.</span></span>

<span data-ttu-id="0bef5-121">Der VMR-7-Filter und der VMR-9-Filter machen verschiedene Schnittstellen verfügbar, die Schritte sind jedoch gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="0bef5-121">The VMR-7 filter and the VMR-9 filter expose different interfaces, but the steps are equivalent for each.</span></span>

## <a name="configure-the-vmr-for-windowless-mode"></a><span data-ttu-id="0bef5-122">Konfigurieren des VMR für den fensterlosen Modus</span><span class="sxs-lookup"><span data-stu-id="0bef5-122">Configure the VMR for Windowless Mode</span></span>

<span data-ttu-id="0bef5-123">Um das VMR-Standardverhalten zu überschreiben, konfigurieren Sie VMR vor dem Aufbau des Filter Diagramms:</span><span class="sxs-lookup"><span data-stu-id="0bef5-123">To override the VMR's default behavior, configure the VMR before building the filter graph:</span></span>

<span data-ttu-id="0bef5-124">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="0bef5-124">**VMR-7**</span></span>

1.  <span data-ttu-id="0bef5-125">Erstellen Sie den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="0bef5-125">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="0bef5-126">Erstellen Sie VMR-7, und fügen Sie es dem Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="0bef5-126">Create the VMR-7 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="0bef5-127">Wenden Sie [**ivmrfilterconfig:: setrenderingmode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) für VMR-7 mit dem **\_ Windows-Flag "vmrmode** " an.</span><span class="sxs-lookup"><span data-stu-id="0bef5-127">Call [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) on the VMR-7 with the **VMRMode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="0bef5-128">Fragen Sie VMR-7 nach der [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="0bef5-128">Query the VMR-7 for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
5.  <span data-ttu-id="0bef5-129">Aufrufen von [**ivmrwindowlesscontrol:: setvideoclippingwindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) für VMR-7.</span><span class="sxs-lookup"><span data-stu-id="0bef5-129">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) on the VMR-7.</span></span> <span data-ttu-id="0bef5-130">Geben Sie ein Handle für das Fenster an, in dem das Video angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bef5-130">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="0bef5-131">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="0bef5-131">**VMR-9**</span></span>

1.  <span data-ttu-id="0bef5-132">Erstellen Sie den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="0bef5-132">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="0bef5-133">Erstellen Sie VMR-9, und fügen Sie es dem Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="0bef5-133">Create the VMR-9 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="0bef5-134">Wenden Sie [**IVMRFilterConfig9:: setrenderingmode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) auf VMR-9 mit dem **VMR9Mode \_ Windows less** -Flag an.</span><span class="sxs-lookup"><span data-stu-id="0bef5-134">Call [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) on the VMR-9 with the **VMR9Mode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="0bef5-135">Fragen Sie VMR-9 nach der [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="0bef5-135">Query the VMR-9 for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
5.  <span data-ttu-id="0bef5-136">Aufrufen von [**IVMRWindowlessControl9:: setvideoclippingwindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) für VMR-9.</span><span class="sxs-lookup"><span data-stu-id="0bef5-136">Call [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) on the VMR-9.</span></span> <span data-ttu-id="0bef5-137">Geben Sie ein Handle für das Fenster an, in dem das Video angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bef5-137">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="0bef5-138">Erstellen Sie jetzt den Rest des Filter Diagramms, indem Sie [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder andere Graph-Erstellungs Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0bef5-138">Now build the rest of the filter graph by calling [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or other graph-building methods.</span></span> <span data-ttu-id="0bef5-139">Der Filter Graph-Manager verwendet automatisch die Instanz von VMR, die Sie dem Diagramm hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="0bef5-139">The Filter Graph Manager automatically uses the instance of the VMR that you added to the graph.</span></span> <span data-ttu-id="0bef5-140">(Ausführliche Informationen dazu, warum dies geschieht, finden Sie unter [Intelligent Connect](intelligent-connect.md).)</span><span class="sxs-lookup"><span data-stu-id="0bef5-140">(For details on why this happens, see [Intelligent Connect](intelligent-connect.md).)</span></span>

<span data-ttu-id="0bef5-141">Der folgende Code zeigt eine Hilfsfunktion, die VMR-7 erstellt, Sie dem Diagramm hinzufügt und den fensterlosen Modus einrichtet.</span><span class="sxs-lookup"><span data-stu-id="0bef5-141">The following code shows a helper function that creates the VMR-7, adds it to the graph, and sets up windowless mode.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



<span data-ttu-id="0bef5-142">Diese Funktion geht davon aus, dass nur einen Videodaten Strom anzeigt und keine statische Bitmap über das Video vermischt.</span><span class="sxs-lookup"><span data-stu-id="0bef5-142">This function assumes that are displaying only one video stream and are not mixing a static bitmap over the video.</span></span> <span data-ttu-id="0bef5-143">Weitere Informationen finden Sie unter [Windows-VMR-Modus](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="0bef5-143">For details, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span> <span data-ttu-id="0bef5-144">Diese Funktion wird wie folgt aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="0bef5-144">You would call this function as follows:</span></span>


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a><span data-ttu-id="0bef5-145">Positionieren des Videos</span><span class="sxs-lookup"><span data-stu-id="0bef5-145">Position the Video</span></span>

<span data-ttu-id="0bef5-146">Nach dem Konfigurieren von VMR ist der nächste Schritt das Festlegen der Position des Videos.</span><span class="sxs-lookup"><span data-stu-id="0bef5-146">After configuring the VMR, the next step is to set the position of the video.</span></span> <span data-ttu-id="0bef5-147">Es gibt zwei zu berücksichtigende Rechtecke, das *Quell* Rechteck und das *Ziel* Rechteck.</span><span class="sxs-lookup"><span data-stu-id="0bef5-147">There are two rectangles to consider, the *source* rectangle and the *destination* rectangle.</span></span> <span data-ttu-id="0bef5-148">Das Quell Rechteck definiert, welcher Teil des Videos angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bef5-148">The source rectangle defines which portion of the video to display.</span></span> <span data-ttu-id="0bef5-149">Das Ziel Rechteck gibt den Bereich im Client Bereich des Fensters an, in dem das Video enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="0bef5-149">The destination rectangle specifies the region in the window's client area that will contain the video.</span></span> <span data-ttu-id="0bef5-150">Die VMR sorgt für das Video Bild für das Quell Rechteck und dehnt das abgeschnittene Bild so aus, dass es an das Ziel Rechteck angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="0bef5-150">The VMR crops the video image to the source rectangle and stretches the cropped image to fit the destination rectangle.</span></span>

<span data-ttu-id="0bef5-151">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="0bef5-151">**VMR-7**</span></span>

1.  <span data-ttu-id="0bef5-152">Um beide Rechtecke anzugeben, können Sie die [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0bef5-152">Call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="0bef5-153">Das Quell Rechteck muss kleiner oder gleich der systemeigenen Videogröße sein. Sie können die [**ivmrwindowlesscontrol:: getnativevideosize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) -Methode verwenden, um die systemeigene Videogröße zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bef5-153">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="0bef5-154">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="0bef5-154">**VMR-9**</span></span>

1.  <span data-ttu-id="0bef5-155">Aufrufen der [**IVMRWindowlessControl9:: setvideoposition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) -Methode, um beide Rechtecke anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0bef5-155">Call the [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="0bef5-156">Das Quell Rechteck muss kleiner oder gleich der systemeigenen Videogröße sein. Sie können die [**IVMRWindowlessControl9:: getnativevideosize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) -Methode verwenden, um die systemeigene Videogröße zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bef5-156">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="0bef5-157">Der folgende Code legt z. b. die Quell-und Ziel Rechtecke für VMR-7 fest.</span><span class="sxs-lookup"><span data-stu-id="0bef5-157">For example, the following code sets the source and destination rectangles for the VMR-7.</span></span> <span data-ttu-id="0bef5-158">Das Quell Rechteck wird auf das gesamte Video Bild festgelegt, und das Ziel Rechteck entspricht dem gesamten Fenster Client Bereich:</span><span class="sxs-lookup"><span data-stu-id="0bef5-158">It sets the source rectangle equal to the entire video image, and the destination rectangle equal to the entire window client area:</span></span>


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



<span data-ttu-id="0bef5-159">Wenn Sie ein Video mit einem kleineren Teil des Client Bereichs belegen möchten, ändern Sie den *rcdest* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="0bef5-159">If you want to video to occupy a smaller portion of the client area, modify the *rcDest* parameter.</span></span> <span data-ttu-id="0bef5-160">Wenn Sie das Video Bild zuschneiden möchten, ändern Sie den *rcsrc* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="0bef5-160">If you want to crop the video image, modify the *rcSrc* parameter.</span></span>

## <a name="handle-window-messages"></a><span data-ttu-id="0bef5-161">Fenster Meldungen behandeln</span><span class="sxs-lookup"><span data-stu-id="0bef5-161">Handle Window Messages</span></span>

<span data-ttu-id="0bef5-162">Da VMR kein eigenes Fenster hat, muss es benachrichtigt werden, wenn das Video neu gezeichnet oder die Größe des Videos geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0bef5-162">Because the VMR does not have its own window, it must be notified if it need to repaint or resize the video.</span></span> <span data-ttu-id="0bef5-163">Reagieren Sie auf die folgenden Fenster Meldungen, indem Sie die aufgeführten VMR-Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0bef5-163">Respond to the following window messages by calling the VMR methods listed.</span></span>

<span data-ttu-id="0bef5-164">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="0bef5-164">**VMR-7**</span></span>

1.  <span data-ttu-id="0bef5-165">[**WM \_ Paint**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="0bef5-165">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="0bef5-166">Nennen Sie [**ivmrwindowlesscontrol:: repaintvideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="0bef5-166">Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span> <span data-ttu-id="0bef5-167">Diese Methode bewirkt, dass VMR-7 den neuesten Videoframe neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="0bef5-167">This method causes the VMR-7 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="0bef5-168">[**WM \_ Display Change**](../gdi/wm-displaychange.md): der Befehl [**ivmrwindowlesscontrol::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="0bef5-168">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="0bef5-169">Diese Methode benachrichtigt VMR-7, dass das Video mit einer neuen Auflösung oder Farbtiefe angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0bef5-169">This method notifies the VMR-7 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="0bef5-170">[**WM \_ Size**](../winmsg/wm-size.md) oder [**WM \_ windowposchge**](../winmsg/wm-windowposchanged.md): Berechnen Sie die Position des Videos neu, und wenden Sie [**ivmrwindowlesscontrol:: setvideoposition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) an, um die Position bei Bedarf zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0bef5-170">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) to update the position, if needed.</span></span>

<span data-ttu-id="0bef5-171">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="0bef5-171">**VMR-9**</span></span>

1.  <span data-ttu-id="0bef5-172">[**WM \_ Paint**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="0bef5-172">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="0bef5-173">Nennen Sie [**IVMRWindowlessControl9:: repaintvideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="0bef5-173">Call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span> <span data-ttu-id="0bef5-174">Diese Methode bewirkt, dass VMR-9 den neuesten Videorahmen neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="0bef5-174">This method causes the VMR-9 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="0bef5-175">[**WM \_ Display Change**](../gdi/wm-displaychange.md): IVMRWindowlessControl9 aufgerufen [**::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="0bef5-175">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span> <span data-ttu-id="0bef5-176">Diese Methode benachrichtigt VMR-9, dass das Video mit einer neuen Auflösung oder Farbtiefe angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0bef5-176">This method notifies the VMR-9 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="0bef5-177">[**WM \_ Size**](../winmsg/wm-size.md) oder [**WM \_ windowposchangi:**](../winmsg/wm-windowposchanged.md)berechnet die Position des Videos neu und ruft [**IVMRWindowlessControl9:: setvideoposition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) auf, um die Position bei Bedarf zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0bef5-177">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) to update the position, if needed.</span></span>

> [!Note]  
> <span data-ttu-id="0bef5-178">Der Standard Handler für die [**WM- \_ windowposchge**](../winmsg/wm-windowposchanged.md) -Nachricht sendet eine [**WM- \_ Größen**](../winmsg/wm-size.md) Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0bef5-178">The default handler for the [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) message sends a [**WM\_SIZE**](../winmsg/wm-size.md) message.</span></span> <span data-ttu-id="0bef5-179">Wenn Ihre Anwendung jedoch **WM \_ windowposchge** abfängt und Sie nicht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, sollten Sie **setvideoposition** zusätzlich zu Ihrem WM- **\_ Größen** Handler in Ihrem **WM- \_ windowposchge** -Handler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0bef5-179">But if your application intercepts **WM\_WINDOWPOSCHANGED** and does not pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), you should call **SetVideoPosition** in your **WM\_WINDOWPOSCHANGED** handler, in addition to your **WM\_SIZE** handler.</span></span>

 

<span data-ttu-id="0bef5-180">Das folgende Beispiel zeigt einen [**WM \_ Paint**](../gdi/wm-paint.md) -Meldungs Handler.</span><span class="sxs-lookup"><span data-stu-id="0bef5-180">The following example shows a [**WM\_PAINT**](../gdi/wm-paint.md) message handler.</span></span> <span data-ttu-id="0bef5-181">Es zeichnet einen Bereich, der durch das Client Rechteck abzüglich des Video Rechtecks definiert wird.</span><span class="sxs-lookup"><span data-stu-id="0bef5-181">It paints a region defined by the client rectangle minus the video rectangle.</span></span> <span data-ttu-id="0bef5-182">Ziehen Sie nicht auf das Video Rechteck, da das VMR darauf zeigt, was zu einem Flimmern führt.</span><span class="sxs-lookup"><span data-stu-id="0bef5-182">Do not draw onto the video rectangle, because the VMR will paint over it, causing flickering.</span></span> <span data-ttu-id="0bef5-183">Legen Sie aus demselben Grund keinen Hintergrund Pinsel in der Fenster Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="0bef5-183">For the same reason, do not set a background brush in your window class.</span></span>


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



<span data-ttu-id="0bef5-184">Obwohl Sie auf [**WM \_ Paint**](../gdi/wm-paint.md) -Meldungen Antworten müssen, müssen Sie zwischen **WM \_ Paint** -Meldungen nichts tun, um das Video zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0bef5-184">Although you must respond to [**WM\_PAINT**](../gdi/wm-paint.md) messages, there is nothing you need to do between **WM\_PAINT** messages to update the video.</span></span> <span data-ttu-id="0bef5-185">Wie in diesem Beispiel gezeigt, können Sie das Video Bild im fensterlosen Modus einfach als selbst Zeichnungs Bereich im Fenster behandeln.</span><span class="sxs-lookup"><span data-stu-id="0bef5-185">As this example shows, windowless mode lets you treat the video image simply as a self-drawing region on the window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bef5-186">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bef5-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bef5-187">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="0bef5-187">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="0bef5-188">Videorendering</span><span class="sxs-lookup"><span data-stu-id="0bef5-188">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
