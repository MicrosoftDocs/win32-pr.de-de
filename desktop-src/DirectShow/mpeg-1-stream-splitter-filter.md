---
description: MPEG-1-Datenstrom Splitter Filter
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: MPEG-1-Datenstrom Splitter Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125221"
---
# <a name="mpeg-1-stream-splitter-filter"></a><span data-ttu-id="32d9f-103">MPEG-1-Datenstrom Splitter Filter</span><span class="sxs-lookup"><span data-stu-id="32d9f-103">MPEG-1 Stream Splitter Filter</span></span>

<span data-ttu-id="32d9f-104">Dieser Filter teilt einen MPEG-1-Systemdaten Strom in seine komponentenaudiodaten und Videodaten Ströme auf.</span><span class="sxs-lookup"><span data-stu-id="32d9f-104">This filter splits an MPEG-1 system stream into its component audio and video streams.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="32d9f-105">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="32d9f-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="32d9f-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Iammediacontent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>iamstreamselect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="32d9f-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32d9f-107">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="32d9f-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="32d9f-108">Haupttyp: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="32d9f-108">Major type: MEDIATYPE_Stream</span></span><br/> <span data-ttu-id="32d9f-109">Untertypen</span><span class="sxs-lookup"><span data-stu-id="32d9f-109">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="32d9f-110">MEDIASUBTYPE_MPEG1System</span><span class="sxs-lookup"><span data-stu-id="32d9f-110">MEDIASUBTYPE_MPEG1System</span></span></li>
<li><span data-ttu-id="32d9f-111">MEDIASUBTYPE_MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="32d9f-111">MEDIASUBTYPE_MPEG1VideoCD</span></span></li>
<li><span data-ttu-id="32d9f-112">MEDIASUBTYPE_Audio</span><span class="sxs-lookup"><span data-stu-id="32d9f-112">MEDIASUBTYPE_Audio</span></span></li>
<li><span data-ttu-id="32d9f-113">MEDIASUBTYPE_Video</span><span class="sxs-lookup"><span data-stu-id="32d9f-113">MEDIASUBTYPE_Video</span></span></li>
</ul>
<span data-ttu-id="32d9f-114">Siehe <a href="mpeg-1-media-types.md"> <strong>MPEG-1-Medientypen</strong></a></span><span class="sxs-lookup"><span data-stu-id="32d9f-114">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32d9f-115">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="32d9f-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="32d9f-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="32d9f-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32d9f-117">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="32d9f-117">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="32d9f-118">Haupttyp: MEDIATYPE_Audio oder MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="32d9f-118">Major type: MEDIATYPE_Audio or MEDIATYPE_Video</span></span><br/> <span data-ttu-id="32d9f-119">Untertyp: MEDIASUBTYPE_MPEG1Payload oder MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="32d9f-119">Subtype: MEDIASUBTYPE_MPEG1Payload or MEDIASUBTYPE_MPEG1Packet</span></span><br/> <span data-ttu-id="32d9f-120">Siehe <a href="mpeg-1-media-types.md"> <strong>MPEG-1-Medientypen</strong></a></span><span class="sxs-lookup"><span data-stu-id="32d9f-120">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32d9f-121">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="32d9f-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="32d9f-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>imediaseeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="32d9f-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32d9f-123">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="32d9f-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="32d9f-124">CLSID_MPEG1Splitter</span><span class="sxs-lookup"><span data-stu-id="32d9f-124">CLSID_MPEG1Splitter</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32d9f-125">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="32d9f-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="32d9f-126">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="32d9f-126">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32d9f-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="32d9f-127">Executable</span></span></td>
<td><span data-ttu-id="32d9f-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="32d9f-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32d9f-129"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="32d9f-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="32d9f-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="32d9f-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32d9f-131"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="32d9f-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="32d9f-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="32d9f-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="32d9f-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32d9f-133">Remarks</span></span>

<span data-ttu-id="32d9f-134">Diese Datei unterstützt nur den Pull-Modus über [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . der Pushmodus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32d9f-134">This file supports pull mode via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) only; it does not support push mode.</span></span>

<span data-ttu-id="32d9f-135">Da der MPEG-1-Inhalt nicht indiziert ist, kann die Suche sehr ungefähre Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="32d9f-135">Because MPEG-1 content is not indexed, seeking can be very approximate.</span></span> <span data-ttu-id="32d9f-136">Es ist in der Regel gut für einen MPEG-1-Systemdaten Strom mit fester Bitrate (in der Regel Hardware, die für Video-CD generiert wird).</span><span class="sxs-lookup"><span data-stu-id="32d9f-136">It is usually good for a fixed bitrate MPEG-1 system stream (which is usually hardware generated for video CD).</span></span>

<span data-ttu-id="32d9f-137">Der Filter unterstützt die [**iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) -Schnittstelle zum Abrufen von ID3-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="32d9f-137">The filter supports the [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) interface for retrieving ID3 metadata.</span></span>

<span data-ttu-id="32d9f-138">Nicht alle MPEG-Beispiele haben Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="32d9f-138">Not all MPEG samples have time stamps.</span></span> <span data-ttu-id="32d9f-139">Das Fehlen eines Zeitstempels in einem MPEG-Beispiel ist kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="32d9f-139">The lack of a time stamp on an MPEG sample is not an error.</span></span> <span data-ttu-id="32d9f-140">Für Filter Entwickler bedeutet dies, dass Sie keinen Fehlercode aus der **Receive** -Methode der Eingabe-PIN zurückgeben sollten, wenn [**imediasample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="32d9f-140">For filter developers, this means that you should not return an error code from your input pin's **Receive** method if [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fails.</span></span> <span data-ttu-id="32d9f-141">Wenn **Receive** einen anderen Wert als S OK zurückgibt \_ , bewirkt dies, dass der Splitter das Senden von Beispielen beendet.</span><span class="sxs-lookup"><span data-stu-id="32d9f-141">If **Receive** returns any value other than S\_OK, it will cause the splitter to stop sending samples.</span></span>

<span data-ttu-id="32d9f-142">Wenn die Datei einen Videostream enthält, unterstützt der MPEG-1-Datenstrom Splitter das Suchen nach Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="32d9f-142">If the file contains a video stream, the MPEG-1 Stream Splitter supports seeking by frame number.</span></span> <span data-ttu-id="32d9f-143">Um Frame basierte Suche zu aktivieren, rufen Sie [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im [Filter Graph-Manager](filter-graph-manager.md) mit dem Wert **Zeit \_ Format \_ Rahmen** auf.</span><span class="sxs-lookup"><span data-stu-id="32d9f-143">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32d9f-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32d9f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32d9f-145">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="32d9f-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




