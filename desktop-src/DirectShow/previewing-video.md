---
description: Anzeigen einer Vorschau für Videos
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Anzeigen einer Vorschau für Videos (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568314"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="b2282-103">Anzeigen einer Vorschau für Videos (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b2282-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="b2282-104">Um ein Video Vorschau Diagramm zu erstellen, nennen Sie die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2282-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="b2282-105">In diesem Beispiel wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="b2282-105">This example assumes the following:</span></span>

-   <span data-ttu-id="b2282-106">*Pbuild* wurde initialisiert, wie unter [Informationen zum Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b2282-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="b2282-107">*pcap* wurde initialisiert, indem eine Instanz des Erfassungs Filters erstellt und dem Filter Diagramm hinzugefügt wurde, wie in [Auswählen eines Aufzeichnungs Geräts](selecting-a-capture-device.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b2282-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="b2282-108">Der erste Parameter für die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode gibt eine PIN-Kategorie an. Verwenden Sie für ein Vorschau Diagramm **die \_ Kategorie \_ Vorschau der PIN**.</span><span class="sxs-lookup"><span data-stu-id="b2282-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="b2282-109">Der zweite Parameter gibt einen Medientyp als GUID des Haupt Typs an.</span><span class="sxs-lookup"><span data-stu-id="b2282-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="b2282-110">Verwenden Sie für Video das **\_ Video MediaType**.</span><span class="sxs-lookup"><span data-stu-id="b2282-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="b2282-111">DV-Geräte liefern verschachtelte Audiodaten und Videos, für die der **Medientyp "MediaType \_ überlappende**" ist.</span><span class="sxs-lookup"><span data-stu-id="b2282-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="b2282-112">(Weitere Informationen zur DV-Erfassung finden Sie unter [digitales Video in DirectShow](digital-video-in-directshow.md).)</span><span class="sxs-lookup"><span data-stu-id="b2282-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="b2282-113">Der dritte Parameter ist ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Erfassungs Filters.</span><span class="sxs-lookup"><span data-stu-id="b2282-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="b2282-114">Die folgenden beiden Parameter sind in diesem Beispiel nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2282-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="b2282-115">Sie werden verwendet, um zusätzliche Filter anzugeben, die möglicherweise erforderlich sind, um den Stream zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="b2282-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="b2282-116">Wenn der letzte Parameter auf **null** festgelegt wird, wählt der Erfassungs Diagramm-Generator basierend auf dem Medientyp einen Standardrenderer für den Stream aus.</span><span class="sxs-lookup"><span data-stu-id="b2282-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="b2282-117">Für Video verwendet der Erfassungs Diagramm-Generator immer den [Videorendererfilter](video-renderer-filter.md) als Standardrenderer.</span><span class="sxs-lookup"><span data-stu-id="b2282-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="b2282-118">In Windows XP und höher ist der Video Mischungs-Renderer (VMR) zwar der Standardvideorenderer für [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Methoden, aber er ist nicht der Standardrenderer für die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b2282-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="b2282-119">Auf jeder Plattform verwendet der Erfassungs Diagramm-Generator immer den alten Videorendererfilter, es sei denn, Sie geben andernfalls an.</span><span class="sxs-lookup"><span data-stu-id="b2282-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="b2282-120">Obwohl die PIN-Kategorie als **\_ \_ Vorschau der PIN-Kategorie** angegeben wird, spielt es keine Rolle, ob der Filter tatsächlich über eine Vorschau-Pin verfügt. es kann eine Videoport-PIN oder nur eine Erfassungs-Pin vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b2282-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="b2282-121">In beiden Fällen erstellt der Erfassungs Diagramm-Generator automatisch das richtige Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b2282-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="b2282-122">Das folgende Diagramm zeigt das einfachste mögliche Diagramm für die Vorschau von Videos.</span><span class="sxs-lookup"><span data-stu-id="b2282-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![Video Vorschau Diagramm](images/vidcap01.png)

<span data-ttu-id="b2282-124">In diesem Diagramm hat der Erfassungs Filter eine Vorschau-PIN, die eine direkte Verbindung mit dem Videorenderer herstellt.</span><span class="sxs-lookup"><span data-stu-id="b2282-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="b2282-125">Wenn der Erfassungs Filter nur über eine Erfassungs-Pin verfügt, fügt der Erfassungs Diagramm-Generator einen [intelligenten Tee](smart-tee-filter.md) -Filter ein, der den Stream in einen Erfassungsdaten Strom und einen Vorschau Datenstrom teilt.</span><span class="sxs-lookup"><span data-stu-id="b2282-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="b2282-126">Dies wird unter [Kombinieren von Video Erfassung und Vorschau](combining-video-capture-and-preview.md)ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b2282-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="b2282-127">In einigen Fällen muss der Videostream den Überlagerungs-Mischungs Filter durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b2282-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="b2282-128">Wenn dies der Fall ist, fügt die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode Sie automatisch dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2282-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2282-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2282-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2282-130">Kombinieren von Video Erfassung und Vorschau</span><span class="sxs-lookup"><span data-stu-id="b2282-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="b2282-131">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="b2282-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



