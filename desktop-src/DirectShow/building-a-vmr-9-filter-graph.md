---
description: Aufbauen eines VMR-9-Filter Diagramms
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Aufbauen eines VMR-9-Filter Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860391"
---
# <a name="building-a-vmr-9-filter-graph"></a><span data-ttu-id="02846-103">Aufbauen eines VMR-9-Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="02846-103">Building a VMR-9 Filter Graph</span></span>

<span data-ttu-id="02846-104">Da der Video Mischungs-Renderer 9-Filter (VMR-9) nicht der Standardvideorenderer ist, muss eine Anwendung, die VMR-9 verwendet, Sie explizit dem Diagramm hinzufügen und eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="02846-104">Because the Video Mixing Renderer 9 Filter (VMR-9) is not the default video renderer, an application that uses the VMR-9 must explicitly add it to the graph and connect it.</span></span> <span data-ttu-id="02846-105">In diesem Abschnitt werden zwei unterschiedliche Ansätze zum Entwickeln von Filter Diagrammen mit VMR-9 vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="02846-105">This section presents two different approaches to building filter graphs with the VMR-9.</span></span>

<span data-ttu-id="02846-106">Verwenden des Erfassungs Diagramm-Generators</span><span class="sxs-lookup"><span data-stu-id="02846-106">Using the Capture Graph Builder</span></span>

<span data-ttu-id="02846-107">Der Erfassungs Diagramm-Generator ist ein Hilfsobjekt zum Erstellen von benutzerdefinierten Filter Diagrammen.</span><span class="sxs-lookup"><span data-stu-id="02846-107">The Capture Graph Builder is a helper object for building custom filter graphs.</span></span> <span data-ttu-id="02846-108">Sie können es verwenden, um VMR-9-Diagramme wie folgt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="02846-108">You can use it to build VMR-9 graphs as follows:</span></span>

1.  <span data-ttu-id="02846-109">Erstellen und initialisieren Sie den Erfassungs Diagramm-Generator, wie im Thema [über den Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.</span><span class="sxs-lookup"><span data-stu-id="02846-109">Create and initialize the Capture Graph Builder, as described in the topic [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
2.  <span data-ttu-id="02846-110">Rufen Sie cokreateinstance auf, um VMR-9 zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="02846-110">Call CoCreateInstance to create the VMR-9:</span></span>
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  <span data-ttu-id="02846-111">Nennen Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) im Filter Graph-Manager, um VMR-9 dem Filter Diagramm hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="02846-111">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) on the Filter Graph Manager to add the VMR-9 to the filter graph:</span></span>
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  <span data-ttu-id="02846-112">Aufrufen von [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) zum Hinzufügen eines Quell Filters für die Videodatei:</span><span class="sxs-lookup"><span data-stu-id="02846-112">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the video file:</span></span>
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  <span data-ttu-id="02846-113">Nennen Sie die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode, um den Videostream für den VMR zu rendern:</span><span class="sxs-lookup"><span data-stu-id="02846-113">Call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to render the video stream to the VMR:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  <span data-ttu-id="02846-114">Optional können Sie RenderStream erneut aufzurufen, um den Audiostream zu rendern:</span><span class="sxs-lookup"><span data-stu-id="02846-114">Optionally, call RenderStream again to render the audio stream:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

<span data-ttu-id="02846-115">Sie können mehrere Videostreams durch Aufrufen von addsourcefilter und RenderStream für jede Quelldatei mischen.</span><span class="sxs-lookup"><span data-stu-id="02846-115">You can mix several video streams by calling AddSourceFilter and RenderStream for each source file.</span></span>

<span data-ttu-id="02846-116">Verwenden des Filter Graph-Managers</span><span class="sxs-lookup"><span data-stu-id="02846-116">Using the Filter Graph Manager</span></span>

<span data-ttu-id="02846-117">Wenn Sie den Erfassungs Diagramm-Generator nicht verwenden möchten, können Sie wie folgt ein VMR-9-Diagramm erstellen, indem Sie einfach die Methoden im Diagramm-Manager des Filters verwenden:</span><span class="sxs-lookup"><span data-stu-id="02846-117">If you prefer not to use the Capture Graph Builder, you can build a VMR-9 graph simply using methods on the Filter Graph Manager, as follows:</span></span>

1.  <span data-ttu-id="02846-118">Erstellen Sie VMR-9, und fügen Sie es dem Diagramm hinzu, wie im vorherigen Verfahren gezeigt.</span><span class="sxs-lookup"><span data-stu-id="02846-118">Create the VMR-9 and add it to the graph, as shown in the previous procedure.</span></span>
2.  <span data-ttu-id="02846-119">Verwenden Sie addsourcefilter, um einen Quell Filter für die Videodatei hinzuzufügen, wie im vorherigen Verfahren gezeigt.</span><span class="sxs-lookup"><span data-stu-id="02846-119">Use AddSourceFilter to add a source filter for the video file, as shown in the previous procedure.</span></span>
3.  <span data-ttu-id="02846-120">Wenn Sie die Audiodatei Renren möchten, erstellen Sie eine Instanz des [DirectSound](directsound-renderer-filter.md) -rendererfilters, und fügen Sie Sie dem Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="02846-120">If you want to render the audio, create an instance of the [DirectSound Renderer](directsound-renderer-filter.md) filter and add it to the filter graph.</span></span>
4.  <span data-ttu-id="02846-121">Verwenden Sie die ibasefilter:: enumpins-Methode, um eine Ausgabe-PIN für den Quell Filter zu suchen.</span><span class="sxs-lookup"><span data-stu-id="02846-121">Use the IBaseFilter::EnumPins method to find an output pin on the source filter.</span></span> <span data-ttu-id="02846-122">Weitere Informationen finden Sie unter Auflisten von [Pins](enumerating-pins.md) .</span><span class="sxs-lookup"><span data-stu-id="02846-122">See [Enumerating Pins](enumerating-pins.md) for details.</span></span>
5.  <span data-ttu-id="02846-123">Fragen Sie den Filter Graph-Manager nach der IFilterGraph2-Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="02846-123">Query the Filter Graph Manager for the IFilterGraph2 interface.</span></span>
6.  <span data-ttu-id="02846-124">Aufrufen von [**IFilterGraph2:: renderex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) mit dem "am \_ renderex \_ renderonexistingrenderzer"-Flag.</span><span class="sxs-lookup"><span data-stu-id="02846-124">Call [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) with the AM\_RENDEREX\_RENDERTOEXISTINGRENDERERS flag.</span></span> <span data-ttu-id="02846-125">Dieser Aufruf rendert die Ausgabe-PIN, wobei nur die rendererfilter verwendet werden, die bereits im Diagramm vorhanden sind – in diesem Fall der VMR-9 und der DirectSound-Renderer.</span><span class="sxs-lookup"><span data-stu-id="02846-125">This call renders the output pin, using only the renderer filters already in the graph — in this case, the VMR-9 and the DirectSound Renderer.</span></span> <span data-ttu-id="02846-126">Dadurch wird verhindert, dass die intelligente Verbindungs Logik dem Diagramm den Standardvideorenderer hinzufügt, sodass die VMR-9 nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="02846-126">This prevents the Intelligent Connect logic from adding the default video renderer to the graph, which would leave the VMR-9 unconnected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02846-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02846-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02846-128">Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator</span><span class="sxs-lookup"><span data-stu-id="02846-128">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



