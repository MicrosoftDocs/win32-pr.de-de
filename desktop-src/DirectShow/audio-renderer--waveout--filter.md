---
description: Filter für audiorenderer (waveout)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filter für audiorenderer (waveout)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346612"
---
# <a name="audio-renderer-waveout-filter"></a><span data-ttu-id="4d2ff-103">Filter für audiorenderer (waveout)</span><span class="sxs-lookup"><span data-stu-id="4d2ff-103">Audio Renderer (WaveOut) Filter</span></span>

<span data-ttu-id="4d2ff-104">Dieser Filter verwendet die waveout \* -API zum Rendering von Wellenform-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="4d2ff-104">This filter uses the waveOut\* API to render waveform audio.</span></span> <span data-ttu-id="4d2ff-105">Der [DirectSound-rendererfilter](directsound-renderer-filter.md) bietet jedoch die gleiche Funktionalität mithilfe von DirectSound.</span><span class="sxs-lookup"><span data-stu-id="4d2ff-105">However, the [DirectSound Renderer Filter](directsound-renderer-filter.md) provides the same functionality using DirectSound.</span></span> <span data-ttu-id="4d2ff-106">Standardmäßig verwendet der Filter Graph-Manager den DirectSound-Renderer anstelle dieses Filters.</span><span class="sxs-lookup"><span data-stu-id="4d2ff-106">By default, the Filter Graph Manager uses the DirectSound Renderer instead of this filter.</span></span> <span data-ttu-id="4d2ff-107">Die Audiomischung ist im waveout-audiorenderer deaktiviert. Wenn Sie also mehrere Audiostreams während der Wiedergabe mischen müssen, verwenden Sie den DirectSound-Renderer.</span><span class="sxs-lookup"><span data-stu-id="4d2ff-107">Audio mixing is disabled in the waveOut Audio Renderer, so if you need to mix multiple audio streams during playback, use the DirectSound renderer.</span></span>

<span data-ttu-id="4d2ff-108">Dieser Filter überprüft den Untertyp des Audiostreams nicht.</span><span class="sxs-lookup"><span data-stu-id="4d2ff-108">This filter does not check the audio stream's subtype.</span></span> <span data-ttu-id="4d2ff-109">Die im Format übergebenen [**wellenformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) -oder [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur enthält die Informationen, die für die Verbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4d2ff-109">The [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure passed in the format contains the information needed for the connection.</span></span>

<span data-ttu-id="4d2ff-110">Dieser Filter unterstützt eine Reihe von Stichproben Raten, die vom Audiotreiber abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="4d2ff-110">This filter supports a range of sample rates that depends on the audio driver.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d2ff-111">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4d2ff-111">Filter Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="4d2ff-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>Iamaudiorendererstats</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>Iamclockslave</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>Iamdirectsound</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>Iamresourcecontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>Ibasicaudiodatei</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-120">IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4d2ff-120">IPersistPropertyBag</span></span></li>
<li><span data-ttu-id="4d2ff-121">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="4d2ff-121">IPersistStream</span></span></li>
<li><span data-ttu-id="4d2ff-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d2ff-124">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="4d2ff-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="4d2ff-125"><strong>MEDIATYPE_Audio</strong></span><span class="sxs-lookup"><span data-stu-id="4d2ff-125"><strong>MEDIATYPE_Audio</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d2ff-126">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="4d2ff-126">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="4d2ff-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="4d2ff-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d2ff-130">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="4d2ff-130">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="4d2ff-131">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="4d2ff-131">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d2ff-132">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4d2ff-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="4d2ff-133">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="4d2ff-133">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d2ff-134">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="4d2ff-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="4d2ff-135"><strong>CLSID_AudioRender</strong></span><span class="sxs-lookup"><span data-stu-id="4d2ff-135"><strong>CLSID_AudioRender</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d2ff-136">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="4d2ff-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="4d2ff-137"><strong>CLSID_AudioProperties</strong> <strong>CLSID_AudioRendererAdvancedProperties</strong></span><span class="sxs-lookup"><span data-stu-id="4d2ff-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d2ff-138">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="4d2ff-138">Executable</span></span></td>
<td><span data-ttu-id="4d2ff-139">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="4d2ff-139">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d2ff-140"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="4d2ff-141"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d2ff-141"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d2ff-142"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="4d2ff-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="4d2ff-143"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d2ff-143"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4d2ff-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d2ff-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d2ff-145">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="4d2ff-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
