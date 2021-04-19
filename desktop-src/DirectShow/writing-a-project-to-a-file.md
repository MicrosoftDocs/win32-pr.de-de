---
description: Schreiben eines Projekts in eine Datei
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Schreiben eines Projekts in eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348663"
---
# <a name="writing-a-project-to-a-file"></a><span data-ttu-id="4b7ee-103">Schreiben eines Projekts in eine Datei</span><span class="sxs-lookup"><span data-stu-id="4b7ee-103">Writing a Project to a File</span></span>

<span data-ttu-id="4b7ee-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="4b7ee-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4b7ee-105">In diesem Artikel wird beschrieben, wie Sie ein [DirectShow-Bearbeitungs Dienst](directshow-editing-services.md) Projekt in eine Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-105">This article describes how to write a [DirectShow Editing Services](directshow-editing-services.md) project to a file.</span></span> <span data-ttu-id="4b7ee-106">Zunächst wird beschrieben, wie Sie eine Datei mit der grundlegenden Renderingengine schreiben.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-106">First it describes how to write a file with the basic render engine.</span></span> <span data-ttu-id="4b7ee-107">Anschließend wird die intelligente Neukomprimierung mit dem intelligenten Renderingmodul beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-107">Then it describes smart recompression with the smart render engine.</span></span>

<span data-ttu-id="4b7ee-108">Einen Überblick darüber, wie DirectShow-Bearbeitungs Dienste Projekte rendern, finden Sie unter [Informationen zu den renderingmodulen](about-the-render-engines.md).</span><span class="sxs-lookup"><span data-stu-id="4b7ee-108">For an overview of how DirectShow Editing Services renders projects, see [About the Render Engines](about-the-render-engines.md).</span></span>

<span data-ttu-id="4b7ee-109">**Verwenden der grundlegenden Renderingengine**</span><span class="sxs-lookup"><span data-stu-id="4b7ee-109">**Using the Basic Render Engine**</span></span>

<span data-ttu-id="4b7ee-110">Beginnen Sie, indem Sie das Front-End des Diagramms wie folgt aufbauen:</span><span class="sxs-lookup"><span data-stu-id="4b7ee-110">Start by building the front end of the graph, as follows:</span></span>

1.  <span data-ttu-id="4b7ee-111">Erstellen Sie die Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-111">Create the render engine.</span></span>
2.  <span data-ttu-id="4b7ee-112">Angeben der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-112">Specify the timeline.</span></span>
3.  <span data-ttu-id="4b7ee-113">Legen Sie den Rendering-Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-113">Set the render range.</span></span> <span data-ttu-id="4b7ee-114">(Optional)</span><span class="sxs-lookup"><span data-stu-id="4b7ee-114">(Optional)</span></span>
4.  <span data-ttu-id="4b7ee-115">Erstellen Sie das Front-End des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-115">Build the front end of the graph.</span></span>

<span data-ttu-id="4b7ee-116">Das folgende Codebeispiel zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-116">The following code example shows these steps.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



<span data-ttu-id="4b7ee-117">Fügen Sie als nächstes Multiplexer-und Datei Schreib Filter zum Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-117">Next, add multiplexer and file-writing filters to the filter graph.</span></span> <span data-ttu-id="4b7ee-118">Dies lässt sich am einfachsten mit dem [Erfassungs Diagramm](capture-graph-builder.md)-Generator, einer DirectShow-Komponente zum Erstellen von Erfassungs Diagrammen, erreichen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-118">The easiest way to do this is with the [Capture Graph Builder](capture-graph-builder.md), a DirectShow component for building capture graphs.</span></span> <span data-ttu-id="4b7ee-119">Der Erfassungs Diagramm-Generator macht die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-119">The capture graph builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="4b7ee-120">Führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="4b7ee-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="4b7ee-121">Erstellen Sie eine Instanz des Erfassungs Diagramm-Generators.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-121">Create an instance of the capture graph builder.</span></span>
2.  <span data-ttu-id="4b7ee-122">Rufen Sie einen Zeiger auf das Diagramm ab, und übergeben Sie ihn an den Diagramm-Generator.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-122">Obtain a pointer to the graph and pass it to the graph builder.</span></span>
3.  <span data-ttu-id="4b7ee-123">Geben Sie den Namen und den Medientyp der Ausgabedatei an.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-123">Specify the name and media type of the output file.</span></span> <span data-ttu-id="4b7ee-124">In diesem Schritt wird auch ein Zeiger auf den MUX-Filter abgerufen, der später erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-124">This step also obtains a pointer to the mux filter, which is required later.</span></span>

<span data-ttu-id="4b7ee-125">Das folgende Codebeispiel zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-125">The following code example shows these steps.</span></span>


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



<span data-ttu-id="4b7ee-126">Verbinden Sie schließlich die Ausgabe Pins auf dem Front-End mit dem MUX-Filter.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-126">Finally, connect the output pins on the front end to the mux filter.</span></span>

1.  <span data-ttu-id="4b7ee-127">Abrufen der Anzahl von Gruppen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-127">Retrieve the number of groups.</span></span>
2.  <span data-ttu-id="4b7ee-128">Rufen Sie für jede PIN einen Zeiger auf die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-128">For each pin, obtain a pointer to the pin.</span></span>
3.  <span data-ttu-id="4b7ee-129">Erstellen Sie optional eine Instanz eines Komprimierungs Filters, um den Stream zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-129">Optionally, create an instance of a compression filter to compress the stream.</span></span> <span data-ttu-id="4b7ee-130">Der Typ des-Kompressors hängt vom Medientyp der Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-130">The type of compressor will depend on the media type of the group.</span></span> <span data-ttu-id="4b7ee-131">Sie können den [Enumerator "System Geräte](system-device-enumerator.md) " verwenden, um die verfügbaren Komprimierungs Filter aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-131">You can use the [System Device Enumerator](system-device-enumerator.md) to enumerate the available compression filters.</span></span> <span data-ttu-id="4b7ee-132">Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4b7ee-132">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>
4.  <span data-ttu-id="4b7ee-133">Legen Sie optional Komprimierungs Parameter fest, z. b. die Keyframe-Rate.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-133">Optionally, set compression parameters such as the key-frame rate.</span></span> <span data-ttu-id="4b7ee-134">Dieser Schritt wird weiter unten in diesem Artikel ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-134">This step is discussed in detail later in the article.</span></span>
5.  <span data-ttu-id="4b7ee-135">[**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-135">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="4b7ee-136">Diese Methode nimmt Zeiger auf die PIN, den Komprimierungs Filter (falls vorhanden) und den Multiplexer.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-136">This method takes pointers to the pin, the compression filter (if any), and the multiplexer.</span></span>

<span data-ttu-id="4b7ee-137">Im folgenden Codebeispiel wird gezeigt, wie die Ausgabe Pins verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-137">The following code example shows how to connect the output pins.</span></span>


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



<span data-ttu-id="4b7ee-138">Verwenden Sie zum Festlegen von Komprimierungs Parametern (Schritt 4, früher) die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-138">To set compression parameters (step 4, previously), use the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="4b7ee-139">Diese Schnittstelle wird auf den Ausgabe Pins von Komprimierungs Filtern verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-139">This interface is exposed on the output pins of compression filters.</span></span> <span data-ttu-id="4b7ee-140">Zählen Sie die Pins des Komprimierungs Filters auf, und Fragen Sie jede Ausgabe-PIN für **IAMVideoCompression** ab.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-140">Enumerate the compression filter's pins, and query each output pin for **IAMVideoCompression**.</span></span> <span data-ttu-id="4b7ee-141">(Informationen zum Auflisten von Pins finden Sie unter [Enumerieren von Pins](enumerating-pins.md).) Achten Sie darauf, alle Schnittstellen Zeiger freizugeben, die Sie während dieses Schritts abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-141">(For information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).) Be sure to release all the interface pointers that you obtained during this step.</span></span>

<span data-ttu-id="4b7ee-142">Nachdem Sie das Filter Diagramm erstellt haben, können Sie die [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) -Methode für den Filter Graph-Manager aufruft.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-142">After you build the filter graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method on the filter graph manager.</span></span> <span data-ttu-id="4b7ee-143">Während der Ausführung des Filter Diagramms werden die Daten in eine Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-143">As the filter graph runs, it writes the data to a file.</span></span> <span data-ttu-id="4b7ee-144">Verwenden Sie die Ereignis Benachrichtigung, um die Wiedergabe zu warten.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-144">Use event notification to wait for playback to complete.</span></span> <span data-ttu-id="4b7ee-145">(Weitere Informationen finden [Sie unter reagieren auf Ereignisse](responding-to-events.md).) Wenn die Wiedergabe abgeschlossen ist, müssen Sie [**IMediaControl:: beenden**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) explizit zum Beenden des Filter Diagramms aufruft.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-145">(See [Responding to Events](responding-to-events.md).) When playback finishes, you must explicitly call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) to stop the filter graph.</span></span> <span data-ttu-id="4b7ee-146">Andernfalls wird die Datei nicht ordnungsgemäß geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-146">Otherwise, the file is not written correctly.</span></span>

<span data-ttu-id="4b7ee-147">**Verwenden der intelligenten Renderingengine**</span><span class="sxs-lookup"><span data-stu-id="4b7ee-147">**Using the Smart Render Engine**</span></span>

<span data-ttu-id="4b7ee-148">Um die Vorteile der intelligenten Neukomprimierung zu nutzen, verwenden Sie die Smart-Rendering-Engine anstelle der grundlegenden Renderingengine.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-148">To get the benefits of smart recompression, use the smart render engine in place of the basic render engine.</span></span> <span data-ttu-id="4b7ee-149">Die Schritte zum Aufbau des Diagramms sind fast identisch.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-149">The steps in building the graph are almost the same.</span></span> <span data-ttu-id="4b7ee-150">Der Hauptunterschied besteht darin, dass die Komprimierung am Front-End des Diagramms erfolgt, nicht im Abschnitt zum Schreiben von Dateien.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-150">The major difference is that compression is handled in the front end of the graph, not in the file-writing section.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b7ee-151">Verwenden Sie die Smart-Rendering-Engine nicht zum Lesen oder Schreiben von Windows Media-Dateien.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-151">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

<span data-ttu-id="4b7ee-152">Jede Videogruppe verfügt über eine-Eigenschaft, die das Komprimierungs Format für diese Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-152">Each video group has a property that specifies the compression format for that group.</span></span> <span data-ttu-id="4b7ee-153">Das Komprimierungs Format muss in Höhe, Breite, Bittiefe und Framerate genau mit dem unkomprimierten Format der Gruppe übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-153">The compression format must exactly match the group's uncompressed format in height, width, bit depth, and frame rate.</span></span> <span data-ttu-id="4b7ee-154">Das Smart-Renderingmodul verwendet das Komprimierungs Format beim Erstellen des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-154">The smart render engine uses the compression format when it constructs the graph.</span></span> <span data-ttu-id="4b7ee-155">Bevor Sie das Komprimierungs Format festlegen, stellen Sie sicher, dass das unkomprimierte Format für diese Gruppe durch Aufrufen von [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-155">Before you set the compression format, make sure to set the uncompressed format for that group by calling [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).</span></span>

<span data-ttu-id="4b7ee-156">Um das Komprimierungs Format einer Gruppe festzulegen, rufen Sie die [**iamtimelinegroup:: sezmartrecompressformat**](iamtimelinegroup-setsmartrecompressformat.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-156">To set a group's compression format, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span> <span data-ttu-id="4b7ee-157">Diese Methode nimmt einen Zeiger auf eine [**SCompFmt0**](scompfmt0.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-157">This method takes a pointer to an [**SCompFmt0**](scompfmt0.md) structure.</span></span> <span data-ttu-id="4b7ee-158">Die **SCompFmt0** -Struktur verfügt über zwei Member: **nformatid**, die 0 (null) sein muss, und **mediaType**, die eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-158">The **SCompFmt0** structure has two members: **nFormatId**, which must be zero, and **MediaType**, which is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="4b7ee-159">Initialisieren Sie die **am- \_ \_ Medientyp** Struktur mit den Formatinformationen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-159">Initialize the **AM\_MEDIA\_TYPE** structure with the format information.</span></span>

> [!Note]  
> <span data-ttu-id="4b7ee-160">Wenn Sie möchten, dass das endgültige Projekt das gleiche Format wie eine der Quelldateien hat, können Sie die am- \_ \_ Medientyp Struktur mithilfe des Medien Detektors direkt aus der Quelldatei beziehen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-160">If you want the final project to have the same format as one of your source files, you can get the AM\_MEDIA\_TYPE structure directly from the source file, using the media detector.</span></span> <span data-ttu-id="4b7ee-161">Weitere Informationen finden [**Sie unter imediadet:: get \_ streammediatype**](imediadet-get-streammediatype.md).</span><span class="sxs-lookup"><span data-stu-id="4b7ee-161">See [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md).</span></span>

 

<span data-ttu-id="4b7ee-162">Wandeln Sie die [**SCompFmt0**](scompfmt0.md) -Variable in einen Zeiger vom Typ **Long** um, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-162">Cast the [**SCompFmt0**](scompfmt0.md) variable to a pointer of type **long**, as shown in the following example.</span></span>


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



<span data-ttu-id="4b7ee-163">Die intelligente Renderingengine sucht automatisch nach einem kompatiblen Komprimierungs Filter.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-163">The smart render engine automatically searches for a compatible compression filter.</span></span> <span data-ttu-id="4b7ee-164">Sie können auch einen Komprimierungs Filter für eine Gruppe angeben, indem Sie [**ismartrenderengine:: setgroupkompressor**](ismartrenderengine-setgroupcompressor.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-164">You can also specify a compression filter for a group by calling [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span></span>

<span data-ttu-id="4b7ee-165">Um das Diagramm zu erstellen, verwenden Sie die gleichen Schritte, die im vorherigen Abschnitt für die grundlegende Renderingengine beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-165">To build the graph, use the same steps that were described for the Basic Render Engine in the previous section.</span></span> <span data-ttu-id="4b7ee-166">Die einzigen Unterschiede sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="4b7ee-166">The only differences are the following:</span></span>

-   <span data-ttu-id="4b7ee-167">Verwenden Sie die Smart-Rendering-Engine, nicht die grundlegende Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-167">Use the smart render engine, not the basic render engine.</span></span> <span data-ttu-id="4b7ee-168">Der Klassen Bezeichner ist CLSID \_ smartrenderengine.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-168">The class identifier is CLSID\_SmartRenderEngine.</span></span>
-   <span data-ttu-id="4b7ee-169">Legen Sie Komprimierungs Parameter fest, nachdem Sie das Front-End erstellt haben, aber bevor Sie die Ausgabe Pins renden</span><span class="sxs-lookup"><span data-stu-id="4b7ee-169">Set compression parameters after you build the front end but before you render the output pins.</span></span> <span data-ttu-id="4b7ee-170">Rufen Sie die [**ismartrenderengine:: getgroupcompressor**](ismartrenderengine-getgroupcompressor.md) -Methode auf, um einen Zeiger auf den Komprimierungs Filter einer Gruppe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-170">Call the [**ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) method to obtain a pointer to a group's compression filter.</span></span> <span data-ttu-id="4b7ee-171">Fragen Sie dann die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle ab, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-171">Then query for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, as described previously.</span></span>
-   <span data-ttu-id="4b7ee-172">Wenn Sie die Ausgabe Pins rendernen, ist es nicht erforderlich, einen Komprimierungs Filter einzufügen.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-172">When you render the output pins, there is no need to insert a compression filter.</span></span> <span data-ttu-id="4b7ee-173">Der Stream ist bereits komprimiert.</span><span class="sxs-lookup"><span data-stu-id="4b7ee-173">The stream is already compressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b7ee-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b7ee-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b7ee-175">Rendern eines Projekts</span><span class="sxs-lookup"><span data-stu-id="4b7ee-175">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



