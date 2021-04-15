---
description: Steuern eines Aufzeichnungs Diagramms
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Steuern eines Aufzeichnungs Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6366645f14822a770b828e59b2201e378a0e1e8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522032"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="ea86c-103">Steuern eines Aufzeichnungs Diagramms</span><span class="sxs-lookup"><span data-stu-id="ea86c-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="ea86c-104">Die [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Schnittstelle des Filter Graph-Managers verfügt über Methoden zum Ausführen, beenden und Anhalten des gesamten Diagramms.</span><span class="sxs-lookup"><span data-stu-id="ea86c-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="ea86c-105">Wenn das Filter Diagramm jedoch Erfassungs-und Vorschau Datenströme enthält, sollten Sie die beiden Streams wahrscheinlich unabhängig voneinander steuern.</span><span class="sxs-lookup"><span data-stu-id="ea86c-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="ea86c-106">Beispielsweise können Sie eine Vorschau des Videos anzeigen, ohne es zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="ea86c-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="ea86c-107">Hierfür können Sie die [**ICaptureGraphBuilder2:: controlstream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea86c-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="ea86c-108">Diese Methode funktioniert nicht, wenn Sie in einer ASF-Datei (Advanced Systems Format) erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="ea86c-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="ea86c-109">Steuern des Erfassungsdaten Stroms</span><span class="sxs-lookup"><span data-stu-id="ea86c-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="ea86c-110">Mit dem folgenden Code wird der Video Erfassungsdaten Strom so festgelegt, dass er vier Sekunden lang ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="ea86c-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


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



<span data-ttu-id="ea86c-111">Der erste Parameter gibt an, welcher Stream als PIN-Kategorie-GUID zu steuern ist.</span><span class="sxs-lookup"><span data-stu-id="ea86c-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="ea86c-112">Der zweite Parameter gibt den Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="ea86c-112">The second parameter gives the media type.</span></span> <span data-ttu-id="ea86c-113">Der dritte Parameter ist ein Zeiger auf den Erfassungs Filter.</span><span class="sxs-lookup"><span data-stu-id="ea86c-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="ea86c-114">Legen Sie den zweiten und den dritten Parameter auf **null** fest, um alle Aufzeichnungsdaten Ströme im Diagramm zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ea86c-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="ea86c-115">Die folgenden beiden Parameter definieren die Zeiten, zu denen der Stream gestartet und beendet wird, relativ zu dem Zeitpunkt, zu dem die Ausführung des Diagramms beginnt.</span><span class="sxs-lookup"><span data-stu-id="ea86c-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="ea86c-116">Nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , um das Diagramm auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ea86c-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="ea86c-117">Die **controlstream** -Methode hat keine Auswirkungen, bis Sie das Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea86c-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="ea86c-118">Wenn das Diagramm bereits ausgeführt wird, werden die Einstellungen sofort wirksam.</span><span class="sxs-lookup"><span data-stu-id="ea86c-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="ea86c-119">Die letzten beiden Parameter werden zum erhalten von Ereignis Benachrichtigungen verwendet, wenn der Stream gestartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea86c-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="ea86c-120">Für jeden Datenstrom, den Sie mit dieser Methode steuern, sendet das Filter Diagramm ein Ereignispaar: das [**EC- \_ \_ streamsteuerelement \_**](ec-stream-control-started.md) wurde beim Start des Streams gestartet, und das EC-Stream-Steuerelement wurde [**\_ \_ \_ beendet**](ec-stream-control-stopped.md) , wenn der Stream beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea86c-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="ea86c-121">Die Werte von **wstartcookie** und **wstopcookie** werden als zweiter Ereignis Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea86c-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="ea86c-122">Daher ist *lParam2* im Start Ereignis mit **wstartcookie identisch**, und *lParam2* im Stop-Ereignis entspricht **wstopcookie**.</span><span class="sxs-lookup"><span data-stu-id="ea86c-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="ea86c-123">Der folgende Code zeigt, wie diese Ereignisse angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="ea86c-123">The following code shows how to get these events:</span></span>


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



<span data-ttu-id="ea86c-124">Die **controlstream** -Methode definiert einige besondere Werte für Start-und Endzeit.</span><span class="sxs-lookup"><span data-stu-id="ea86c-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



|             |                                        |                                    |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="ea86c-125">Start</span><span class="sxs-lookup"><span data-stu-id="ea86c-125">Start</span></span>                                  | <span data-ttu-id="ea86c-126">Stop</span><span class="sxs-lookup"><span data-stu-id="ea86c-126">Stop</span></span>                               |
| <span data-ttu-id="ea86c-127">Maxlonglong</span><span class="sxs-lookup"><span data-stu-id="ea86c-127">MAXLONGLONG</span></span> | <span data-ttu-id="ea86c-128">Starten Sie diesen Stream nie.</span><span class="sxs-lookup"><span data-stu-id="ea86c-128">Never start this stream.</span></span>               | <span data-ttu-id="ea86c-129">Beenden Sie nicht, bis das Diagramm angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="ea86c-129">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="ea86c-130">**NULL**</span><span class="sxs-lookup"><span data-stu-id="ea86c-130">**NULL**</span></span>    | <span data-ttu-id="ea86c-131">Sofort starten, wenn das Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea86c-131">Start immediately when the graph runs.</span></span> | <span data-ttu-id="ea86c-132">Sofort beendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea86c-132">Stop immediately.</span></span>                  |



 

<span data-ttu-id="ea86c-133">Mit dem folgenden Code wird der Aufzeichnungsdaten Strom beispielsweise sofort beendet:</span><span class="sxs-lookup"><span data-stu-id="ea86c-133">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="ea86c-134">Obwohl Sie den Erfassungsdaten Strom abbrechen und später neu starten können, wird dadurch eine Lücke in den Zeitstempeln erzeugt.</span><span class="sxs-lookup"><span data-stu-id="ea86c-134">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="ea86c-135">Bei der Wiedergabe erscheint das Video während der Lücke (abhängig vom Dateiformat).</span><span class="sxs-lookup"><span data-stu-id="ea86c-135">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="ea86c-136">Steuern des Vorschau Datenstroms</span><span class="sxs-lookup"><span data-stu-id="ea86c-136">Controlling the Preview Stream</span></span>

<span data-ttu-id="ea86c-137">Um die Vorschau-PIN zu steuern, wenden Sie **controlstream** an, und legen Sie den ersten Parameter auf Pin \_ Category \_ Preview fest.</span><span class="sxs-lookup"><span data-stu-id="ea86c-137">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="ea86c-138">Dies funktioniert genauso wie bei der \_ Erfassung der PIN-Kategorie \_ , mit dem Unterschied, dass Sie keine Verweis Zeiten zum Angeben des Starts und Stopps verwenden können, da die Vorschau Rahmen keine Zeitstempel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ea86c-138">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="ea86c-139">Daher muss **null** oder maxlonglong verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea86c-139">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="ea86c-140">Verwenden Sie **null** , um den Vorschau Datenstrom zu starten:</span><span class="sxs-lookup"><span data-stu-id="ea86c-140">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="ea86c-141">Verwenden Sie maxlonglong, um den Vorschau Datenstrom anzuhalten:</span><span class="sxs-lookup"><span data-stu-id="ea86c-141">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="ea86c-142">Es spielt keine Rolle, ob der Vorschau Datenstrom aus einer Vorschau-PIN im Erfassungs Filter oder aus dem Smart Tee-Filter stammt.</span><span class="sxs-lookup"><span data-stu-id="ea86c-142">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="ea86c-143">Die **controlstream** -Methode funktioniert in jedem Fall.</span><span class="sxs-lookup"><span data-stu-id="ea86c-143">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="ea86c-144">Bei Video Port Pins schlägt die Methode jedoch fehl.</span><span class="sxs-lookup"><span data-stu-id="ea86c-144">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="ea86c-145">In diesem Fall besteht ein anderer Ansatz darin, das Videofenster auszublenden.</span><span class="sxs-lookup"><span data-stu-id="ea86c-145">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="ea86c-146">Fragen Sie das Diagramm nach **IVideoWindow** ab, und verwenden Sie die [**\_ sichtbare IVideoWindow::p UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) -Methode, um das Fenster anzuzeigen oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="ea86c-146">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


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



<span data-ttu-id="ea86c-147">Wenn Sie [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert oafalse vor dem Ausführen des Diagramms aufgerufen haben, blendet der Videorenderer-Filter das Fenster aus, bis Sie andernfalls angeben.</span><span class="sxs-lookup"><span data-stu-id="ea86c-147">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="ea86c-148">Standardmäßig zeigt der Videorenderer das Fenster an, wenn Sie das Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea86c-148">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="ea86c-149">Hinweise zur Datenstrom Steuerung</span><span class="sxs-lookup"><span data-stu-id="ea86c-149">Remarks about Stream Control</span></span>

<span data-ttu-id="ea86c-150">Das Standardverhalten für eine PIN besteht darin, bei der Ausführung des Diagramms Beispiele zu liefern.</span><span class="sxs-lookup"><span data-stu-id="ea86c-150">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="ea86c-151">Nehmen Sie beispielsweise an, dass Sie **controlstream** mit PIN \_ Category Capture, \_ aber nicht mit der Vorschau der PIN-Kategorie aufgerufen haben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ea86c-151">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="ea86c-152">Wenn Sie das Diagramm ausführen, wird der vorschaustream sofort ausgeführt, während der Erfassungsdaten Strom zu jedem Zeitpunkt ausgeführt wird, den Sie in **controlstream** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="ea86c-152">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="ea86c-153">Wenn Sie mehr als einen Stream erfassen und an einen MUX-Filter senden – wenn Sie z. b. Audiodaten und Videos in einer AVI-Datei erfassen – sollten Sie beide Streams zusammen steuern.</span><span class="sxs-lookup"><span data-stu-id="ea86c-153">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="ea86c-154">Andernfalls blockiert der Mux-Filter möglicherweise das warten auf einen Stream, da er versucht, die beiden Streams zu überdenken.</span><span class="sxs-lookup"><span data-stu-id="ea86c-154">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="ea86c-155">Legen Sie vor dem Ausführen des Diagramms die gleichen Start-und Endzeiten für alle Erfassungsdaten Ströme fest:</span><span class="sxs-lookup"><span data-stu-id="ea86c-155">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="ea86c-156">Intern verwendet die **controlstream** -Methode die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle, die auf den Pins des Erfassungs Filters verfügbar ist, den intelligenten Tee-Filter (falls vorhanden) und ggf. den MUX-Filter.</span><span class="sxs-lookup"><span data-stu-id="ea86c-156">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="ea86c-157">Sie können diese Schnittstelle direkt verwenden, anstatt **controlstream** aufrufen zu müssen, obwohl es keinen besonderen Vorteil gibt.</span><span class="sxs-lookup"><span data-stu-id="ea86c-157">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea86c-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea86c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea86c-159">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="ea86c-159">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



