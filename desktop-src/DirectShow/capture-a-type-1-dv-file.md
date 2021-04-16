---
description: Erfassen einer DV-Datei vom Typ "1"
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Erfassen einer DV-Datei vom Typ "1"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558947"
---
# <a name="capture-a-type-1-dv-file"></a><span data-ttu-id="6513a-103">Erfassen einer DV-Datei vom Typ "1"</span><span class="sxs-lookup"><span data-stu-id="6513a-103">Capture a Type-1 DV File</span></span>

<span data-ttu-id="6513a-104">Eine "Type-1 DV AVI"-Datei enthält einen einzelnen überlappenden Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="6513a-104">A type-1 DV AVI file contains a single interleaved stream.</span></span> <span data-ttu-id="6513a-105">Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Datei vom Typ 1 zu erfassen, während die Vorschau angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6513a-105">To capture a type-1 file while previewing, use the filter graph shown in the following diagram.</span></span>

![Typ-1-Erfassung mit Vorschau](images/dv1-cap.png)

<span data-ttu-id="6513a-107">Die Filter in diesem Diagramm umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6513a-107">Filters in this graph include:</span></span>

-   <span data-ttu-id="6513a-108">Der [Smart Tee](smart-tee-filter.md) -Filter teilt den überlappenden DV in einen Aufzeichnungsdaten Strom und einen Vorschau Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="6513a-108">The [Smart Tee](smart-tee-filter.md) filter splits the interleaved DV into a capture stream and a preview stream.</span></span> <span data-ttu-id="6513a-109">Beide Streams enthalten die gleichen verschachtelten Daten.</span><span class="sxs-lookup"><span data-stu-id="6513a-109">Both streams contain the same interleaved data.</span></span>
-   <span data-ttu-id="6513a-110">Der [AVI MUX](avi-mux-filter.md) und der [dateiwriter](file-writer-filter.md) schreiben den verschachtelten Stream auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="6513a-110">The [AVI Mux](avi-mux-filter.md) and [File Writer](file-writer-filter.md) write the interleaved stream to disk.</span></span>
-   <span data-ttu-id="6513a-111">Der [DV-Splitter](dv-splitter-filter.md) teilt den verschachtelten Stream in einen DV-Videostream und einen Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="6513a-111">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream and an audio stream.</span></span> <span data-ttu-id="6513a-112">Beide Streams sind rendererd für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="6513a-112">Both streams are rendererd for preview.</span></span>
-   <span data-ttu-id="6513a-113">Der [DV-Video-Decoder](dv-video-decoder-filter.md) decodiert den DV-Videodaten Strom für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="6513a-113">The [DV Video Decoder](dv-video-decoder-filter.md) decodes the DV video stream for previewing.</span></span>

<span data-ttu-id="6513a-114">Erstellen Sie dieses Diagramm wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6513a-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="6513a-115">Aufrufen von [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , um den AVI MUX-Filter mit dem dateiwriter-Filter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="6513a-115">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
2.  <span data-ttu-id="6513a-116">Ruft [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) mit der PIN Category Pin \_ Category \_ Capture auf, um den Aufzeichnungsdaten Strom zu rendern.</span><span class="sxs-lookup"><span data-stu-id="6513a-116">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the pin category PIN\_CATEGORY\_CAPTURE to render the capture stream.</span></span> <span data-ttu-id="6513a-117">Der Erfassungs Diagramm-Generator fügt automatisch den intelligenten Tee-Filter ein.</span><span class="sxs-lookup"><span data-stu-id="6513a-117">The Capture Graph Builder automatically inserts the Smart Tee filter.</span></span>
3.  <span data-ttu-id="6513a-118">RenderStream erneut aufzurufen, aber mit der PIN Category Pin \_ Category \_ Preview, um den Vorschau Datenstrom zu rendern.</span><span class="sxs-lookup"><span data-stu-id="6513a-118">Call RenderStream again, but with the pin category PIN\_CATEGORY\_PREVIEW, to render the preview stream.</span></span> <span data-ttu-id="6513a-119">Überspringen Sie diesen Befehl, wenn Sie das Video nicht in der Vorschau anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="6513a-119">Skip this call if you do not want to preview the video.</span></span>

<span data-ttu-id="6513a-120">Bei beiden Aufrufen von RenderStream ist MediaType überlappende der Medientyp, d. h. überlappende \_ DV-Videos.</span><span class="sxs-lookup"><span data-stu-id="6513a-120">For both calls to RenderStream, the media type is MEDIATYPE\_Interleaved, meaning interleaved DV video.</span></span> <span data-ttu-id="6513a-121">In diesem Code fügt der Erfassungs Diagramm-Generator automatisch jeden benötigten Filter hinzu, mit Ausnahme des msdv-Erfassungs Filters.</span><span class="sxs-lookup"><span data-stu-id="6513a-121">In this code, the Capture Graph Builder automatically adds every filter that is needed, except for the MSDV capture filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6513a-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6513a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6513a-123">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6513a-123">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



