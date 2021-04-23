---
description: H.264-Videotypen
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: H.264-Videotypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692a751e197e2e7bbb088b30dd2a3f5f199d56de
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909018"
---
# <a name="h264-video-types"></a><span data-ttu-id="e1f53-103">H.264-Videotypen</span><span class="sxs-lookup"><span data-stu-id="e1f53-103">H.264 Video Types</span></span>

<span data-ttu-id="e1f53-104">Die folgenden Medienuntertypen sind für H.264-Video definiert.</span><span class="sxs-lookup"><span data-stu-id="e1f53-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="e1f53-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="e1f53-105">Subtype</span></span>                | <span data-ttu-id="e1f53-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="e1f53-106">FOURCC</span></span> | <span data-ttu-id="e1f53-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1f53-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="e1f53-108">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="e1f53-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="e1f53-109">"AVC1"</span><span class="sxs-lookup"><span data-stu-id="e1f53-109">'AVC1'</span></span> | <span data-ttu-id="e1f53-110">H.264-Bitstream ohne Startcodes.</span><span class="sxs-lookup"><span data-stu-id="e1f53-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="e1f53-111">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="e1f53-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="e1f53-112">'H264'</span><span class="sxs-lookup"><span data-stu-id="e1f53-112">'H264'</span></span> | <span data-ttu-id="e1f53-113">H.264-Bitstream mit Startcodes.</span><span class="sxs-lookup"><span data-stu-id="e1f53-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="e1f53-114">**MEDIASUBTYPE \_ h264**</span><span class="sxs-lookup"><span data-stu-id="e1f53-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="e1f53-115">'h264'</span><span class="sxs-lookup"><span data-stu-id="e1f53-115">'h264'</span></span> | <span data-ttu-id="e1f53-116">Entspricht **MEDIASUBTYPE \_ H264** mit einem anderen FOURCC.</span><span class="sxs-lookup"><span data-stu-id="e1f53-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="e1f53-117">**MEDIASUBTYPE \_ X264**</span><span class="sxs-lookup"><span data-stu-id="e1f53-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="e1f53-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="e1f53-118">'X264'</span></span> | <span data-ttu-id="e1f53-119">Entspricht **MEDIASUBTYPE \_ H264** mit einem anderen FOURCC.</span><span class="sxs-lookup"><span data-stu-id="e1f53-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="e1f53-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="e1f53-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="e1f53-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="e1f53-121">'x264'</span></span> | <span data-ttu-id="e1f53-122">Entspricht **MEDIASUBTYPE \_ H264** mit einem anderen FOURCC.</span><span class="sxs-lookup"><span data-stu-id="e1f53-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="e1f53-123">Diese Untertyp-GUIDs werden in wmcodecdsp.h deklariert.</span><span class="sxs-lookup"><span data-stu-id="e1f53-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="e1f53-124">Der Hauptunterschied zwischen diesen Medientypen ist das Vorhandensein von Startcodes im Bitstream.</span><span class="sxs-lookup"><span data-stu-id="e1f53-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="e1f53-125">Wenn der Untertyp **MEDIASUBTYPE \_ AVC1 ist,** enthält der Bitstream keine Startcodes.</span><span class="sxs-lookup"><span data-stu-id="e1f53-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="e1f53-126">H.264-Bitstream mit Startcodes</span><span class="sxs-lookup"><span data-stu-id="e1f53-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="e1f53-127">H.264-Bitstreams, die über die Luft übertragen oder in MPEG-2-Programm- oder Transportstreams enthalten oder auf HD-DVD aufgezeichnet werden, sind wie in Anhang B von ITU-T Rec. H.264 beschrieben formatiert.</span><span class="sxs-lookup"><span data-stu-id="e1f53-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="e1f53-128">Gemäß dieser Spezifikation besteht der Bitstream aus einer Sequenz von NALUs (Network Abstraction Layer Units), denen jeweils ein Startcode vorangestellt ist, der 0x000001 oder 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="e1f53-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="e1f53-129">Wenn Startcodes im Bitstream vorhanden sind, wird der folgende Medientyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="e1f53-129">When start codes are present in the bitstream, the following media type is used:</span></span>



| <span data-ttu-id="e1f53-130">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="e1f53-130">Label</span></span> | <span data-ttu-id="e1f53-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e1f53-131">Value</span></span> |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f53-132">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="e1f53-132">Major type</span></span>  | <span data-ttu-id="e1f53-133">**\_MEDIATYPE-Video**</span><span class="sxs-lookup"><span data-stu-id="e1f53-133">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="e1f53-134">Untertypen</span><span class="sxs-lookup"><span data-stu-id="e1f53-134">Subtypes</span></span>    | <span data-ttu-id="e1f53-135">**MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ h264**, **MEDIASUBTYPE \_ X264** oder **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="e1f53-135">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="e1f53-136">Formattyp</span><span class="sxs-lookup"><span data-stu-id="e1f53-136">Format type</span></span> | <span data-ttu-id="e1f53-137">**FORMAT \_ VideoInfo**, **FORMAT \_ VideoInfo2**, **FORMAT \_ MPEG2Video** oder **GUID \_ NULL**</span><span class="sxs-lookup"><span data-stu-id="e1f53-137">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="e1f53-138">Wenn der Formattyp **GUID \_ NULL ist,** ist keine Formatstruktur vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e1f53-138">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="e1f53-139">Wenn der Bitstream Startcodes enthält, ist jeder der hier aufgeführten Formattypen ausreichend, da der Decoder keine zusätzlichen Informationen benötigt, um den Stream zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="e1f53-139">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="e1f53-140">Der Bitstream enthält bereits alle informationen, die vom Decoder benötigt werden, und die Startcodes ermöglichen es dem Decoder, den Anfang jeder N QR zu finden.</span><span class="sxs-lookup"><span data-stu-id="e1f53-140">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="e1f53-141">Die folgenden Untertypen sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="e1f53-141">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="e1f53-142">H.264-Bitstream ohne Startcodes</span><span class="sxs-lookup"><span data-stu-id="e1f53-142">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="e1f53-143">Im MP4-Containerformat werden H.264-Daten ohne Startcodes gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e1f53-143">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="e1f53-144">Stattdessen wird jedem N BYTES ein Längenfeld vorangestellt, das die Länge des N WIES in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="e1f53-144">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="e1f53-145">Die Größe des Längenfelds kann variieren, beträgt jedoch in der Regel 1, 2 oder 4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="e1f53-145">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="e1f53-146">Wenn im Bitstream keine Startcodes vorhanden sind, wird der folgende Medientyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1f53-146">When start codes are not present in the bitstream, the following media type is used.</span></span>



| <span data-ttu-id="e1f53-147">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="e1f53-147">Label</span></span> | <span data-ttu-id="e1f53-148">Wert</span><span class="sxs-lookup"><span data-stu-id="e1f53-148">Value</span></span> |
|-------------|------------------------|
| <span data-ttu-id="e1f53-149">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="e1f53-149">Major type</span></span>  | <span data-ttu-id="e1f53-150">**\_MEDIATYPE-Video**</span><span class="sxs-lookup"><span data-stu-id="e1f53-150">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="e1f53-151">Subtype</span><span class="sxs-lookup"><span data-stu-id="e1f53-151">Subtype</span></span>     | <span data-ttu-id="e1f53-152">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="e1f53-152">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="e1f53-153">Formattyp</span><span class="sxs-lookup"><span data-stu-id="e1f53-153">Format type</span></span> | <span data-ttu-id="e1f53-154">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="e1f53-154">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="e1f53-155">Der Formatblock ist eine [**MPEG2VIDEOINFO-Struktur.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)</span><span class="sxs-lookup"><span data-stu-id="e1f53-155">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="e1f53-156">Diese Struktur sollte wie folgt ausgefüllt werden:</span><span class="sxs-lookup"><span data-stu-id="e1f53-156">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="e1f53-157">**hdr:** Eine [**VIDEOINFOHEADER2-Struktur,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) die den Bitstream beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e1f53-157">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="e1f53-158">Nach dem [**BITMAPINFOHEADER-Teil**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) der Struktur ist keine Farbtabelle vorhanden, und **biClrUsed** muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e1f53-158">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="e1f53-159">**dwStartTimeCode:** Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1f53-159">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="e1f53-160">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="e1f53-160">Set to zero.</span></span>
-   <span data-ttu-id="e1f53-161">**cbSequenceHeader:** Die Länge des **dwSequenceHeader-Arrays** in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e1f53-161">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="e1f53-162">**dwProfile:** Gibt das H.264-Profil an.</span><span class="sxs-lookup"><span data-stu-id="e1f53-162">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="e1f53-163">**dwLevel:** Gibt die H.264-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="e1f53-163">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="e1f53-164">**dwFlags:** Die Anzahl der Bytes, die für das Längenfeld verwendet werden, das vor jeder **NALU** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e1f53-164">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="e1f53-165">Das Feld length gibt die Größe der folgenden NALU in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="e1f53-165">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="e1f53-166">Wenn **dwFlags** beispielsweise 4 ist, wird jeder NALU ein Feld mit einer Länge von 4 Byte vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="e1f53-166">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="e1f53-167">Die gültigen Werte sind 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="e1f53-167">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="e1f53-168">**dwSequenceHeader:** Ein Bytearray, das sequence parameter set (SPS) und picture parameter set (PPS) NALUs enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e1f53-168">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="e1f53-169">Der MP4-Container kann Sequenzparametersätze (Sequence Parameter Sets, SPS) oder Bildparametersätze (Picture Parameter Sets, PPS) als spezielle NAL-Einheiten in Dateiheadern oder in einem separaten Stream (getrennt vom Videostream) enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1f53-169">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="e1f53-170">Wenn das Format festgelegt ist, kann der Medientyp SPS- und PPS-NAL-Einheiten im **dwSequenceHeader-Array** angeben.</span><span class="sxs-lookup"><span data-stu-id="e1f53-170">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="e1f53-171">Wenn **cbSequenceHeader** größer als 0 (null) ist, ist **dwSequenceHeader** der Anfang eines Bytearrays, das SPS- und PPS-NALUs enthält, getrennt durch Felder mit einer Länge von 2 Byte, alle in Netzwerk-Bytereihenfolge (Big-Endian).</span><span class="sxs-lookup"><span data-stu-id="e1f53-171">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="e1f53-172">Es ist möglich, sowohl SPS als auch PPS zu verwenden, nur einen dieser Typen oder keinen.</span><span class="sxs-lookup"><span data-stu-id="e1f53-172">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="e1f53-173">Der tatsächliche Typ der einzelnen N ORGANISATIONSeinheiten kann durch Untersuchen des **Felds für den nal \_ Unit \_ Type** (NAL-Einheitentyp) des N WIES selbst bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="e1f53-173">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="e1f53-174">Wenn dieser Medientyp verwendet wird, beginnt jedes Medienbeispiel am Anfang einer N WIEE, und NAL-Einheiten umfassen keine Stichproben.</span><span class="sxs-lookup"><span data-stu-id="e1f53-174">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="e1f53-175">Dies ermöglicht dem Decoder die Wiederherstellung nach Datenbeschädigungen oder gelöschten Stichproben.</span><span class="sxs-lookup"><span data-stu-id="e1f53-175">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



