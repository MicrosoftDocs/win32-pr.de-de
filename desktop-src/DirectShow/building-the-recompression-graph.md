---
description: Das neukomprimierungs Diagramm wird erstellt.
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Das neukomprimierungs Diagramm wird erstellt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860035"
---
# <a name="building-the-recompression-graph"></a><span data-ttu-id="7c95b-103">Das neukomprimierungs Diagramm wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c95b-103">Building the Recompression Graph</span></span>

<span data-ttu-id="7c95b-104">Ein typisches Filter Diagramm für die Neukomprimierung von AVI-Dateien sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="7c95b-104">A typical filter graph for AVI file recompression looks like the following:</span></span>

![Diagramm der AVI-Neukomprimierung](images/avi2avi4.png)

<span data-ttu-id="7c95b-106">Der [avi-Splitter Filter](avi-splitter-filter.md) Ruft Daten aus dem [Datei Quell Filter (Async)](file-source--async--filter.md) ab und analysiert sie in Video-und Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="7c95b-106">The [AVI Splitter Filter](avi-splitter-filter.md) pulls data from the [File Source (Async) Filter](file-source--async--filter.md) and parses it into video and audio streams.</span></span> <span data-ttu-id="7c95b-107">Das Video Debug decodiert das komprimierte Video, bei dem es durch den Video-Kompressor erneut komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="7c95b-107">The video decompressor decodes the compressed video, where it is recompressed by the video compressor.</span></span> <span data-ttu-id="7c95b-108">Die Auswahl der Dekompressoren hängt von der Quelldatei ab. Sie wird automatisch von [Intelligent Connect](intelligent-connect.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7c95b-108">The choice of decompressors depends on the source file; it will be handled automatically by [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="7c95b-109">Die Anwendung muss den-Kompressor auswählen, in der Regel durch das präsentieren einer Liste für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7c95b-109">The application must choose the compressor, typically by presenting a list to the user.</span></span> <span data-ttu-id="7c95b-110">(Siehe [Auswählen eines Komprimierungs Filters](choosing-a-compression-filter.md).)</span><span class="sxs-lookup"><span data-stu-id="7c95b-110">(See [Choosing a Compression Filter](choosing-a-compression-filter.md).)</span></span>

<span data-ttu-id="7c95b-111">Das komprimierte Video wechselt dann zum [AVI MUX-Filter](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7c95b-111">The compressed video then goes to the [AVI Mux Filter](avi-mux-filter.md).</span></span> <span data-ttu-id="7c95b-112">Der Audiodatenstrom in diesem Beispiel ist nicht komprimiert und wird daher direkt vom avi-Splitter zum AVI MUX geleitet.</span><span class="sxs-lookup"><span data-stu-id="7c95b-112">The audio stream in this example is not compressed, so it goes directly from the AVI Splitter to the AVI Mux.</span></span> <span data-ttu-id="7c95b-113">Der AVI MUX lässt die beiden Streams ein, und der [dateiwriter-Filter](file-writer-filter.md) schreibt die Ausgabe auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="7c95b-113">The AVI Mux interleaves the two streams, and the [File Writer Filter](file-writer-filter.md) writes the output to disk.</span></span> <span data-ttu-id="7c95b-114">Beachten Sie, dass AVI MUX erforderlich ist, auch wenn die ursprüngliche Datei über keinen Audiodatenstrom verfügt.</span><span class="sxs-lookup"><span data-stu-id="7c95b-114">Note that the AVI Mux is required even if the original file does not have an audio stream.</span></span>

<span data-ttu-id="7c95b-115">Die einfachste Möglichkeit zum Erstellen dieses Filter Diagramms ist die Verwendung des [Erfassungs Diagramm](capture-graph-builder.md)-Generators, bei dem es sich um eine DirectShow-Komponente zum Erstellen von Erfassungs Diagrammen und anderen benutzerdefinierten Filter Diagrammen handelt.</span><span class="sxs-lookup"><span data-stu-id="7c95b-115">The easiest way to build this filter graph is to use the [Capture Graph Builder](capture-graph-builder.md), which is a DirectShow component for building capture graphs and other custom filter graphs.</span></span>

<span data-ttu-id="7c95b-116">Starten Sie, indem Sie CoCreateInstance aufrufen, um den Erfassungs Diagramm-Generator zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="7c95b-116">Start by calling CoCreateInstance to create the Capture Graph Builder:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



<span data-ttu-id="7c95b-117">Verwenden Sie dann den Erfassungs Diagramm-Generator, um das Filter Diagramm zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="7c95b-117">Then use the Capture Graph Builder to build the filter graph:</span></span>

1.  <span data-ttu-id="7c95b-118">Erstellen Sie den Renderingabschnitt des Diagramms, der den AVI MUX-Filter und den [dateiwriter](file-writer-filter.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="7c95b-118">Build the rendering section of the graph, which includes the AVI Mux filter and the [File Writer](file-writer-filter.md).</span></span>
2.  <span data-ttu-id="7c95b-119">Fügen Sie dem Diagramm den Quell Filter und den Komprimierungs Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="7c95b-119">Add the source filter and the compression filter to the graph.</span></span>
3.  <span data-ttu-id="7c95b-120">Verbinden Sie den Quell Filter mit dem MUX-Filter.</span><span class="sxs-lookup"><span data-stu-id="7c95b-120">Connect the source filter to the MUX filter.</span></span> <span data-ttu-id="7c95b-121">Der Erfassungs Diagramm-Generator fügt alle Splitter Filter ein, die zum Analysieren der Quelldatei erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7c95b-121">The capture graph builder inserts whatever splitter and decoder filters are needed to parse the source file.</span></span> <span data-ttu-id="7c95b-122">Sie kann auch die Video-und Audiostreams durch Komprimierungs Filter weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="7c95b-122">It can also route the video and audio streams through compression filters.</span></span>

<span data-ttu-id="7c95b-123">In den folgenden Abschnitten werden die einzelnen Schritte erläutert.</span><span class="sxs-lookup"><span data-stu-id="7c95b-123">The following sections explain each of these steps.</span></span>

<span data-ttu-id="7c95b-124">Erstellen des renderingabschnitts</span><span class="sxs-lookup"><span data-stu-id="7c95b-124">Build the Rendering Section</span></span>

<span data-ttu-id="7c95b-125">Um den Renderingabschnitt des Diagramms zu erstellen, müssen Sie die [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7c95b-125">To build the rendering section of the graph, call the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method.</span></span> <span data-ttu-id="7c95b-126">Diese Methode nimmt Eingabeparameter an, die den Medien Untertyp für die Ausgabe und den Namen der Ausgabedatei angeben.</span><span class="sxs-lookup"><span data-stu-id="7c95b-126">This method takes input parameters that specify the media subtype for the output and the name of the output file.</span></span> <span data-ttu-id="7c95b-127">Sie gibt Zeiger auf den MUX-Filter und den dateiwriter zurück.</span><span class="sxs-lookup"><span data-stu-id="7c95b-127">It returns pointers to the MUX filter and the file writer.</span></span> <span data-ttu-id="7c95b-128">Der Mux-Filter ist für die nächste Phase der Diagramm Bildung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c95b-128">The MUX filter is needed for the next stage of graph building.</span></span> <span data-ttu-id="7c95b-129">Der Zeiger auf den dateiwriter ist für dieses Beispiel nicht erforderlich, sodass der Parameter **null** sein kann:</span><span class="sxs-lookup"><span data-stu-id="7c95b-129">The pointer to the file writer is not needed for this example, so that parameter can be **NULL**:</span></span>


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



<span data-ttu-id="7c95b-130">Wenn die Methode zurückgegeben wird, hat der Mux-Filter einen ausstehenden Verweis Zähler. Achten Sie daher darauf, dass Sie den Zeiger später freigeben.</span><span class="sxs-lookup"><span data-stu-id="7c95b-130">When the method returns, the MUX filter has an outstanding reference count, so be sure to release the pointer later.</span></span>

<span data-ttu-id="7c95b-131">Das folgende Diagramm zeigt das Filter Diagramm an dieser Stelle.</span><span class="sxs-lookup"><span data-stu-id="7c95b-131">The following diagram shows the filter graph at this point.</span></span>

![Renderingabschnitt des Filter Diagramms](images/avi2avi1.png)

<span data-ttu-id="7c95b-133">Der Mux-Filter macht zwei Schnittstellen zum Steuern des AVI-Formats verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7c95b-133">The MUX filter exposes two interfaces for controlling the AVI format:</span></span>

-   <span data-ttu-id="7c95b-134">[**Iconfiginterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): legt den Überlappung-Modus fest.</span><span class="sxs-lookup"><span data-stu-id="7c95b-134">[**IConfigInterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): Sets the interleaving mode.</span></span>
-   <span data-ttu-id="7c95b-135">[**Iconfigavimux-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): legt den masterb Stream und den AVI-Kompatibilitäts Index fest.</span><span class="sxs-lookup"><span data-stu-id="7c95b-135">[**IConfigAviMux Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): Sets the master stream and the AVI compatibility index.</span></span>

<span data-ttu-id="7c95b-136">Hinzufügen der Quell-und Komprimierungs Filter</span><span class="sxs-lookup"><span data-stu-id="7c95b-136">Add the Source and Compression Filters</span></span>

<span data-ttu-id="7c95b-137">Der nächste Schritt besteht darin, die Quell-und Komprimierungs Filter dem Filter Diagramm hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7c95b-137">The next step is to add the source and compression filters to the filter graph.</span></span> <span data-ttu-id="7c95b-138">Der Erfassungs Diagramm-Generator erstellt automatisch eine Instanz des Filter Graph-Managers, wenn Sie setoutputfilename aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7c95b-138">The Capture Graph Builder automatically creates an instance of the Filter Graph Manager when you call SetOutputFileName.</span></span> <span data-ttu-id="7c95b-139">Rufen Sie einen Zeiger darauf ab, indem Sie die [**ICaptureGraphBuilder2:: getfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) -Methode aufrufen:</span><span class="sxs-lookup"><span data-stu-id="7c95b-139">Get a pointer to it by calling the [**ICaptureGraphBuilder2::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) method:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



<span data-ttu-id="7c95b-140">Aufrufen Sie nun die [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) -Methode, um den asynchronen Datei Quell Filter hinzuzufügen, und die [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode, um den Video-Kompressor hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="7c95b-140">Now call the [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) method to add the Async File Source filter, and the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method to add the video compressor:</span></span>


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



<span data-ttu-id="7c95b-141">An diesem Punkt sind der Quell Filter und der Komprimierungs Filter nicht mit anderen im Diagramm verbunden, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7c95b-141">At this point, the source filter and the compression filter are not connected to anything else in the graph, as shown in the following illustration:</span></span>

![Diagramm mit Quell-und Komprimierungs Filtern Filtern](images/avi2avi2.png)

<span data-ttu-id="7c95b-143">Verbinden Sie die Quelle mit dem MUX</span><span class="sxs-lookup"><span data-stu-id="7c95b-143">Connect the Source to the Mux</span></span>

<span data-ttu-id="7c95b-144">Der letzte Schritt besteht darin, den Quell Filter über den Video-Kompressor mit dem AVI MUX-Filter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="7c95b-144">The final step is to connect the source filter to the AVI Mux filter, through the video compressor.</span></span> <span data-ttu-id="7c95b-145">Verwenden Sie die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode, die eine Ausgabe-PIN im Quell Filter mit einem angegebenen Senderfilter verbindet, optional über einen Komprimierungs Filter.</span><span class="sxs-lookup"><span data-stu-id="7c95b-145">Use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method, which connects an output pin on the source filter to a specified sink filter, optionally through a compression filter.</span></span>

<span data-ttu-id="7c95b-146">Die ersten beiden Parameter geben an, welche der Pins des Quell Filters eine Verbindung herstellen soll, indem Sie eine PIN-Kategorie und einen Medientyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="7c95b-146">The first two parameters specify which of the source filter's pins to connect, by designating a pin category and a media type.</span></span> <span data-ttu-id="7c95b-147">Der asynchrone Datei Quell Filter hat nur eine Ausgabe-PIN, daher sollten diese Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7c95b-147">The Async File Source filter has only one output pin, so these parameters should be **NULL**.</span></span> <span data-ttu-id="7c95b-148">Mit den nächsten drei Parametern werden der Quell Filter, der Komprimierungs Filter (falls vorhanden) und der Mux-Filter angegeben.</span><span class="sxs-lookup"><span data-stu-id="7c95b-148">The next three parameters specify the source filter, the compression filter (if any), and the Mux filter.</span></span>

<span data-ttu-id="7c95b-149">Im folgenden Codebeispiel wird der Videostream über den Video-Kompressor gerendert:</span><span class="sxs-lookup"><span data-stu-id="7c95b-149">The following code example renders the video stream through the video compressor:</span></span>


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



<span data-ttu-id="7c95b-150">Im folgenden Diagramm wird das Filter Diagramm bisher gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c95b-150">The following diagram shows the filter graph so far.</span></span>

![gerenderter Videostream](images/avi2avi3.png)

<span data-ttu-id="7c95b-152">Angenommen, die Quelldatei enthält einen Audiodatenstrom. der [avi-Splitter](avi-splitter-filter.md) Filter hat eine Ausgabe-PIN für das Audioformat erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c95b-152">Assuming that the source file has an audio stream, the [AVI Splitter](avi-splitter-filter.md) filter has created an output pin for the audio.</span></span> <span data-ttu-id="7c95b-153">Um diese PIN zu verbinden, nennen Sie RenderStream erneut:</span><span class="sxs-lookup"><span data-stu-id="7c95b-153">To connect this pin, call RenderStream again:</span></span>


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



<span data-ttu-id="7c95b-154">Hier ist kein Komprimierungs Filter angegeben.</span><span class="sxs-lookup"><span data-stu-id="7c95b-154">Here, no compression filter is specified.</span></span> <span data-ttu-id="7c95b-155">Die Ausgabe-PIN des Quell Filters ist bereits verbunden, sodass die RenderStream-Methode im Splitter Filter eine nicht verbundene Ausgabe-PIN durchsucht.</span><span class="sxs-lookup"><span data-stu-id="7c95b-155">The source filter's output pin is already connected, so the RenderStream method searches for an unconnected output pin on the splitter filter.</span></span> <span data-ttu-id="7c95b-156">Er findet die audiopin und verbindet Sie direkt mit dem MUX-Filter.</span><span class="sxs-lookup"><span data-stu-id="7c95b-156">It finds the audio pin and connects it directly to the MUX filter.</span></span> <span data-ttu-id="7c95b-157">Wenn die Quelldatei nicht über einen Audiodatenstrom verfügt, tritt beim zweiten RenderStream-RenderStream ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7c95b-157">If the source file does not have an audio stream, the second call to RenderStream will fail.</span></span> <span data-ttu-id="7c95b-158">Dieses Verhalten ist normal.</span><span class="sxs-lookup"><span data-stu-id="7c95b-158">This is expected behavior.</span></span> <span data-ttu-id="7c95b-159">Das Diagramm ist nach dem ersten Aufruf von RenderStream fertiggestellt, sodass der Fehler im zweiten Aufruf harmlos ist.</span><span class="sxs-lookup"><span data-stu-id="7c95b-159">The graph is complete after the first call to RenderStream, so the failure in the second call is harmless.</span></span>

<span data-ttu-id="7c95b-160">In diesem Beispiel ist die Reihenfolge der beiden RenderStream-Aufrufe wichtig.</span><span class="sxs-lookup"><span data-stu-id="7c95b-160">In this example, the order of the two RenderStream calls is important.</span></span> <span data-ttu-id="7c95b-161">Da der zweite-Befehl keinen-Kompressor angibt, verbindet er jede nicht verbundene PIN vom avi-Splitter.</span><span class="sxs-lookup"><span data-stu-id="7c95b-161">Because the second call does not specify a compressor, it will connect any unconnected pin from the AVI Splitter.</span></span> <span data-ttu-id="7c95b-162">Wenn Sie diesen Vorgang vor dem anderen durchführen, wird der Videostream möglicherweise ohne den Video-Kompressor mit dem AVI-MUX verbunden.</span><span class="sxs-lookup"><span data-stu-id="7c95b-162">If you make this call before the other one, it might connect the video stream to the AVI Mux, without your video compressor.</span></span> <span data-ttu-id="7c95b-163">Daher muss der spezifischere-Befehl (mit dem Komprimierungs Filter) zuerst erfolgen.</span><span class="sxs-lookup"><span data-stu-id="7c95b-163">Therefore, the more specific call (with the compression filter) must happen first.</span></span>

<span data-ttu-id="7c95b-164">Bei der vorherigen Erörterung wurde angenommen, dass die Quelldatei eine AVI-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="7c95b-164">The previous discussion has assumed that the source file is an AVI file.</span></span> <span data-ttu-id="7c95b-165">Diese Technik funktioniert jedoch auch mit anderen Dateitypen, z. b. MPEG-Dateien.</span><span class="sxs-lookup"><span data-stu-id="7c95b-165">However, this technique also works with other file types, such as MPEG files.</span></span> <span data-ttu-id="7c95b-166">Das resultierende Filter Diagramm unterscheidet sich etwas.</span><span class="sxs-lookup"><span data-stu-id="7c95b-166">The resulting filter graph will be somewhat different.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c95b-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c95b-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c95b-168">Neukomprimieren einer AVI-Datei</span><span class="sxs-lookup"><span data-stu-id="7c95b-168">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 



