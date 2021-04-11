---
description: AVI-Zeichnungs Filter
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: AVI-Zeichnungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123680"
---
# <a name="avi-draw-filter"></a><span data-ttu-id="52e16-103">AVI-Zeichnungs Filter</span><span class="sxs-lookup"><span data-stu-id="52e16-103">AVI Draw Filter</span></span>

<span data-ttu-id="52e16-104">Der AVI-Zeichnungs Filter wird automatisch in ein Wiedergabe Diagramm und nicht in den [AVI-Dekompressor](avi-decompressor-filter.md) gezogen, wenn das Video an einen externen NTSC-Fernsehmonitor ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="52e16-104">The AVI Draw filter is pulled automatically into a playback graph instead of the [AVI Decompressor](avi-decompressor-filter.md) when video is being output to an external NTSC television monitor.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52e16-105">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="52e16-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="52e16-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="52e16-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52e16-107">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="52e16-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="52e16-108">Haupttyp: MEDIATYPE_VideoSubtypes:</span><span class="sxs-lookup"><span data-stu-id="52e16-108">Major Type: MEDIATYPE_VideoSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="52e16-109">MEDIASUBTYPE_MJPG</span><span class="sxs-lookup"><span data-stu-id="52e16-109">MEDIASUBTYPE_MJPG</span></span></li>
<li><span data-ttu-id="52e16-110">MEDIASUBTYPE_TVMJ</span><span class="sxs-lookup"><span data-stu-id="52e16-110">MEDIASUBTYPE_TVMJ</span></span></li>
<li><span data-ttu-id="52e16-111">MEDIASUBTYPE_WAKE</span><span class="sxs-lookup"><span data-stu-id="52e16-111">MEDIASUBTYPE_WAKE</span></span></li>
<li><span data-ttu-id="52e16-112">MEDIASUBTYPE_CFCC</span><span class="sxs-lookup"><span data-stu-id="52e16-112">MEDIASUBTYPE_CFCC</span></span></li>
<li><span data-ttu-id="52e16-113">MEDIASUBTYPE_IJPG</span><span class="sxs-lookup"><span data-stu-id="52e16-113">MEDIASUBTYPE_IJPG</span></span></li>
<li><span data-ttu-id="52e16-114">MEDIASUBTYPE_Plum</span><span class="sxs-lookup"><span data-stu-id="52e16-114">MEDIASUBTYPE_Plum</span></span></li>
<li><span data-ttu-id="52e16-115">MEDIASUBTYPE_DVCS</span><span class="sxs-lookup"><span data-stu-id="52e16-115">MEDIASUBTYPE_DVCS</span></span></li>
<li><span data-ttu-id="52e16-116">MEDIASUBTYPE_DVSD</span><span class="sxs-lookup"><span data-stu-id="52e16-116">MEDIASUBTYPE_DVSD</span></span></li>
<li><span data-ttu-id="52e16-117">MEDIASUBTYPE_MDVF</span><span class="sxs-lookup"><span data-stu-id="52e16-117">MEDIASUBTYPE_MDVF</span></span></li>
<li><span data-ttu-id="52e16-118">Formattyp: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="52e16-118">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52e16-119">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="52e16-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="52e16-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="52e16-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52e16-121">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="52e16-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="52e16-122">MEDIATYPE_Video MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="52e16-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52e16-123">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="52e16-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="52e16-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>ioverlaynotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="52e16-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52e16-125">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="52e16-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="52e16-126">CLSID_AVIDraw</span><span class="sxs-lookup"><span data-stu-id="52e16-126">CLSID_AVIDraw</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52e16-127">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="52e16-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="52e16-128">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="52e16-128">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52e16-129">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="52e16-129">Executable</span></span></td>
<td><span data-ttu-id="52e16-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="52e16-130">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52e16-131"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="52e16-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="52e16-132">MERIT_NORMAL + 100</span><span class="sxs-lookup"><span data-stu-id="52e16-132">MERIT_NORMAL + 100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52e16-133"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="52e16-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="52e16-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="52e16-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="52e16-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52e16-135">Remarks</span></span>

<span data-ttu-id="52e16-136">Da der AVI-Zeichnungs Filter und der [VFW-Erfassungs Filter](vfw-capture-filter.md) beide eine Verbindung mit derselben Hardware herstellen, dürfen Sie sich nicht im selben Filter Diagramm befinden.</span><span class="sxs-lookup"><span data-stu-id="52e16-136">Since the AVI Draw filter and the [VFW Capture Filter](vfw-capture-filter.md) both connect to the same hardware, they cannot be in the same filter graph.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52e16-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52e16-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52e16-138">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="52e16-138">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




