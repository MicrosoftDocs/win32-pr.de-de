---
description: MPEG-1-audiodecoderfilter
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: MPEG-1-audiodecoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f2c68243544a8c6a77cbd8101c85d68f393c3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344180"
---
# <a name="mpeg-1-audio-decoder-filter"></a><span data-ttu-id="f192a-103">MPEG-1-audiodecoderfilter</span><span class="sxs-lookup"><span data-stu-id="f192a-103">MPEG-1 Audio Decoder Filter</span></span>

<span data-ttu-id="f192a-104">Decodiert MPEG-1 Layer I-und Layer II-Audiodaten in PCM.</span><span class="sxs-lookup"><span data-stu-id="f192a-104">Decodes MPEG-1 Layer I and Layer II audio to PCM.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f192a-105">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f192a-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f192a-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="f192a-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f192a-107">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="f192a-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="f192a-108">MEDIATYPE_Audio FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="f192a-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span></span><br/> <span data-ttu-id="f192a-109">Die folgenden Untertypen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f192a-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="f192a-110">MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="f192a-110">MEDIASUBTYPE_MPEG1Packet</span></span></li>
<li><span data-ttu-id="f192a-111">MEDIASUBTYPE_MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="f192a-111">MEDIASUBTYPE_MPEG1Payload</span></span></li>
<li><span data-ttu-id="f192a-112">MEDIASUBTYPE_MPEG1AudioPayload</span><span class="sxs-lookup"><span data-stu-id="f192a-112">MEDIASUBTYPE_MPEG1AudioPayload</span></span></li>
<li><span data-ttu-id="f192a-113">GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="f192a-113">GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f192a-114">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="f192a-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f192a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="f192a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f192a-116">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="f192a-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f192a-117">MEDIATYPE_Audio MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="f192a-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f192a-118">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f192a-118">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f192a-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="f192a-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f192a-120">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="f192a-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="f192a-121">CLSID_CMpegAudioCodec</span><span class="sxs-lookup"><span data-stu-id="f192a-121">CLSID_CMpegAudioCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f192a-122">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="f192a-122">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f192a-123">CLSID_MpegAudioDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="f192a-123">CLSID_MpegAudioDecoderPropertyPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f192a-124">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="f192a-124">Executable</span></span></td>
<td><span data-ttu-id="f192a-125">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f192a-125">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f192a-126"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="f192a-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f192a-127">0x03680001</span><span class="sxs-lookup"><span data-stu-id="f192a-127">0x03680001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f192a-128"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="f192a-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f192a-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f192a-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f192a-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f192a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f192a-131">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="f192a-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




