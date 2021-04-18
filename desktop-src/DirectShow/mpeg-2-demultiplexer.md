---
description: Dieser Filter demultiplexes MPEG-2-Transport-und Programmstreams, die im Pushmodus übermittelt werden.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2-Demultiplexer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344326"
---
# <a name="mpeg-2-demultiplexer"></a><span data-ttu-id="b42f8-103">MPEG-2-Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="b42f8-103">MPEG-2 Demultiplexer</span></span>

<span data-ttu-id="b42f8-104">Dieser Filter demultiplexes MPEG-2-Transport-und Programmstreams, die im Pushmodus übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="b42f8-104">This filter demultiplexes MPEG-2 transport and program streams that are delivered in push-mode.</span></span> <span data-ttu-id="b42f8-105">Ab Windows XP unterstützt dieser Filter auch Programmstreams im Pull-Modus (Dateiwiedergabe).</span><span class="sxs-lookup"><span data-stu-id="b42f8-105">Starting in Windows XP, this filter also supports program streams in pull mode (file playback).</span></span> <span data-ttu-id="b42f8-106">Verwenden Sie auf früheren Plattformen den [MPEG-2-Splitter](mpeg-2-splitter.md) Filter für Programmstreams im Pullmodus.</span><span class="sxs-lookup"><span data-stu-id="b42f8-106">On earlier platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter for program streams in pull mode.</span></span> <span data-ttu-id="b42f8-107">Dieser Filter kann in jedem Filter Diagrammtyp verwendet werden, einschließlich eines digitalen Diagramm Diagramms.</span><span class="sxs-lookup"><span data-stu-id="b42f8-107">This filter can be used in any type of filter graph, including a BDA digital TV filter graph.</span></span>

> [!Note]  
> <span data-ttu-id="b42f8-108">Der MPEG-2-Demultiplexer unterstützt keine Frame-exakte Suche.</span><span class="sxs-lookup"><span data-stu-id="b42f8-108">The MPEG-2 Demultiplexer does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b42f8-109">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b42f8-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="b42f8-110">Alle Modi:</span><span class="sxs-lookup"><span data-stu-id="b42f8-110">All modes:</span></span><br/>
<ul>
<li><span data-ttu-id="b42f8-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="b42f8-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="b42f8-112"><strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="b42f8-112"><strong>ISpecifyPropertyPages</strong></span></span></li>
</ul>
<span data-ttu-id="b42f8-113">Nur Pushmodus:</span><span class="sxs-lookup"><span data-stu-id="b42f8-113">Push mode only:</span></span><br/>
<ul>
<li><span data-ttu-id="b42f8-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>Iamfilterfehlflags</strong></a></span><span class="sxs-lookup"><span data-stu-id="b42f8-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="b42f8-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span><span class="sxs-lookup"><span data-stu-id="b42f8-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span></span></li>
<li><span data-ttu-id="b42f8-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="b42f8-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b42f8-117">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="b42f8-117">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="b42f8-118">Haupttyp: MEDIATYPE_STREAM</span><span class="sxs-lookup"><span data-stu-id="b42f8-118">Major type: MEDIATYPE_STREAM</span></span><br/> <span data-ttu-id="b42f8-119">Untertyp</span><span class="sxs-lookup"><span data-stu-id="b42f8-119">Subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="b42f8-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="b42f8-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="b42f8-121">MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="b42f8-121">MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="b42f8-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="b42f8-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="b42f8-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span><span class="sxs-lookup"><span data-stu-id="b42f8-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span></span></li>
</ul>
<span data-ttu-id="b42f8-124">Weitere Informationen finden Sie unter <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer-Medientypen</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b42f8-124">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b42f8-125">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b42f8-125">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="b42f8-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="b42f8-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b42f8-127">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="b42f8-127">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="b42f8-128">Elementare Audiodaten Ströme müssen einen Haupttyp von MEDIATYPE_Audio oder MEDIATYPE_Video haben.</span><span class="sxs-lookup"><span data-stu-id="b42f8-128">Audio and video elementary streams must have a major type of MEDIATYPE_Audio or MEDIATYPE_Video.</span></span><br/> <span data-ttu-id="b42f8-129">Weitere Informationen finden Sie unter <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer-Medientypen</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b42f8-129">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b42f8-130">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b42f8-130">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="b42f8-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, nur <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>-Pushmodus: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>iampushsource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="b42f8-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span></span><br/> <span data-ttu-id="b42f8-132">Nur Pull-Modus: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="b42f8-132">Pull mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b42f8-133">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="b42f8-133">Filter CLSID</span></span></td>
<td><span data-ttu-id="b42f8-134">CLSID_MPEG2Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="b42f8-134">CLSID_MPEG2Demultiplexer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b42f8-135">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="b42f8-135">Property Page CLSID</span></span></td>
<td><span data-ttu-id="b42f8-136">Nur für Testzwecke verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b42f8-136">Available for testing only.</span></span> <span data-ttu-id="b42f8-137">Verwenden der <strong>ISpecifyPropertyPages</strong> -Schnittstelle für den Zugriff auf die Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="b42f8-137">Use the <strong>ISpecifyPropertyPages</strong> interface to access the property pages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b42f8-138">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="b42f8-138">Executable</span></span></td>
<td><span data-ttu-id="b42f8-139">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="b42f8-139">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b42f8-140"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="b42f8-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="b42f8-141">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b42f8-141">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b42f8-142"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="b42f8-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="b42f8-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b42f8-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b42f8-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b42f8-144">Remarks</span></span>

<span data-ttu-id="b42f8-145">Um elementare Audiodaten Ströme auszugeben, muss die Demux die Datenströme PCR und SCR empfangen.</span><span class="sxs-lookup"><span data-stu-id="b42f8-145">To output audio and video elementary streams, the demux must receive the PCR and SCR streams.</span></span> <span data-ttu-id="b42f8-146">Auf der Eingabe Seite bedeutet dies, dass ein Transportstream die Tabellen Pat und PMT enthalten muss, die die PID für den PCR-Stream definieren. und Programm Datenströme müssen mindestens einen Pack-Header enthalten.</span><span class="sxs-lookup"><span data-stu-id="b42f8-146">On the input side, this means a transport stream must contain the PAT and PMT tables that define the PID for the PCR stream; and program streams must contain at least one pack header.</span></span>

## <a name="requirements"></a><span data-ttu-id="b42f8-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b42f8-147">Requirements</span></span>



| <span data-ttu-id="b42f8-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b42f8-148">Requirement</span></span> | <span data-ttu-id="b42f8-149">Wert</span><span class="sxs-lookup"><span data-stu-id="b42f8-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b42f8-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b42f8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b42f8-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b42f8-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b42f8-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b42f8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b42f8-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b42f8-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b42f8-154">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b42f8-154">End of server support</span></span><br/>    | <span data-ttu-id="b42f8-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b42f8-155">Windows Server 2003 R2</span></span><br/>                          |



## <a name="see-also"></a><span data-ttu-id="b42f8-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b42f8-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b42f8-157">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="b42f8-157">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="b42f8-158">Verwenden von MPEG-2 Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="b42f8-158">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




