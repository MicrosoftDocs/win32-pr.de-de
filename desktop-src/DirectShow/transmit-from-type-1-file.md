---
description: Übertragen von Datei vom Typ "-1"
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Übertragen von Datei vom Typ "-1"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042410"
---
# <a name="transmit-from-type-1-file"></a><span data-ttu-id="e24d2-103">Übertragen von Datei vom Typ "-1"</span><span class="sxs-lookup"><span data-stu-id="e24d2-103">Transmit from Type-1 File</span></span>

<span data-ttu-id="e24d2-104">Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Datei vom Typ 1 zu übertragen, während Sie die Datei in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e24d2-104">To transmit a type-1 file while previewing the file, use the filter graph shown in the following diagram.</span></span>

![Type-1-Übertragung mit Vorschau](images/dv1-transmit.png)

<span data-ttu-id="e24d2-106">Die Filter in diesem Diagramm umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e24d2-106">Filters in this graph include:</span></span>

-   <span data-ttu-id="e24d2-107">Der [avi-Splitter](avi-splitter-filter.md) analysiert die AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="e24d2-107">The [AVI Splitter](avi-splitter-filter.md) parses the AVI file.</span></span> <span data-ttu-id="e24d2-108">Für eine DV-Datei vom Typ "1" liefert die Ausgabe-PIN verschachtelte DV-Beispiele.</span><span class="sxs-lookup"><span data-stu-id="e24d2-108">For a type-1 DV file, the output pin delivers interleaved DV samples.</span></span>
-   <span data-ttu-id="e24d2-109">Der [unendliche Pin-Tee](infinite-pin-tee-filter.md) -Filter teilt den verschachtelten DV in einen übertragungstream und einen Vorschau Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e24d2-109">The [Infinite Pin Tee](infinite-pin-tee-filter.md) filter splits the interleaved DV into a transmit stream and a preview stream.</span></span> <span data-ttu-id="e24d2-110">Beide Streams enthalten die gleichen verschachtelten Daten.</span><span class="sxs-lookup"><span data-stu-id="e24d2-110">Both streams contain the same interleaved data.</span></span> <span data-ttu-id="e24d2-111">(Dieses Diagramm verwendet den unendlichen Pin-Tee anstelle des [intelligenten Ausstellers](smart-tee-filter.md), da es keine Gefahr gibt, Rahmen beim Lesen aus einer Datei zu löschen, wie es bei Live Capture der Fall ist.)</span><span class="sxs-lookup"><span data-stu-id="e24d2-111">(This graph uses the Infinite Pin Tee instead of the [Smart Tee](smart-tee-filter.md), because there is no danger of dropping frames when reading from a file, as there is with live capture.)</span></span>
-   <span data-ttu-id="e24d2-112">Der [DV-Splitter](dv-splitter-filter.md) teilt den verschachtelten Stream in einen DV-Videostream, der vom [DV-Video Decoder](dv-video-decoder-filter.md)und einem Audiostream decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="e24d2-112">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream, which is decoded by the [DV Video Decoder](dv-video-decoder-filter.md), and an audio stream.</span></span> <span data-ttu-id="e24d2-113">Beide Streams sind rendererd für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="e24d2-113">Both streams are rendererd for preview.</span></span>

<span data-ttu-id="e24d2-114">Erstellen Sie dieses Diagramm wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e24d2-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  <span data-ttu-id="e24d2-115">Aufrufen von [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) zum Hinzufügen des Quell Filters zum Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="e24d2-115">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add the source filter to the filter graph.</span></span>
2.  <span data-ttu-id="e24d2-116">Erstellen Sie den avi-Splitter und den unbegrenzten Pin-Tee, und fügen Sie Sie dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="e24d2-116">Create the AVI Splitter and the Infinite Pin Tee, and add them to the graph.</span></span>
3.  <span data-ttu-id="e24d2-117">Ruft [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) auf, um den Quell Filter mit dem avi-Splitter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="e24d2-117">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the source filter to the AVI Splitter.</span></span> <span data-ttu-id="e24d2-118">Angeben von MediaType \_ , um sicherzustellen, dass die Methode fehlschlägt, wenn die Quelldatei keine Type-1-DV-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="e24d2-118">Specifying MEDIATYPE\_Interleaved to ensure that the method fails if the source file is not a type-1 DV file.</span></span> <span data-ttu-id="e24d2-119">In diesem Fall können Sie den Typ-2-Übertragungs Graph stattdessen wiederherstellen und versuchen, ein Diagramm vom Typ 2 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e24d2-119">In that case, you can back out and attempt to build a type-2 transmit graph instead.</span></span>
4.  <span data-ttu-id="e24d2-120">**RenderStream** erneut aufgerufen, um den überlappenden Stream vom avi-Splitter an den unbegrenzten Pin-Empfänger weiterzuleiten</span><span class="sxs-lookup"><span data-stu-id="e24d2-120">Call **RenderStream** again to route the interleaved stream from the AVI Splitter to the Infinite Pin Tee</span></span>
5.  <span data-ttu-id="e24d2-121">RenderStream wird ein drittes Mal aufgerufen, um einen Stream vom unbegrenzten Pin-Empfänger an den msdv-Filter für die Übertragung an das Gerät weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="e24d2-121">Call RenderStream a third time to route one stream from the Infinite Pin Tee to the MSDV filter, for transmit to the device.</span></span>
6.  <span data-ttu-id="e24d2-122">**RenderStream** ein letztes Mal aufgerufen, um den Vorschau Abschnitt des Diagramms zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e24d2-122">Call **RenderStream** one last time, to build the preview section of the graph.</span></span>

<span data-ttu-id="e24d2-123">Wenn Sie die Vorschau nicht wünschen, verbinden Sie einfach die Datei Quelle mit dem msdv-Filter:</span><span class="sxs-lookup"><span data-stu-id="e24d2-123">If you do not want preview, simply connect the file source to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="e24d2-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e24d2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e24d2-125">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e24d2-125">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



