---
description: AVI-Splitter Filter
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: AVI-Splitter Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125318"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="0e15e-103">AVI-Splitter Filter</span><span class="sxs-lookup"><span data-stu-id="0e15e-103">AVI Splitter Filter</span></span>

<span data-ttu-id="0e15e-104">Der avi-Splitter Filter wird für die Wiedergabe von AVI-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e15e-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="0e15e-105">Sie akzeptiert Daten im AVI-Format und teilt Sie zur weiteren Verarbeitung und/oder zum Rendering in die zugehörigen Datenströme auf.</span><span class="sxs-lookup"><span data-stu-id="0e15e-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e15e-106">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0e15e-106">Filter Interfaces</span></span>                        | <span data-ttu-id="0e15e-107">[**Iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ipersistmediapropertybag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="0e15e-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="0e15e-108">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="0e15e-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="0e15e-109">MediaType \_ Stream, mediasubtype \_ AVI</span><span class="sxs-lookup"><span data-stu-id="0e15e-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="0e15e-110">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="0e15e-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0e15e-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0e15e-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="0e15e-112">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="0e15e-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="0e15e-113">Üblicherweise **mediaType- \_ Video** oder **mediaType \_ -Audiodatei**.</span><span class="sxs-lookup"><span data-stu-id="0e15e-113">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="0e15e-114">Der genaue Typ hängt vom Inhalt der Datei ab, davon, ob die Datei komprimiert ist und welcher Codec verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0e15e-114">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="0e15e-115">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0e15e-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0e15e-116">[**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0e15e-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="0e15e-117">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="0e15e-117">Filter CLSID</span></span>                             | <span data-ttu-id="0e15e-118">CLSID- \_ avisplitter</span><span class="sxs-lookup"><span data-stu-id="0e15e-118">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="0e15e-119">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="0e15e-119">Property Page CLSID</span></span>                      | <span data-ttu-id="0e15e-120">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="0e15e-120">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="0e15e-121">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="0e15e-121">Executable</span></span>                               | <span data-ttu-id="0e15e-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0e15e-122">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="0e15e-123">Verdienst</span><span class="sxs-lookup"><span data-stu-id="0e15e-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="0e15e-124">Verdienst \_ Normal</span><span class="sxs-lookup"><span data-stu-id="0e15e-124">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="0e15e-125">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="0e15e-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0e15e-126">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="0e15e-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="0e15e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e15e-127">Remarks</span></span>

<span data-ttu-id="0e15e-128">Dieser Filter ist in der Regel mit dem asynchronen [Datei Quell](file-source--async--filter.md) Filter in der eingabepin verbunden.</span><span class="sxs-lookup"><span data-stu-id="0e15e-128">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="0e15e-129">Es kann eine Verbindung mit jedem Filter herstellen, dessen Ausgabepin [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) unterstützt und den richtigen Medientyp für die Eingabe-PIN des avi-Splitter Filters anbietet.</span><span class="sxs-lookup"><span data-stu-id="0e15e-129">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="0e15e-130">Die Ausgabe Pins für den avi-Splitter unterstützen die IPropertyBag:: Read-Methode zum Lesen von Eigenschaften aus einzelnen Streams.</span><span class="sxs-lookup"><span data-stu-id="0e15e-130">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="0e15e-131">Derzeit ist die folgende Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="0e15e-131">Currently, the following property is defined.</span></span>



| <span data-ttu-id="0e15e-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0e15e-132">Property</span></span> | <span data-ttu-id="0e15e-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e15e-133">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e15e-134">name</span><span class="sxs-lookup"><span data-stu-id="0e15e-134">name</span></span>     | <span data-ttu-id="0e15e-135">Gibt den Namen des Streams zurück, der aus dem Block `'strn'` in der AVI-Datei entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="0e15e-135">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="0e15e-136">Wenn dieser Block nicht vorhanden ist, gibt die Read-Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="0e15e-136">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="0e15e-137">Die IPropertyBag:: Write-Methode gibt "E Fail" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="0e15e-137">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="0e15e-138">Der [AVI MUX](avi-mux-filter.md) -Filter unterstützt IPropertyBag:: Write zum Speichern von streameigenschaften in einer AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="0e15e-138">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="0e15e-139">Der avi-Splitter gestattet es nicht, dass Downstream-Filter Ihre eigene Zuweisung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e15e-139">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="0e15e-140">Die interanhaltedauer in der Datei bestimmt, wie viel Arbeitsspeicher der avi-Splitter für deren Verarbeitung zuweist.</span><span class="sxs-lookup"><span data-stu-id="0e15e-140">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="0e15e-141">Eine Datei, die in einem Sekunde verschachtelt ist, benötigt viel mehr Arbeitsspeicher als eine Datei, deren Interleave-Dauer auf einen oder zwei Frames festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0e15e-141">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="0e15e-142">Auf modernen Computern ist dies in der Regel kein Problem, es sei denn, Sie führen mehrere Instanzen des avi-Splitter gleichzeitig aus.</span><span class="sxs-lookup"><span data-stu-id="0e15e-142">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="0e15e-143">Diejenigen</span><span class="sxs-lookup"><span data-stu-id="0e15e-143">Seeking</span></span>

<span data-ttu-id="0e15e-144">Wenn die Datei einen Videostream enthält, unterstützt der avi-Splitter das Suchen nach Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="0e15e-144">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="0e15e-145">Um Frame basierte Suche zu aktivieren, rufen Sie [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im [Filter Graph-Manager](filter-graph-manager.md) mit dem Wert **Zeit \_ Format \_ Rahmen** auf.</span><span class="sxs-lookup"><span data-stu-id="0e15e-145">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="0e15e-146">Wenn die Datei einen Audiodatenstrom enthält, unterstützt der avi-Splitter das Suchen nach Stichproben Nummer.</span><span class="sxs-lookup"><span data-stu-id="0e15e-146">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="0e15e-147">Zum Aktivieren der Beispiel basierten Suche wenden Sie [**settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im Filter Graph-Manager mit dem **\_ \_ Beispiel Wert Zeitformat** an.</span><span class="sxs-lookup"><span data-stu-id="0e15e-147">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="0e15e-148">In beiden Fällen muss die Ausgabe-PIN für diesen Datenstrom mit einem rendererfilter verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="0e15e-148">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e15e-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e15e-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e15e-150">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="0e15e-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



