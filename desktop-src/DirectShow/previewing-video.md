---
description: In diesem Beispiel wird ein Videovorschaudiagramm mithilfe der ICaptureGraphBuilder2::RenderStream-Methode in DirectShow erstellt.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Videovorschau (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406893"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="20a5b-103">Videovorschau (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="20a5b-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="20a5b-104">Um ein Videovorschaudiagramm zu erstellen, rufen Sie die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="20a5b-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="20a5b-105">In diesem Beispiel wird Folgendes angenommen:</span><span class="sxs-lookup"><span data-stu-id="20a5b-105">This example assumes the following:</span></span>

-   <span data-ttu-id="20a5b-106">*pBuild* wurde initialisiert, wie unter [Informationen zum Capture Graph Builder](about-the-capture-graph-builder.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="20a5b-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="20a5b-107">*pCap* wurde initialisiert, indem eine Instanz des Erfassungsfilters erstellt und dem Filterdiagramm hinzugefügt wurde, wie unter [Auswählen eines Erfassungsgeräts](selecting-a-capture-device.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="20a5b-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="20a5b-108">Der erste Parameter für die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) gibt eine Stecknadelkategorie an. Verwenden Sie für ein Vorschaudiagramm **PIN \_ CATEGORY \_ PREVIEW**.</span><span class="sxs-lookup"><span data-stu-id="20a5b-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="20a5b-109">Der zweite Parameter gibt einen Medientyp als Haupttyp-GUID an.</span><span class="sxs-lookup"><span data-stu-id="20a5b-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="20a5b-110">Verwenden Sie für Videos **MEDIATYPE \_ Video**.</span><span class="sxs-lookup"><span data-stu-id="20a5b-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="20a5b-111">DV-Geräte stellen verschachtelte Audio- und Videodaten bereit, für die der Medientyp **MEDIATYPE \_ Interleaved** lautet.</span><span class="sxs-lookup"><span data-stu-id="20a5b-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="20a5b-112">(Weitere Informationen zur DV-Erfassung finden Sie unter [Digitales Video in DirectShow](digital-video-in-directshow.md).)</span><span class="sxs-lookup"><span data-stu-id="20a5b-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="20a5b-113">Der dritte Parameter ist ein Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Erfassungsfilters.</span><span class="sxs-lookup"><span data-stu-id="20a5b-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="20a5b-114">Die nächsten beiden Parameter sind in diesem Beispiel nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20a5b-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="20a5b-115">Sie werden verwendet, um zusätzliche Filter anzugeben, die möglicherweise zum Rendern des Streams erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="20a5b-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="20a5b-116">Das Festlegen des letzten Parameters auf **NULL** bewirkt, dass der Capture Graph Builder basierend auf dem Medientyp einen Standardrenderer für den Stream auswählt.</span><span class="sxs-lookup"><span data-stu-id="20a5b-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="20a5b-117">Für Videos verwendet der Capture Graph Builder immer den [Videorendererfilter](video-renderer-filter.md) als Standardrenderer.</span><span class="sxs-lookup"><span data-stu-id="20a5b-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="20a5b-118">In Windows XP und höher ist der Video Mixing Renderer (VMR) zwar der Standardvideorenderer für [**IGraphBuilder-Methoden,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) aber nicht der Standardrenderer für die [**RenderStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)</span><span class="sxs-lookup"><span data-stu-id="20a5b-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="20a5b-119">Auf jeder Plattform verwendet der Capture Graph Builder immer den alten Videorendererfilter, sofern Sie nichts anderes angeben.</span><span class="sxs-lookup"><span data-stu-id="20a5b-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="20a5b-120">Obwohl die Stecknadelkategorie als **PIN \_ CATEGORY \_ PREVIEW** angegeben wird, spielt es keine Rolle, ob der Filter tatsächlich über einen Vorschauanschluss verfügt. Es kann sich um einen Videoportanschluss oder nur um einen Erfassungspin handelt.</span><span class="sxs-lookup"><span data-stu-id="20a5b-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="20a5b-121">In beiden Fällen erstellt der Capture Graph Builder automatisch das richtige Diagramm.</span><span class="sxs-lookup"><span data-stu-id="20a5b-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="20a5b-122">Das folgende Diagramm zeigt das einfachste Diagramm für die Videovorschau.</span><span class="sxs-lookup"><span data-stu-id="20a5b-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![Videovorschaudiagramm](images/vidcap01.png)

<span data-ttu-id="20a5b-124">In diesem Diagramm verfügt der Erfassungsfilter über einen Vorschaupin, der eine direkte Verbindung mit dem Videorenderer herstellt.</span><span class="sxs-lookup"><span data-stu-id="20a5b-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="20a5b-125">Wenn der Erfassungsfilter nur über einen Erfassungspin verfügt, fügt der Capture Graph Builder einen [Smart Tee-Filter](smart-tee-filter.md) ein, der den Datenstrom in einen Erfassungsstream und einen Vorschaudatenstrom aufteilt.</span><span class="sxs-lookup"><span data-stu-id="20a5b-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="20a5b-126">Dies wird unter [Kombinieren von Videoaufnahme und Vorschau](combining-video-capture-and-preview.md)ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="20a5b-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="20a5b-127">In einigen Fällen muss der Videostream den Filter Overlay Mixer durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="20a5b-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="20a5b-128">In diesem Falle fügt die [**RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) sie automatisch dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="20a5b-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20a5b-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20a5b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20a5b-130">Kombinieren von Videoaufnahme und Vorschau</span><span class="sxs-lookup"><span data-stu-id="20a5b-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="20a5b-131">Videoaufnahme</span><span class="sxs-lookup"><span data-stu-id="20a5b-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



