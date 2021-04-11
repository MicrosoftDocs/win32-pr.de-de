---
description: QuickTime Movie Parser-Filter
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: QuickTime Movie Parser-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341949"
---
# <a name="quicktime-movie-parser-filter"></a><span data-ttu-id="a623c-103">QuickTime Movie Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="a623c-103">QuickTime Movie Parser Filter</span></span>

<span data-ttu-id="a623c-104">Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="a623c-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="a623c-105">Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a623c-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="a623c-106">Der Filter für den QuickTime-Movie-Parser teilt die Daten von Apple® QuickTime® in Audiodaten und Videostreams.</span><span class="sxs-lookup"><span data-stu-id="a623c-106">The QuickTime Movie Parser filter splits Apple® QuickTime® data into audio and video streams.</span></span> <span data-ttu-id="a623c-107">Es unterstützt QuickTime 2,0 und früher.</span><span class="sxs-lookup"><span data-stu-id="a623c-107">It supports QuickTime 2.0 and earlier.</span></span> <span data-ttu-id="a623c-108">Die Eingabe-PIN stellt eine Verbindung mit einem Quell Filter her, z. b. dem asynchronen [Datei Quell](file-source--async--filter.md) Filter oder dem [URL-Quell](file-source--url--filter.md) Filter.</span><span class="sxs-lookup"><span data-stu-id="a623c-108">The input pin connects to a source filter such as the [Async File Source](file-source--async--filter.md) filter or the [URL File Source](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="a623c-109">Der Parser verwendet den [AVI Decompressor](avi-decompressor-filter.md) -oder [Qt Decompressor](qt-decompressor-filter.md) -Filter, um die QuickTime-Dateien zu dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="a623c-109">The Parser uses the [AVI Decompressor](avi-decompressor-filter.md) or [QT Decompressor](qt-decompressor-filter.md) filter to decompress QuickTime files.</span></span> <span data-ttu-id="a623c-110">Der Filter erstellt eine Ausgabe-PIN für den Videostream und eine Ausgabe-PIN für den Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="a623c-110">The filter creates one output pin for the video stream and one output pin for the audio stream.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a623c-111">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a623c-111">Filter Interfaces</span></span></td>
<td><span data-ttu-id="a623c-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Iammediacontent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="a623c-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a623c-113">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="a623c-113">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="a623c-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span><span class="sxs-lookup"><span data-stu-id="a623c-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a623c-115">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="a623c-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="a623c-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="a623c-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a623c-117">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="a623c-117">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="a623c-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="a623c-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></li>
<li><span data-ttu-id="a623c-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="a623c-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a623c-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a623c-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="a623c-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="a623c-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a623c-122">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="a623c-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="a623c-123">CLSID_QuickTimeParser</span><span class="sxs-lookup"><span data-stu-id="a623c-123">CLSID_QuickTimeParser</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a623c-124">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="a623c-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="a623c-125">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="a623c-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a623c-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="a623c-126">Executable</span></span></td>
<td><span data-ttu-id="a623c-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a623c-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a623c-128"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="a623c-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="a623c-129">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="a623c-129">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a623c-130"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="a623c-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="a623c-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a623c-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a623c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a623c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a623c-133">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="a623c-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



