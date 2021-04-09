---
description: H. 264-Video Typen
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: H. 264-Video Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957704"
---
# <a name="h264-video-types"></a><span data-ttu-id="67f8d-103">H. 264-Video Typen</span><span class="sxs-lookup"><span data-stu-id="67f8d-103">H.264 Video Types</span></span>

<span data-ttu-id="67f8d-104">Die folgenden Medien Untertypen sind für das H. 264-Video definiert.</span><span class="sxs-lookup"><span data-stu-id="67f8d-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="67f8d-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="67f8d-105">Subtype</span></span>                | <span data-ttu-id="67f8d-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="67f8d-106">FOURCC</span></span> | <span data-ttu-id="67f8d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67f8d-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="67f8d-108">**Mediasubtype \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="67f8d-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="67f8d-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="67f8d-109">'AVC1'</span></span> | <span data-ttu-id="67f8d-110">H. 264-Bitstrom ohne Start Codes.</span><span class="sxs-lookup"><span data-stu-id="67f8d-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="67f8d-111">**Mediasubtype \_ H264**</span><span class="sxs-lookup"><span data-stu-id="67f8d-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="67f8d-112">H264</span><span class="sxs-lookup"><span data-stu-id="67f8d-112">'H264'</span></span> | <span data-ttu-id="67f8d-113">H. 264-Bitstrom mit Start Codes.</span><span class="sxs-lookup"><span data-stu-id="67f8d-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="67f8d-114">**Mediasubtype \_ H264**</span><span class="sxs-lookup"><span data-stu-id="67f8d-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="67f8d-115">H264</span><span class="sxs-lookup"><span data-stu-id="67f8d-115">'h264'</span></span> | <span data-ttu-id="67f8d-116">Äquivalent zu **mediasubtype \_ H264** mit einem anderen FourCC.</span><span class="sxs-lookup"><span data-stu-id="67f8d-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="67f8d-117">**Mediasubtype \_ X264**</span><span class="sxs-lookup"><span data-stu-id="67f8d-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="67f8d-118">X264</span><span class="sxs-lookup"><span data-stu-id="67f8d-118">'X264'</span></span> | <span data-ttu-id="67f8d-119">Äquivalent zu **mediasubtype \_ H264** mit einem anderen FourCC.</span><span class="sxs-lookup"><span data-stu-id="67f8d-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="67f8d-120">**Mediasubtype \_ x264**</span><span class="sxs-lookup"><span data-stu-id="67f8d-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="67f8d-121">x264</span><span class="sxs-lookup"><span data-stu-id="67f8d-121">'x264'</span></span> | <span data-ttu-id="67f8d-122">Äquivalent zu **mediasubtype \_ H264** mit einem anderen FourCC.</span><span class="sxs-lookup"><span data-stu-id="67f8d-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="67f8d-123">Diese Untertyp-GUIDs werden in wmcodecdsp. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="67f8d-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="67f8d-124">Der Hauptunterschied zwischen diesen Medientypen besteht darin, dass Start Codes im Bitstream vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="67f8d-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="67f8d-125">Wenn der Untertyp **mediasubtype \_ AVC1** ist, enthält der Bitstrom keine Start Codes.</span><span class="sxs-lookup"><span data-stu-id="67f8d-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="67f8d-126">H. 264-Bitstream mit Start Codes</span><span class="sxs-lookup"><span data-stu-id="67f8d-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="67f8d-127">H. 264-Bitstreams, die per Funk übertragen oder in MPEG-2-oder Transportdaten Strömen enthalten oder auf HD-DVD aufgezeichnet werden, werden wie in Anhang B von ITU-T Rec. H. 264 beschrieben formatiert.</span><span class="sxs-lookup"><span data-stu-id="67f8d-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="67f8d-128">Gemäß dieser Spezifikation besteht der Bitstrom aus einer Sequenz von Einheiten für die Netzwerk Abstraktionsschicht (nalus), denen jeweils ein Startcode vorangestellt ist, der 0x000001 oder 0x00000001 entspricht.</span><span class="sxs-lookup"><span data-stu-id="67f8d-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="67f8d-129">Wenn im Bitstream Start Codes vorhanden sind, wird der folgende Medientyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="67f8d-129">When start codes are present in the bitstream, the following media type is used:</span></span>



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f8d-130">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="67f8d-130">Major type</span></span>  | <span data-ttu-id="67f8d-131">**MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="67f8d-131">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="67f8d-132">Untertypen</span><span class="sxs-lookup"><span data-stu-id="67f8d-132">Subtypes</span></span>    | <span data-ttu-id="67f8d-133">**Mediasubtype \_ H264**, **mediasubtype \_ H264**, **mediasubtype \_ x264** oder **mediasubtype \_ x264**</span><span class="sxs-lookup"><span data-stu-id="67f8d-133">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="67f8d-134">Formattyp</span><span class="sxs-lookup"><span data-stu-id="67f8d-134">Format type</span></span> | <span data-ttu-id="67f8d-135">**Format \_ Videoinfo**, **Format \_ VideoInfo2**, **Format \_ MPEG2Video** oder **GUID \_ null**</span><span class="sxs-lookup"><span data-stu-id="67f8d-135">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="67f8d-136">Wenn der Formattyp " **GUID \_ null**" ist, ist keine Format Struktur vorhanden.</span><span class="sxs-lookup"><span data-stu-id="67f8d-136">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="67f8d-137">Wenn der Bitstrom Start Codes enthält, sind die hier aufgeführten Format Typen ausreichend, da der Decoder keine zusätzlichen Informationen zum Analysieren des Streams benötigt.</span><span class="sxs-lookup"><span data-stu-id="67f8d-137">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="67f8d-138">Der Bitstrom enthält bereits alle Informationen, die vom Decoder benötigt werden, und die Start Codes ermöglichen es dem Decoder, den Start der einzelnen Nalu zu finden.</span><span class="sxs-lookup"><span data-stu-id="67f8d-138">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="67f8d-139">Die folgenden Untertypen sind äquivalent:</span><span class="sxs-lookup"><span data-stu-id="67f8d-139">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="67f8d-140">H. 264-Bitstream ohne Start Codes</span><span class="sxs-lookup"><span data-stu-id="67f8d-140">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="67f8d-141">Das MP4-Containerformat speichert H. 264-Daten ohne Start Codes.</span><span class="sxs-lookup"><span data-stu-id="67f8d-141">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="67f8d-142">Stattdessen wird jedem Nalu ein Längenfeld vorangestellt, das die Länge der Nalu in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="67f8d-142">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="67f8d-143">Die Größe des Längen Felds kann variieren, ist jedoch in der Regel 1, 2 oder 4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="67f8d-143">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="67f8d-144">Wenn keine Start Codes im Bitstream vorhanden sind, wird der folgende Medientyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="67f8d-144">When start codes are not present in the bitstream, the following media type is used.</span></span>



|             |                        |
|-------------|------------------------|
| <span data-ttu-id="67f8d-145">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="67f8d-145">Major type</span></span>  | <span data-ttu-id="67f8d-146">**MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="67f8d-146">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="67f8d-147">Subtype</span><span class="sxs-lookup"><span data-stu-id="67f8d-147">Subtype</span></span>     | <span data-ttu-id="67f8d-148">**Mediasubtype \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="67f8d-148">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="67f8d-149">Formattyp</span><span class="sxs-lookup"><span data-stu-id="67f8d-149">Format type</span></span> | <span data-ttu-id="67f8d-150">**MPEG2Video formatieren \_**</span><span class="sxs-lookup"><span data-stu-id="67f8d-150">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="67f8d-151">Der Format Block ist eine [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="67f8d-151">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="67f8d-152">Diese Struktur sollte wie folgt ausgefüllt werden:</span><span class="sxs-lookup"><span data-stu-id="67f8d-152">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="67f8d-153">**HDR**: eine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur, die den Bitstream beschreibt.</span><span class="sxs-lookup"><span data-stu-id="67f8d-153">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="67f8d-154">Nach dem [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Teil der Struktur ist keine Farbtabelle vorhanden, und **biclrused** muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="67f8d-154">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="67f8d-155">**dwstarttimecode**: wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67f8d-155">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="67f8d-156">Auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="67f8d-156">Set to zero.</span></span>
-   <span data-ttu-id="67f8d-157">**cbsequenceheader**: die Länge des **dwsequenceheader** -Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="67f8d-157">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="67f8d-158">**dwprofile**: gibt das H. 264-Profil an.</span><span class="sxs-lookup"><span data-stu-id="67f8d-158">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="67f8d-159">**dwlevel**: gibt die H. 264-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="67f8d-159">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="67f8d-160">**dwFlags**: die Anzahl von Bytes, die für das Längenfeld verwendet wird, das vor jedem **Nalu** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="67f8d-160">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="67f8d-161">Das Längenfeld gibt die Größe der folgenden Nalu in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="67f8d-161">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="67f8d-162">Wenn **dwFlags** z. b. 4 ist, wird jedem Nalu ein 4-Byte-Längenfeld vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="67f8d-162">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="67f8d-163">Gültige Werte sind 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="67f8d-163">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="67f8d-164">**dwsequenceheader**: ein Bytearray, das Sequence Parameter Set (SPS) und Picture Parameter Set (PPS) nalus enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="67f8d-164">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="67f8d-165">Der MP4-Container enthält möglicherweise Sequenz Parametersätze (SPS) oder Bildparameter Sätze (PPS) als spezielle nal-Einheiten in Datei Headern oder in einem separaten Stream (unterscheidet sich vom Videostream).</span><span class="sxs-lookup"><span data-stu-id="67f8d-165">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="67f8d-166">Wenn das Format festgelegt wird, kann der Medientyp SPS und PPS-nal-Einheiten im **dwsequenceheader** -Array angeben.</span><span class="sxs-lookup"><span data-stu-id="67f8d-166">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="67f8d-167">Wenn **cbsequenceheader** größer als 0 (null) ist, handelt es sich bei **dwsequenceheader** um den Anfang eines Bytearrays, das SPS und PPS nalus enthält, getrennt durch 2-Byte-Längenfelder (Big-Endian).</span><span class="sxs-lookup"><span data-stu-id="67f8d-167">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="67f8d-168">Es ist möglich, sowohl SPS als auch PPS, nur einen dieser Typen oder None zu haben.</span><span class="sxs-lookup"><span data-stu-id="67f8d-168">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="67f8d-169">Der tatsächliche Typ der einzelnen Nalu kann ermittelt werden, indem das Feld " **nal \_ Unit \_ Type** " des Nalu selbst überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="67f8d-169">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="67f8d-170">Wenn dieser Medientyp verwendet wird, beginnt jedes Medien Beispiel am Anfang eines Nalu, und NAL-Einheiten umfassen keine Stichproben.</span><span class="sxs-lookup"><span data-stu-id="67f8d-170">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="67f8d-171">Dadurch kann der Decoder nach Daten Beschädigungen oder gelöschten Beispielen wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="67f8d-171">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



