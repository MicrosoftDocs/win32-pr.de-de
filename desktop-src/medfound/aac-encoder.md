---
description: Der Microsoft Media Foundation AAC-Encoder ist eine Media Foundation Transformation, mit der das von ISO/IEC 13818-7 (MPEG-2-Audioteil 7) definierte LC-Profil (Advanced audiocoding (AAC) Low Komplexitäts Profil codiert wird.
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: AAC-Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862756"
---
# <a name="aac-encoder"></a><span data-ttu-id="bf382-103">AAC-Encoder</span><span class="sxs-lookup"><span data-stu-id="bf382-103">AAC Encoder</span></span>

<span data-ttu-id="bf382-104">Der Microsoft Media Foundation AAC-Encoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , mit der das von ISO/IEC 13818-7 (MPEG-2-Audioteil 7) definierte LC-Profil (Advanced audiocoding (AAC) Low Komplexitäts Profil codiert wird.</span><span class="sxs-lookup"><span data-stu-id="bf382-104">The Microsoft Media Foundation AAC encoder is a [Media Foundation Transform](media-foundation-transforms.md) that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile, as defined by ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .</span></span>

<span data-ttu-id="bf382-105">Der AAC-Encoder unterstützt keine Codierung zu anderen AAC-Profilen, wie z. b. Main, SSR oder LTP.</span><span class="sxs-lookup"><span data-stu-id="bf382-105">The AAC encoder does not support encoding to any other AAC profiles, such as Main, SSR, or LTP.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="bf382-106">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="bf382-106">Class Identifier</span></span>

<span data-ttu-id="bf382-107">Der Klassen Bezeichner (CLSID) des AAC-Encoders ist **CLSID \_ aacmscoder**, der in der Header Datei "wmcodecdsp. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bf382-107">The class identifier (CLSID) of the AAC encoder is **CLSID\_AACMFTEncoder**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="bf382-108">Medientypen</span><span class="sxs-lookup"><span data-stu-id="bf382-108">Media Types</span></span>

<span data-ttu-id="bf382-109">Der AAC-Encoder unterstützt die folgenden Medientypen.</span><span class="sxs-lookup"><span data-stu-id="bf382-109">The AAC encoder supports the following media types.</span></span> <span data-ttu-id="bf382-110">Sie können die Typen zuerst in den Reihenfolge-Eingabetyp oder den Ausgabetyp zuerst festlegen.</span><span class="sxs-lookup"><span data-stu-id="bf382-110">You can set the types in either order input type first, or output type first.</span></span>

### <a name="input-types"></a><span data-ttu-id="bf382-111">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="bf382-111">Input Types</span></span>

<span data-ttu-id="bf382-112">Legen Sie die folgenden Attribute für den Eingabe Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="bf382-112">Set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf382-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="bf382-113">Attribute</span></span></th>
<th><span data-ttu-id="bf382-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf382-114">Description</span></span></th>
<th><span data-ttu-id="bf382-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf382-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf382-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="bf382-117">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="bf382-117">Major type.</span></span></td>
<td><span data-ttu-id="bf382-118">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="bf382-118">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf382-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="bf382-120">Untertyp.</span><span class="sxs-lookup"><span data-stu-id="bf382-120">Subtype.</span></span></td>
<td><span data-ttu-id="bf382-121">Muss <strong>MFAudioFormat_PCM</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="bf382-121">Must be <strong>MFAudioFormat_PCM</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf382-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="bf382-123">Bits pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="bf382-123">Bits per sample.</span></span></td>
<td><span data-ttu-id="bf382-124">Muss 16 sein.</span><span class="sxs-lookup"><span data-stu-id="bf382-124">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf382-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="bf382-126">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="bf382-126">Samples per second.</span></span></td>
<td><span data-ttu-id="bf382-127">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bf382-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="bf382-128">44100 (44,1 kHz)</span><span class="sxs-lookup"><span data-stu-id="bf382-128">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="bf382-129">48000 (48 kHz)</span><span class="sxs-lookup"><span data-stu-id="bf382-129">48000 (48 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf382-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="bf382-131">Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="bf382-131">Number of channels.</span></span></td>
<td><span data-ttu-id="bf382-132">Muss 1 (Mono) oder 2 (Stereo) oder 6 (5,1) sein.</span><span class="sxs-lookup"><span data-stu-id="bf382-132">Must be 1 (mono) or 2 (stereo), or 6 (5.1).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bf382-133">Unterstützung für 6 Audiokanäle wurde mit Windows 10 eingeführt und ist für frühere Versionen von Windows nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf382-133">Support for 6 audio channels was introduced with Windows 10 and is not available for earlier versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bf382-134">Nachdem der Eingabetyp festgelegt wurde, leitet der Encoder die folgenden Werte ab und fügt Sie dem Medientyp hinzu:</span><span class="sxs-lookup"><span data-stu-id="bf382-134">After the input type is set, the encoder derives the following values and adds them to the media type:</span></span>

-   [<span data-ttu-id="bf382-135">**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="bf382-135">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="bf382-136">**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="bf382-136">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="bf382-137">**MF-mittlere mittlere \_ \_ \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="bf382-137">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a><span data-ttu-id="bf382-138">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="bf382-138">Output Types</span></span>

<span data-ttu-id="bf382-139">Legen Sie die folgenden Attribute für den Ausgabe Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="bf382-139">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf382-140">Attribut</span><span class="sxs-lookup"><span data-stu-id="bf382-140">Attribute</span></span></th>
<th><span data-ttu-id="bf382-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf382-141">Description</span></span></th>
<th><span data-ttu-id="bf382-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf382-142">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf382-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="bf382-144">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="bf382-144">Major type.</span></span></td>
<td><span data-ttu-id="bf382-145">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="bf382-145">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf382-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="bf382-147">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="bf382-147">Audio subtype.</span></span></td>
<td><span data-ttu-id="bf382-148">Muss <strong>MFAudioFormat_AAC</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="bf382-148">Must be <strong>MFAudioFormat_AAC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf382-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="bf382-150">Bits pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="bf382-150">Bits per sample.</span></span></td>
<td><span data-ttu-id="bf382-151">Muss 16 sein.</span><span class="sxs-lookup"><span data-stu-id="bf382-151">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf382-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="bf382-153">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="bf382-153">Samples per second.</span></span></td>
<td><span data-ttu-id="bf382-154">Muss mit dem Eingabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="bf382-154">Must match the input type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf382-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="bf382-156">Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="bf382-156">Number of channels.</span></span></td>
<td><span data-ttu-id="bf382-157">Muss mit dem Eingabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="bf382-157">Must match the input type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf382-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf382-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="bf382-159">Die Bitrate des codierten AAC-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="bf382-159">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="bf382-160">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bf382-160">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="bf382-161">12000</span><span class="sxs-lookup"><span data-stu-id="bf382-161">12000</span></span></li>
<li><span data-ttu-id="bf382-162">16000</span><span class="sxs-lookup"><span data-stu-id="bf382-162">16000</span></span></li>
<li><span data-ttu-id="bf382-163">20000</span><span class="sxs-lookup"><span data-stu-id="bf382-163">20000</span></span></li>
<li><span data-ttu-id="bf382-164">24.000</span><span class="sxs-lookup"><span data-stu-id="bf382-164">24000</span></span></li>
</ul>
<span data-ttu-id="bf382-165">Der Standardwert für Mono und Stereo ist 12000 (96 Kbit/s).</span><span class="sxs-lookup"><span data-stu-id="bf382-165">The default value for both mono and stereo is 12000 (96 Kbps).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf382-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="bf382-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="bf382-167">Der AAC-Nutz Lasttyp.</span><span class="sxs-lookup"><span data-stu-id="bf382-167">The AAC payload type.</span></span></td>
<td><span data-ttu-id="bf382-168">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="bf382-168">Optional.</span></span> <span data-ttu-id="bf382-169">Wenn festgelegt, muss der Wert 0 (null) sein, was bedeutet, dass der Stream nur raw_data_block Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="bf382-169">If set, the value must be zero, indicating that the stream contains raw_data_block elements only.</span></span><br/> <span data-ttu-id="bf382-170">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="bf382-170">Optional.</span></span> <span data-ttu-id="bf382-171">Wenn das-Attribut nicht festgelegt ist, ist der Standardwert 0 (null) und gibt an, dass der Stream nur raw_data_block Elemente (RAW AAC) enthält.</span><span class="sxs-lookup"><span data-stu-id="bf382-171">If the attribute is not set, the default value is zero, indicating that the stream contains raw_data_block elements only (raw AAC).</span></span> <br/> <span data-ttu-id="bf382-172">Wenn dieses Attribut in Windows 7 festgelegt ist, muss der Wert 0 (null) lauten.</span><span class="sxs-lookup"><span data-stu-id="bf382-172">In Windows 7, if this attribute is set, the value must be zero.</span></span><br/> <span data-ttu-id="bf382-173">Ab Windows 8 kann der Wert 0 (RAW AAC) oder 1 (ADTs AAC) lauten.</span><span class="sxs-lookup"><span data-stu-id="bf382-173">Starting in Windows 8, the value can be 0 (raw AAC) or 1 (ADTS AAC).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf382-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="bf382-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="bf382-175">Das AAC-Audioprofil und die Ebene.</span><span class="sxs-lookup"><span data-stu-id="bf382-175">The AAC audio profile and level.</span></span></td>
<td><span data-ttu-id="bf382-176">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="bf382-176">Optional.</span></span> <span data-ttu-id="bf382-177">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bf382-177">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="bf382-178">0x29 (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf382-178">0x29 (default)</span></span></li>
<li><span data-ttu-id="bf382-179">0x2A</span><span class="sxs-lookup"><span data-stu-id="bf382-179">0x2A</span></span></li>
<li><span data-ttu-id="bf382-180">0x2B</span><span class="sxs-lookup"><span data-stu-id="bf382-180">0x2B</span></span></li>
<li><span data-ttu-id="bf382-181">0x2c</span><span class="sxs-lookup"><span data-stu-id="bf382-181">0x2C</span></span></li>
<li><span data-ttu-id="bf382-182">0x2E</span><span class="sxs-lookup"><span data-stu-id="bf382-182">0x2E</span></span></li>
<li><span data-ttu-id="bf382-183">0x2F</span><span class="sxs-lookup"><span data-stu-id="bf382-183">0x2F</span></span></li>
<li><span data-ttu-id="bf382-184">0x30</span><span class="sxs-lookup"><span data-stu-id="bf382-184">0x30</span></span></li>
<li><span data-ttu-id="bf382-185">0x31</span><span class="sxs-lookup"><span data-stu-id="bf382-185">0x31</span></span></li>
<li><span data-ttu-id="bf382-186">0x32</span><span class="sxs-lookup"><span data-stu-id="bf382-186">0x32</span></span></li>
<li><span data-ttu-id="bf382-187">0x33</span><span class="sxs-lookup"><span data-stu-id="bf382-187">0x33</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bf382-188">In der folgenden Tabelle sind die Werte aufgelistet, die für das MF_MT_AAC_PROFILE_LEVEL_INDICATION-Attribut verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bf382-188">The following table lists the values that can be used for the MF_MT_AAC_PROFILE_LEVEL_INDICATION attribute.</span></span>

| <span data-ttu-id="bf382-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION Wert</span><span class="sxs-lookup"><span data-stu-id="bf382-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION value</span></span> | <span data-ttu-id="bf382-190">Profil</span><span class="sxs-lookup"><span data-stu-id="bf382-190">Profile</span></span>                           |
|------------------------------------------|-----------------------------------|
| <span data-ttu-id="bf382-191">0x29</span><span class="sxs-lookup"><span data-stu-id="bf382-191">0x29</span></span>                                     | <span data-ttu-id="bf382-192">AAC-Profil L2</span><span class="sxs-lookup"><span data-stu-id="bf382-192">AAC Profile L2</span></span>                    | 
| <span data-ttu-id="bf382-193">0x2A</span><span class="sxs-lookup"><span data-stu-id="bf382-193">0x2A</span></span>                                     | <span data-ttu-id="bf382-194">AAC-Profil L4</span><span class="sxs-lookup"><span data-stu-id="bf382-194">AAC Profile L4</span></span>                    | 
| <span data-ttu-id="bf382-195">0x2B</span><span class="sxs-lookup"><span data-stu-id="bf382-195">0x2B</span></span>                                     | <span data-ttu-id="bf382-196">AAC-Profil L5</span><span class="sxs-lookup"><span data-stu-id="bf382-196">AAC Profile L5</span></span>                    | 
| <span data-ttu-id="bf382-197">0x2c</span><span class="sxs-lookup"><span data-stu-id="bf382-197">0x2C</span></span>                                     | <span data-ttu-id="bf382-198">Hoch Effizienz v1-AAC-Profil L2</span><span class="sxs-lookup"><span data-stu-id="bf382-198">High Efficiency v1 AAC Profile L2</span></span> | 
| <span data-ttu-id="bf382-199">0x2E</span><span class="sxs-lookup"><span data-stu-id="bf382-199">0x2E</span></span>                                     | <span data-ttu-id="bf382-200">Hoch Effizienz v1-AAC-Profil L4</span><span class="sxs-lookup"><span data-stu-id="bf382-200">High Efficiency v1 AAC Profile L4</span></span> | 
| <span data-ttu-id="bf382-201">0x2F</span><span class="sxs-lookup"><span data-stu-id="bf382-201">0x2F</span></span>                                     | <span data-ttu-id="bf382-202">Hoch Effizienz v1-AAC-Profil L5</span><span class="sxs-lookup"><span data-stu-id="bf382-202">High Efficiency v1 AAC Profile L5</span></span> | 
| <span data-ttu-id="bf382-203">0x30</span><span class="sxs-lookup"><span data-stu-id="bf382-203">0x30</span></span>                                     | <span data-ttu-id="bf382-204">Hoch Effizienz v2-AAC-Profil L2</span><span class="sxs-lookup"><span data-stu-id="bf382-204">High Efficiency v2 AAC Profile L2</span></span> | 
| <span data-ttu-id="bf382-205">0x31</span><span class="sxs-lookup"><span data-stu-id="bf382-205">0x31</span></span>                                     | <span data-ttu-id="bf382-206">Hoch Effizienz v2-AAC-Profil L3</span><span class="sxs-lookup"><span data-stu-id="bf382-206">High Efficiency v2 AAC Profile L3</span></span> | 
| <span data-ttu-id="bf382-207">0x32</span><span class="sxs-lookup"><span data-stu-id="bf382-207">0x32</span></span>                                     | <span data-ttu-id="bf382-208">Hoch Effizienz v2 AAC-Profil L4</span><span class="sxs-lookup"><span data-stu-id="bf382-208">High Efficiency v2 AAC Profile L4</span></span> | 
| <span data-ttu-id="bf382-209">0x33</span><span class="sxs-lookup"><span data-stu-id="bf382-209">0x33</span></span>                                     | <span data-ttu-id="bf382-210">Hoch Effizienz v2-AAC-Profil L5</span><span class="sxs-lookup"><span data-stu-id="bf382-210">High Efficiency v2 AAC Profile L5</span></span> | 

 

<span data-ttu-id="bf382-211">Nachdem der Ausgabetyp festgelegt wurde, aktualisiert der AAC-Encoder den Typ durch Hinzufügen des [**\_ \_ Benutzer \_ Daten Attributs MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="bf382-211">After the output type is set, the AAC encoder updates the type by adding the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="bf382-212">Dieses Attribut enthält den Teil der [**heaacwaveinfo**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) -Struktur, der nach der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur angezeigt wird (d. h. nach dem **wfx** -Member).</span><span class="sxs-lookup"><span data-stu-id="bf382-212">This attribute contains the portion of the [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="bf382-213">Danach folgen die audiospecificconfig ()-Daten gemäß ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="bf382-213">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="bf382-214">Jedes Ausgabe Beispiel enthält einen komprimierten AAC-Frame ohne Header.</span><span class="sxs-lookup"><span data-stu-id="bf382-214">Each output sample contains one compressed AAC frame with no header.</span></span> <span data-ttu-id="bf382-215">Dieses Format entspricht dem RAW \_ Data \_ Block ()-Element, das von MPEG-2 definiert wird.</span><span class="sxs-lookup"><span data-stu-id="bf382-215">This format is equivalent to the raw\_data\_block() element defined by MPEG-2.</span></span> <span data-ttu-id="bf382-216">Das [MF MT-Attribut des \_ AAC- \_ \_ Nutz Last \_ Typs](mf-mt-aac-payload-type.md) muss, sofern im Ausgabetyp vorhanden, auf NULL festgelegt werden, um diesen Nutz Lasttyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bf382-216">The [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) attribute, if present in the output type, must be set to zero to indicate this payload type.</span></span>

<span data-ttu-id="bf382-217">Jedes Ausgabe Beispiel enthält einen komprimierten AAC-Frame, der 1024 PCM-Stichproben entspricht.</span><span class="sxs-lookup"><span data-stu-id="bf382-217">Each output sample contains one compressed AAC frame corresponding to 1024 PCM samples.</span></span> <span data-ttu-id="bf382-218">Bei einer Samplingrate von 48 kHz beträgt die Dauer eines komprimierten Frames z. b. 21,33 ms.</span><span class="sxs-lookup"><span data-stu-id="bf382-218">For example, at 48 Khz sampling rate, the duration of one compressed frame is 21.33 msec.</span></span>

<span data-ttu-id="bf382-219">Wenn der [MF-AAC-AAC- \_ \_ \_ Nutz \_ Lasttyp](mf-mt-aac-payload-type.md) 0 (null) ist (Standardwert), enthält jedes Ausgabe Beispiel ein unformatiertes \_ Daten \_ Block Element () gemäß ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="bf382-219">If [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) is zero (the default value), each output sample contains one raw\_data\_block() element as defined by ISO/IEC 13818-7.</span></span>

## <a name="example-media-types"></a><span data-ttu-id="bf382-220">Beispiel Medientypen</span><span class="sxs-lookup"><span data-stu-id="bf382-220">Example Media Types</span></span>

<span data-ttu-id="bf382-221">Im folgenden finden Sie ein Beispiel für die Medientypen, die zum Codieren zwischen 44,1-kHz-, 160-KBit/s-Stereo Audiodaten und RAW AAC</span><span class="sxs-lookup"><span data-stu-id="bf382-221">Here is an example of the media types needed to encode from 44.1-kHz, 160-Kbps stereo audio to raw AAC</span></span>

<span data-ttu-id="bf382-222">Eingabe Medientyp:</span><span class="sxs-lookup"><span data-stu-id="bf382-222">Input media type:</span></span>



| <span data-ttu-id="bf382-223">Attribut</span><span class="sxs-lookup"><span data-stu-id="bf382-223">Attribute</span></span>                                                                                    | <span data-ttu-id="bf382-224">Wert</span><span class="sxs-lookup"><span data-stu-id="bf382-224">Value</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="bf382-225">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf382-225">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="bf382-226">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="bf382-226">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="bf382-227">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="bf382-227">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="bf382-228">**MF Audioformat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="bf382-228">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="bf382-229">**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**</span><span class="sxs-lookup"><span data-stu-id="bf382-229">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="bf382-230">16</span><span class="sxs-lookup"><span data-stu-id="bf382-230">16</span></span>                     |
| [<span data-ttu-id="bf382-231">**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="bf382-231">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="bf382-232">44100</span><span class="sxs-lookup"><span data-stu-id="bf382-232">44100</span></span>                  |
| [<span data-ttu-id="bf382-233">**MF \_ \_ -MT- \_ audionum- \_ Kanäle**</span><span class="sxs-lookup"><span data-stu-id="bf382-233">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="bf382-234">2</span><span class="sxs-lookup"><span data-stu-id="bf382-234">2</span></span>                      |
| [<span data-ttu-id="bf382-235">**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="bf382-235">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="bf382-236">176400 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-236">176400 (optional)</span></span>      |
| [<span data-ttu-id="bf382-237">**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="bf382-237">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="bf382-238">4 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-238">4 (optional)</span></span>           |
| [<span data-ttu-id="bf382-239">**\_ \_ alle \_ Beispiele \_ unabhängig von MF**</span><span class="sxs-lookup"><span data-stu-id="bf382-239">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="bf382-240">1 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-240">1 (optional)</span></span>           |
| [<span data-ttu-id="bf382-241">**MF-mittlere mittlere \_ \_ \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="bf382-241">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                  | <span data-ttu-id="bf382-242">1411200 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-242">1411200 (optional)</span></span>     |
| [<span data-ttu-id="bf382-243">**\_Beispiele für \_ die \_ große Größe \_ von MF MT**</span><span class="sxs-lookup"><span data-stu-id="bf382-243">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)                   | <span data-ttu-id="bf382-244">1 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-244">1 (optional)</span></span>           |



 

<span data-ttu-id="bf382-245">Ausgabe Medientyp:</span><span class="sxs-lookup"><span data-stu-id="bf382-245">Output media type:</span></span>



| <span data-ttu-id="bf382-246">Attribut</span><span class="sxs-lookup"><span data-stu-id="bf382-246">Attribute</span></span>                                                                                      | <span data-ttu-id="bf382-247">Wert</span><span class="sxs-lookup"><span data-stu-id="bf382-247">Value</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf382-248">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf382-248">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="bf382-249">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="bf382-249">**MFMediaType\_Audio**</span></span>                                                                          |
| [<span data-ttu-id="bf382-250">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="bf382-250">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="bf382-251">**MF Audioformat- \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="bf382-251">**MFAudioFormat\_AAC**</span></span>                                                                          |
| [<span data-ttu-id="bf382-252">**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**</span><span class="sxs-lookup"><span data-stu-id="bf382-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="bf382-253">16</span><span class="sxs-lookup"><span data-stu-id="bf382-253">16</span></span>                                                                                              |
| [<span data-ttu-id="bf382-254">**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="bf382-254">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="bf382-255">44100</span><span class="sxs-lookup"><span data-stu-id="bf382-255">44100</span></span>                                                                                           |
| [<span data-ttu-id="bf382-256">**MF \_ \_ -MT- \_ audionum- \_ Kanäle**</span><span class="sxs-lookup"><span data-stu-id="bf382-256">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="bf382-257">2</span><span class="sxs-lookup"><span data-stu-id="bf382-257">2</span></span>                                                                                               |
| [<span data-ttu-id="bf382-258">**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="bf382-258">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="bf382-259">20000</span><span class="sxs-lookup"><span data-stu-id="bf382-259">20000</span></span>                                                                                           |
| [<span data-ttu-id="bf382-260">MF- \_ MT- \_ AAC- \_ Nutzlast \_</span><span class="sxs-lookup"><span data-stu-id="bf382-260">MF\_MT\_AAC\_PAYLOAD\_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="bf382-261">0 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-261">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="bf382-262">Anzeige der MF \_ \_ \_ -AAC- \_ \_ audioprofilebene \_</span><span class="sxs-lookup"><span data-stu-id="bf382-262">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="bf382-263">0x29 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-263">0x29 (optional)</span></span>                                                                                 |
| [<span data-ttu-id="bf382-264">**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="bf382-264">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="bf382-265">1 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-265">1 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="bf382-266">**\_ \_ alle \_ Beispiele \_ unabhängig von MF**</span><span class="sxs-lookup"><span data-stu-id="bf382-266">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)           | <span data-ttu-id="bf382-267">0 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-267">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="bf382-268">**MF-mittlere mittlere \_ \_ \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="bf382-268">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                    | <span data-ttu-id="bf382-269">160000 (optional)</span><span class="sxs-lookup"><span data-stu-id="bf382-269">160000 (optional)</span></span>                                                                               |
| [<span data-ttu-id="bf382-270">**\_ \_ Benutzer \_ Daten für MF-MT**</span><span class="sxs-lookup"><span data-stu-id="bf382-270">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="bf382-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} optionale</span><span class="sxs-lookup"><span data-stu-id="bf382-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bf382-272">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf382-272">Remarks</span></span>

<span data-ttu-id="bf382-273">In der aktuellen Implementierung muss jede Eingabe Stichprobe über eine gültige Zeit und Dauer verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf382-273">In the current implementation, every input sample must have a valid time and duration.</span></span> <span data-ttu-id="bf382-274">Um die Stichproben Zeit festzulegen, wenden Sie [**imfsample:: setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)an.</span><span class="sxs-lookup"><span data-stu-id="bf382-274">To set the sample time, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="bf382-275">Um die Stichproben Dauer festzulegen, müssen Sie [**imfsample:: setsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bf382-275">To set the sample duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="bf382-276">Wenn die Stichproben Zeit nicht festgelegt ist, gibt die [**IMF Transform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode von " **MF \_ E \_ No \_ Sample \_ timestamp**" zurück.</span><span class="sxs-lookup"><span data-stu-id="bf382-276">If the sample time is not set, the encoder's [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method returns **MF\_E\_NO\_SAMPLE\_TIMESTAMP**.</span></span> <span data-ttu-id="bf382-277">Wenn die Stichproben Dauer nicht festgelegt ist, gibt die **ProcessInput** -Methode die " **MF \_ E \_ No \_ Sample \_ Duration**" zurück.</span><span class="sxs-lookup"><span data-stu-id="bf382-277">If the sample duration is not set, the **ProcessInput** method returns **MF\_E\_NO\_SAMPLE\_DURATION**.</span></span>

<span data-ttu-id="bf382-278">Die Stichproben Dauer kann wie folgt berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="bf382-278">Sample duration can be calculated as follows:</span></span>


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



<span data-ttu-id="bf382-279">Dabei ist *naudiosamplesperchannel* die Anzahl von PCM-Audiobeispielen pro Kanal im Eingabepuffer, und *nsamplespersec* ist die Samplingrate in Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="bf382-279">where *nAudioSamplesPerChannel* is the number of PCM audio samples per channel in the input buffer, and *nSamplesPerSec* is the sampling rate, in samples per second.</span></span>

> [!Note]  
> <span data-ttu-id="bf382-280">Aufgrund eines Fehlers in der aktuellen Implementierung, wenn die Stichproben Dauer auf NULL festgelegt ist, wird der [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Befehl erfolgreich ausgeführt, aber ein nachfolgende Rückruf von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) löst eine Ausnahme aufgrund einer Division durch NULL aus.</span><span class="sxs-lookup"><span data-stu-id="bf382-280">Due to a bug in the current implementation, if the sample duration is set to zero, the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) call succeeds, but a subsequent call to [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) will throw a divide-by-zero exception.</span></span> <span data-ttu-id="bf382-281">Um diesen Fehler zu vermeiden, legen Sie für jedes Eingabe Beispiel eine gültige Dauer ungleich NULL fest.</span><span class="sxs-lookup"><span data-stu-id="bf382-281">To avoid this error, set a valid nonzero duration on each input sample.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf382-282">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf382-282">Requirements</span></span>



| <span data-ttu-id="bf382-283">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf382-283">Requirement</span></span> | <span data-ttu-id="bf382-284">Wert</span><span class="sxs-lookup"><span data-stu-id="bf382-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf382-285">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf382-285">Minimum supported client</span></span><br/> | <span data-ttu-id="bf382-286">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf382-286">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bf382-287">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf382-287">Minimum supported server</span></span><br/> | <span data-ttu-id="bf382-288">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf382-288">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bf382-289">DLL</span><span class="sxs-lookup"><span data-stu-id="bf382-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf382-290"><dt>Mfaacenc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf382-290"><dt>Mfaacenc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf382-291">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf382-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf382-292">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="bf382-292">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="bf382-293">**AAC-Decoder**</span><span class="sxs-lookup"><span data-stu-id="bf382-293">**AAC Decoder**</span></span>](aac-decoder.md)
</dt> <dt>

[<span data-ttu-id="bf382-294">AAC-Medientypen</span><span class="sxs-lookup"><span data-stu-id="bf382-294">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="bf382-295">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="bf382-295">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="bf382-296">MPEG-4-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf382-296">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bf382-297">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf382-297">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

