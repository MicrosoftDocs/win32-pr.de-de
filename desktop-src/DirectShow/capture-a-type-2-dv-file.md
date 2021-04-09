---
description: Erfassung einer Type-2-DV-Datei
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Erfassung einer Type-2-DV-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860033"
---
# <a name="capture-a-type-2-dv-file"></a><span data-ttu-id="d9084-103">Erfassung einer Type-2-DV-Datei</span><span class="sxs-lookup"><span data-stu-id="d9084-103">Capture a Type-2 DV File</span></span>

<span data-ttu-id="d9084-104">Eine Type-2-DV-AVI-Datei enthält zwei Streams, eine mit DV-Video und eine andere, die Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="d9084-104">A type-2 DV AVI file has two streams, one that contains DV video and another that contains audio.</span></span> <span data-ttu-id="d9084-105">Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Datei vom Typ 2 zu erfassen, während die Vorschau angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d9084-105">To capture a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![Typ-2-Erfassung mit Vorschau](images/dv2-cap.png)

<span data-ttu-id="d9084-107">Dieses Diagramm ist fast identisch mit dem Diagramm für die Erfassung von Type-1 (siehe [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span><span class="sxs-lookup"><span data-stu-id="d9084-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span></span> <span data-ttu-id="d9084-108">Der Erfassungsdaten Strom durchläuft jedoch den [DV-Splitter](dv-splitter-filter.md) Filter, bevor der [AVI MUX](avi-mux-filter.md) -Filter erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="d9084-108">However, the capture stream goes through the [DV Splitter](dv-splitter-filter.md) filter before reaching the [AVI Mux](avi-mux-filter.md) filter.</span></span> <span data-ttu-id="d9084-109">Der AVI-MUX empfängt daher zwei Streams, einen Audiostream und einen DV-codierten Videostream.</span><span class="sxs-lookup"><span data-stu-id="d9084-109">The AVI Mux therefore receives two streams, an audio stream and a DV-encoded video stream.</span></span>

<span data-ttu-id="d9084-110">Erstellen Sie dieses Diagramm wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d9084-110">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="d9084-111">Erstellen Sie den DV-Splitter, und fügen Sie ihn dem Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="d9084-111">Create the DV Splitter and add it to the filter graph.</span></span>
2.  <span data-ttu-id="d9084-112">Aufrufen von [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , um den AVI MUX-Filter mit dem dateiwriter-Filter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="d9084-112">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
3.  <span data-ttu-id="d9084-113">[**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) zum Verbinden des msdv-Erfassungs Filters mit dem DV-Splitter aufruft.</span><span class="sxs-lookup"><span data-stu-id="d9084-113">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the MSDV capture filter to the DV Splitter.</span></span> <span data-ttu-id="d9084-114">Dieser Befehl verbindet auch einen der Ausgabe Pins des DV-Splitters mit dem AVI MUX.</span><span class="sxs-lookup"><span data-stu-id="d9084-114">This call also connects one of the DV Splitter's output pins to the AVI Mux.</span></span>
4.  <span data-ttu-id="d9084-115">RenderStream erneut aufgerufen, um die andere PIN des DV-Splitters mit dem AVI-MUX zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="d9084-115">Call RenderStream again to connect the DV Splitter's other pin to the AVI Mux.</span></span>
5.  <span data-ttu-id="d9084-116">RenderStream wird ein drittes Mal aufgerufen, um den Vorschau Datenstrom zu rendern.</span><span class="sxs-lookup"><span data-stu-id="d9084-116">Call RenderStream a third time to render the preview stream.</span></span> <span data-ttu-id="d9084-117">Überspringen Sie diesen Schritt, wenn Sie das Video nicht in der Vorschau anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d9084-117">Skip this step if do not want to preview the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9084-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9084-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9084-119">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d9084-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



