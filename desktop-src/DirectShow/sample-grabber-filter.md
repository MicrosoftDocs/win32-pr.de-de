---
description: Der Filter Sample Grabber bietet eine Möglichkeit zum Abrufen von Stichproben, wenn sie durch das Filterdiagramm übergeben werden.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Beispielgrabfilter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909668"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="d06f1-103">Beispielgrabfilter</span><span class="sxs-lookup"><span data-stu-id="d06f1-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="d06f1-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d06f1-104">\[Deprecated.</span></span> <span data-ttu-id="d06f1-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="d06f1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d06f1-106">Der Filter Sample Grabber bietet eine Möglichkeit zum Abrufen von Stichproben, wenn sie durch das Filterdiagramm übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d06f1-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="d06f1-107">Es handelt sich um einen Transformationsfilter mit einem Eingabepin und einem Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="d06f1-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="d06f1-108">Alle Stichproben werden unverändert nachgelagert übergibt, sodass Sie sie in ein Filterdiagramm einfügen können, ohne den Datenstrom zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d06f1-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="d06f1-109">Ihre Anwendung kann dann einzelne Beispiele aus dem Filter abrufen, indem sie Methoden auf der [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="d06f1-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="d06f1-110">Wenn Sie Beispiele abrufen möchten, ohne die Daten zu rendern, verbinden Sie den Sample Grabber-Filter mit dem [**Filter NULL-Renderer.**](null-renderer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="d06f1-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



| <span data-ttu-id="d06f1-111">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d06f1-111">Label</span></span> | <span data-ttu-id="d06f1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d06f1-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d06f1-113">Filtern von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d06f1-113">Filter interfaces</span></span>                        | <span data-ttu-id="d06f1-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="d06f1-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="d06f1-115">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d06f1-115">Input pin media types</span></span>                    | <span data-ttu-id="d06f1-116">Ein beliebiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="d06f1-116">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="d06f1-117">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d06f1-117">Input pin interfaces</span></span>                     | <span data-ttu-id="d06f1-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d06f1-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="d06f1-119">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d06f1-119">Output pin media types</span></span>                   | <span data-ttu-id="d06f1-120">Ein beliebiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="d06f1-120">Any media type.</span></span> <span data-ttu-id="d06f1-121">Entspricht dem Eingabemedientyp.</span><span class="sxs-lookup"><span data-stu-id="d06f1-121">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="d06f1-122">Schnittstellen für Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="d06f1-122">Output pin interfaces</span></span>                    | <span data-ttu-id="d06f1-123">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d06f1-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="d06f1-124">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="d06f1-124">Filter CLSID</span></span>                             | <span data-ttu-id="d06f1-125">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="d06f1-125">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="d06f1-126">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="d06f1-126">Property Page CLSID</span></span>                      | <span data-ttu-id="d06f1-127">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="d06f1-127">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="d06f1-128">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="d06f1-128">Executable</span></span>                               | <span data-ttu-id="d06f1-129">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="d06f1-129">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="d06f1-130">Verdienst</span><span class="sxs-lookup"><span data-stu-id="d06f1-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="d06f1-131">NOT USE (NICHT \_ \_ \_ VERWENDEN)</span><span class="sxs-lookup"><span data-stu-id="d06f1-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="d06f1-132">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="d06f1-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d06f1-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="d06f1-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d06f1-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d06f1-134">Remarks</span></span>

<span data-ttu-id="d06f1-135">Um diesen Filter zu verwenden, fügen Sie ihn dem Filterdiagramm hinzu, und rufen [**Sie ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) mit dem gewünschten Medientyp auf.</span><span class="sxs-lookup"><span data-stu-id="d06f1-135">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="d06f1-136">Diese Methode gibt den Medientyp für die Ein- und Ausgabe-PIN-Verbindungen des Filters an.</span><span class="sxs-lookup"><span data-stu-id="d06f1-136">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="d06f1-137">Verbinden Sie den Filter dann mit anderen Filtern im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="d06f1-137">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="d06f1-138">Wenn Sie [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) mit dem Wert **TRUE** aufrufen, puffert der Filter jedes empfangene Beispiel, bevor er es nachgeschaltet übergibt.</span><span class="sxs-lookup"><span data-stu-id="d06f1-138">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="d06f1-139">Rufen Sie die [**ISampleGrabber::GetCurrentBuffer-Methode**](isamplegrabber-getcurrentbuffer.md) auf, um den aktuellen Inhalt des Puffers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d06f1-139">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="d06f1-140">Alternativ können Sie [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) aufrufen, damit der Filter immer dann eine Rückruffunktion aufruft, wenn er ein Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="d06f1-140">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="d06f1-141">Der Filter weist die folgenden Einschränkungen für Videoformate auf:</span><span class="sxs-lookup"><span data-stu-id="d06f1-141">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="d06f1-142">Videotypen mit top-down-Ausrichtung (negative **biHeight)** werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d06f1-142">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="d06f1-143">Die [**Formatstruktur VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) wird nicht unterstützt (Formattyp entspricht **FORMAT \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="d06f1-143">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="d06f1-144">Sie lehnt alle Videotypen ab, bei denen der Oberflächenschritt nicht mit der Videobreite übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d06f1-144">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="d06f1-145">Daher stellt der Sample Grabber für einige Videotypen keine Verbindung mit dem Video Mixing Renderer (VMR) herstellen.</span><span class="sxs-lookup"><span data-stu-id="d06f1-145">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="d06f1-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d06f1-146">Requirements</span></span>



| <span data-ttu-id="d06f1-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d06f1-147">Requirement</span></span> | <span data-ttu-id="d06f1-148">Wert</span><span class="sxs-lookup"><span data-stu-id="d06f1-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d06f1-149">Header</span><span class="sxs-lookup"><span data-stu-id="d06f1-149">Header</span></span><br/> | <dl> <span data-ttu-id="d06f1-150"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="d06f1-150"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d06f1-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d06f1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06f1-152">DirectShow Editing Services Objects</span><span class="sxs-lookup"><span data-stu-id="d06f1-152">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="d06f1-153">Verwenden des Beispielgrabbers</span><span class="sxs-lookup"><span data-stu-id="d06f1-153">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




