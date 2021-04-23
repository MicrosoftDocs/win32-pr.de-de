---
description: MPEG-2-Demultiplexer-Medientypen
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MPEG-2-Demultiplexer-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909998"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="65edb-103">MPEG-2-Demultiplexer-Medientypen</span><span class="sxs-lookup"><span data-stu-id="65edb-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="65edb-104">Der [MPEG-2-Demultiplexer-Filter](mpeg-2-demultiplexer.md) erkennt die folgenden Medientypen.</span><span class="sxs-lookup"><span data-stu-id="65edb-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="65edb-105">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="65edb-105">Input Types</span></span>

<span data-ttu-id="65edb-106">Der Haupttyp ist immer **MEDIATYPE \_ Stream.**</span><span class="sxs-lookup"><span data-stu-id="65edb-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="65edb-107">Der Untertyp kann einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="65edb-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="65edb-108">GUID</span><span class="sxs-lookup"><span data-stu-id="65edb-108">GUID</span></span>                                             | <span data-ttu-id="65edb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65edb-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65edb-110">**\_KSDATAFORMAT-UNTERTYP \_ BDA \_ \_ MPEG2-TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="65edb-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="65edb-111">Transportstream aus einem BDA-Gerätefilter (Broadcast Driver Architecture).</span><span class="sxs-lookup"><span data-stu-id="65edb-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="65edb-112">Der MPEG-2-Demultiplexer behandelt diesen Untertyp identisch mit **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**.</span><span class="sxs-lookup"><span data-stu-id="65edb-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="65edb-113">**MEDIASUBTYPE \_ \_ MPEG2-PROGRAMM**</span><span class="sxs-lookup"><span data-stu-id="65edb-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="65edb-114">Programmstream</span><span class="sxs-lookup"><span data-stu-id="65edb-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="65edb-115">**MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="65edb-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="65edb-116">Transportstream (TS) mit 188-Byte-Paketen</span><span class="sxs-lookup"><span data-stu-id="65edb-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="65edb-117">**MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT-STRIDE \_**</span><span class="sxs-lookup"><span data-stu-id="65edb-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="65edb-118">Transportstream mit "strided"-Paketen.</span><span class="sxs-lookup"><span data-stu-id="65edb-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="65edb-119">Dieser Untertyp gibt an, dass die TS-Pakete möglicherweise mit zusätzlichen Bytes aufschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="65edb-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="65edb-120">Weitere Informationen finden Sie unter [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="65edb-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="65edb-121">Bei Transportpaketen mit Striding **(MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE)** muss jedes Medienbeispiel eine ganzzahlige Anzahl von Transportpaketen enthalten, wie in [**MPEG2 \_ TRANSPORT \_ STRIDE beschrieben.**](mpeg2-transport-stride.md)</span><span class="sxs-lookup"><span data-stu-id="65edb-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="65edb-122">Für alle anderen Eingabetypen gelten keine Einschränkungen für Beispielgrenzen. Einzelne Pakete können Beispielgrenzen umfassen.</span><span class="sxs-lookup"><span data-stu-id="65edb-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="65edb-123">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="65edb-123">Output Types</span></span>

<span data-ttu-id="65edb-124">Der MPEG-2-Demultiplexer überprüft keine Ausgabetypen. Der Downstreamfilter ist für die Analyse der Daten verantwortlich, die er vom Demultiplexer empfängt.</span><span class="sxs-lookup"><span data-stu-id="65edb-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="65edb-125">Die folgenden Typen werden jedoch häufig von Downstreamfiltern als Ausgabe vom Demultiplexer akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="65edb-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="65edb-126">MPEG-2-Abschnitte</span><span class="sxs-lookup"><span data-stu-id="65edb-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65edb-127">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="65edb-127">Major Type</span></span></td>
<td><span data-ttu-id="65edb-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="65edb-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65edb-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="65edb-129">Subtype</span></span></td>
<td><span data-ttu-id="65edb-130">Einer der folgenden Punkte trifft zu:</span><span class="sxs-lookup"><span data-stu-id="65edb-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="65edb-131"><strong>MEDIASUBTYPE_ATSC_SI:</strong>ATSC-Dienstinformationen.</span><span class="sxs-lookup"><span data-stu-id="65edb-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="65edb-132"><strong>MEDIASUBTYPE_DVB_SI:</strong>WEBDIENST-Dienstinformationen.</span><span class="sxs-lookup"><span data-stu-id="65edb-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="65edb-133"><strong>MEDIASUBTYPE_ISDB_SI:</strong>IsDB-Dienstinformationen (Integrated Services Digital Broadcasting).</span><span class="sxs-lookup"><span data-stu-id="65edb-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="65edb-134"><strong>MEDIASUBTYPE_MPEG2DATA:</strong>MPEG-2-Abschnittsdaten.</span><span class="sxs-lookup"><span data-stu-id="65edb-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65edb-135">Formattyp</span><span class="sxs-lookup"><span data-stu-id="65edb-135">Format Type</span></span></td>
<td><span data-ttu-id="65edb-136">Keine</span><span class="sxs-lookup"><span data-stu-id="65edb-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="65edb-137">MPEG-2-Video</span><span class="sxs-lookup"><span data-stu-id="65edb-137">MPEG-2 Video</span></span>



| <span data-ttu-id="65edb-138">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="65edb-138">Label</span></span> | <span data-ttu-id="65edb-139">Wert</span><span class="sxs-lookup"><span data-stu-id="65edb-139">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="65edb-140">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="65edb-140">Major type</span></span>       | <span data-ttu-id="65edb-141">**\_MEDIATYPE-Video**</span><span class="sxs-lookup"><span data-stu-id="65edb-141">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="65edb-142">Subtype</span><span class="sxs-lookup"><span data-stu-id="65edb-142">Subtype</span></span>          | <span data-ttu-id="65edb-143">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="65edb-143">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="65edb-144">Formattyp</span><span class="sxs-lookup"><span data-stu-id="65edb-144">Format Type</span></span>      | <span data-ttu-id="65edb-145">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="65edb-145">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="65edb-146">Formatstruktur</span><span class="sxs-lookup"><span data-stu-id="65edb-146">Format Structure</span></span> | [<span data-ttu-id="65edb-147">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="65edb-147">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="65edb-148">MPEG-2-Audio</span><span class="sxs-lookup"><span data-stu-id="65edb-148">MPEG-2 Audio</span></span>



| <span data-ttu-id="65edb-149">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="65edb-149">Label</span></span> | <span data-ttu-id="65edb-150">Wert</span><span class="sxs-lookup"><span data-stu-id="65edb-150">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="65edb-151">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="65edb-151">Major type</span></span>       | <span data-ttu-id="65edb-152">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="65edb-152">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="65edb-153">Subtype</span><span class="sxs-lookup"><span data-stu-id="65edb-153">Subtype</span></span>          | <span data-ttu-id="65edb-154">**MEDIASUBTYPE \_ \_ MPEG2-AUDIO**</span><span class="sxs-lookup"><span data-stu-id="65edb-154">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="65edb-155">Formattyp</span><span class="sxs-lookup"><span data-stu-id="65edb-155">Format Type</span></span>      | <span data-ttu-id="65edb-156">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="65edb-156">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="65edb-157">Formatstruktur</span><span class="sxs-lookup"><span data-stu-id="65edb-157">Format Structure</span></span> | <span data-ttu-id="65edb-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65edb-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="65edb-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65edb-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65edb-160">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="65edb-160">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
