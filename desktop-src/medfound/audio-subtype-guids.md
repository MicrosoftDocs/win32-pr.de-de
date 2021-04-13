---
description: Audiountertyp-GUIDs
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: Audiountertyp-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484131"
---
# <a name="audio-subtype-guids"></a><span data-ttu-id="0df26-103">Audiountertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="0df26-103">Audio Subtype GUIDs</span></span>

<span data-ttu-id="0df26-104">Die folgenden audiountertyp-GUIDs sind definiert.</span><span class="sxs-lookup"><span data-stu-id="0df26-104">The following audio subtype GUIDs are defined.</span></span> <span data-ttu-id="0df26-105">Um den Untertyp anzugeben, legen Sie das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " für den Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="0df26-105">To specify the subtype, set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="0df26-106">Sofern nicht angegeben, werden diese Konstanten in der Header Datei "mfapi. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="0df26-106">Except where noted, these constants are defined in the header file mfapi.h.</span></span>

<span data-ttu-id="0df26-107">Wenn diese Untertypen verwendet werden, legen Sie das [MF \_ MT- \_ \_ Haupttyp](mf-mt-major-type-attribute.md) Attribut auf **mfmediatype \_ -Audiodaten** fest.</span><span class="sxs-lookup"><span data-stu-id="0df26-107">When these subtypes are used, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0df26-108">GUID</span><span class="sxs-lookup"><span data-stu-id="0df26-108">GUID</span></span></th>
<th><span data-ttu-id="0df26-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0df26-109">Description</span></span></th>
<th><span data-ttu-id="0df26-110">Formattag (FourCC)</span><span class="sxs-lookup"><span data-stu-id="0df26-110">Format Tag (FOURCC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0df26-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span></span></td>
<td><span data-ttu-id="0df26-112">"Advanced audiocoding" (AAC).</span><span class="sxs-lookup"><span data-stu-id="0df26-112">Advanced Audio Coding (AAC).</span></span><br/> <span data-ttu-id="0df26-113">Dieser Untertyp wird für AAC verwendet, der in einer AVI-Datei mit einem audioformattag gleich 0x00FF enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0df26-113">This subtype is used for AAC contained in an AVI file with an audio format tag equal to 0x00FF.</span></span> <br/> <span data-ttu-id="0df26-114">Weitere Informationen finden Sie unter <a href="aac-decoder.md"><strong>AAC-Decoder</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0df26-114">For more information, see <a href="aac-decoder.md"><strong>AAC Decoder</strong></a>.</span></span><br/> <span data-ttu-id="0df26-115">Definiert in "wmcodecdsp. h"</span><span class="sxs-lookup"><span data-stu-id="0df26-115">Defined in wmcodecdsp.h</span></span><br/></td>
<td><span data-ttu-id="0df26-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="0df26-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-117"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-117"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="0df26-118">"Advanced audiocoding" (AAC).</span><span class="sxs-lookup"><span data-stu-id="0df26-118">Advanced Audio Coding (AAC).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0df26-119">Entspricht MEDIASUBTYPE_MPEG_HEAAC, die in wmcodecdsp. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0df26-119">Equivalent to MEDIASUBTYPE_MPEG_HEAAC, defined in wmcodecdsp.h.</span></span>
</blockquote>
<br/> <span data-ttu-id="0df26-120">Der Stream kann unformatierte AAC-Daten oder AAC-Daten in einem Datenstrom (Stream Data Transport Stream, ADTs) enthalten.</span><span class="sxs-lookup"><span data-stu-id="0df26-120">The stream can contain raw AAC data or AAC data in an Audio Data Transport Stream (ADTS) stream.</span></span><br/> <span data-ttu-id="0df26-121">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="0df26-121">For more information, see:</span></span><br/>
<ul>
<li><span data-ttu-id="0df26-122"><a href="aac-decoder.md"><strong>AAC-Decoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="0df26-122"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></li>
<li><span data-ttu-id="0df26-123"><a href="mpeg-4-file-source.md">MPEG-4-Datei Quelle</a></span><span class="sxs-lookup"><span data-stu-id="0df26-123"><a href="mpeg-4-file-source.md">MPEG-4 File Source</a></span></span></li>
</ul></td>
<td><span data-ttu-id="0df26-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span><span class="sxs-lookup"><span data-stu-id="0df26-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-125"><strong>MFAudioFormat_ADTS</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-125"><strong>MFAudioFormat_ADTS</strong></span></span></td>
<td><span data-ttu-id="0df26-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0df26-126">Not used.</span></span></td>
<td><span data-ttu-id="0df26-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span><span class="sxs-lookup"><span data-stu-id="0df26-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-128"><strong>MFAudioFormat_ALAC</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-128"><strong>MFAudioFormat_ALAC</strong></span></span></td>
<td><span data-ttu-id="0df26-129">Apple-Audiocodec ohne Verlust</span><span class="sxs-lookup"><span data-stu-id="0df26-129">Apple Lossless Audio Codec</span></span><br/> <span data-ttu-id="0df26-130">Unterstützt in Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="0df26-130">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="0df26-131">WAVE_FORMAT_ALAC (0x6c61)</span><span class="sxs-lookup"><span data-stu-id="0df26-131">WAVE_FORMAT_ALAC (0x6C61)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-132"><strong>MFAudioFormat_AMR_NB</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-132"><strong>MFAudioFormat_AMR_NB</strong></span></span></td>
<td><span data-ttu-id="0df26-133">Adaptative mehrstufige Audiodaten</span><span class="sxs-lookup"><span data-stu-id="0df26-133">Adaptative Multi-Rate audio</span></span><br/> <span data-ttu-id="0df26-134">Wird in Windows 8.1 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0df26-134">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="0df26-135">WAVE_FORMAT_AMR_NB</span><span class="sxs-lookup"><span data-stu-id="0df26-135">WAVE_FORMAT_AMR_NB</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-136"><strong>MFAudioFormat_AMR_WB</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-136"><strong>MFAudioFormat_AMR_WB</strong></span></span></td>
<td><span data-ttu-id="0df26-137">Adaptative mehrstufige Wideband-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="0df26-137">Adaptative Multi-Rate Wideband audio</span></span><br/> <span data-ttu-id="0df26-138">Wird in Windows 8.1 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0df26-138">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="0df26-139">WAVE_FORMAT_AMR_WB</span><span class="sxs-lookup"><span data-stu-id="0df26-139">WAVE_FORMAT_AMR_WB</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-140"><strong>MFAudioFormat_AMR_WP</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-140"><strong>MFAudioFormat_AMR_WP</strong></span></span></td>
<td><span data-ttu-id="0df26-141">Wird in Windows 8.1 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0df26-141">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="0df26-142">WAVE_FORMAT_AMR_WP</span><span class="sxs-lookup"><span data-stu-id="0df26-142">WAVE_FORMAT_AMR_WP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-143"><strong>MFAudioFormat_Dolby_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-143"><strong>MFAudioFormat_Dolby_AC3</strong></span></span></td>
<td><span data-ttu-id="0df26-144">Dolby Digital (AC-3).</span><span class="sxs-lookup"><span data-stu-id="0df26-144">Dolby Digital (AC-3).</span></span><br/> <span data-ttu-id="0df26-145">Gleicher GUID-Wert wie <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, der in "ksuuids. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0df26-145">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, which is defined in ksuuids.h</span></span><br/></td>
<td><span data-ttu-id="0df26-146">Keine.</span><span class="sxs-lookup"><span data-stu-id="0df26-146">None.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span></span></td>
<td><span data-ttu-id="0df26-148">Dolby AC-3-Audiodatei über Sony/Philips Digital Interface (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="0df26-148">Dolby AC-3 audio over Sony/Philips Digital Interface (S/PDIF).</span></span><br/> <span data-ttu-id="0df26-149">Dieser GUID-Wert ist identisch mit den folgenden Untertypen:</span><span class="sxs-lookup"><span data-stu-id="0df26-149">This GUID value is identical to the following subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="0df26-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>in "ksmedia. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="0df26-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, defined in ksmedia.h.</span></span></li>
<li><span data-ttu-id="0df26-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>in "UUIDs. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="0df26-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, defined in uuids.h.</span></span></li>
</ul></td>
<td><span data-ttu-id="0df26-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span><span class="sxs-lookup"><span data-stu-id="0df26-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span></span></td>
<td><span data-ttu-id="0df26-154">Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="0df26-154">Dolby Digital Plus.</span></span><br/> <span data-ttu-id="0df26-155">Gleicher GUID-Wert wie <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, der in wmcodecdsp. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0df26-155">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, which is defined in wmcodecdsp.h.</span></span><br/></td>
<td><span data-ttu-id="0df26-156">Keine</span><span class="sxs-lookup"><span data-stu-id="0df26-156">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-157"><strong>MFAudioFormat_DRM</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-157"><strong>MFAudioFormat_DRM</strong></span></span></td>
<td><span data-ttu-id="0df26-158">Verschlüsselte Audiodaten, die mit einem sicheren Audiopfad verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0df26-158">Encrypted audio data used with secure audio path.</span></span></td>
<td><span data-ttu-id="0df26-159">WAVE_FORMAT_DRM (0x0009)</span><span class="sxs-lookup"><span data-stu-id="0df26-159">WAVE_FORMAT_DRM (0x0009)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-160"><strong>MFAudioFormat_DTS</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-160"><strong>MFAudioFormat_DTS</strong></span></span></td>
<td><span data-ttu-id="0df26-161">Digital Theater Systems (DTS)-Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="0df26-161">Digital Theater Systems (DTS) audio.</span></span></td>
<td><span data-ttu-id="0df26-162">WAVE_FORMAT_DTS (0x0008)</span><span class="sxs-lookup"><span data-stu-id="0df26-162">WAVE_FORMAT_DTS (0x0008)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-163"><strong>MFAudioFormat_FLAC</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-163"><strong>MFAudioFormat_FLAC</strong></span></span></td>
<td><span data-ttu-id="0df26-164">Kostenloser Audiocodec ohne Verlust</span><span class="sxs-lookup"><span data-stu-id="0df26-164">Free Lossless Audio Codec</span></span><br/> <span data-ttu-id="0df26-165">Unterstützt in Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="0df26-165">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="0df26-166">WAVE_FORMAT_FLAC (0xF 1AC)</span><span class="sxs-lookup"><span data-stu-id="0df26-166">WAVE_FORMAT_FLAC (0xF1AC)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-167"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-167"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="0df26-168">Unkomprimierte IEEE-Gleit Komma-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="0df26-168">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="0df26-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span><span class="sxs-lookup"><span data-stu-id="0df26-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span></span></td>
<td><span data-ttu-id="0df26-171">Unkomprimierte IEEE-Gleit Komma-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="0df26-171">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="0df26-172">Keine</span><span class="sxs-lookup"><span data-stu-id="0df26-172">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-173"><strong>MFAudioFormat_MP3</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-173"><strong>MFAudioFormat_MP3</strong></span></span></td>
<td><span data-ttu-id="0df26-174">MPEG-Audioschicht-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="0df26-174">MPEG Audio Layer-3 (MP3).</span></span></td>
<td><span data-ttu-id="0df26-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span><span class="sxs-lookup"><span data-stu-id="0df26-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-176"><strong>MFAudioFormat_MPEG</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-176"><strong>MFAudioFormat_MPEG</strong></span></span></td>
<td><span data-ttu-id="0df26-177">MPEG-1-audionutzlast.</span><span class="sxs-lookup"><span data-stu-id="0df26-177">MPEG-1 audio payload.</span></span></td>
<td><span data-ttu-id="0df26-178">WAVE_FORMAT_MPEG (0x0050)</span><span class="sxs-lookup"><span data-stu-id="0df26-178">WAVE_FORMAT_MPEG (0x0050)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-179"><strong>MFAudioFormat_MSP1</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-179"><strong>MFAudioFormat_MSP1</strong></span></span></td>
<td><span data-ttu-id="0df26-180">Windows Media Audio 9 Voice-Codec.</span><span class="sxs-lookup"><span data-stu-id="0df26-180">Windows Media Audio 9 Voice codec.</span></span></td>
<td><span data-ttu-id="0df26-181">WAVE_FORMAT_WMAVOICE9 (0x000a)</span><span class="sxs-lookup"><span data-stu-id="0df26-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-182"><strong>MFAudioFormat_Opus</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-182"><strong>MFAudioFormat_Opus</strong></span></span></td>
<td><span data-ttu-id="0df26-183">Opus</span><span class="sxs-lookup"><span data-stu-id="0df26-183">Opus</span></span><br/> <span data-ttu-id="0df26-184">Unterstützt in Windows 10 und höher.</span><span class="sxs-lookup"><span data-stu-id="0df26-184">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="0df26-185">WAVE_FORMAT_OPUS (0x704f)</span><span class="sxs-lookup"><span data-stu-id="0df26-185">WAVE_FORMAT_OPUS (0x704F)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-186"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-186"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="0df26-187">Nicht komprimierte PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="0df26-187">Uncompressed PCM audio.</span></span></td>
<td><span data-ttu-id="0df26-188">WAVE_FORMAT_PCM (1)</span><span class="sxs-lookup"><span data-stu-id="0df26-188">WAVE_FORMAT_PCM (1)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-189"><strong>MFAudioFormat_QCELP</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-189"><strong>MFAudioFormat_QCELP</strong></span></span></td>
<td><span data-ttu-id="0df26-190">QCELP (Qualcomm-Code begeisterte lineare Vorhersage).</span><span class="sxs-lookup"><span data-stu-id="0df26-190">QCELP (Qualcomm Code Excited Linear Prediction) audio.</span></span></td>
<td><span data-ttu-id="0df26-191">Keine</span><span class="sxs-lookup"><span data-stu-id="0df26-191">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-192"><strong>MFAudioFormat_WMASPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-192"><strong>MFAudioFormat_WMASPDIF</strong></span></span></td>
<td><span data-ttu-id="0df26-193">Windows Media Audio 9 Professional-Codec über S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="0df26-193">Windows Media Audio 9 Professional codec over S/PDIF.</span></span></td>
<td><span data-ttu-id="0df26-194">WAVE_FORMAT_WMASPDIF (0x0164)</span><span class="sxs-lookup"><span data-stu-id="0df26-194">WAVE_FORMAT_WMASPDIF (0x0164)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span></span></td>
<td><span data-ttu-id="0df26-196">Windows Media Audio 9 Verlust lose Codec oder Windows Media Audio 9,1-Codec.</span><span class="sxs-lookup"><span data-stu-id="0df26-196">Windows Media Audio 9 Lossless codec or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="0df26-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span><span class="sxs-lookup"><span data-stu-id="0df26-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0df26-198"><strong>MFAudioFormat_WMAudioV8</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-198"><strong>MFAudioFormat_WMAudioV8</strong></span></span></td>
<td><span data-ttu-id="0df26-199">Windows Media Audio 8-Codec, Windows Media Audio 9-Codec oder Windows Media Audio 9,1-Codec.</span><span class="sxs-lookup"><span data-stu-id="0df26-199">Windows Media Audio 8 codec, Windows Media Audio 9 codec, or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="0df26-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span><span class="sxs-lookup"><span data-stu-id="0df26-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0df26-201"><strong>MFAudioFormat_WMAudioV9</strong></span><span class="sxs-lookup"><span data-stu-id="0df26-201"><strong>MFAudioFormat_WMAudioV9</strong></span></span></td>
<td><span data-ttu-id="0df26-202">Windows Media Audio 9 Professional Codec oder Windows Media Audio 9,1 Professional-Codec.</span><span class="sxs-lookup"><span data-stu-id="0df26-202">Windows Media Audio 9 Professional codec or Windows Media Audio 9.1 Professional codec.</span></span></td>
<td><span data-ttu-id="0df26-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span><span class="sxs-lookup"><span data-stu-id="0df26-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0df26-204">Die in der dritten Spalte der Tabelle aufgeführten Formatierungs Tags werden in der **WaveFormatEx** -Struktur verwendet und in der Header Datei mmreg. h definiert.</span><span class="sxs-lookup"><span data-stu-id="0df26-204">The format tags listed in the third column of this table are used in the **WAVEFORMATEX** structure, and are defined in the header file mmreg.h.</span></span>

<span data-ttu-id="0df26-205">Bei Angabe eines audioformattags können Sie eine GUID für einen audiountertyp wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="0df26-205">Given an audio format tag, you can create an audio subtype GUID as follows:</span></span>

1.  <span data-ttu-id="0df26-206">Beginnen Sie mit dem Wert " **MF \_ Audioformat**", der in "mfaph. i" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0df26-206">Start with the value **MFAudioFormat\_Base**, which is defined in mfaph.i.</span></span>
2.  <span data-ttu-id="0df26-207">Ersetzen Sie das erste **DWORD** dieser GUID durch das Formattag.</span><span class="sxs-lookup"><span data-stu-id="0df26-207">Replace the first **DWORD** of this GUID with the format tag.</span></span>

<span data-ttu-id="0df26-208">Sie können das " [**\_ mediaType- \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) "-Makro definieren, um eine neue GUID-Konstante zu definieren, die diesem Muster folgt.</span><span class="sxs-lookup"><span data-stu-id="0df26-208">You can use the [**DEFINE\_MEDIATYPE\_GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) macro to define a new GUID constant that follows this pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0df26-209">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0df26-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df26-210">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="0df26-210">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="0df26-211">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="0df26-211">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="0df26-212">Medientyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="0df26-212">Media Type GUIDs</span></span>](media-type-guids.md)
</dt> <dt>

[<span data-ttu-id="0df26-213">Medientypen</span><span class="sxs-lookup"><span data-stu-id="0df26-213">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




