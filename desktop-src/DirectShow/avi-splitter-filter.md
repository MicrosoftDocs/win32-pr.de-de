---
description: AVI-Splitterfilter
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: AVI-Splitterfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909658"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="60958-103">AVI-Splitterfilter</span><span class="sxs-lookup"><span data-stu-id="60958-103">AVI Splitter Filter</span></span>

<span data-ttu-id="60958-104">Der AVI-Splitterfilter wird für die Wiedergabe von AVI-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="60958-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="60958-105">Sie akzeptiert Daten im AVI-Format und teilt sie zur weiteren Verarbeitung und/oder zum Rendern in die konstituierenden Datenströme auf.</span><span class="sxs-lookup"><span data-stu-id="60958-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



| <span data-ttu-id="60958-106">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="60958-106">Label</span></span> | <span data-ttu-id="60958-107">Wert</span><span class="sxs-lookup"><span data-stu-id="60958-107">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60958-108">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="60958-108">Filter Interfaces</span></span>                        | <span data-ttu-id="60958-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="60958-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="60958-110">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="60958-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="60958-111">MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Avi</span><span class="sxs-lookup"><span data-stu-id="60958-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="60958-112">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="60958-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="60958-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="60958-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="60958-114">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="60958-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="60958-115">In der Regel **MEDIATYPE \_ Video** oder **MEDIATYPE \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="60958-115">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="60958-116">Der genaue Typ hängt vom Inhalt der Datei ab, davon, ob die Datei komprimiert ist und welcher Codec verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="60958-116">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="60958-117">Ausgabe-PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="60958-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="60958-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="60958-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="60958-119">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="60958-119">Filter CLSID</span></span>                             | <span data-ttu-id="60958-120">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="60958-120">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="60958-121">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="60958-121">Property Page CLSID</span></span>                      | <span data-ttu-id="60958-122">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="60958-122">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="60958-123">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="60958-123">Executable</span></span>                               | <span data-ttu-id="60958-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="60958-124">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="60958-125">Verdienst</span><span class="sxs-lookup"><span data-stu-id="60958-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="60958-126">NORMALER WERT \_</span><span class="sxs-lookup"><span data-stu-id="60958-126">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="60958-127">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="60958-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="60958-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="60958-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="60958-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60958-129">Remarks</span></span>

<span data-ttu-id="60958-130">Dieser Filter ist in der Regel mit dem Filter [Async File Source (Asynchrone Dateiquelle)](file-source--async--filter.md) auf dem Eingabepin verbunden.</span><span class="sxs-lookup"><span data-stu-id="60958-130">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="60958-131">Er kann eine Verbindung mit jedem Filter herstellen, dessen Ausgabepin [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) unterstützt, und bietet den richtigen Medientyp für den Eingabepin des AVI-Splitterfilters.</span><span class="sxs-lookup"><span data-stu-id="60958-131">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="60958-132">Die Ausgabepins auf dem AVI-Splitter unterstützen die IPropertyBag::Read-Methode zum Lesen von Eigenschaften aus einzelnen Streams.</span><span class="sxs-lookup"><span data-stu-id="60958-132">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="60958-133">Derzeit ist die folgende Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="60958-133">Currently, the following property is defined.</span></span>



| <span data-ttu-id="60958-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="60958-134">Property</span></span> | <span data-ttu-id="60958-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60958-135">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60958-136">name</span><span class="sxs-lookup"><span data-stu-id="60958-136">name</span></span>     | <span data-ttu-id="60958-137">Gibt den Namen des Streams aus dem `'strn'` Block in der AVI-Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="60958-137">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="60958-138">Wenn dieser Block nicht vorhanden ist, gibt die Read-Methode E \_ INVALIDARG zurück.</span><span class="sxs-lookup"><span data-stu-id="60958-138">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="60958-139">Die IPropertyBag::Write-Methode gibt E \_ FAIL zurück.</span><span class="sxs-lookup"><span data-stu-id="60958-139">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="60958-140">Der [AVI Mux-Filter](avi-mux-filter.md) unterstützt IPropertyBag::Write zum Speichern von Streameigenschaften in einer AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="60958-140">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="60958-141">Der AVI-Splitter lässt nicht zu, dass Downstreamfilter einen eigenen Allocator verwenden.</span><span class="sxs-lookup"><span data-stu-id="60958-141">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="60958-142">Die Verschachtelungsdauer in der Datei bestimmt, wie viel Arbeitsspeicher der AVI-Splitter für die Verarbeitung zuweist.</span><span class="sxs-lookup"><span data-stu-id="60958-142">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="60958-143">Eine Datei, die in Blöcken von einer Sekunde überlappend ist, benötigt viel mehr Arbeitsspeicher für die Verarbeitung als eine Datei, deren Verschachtelungsdauer auf ein oder zwei Frames festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60958-143">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="60958-144">Auf modernen Computern ist dies in der Regel kein Problem, es sei denn, Sie führen mehrere Instanzen des AVI-Splitters gleichzeitig aus.</span><span class="sxs-lookup"><span data-stu-id="60958-144">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="60958-145">Suchen</span><span class="sxs-lookup"><span data-stu-id="60958-145">Seeking</span></span>

<span data-ttu-id="60958-146">Wenn die Datei einen Videostream enthält, unterstützt der AVI-Splitter suchweise nach Framenummer.</span><span class="sxs-lookup"><span data-stu-id="60958-146">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="60958-147">Um die framebasierte Suche zu aktivieren, rufen Sie [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im [Filtergraph-Manager](filter-graph-manager.md) mit dem Wert **TIME FORMAT \_ \_ FRAME** auf.</span><span class="sxs-lookup"><span data-stu-id="60958-147">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="60958-148">Wenn die Datei einen Audiodatenstrom enthält, unterstützt der AVI-Splitter Such- nach Beispielnummer.</span><span class="sxs-lookup"><span data-stu-id="60958-148">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="60958-149">Um die beispielbasierte Suche zu aktivieren, rufen [**Sie SetTimeFormat im**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) Filterdiagramm-Manager mit dem Wert **TIME FORMAT SAMPLE \_ \_ auf.**</span><span class="sxs-lookup"><span data-stu-id="60958-149">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="60958-150">In beiden Fällen muss der Ausgabepin für diesen Stream mit einem Rendererfilter verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="60958-150">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60958-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60958-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60958-152">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="60958-152">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



