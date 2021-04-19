---
description: MPEG-2-Demultiplexer-Medientypen
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MPEG-2-Demultiplexer-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355105"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="6261a-103">MPEG-2-Demultiplexer-Medientypen</span><span class="sxs-lookup"><span data-stu-id="6261a-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="6261a-104">Der [MPEG-2-Demultiplexer-](mpeg-2-demultiplexer.md) Filter erkennt die folgenden Medientypen.</span><span class="sxs-lookup"><span data-stu-id="6261a-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="6261a-105">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="6261a-105">Input Types</span></span>

<span data-ttu-id="6261a-106">Der Haupttyp ist immer **mediaType \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="6261a-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="6261a-107">Der Untertyp kann eine der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="6261a-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="6261a-108">GUID</span><span class="sxs-lookup"><span data-stu-id="6261a-108">GUID</span></span>                                             | <span data-ttu-id="6261a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6261a-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6261a-110">**"Ksdataformat"- \_ Untertyp " \_ BDA" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6261a-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="6261a-111">Transportstream von einem Stream-Geräte Filter (Broadcast Driver Architecture).</span><span class="sxs-lookup"><span data-stu-id="6261a-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="6261a-112">Der MPEG-2-Demultiplexer behandelt diesen Untertyp identisch mit **mediasubtype \_ - \_ Transport**.</span><span class="sxs-lookup"><span data-stu-id="6261a-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="6261a-113">**Mediasubtype \_ - \_ Programm**</span><span class="sxs-lookup"><span data-stu-id="6261a-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="6261a-114">Programmstream</span><span class="sxs-lookup"><span data-stu-id="6261a-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="6261a-115">**Mediasubtype \_ MPEG2- \_ Transport**</span><span class="sxs-lookup"><span data-stu-id="6261a-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="6261a-116">Transport Datenstrom (TS) mit 188-Byte-Paketen</span><span class="sxs-lookup"><span data-stu-id="6261a-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="6261a-117">**Mediasubtype \_ MPEG2- \_ Transport \_ Stride**</span><span class="sxs-lookup"><span data-stu-id="6261a-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="6261a-118">Transportstream mit "stricherten" Paketen.</span><span class="sxs-lookup"><span data-stu-id="6261a-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="6261a-119">Dieser Untertyp gibt an, dass die TS-Pakete mit zusätzlichen Bytes aufgefüllt werden können.</span><span class="sxs-lookup"><span data-stu-id="6261a-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="6261a-120">Weitere Informationen finden Sie unter [**MPEG2- \_ Transport \_ Stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="6261a-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="6261a-121">Für strichlige Transport Pakete (**mediasubtype \_ MPEG2 \_ Transport \_ Stride**) muss jedes Medien Beispiel eine ganzzahlige Anzahl von Transport Paketen enthalten, wie in " [**MPEG2- \_ Transport \_ Stride**](mpeg2-transport-stride.md)" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6261a-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="6261a-122">Für alle anderen Eingabetypen gibt es keine Einschränkungen für die Beispiel Grenzen. einzelne Pakete können Beispiel Grenzen umfassen.</span><span class="sxs-lookup"><span data-stu-id="6261a-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="6261a-123">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="6261a-123">Output Types</span></span>

<span data-ttu-id="6261a-124">Der MPEG-2-Demultiplexer überprüft keine Ausgabetypen. der downstreamfilter ist für die Verarbeitung der Daten, die er vom Demultiplexer empfängt, verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="6261a-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="6261a-125">Die folgenden Typen werden jedoch häufig von downstreamfiltern als Ausgabe des demultiplexers akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6261a-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="6261a-126">MPEG-2-Abschnitte</span><span class="sxs-lookup"><span data-stu-id="6261a-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6261a-127">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="6261a-127">Major Type</span></span></td>
<td><span data-ttu-id="6261a-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="6261a-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6261a-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="6261a-129">Subtype</span></span></td>
<td><span data-ttu-id="6261a-130">Einer der folgenden Punkte trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6261a-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="6261a-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: Informationen zum ATSC-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6261a-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="6261a-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: Informationen zum DVB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6261a-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="6261a-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Informationen zum ISDB-Dienst (Integrated Services Digital Broadcasting).</span><span class="sxs-lookup"><span data-stu-id="6261a-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="6261a-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2-Abschnitts Daten.</span><span class="sxs-lookup"><span data-stu-id="6261a-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6261a-135">Formattyp</span><span class="sxs-lookup"><span data-stu-id="6261a-135">Format Type</span></span></td>
<td><span data-ttu-id="6261a-136">Keine</span><span class="sxs-lookup"><span data-stu-id="6261a-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="6261a-137">MPEG-2-Video</span><span class="sxs-lookup"><span data-stu-id="6261a-137">MPEG-2 Video</span></span>



|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="6261a-138">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="6261a-138">Major type</span></span>       | <span data-ttu-id="6261a-139">**MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="6261a-139">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="6261a-140">Subtype</span><span class="sxs-lookup"><span data-stu-id="6261a-140">Subtype</span></span>          | <span data-ttu-id="6261a-141">**Video zu mediasubtype \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="6261a-141">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="6261a-142">Formattyp</span><span class="sxs-lookup"><span data-stu-id="6261a-142">Format Type</span></span>      | <span data-ttu-id="6261a-143">**MPEG2Video formatieren \_**</span><span class="sxs-lookup"><span data-stu-id="6261a-143">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="6261a-144">Format Struktur</span><span class="sxs-lookup"><span data-stu-id="6261a-144">Format Structure</span></span> | [<span data-ttu-id="6261a-145">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="6261a-145">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="6261a-146">MPEG-2-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="6261a-146">MPEG-2 Audio</span></span>



|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="6261a-147">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="6261a-147">Major type</span></span>       | <span data-ttu-id="6261a-148">**MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="6261a-148">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="6261a-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="6261a-149">Subtype</span></span>          | <span data-ttu-id="6261a-150">**Mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="6261a-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="6261a-151">Formattyp</span><span class="sxs-lookup"><span data-stu-id="6261a-151">Format Type</span></span>      | <span data-ttu-id="6261a-152">**Formatieren von \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="6261a-152">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="6261a-153">Format Struktur</span><span class="sxs-lookup"><span data-stu-id="6261a-153">Format Structure</span></span> | <span data-ttu-id="6261a-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6261a-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6261a-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6261a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6261a-156">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="6261a-156">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
