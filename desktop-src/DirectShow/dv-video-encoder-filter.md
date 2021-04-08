---
description: DV-Video Encoder-Filter
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: DV-Video Encoder-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957762"
---
# <a name="dv-video-encoder-filter"></a><span data-ttu-id="8e9c0-103">DV-Video Encoder-Filter</span><span class="sxs-lookup"><span data-stu-id="8e9c0-103">DV Video Encoder Filter</span></span>

<span data-ttu-id="8e9c0-104">Mit diesem Filter wird ein unkomprimierter Videostream in ein digitales Video (DV) codiert.</span><span class="sxs-lookup"><span data-stu-id="8e9c0-104">This filter encodes an uncompressed video stream into digital video (DV).</span></span> <span data-ttu-id="8e9c0-105">Sie stellt eine benutzerdefinierte Schnittstelle ( [**idvenc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)) zum Festlegen der Codierungs Auflösung und des Codierungs Formats bereit.</span><span class="sxs-lookup"><span data-stu-id="8e9c0-105">It provides a custom interface, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), for setting the encoding resolution and format.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e9c0-106">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8e9c0-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="8e9c0-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>idvenc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="8e9c0-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9c0-108">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="8e9c0-108">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="8e9c0-109">Haupttyp: MEDIATYPE_VideoThe folgenden Untertypen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8e9c0-109">Major type: MEDIATYPE_VideoThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="8e9c0-110">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="8e9c0-110">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="8e9c0-111">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="8e9c0-111">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="8e9c0-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="8e9c0-112">MEDIASUBTYPE_RGB555</span></span></li>
</ul></li>
<li><span data-ttu-id="8e9c0-113">Formattyp: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="8e9c0-113">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e9c0-114">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="8e9c0-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="8e9c0-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e9c0-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9c0-116">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="8e9c0-116">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="8e9c0-117">Haupttyp: MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="8e9c0-117">Major type: MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="8e9c0-118">Untertyp: MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="8e9c0-118">Subtype: MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="8e9c0-119">Formattyp: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="8e9c0-119">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e9c0-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8e9c0-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="8e9c0-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e9c0-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9c0-122">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="8e9c0-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="8e9c0-123">CLSID_DVVideoEnc</span><span class="sxs-lookup"><span data-stu-id="8e9c0-123">CLSID_DVVideoEnc</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e9c0-124">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="8e9c0-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="8e9c0-125">CLSID_DVEncPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="8e9c0-125">CLSID_DVEncPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9c0-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="8e9c0-126">Executable</span></span></td>
<td><span data-ttu-id="8e9c0-127">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="8e9c0-127">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e9c0-128"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="8e9c0-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="8e9c0-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="8e9c0-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9c0-130"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="8e9c0-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="8e9c0-131">CLSID_VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="8e9c0-131">CLSID_VideoCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8e9c0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e9c0-132">Remarks</span></span>

<span data-ttu-id="8e9c0-133">Bei einem 16-Bit-Video (mediasubtype \_ RGB555 oder mediasubtype \_ RGB565) müssen die Eingaben 720 x 480 Pixel für NTSC oder 720 x 576 Pixel für PAL lauten.</span><span class="sxs-lookup"><span data-stu-id="8e9c0-133">For 16-bit video (MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565), the input must be 720 x 480 pixels for NTSC, or 720 x 576 pixels for PAL.</span></span> <span data-ttu-id="8e9c0-134">Bei 24-Bit-Videos gibt es keine Größenbeschränkungen für die Eingabe.</span><span class="sxs-lookup"><span data-stu-id="8e9c0-134">For 24-bit video, there are no size constraints on the input.</span></span>

<span data-ttu-id="8e9c0-135">Die Ausgabe lautet immer 720 x 480 für NTSC oder 720 x 576 für PAL; 24-Bit-Video wird so skaliert, dass diese Dimensionen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="8e9c0-135">The output is always 720 x 480 for NTSC or 720 x 576 for PAL; 24-bit video is scaled to fit these dimensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e9c0-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e9c0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e9c0-137">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="8e9c0-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="8e9c0-138">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8e9c0-138">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




