---
description: MPEG-2-Splitter
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2-Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213959"
---
# <a name="mpeg-2-splitter"></a><span data-ttu-id="90f2f-103">MPEG-2-Splitter</span><span class="sxs-lookup"><span data-stu-id="90f2f-103">MPEG-2 Splitter</span></span>

<span data-ttu-id="90f2f-104">Ab Microsoft® Windows® XP ist der MPEG-2-Splitter Filter veraltet.</span><span class="sxs-lookup"><span data-stu-id="90f2f-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="90f2f-105">Verwenden Sie stattdessen den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="90f2f-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

<span data-ttu-id="90f2f-106">Verwenden Sie auf früheren Plattformen den MPEG-2-Splitter für MPEG-2-Programm Datenströme, die im Pullmodus übermittelt wurden und mindestens einen der folgenden Streamtypen enthalten: MPEG-2-Video; MPEG-2-Audiodatei; Nach Definition für DVD-Video codierte AC3-Audiodaten oder PCM-Audiocodierung gemäß Definition für DVD-Video.</span><span class="sxs-lookup"><span data-stu-id="90f2f-106">On earlier platforms, use the MPEG-2 Splitter for MPEG-2 program streams delivered in pull mode that contain at least one of the following stream types: MPEG-2 video; MPEG-2 audio; AC3 audio encoded as defined for DVD video; or PCM audio encoded as defined for DVD video.</span></span> <span data-ttu-id="90f2f-107">Dieser Filter analysiert die Streams, erstellt eine Ausgabe-PIN für jeden Stream und gibt die komprimierten MPEG-Audiodaten oder Video Pakete an einen MPEG-2-Decoderfilter aus.</span><span class="sxs-lookup"><span data-stu-id="90f2f-107">This filter parses the streams, creates an output pin for each stream, and outputs the compressed MPEG audio or video packets to an MPEG-2 decoder filter.</span></span>

<span data-ttu-id="90f2f-108">Verwenden Sie für Programm-und Transportstreams, die im Pushmodus übermittelt werden, den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md)auf allen Plattformen.</span><span class="sxs-lookup"><span data-stu-id="90f2f-108">For program and transport streams delivered in push-mode, use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md), on all platforms.</span></span>

> [!Note]  
> <span data-ttu-id="90f2f-109">Der MPEG-2-Splitter unterstützt keine Frame genaue Suche.</span><span class="sxs-lookup"><span data-stu-id="90f2f-109">The MPEG-2 Splitter does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90f2f-110">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="90f2f-110">Filter Interfaces</span></span></td>
<td><span data-ttu-id="90f2f-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>iamprose</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>iamstreamselect</strong></a></span><span class="sxs-lookup"><span data-stu-id="90f2f-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90f2f-112">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="90f2f-112">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="90f2f-113">MEDIATYPE_Stream MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="90f2f-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="90f2f-114">MEDIATYPE_Stream MEDIASUBTYPE_MPEG1_Video</span><span class="sxs-lookup"><span data-stu-id="90f2f-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span></span></li>
<li><span data-ttu-id="90f2f-115">MEDIATYPE_Stream MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="90f2f-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90f2f-116">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="90f2f-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="90f2f-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="90f2f-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90f2f-118">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="90f2f-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="90f2f-119">Hängt vom Streamtyp ab.</span><span class="sxs-lookup"><span data-stu-id="90f2f-119">Depends on the stream type.</span></span> <span data-ttu-id="90f2f-120">Siehe <a href="mpeg-2-splitter-media-types.md">MPEG-2-Splitter Medientypen</a></span><span class="sxs-lookup"><span data-stu-id="90f2f-120">See <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90f2f-121">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="90f2f-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="90f2f-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="90f2f-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90f2f-123">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="90f2f-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="90f2f-124">CLSID_MMSPLITTER</span><span class="sxs-lookup"><span data-stu-id="90f2f-124">CLSID_MMSPLITTER</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90f2f-125">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="90f2f-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="90f2f-126">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="90f2f-126">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90f2f-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="90f2f-127">Executable</span></span></td>
<td><span data-ttu-id="90f2f-128">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="90f2f-128">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90f2f-129"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="90f2f-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="90f2f-130">MERIT_NORMAL + 1</span><span class="sxs-lookup"><span data-stu-id="90f2f-130">MERIT_NORMAL + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90f2f-131"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="90f2f-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="90f2f-132">CLSID_AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="90f2f-132">CLSID_AudioInputDeviceCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="90f2f-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90f2f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90f2f-134">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="90f2f-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="90f2f-135">Verwenden des MPEG-2-Splitters</span><span class="sxs-lookup"><span data-stu-id="90f2f-135">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



