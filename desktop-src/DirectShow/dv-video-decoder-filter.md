---
description: DV-Video-Decoderfilter
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: DV-Video-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520464"
---
# <a name="dv-video-decoder-filter"></a><span data-ttu-id="42182-103">DV-Video-Decoderfilter</span><span class="sxs-lookup"><span data-stu-id="42182-103">DV Video Decoder Filter</span></span>

<span data-ttu-id="42182-104">Mit diesem Filter wird ein Digital Video-Stream (DV) in ein unkomprimiertes Video decodiert.</span><span class="sxs-lookup"><span data-stu-id="42182-104">This filter decodes a digital video (DV) stream into uncompressed video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42182-105">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="42182-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="42182-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>iipdvdec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="42182-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42182-107">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="42182-107">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="42182-108">MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="42182-108">MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="42182-109">MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="42182-109">MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="42182-110">FORMAT_VideoInfo FORMAT_DvInfo</span><span class="sxs-lookup"><span data-stu-id="42182-110">FORMAT_VideoInfo, FORMAT_DvInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42182-111">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="42182-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="42182-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="42182-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42182-113">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="42182-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="42182-114"><strong>Haupttyp</strong>: MEDIATYPE_Video<strong>Untertypen</strong>:</span><span class="sxs-lookup"><span data-stu-id="42182-114"><strong>Major type</strong>: MEDIATYPE_Video<strong>Subtypes</strong>:</span></span><br/>
<ul>
<li><span data-ttu-id="42182-115">MEDIASUBTYPE_YUY2</span><span class="sxs-lookup"><span data-stu-id="42182-115">MEDIASUBTYPE_YUY2</span></span></li>
<li><span data-ttu-id="42182-116">MEDIASUBTYPE_UYVY</span><span class="sxs-lookup"><span data-stu-id="42182-116">MEDIASUBTYPE_UYVY</span></span></li>
<li><span data-ttu-id="42182-117">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="42182-117">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="42182-118">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="42182-118">MEDIASUBTYPE_RGB32</span></span></li>
<li><span data-ttu-id="42182-119">MEDIASUBTYPE_ARGB32</span><span class="sxs-lookup"><span data-stu-id="42182-119">MEDIASUBTYPE_ARGB32</span></span></li>
<li><span data-ttu-id="42182-120">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="42182-120">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="42182-121">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="42182-121">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="42182-122">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="42182-122">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="42182-123">MEDIASUBTYPE_Y41P</span><span class="sxs-lookup"><span data-stu-id="42182-123">MEDIASUBTYPE_Y41P</span></span></li>
</ul><span data-ttu-id="42182-124">
<strong>Format Typen</strong>:</span><span class="sxs-lookup"><span data-stu-id="42182-124">
<strong>Format types</strong>:</span></span><br/> <span data-ttu-id="42182-125">Format_VideoInfo Format_VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="42182-125">Format_VideoInfo, Format_VideoInfo2</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42182-126">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="42182-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="42182-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="42182-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42182-128">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="42182-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="42182-129">CLSID_DVVideoCodec</span><span class="sxs-lookup"><span data-stu-id="42182-129">CLSID_DVVideoCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42182-130">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="42182-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="42182-131">CLSID_DVDecPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="42182-131">CLSID_DVDecPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42182-132">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="42182-132">Executable</span></span></td>
<td><span data-ttu-id="42182-133">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="42182-133">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42182-134"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="42182-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="42182-135">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42182-135">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42182-136"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="42182-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="42182-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="42182-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="42182-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42182-138">Remarks</span></span>

<span data-ttu-id="42182-139">Verwenden Sie die [**iipdvdec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) -Schnittstelle, um die Decodierungs Auflösung auf Full, halbsize, Quarter Size oder One-achte zu setzen.</span><span class="sxs-lookup"><span data-stu-id="42182-139">Use the [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) interface to set the decoding resolution to full, half size, quarter size, or one-eighth size.</span></span>

<span data-ttu-id="42182-140">**Interlacing**: in früheren Versionen des Decoders ist das Video immer Deinterlacing.</span><span class="sxs-lookup"><span data-stu-id="42182-140">**Interlacing**: Earlier versions of the decoder always deinterlace the video.</span></span> <span data-ttu-id="42182-141">Ab DirectX 9,0 kann der DV-Video Decoder das Interlacing beibehalten.</span><span class="sxs-lookup"><span data-stu-id="42182-141">As of DirectX 9.0, the DV Video Decoder can preserve the interlacing.</span></span> <span data-ttu-id="42182-142">Dadurch kann das Zeilen Sprung Video durch den Video Mischungs-Renderer (VMR) deinstalgt werden, um die renderingqualität zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="42182-142">This enables the interlaced video to be deinterlaced by the Video Mixing Renderer (VMR), for improved rendering quality.</span></span> <span data-ttu-id="42182-143">Um dieses Feature verwenden zu können, muss der downstreamfilter [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formate unterstützen, die durch das Wert Format \_ VideoInfo2 im **Format Type** -Member der [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur "am" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="42182-143">To use this feature, the downstream filter must support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, indicated by that value Format\_VideoInfo2 in the **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="42182-144">Bei der Ausgabe der vollständigen Auflösung werden die Deinterlacing-Flags (**dwinterlace**) in der **VIDEOINFOHEADER2** -Struktur auf festgelegt `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , was Zeilen Sprung Felder angibt.</span><span class="sxs-lookup"><span data-stu-id="42182-144">At full resolution output, the deinterlacing flags (**dwInterlace**) in the **VIDEOINFOHEADER2** structure are set to `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave`, indicating interlaced fields.</span></span> <span data-ttu-id="42182-145">Bei der Hälfte der Auflösung oder bei einem niedrigeren Wert ist **dwinterlace** auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42182-145">At half resolution or lower, **dwInterlace** is set to zero, indicating progressive frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42182-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="42182-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42182-147">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="42182-147">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="42182-148">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="42182-148">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




