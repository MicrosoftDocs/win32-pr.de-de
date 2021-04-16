---
description: Qt-Debug-Filter
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Qt-Debug-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481475"
---
# <a name="qt-decompressor-filter"></a><span data-ttu-id="99871-103">Qt-Debug-Filter</span><span class="sxs-lookup"><span data-stu-id="99871-103">QT Decompressor Filter</span></span>

<span data-ttu-id="99871-104">Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="99871-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="99871-105">Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="99871-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="99871-106">Der Qt-Debug-Filter decomiert Apple® QuickTime® 2,0-Video.</span><span class="sxs-lookup"><span data-stu-id="99871-106">The QT Decompressor filter decompresses Apple® QuickTime® 2.0 video.</span></span> <span data-ttu-id="99871-107">Dieses Format wird in der Regel in älteren QuickTime-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="99871-107">This format is typically used in older QuickTime files.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99871-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="99871-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="99871-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="99871-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99871-110">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="99871-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="99871-111">MEDIATYPE_Video FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="99871-111">MEDIATYPE_Video, FORMAT_VideoInfo</span></span><br/> <span data-ttu-id="99871-112">Die folgenden Untertypen sind gültig:</span><span class="sxs-lookup"><span data-stu-id="99871-112">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="99871-113">MEDIASUBTYPE_QTRpza</span><span class="sxs-lookup"><span data-stu-id="99871-113">MEDIASUBTYPE_QTRpza</span></span></li>
<li><span data-ttu-id="99871-114">MEDIASUBTYPE_QTSmc</span><span class="sxs-lookup"><span data-stu-id="99871-114">MEDIASUBTYPE_QTSmc</span></span></li>
<li><span data-ttu-id="99871-115">MEDIASUBTYPE_QTRle</span><span class="sxs-lookup"><span data-stu-id="99871-115">MEDIASUBTYPE_QTRle</span></span></li>
<li><span data-ttu-id="99871-116">MEDIASUBTYPE_QTJpeg</span><span class="sxs-lookup"><span data-stu-id="99871-116">MEDIASUBTYPE_QTJpeg</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99871-117">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="99871-117">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="99871-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="99871-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99871-119">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="99871-119">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="99871-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="99871-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99871-121">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="99871-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="99871-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="99871-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99871-123">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="99871-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="99871-124">CLSID_QTDec</span><span class="sxs-lookup"><span data-stu-id="99871-124">CLSID_QTDec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99871-125">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="99871-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="99871-126">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="99871-126">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99871-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="99871-127">Executable</span></span></td>
<td><span data-ttu-id="99871-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="99871-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="99871-129"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="99871-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="99871-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="99871-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="99871-131"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="99871-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="99871-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="99871-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="99871-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99871-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99871-134">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="99871-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




