---
description: Steuern eines Erfassungsdiagramms
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Steuern eines Erfassungsdiagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00573256c1c010e23dfc598ceca5ac62d772711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119475"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="5d1e0-103">Steuern eines Erfassungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="5d1e0-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="5d1e0-104">Die [**IMediaControl-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediacontrol) des Filtergraph-Managers verfügt über Methoden zum Ausführen, Beenden und Anhalten des gesamten Graphen.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="5d1e0-105">Wenn das Filterdiagramm jedoch über Erfassungs- und Vorschaudatenströme verfügt, sollten Sie die beiden Datenströme unabhängig voneinander steuern.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="5d1e0-106">Es kann beispielsweise sein, dass Sie eine Vorschau des Videos anzeigen möchten, ohne es zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="5d1e0-107">Hierzu können Sie die [**ICaptureGraphBuilder2::ControlStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="5d1e0-108">Diese Methode funktioniert nicht bei der Erfassung in einer ASF-Datei (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="5d1e0-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="5d1e0-109">Steuern des Erfassungsstreams</span><span class="sxs-lookup"><span data-stu-id="5d1e0-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="5d1e0-110">Der folgende Code legt fest, dass der Videoaufzeichnungsstream vier Sekunden lang ausgeführt wird und eine Sekunde nach der Ausführung des Diagramms beginnt:</span><span class="sxs-lookup"><span data-stu-id="5d1e0-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="5d1e0-111">Der erste Parameter gibt an, welcher Stream als PIN-Kategorie-GUID gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="5d1e0-112">Der zweite Parameter gibt den Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-112">The second parameter gives the media type.</span></span> <span data-ttu-id="5d1e0-113">Der dritte Parameter ist ein Zeiger auf den Erfassungsfilter.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="5d1e0-114">Um alle Erfassungsstreams im Diagramm zu steuern, legen Sie den zweiten und dritten Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="5d1e0-115">Die nächsten beiden Parameter definieren die Zeiten, zu denen der Stream gestartet und beendet wird, relativ zur Zeit, zu der das Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="5d1e0-116">Rufen Sie [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) auf, um das Diagramm auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="5d1e0-117">Bis sie das Diagramm ausführen, hat die **ControlStream-Methode** keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="5d1e0-118">Wenn das Diagramm bereits ausgeführt wird, werden die Einstellungen sofort wirksam.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="5d1e0-119">Die letzten beiden Parameter werden zum Abrufen von Ereignisbenachrichtigungen verwendet, wenn der Stream gestartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="5d1e0-120">Für jeden Stream, den Sie mit dieser Methode steuern, sendet das Filterdiagramm ein Ereignispaar: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) beim Starten des Streams und [**EC STREAM CONTROL \_ \_ \_ STOPPED,**](ec-stream-control-stopped.md) wenn der Stream beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="5d1e0-121">Die Werte von **wStartCookie** und **wStopCookie** werden als zweiter Ereignisparameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="5d1e0-122">Daher entspricht *lParam2* im Startereignis **wStartCookie** und *lParam2* im Beendigungsereignis **wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="5d1e0-123">Der folgende Code zeigt, wie diese Ereignisse abzurufen sind:</span><span class="sxs-lookup"><span data-stu-id="5d1e0-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="5d1e0-124">Die **ControlStream-Methode** definiert einige spezielle Werte für die Start- und Beendigungszeiten.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="5d1e0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5d1e0-125">Value</span></span> | <span data-ttu-id="5d1e0-126">Start</span><span class="sxs-lookup"><span data-stu-id="5d1e0-126">Start</span></span>                                  | <span data-ttu-id="5d1e0-127">Beenden</span><span class="sxs-lookup"><span data-stu-id="5d1e0-127">Stop</span></span>                               |
|-------------|----------------------------------------|---------|
| <span data-ttu-id="5d1e0-128">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="5d1e0-128">MAXLONGLONG</span></span> | <span data-ttu-id="5d1e0-129">Starten Sie diesen Stream nie.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-129">Never start this stream.</span></span>               | <span data-ttu-id="5d1e0-130">Beenden Sie nicht, bis das Diagramm beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-130">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="5d1e0-131">**NULL**</span><span class="sxs-lookup"><span data-stu-id="5d1e0-131">**NULL**</span></span>    | <span data-ttu-id="5d1e0-132">Starten Sie sofort, wenn das Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-132">Start immediately when the graph runs.</span></span> | <span data-ttu-id="5d1e0-133">Beenden Sie sofort.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-133">Stop immediately.</span></span>                  |



 

<span data-ttu-id="5d1e0-134">Mit dem folgenden Code wird der Erfassungsstream beispielsweise sofort beendet:</span><span class="sxs-lookup"><span data-stu-id="5d1e0-134">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="5d1e0-135">Sie können den Erfassungsstream zwar beenden und später neu starten, dies führt jedoch zu einer Lücke in den Zeitstempeln.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-135">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="5d1e0-136">Bei der Wiedergabe wird das Video während der Lücke angehalten (je nach Dateiformat).</span><span class="sxs-lookup"><span data-stu-id="5d1e0-136">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="5d1e0-137">Steuern des Vorschaudatenstroms</span><span class="sxs-lookup"><span data-stu-id="5d1e0-137">Controlling the Preview Stream</span></span>

<span data-ttu-id="5d1e0-138">Um den Vorschaupin zu steuern, rufen **Sie ControlStream** auf, legen aber den ersten Parameter auf PIN \_ CATEGORY PREVIEW \_ fest.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-138">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="5d1e0-139">Dies funktioniert genauso wie bei PIN \_ CATEGORY \_ CAPTURE, mit der Ausnahme, dass Sie keine Verweiszeiten verwenden können, um start und stop anzugeben, da die Vorschauframes keine Zeitstempel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-139">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="5d1e0-140">Daher müssen Sie **NULL** oder MAXLONGLONG verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-140">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="5d1e0-141">Verwenden Sie **NULL,** um den Vorschaustream zu starten:</span><span class="sxs-lookup"><span data-stu-id="5d1e0-141">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="5d1e0-142">Verwenden Sie MAXLONGLONG, um den Vorschaustream zu beenden:</span><span class="sxs-lookup"><span data-stu-id="5d1e0-142">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="5d1e0-143">Es spielt keine Rolle, ob der Vorschaudatenstrom von einem Vorschaupin im Erfassungsfilter oder vom Smart Tee-Filter stammt.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-143">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="5d1e0-144">Die **ControlStream-Methode** funktioniert auf beide Weise.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-144">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="5d1e0-145">Bei Videoport-Pins schlägt die -Methode jedoch fehl.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-145">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="5d1e0-146">In diesem Fall besteht ein anderer Ansatz darin, das Videofenster auszublenden.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-146">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="5d1e0-147">Fragen Sie das Diagramm nach **IVideoWindow** ab, und verwenden Sie die [**IVideoWindow::p ut \_ Visible-Methode,**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) um das Fenster ein- oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-147">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="5d1e0-148">Wenn Sie [**außerdem IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert OAFALSE aufrufen, bevor Sie das Diagramm ausführen, blendet der Filter Videorenderer das Fenster aus, bis Sie dies anders angeben.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-148">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="5d1e0-149">Standardmäßig zeigt der Videorenderer das Fenster an, wenn Sie das Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-149">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="5d1e0-150">Hinweise zum Stream-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5d1e0-150">Remarks about Stream Control</span></span>

<span data-ttu-id="5d1e0-151">Das Standardverhalten für eine Stecknadel ist die Bereitstellung von Beispielen, wenn das Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-151">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="5d1e0-152">Angenommen, Sie rufen **ControlStream** mit PIN \_ CATEGORY \_ CAPTURE, aber nicht mit PIN \_ CATEGORY \_ PREVIEW auf.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-152">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="5d1e0-153">Wenn Sie das Diagramm ausführen, wird der Vorschaustream sofort ausgeführt, während der Erfassungsstream zu einem beliebigen Zeitpunkt ausgeführt wird, den Sie in **ControlStream** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-153">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="5d1e0-154">Wenn Sie mehrere Streams erfassen und an einen Mux-Filter senden , z. B. wenn Sie Audio- und Videodaten in einer AVI-Datei erfassen, sollten Sie beide Streams zusammen steuern.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-154">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="5d1e0-155">Andernfalls kann der mux-Filter das Warten auf einen Stream blockieren, da er versucht, die beiden Streams zu verschachteln.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-155">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="5d1e0-156">Legen Sie die gleichen Start- und Stoppzeiten für alle Erfassungsstreams fest, bevor Sie den Graphen ausführen:</span><span class="sxs-lookup"><span data-stu-id="5d1e0-156">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="5d1e0-157">Intern verwendet die **ControlStream-Methode** die [**IAMStreamControl-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) die an den Pins des Erfassungsfilters verfügbar gemacht wird, den Smart Tee-Filter (falls vorhanden) und möglicherweise den Mux-Filter.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-157">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="5d1e0-158">Sie können diese Schnittstelle direkt verwenden, anstatt **ControlStream** aufzurufen, obwohl dies keinen besonderen Vorteil bietet.</span><span class="sxs-lookup"><span data-stu-id="5d1e0-158">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d1e0-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d1e0-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d1e0-160">Videoaufnahme</span><span class="sxs-lookup"><span data-stu-id="5d1e0-160">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



