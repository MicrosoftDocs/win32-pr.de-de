---
description: Der Sample Grabber-Filter bietet eine Möglichkeit zum Abrufen von Beispielen beim Durchlaufen des Filter Diagramms.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Beispiel für einen Grabber Filter (qedit. h)
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
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368303"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="dea6c-103">Beispiel für einen Grabber Filter</span><span class="sxs-lookup"><span data-stu-id="dea6c-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="dea6c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="dea6c-104">\[Deprecated.</span></span> <span data-ttu-id="dea6c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="dea6c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dea6c-106">Der Sample Grabber-Filter bietet eine Möglichkeit zum Abrufen von Beispielen beim Durchlaufen des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="dea6c-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="dea6c-107">Es handelt sich um einen Transformations Filter mit einer Eingabe-und einer Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="dea6c-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="dea6c-108">Alle Beispiele bleiben unverändert, sodass Sie Sie in ein Filter Diagramm einfügen können, ohne den Datenstream zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dea6c-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="dea6c-109">Die Anwendung kann dann einzelne Beispiele aus dem Filter abrufen, indem Sie Methoden für die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dea6c-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="dea6c-110">Wenn Sie Beispiele abrufen möchten, ohne die Daten zu rendern, verbinden Sie den Sample Grabber Filter mit dem Filter [**null-Renderer**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="dea6c-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea6c-111">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dea6c-111">Filter interfaces</span></span>                        | <span data-ttu-id="dea6c-112">[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **isamplegrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="dea6c-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="dea6c-113">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="dea6c-113">Input pin media types</span></span>                    | <span data-ttu-id="dea6c-114">Ein beliebiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="dea6c-114">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="dea6c-115">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="dea6c-115">Input pin interfaces</span></span>                     | <span data-ttu-id="dea6c-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="dea6c-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="dea6c-117">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="dea6c-117">Output pin media types</span></span>                   | <span data-ttu-id="dea6c-118">Ein beliebiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="dea6c-118">Any media type.</span></span> <span data-ttu-id="dea6c-119">Entspricht dem Eingabe Medientyp.</span><span class="sxs-lookup"><span data-stu-id="dea6c-119">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="dea6c-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dea6c-120">Output pin interfaces</span></span>                    | <span data-ttu-id="dea6c-121">[**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="dea6c-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="dea6c-122">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="dea6c-122">Filter CLSID</span></span>                             | <span data-ttu-id="dea6c-123">CLSID- \_ samplegrabber</span><span class="sxs-lookup"><span data-stu-id="dea6c-123">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="dea6c-124">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="dea6c-124">Property Page CLSID</span></span>                      | <span data-ttu-id="dea6c-125">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="dea6c-125">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="dea6c-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="dea6c-126">Executable</span></span>                               | <span data-ttu-id="dea6c-127">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="dea6c-127">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="dea6c-128">Verdienst</span><span class="sxs-lookup"><span data-stu-id="dea6c-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="dea6c-129">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="dea6c-129">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="dea6c-130">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="dea6c-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="dea6c-131">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="dea6c-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="dea6c-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dea6c-132">Remarks</span></span>

<span data-ttu-id="dea6c-133">Wenn Sie diesen Filter verwenden möchten, fügen Sie ihn dem Filter Diagramm hinzu, und nennen Sie [**isamplegrabber:: setmediatype**](isamplegrabber-setmediatype.md) mit dem gewünschten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="dea6c-133">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="dea6c-134">Diese Methode gibt den Medientyp für die Eingabe-und Ausgabe-PIN-Verbindungen des Filters an.</span><span class="sxs-lookup"><span data-stu-id="dea6c-134">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="dea6c-135">Verbinden Sie den Filter dann mit anderen Filtern im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="dea6c-135">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="dea6c-136">Wenn Sie [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md) mit dem Wert **true** aufrufen, puffert der Filter jedes empfangene Beispiel, bevor es nach unten übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="dea6c-136">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="dea6c-137">Rufen Sie die [**isamplegrabber:: getcurrentbuffer**](isamplegrabber-getcurrentbuffer.md) -Methode auf, um den aktuellen Inhalt des Puffers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dea6c-137">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="dea6c-138">Alternativ können Sie [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md) aufrufen, damit der Filter immer dann eine Rückruffunktion aufruft, wenn er ein Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="dea6c-138">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="dea6c-139">Für den Filter gelten die folgenden Einschränkungen für Videoformate:</span><span class="sxs-lookup"><span data-stu-id="dea6c-139">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="dea6c-140">Video Typen mit der Top-Down-Ausrichtung (negative **biheight**) werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dea6c-140">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="dea6c-141">Die [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format Struktur (formatType entspricht **Format \_ VideoInfo2**) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dea6c-141">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="dea6c-142">Alle Videotypen, bei denen der Surface-Stride nicht mit der Video Breite identisch ist, werden abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="dea6c-142">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="dea6c-143">Folglich stellt der Sample Grabber für einige Video Typen keine Verbindung mit dem Video Mischungs-Renderer (VMR) her.</span><span class="sxs-lookup"><span data-stu-id="dea6c-143">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea6c-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dea6c-144">Requirements</span></span>



| <span data-ttu-id="dea6c-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dea6c-145">Requirement</span></span> | <span data-ttu-id="dea6c-146">Wert</span><span class="sxs-lookup"><span data-stu-id="dea6c-146">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dea6c-147">Header</span><span class="sxs-lookup"><span data-stu-id="dea6c-147">Header</span></span><br/> | <dl> <span data-ttu-id="dea6c-148"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dea6c-148"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea6c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dea6c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea6c-150">DirectShow-Bearbeitungs Dienste-Objekte</span><span class="sxs-lookup"><span data-stu-id="dea6c-150">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="dea6c-151">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="dea6c-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




