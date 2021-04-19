---
description: In diesem Thema wird beschrieben, wie eine Topologie für die Audiowiedergabe oder Videowiedergabe erstellt wird.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Erstellen von Wiedergabe Topologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344386"
---
# <a name="creating-playback-topologies"></a><span data-ttu-id="d5c82-103">Erstellen von Wiedergabe Topologien</span><span class="sxs-lookup"><span data-stu-id="d5c82-103">Creating Playback Topologies</span></span>

<span data-ttu-id="d5c82-104">In diesem Thema wird beschrieben, wie eine Topologie für die Audiowiedergabe oder Videowiedergabe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d5c82-104">This topic describes how to create a topology for audio or video playback.</span></span> <span data-ttu-id="d5c82-105">Für die einfache Wiedergabe können Sie eine partielle Topologie erstellen, in der die Quellknoten direkt mit den Ausgabe Knoten verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="d5c82-105">For basic playback, you can create a partial topology, in which the source nodes are connected directly to the output nodes.</span></span> <span data-ttu-id="d5c82-106">Sie müssen keine Knoten für die zwischen Transformationen, wie z. b. Decoder oder Farb Konverter, einfügen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-106">You do not need to insert any nodes for the intermediate transforms, such as decoders or color converters.</span></span> <span data-ttu-id="d5c82-107">Die Medien Sitzung verwendet den topologielader zum Auflösen der Topologie, und das topologielader fügt die benötigten Transformationen ein.</span><span class="sxs-lookup"><span data-stu-id="d5c82-107">The Media Session will use the topology loader to resolve the topology, and the topology loader will insert the transforms that are required.</span></span>

-   [<span data-ttu-id="d5c82-108">Erstellen der Topologie</span><span class="sxs-lookup"><span data-stu-id="d5c82-108">Creating the Topology</span></span>](#creating-the-topology)
-   [<span data-ttu-id="d5c82-109">Verbinden von Datenströmen mit Medien senken</span><span class="sxs-lookup"><span data-stu-id="d5c82-109">Connecting Streams to Media Sinks</span></span>](#connecting-streams-to-media-sinks)
-   [<span data-ttu-id="d5c82-110">Erstellen der Medien Senke</span><span class="sxs-lookup"><span data-stu-id="d5c82-110">Creating the Media Sink</span></span>](#creating-the-media-sink)
-   [<span data-ttu-id="d5c82-111">Next Steps</span><span class="sxs-lookup"><span data-stu-id="d5c82-111">Next Steps</span></span>](#next-steps)
-   [<span data-ttu-id="d5c82-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5c82-112">Related topics</span></span>](#related-topics)

## <a name="creating-the-topology"></a><span data-ttu-id="d5c82-113">Erstellen der Topologie</span><span class="sxs-lookup"><span data-stu-id="d5c82-113">Creating the Topology</span></span>

<span data-ttu-id="d5c82-114">Im folgenden finden Sie die allgemeinen Schritte zum Erstellen einer partiellen Wiedergabe Topologie aus einer Medienquelle:</span><span class="sxs-lookup"><span data-stu-id="d5c82-114">Here are the overall steps for creating a partial playback topology from a media source:</span></span>

1.  <span data-ttu-id="d5c82-115">Erstellen Sie die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="d5c82-115">Create the media source.</span></span> <span data-ttu-id="d5c82-116">In den meisten Fällen verwenden Sie den quellresolver zum Erstellen der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="d5c82-116">In most cases, you will use the source resolver to create the media source.</span></span> <span data-ttu-id="d5c82-117">Weitere Informationen finden Sie unter [quellresolver](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="d5c82-117">For more information, see [Source Resolver](source-resolver.md).</span></span>
2.  <span data-ttu-id="d5c82-118">Den Präsentations Deskriptor der Medienquelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5c82-118">Get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="d5c82-119">Erstellen Sie eine leere Topologie.</span><span class="sxs-lookup"><span data-stu-id="d5c82-119">Create an empty topology.</span></span>
4.  <span data-ttu-id="d5c82-120">Verwenden Sie den Präsentations Deskriptor, um die streamdeskriptoren aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-120">Use the presentation descriptor to enumerate the stream descriptors.</span></span> <span data-ttu-id="d5c82-121">Für jeden Datenstrom Deskriptor:</span><span class="sxs-lookup"><span data-stu-id="d5c82-121">For each stream descriptor:</span></span>
    1.  <span data-ttu-id="d5c82-122">Holen Sie sich den Haupt Medientyp des Streams, z. b. Audiodaten oder Videos.</span><span class="sxs-lookup"><span data-stu-id="d5c82-122">Get the stream's major media type, such as audio or video.</span></span>
    2.  <span data-ttu-id="d5c82-123">Überprüfen Sie, ob der Stream aktuell ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d5c82-123">Check if the stream is currently selected.</span></span> <span data-ttu-id="d5c82-124">(Optional können Sie einen Stream basierend auf dem Medientyp auswählen oder deaktivieren.)</span><span class="sxs-lookup"><span data-stu-id="d5c82-124">(Optionally, you can select or deselect a stream, based on the media type.)</span></span>
    3.  <span data-ttu-id="d5c82-125">Wenn der Stream ausgewählt ist, erstellen Sie basierend auf dem Medientyp des Streams ein Aktivierungs Objekt für die Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="d5c82-125">If the stream is selected, create an activation object for the media sink, based on the stream's media type.</span></span>
    4.  <span data-ttu-id="d5c82-126">Fügen Sie einen Quellknoten für den Stream und einen Ausgabe Knoten für die Medien Senke hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5c82-126">Add a source node for the stream and an output node for the media sink.</span></span>
    5.  <span data-ttu-id="d5c82-127">Verbinden Sie den Quellknoten mit dem Ausgabe Knoten.</span><span class="sxs-lookup"><span data-stu-id="d5c82-127">Connect the source node to the output node.</span></span>

<span data-ttu-id="d5c82-128">Um diesen Prozess zu vereinfachen, ist der Beispielcode in diesem Thema in mehrere Funktionen gegliedert.</span><span class="sxs-lookup"><span data-stu-id="d5c82-128">To make this process easier to follow, the example code in this topic is organized into several functions.</span></span> <span data-ttu-id="d5c82-129">Die Funktion der obersten Ebene hat den Namen `CreatePlaybackTopology` .</span><span class="sxs-lookup"><span data-stu-id="d5c82-129">The top-level function is named `CreatePlaybackTopology`.</span></span> <span data-ttu-id="d5c82-130">Es werden drei Parameter benötigt:</span><span class="sxs-lookup"><span data-stu-id="d5c82-130">It takes three parameters:</span></span>

-   <span data-ttu-id="d5c82-131">Ein Zeiger auf eine [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="d5c82-131">A pointer to a [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="d5c82-132">Ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="d5c82-132">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span> <span data-ttu-id="d5c82-133">Rufen Sie diesen Zeiger durch Aufrufen von [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)ab.</span><span class="sxs-lookup"><span data-stu-id="d5c82-133">Get this pointer by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="d5c82-134">Für Quellen mit mehreren Präsentationen werden die Präsentations Deskriptoren für nachfolgende Präsentationen im Ereignis [menewpresentation](menewpresentation.md) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d5c82-134">For sources with multiple presentations, the presentation descriptors for subsequent presentations are delivered in the [MENewPresentation](menewpresentation.md) event.</span></span>
-   <span data-ttu-id="d5c82-135">Ein Handle für ein Anwendungsfenster.</span><span class="sxs-lookup"><span data-stu-id="d5c82-135">A handle to an application window.</span></span> <span data-ttu-id="d5c82-136">Wenn die Quelle über einen Videostream verfügt, wird das Video in diesem Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5c82-136">If the source has a video stream, the video will be displayed in this window.</span></span>

<span data-ttu-id="d5c82-137">Die-Funktion gibt einen Zeiger auf eine partielle Wiedergabe Topologie im *pptopology* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="d5c82-137">The function returns a pointer to a partial playback topology in the *ppTopology* parameter.</span></span>


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="d5c82-138">Diese Funktion führt folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d5c82-138">This function performs the following steps:</span></span>

1.  <span data-ttu-id="d5c82-139">Rufen Sie [**mfkreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) auf, um die Topologie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-139">Call [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) to create the topology.</span></span> <span data-ttu-id="d5c82-140">Anfänglich enthält die Topologie keine Knoten.</span><span class="sxs-lookup"><span data-stu-id="d5c82-140">Initially, the topology does not contain any nodes.</span></span>
2.  <span data-ttu-id="d5c82-141">Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorcount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , um die Anzahl der Streams in der Präsentation zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5c82-141">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the presentation.</span></span>
3.  <span data-ttu-id="d5c82-142">Für jeden Stream wird die Anwendungs definierte Funktion für `AddBranchToPartialTopology` eine Verzweigung in der Topologie aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-142">For each stream, call the application-defined `AddBranchToPartialTopology` function to a branch in the topology.</span></span> <span data-ttu-id="d5c82-143">Diese Funktion wird im nächsten Abschnitt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5c82-143">This function is shown in the next section.</span></span>

## <a name="connecting-streams-to-media-sinks"></a><span data-ttu-id="d5c82-144">Verbinden von Datenströmen mit Medien senken</span><span class="sxs-lookup"><span data-stu-id="d5c82-144">Connecting Streams to Media Sinks</span></span>

<span data-ttu-id="d5c82-145">Fügen Sie für jeden ausgewählten Stream einen Quellknoten und einen Ausgabe Knoten hinzu, und verbinden Sie dann die beiden Knoten.</span><span class="sxs-lookup"><span data-stu-id="d5c82-145">For each selected stream, add a source node and an output node, then connect the two nodes.</span></span> <span data-ttu-id="d5c82-146">Der Quellknoten stellt den Datenstrom dar.</span><span class="sxs-lookup"><span data-stu-id="d5c82-146">The source node represents the stream.</span></span> <span data-ttu-id="d5c82-147">Der Ausgabe Knoten stellt den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) oder den [streamingaudiorenderer](streaming-audio-renderer.md) (SAR) dar.</span><span class="sxs-lookup"><span data-stu-id="d5c82-147">The output node represents either the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) or the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

<span data-ttu-id="d5c82-148">Die- `AddBranchToPartialTopology` Funktion, wie im folgenden Beispiel gezeigt, übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="d5c82-148">The `AddBranchToPartialTopology` function, shown in the next example, takes the following parameters:</span></span>

-   <span data-ttu-id="d5c82-149">Ein Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der Topologie.</span><span class="sxs-lookup"><span data-stu-id="d5c82-149">A pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span>
-   <span data-ttu-id="d5c82-150">Ein Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="d5c82-150">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="d5c82-151">Ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="d5c82-151">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span>
-   <span data-ttu-id="d5c82-152">Der null basierte Index des Streams.</span><span class="sxs-lookup"><span data-stu-id="d5c82-152">The zero-based index of the stream.</span></span>
-   <span data-ttu-id="d5c82-153">Ein Handle für das Videofenster.</span><span class="sxs-lookup"><span data-stu-id="d5c82-153">A handle to the video window.</span></span> <span data-ttu-id="d5c82-154">Dieses Handle wird nur für den Videostream verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5c82-154">This handle is used only for the video stream.</span></span>


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



<span data-ttu-id="d5c82-155">Die Funktion führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="d5c82-155">The function does the following:</span></span>

1.  <span data-ttu-id="d5c82-156">Ruft [**IMF presentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) auf und übergibt den streamindex.</span><span class="sxs-lookup"><span data-stu-id="d5c82-156">Calls [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and passes in the stream index.</span></span> <span data-ttu-id="d5c82-157">Diese Methode gibt einen Zeiger auf den Datenstrom Deskriptor für diesen Stream zusammen mit einem booleschen Wert zurück, der angibt, ob der Stream ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d5c82-157">This method returns a pointer to the stream descriptor for that stream, along with a Boolean value indicating whether the stream is selected.</span></span>
2.  <span data-ttu-id="d5c82-158">Wenn der Stream nicht ausgewählt ist, wird die Funktion beendet, und \_ es wird OK zurückgegeben, da die Anwendung nur dann eine topologieverzweigung für einen Stream erstellen muss, wenn Sie ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d5c82-158">If the stream is not selected, the function exits and returns S\_OK, because the application does not need to create a topology branch for a stream unless it is selected.</span></span>
3.  <span data-ttu-id="d5c82-159">Wenn der Stream ausgewählt ist, vervollständigt die Funktion den topologiebranch wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d5c82-159">If the stream is selected, the function completes the topology branch as follows:</span></span>
    1.  <span data-ttu-id="d5c82-160">Erstellt ein Aktivierungs Objekt für die Senke, indem die von der Anwendung definierte createmediasinkaktivierungs-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d5c82-160">Creates an activation object for the sink, by calling the application-defined CreateMediaSinkActivate function.</span></span> <span data-ttu-id="d5c82-161">Diese Funktion wird im nächsten Abschnitt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5c82-161">This function is shown in the next section.</span></span>
    2.  <span data-ttu-id="d5c82-162">Fügt der Topologie einen Quellknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5c82-162">Adds a source node to the topology.</span></span> <span data-ttu-id="d5c82-163">Code für diesen Schritt finden Sie im Thema [Erstellen von Quellknoten](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="d5c82-163">Code for this step is shown in the topic [Creating Source Nodes](creating-source-nodes.md).</span></span>
    3.  <span data-ttu-id="d5c82-164">Fügt der Topologie einen Ausgabe Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5c82-164">Adds an output node to the topology.</span></span> <span data-ttu-id="d5c82-165">Code für diesen Schritt wird im Thema Erstellen von [Ausgabe Knoten](creating-output-nodes.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5c82-165">Code for this step is shown in the topic [Creating Output Nodes](creating-output-nodes.md).</span></span>
    4.  <span data-ttu-id="d5c82-166">Verbindet die beiden Knoten durch Aufrufen von [**imftopologynode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) auf dem Quellknoten.</span><span class="sxs-lookup"><span data-stu-id="d5c82-166">Connects the two nodes by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the source node.</span></span> <span data-ttu-id="d5c82-167">Durch das Verbinden der Knoten gibt die Anwendung an, dass der upstreamknoten Daten an den downstreamknoten übermitteln soll.</span><span class="sxs-lookup"><span data-stu-id="d5c82-167">By connecting the nodes, the application indicates that the upstream node should deliver data to the downstream node.</span></span> <span data-ttu-id="d5c82-168">Ein Quellknoten verfügt über eine Ausgabe, und ein Ausgabe Knoten verfügt über eine Eingabe, sodass beide streamindizes NULL sind.</span><span class="sxs-lookup"><span data-stu-id="d5c82-168">A source node has one output, and an output node has one input, so both stream indexes are zero.</span></span>

<span data-ttu-id="d5c82-169">Erweiterte Anwendungen können Streams auswählen oder deaktivieren, anstatt die Standardkonfiguration der Quelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5c82-169">More advanced applications can select or deselect streams, instead of using the source's default configuration.</span></span> <span data-ttu-id="d5c82-170">Eine Quelle kann über mehrere Datenströme verfügen, von denen jede möglicherweise standardmäßig ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d5c82-170">A source could have multiple streams, and any of them might be selected by default.</span></span> <span data-ttu-id="d5c82-171">Der Präsentations Deskriptor der Medienquelle verfügt über einen Standardsatz von streamauswahlen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-171">The media source's presentation descriptor has a default set of stream selections.</span></span> <span data-ttu-id="d5c82-172">In einer einfachen Videodatei mit einem einzelnen Audiostream und Videostream wählt die Medienquelle in der Regel beide Streams standardmäßig aus.</span><span class="sxs-lookup"><span data-stu-id="d5c82-172">In a simple video file with a single audio stream and video stream, the media source will usually select both streams by default.</span></span> <span data-ttu-id="d5c82-173">Eine Datei kann jedoch mehrere Audiostreams für verschiedene Sprachen oder mehrere Videostreams enthalten, die mit unterschiedlichen Bitraten codiert sind.</span><span class="sxs-lookup"><span data-stu-id="d5c82-173">However, a file might have multiple audio streams for different languages, or multiple video streams encoded at different bit rates.</span></span> <span data-ttu-id="d5c82-174">In diesem Fall werden einige der Streams standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5c82-174">In that case, some of the streams will be unselected by default.</span></span> <span data-ttu-id="d5c82-175">Die Anwendung kann die Auswahl ändern, indem Sie [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) und [**imfpresentationdescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) im Präsentations Deskriptor aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-175">The application can change the selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) on the presentation descriptor.</span></span>

## <a name="creating-the-media-sink"></a><span data-ttu-id="d5c82-176">Erstellen der Medien Senke</span><span class="sxs-lookup"><span data-stu-id="d5c82-176">Creating the Media Sink</span></span>

<span data-ttu-id="d5c82-177">Die Next-Funktion erstellt ein Aktivierungs Objekt für die EVR-oder SAR-Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="d5c82-177">The next function creates an activation object for the EVR or SAR media sink.</span></span>


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



<span data-ttu-id="d5c82-178">Diese Funktion führt folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d5c82-178">This function performs the following steps:</span></span>

1.  <span data-ttu-id="d5c82-179">Ruft [**IMF-Deskriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den Datenstrom Deskriptor auf.</span><span class="sxs-lookup"><span data-stu-id="d5c82-179">Calls [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span> <span data-ttu-id="d5c82-180">Diese Methode gibt einen [**IMF Media**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) Type-Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="d5c82-180">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface pointer.</span></span>

2.  <span data-ttu-id="d5c82-181">Ruft [**IMF mediatypeer Handler:: getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype)auf.</span><span class="sxs-lookup"><span data-stu-id="d5c82-181">Calls [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="d5c82-182">Diese Methode gibt die GUID des Haupt Typs für den Datenstrom zurück.</span><span class="sxs-lookup"><span data-stu-id="d5c82-182">This method returns the major type GUID for the stream.</span></span>

3.  <span data-ttu-id="d5c82-183">Wenn der Streamtyp audiobasiert ist, ruft die Funktion [**mfkreateaudiorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) auf, um das Aktivierungs Objekt für audiorenderer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-183">If the stream type is audio, the function calls [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) to create the audio renderer activation object.</span></span> <span data-ttu-id="d5c82-184">Wenn der Streamtyp "Video" ist, ruft die Funktion " [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) " auf, um das Videorenderer-Aktivierungs Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5c82-184">If the stream type is video, the function calls [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the video renderer activation object.</span></span> <span data-ttu-id="d5c82-185">Beide Funktionen geben einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="d5c82-185">Both of these functions return a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="d5c82-186">Dieser Zeiger wird verwendet, um den Ausgabe Knoten für die Senke zu initialisieren, wie zuvor gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5c82-186">This pointer is used to initialize the output node for the sink, as shown previously.</span></span>

<span data-ttu-id="d5c82-187">Für jeden anderen Streamtyp wird in diesem Beispiel ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5c82-187">For any other stream type, this example returns an error code.</span></span> <span data-ttu-id="d5c82-188">Alternativ können Sie einfach den Datenstrom deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d5c82-188">Alternatively, you could simply deselect the stream.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d5c82-189">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d5c82-189">Next Steps</span></span>

<span data-ttu-id="d5c82-190">Um jeweils eine Mediendatei wiederzugeben, stellen Sie die Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in eine Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="d5c82-190">To play one media file at a time, queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="d5c82-191">Die Medien Sitzung verwendet den topologielader zum Auflösen der Topologie.</span><span class="sxs-lookup"><span data-stu-id="d5c82-191">The Media Session will use the topology loader to resolve the topology.</span></span> <span data-ttu-id="d5c82-192">Ein umfassendes Beispiel finden Sie unter wieder [Gabe von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="d5c82-192">For a complete example, see [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5c82-193">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5c82-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5c82-194">Wiedergabe nicht geschützter Mediendateien</span><span class="sxs-lookup"><span data-stu-id="d5c82-194">How to Play Unprotected Media Files</span></span>](how-to-play-unprotected-media-files.md)
</dt> <dt>

[<span data-ttu-id="d5c82-195">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="d5c82-195">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="d5c82-196">Topologien</span><span class="sxs-lookup"><span data-stu-id="d5c82-196">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



