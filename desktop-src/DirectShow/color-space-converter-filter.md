---
description: Farb Raum Konverter-Filter
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Farb Raum Konverter-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481182"
---
# <a name="color-space-converter-filter"></a><span data-ttu-id="05914-103">Farb Raum Konverter-Filter</span><span class="sxs-lookup"><span data-stu-id="05914-103">Color Space Converter Filter</span></span>

<span data-ttu-id="05914-104">Dieser Transformations Filter konvertiert von einem RGB-Farbtyp in einen anderen RGB-Typ, z. b. zwischen 24-Bit-und 8-Bit-RGB-Farbe.</span><span class="sxs-lookup"><span data-stu-id="05914-104">This transform filter converts from one RGB color type to another RGB type, such as between 24-bit and 8-bit RGB color.</span></span> <span data-ttu-id="05914-105">Da diese Art der Konvertierung in einem Video Dekompressor in der Regel effizienter gehandhabt wird, besteht der Haupt Verwendungsbereich des Farb Raum Konverters darin, dass die Streamquelle aus nicht komprimierten RGB-Frames besteht.</span><span class="sxs-lookup"><span data-stu-id="05914-105">Since this type of conversion is generally handled more efficiently within a video decompressor, the main use of the Color Space Converter is when the stream source consists of uncompressed RGB frames.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05914-106">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="05914-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="05914-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="05914-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05914-108">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="05914-108">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="05914-109">MEDIATYPE_Video FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="05914-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="05914-110">Die folgenden Untertypen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="05914-110">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="05914-111">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="05914-111">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="05914-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="05914-112">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="05914-113">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="05914-113">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="05914-114">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="05914-114">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="05914-115">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="05914-115">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05914-116">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="05914-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="05914-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="05914-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05914-118">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="05914-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="05914-119">MEDIATYPE_Video FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="05914-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="05914-120">Die folgenden Untertypen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="05914-120">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="05914-121">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="05914-121">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="05914-122">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="05914-122">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="05914-123">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="05914-123">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="05914-124">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="05914-124">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="05914-125">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="05914-125">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05914-126">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="05914-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="05914-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="05914-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05914-128">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="05914-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="05914-129">CLSID_Colour</span><span class="sxs-lookup"><span data-stu-id="05914-129">CLSID_Colour</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05914-130">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="05914-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="05914-131">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="05914-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05914-132">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="05914-132">Executable</span></span></td>
<td><span data-ttu-id="05914-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="05914-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05914-134"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="05914-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="05914-135">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="05914-135">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05914-136"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="05914-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="05914-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="05914-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="05914-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05914-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05914-139">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="05914-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




