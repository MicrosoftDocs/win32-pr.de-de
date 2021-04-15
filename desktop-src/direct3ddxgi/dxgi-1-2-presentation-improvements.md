---
title: Kippen von Modellen, Dirty Rechtecke, scrollt-Bereiche
description: DXGI 1,2 unterstützt eine neue Swapkette für das Flip-Modell, geänderte Rechtecke und aufgeschlüsselten Bereichen. Wir erläutern die Vorteile der Verwendung der neuen pullmodellaustauschkette und der Optimierung der Präsentation durch die Angabe von Änderungs Rechtecke und den Bereichen mit Rollup.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104570187"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a><span data-ttu-id="2bd1c-104">Kippen von Modellen, Dirty Rechtecke, scrollt-Bereiche</span><span class="sxs-lookup"><span data-stu-id="2bd1c-104">Flip model, dirty rectangles, scrolled areas</span></span>

<span data-ttu-id="2bd1c-105">DXGI 1,2 unterstützt eine neue Swapkette für das Flip-Modell, geänderte Rechtecke und aufgeschlüsselten Bereichen.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-105">DXGI 1.2 supports a new flip-model swap chain, dirty rectangles, and scrolled areas.</span></span> <span data-ttu-id="2bd1c-106">Wir erläutern die Vorteile der Verwendung der neuen pullmodellaustauschkette und der Optimierung der Präsentation durch die Angabe von Änderungs Rechtecke und den Bereichen mit Rollup.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-106">We explain the benefits of using the new flip-model swap chain and of optimizing presentation by specifying dirty rectangles and scrolled areas.</span></span>

## <a name="dxgi-flip-model-presentation"></a><span data-ttu-id="2bd1c-107">DXGI-Flip-Model-Präsentation</span><span class="sxs-lookup"><span data-stu-id="2bd1c-107">DXGI flip-model presentation</span></span>

<span data-ttu-id="2bd1c-108">DXGI 1,2 fügt Unterstützung für das Flip Presentation Model für Direct3D 10-APIs und spätere APIs hinzu.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-108">DXGI 1.2 adds support for the flip presentation model for Direct3D 10 and later APIs.</span></span> <span data-ttu-id="2bd1c-109">In Windows 7 hat Direct3D 9Ex zuerst die [Flip-Model-Präsentation](../direct3darticles/direct3d-9ex-improvements.md) angenommen, um zu verhindern, dass der Austausch Ketten Puffer unnötig kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-109">In Windows 7, Direct3D 9EX first adopted [flip-model presentation](../direct3darticles/direct3d-9ex-improvements.md) to avoid unnecessarily copying the swap-chain buffer.</span></span> <span data-ttu-id="2bd1c-110">Durch die Verwendung von Flip Model werden backpuffervorgänge zwischen der Laufzeit und der Desktopfenster-Manager (DWM) gekippt, sodass DWM immer direkt aus dem Hintergrund Puffer besteht, anstatt den Inhalt des hinterpuffers zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-110">By using flip model, back buffers are flipped between the runtime and Desktop Window Manager (DWM), so DWM always composes directly from the back buffer instead of copying the back buffer content.</span></span>

<span data-ttu-id="2bd1c-111">DXGI 1,2-APIs enthalten eine überarbeitete DXGI-SwapChain-Schnittstelle, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="2bd1c-111">DXGI 1.2 APIs include a revised DXGI swap-chain interface, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="2bd1c-112">Sie können mehrere [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) -Schnittstellen Methoden verwenden, um das entsprechende **IDXGISwapChain1** -Objekt für die Verwendung mit einem [**HWND**](../winprog/windows-data-types.md) -handle, einem [corewindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) -Objekt, einer [directcomposition](../directcomp/directcomposition-portal.md)oder dem [**Windows. UI. XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) -Framework zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-112">You can use multiple [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) interface methods to create the appropriate **IDXGISwapChain1** object to use with an [**HWND**](../winprog/windows-data-types.md) handle, a [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) object, [DirectComposition](../directcomp/directcomposition-portal.md), or the [**Windows.UI.Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) framework.</span></span>

<span data-ttu-id="2bd1c-113">Wählen Sie das Modell zum Kippen der Darstellung aus, indem Sie den [**DXGI-swapffekt-Wert für die \_ \_ \_ \_ sequenzielle**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) Enumeration im **SwapEffect** -Member der [**DXGI- \_ \_ SwapChain \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) -Struktur und den **BUFFERCOUNT** -Member der **DXGI- \_ Swap- \_ Kette \_ DESC1** auf mindestens 2 festlegen.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-113">You select the flip presentation model by specifying the [**DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) enumeration value in the **SwapEffect** member of the [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and by setting the **BufferCount** member of **DXGI\_SWAP\_CHAIN\_DESC1** to a minimum of 2.</span></span> <span data-ttu-id="2bd1c-114">Weitere Informationen zur Verwendung des DXGI-Flip-Modells finden Sie unter [DXGI Flip Model](dxgi-flip-model.md).</span><span class="sxs-lookup"><span data-stu-id="2bd1c-114">For more info about how to use DXGI flip model, see [DXGI flip model](dxgi-flip-model.md).</span></span> <span data-ttu-id="2bd1c-115">Aufgrund der glatteren Präsentation des Flip Presentation Model und anderer neuer Funktionen empfiehlt es sich, das Modell "Flip Presentation Model" für alle neuen apps zu verwenden, die Sie mit Direct3D 10-und höher-APIs schreiben.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-115">Because of the flip presentation model's smoother presentation and other new functionality, we recommend that you use flip presentation model for all new apps that you write with Direct3D 10 and later APIs.</span></span>

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a><span data-ttu-id="2bd1c-116">Verwenden von Dirty Rechtecke und des Schiebe Rechtecks bei der Präsentation der Austausch Kette</span><span class="sxs-lookup"><span data-stu-id="2bd1c-116">Using dirty rectangles and the scroll rectangle in swap chain presentation</span></span>

<span data-ttu-id="2bd1c-117">Durch die Verwendung von Dirty Rechtecke und des Bild Lauf Rechtecks in der Präsentation der Austausch Kette sparen Sie die Nutzung der Speicherbandbreite und die damit verbundene Nutzung der Systemleistung, da die Menge der Pixeldaten, die das Betriebssystem zum Zeichnen des nächsten dargestellten Frames benötigt, reduziert wird, wenn das Betriebssystem nicht den gesamten Frame zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-117">By using dirty rectangles and the scroll rectangle in swap chain presentation, you save on the usage of memory bandwidth and the related usage of system power because the amount of pixel data that the operating system needs to draw the next presented frame is reduced if the operating system doesn't need to draw the entire frame.</span></span> <span data-ttu-id="2bd1c-118">Für apps, die häufig über Remotedesktopverbindung und andere Technologien für den Remote Zugriff angezeigt werden, sind die Einsparungen besonders in der Anzeigequalität erkennbar, da diese Technologien geänderte Rechtecke und Bild Lauf Metadaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-118">For apps that are often displayed via Remote Desktop Connection and other remote-accessing technologies, the savings are particularly noticeable in the display quality because these technologies use dirty rectangles and scroll metadata.</span></span>

<span data-ttu-id="2bd1c-119">Sie können Scroll nur mit DXGI-Swapketten verwenden, die im Flip Presentation Model ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-119">You can use scroll only with DXGI swap chains that run in flip presentation model.</span></span> <span data-ttu-id="2bd1c-120">Sie können Dirty Rechtecke mit DXGI-Swapketten verwenden, die sowohl im Flip Model-als auch im BitBLT-Modell ausgeführt werden (festgelegt mit [**DXGI- \_ \_ swapffekt \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)</span><span class="sxs-lookup"><span data-stu-id="2bd1c-120">You can use dirty rectangles with DXGI swap chains that run in both flip model and bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span>

<span data-ttu-id="2bd1c-121">In diesem Szenario und dieser Abbildung zeigen wir die Funktionalität der Verwendung von Änderungs Rechtecke und des Bildlaufs.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-121">In this scenario and illustration we show the functionality of using dirty rectangles and scroll.</span></span> <span data-ttu-id="2bd1c-122">Hier enthält eine Bild lauffähigen App Text und animationsvideos.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-122">Here, a scrollable app contains text and animating video.</span></span> <span data-ttu-id="2bd1c-123">Die APP verwendet Dirty Rechtecke, um nur das Animationsvideo und die neue Zeile für das Fenster zu aktualisieren, anstatt das gesamte Fenster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-123">The app uses dirty rectangles to just update the animating video and new line for the window, instead of updating the entire window.</span></span> <span data-ttu-id="2bd1c-124">Mit dem scrollrechteck kann das Betriebssystem den zuvor gerenderten Inhalt in den neuen Frame kopieren und übersetzen und nur die neue Zeile im neuen Frame rendern.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-124">The scroll rectangle allows the operating system to copy and translate the previously rendered content on the new frame and to render only the new line on the new frame.</span></span>

<span data-ttu-id="2bd1c-125">Die APP führt eine Präsentation durch Aufrufen der [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Methode aus.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-125">The app performs presentation by calling the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method.</span></span> <span data-ttu-id="2bd1c-126">In diesem-Befehl übergibt die APP einen Zeiger auf eine [**DXGI-Struktur der \_ vorhandenen \_ Parameter**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) , die geänderte Rechtecke und die Anzahl der modifizierten Rechtecke, das Schiebe Rechteck und den zugeordneten Bild Lauf Offset oder sowohl geänderte Rechtecke als auch das Schiebe Rechteck enthält.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-126">In this call, the app passes a pointer to a [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) structure that includes dirty rectangles and the number of dirty rectangles, or the scroll rectangle and the associated scroll offset, or both dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="2bd1c-127">Unsere App übergibt 2 geänderte Rechtecke und das Schiebe Rechteck.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-127">Our app passes 2 dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="2bd1c-128">Das Schiebe Rechteck ist der Bereich des vorherigen Frames, der vom Betriebssystem in den aktuellen Frame kopiert werden muss, bevor der aktuelle Frame gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-128">The scroll rectangle is the area of the previous frame that the operating system needs to copy to the current frame before it renders the current frame.</span></span> <span data-ttu-id="2bd1c-129">Die APP gibt das Animationsvideo und die neue Zeile als modifizierte Rechtecke an, und das Betriebssystem rendert Sie im aktuellen Frame.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-129">The app specifies the animating video and new line as dirty rectangles, and the operating system renders them on the current frame.</span></span>

![Abbildung der überlappenden Scroll-und Dirty Rechtecke](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

<span data-ttu-id="2bd1c-131">Das gestrichelte Rechteck zeigt das Bild Lauf Rechteck im aktuellen Frame an.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-131">The dashed rectangle shows the scroll rectangle in the current frame.</span></span> <span data-ttu-id="2bd1c-132">Das Bild Lauf Rechteck wird vom **pscrollrect** -Member von [**DXGI \_ Present- \_ Parametern**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters)angegeben.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-132">The scroll rectangle is specified by the **pScrollRect** member of [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span></span> <span data-ttu-id="2bd1c-133">Der Pfeil zeigt den scrolloffset an.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-133">The arrow shows the scroll offset.</span></span> <span data-ttu-id="2bd1c-134">Der Bild Lauf Offset wird vom **pscrolloffset** -Member von **DXGI \_ Present- \_ Parametern** angegeben.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-134">The scroll offset is specified by the **pScrollOffset** member of **DXGI\_PRESENT\_PARAMETERS**.</span></span> <span data-ttu-id="2bd1c-135">Gefüllte Rechtecke zeigen geänderte Rechtecke an, dass die APP mit neuem Inhalt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-135">Filled rectangles show dirty rectangles that the app updated with new content.</span></span> <span data-ttu-id="2bd1c-136">Die gefüllten Rechtecke werden von den **dirtyreczcount** -und **pdirtyrects** -Membern von **DXGI \_ Present- \_ Parametern** angegeben.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-136">The filled rectangles are specified by the **DirtyRectsCount** and **pDirtyRects** members of **DXGI\_PRESENT\_PARAMETERS**.</span></span>

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a><span data-ttu-id="2bd1c-137">Beispiel 2: Puffer-Swap-Kette mit Änderungs Rechtecke und Schiebe Rechteck</span><span class="sxs-lookup"><span data-stu-id="2bd1c-137">Sample 2-buffer flip-model swap chain with dirty rectangles and scroll rectangle</span></span>

<span data-ttu-id="2bd1c-138">Die nächste Abbildung und Sequenz zeigt ein Beispiel für einen DXGI Flip-Model Presentation-Vorgang, der geänderte Rechtecke und ein scrollrechteck verwendet.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-138">The next illustration and sequence shows an example of a DXGI flip-model presentation operation that uses dirty rectangles and a scroll rectangle.</span></span> <span data-ttu-id="2bd1c-139">In diesem Beispiel verwenden wir die minimale Anzahl von Puffern für die Darstellung von Flip-Modellen, bei der es sich um eine Puffer Anzahl von zwei handelt, einen vorderen Puffer, der den Inhalt der APP anzeigt, und einen Hintergrund Puffer, der den aktuellen Frame enthält, den die APP Renderen möchte.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-139">In this example we use the minimum number of buffers for flip-model presentation, which is a buffer count of two, one front buffer that contains the app display content and one back buffer that contains the current frame that the app wants to render.</span></span>

1.  <span data-ttu-id="2bd1c-140">Wie im Vorder-Puffer am Anfang des Frames gezeigt, zeigt die scrollbare App anfänglich einen Frame mit Text und animationsvideos an.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-140">As shown in the front buffer at the beginning of the frame, the scrollable app initially shows a frame with some text and animating video.</span></span>
2.  <span data-ttu-id="2bd1c-141">Um den nächsten Frame zu rendern, rendert die APP auf dem Hintergrund Puffer die geänderten Rechtecke, die das Animationsvideo aktualisieren, und die neue Zeile für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-141">To render the next frame, the app renders onto the back buffer the dirty rectangles that update the animating video and the new line for the window.</span></span>
3.  <span data-ttu-id="2bd1c-142">Wenn die APP [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)aufruft, werden die Änderungs Rechtecke und das Schiebe Rechteck und der Offset angegeben.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-142">When the app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), it specifies the dirty rectangles and the scroll rectangle and offset.</span></span> <span data-ttu-id="2bd1c-143">Die Laufzeit kopiert das Schiebe Rechteck aus dem vorherigen Frame minus den aktualisierten, modifizierten Rechtecke auf den aktuellen Hintergrund Puffer.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-143">The runtime next copies the scroll rectangle from the previous frame minus the updated dirty rectangles onto the current back buffer.</span></span>
4.  <span data-ttu-id="2bd1c-144">Die Laufzeit vertauscht schließlich die Vorder-und Hintergrund Puffer.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-144">The runtime finally swaps the front and back buffers.</span></span>

![Beispiel für eine Swap-Modell-SwapChain mit Scroll-und Dirty Rechtecke](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a><span data-ttu-id="2bd1c-146">Nachverfolgen von Dirty Rechtecke und scrollrechtecke über mehrere Frames hinweg</span><span class="sxs-lookup"><span data-stu-id="2bd1c-146">Tracking dirty rectangles and scroll rectangles across multiple frames</span></span>

<span data-ttu-id="2bd1c-147">Wenn Sie in Ihrer APP modifizierte Rechtecke verwenden, müssen Sie die geänderten Rechtecke nachverfolgen, um inkrementelles Rendering zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2bd1c-147">When you use dirty rectangles in your app, you must track the dirty rectangles to support incremental rendering.</span></span> <span data-ttu-id="2bd1c-148">Wenn Ihre APP [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) mit Dirty Rechtecke aufruft, müssen Sie sicherstellen, dass jedes Pixel innerhalb der modifizierten Rechtecke auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-148">When your app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) with dirty rectangles, you must ensure that every pixel within the dirty rectangles is up to date.</span></span> <span data-ttu-id="2bd1c-149">Wenn Sie den gesamten Bereich des Dirty-Rechtecks nicht vollständig neu rendern oder wenn Sie für bestimmte Bereiche, die sich in der Hand befinden, nicht wissen, müssen Sie einige Daten aus dem vorherigen vollständig zusammenhängenden Hintergrund Puffer in den aktuellen, veralteten Hintergrund Puffer kopieren, bevor Sie das Rendering starten.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-149">If you aren't completely re-rendering the whole area of the dirty rectangle or if you can’t know for certain the areas that are dirtied, you must copy some data from the previous fully coherent back buffer to the current, stale back buffer before you start rendering.</span></span>

<span data-ttu-id="2bd1c-150">Die Laufzeit kopiert nur die Unterschiede zwischen den aktualisierten Bereichen des vorherigen Frames und den aktualisierten Bereichen des aktuellen Frames auf den aktuellen Hintergrund Puffer.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-150">The runtime copies only the differences between updated areas of the previous frame and updated areas of the current frame onto the current back buffer.</span></span> <span data-ttu-id="2bd1c-151">Wenn sich diese Bereiche überschneiden, kopiert die Runtime nur den Unterschied zwischen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-151">If these areas intersect, the runtime copies only the difference between them.</span></span> <span data-ttu-id="2bd1c-152">Wie Sie im folgenden Diagramm und in der folgenden Reihenfolge sehen können, müssen Sie die Schnittmenge zwischen dem Dirty-Rechteck von Frame 1 und dem Dirty Rechteck von Frame 2 in das Dirty-Rechteck von Frame 2 kopieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-152">As you can see in the following diagram and sequence, you must copy the intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>

1.  <span data-ttu-id="2bd1c-153">In Frame 1 ist ein Dirty Rechteck vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-153">Present dirty rectangle in frame 1.</span></span>
2.  <span data-ttu-id="2bd1c-154">Kopieren Sie die Schnittmenge zwischen dem Dirty-Rechteck von Frame 1 und dem Dirty Rechteck von Frame 2 in das geänderte Rechteck von Frame 2.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-154">Copy intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>
3.  <span data-ttu-id="2bd1c-155">Geändertes Rechteck in Frame 2 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-155">Present dirty rectangle in frame 2.</span></span>

![Nachverfolgen von Scroll-und Dirty Rechtecke über mehrere Frames hinweg](images/track-dirty-rects-scroll-rects.png)

<span data-ttu-id="2bd1c-157">Zum verallgemeinern für eine Swapkette mit N Puffern wird der Bereich, der von der Laufzeit vom letzten Frame zum aktuellen Frame auf dem aktuellen Frame kopiert wird, wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="2bd1c-157">To generalize, for a swap chain with N buffers, the area that the runtime copies from the last frame to the current frame on the current frame’s present is:</span></span>

![Gleichung zum Berechnen des Bereichs, der von der Laufzeit kopiert wird](images/runtime-copy-equation.png)

<span data-ttu-id="2bd1c-159">Where Buffer gibt den Puffer Index in einer Swapkette an, beginnend mit dem aktuellen Puffer Index bei Null.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-159">where buffer indicates the buffer index in a swap chain, starting with current buffer index at zero.</span></span>

<span data-ttu-id="2bd1c-160">Sie können alle Schnittpunkte zwischen dem vorherigen Frame und den geänderten Rechtecke des aktuellen Frames nachverfolgen, indem Sie eine Kopie der modifizierten Rechtecke des vorherigen Frames aufbewahren oder die Änderungs Rechtecke des neuen Frames mit dem entsprechenden Inhalt aus dem vorherigen Frame neu rendern.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-160">You can keep track of any intersections between the previous frame and the current frame’s dirty rectangles by keeping a copy of the previous frame’s dirty rectangles or by re-rendering the new frame’s dirty rectangles with the appropriate content from the previous frame.</span></span>

<span data-ttu-id="2bd1c-161">Entsprechend müssen Sie in den Fällen, in denen die Swapkette mehr als zwei Back-Puffer aufweist, sicherstellen, dass sich überlappende Bereiche zwischen den geänderten Rechtecke des aktuellen Puffers und den geänderten Rechtecke aller vorherigen Frames kopiert oder erneut gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-161">Similarly, in the cases where the swap chain has more than 2 back buffers, you must ensure that overlapping areas between the current buffer’s dirty rectangles and the dirty rectangles of all previous frame’s are copied or re-rendered.</span></span>

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a><span data-ttu-id="2bd1c-162">Nachverfolgen einer einzelnen Schnittmenge zwischen 2 modifizierten Rechtecke</span><span class="sxs-lookup"><span data-stu-id="2bd1c-162">Tracking a single intersection between 2 dirty rectangles</span></span>

<span data-ttu-id="2bd1c-163">Im einfachsten Fall, wenn Sie ein einzelnes Dirty Rechteck pro Frame aktualisieren, können sich die geänderten Rechtecke über zwei Frames hinweg überschneiden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-163">In the simplest case, when you update a single dirty rectangle per frame, the dirty rectangles across two frames might intersect.</span></span> <span data-ttu-id="2bd1c-164">Um herauszufinden, ob sich das geänderte Rechteck des vorherigen Frames und das geänderte Rechteck des aktuellen Frames überlappen, müssen Sie überprüfen, ob sich das geänderte Rechteck des vorherigen Frames mit dem modifizierten Rechteck des aktuellen Frames überschneidet.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-164">To find out whether the dirty rectangle of the previous frame and the dirty rectangle of the current frame overlap, you need to verify whether the dirty rectangle of the previous frame intersects with the dirty rectangle of the current frame.</span></span> <span data-ttu-id="2bd1c-165">Sie können die GDI [**intersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) -Funktion aufzurufen, um zu bestimmen, ob zwei [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen, die die beiden geänderten Rechtecke darstellen, sich überschneiden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-165">You can call the GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) function to determine whether two [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that represent the two dirty rectangles intersect.</span></span>

<span data-ttu-id="2bd1c-166">In diesem Code Ausschnitt gibt ein Aufruf von [**intersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) die Schnittmenge zweier Dirty Rechtecke in einem anderen [**Rect**](/previous-versions//dd162897(v=vs.85)) namens dirtyrectcopy zurück.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-166">In this code snippet, a call to [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) returns the intersection of two dirty rectangles in another [**RECT**](/previous-versions//dd162897(v=vs.85)) called dirtyRectCopy.</span></span> <span data-ttu-id="2bd1c-167">Nachdem der Code Ausschnitt feststellt, dass sich die beiden modifizierten Rechtecke überschneiden, wird die [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) -Methode aufgerufen, um den Bereich der Schnittmenge in den aktuellen Frame zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-167">After the code snippet determines that the two dirty rectangles intersect, it calls the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy the region of intersection into the current frame.</span></span>

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

<span data-ttu-id="2bd1c-168">Wenn Sie diesen Code Ausschnitt in Ihrer Anwendung verwenden, ist die APP bereit zum Abrufen von [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , um den aktuellen Frame mit dem aktuellen, geänderten Rechteck zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-168">If you use this code snippet in your application, the app will then be ready to call [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) to update the current frame with the current dirty rectangle.</span></span>

### <a name="tracking-intersections-between-n-dirty-rectangles"></a><span data-ttu-id="2bd1c-169">Nachverfolgen von Schnittpunkten zwischen N Änderungs Rechtecke</span><span class="sxs-lookup"><span data-stu-id="2bd1c-169">Tracking intersections between N dirty rectangles</span></span>

<span data-ttu-id="2bd1c-170">Wenn Sie mehrere modifizierte Rechtecke angeben, die ein geändertes Rechteck für die neu aufgezeigte scrolllinie pro Frame einschließen können, müssen Sie alle Überschneidungen überprüfen und nachverfolgen, die zwischen allen modifizierten Rechtecke des vorherigen Frames und allen geänderten Rechtecke des aktuellen Frames auftreten können.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-170">If you specify multiple dirty rectangles, which can include a dirty rectangle for the newly revealed scroll line, per frame, you need to verify and track any overlaps that might occur between all the dirty rectangles of the previous frame and all the dirty rectangles of the current frame.</span></span> <span data-ttu-id="2bd1c-171">Um die Schnittpunkte zwischen den modifizierten Rechtecke des vorherigen Frames und den geänderten Rechtecke des aktuellen Frames zu berechnen, können Sie die geänderten Rechtecke in den Regionen gruppieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-171">To calculate the intersections between the dirty rectangles of the previous frame and the dirty rectangles of the current frame, you can group the dirty rectangles into regions.</span></span>

<span data-ttu-id="2bd1c-172">In diesem Code Ausschnitt wird die GDI-Funktion " [**setrectrgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) " aufgerufen, um jedes geänderte Rechteck in einen rechteckigen Bereich zu konvertieren. Anschließend wird die GDI [**combinergn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) -Funktion aufgerufen, um alle geänderten rechteckigen Bereiche in einer Gruppe zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-172">In this code snippet, we call the GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) function to convert each dirty rectangle into a rectangular region and then we call the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to combine all the dirty rectangular regions into a group.</span></span>

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

<span data-ttu-id="2bd1c-173">Sie können jetzt die GDI [**combinergn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) -Funktion verwenden, um die Schnittmenge zwischen dem geänderten Bereich des vorherigen Frames und dem geänderten Bereich des aktuellen Frames zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-173">You can now use the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to determine the intersection between the dirty region of the previous frame and the dirty region of the current frame.</span></span> <span data-ttu-id="2bd1c-174">Nachdem Sie den sich überschneidenden Bereich abgerufen haben, rufen Sie die GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) -Funktion auf, um jedes einzelne Rechteck aus dem überschneidenden Bereich abzurufen, und rufen Sie dann die [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) -Methode auf, um jedes überschneidende Rechteck in den aktuellen Hintergrund Puffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-174">After you obtain the intersecting region, call the GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) function to obtain each individual rectangle from the intersecting region and then call the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy each intersecting rectangle into the current back buffer.</span></span> <span data-ttu-id="2bd1c-175">Der nächste Code Ausschnitt zeigt, wie diese GDI-und Direct3D-Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-175">The next code snippet shows how to use these GDI and Direct3D functions.</span></span>

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a><span data-ttu-id="2bd1c-176">BitBLT-Modell Austausch Kette mit Dirty Rechtecke</span><span class="sxs-lookup"><span data-stu-id="2bd1c-176">Bitblt model swap chain with dirty rectangles</span></span>

<span data-ttu-id="2bd1c-177">Sie können Dirty Rechtecke mit DXGI-Austausch Ketten verwenden, die im BitBLT-Modell ausgeführt werden (festgelegt mit [**DXGI- \_ Swap- \_ Effekt \_ sequenziell**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="2bd1c-177">You can use dirty rectangles with DXGI swap chains that run in bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span> <span data-ttu-id="2bd1c-178">BitBLT-Modell Austausch Ketten, die mehr als einen Puffer verwenden, müssen überlappende geänderte Rechtecke auf die gleiche Weise nachverfolgen, wie in nach [Verfolgen von Dirty Rechtecke und Bild Lauf Rechtecke über mehrere Frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) für das Kippen von Modell Austausch Ketten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-178">Bitblt model swap chains that use more than one buffer must also track overlapping dirty rectangles across frames in the same way as described in [Tracking dirty rectangles and scroll rectangles across multiple frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) for flip model swap chains.</span></span> <span data-ttu-id="2bd1c-179">BitBLT-Modell Austausch Ketten mit nur einem Puffer müssen überlappende geänderte Rechtecke nicht nachverfolgt werden, da der gesamte Puffer jedes Frame neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-179">Bitblt model swap chains with just one buffer need not track overlapping dirty rectangles because the entire buffer is redrawn every frame.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bd1c-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2bd1c-180">Related topics</span></span>

[<span data-ttu-id="2bd1c-181">DXGI 1,2-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="2bd1c-181">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
