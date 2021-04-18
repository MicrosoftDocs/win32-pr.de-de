---
description: ACM-Wrapper Filter
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: ACM-Wrapper Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338880"
---
# <a name="acm-wrapper-filter"></a><span data-ttu-id="cbe4e-103">ACM-Wrapper Filter</span><span class="sxs-lookup"><span data-stu-id="cbe4e-103">ACM Wrapper Filter</span></span>

<span data-ttu-id="cbe4e-104">Mit dem ACM-Wrapper Filter können ACM-Codecs (Audiokomprimierungs-Manager) einem Filter Diagramm beitreten.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-104">The ACM Wrapper filter enables Audio Compression Manager (ACM) codecs to join a filter graph.</span></span> <span data-ttu-id="cbe4e-105">Er kann entweder als Filter für die herab Komprimierung oder als Komprimierungs Filter fungieren.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-105">It can act either as a decompression filter or as a compression filter.</span></span>

<span data-ttu-id="cbe4e-106">Als Filter für die Komprimierung wird der ACM-Wrapper in der Kategorie "DirectShow-Filter" (CLSID \_ legacyamfiltercategory) angezeigt, und es ist ein Verdienst des Werts " \_ Normal".</span><span class="sxs-lookup"><span data-stu-id="cbe4e-106">As a decompression filter, the ACM Wrapper appears in the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory) and has a merit of MERIT\_NORMAL.</span></span> <span data-ttu-id="cbe4e-107">Der Typ der Verbindungs Medien in der Eingabe-PIN bestimmt, welcher Codec vom Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-107">The connection media type on the input pin determines which codec the filter uses.</span></span> <span data-ttu-id="cbe4e-108">In der Regel muss die Anwendung dem Filter Diagramm den Filter nicht hinzufügen. Sie wird automatisch vom Filter Graph-Manager abgerufen, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-108">Typically, the application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span> <span data-ttu-id="cbe4e-109">Die Komprimierung erfolgt nur für PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-109">Decompression is only to PCM audio.</span></span>

<span data-ttu-id="cbe4e-110">Als Komprimierungs Filter wird der ACM-Wrapper in der Kategorie "Audio-Kompressoren" (CLSID \_ audiocompressorcategory) angezeigt, und es wird \_ die \_ \_ Nutzung nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-110">As a compression filter, the ACM Wrapper appears in the "Audio Compressors" category (CLSID\_AudioCompressorCategory) and has a merit of MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="cbe4e-111">Jeder Codec wird als separate Instanz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-111">Each codec appears as a separate instance.</span></span> <span data-ttu-id="cbe4e-112">Zur Komprimierung können Sie den Filter nicht direkt mit cokreatanstance erstellen.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-112">For compression, you cannot directly create the filter with CoCreateInstance.</span></span> <span data-ttu-id="cbe4e-113">Stattdessen müssen Sie den Enumerator für Systemgeräte verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-113">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="cbe4e-114">Weitere Informationen finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="cbe4e-114">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cbe4e-115">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cbe4e-115">Filter interfaces</span></span></td>
<td><span data-ttu-id="cbe4e-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, ipersistent, IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cbe4e-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbe4e-117">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="cbe4e-117">Input pin media types</span></span></td>
<td><span data-ttu-id="cbe4e-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="cbe4e-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbe4e-119">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="cbe4e-119">Input pin interfaces</span></span></td>
<td><span data-ttu-id="cbe4e-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="cbe4e-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbe4e-121">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="cbe4e-121">Output pin media types</span></span></td>
<td><span data-ttu-id="cbe4e-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. eine beliebige Kombination der folgenden Möglichkeiten ist möglich:</span><span class="sxs-lookup"><span data-stu-id="cbe4e-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Any combination of the following are possible:</span></span><br/>
<ul>
<li><span data-ttu-id="cbe4e-123">Stichproben pro Sekunde (kHz): 44,1, 22,05, 11,025 oder 8,0.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-123">Samples per second (kHz): 44.1, 22.05, 11.025, or 8.0.</span></span></li>
<li><span data-ttu-id="cbe4e-124">Kanäle: Stereo oder Mono.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-124">Channels: Stereo or mono.</span></span></li>
<li><span data-ttu-id="cbe4e-125">Bits pro Stichprobe: 8 oder 16.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-125">Bits per sample: 8 or 16.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbe4e-126">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cbe4e-126">Output pin interfaces</span></span></td>
<td><span data-ttu-id="cbe4e-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>Iamstreamconfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="cbe4e-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbe4e-128">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="cbe4e-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="cbe4e-129">CLSID_ACMWrapper</span><span class="sxs-lookup"><span data-stu-id="cbe4e-129">CLSID_ACMWrapper</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbe4e-130">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="cbe4e-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="cbe4e-131">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="cbe4e-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbe4e-132">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="cbe4e-132">Executable</span></span></td>
<td><span data-ttu-id="cbe4e-133">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="cbe4e-133">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cbe4e-134"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="cbe4e-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="cbe4e-135">MERIT_NORMAL oder MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="cbe4e-135">MERIT_NORMAL or MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbe4e-136"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="cbe4e-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="cbe4e-137">CLSID_LegacyAmFilterCategory oder CLSID_AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="cbe4e-137">CLSID_LegacyAmFilterCategory or CLSID_AudioCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="cbe4e-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbe4e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbe4e-139">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="cbe4e-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




