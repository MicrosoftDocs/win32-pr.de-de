---
description: Filter für Wave-Parser
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filter für Wave-Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369889"
---
# <a name="wave-parser-filter"></a><span data-ttu-id="a249e-103">Filter für Wave-Parser</span><span class="sxs-lookup"><span data-stu-id="a249e-103">WAVE Parser Filter</span></span>

<span data-ttu-id="a249e-104">Der Wave-Parser-Filter analysiert Audiodaten im WAV-Format aus WAV-, au-oder AIF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="a249e-104">The WAVE Parser filter parses WAV-format audio data from .wav, .au, or .aif files.</span></span> <span data-ttu-id="a249e-105">Der upstreamfilter muss der asynchrone [Datei Quell](file-source--async--filter.md) Filter, der [URL-Quell](file-source--url--filter.md) Filter oder ein kompatibler asynchroner Quell Filter eines Drittanbieters sein, der WAV-Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="a249e-105">The upstream filter must be the [Async File Source](file-source--async--filter.md) filter, [URL File Source](file-source--url--filter.md) filter, or a compatible third-party asynchronous source filter that contains WAV audio data.</span></span> <span data-ttu-id="a249e-106">Der Ausgabestream ist Audiodaten, die Sie direkt mit einem audiorenderingfilter oder einem dazwischen liegenden audiotransformations Filter verbinden können.</span><span class="sxs-lookup"><span data-stu-id="a249e-106">The output stream is audio data, which you can connect directly to an audio rendering filter or to an intervening audio transform filter.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a249e-107">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a249e-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="a249e-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Iammediacontent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>ipersistmediapropertybag</strong></a></span><span class="sxs-lookup"><span data-stu-id="a249e-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a249e-109">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="a249e-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="a249e-110">Haupttyp: MEDIATYPE_StreamThe folgenden Untertypen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a249e-110">Major type: MEDIATYPE_StreamThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="a249e-111">MEDIASUBTYPE_AIFF</span><span class="sxs-lookup"><span data-stu-id="a249e-111">MEDIASUBTYPE_AIFF</span></span></li>
<li><span data-ttu-id="a249e-112">MEDIASUBTYPE_AU</span><span class="sxs-lookup"><span data-stu-id="a249e-112">MEDIASUBTYPE_AU</span></span></li>
<li><span data-ttu-id="a249e-113">MEDIASUBTYPE_WAVE</span><span class="sxs-lookup"><span data-stu-id="a249e-113">MEDIASUBTYPE_WAVE</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a249e-114">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="a249e-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="a249e-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="a249e-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a249e-116">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="a249e-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="a249e-117">Haupttyp: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM oder ein anderer Komprimierungstyp.</span><span class="sxs-lookup"><span data-stu-id="a249e-117">Major type: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM or other compression type.</span></span> <span data-ttu-id="a249e-118">(Siehe <a href="audio-subtypes.md"><strong>audiountertypen</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="a249e-118">(See <a href="audio-subtypes.md"><strong>Audio Subtypes</strong></a>.)</span></span><br/> <span data-ttu-id="a249e-119">Formattyp: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="a249e-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a249e-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a249e-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="a249e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="a249e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a249e-122">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="a249e-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="a249e-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span><span class="sxs-lookup"><span data-stu-id="a249e-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a249e-124">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="a249e-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="a249e-125">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="a249e-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a249e-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="a249e-126">Executable</span></span></td>
<td><span data-ttu-id="a249e-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a249e-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a249e-128"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="a249e-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="a249e-129">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="a249e-129">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a249e-130"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="a249e-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="a249e-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a249e-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a249e-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a249e-132">Remarks</span></span>

<span data-ttu-id="a249e-133">Dieser Filter unterstützt die folgenden Dateitypen:</span><span class="sxs-lookup"><span data-stu-id="a249e-133">This filter supports the following file types:</span></span>

-   <span data-ttu-id="a249e-134">Wave (. wav)</span><span class="sxs-lookup"><span data-stu-id="a249e-134">WAVE (.wav)</span></span>
-   <span data-ttu-id="a249e-135">AIFF und AIFF-C (. AIF)</span><span class="sxs-lookup"><span data-stu-id="a249e-135">AIFF and AIFF-C (.aif)</span></span>
-   <span data-ttu-id="a249e-136">Au (. au)</span><span class="sxs-lookup"><span data-stu-id="a249e-136">AU (.au)</span></span>

<span data-ttu-id="a249e-137">Allerdings gelten für das Audioformat die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="a249e-137">However, it has the following limitations on the audio format:</span></span>

-   <span data-ttu-id="a249e-138">Das Audioformat muss ein lineares 8-Bit-oder 16-Bit-PCM sein.</span><span class="sxs-lookup"><span data-stu-id="a249e-138">The audio must be 8-bit or 16-bit linear PCM.</span></span>
-   <span data-ttu-id="a249e-139">Bei AIFF-C-Dateien muss die Audiodatei in der Big-Endian-Byte Reihenfolge (Komprimierungstyp "None") dekomprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="a249e-139">For AIFF-C files, the audio must be uncompressed, in big-endian byte order (compression type 'NONE').</span></span>

## <a name="related-topics"></a><span data-ttu-id="a249e-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a249e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a249e-141">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="a249e-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




