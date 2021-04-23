---
description: Steuern eines Erfassungsdiagramms
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Steuern eines Erfassungsdiagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0089fa11adbc0ac861fb9e8e30e2cd0f56b23680
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909048"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="b5054-103">Steuern eines Erfassungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="b5054-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="b5054-104">Die [**IMediaControl-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediacontrol) des Filter graph-Managers verfügt über Methoden zum Ausführen, Beenden und Anhalten des gesamten Graphen.</span><span class="sxs-lookup"><span data-stu-id="b5054-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="b5054-105">Wenn das Filterdiagramm jedoch Erfassungs- und Vorschaustreams auflistet, möchten Sie die beiden Datenströme wahrscheinlich unabhängig voneinander steuern.</span><span class="sxs-lookup"><span data-stu-id="b5054-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="b5054-106">Sie können z. B. eine Vorschau des Videos anzeigen, ohne es zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="b5054-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="b5054-107">Hierzu können Sie die [**ICaptureGraphBuilder2::ControlStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5054-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="b5054-108">Diese Methode funktioniert nicht, wenn sie in einer ASF-Datei (Advanced Systems Format) erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="b5054-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="b5054-109">Steuern des Erfassungsstreams</span><span class="sxs-lookup"><span data-stu-id="b5054-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="b5054-110">Der folgende Code legt fest, dass der Videoaufzeichnungsstream vier Sekunden lang ausgeführt wird, beginnend eine Sekunde nach der Ausführung des Diagramms:</span><span class="sxs-lookup"><span data-stu-id="b5054-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


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



<span data-ttu-id="b5054-111">Der erste Parameter gibt an, welcher Stream als PIN-Kategorie-GUID zu steuern ist.</span><span class="sxs-lookup"><span data-stu-id="b5054-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="b5054-112">Der zweite Parameter gibt den Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="b5054-112">The second parameter gives the media type.</span></span> <span data-ttu-id="b5054-113">Der dritte Parameter ist ein Zeiger auf den Erfassungsfilter.</span><span class="sxs-lookup"><span data-stu-id="b5054-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="b5054-114">Um alle Erfassungsstreams im Diagramm zu steuern, legen Sie den zweiten und dritten Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="b5054-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="b5054-115">Die nächsten beiden Parameter definieren die Zeiten, zu denen der Stream gestartet und stoppt, relativ zur Zeit, zu der die Ausführung des Diagramms beginnt.</span><span class="sxs-lookup"><span data-stu-id="b5054-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="b5054-116">Rufen [**Sie IMediaControl::Run auf,**](/windows/desktop/api/Control/nf-control-imediacontrol-run) um den Graphen ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="b5054-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="b5054-117">Bis sie das Diagramm ausführen, hat die **ControlStream-Methode** keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="b5054-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="b5054-118">Wenn das Diagramm bereits ausgeführt wird, werden die Einstellungen sofort wirksam.</span><span class="sxs-lookup"><span data-stu-id="b5054-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="b5054-119">Die letzten beiden Parameter werden zum Abrufen von Ereignisbenachrichtigungen verwendet, wenn der Stream gestartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5054-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="b5054-120">Für jeden Stream, den Sie mit dieser Methode steuern, sendet das Filterdiagramm ein Ereignispaar: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) beim Start des Streams und [**EC STREAM CONTROL \_ \_ \_ STOPPED,**](ec-stream-control-stopped.md) wenn der Stream beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5054-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="b5054-121">Die Werte von **wStartCookie** und **wStopCookie** werden als zweiter Ereignisparameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5054-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="b5054-122">Daher entspricht *lParam2* im Startereignis **wStartCookie** und *lParam2* im Beendigungsereignis **wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="b5054-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="b5054-123">Der folgende Code zeigt, wie diese Ereignisse abzurufen sind:</span><span class="sxs-lookup"><span data-stu-id="b5054-123">The following code shows how to get these events:</span></span>


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



<span data-ttu-id="b5054-124">Die **ControlStream-Methode** definiert einige spezielle Werte für die Start- und Beendigungszeiten.</span><span class="sxs-lookup"><span data-stu-id="b5054-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="b5054-125">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="b5054-125">Label</span></span> | <span data-ttu-id="b5054-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b5054-126">Value</span></span> |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="b5054-127">Starten</span><span class="sxs-lookup"><span data-stu-id="b5054-127">Start</span></span>                                  | <span data-ttu-id="b5054-128">Beenden</span><span class="sxs-lookup"><span data-stu-id="b5054-128">Stop</span></span>                               |
| <span data-ttu-id="b5054-129">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="b5054-129">MAXLONGLONG</span></span> | <span data-ttu-id="b5054-130">Starten Sie diesen Stream nie.</span><span class="sxs-lookup"><span data-stu-id="b5054-130">Never start this stream.</span></span>               | <span data-ttu-id="b5054-131">Beenden Sie nicht, bis das Diagramm beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5054-131">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="b5054-132">**NULL**</span><span class="sxs-lookup"><span data-stu-id="b5054-132">**NULL**</span></span>    | <span data-ttu-id="b5054-133">Starten Sie sofort, wenn das Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5054-133">Start immediately when the graph runs.</span></span> | <span data-ttu-id="b5054-134">Beenden Sie sofort.</span><span class="sxs-lookup"><span data-stu-id="b5054-134">Stop immediately.</span></span>                  |



 

<span data-ttu-id="b5054-135">Der folgende Code beendet z. B. den Erfassungsstream sofort:</span><span class="sxs-lookup"><span data-stu-id="b5054-135">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b5054-136">Sie können den Erfassungsstream zwar beenden und später neu starten, dies führt jedoch zu einer Lücke in den Zeitstempeln.</span><span class="sxs-lookup"><span data-stu-id="b5054-136">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="b5054-137">Bei der Wiedergabe wird das Video während der Lücke angehalten (je nach Dateiformat).</span><span class="sxs-lookup"><span data-stu-id="b5054-137">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="b5054-138">Steuern des Vorschaudatenstroms</span><span class="sxs-lookup"><span data-stu-id="b5054-138">Controlling the Preview Stream</span></span>

<span data-ttu-id="b5054-139">Um den Vorschaupin zu steuern, rufen **Sie ControlStream** auf, legen aber den ersten Parameter auf PIN \_ CATEGORY PREVIEW \_ fest.</span><span class="sxs-lookup"><span data-stu-id="b5054-139">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="b5054-140">Dies funktioniert genauso wie bei PIN \_ CATEGORY \_ CAPTURE, mit der Ausnahme, dass Sie keine Verweiszeiten verwenden können, um start und stop anzugeben, da die Vorschauframes keine Zeitstempel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b5054-140">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="b5054-141">Daher müssen Sie **NULL** oder MAXLONGLONG verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5054-141">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="b5054-142">Verwenden Sie **NULL,** um den Vorschaustream zu starten:</span><span class="sxs-lookup"><span data-stu-id="b5054-142">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b5054-143">Verwenden Sie MAXLONGLONG, um den Vorschaustream zu beenden:</span><span class="sxs-lookup"><span data-stu-id="b5054-143">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b5054-144">Es spielt keine Rolle, ob der Vorschaudatenstrom von einem Vorschaupin im Erfassungsfilter oder vom Smart Tee-Filter stammt.</span><span class="sxs-lookup"><span data-stu-id="b5054-144">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="b5054-145">Die **ControlStream-Methode** funktioniert auf beide Weise.</span><span class="sxs-lookup"><span data-stu-id="b5054-145">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="b5054-146">Bei Videoport-Pins ist die -Methode jedoch fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="b5054-146">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="b5054-147">In diesem Fall besteht ein anderer Ansatz im Ausblenden des Videofensters.</span><span class="sxs-lookup"><span data-stu-id="b5054-147">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="b5054-148">Fragen Sie das Diagramm **nach IVideoWindow ab,** und verwenden Sie die [**IVideoWindow::p ut \_ Visible-Methode,**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) um das Fenster anzuzeigen oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="b5054-148">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


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



<span data-ttu-id="b5054-149">Wenn Sie [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert OAFALSE aufrufen, bevor Sie das Diagramm ausführen, blendet der Videorendererfilter das Fenster aus, bis Sie etwas anderes angeben.</span><span class="sxs-lookup"><span data-stu-id="b5054-149">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="b5054-150">Standardmäßig zeigt der Videorenderer das Fenster an, wenn Sie das Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5054-150">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="b5054-151">Hinweise zum Stream-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b5054-151">Remarks about Stream Control</span></span>

<span data-ttu-id="b5054-152">Das Standardverhalten für eine Stecknadel ist das Ausliefern von Stichproben, wenn der Graph ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5054-152">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="b5054-153">Angenommen, Sie rufen **ControlStream** mit PIN \_ CATEGORY \_ CAPTURE auf, aber nicht mit PIN \_ CATEGORY \_ PREVIEW.</span><span class="sxs-lookup"><span data-stu-id="b5054-153">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="b5054-154">Wenn Sie das Diagramm ausführen, wird der Vorschaustream sofort ausgeführt, während der Erfassungsstream zu dem Zeitpunkt ausgeführt wird, den Sie in **ControlStream angegeben haben.**</span><span class="sxs-lookup"><span data-stu-id="b5054-154">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="b5054-155">Wenn Sie mehr als einen Stream erfassen und an einen Muxfilter senden , z. B. wenn Sie Audio- und Videodaten in einer AVI-Datei erfassen, sollten Sie beide Streams gemeinsam steuern.</span><span class="sxs-lookup"><span data-stu-id="b5054-155">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="b5054-156">Andernfalls kann der Muxfilter das Warten auf einen Stream blockieren, da er versucht, die beiden Streams zu verweben.</span><span class="sxs-lookup"><span data-stu-id="b5054-156">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="b5054-157">Legen Sie die gleichen Start- und Stoppzeiten für alle Erfassungsstreams fest, bevor Sie den Graphen ausführen:</span><span class="sxs-lookup"><span data-stu-id="b5054-157">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="b5054-158">Intern verwendet die **ControlStream-Methode** die [**IAMStreamControl-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) die auf den Pins des Erfassungsfilters, dem Smart Tee-Filter (falls vorhanden) und möglicherweise dem Muxfilter verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="b5054-158">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="b5054-159">Sie können diese Schnittstelle direkt verwenden, anstatt **ControlStream** auf aufruft, obwohl dies keinen besonderen Vorteil bietet.</span><span class="sxs-lookup"><span data-stu-id="b5054-159">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5054-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5054-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5054-161">Videoaufnahme</span><span class="sxs-lookup"><span data-stu-id="b5054-161">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



