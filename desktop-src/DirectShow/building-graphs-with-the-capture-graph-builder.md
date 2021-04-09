---
description: Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860472"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a><span data-ttu-id="26b16-103">Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator</span><span class="sxs-lookup"><span data-stu-id="26b16-103">Building Graphs with the Capture Graph Builder</span></span>

<span data-ttu-id="26b16-104">Trotz des Namens ist der Erfassungs Diagramm-Generator nützlich zum Erstellen vieler Arten von benutzerdefinierten Filter Diagrammen, nicht nur zum Erfassen von Diagrammen.</span><span class="sxs-lookup"><span data-stu-id="26b16-104">Despite its name, the Capture Graph Builder is useful for building many kinds of custom filter graphs, not only capture graphs.</span></span> <span data-ttu-id="26b16-105">Dieser Artikel bietet einen kurzen Überblick über die Verwendung dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="26b16-105">This article provides a brief overview of how to use this object.</span></span>

<span data-ttu-id="26b16-106">Der Erfassungs Diagramm-Generator macht die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26b16-106">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="26b16-107">Beginnen Sie, indem Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um den Erfassungs Diagramm-Generator und den Filter Graph-Manager zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="26b16-107">Start by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="26b16-108">Initialisieren Sie dann den Erfassungs Diagramm-Generator, indem Sie [**ICaptureGraphBuilder2:: setfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) mit einem Zeiger auf den Filter Graph-Manager wie folgt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="26b16-108">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager, as follows:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a><span data-ttu-id="26b16-109">Verbinden von Filtern</span><span class="sxs-lookup"><span data-stu-id="26b16-109">Connecting Filters</span></span>

<span data-ttu-id="26b16-110">Mit der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode werden zwei oder drei Filter in einer Kette miteinander verbunden.</span><span class="sxs-lookup"><span data-stu-id="26b16-110">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method connects two or three filters together in a chain.</span></span> <span data-ttu-id="26b16-111">Im Allgemeinen funktioniert die-Methode am besten, wenn jeder Filter nicht mehr als eine Eingabe-PIN oder eine Ausgabe-PIN desselben Typs aufweist.</span><span class="sxs-lookup"><span data-stu-id="26b16-111">Generally, the method works best when each filter has no more than one input pin or output pin of the same type.</span></span> <span data-ttu-id="26b16-112">In dieser Diskussion werden zunächst die ersten beiden Parameter von **RenderStream** ignoriert und die letzten drei Parameter fokussiert.</span><span class="sxs-lookup"><span data-stu-id="26b16-112">This discussion begins by ignoring the first two parameters of **RenderStream** and focusing on the last three parameters.</span></span> <span data-ttu-id="26b16-113">Der dritte Parameter ist ein [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger, der entweder einen Filter (als [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstellen Zeiger) oder eine Ausgabe-PIN (als [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen Zeiger) angeben kann.</span><span class="sxs-lookup"><span data-stu-id="26b16-113">The third parameter is an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer, which can specify either a filter (as an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointer) or an output pin (as an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointer).</span></span> <span data-ttu-id="26b16-114">Der vierte und fünfte Parameter geben **ibasefilter** -Zeiger an.</span><span class="sxs-lookup"><span data-stu-id="26b16-114">The fourth and fifth parameters specify **IBaseFilter** pointers.</span></span> <span data-ttu-id="26b16-115">Die **RenderStream** -Methode verbindet alle drei Filter in einer Kette.</span><span class="sxs-lookup"><span data-stu-id="26b16-115">The **RenderStream** method connects all three filters in a chain.</span></span> <span data-ttu-id="26b16-116">Nehmen wir beispielsweise an, dass *A*, *B* und *C* Filter sind.</span><span class="sxs-lookup"><span data-stu-id="26b16-116">For example, suppose that *A*, *B*, and *C* are filters.</span></span> <span data-ttu-id="26b16-117">Nehmen Sie jetzt an, dass jeder Filter genau eine Eingabe-und eine Ausgabe-PIN hat.</span><span class="sxs-lookup"><span data-stu-id="26b16-117">Assume for now that each filter has exactly one input pin and one output pin.</span></span> <span data-ttu-id="26b16-118">Der folgende-Befehl verbindet A mit b und dann b mit C:</span><span class="sxs-lookup"><span data-stu-id="26b16-118">The following call connects A to B, and then B to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

<span data-ttu-id="26b16-119">Alle Verbindungen sind "intelligent", was bedeutet, dass dem Diagramm nach Bedarf zusätzliche Filter hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="26b16-119">All connections are "intelligent," meaning that additional filters are added to the graph as needed.</span></span> <span data-ttu-id="26b16-120">Weitere Informationen finden Sie unter [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="26b16-120">For details, see [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="26b16-121">Legen Sie den Mittelwert auf **null** fest, um nur zwei Filter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="26b16-121">To connect just two filters, set the middle value to **NULL**.</span></span> <span data-ttu-id="26b16-122">Beispielsweise wird mit diesem-Befehl eine mit C verbunden:</span><span class="sxs-lookup"><span data-stu-id="26b16-122">For example, this call connects A to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

<span data-ttu-id="26b16-123">Sie können längere Ketten erstellen, indem Sie die-Methode zweimal aufrufen:</span><span class="sxs-lookup"><span data-stu-id="26b16-123">You can create longer chains by calling the method twice:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

<span data-ttu-id="26b16-124">Wenn der letzte Parameter **null** ist, sucht die Methode automatisch einen Standardrenderer.</span><span class="sxs-lookup"><span data-stu-id="26b16-124">If the last parameter is **NULL**, the method automatically locates a default renderer.</span></span> <span data-ttu-id="26b16-125">Er verwendet den [Videorenderer](video-renderer-filter.md) für Video und den [DirectSound-Renderer](directsound-renderer-filter.md) für Audio.</span><span class="sxs-lookup"><span data-stu-id="26b16-125">It uses the [Video Renderer](video-renderer-filter.md) for video and the [DirectSound Renderer](directsound-renderer-filter.md) for audio.</span></span> <span data-ttu-id="26b16-126">Bisher</span><span class="sxs-lookup"><span data-stu-id="26b16-126">Thus:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

<span data-ttu-id="26b16-127">für die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="26b16-127">is equivalent to</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

<span data-ttu-id="26b16-128">Dabei ist *R* der geeignete Renderer.</span><span class="sxs-lookup"><span data-stu-id="26b16-128">where *R* is the appropriate renderer.</span></span> <span data-ttu-id="26b16-129">Um den Filter für den Video Mischungs Renderer anstelle des Videorenderers zu verbinden, müssen Sie ihn jedoch explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="26b16-129">To connect the Video Mixing Renderer filter instead of the Video Renderer, however, you must specify it explicitly.</span></span>

<span data-ttu-id="26b16-130">Wenn Sie anstelle einer PIN einen Filter im dritten Parameter angeben, müssen Sie möglicherweise angeben, welche Ausgabepin für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26b16-130">If you specify a filter in the third parameter, rather than a pin, you may need to indicate which output pin should be used for the connection.</span></span> <span data-ttu-id="26b16-131">Dies ist der Zweck der ersten beiden Parameter der Methode.</span><span class="sxs-lookup"><span data-stu-id="26b16-131">That is the purpose of the method's first two parameters.</span></span> <span data-ttu-id="26b16-132">Der erste Parameter gilt nur für Erfassungs Filter.</span><span class="sxs-lookup"><span data-stu-id="26b16-132">The first parameter applies only to capture filters.</span></span> <span data-ttu-id="26b16-133">Gibt eine GUID an, die eine PIN-Kategorie angibt.</span><span class="sxs-lookup"><span data-stu-id="26b16-133">It specifies a GUID that indicates a pin category.</span></span> <span data-ttu-id="26b16-134">Eine umfassende Liste der Kategorien finden Sie unter [PIN-Eigenschaften Satz](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="26b16-134">For a complete list of categories, see [Pin Property Set](pin-property-set.md).</span></span> <span data-ttu-id="26b16-135">Zwei der Kategorien sind für alle Erfassungs Filter gültig:</span><span class="sxs-lookup"><span data-stu-id="26b16-135">Two of the categories are valid for all capture filters:</span></span>

-   <span data-ttu-id="26b16-136">**Erfassung der PIN- \_ Kategorie \_**</span><span class="sxs-lookup"><span data-stu-id="26b16-136">**PIN\_CATEGORY\_CAPTURE**</span></span>
-   <span data-ttu-id="26b16-137">**\_Kategorie \_ Vorschau anheften**</span><span class="sxs-lookup"><span data-stu-id="26b16-137">**PIN\_CATEGORY\_PREVIEW**</span></span>

<span data-ttu-id="26b16-138">Wenn ein Erfassungs Filter keine separaten Pins für Erfassung und Vorschau bereitstellt, fügt die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode einen [intelligenten Tee](smart-tee-filter.md) -Filter ein, der den Stream in einen Erfassungsdaten Strom und einen Vorschau Datenstrom teilt.</span><span class="sxs-lookup"><span data-stu-id="26b16-138">If a capture filter does not supply separate pins for capture and preview, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="26b16-139">Aus Sicht der Anwendung können Sie einfach alle Erfassungs Filter als separate Pins behandeln und die zugrunde liegende Topologie des Diagramms ignorieren.</span><span class="sxs-lookup"><span data-stu-id="26b16-139">From the application's standpoint, you can simply treat all capture filters as having separate pins and ignore the underlying topology of the graph.</span></span>

<span data-ttu-id="26b16-140">Verbinden Sie für die Datei Erfassung den Erfassungs-PIN mit einem MUX-Filter.</span><span class="sxs-lookup"><span data-stu-id="26b16-140">For file capture, connect the capture pin to a mux filter.</span></span> <span data-ttu-id="26b16-141">Verbinden Sie für die Live Vorschau die Vorschau-PIN mit einem Renderer.</span><span class="sxs-lookup"><span data-stu-id="26b16-141">For live preview, connect the preview pin to a renderer.</span></span> <span data-ttu-id="26b16-142">Wenn Sie die beiden Kategorien umschalten, kann das Diagramm während der Datei Erfassung eine übermäßige Anzahl von Frames löschen. Wenn das Diagramm jedoch ordnungsgemäß verbunden ist, werden die Vorschau Rahmen nach Bedarf gelöscht, um den Durchsatz für den Aufzeichnungsdaten Strom aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="26b16-142">If you switch the two categories, the graph might drop an excessive number of frames during the file capture; but if the graph is connected properly, it drops preview frames as needed in order to maintain throughput on the capture stream.</span></span>

<span data-ttu-id="26b16-143">Im folgenden Beispiel wird gezeigt, wie beide Streams verbunden werden:</span><span class="sxs-lookup"><span data-stu-id="26b16-143">The following example shows how to connect both streams:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="26b16-144">Einige Erfassungs Filter unterstützen auch Untertitel, die durch die **Pin- \_ Kategorie \_ VBI** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26b16-144">Some capture filters also support closed captions, indicated by **PIN\_CATEGORY\_VBI**.</span></span> <span data-ttu-id="26b16-145">Um die Untertitel in einer Datei zu erfassen, müssen Sie diese Kategorie in den MUX-Filter Rendering.</span><span class="sxs-lookup"><span data-stu-id="26b16-145">To capture the closed captions to a file, render this category to the mux filter.</span></span> <span data-ttu-id="26b16-146">Um die Untertitel in Ihrem Vorschaufenster anzuzeigen, stellen Sie eine Verbindung mit dem Renderer her:</span><span class="sxs-lookup"><span data-stu-id="26b16-146">To view the closed captions in your preview window, connect to the renderer:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="26b16-147">Der zweite Parameter für [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifiziert den Medientyp und ist in der Regel einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="26b16-147">The second parameter to [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifies the media type, and is typically one of the following:</span></span>

-   <span data-ttu-id="26b16-148">MediaType \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="26b16-148">MEDIATYPE\_Audio</span></span>
-   <span data-ttu-id="26b16-149">MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="26b16-149">MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="26b16-150">Überlappende MediaType \_ (DV)</span><span class="sxs-lookup"><span data-stu-id="26b16-150">MEDIATYPE\_Interleaved (DV)</span></span>

<span data-ttu-id="26b16-151">Sie können diesen Parameter immer dann verwenden, wenn die Ausgabe Pins des Filters die Enumeration bevorzugter Medientypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="26b16-151">You can use this parameter whenever the filter's output pins support the enumeration of preferred media types.</span></span> <span data-ttu-id="26b16-152">Bei Datei Quellen fügt der Erfassungs Diagramm-Generator bei Bedarf automatisch einen Parserfilter hinzu und fragt dann die Medientypen auf dem Parser ab.</span><span class="sxs-lookup"><span data-stu-id="26b16-152">For file sources, the Capture Graph Builder automatically adds a parser filter if needed, and then queries the media types on the parser.</span></span> <span data-ttu-id="26b16-153">(Ein Beispiel finden Sie unter [Erneutes Komprimieren einer AVI-Datei](recompressing-an-avi-file.md).) Wenn der letzte Filter in der Kette über mehrere Eingabe Pins verfügt, versucht die-Methode, ihre Medientypen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="26b16-153">(For an example, see [Recompressing an AVI File](recompressing-an-avi-file.md).) Also, if the last filter in the chain has several input pins, the method attempts to enumerate their media types.</span></span> <span data-ttu-id="26b16-154">Diese Funktionalität wird jedoch nicht von allen Filtern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26b16-154">However, not all filters support this functionality.</span></span>

## <a name="finding-interfaces-on-filters-and-pins"></a><span data-ttu-id="26b16-155">Suchen nach Schnittstellen für Filter und Pins</span><span class="sxs-lookup"><span data-stu-id="26b16-155">Finding Interfaces on Filters and Pins</span></span>

<span data-ttu-id="26b16-156">Nachdem Sie ein Diagramm erstellt haben, müssen Sie in der Regel verschiedene Schnittstellen suchen, die von Filtern und Pins im Diagramm verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="26b16-156">After you build a graph, you will typically need to locate various interfaces exposed by filters and pins in the graph.</span></span> <span data-ttu-id="26b16-157">Ein Erfassungs Filter kann z. b. die [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) -Schnittstelle verfügbar machen, während die Ausgabe Pins des Filters die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle verfügbar machen können.</span><span class="sxs-lookup"><span data-stu-id="26b16-157">For example, a capture filter might expose the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface, while the filter's output pins might expose the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span>

<span data-ttu-id="26b16-158">Die einfachste Möglichkeit, eine Schnittstelle zu finden, ist die Verwendung der [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode.</span><span class="sxs-lookup"><span data-stu-id="26b16-158">The simplest way to find an interface is to use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method.</span></span> <span data-ttu-id="26b16-159">Diese Methode durchläuft das Diagramm (Filter und Pins), bis die gewünschte Schnittstelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="26b16-159">This method walks the graph (filters and pins) until it locates the desired interface.</span></span> <span data-ttu-id="26b16-160">Sie können den Startpunkt für die Suche angeben, und Sie können die Suche auf Filter auf Upstream oder downstreamwerte vom Startpunkt beschränken.</span><span class="sxs-lookup"><span data-stu-id="26b16-160">You can specify the starting point for the search, and you can limit the search to filters upstream or downstream from the starting point.</span></span>

<span data-ttu-id="26b16-161">Im folgenden Beispiel wird die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle in einer Video Vorschau-Pin gesucht:</span><span class="sxs-lookup"><span data-stu-id="26b16-161">The following example searches for the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on a video preview pin:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> <span data-ttu-id="26b16-162">Das Thema [Suchen einer Schnittstelle in einem Filter oder einer PIN](find-an-interface-on-a-filter-or-pin.md) zeigt einen alternativen Ansatz, der anstelle von [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="26b16-162">The topic [Find an Interface on a Filter or Pin](find-an-interface-on-a-filter-or-pin.md) shows an alternative approach that uses the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface instead of [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span></span> <span data-ttu-id="26b16-163">Welche Vorgehensweise verwendet werden soll, hängt von Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="26b16-163">Which approach to use depends on your application.</span></span> <span data-ttu-id="26b16-164">Wenn Ihre Anwendung bereits **ICaptureGraphBuilder2** zum Erstellen des Diagramms verwendet, ist [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) ein guter Ansatz.</span><span class="sxs-lookup"><span data-stu-id="26b16-164">If your application already uses **ICaptureGraphBuilder2** to build the graph, then [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) is a good approach.</span></span> <span data-ttu-id="26b16-165">Andernfalls sollten Sie die **igraphbuilder** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="26b16-165">Otherwise, consider using the **IGraphBuilder** methods.</span></span>

 

## <a name="finding-pins"></a><span data-ttu-id="26b16-166">Suchen von Pins</span><span class="sxs-lookup"><span data-stu-id="26b16-166">Finding Pins</span></span>

<span data-ttu-id="26b16-167">In den meisten Fällen müssen Sie möglicherweise eine einzelne PIN für einen Filter finden, obwohl die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -und [**findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methoden in den meisten Fällen Ihnen die Probleme ersparen.</span><span class="sxs-lookup"><span data-stu-id="26b16-167">Less commonly, you may need to locate an individual pin on a filter, although in most cases the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) and [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) methods will save you the trouble.</span></span> <span data-ttu-id="26b16-168">Wenn Sie eine bestimmte PIN für einen Filter finden müssen, ist die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Hilfsmethode nützlich.</span><span class="sxs-lookup"><span data-stu-id="26b16-168">If you do need to find a particular pin on a filter, the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper method is useful.</span></span> <span data-ttu-id="26b16-169">Geben Sie die Kategorie, den Medientyp (Video oder Audiodatei) und die Richtung an, und geben Sie an, ob die PIN nicht verbunden sein muss.</span><span class="sxs-lookup"><span data-stu-id="26b16-169">Specify the category, the media type (video or audio), the direction, and whether the pin must be unconnected.</span></span>

<span data-ttu-id="26b16-170">Der folgende Code sucht z. b. nach einer nicht verbundenen Video Vorschau-PIN für einen Erfassungs Filter:</span><span class="sxs-lookup"><span data-stu-id="26b16-170">For example, the following code searches for an unconnected video preview pin on a capture filter:</span></span>


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="26b16-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26b16-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26b16-172">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="26b16-172">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
