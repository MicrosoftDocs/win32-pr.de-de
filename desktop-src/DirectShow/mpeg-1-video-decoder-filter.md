---
description: MPEG-1-Video-Decoderfilter
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: MPEG-1-Video-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344777"
---
# <a name="mpeg-1-video-decoder-filter"></a><span data-ttu-id="c7129-103">MPEG-1-Video-Decoderfilter</span><span class="sxs-lookup"><span data-stu-id="c7129-103">MPEG-1 Video Decoder Filter</span></span>

<span data-ttu-id="c7129-104">Decodiert MPEG-1-Video.</span><span class="sxs-lookup"><span data-stu-id="c7129-104">Decodes MPEG-1 video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7129-105">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c7129-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="c7129-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7129-107">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="c7129-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="c7129-108">MEDIATYPE_Video FORMAT_MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="c7129-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span></span><br/> <span data-ttu-id="c7129-109">Die folgenden Untertypen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c7129-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="c7129-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span></span></li>
<li><span data-ttu-id="c7129-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7129-112">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="c7129-112">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="c7129-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7129-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7129-114">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="c7129-114">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="c7129-115">Haupttyp: <strong>MEDIATYPE_Video</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-115">Major type: <strong>MEDIATYPE_Video</strong>,</span></span><br/> <span data-ttu-id="c7129-116">Formattyp: <strong>FORMAT_VideoInfo</strong> oder <strong>FORMAT_VideoInfo2</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-116">Format type: <strong>FORMAT_VideoInfo</strong> or <strong>FORMAT_VideoInfo2</strong></span></span><br/> <span data-ttu-id="c7129-117">Untertypen</span><span class="sxs-lookup"><span data-stu-id="c7129-117">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="c7129-118"><strong>MEDIASUBTYPE_RGB24</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-118"><strong>MEDIASUBTYPE_RGB24</strong></span></span></li>
<li><span data-ttu-id="c7129-119"><strong>MEDIASUBTYPE_RGB32</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-119"><strong>MEDIASUBTYPE_RGB32</strong></span></span></li>
<li><span data-ttu-id="c7129-120"><strong>MEDIASUBTYPE_RGB8</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-120"><strong>MEDIASUBTYPE_RGB8</strong></span></span></li>
<li><span data-ttu-id="c7129-121"><strong>MEDIASUBTYPE_RGB555</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-121"><strong>MEDIASUBTYPE_RGB555</strong></span></span></li>
<li><span data-ttu-id="c7129-122"><strong>MEDIASUBTYPE_RGB565</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-122"><strong>MEDIASUBTYPE_RGB565</strong></span></span></li>
<li><span data-ttu-id="c7129-123"><strong>MEDIASUBTYPE_UYVY</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-123"><strong>MEDIASUBTYPE_UYVY</strong></span></span></li>
<li><span data-ttu-id="c7129-124"><strong>MEDIASUBTYPE_Y41P</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-124"><strong>MEDIASUBTYPE_Y41P</strong></span></span></li>
<li><span data-ttu-id="c7129-125"><strong>MEDIASUBTYPE_YUY2</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-125"><strong>MEDIASUBTYPE_YUY2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7129-126">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c7129-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="c7129-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7129-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7129-128">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="c7129-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="c7129-129"><strong>CLSID_CMpegVideoCodec</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-129"><strong>CLSID_CMpegVideoCodec</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7129-130">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="c7129-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="c7129-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span><span class="sxs-lookup"><span data-stu-id="c7129-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7129-132">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="c7129-132">Executable</span></span></td>
<td><span data-ttu-id="c7129-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c7129-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7129-134"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="c7129-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="c7129-135">0x40000001</span><span class="sxs-lookup"><span data-stu-id="c7129-135">0x40000001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7129-136"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="c7129-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="c7129-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c7129-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c7129-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7129-138">Remarks</span></span>

<span data-ttu-id="c7129-139">Dieser Filter kann in eine DirectDraw-Oberfläche decodieren.</span><span class="sxs-lookup"><span data-stu-id="c7129-139">This filter can decode into a DirectDraw Surface.</span></span> <span data-ttu-id="c7129-140">Der Filter verwendet MMX, wenn der Computer MMX unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7129-140">The filter uses MMX if the machine supports MMX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7129-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7129-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7129-142">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="c7129-142">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




