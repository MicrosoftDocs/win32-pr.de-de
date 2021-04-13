---
description: DVD-Navigator-Filter
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: DVD-Navigator-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481854"
---
# <a name="dvd-navigator-filter"></a><span data-ttu-id="e5d23-103">DVD-Navigator-Filter</span><span class="sxs-lookup"><span data-stu-id="e5d23-103">DVD Navigator Filter</span></span>

<span data-ttu-id="e5d23-104">Der Filter für den DVD-Navigator ist der Quell Filter für ein DVD-Video Wiedergabe Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="e5d23-104">The DVD Navigator filter is the source filter for a DVD-Video playback filter graph.</span></span> <span data-ttu-id="e5d23-105">Dadurch werden alle erforderlichen Dateien in einem DVD-Video Volume geöffnet, die linearen DVD-Video. VOB-Dateien werden durchlaufen, und der resultierende MPEG-2-Programm Datenstrom wird analysiert, und der Stream wird in drei (Video-, Audio-, subbild-) Ausgabe Pins aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="e5d23-105">It opens all necessary files in a DVD-Video volume, navigates through the linear DVD-Video .vob files, and parses the resulting MPEG-2 program stream, splitting the stream into three (video, audio, subpicture) output pins.</span></span>

<span data-ttu-id="e5d23-106">Der DVD-navigatorfilter implementiert auch die [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Schnittstellen, mit denen eine DVD-Wiedergabe Anwendung die DVD-Video Wiedergabe steuern kann.</span><span class="sxs-lookup"><span data-stu-id="e5d23-106">The DVD Navigator filter also implements the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interfaces that enable a DVD playback application to control DVD-Video playback.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5d23-107">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e5d23-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="e5d23-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-109">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="e5d23-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="e5d23-110">MEDIATYPE_Stream MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="e5d23-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-111">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="e5d23-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="e5d23-112">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e5d23-112">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-113">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="e5d23-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="e5d23-114">Basis Typen:</span><span class="sxs-lookup"><span data-stu-id="e5d23-114">Base types:</span></span><br/>
<ul>
<li><span data-ttu-id="e5d23-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="e5d23-116">Audiodatei <strong></strong>: MEDIATYPE_DVD_ENCRYPTED_PACK <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="e5d23-117">Subbild: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-117">Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="e5d23-118">Erweiterte Typen:</span><span class="sxs-lookup"><span data-stu-id="e5d23-118">Extended types:</span></span><br/> <span data-ttu-id="e5d23-119">Video:</span><span class="sxs-lookup"><span data-stu-id="e5d23-119">Video:</span></span><br/>
<ul>
<li><span data-ttu-id="e5d23-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="e5d23-121"><strong>MEDIATYPE_Video</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="e5d23-122"><strong>MEDIATYPE_MPEG2_PES</strong> <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
</ul>
<span data-ttu-id="e5d23-123">Audio:</span><span class="sxs-lookup"><span data-stu-id="e5d23-123">Audio:</span></span><br/>
<ul>
<li><span data-ttu-id="e5d23-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="e5d23-125"><strong>MEDIATYPE_Audio</strong> <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="e5d23-126"><strong>MEDIATYPE_MPEG2_PES</strong> <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
</ul>
<span data-ttu-id="e5d23-127">Untertitel</span><span class="sxs-lookup"><span data-stu-id="e5d23-127">Subpicture:</span></span><br/>
<ul>
<li><span data-ttu-id="e5d23-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="e5d23-129"><strong>MEDIATYPE_Video</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="e5d23-130"><strong>MEDIATYPE_MPEG2_PES</strong> <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="e5d23-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="e5d23-131">Um die erweiterten Typen zu aktivieren, geben Sie <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2:: SetOption</strong></a> ein, und legen Sie das</span><span class="sxs-lookup"><span data-stu-id="e5d23-131">To enable the extended types, call <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> and set the</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-132">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e5d23-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="e5d23-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5d23-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-134">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="e5d23-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="e5d23-135">CLSID_DVDNavigator</span><span class="sxs-lookup"><span data-stu-id="e5d23-135">CLSID_DVDNavigator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-136">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="e5d23-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="e5d23-137">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="e5d23-137">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-138">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="e5d23-138">Executable</span></span></td>
<td><span data-ttu-id="e5d23-139">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="e5d23-139">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d23-140"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="e5d23-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="e5d23-141">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="e5d23-141">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d23-142"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="e5d23-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="e5d23-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e5d23-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e5d23-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5d23-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d23-145">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="e5d23-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="e5d23-146">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e5d23-146">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




