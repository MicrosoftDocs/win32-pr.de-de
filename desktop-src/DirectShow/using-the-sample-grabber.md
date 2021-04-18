---
description: Der Beispiel-Grabber Filter ist ein Transformations Filter, der zum Erfassen von Medien Beispielen aus einem Stream verwendet werden kann, während diese das Filter Diagramm durchlaufen.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Verwenden der Beispiel-Grabber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357877"
---
# <a name="using-the-sample-grabber"></a><span data-ttu-id="a1bd0-103">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="a1bd0-103">Using the Sample Grabber</span></span>

<span data-ttu-id="a1bd0-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="a1bd0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a1bd0-105">Der [**Beispiel-Grabber**](sample-grabber-filter.md) Filter ist ein Transformations Filter, der zum Erfassen von Medien Beispielen aus einem Stream verwendet werden kann, während diese das Filter Diagramm durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-105">The [**Sample Grabber**](sample-grabber-filter.md) filter is a transform filter that can be used to grab media samples from a stream as they pass through the filter graph.</span></span>

<span data-ttu-id="a1bd0-106">Wenn Sie einfach eine Bitmap aus einer Videodatei erfassen möchten, ist es einfacher, das [Media Detector-Objekt (mediadet)](media-detector--mediadet.md) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-106">If you simply want to grab a bitmap from a video file, it is easier to use the [Media Detector (MediaDet)](media-detector--mediadet.md) object.</span></span> <span data-ttu-id="a1bd0-107">Ausführliche Informationen finden Sie unter [Erfassen eines Poster-Frames](grabbing-a-poster-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="a1bd0-107">See [Grabbing a Poster Frame](grabbing-a-poster-frame.md) for details.</span></span> <span data-ttu-id="a1bd0-108">Der Beispiel-Grabber ist jedoch flexibler, da er mit nahezu jedem Medientyp funktioniert (siehe [**isamplegrabber:: setmediatype**](isamplegrabber-setmediatype.md) für die wenigen Ausnahmen) und eine größere Kontrolle für die Anwendung bietet.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-108">The Sample Grabber is more flexible, however, because it works with nearly any media type (see [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) for the few exceptions), and offers more control to the application.</span></span>

-   [<span data-ttu-id="a1bd0-109">Erstellen des Filter Graph-Managers</span><span class="sxs-lookup"><span data-stu-id="a1bd0-109">Create the Filter Graph Manager</span></span>](#create-the-filter-graph-manager)
-   [<span data-ttu-id="a1bd0-110">Hinzufügen des beispielgrabsteins zum Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="a1bd0-110">Add the Sample Grabber to the Filter Graph</span></span>](#add-the-sample-grabber-to-the-filter-graph)
-   [<span data-ttu-id="a1bd0-111">Festlegen des Medientyps</span><span class="sxs-lookup"><span data-stu-id="a1bd0-111">Set the Media Type</span></span>](#set-the-media-type)
-   [<span data-ttu-id="a1bd0-112">Erstellen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="a1bd0-112">Build the Filter Graph</span></span>](#build-the-filter-graph)
-   [<span data-ttu-id="a1bd0-113">Ausführen des Diagramms</span><span class="sxs-lookup"><span data-stu-id="a1bd0-113">Run the Graph</span></span>](#run-the-graph)
-   [<span data-ttu-id="a1bd0-114">Holen Sie sich das Beispiel</span><span class="sxs-lookup"><span data-stu-id="a1bd0-114">Grab the Sample</span></span>](#grab-the-sample)
-   [<span data-ttu-id="a1bd0-115">Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="a1bd0-115">Example Code</span></span>](#example-code)
-   [<span data-ttu-id="a1bd0-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1bd0-116">Related topics</span></span>](#related-topics)

## <a name="create-the-filter-graph-manager"></a><span data-ttu-id="a1bd0-117">Erstellen des Filter Graph-Managers</span><span class="sxs-lookup"><span data-stu-id="a1bd0-117">Create the Filter Graph Manager</span></span>

<span data-ttu-id="a1bd0-118">Erstellen Sie zunächst den [Filter Graph-Manager](filter-graph-manager.md) , und Fragen Sie die Schnittstellen [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) ab.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-118">To start, create the [Filter Graph Manager](filter-graph-manager.md) and query for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a><span data-ttu-id="a1bd0-119">Hinzufügen des beispielgrabsteins zum Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="a1bd0-119">Add the Sample Grabber to the Filter Graph</span></span>

<span data-ttu-id="a1bd0-120">Erstellen Sie eine Instanz des Sample-Grabber Filters und addieren Sie zum Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-120">Create an instance of the Sample Grabber filter and addit to the filter graph.</span></span> <span data-ttu-id="a1bd0-121">Fragen Sie den beispielgrabfilter für die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-121">Query the Sample Grabber filter for the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a><span data-ttu-id="a1bd0-122">Festlegen des Medientyps</span><span class="sxs-lookup"><span data-stu-id="a1bd0-122">Set the Media Type</span></span>

<span data-ttu-id="a1bd0-123">Wenn Sie die Beispiel-Grabber erstmalig erstellen, hat Sie keinen bevorzugten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-123">When you first create the Sample Grabber, it has no preferred media type.</span></span> <span data-ttu-id="a1bd0-124">Dies bedeutet, dass Sie eine Verbindung mit fast jedem Filter im Diagramm herstellen können, aber Sie haben keine Kontrolle über die Art der empfangenen Daten.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-124">This means you can connect to almost any filter in the graph, but you would have no control over the type of data that it received.</span></span> <span data-ttu-id="a1bd0-125">Bevor Sie den Rest des Diagramms aufbauen, müssen Sie daher einen Medientyp für den beispielgrabber festlegen, indem Sie die [**isamplegrabber:: setmediatype**](isamplegrabber-setmediatype.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-125">Before building the rest of the graph, therefore, you must set a media type for the Sample Grabber, by calling the [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) method.</span></span>

<span data-ttu-id="a1bd0-126">Wenn der Sample Grabber eine Verbindung herstellt, vergleicht dieser den Medientyp mit dem Medientyp, der vom anderen Filter angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-126">When the Sample Grabber connects, it will compare this media type against the media type offered by the other filter.</span></span> <span data-ttu-id="a1bd0-127">Die einzigen Felder, die überprüft werden, sind der Haupttyp, der Untertyp und der Formattyp.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-127">The only fields that it checks are the major type, subtype, and format type.</span></span> <span data-ttu-id="a1bd0-128">Für einen dieser Werte bedeutet der Wert GUID \_ NULL, dass "beliebige Werte akzeptieren" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-128">For any of these, the value GUID\_NULL means "accept any value."</span></span> <span data-ttu-id="a1bd0-129">In den meisten Fällen möchten Sie den Haupttyp und den Untertyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-129">Most of the time, you will want to set the major type and subtype.</span></span> <span data-ttu-id="a1bd0-130">Der folgende Code gibt beispielsweise ein unkomprimiertes 24-Bit-RGB-Video an:</span><span class="sxs-lookup"><span data-stu-id="a1bd0-130">For example, the following code specifies uncompressed 24-bit RGB video:</span></span>


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a><span data-ttu-id="a1bd0-131">Erstellen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="a1bd0-131">Build the Filter Graph</span></span>

<span data-ttu-id="a1bd0-132">Nun können Sie den Rest des Filter Diagramms erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-132">Now you can build the rest of the filter graph.</span></span> <span data-ttu-id="a1bd0-133">Da der beispielgrabber nur mithilfe des von Ihnen angegebenen Medientyps eine Verbindung herstellt, können Sie die [intelligenten Verbindungs](intelligent-connect.md) Mechanismen des Filter Graph-Managers nutzen, wenn Sie das Diagramm erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-133">Because the Sample Grabber will only connect using the media type you have specified, this lets you take advantage of the Filter Graph Manager's [Intelligent Connect](intelligent-connect.md) mechanisms when you build the graph.</span></span>

<span data-ttu-id="a1bd0-134">Wenn Sie z. b. nicht komprimierte Videos angegeben haben, können Sie einen Quell Filter mit dem beispielgrabber verbinden, und der Filter Graph-Manager fügt automatisch den Datei Parser und den Decoder hinzu.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-134">For example, if you specified uncompressed video, you can connect a source filter to the Sample Grabber, and the Filter Graph Manager will automatically add the file parser and the decoder.</span></span> <span data-ttu-id="a1bd0-135">Im folgenden Beispiel wird die Hilfsfunktion connectfilters verwendet, die unter [Verbinden von zwei Filtern](connect-two-filters.md)aufgeführt ist:</span><span class="sxs-lookup"><span data-stu-id="a1bd0-135">The following example uses the ConnectFilters helper function, which is listed in [Connect Two Filters](connect-two-filters.md):</span></span>


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="a1bd0-136">Der Beispiel Grabber ist ein Transformations Filter, sodass die Ausgabe-PIN mit einem anderen Filter verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-136">The Sample Grabber is a transform filter, so the output pin must be connected to another filter.</span></span> <span data-ttu-id="a1bd0-137">Häufig möchten Sie die Beispiele auch verwerfen, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-137">Often, you may simply want to discard the samples after you are done with them.</span></span> <span data-ttu-id="a1bd0-138">Verbinden Sie in diesem Fall den Beispiel-Grabber mit dem [**Filter NULL-Renderer**](null-renderer-filter.md), der die empfangenen Daten verwirft.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-138">In that case, connect the Sample Grabber to the [**Null Renderer Filter**](null-renderer-filter.md), which discards the data that it receives.</span></span>

<span data-ttu-id="a1bd0-139">Im folgenden Beispiel wird die Beispiel-Grabber mit dem NULL-rendererfilter verbunden:</span><span class="sxs-lookup"><span data-stu-id="a1bd0-139">The following example connects the Sample Grabber to the Null Renderer filter:</span></span>


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="a1bd0-140">Beachten Sie, dass das Platzieren des Beispiel Grabsteins zwischen einem Video Decoder und dem Videorenderer die Renderingleistung erheblich beeinträchtigen kann.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-140">Be aware that placing the Sample Grabber between a video decoder and the video renderer can significantly hurt rendering performance.</span></span> <span data-ttu-id="a1bd0-141">Der Beispiel Grabber ist ein übergreifendes Filter, d. h. der Ausgabepuffer ist mit dem Eingabepuffer identisch.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-141">The Sample Grabber is a trans-in-place filter, which means the output buffer is the same as the input buffer.</span></span> <span data-ttu-id="a1bd0-142">Beim Video Rendering befindet sich der Ausgabepuffer wahrscheinlich auf der Grafikkarte, bei der Lesevorgänge im Vergleich zu Lesevorgängen im Hauptspeicher wesentlich langsamer sind.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-142">For video rendering, the output buffer is likely to be located on the graphics card, where read operations are much slower, compared with read operations in main memory.</span></span>

## <a name="run-the-graph"></a><span data-ttu-id="a1bd0-143">Ausführen des Diagramms</span><span class="sxs-lookup"><span data-stu-id="a1bd0-143">Run the Graph</span></span>

<span data-ttu-id="a1bd0-144">Der Beispiel Grabber funktioniert in einem von zwei Modi:</span><span class="sxs-lookup"><span data-stu-id="a1bd0-144">The Sample Grabber operates in one of two modes:</span></span>

-   <span data-ttu-id="a1bd0-145">Der Puffer Modus erstellt eine Kopie jeder Stichprobe, bevor das Beispiel für die downstreamausgabe bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-145">Buffering mode makes a copy of each sample before delivering the sample downstream.</span></span>
-   <span data-ttu-id="a1bd0-146">Der Rückruf Modus Ruft eine Anwendungs definierte Rückruffunktion für jedes Beispiel auf.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-146">Callback mode invokes an application-defined callback function on each sample.</span></span>

<span data-ttu-id="a1bd0-147">In diesem Artikel wird der Puffer Modus beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-147">This article describes buffering mode.</span></span> <span data-ttu-id="a1bd0-148">(Bevor Sie den Rückruf Modus verwenden, beachten Sie, dass die Rückruffunktion sehr eingeschränkt sein muss.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-148">(Before using callback mode, be aware that the callback function must be quite limited.</span></span> <span data-ttu-id="a1bd0-149">Andernfalls kann die Leistung drastisch reduziert werden, und es kann sogar zu Deadlocks führen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-149">Otherwise, it can drastically reduce performance or even cause deadlocks.</span></span> <span data-ttu-id="a1bd0-150">Weitere Informationen finden Sie unter [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md).) Um den Puffer Modus zu aktivieren, müssen Sie die [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md) -Methode mit dem Wert " **true**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-150">For more information, see [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) To activate buffering mode, call the [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) method with the value **TRUE**.</span></span>

<span data-ttu-id="a1bd0-151">Optional können Sie die [**isamplegrabber:: setoneshot**](isamplegrabber-setoneshot.md) -Methode mit dem Wert " **true**" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-151">Optionally, call the [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) method with the value **TRUE**.</span></span> <span data-ttu-id="a1bd0-152">Dies bewirkt, dass der Sample Grabber nach dem Empfang des ersten Medien Beispiels angehalten wird. Dies ist hilfreich, wenn Sie einen einzelnen Frame aus dem Stream ziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-152">This causes the Sample Grabber to halt after it receives the first media sample, which is useful if you want to grab a single frame from the stream.</span></span> <span data-ttu-id="a1bd0-153">Suchen Sie nach der gewünschten Zeit, führen Sie das Diagramm aus, und warten Sie auf das " [**EC \_ Complete**](ec-complete.md) "-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-153">Seek to the desired time, run the graph, and wait for the [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="a1bd0-154">Beachten Sie, dass die Ebene der Frame Genauigkeit von der Quelle abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-154">Note that the level of frame accuracy depends on the source.</span></span> <span data-ttu-id="a1bd0-155">Beispielsweise ist das Suchen einer MPEG-Datei oft nicht Frame genau.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-155">For example, seeking an MPEG file is often not frame accurate.</span></span>

<span data-ttu-id="a1bd0-156">Wenn Sie das Diagramm so schnell wie möglich ausführen möchten, schalten Sie die Diagramm Uhr ein, wie unter [Festlegen der Graph-Uhr](setting-the-graph-clock.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-156">To run the graph as fast as possible, turn of the graph clock as described in [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

<span data-ttu-id="a1bd0-157">Im folgenden Beispiel werden der One-Shot-Modus und der Puffer Modus aktiviert, das Filter Diagramm ausgeführt und auf den Abschluss gewartet.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-157">The following example enables one-shot mode and buffering mode, runs the filter graph, and waits for completion.</span></span>


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a><span data-ttu-id="a1bd0-158">Holen Sie sich das Beispiel</span><span class="sxs-lookup"><span data-stu-id="a1bd0-158">Grab the Sample</span></span>

<span data-ttu-id="a1bd0-159">Im Puffer Modus speichert der Beispiel Grabber eine Kopie jeder Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-159">In buffering mode, the Sample Grabber stores a copy of every sample.</span></span> <span data-ttu-id="a1bd0-160">Die Methode [**isamplegrabber:: getcurrentbuffer**](isamplegrabber-getcurrentbuffer.md) kopiert den Puffer in ein Array, das vom Aufrufer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-160">The [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method copies the buffer into a caller-allocated array.</span></span> <span data-ttu-id="a1bd0-161">Um die Größe des benötigten Arrays zu ermitteln, müssen Sie zuerst **getcurrentbuffer** mit einem **null** -Zeiger für die Array Adresse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-161">To determine the size of the array that is needed, first call **GetCurrentBuffer** with a **NULL** pointer for the array address.</span></span> <span data-ttu-id="a1bd0-162">Weisen Sie dann das Array zu, und nennen Sie die Methode ein zweites Mal, um den Puffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-162">Then allocate the array and call the method a second time to copy the buffer.</span></span> <span data-ttu-id="a1bd0-163">Das folgende Beispiel zeigt die erforderlichen Schritte:</span><span class="sxs-lookup"><span data-stu-id="a1bd0-163">The following example shows these steps.</span></span>


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="a1bd0-164">Sie müssen das genaue Format der Daten im Puffer kennen.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-164">You will need to know the exact format of the data in the buffer.</span></span> <span data-ttu-id="a1bd0-165">Um diese Informationen abzurufen, nennen Sie die [**isamplegrabber:: getconnectedmediatype**](isamplegrabber-getconnectedmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-165">To get this information, call the [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) method.</span></span> <span data-ttu-id="a1bd0-166">Diese Methode füllt eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur mit dem-Format auf.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-166">This method fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure with the format.</span></span>

<span data-ttu-id="a1bd0-167">Bei einem unkomprimierten Videostream sind die Formatinformationen in einer [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-167">For an uncompressed video stream, the format information is contained in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="a1bd0-168">Im folgenden Beispiel wird veranschaulicht, wie die Formatinformationen für einen unkomprimierten Videostream angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-168">The following example shows how to get the format information for an uncompressed video stream.</span></span>


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> <span data-ttu-id="a1bd0-169">Der Beispiel Grabber unterstützt [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)nicht.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-169">The Sample Grabber does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

 

## <a name="example-code"></a><span data-ttu-id="a1bd0-170">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="a1bd0-170">Example Code</span></span>

<span data-ttu-id="a1bd0-171">Dies ist der gesamte Code für die vorherigen Beispiele.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-171">Here is the complete code for the previous examples.</span></span>

> [!Note]  
> <span data-ttu-id="a1bd0-172">In diesem Beispiel wird die Funktion " [saferelease](../medfound/saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a1bd0-172">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="a1bd0-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1bd0-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1bd0-174">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="a1bd0-174">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
