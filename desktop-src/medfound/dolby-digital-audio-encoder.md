---
description: Der Dolby-Audioencoder ist eine Media Foundation-Transformation (MFT), die Mono- oder Stereoaudio in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Dolby Digital Audio Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f901587b816bc17d62f4095e093b661ce55f0009
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153563"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="4a2da-103">Dolby Digital Audio Encoder</span><span class="sxs-lookup"><span data-stu-id="4a2da-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="4a2da-104">Der Dolby-Audioencoder ist eine [Media Foundation-Transformation](media-foundation-transforms.md) (MFT), die Mono- oder Stereoaudio in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4a2da-104">The Dolby audio encoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="4a2da-105">Der Encoder unterstützt keine Mehrkanaleingaben, z.B. die 5.1-Kanalkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4a2da-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a2da-106">Bei Windows-Versionen vor Windows 8 ist die Microsoft-Implementierung der Dolby Digital-Technologie gemäß den Bedingungen des Dolby Digital-Lizenzierungsprogramms auf die Verwendung durch Microsoft-Anwendungen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="4a2da-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="4a2da-107">Weitere Informationen zu Dolby Digital-Audio finden Sie im ATSC-Dokument (Advanced Tv Systems Committee) *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span><span class="sxs-lookup"><span data-stu-id="4a2da-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="4a2da-108">Klassenbezeichner</span><span class="sxs-lookup"><span data-stu-id="4a2da-108">Class Identifier</span></span>

<span data-ttu-id="4a2da-109">Der Klassenbezeichner (CLSID) des Dolby-Audioencoders ist **CLSID \_ CMSSpanbyDigitalEncMFT,** definiert in der Headerdatei wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="4a2da-109">The class identifier (CLSID) of the Dolby audio encoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="4a2da-110">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="4a2da-110">Output Types</span></span>

<span data-ttu-id="4a2da-111">Der Ausgabetyp muss zuerst vor dem Eingabetyp festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4a2da-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="4a2da-112">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabemedientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a2da-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a2da-113">attribute</span><span class="sxs-lookup"><span data-stu-id="4a2da-113">Attribute</span></span></th>
<th><span data-ttu-id="4a2da-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a2da-114">Description</span></span></th>
<th><span data-ttu-id="4a2da-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a2da-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4a2da-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="4a2da-117">Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="4a2da-117">Major type.</span></span></td>
<td><span data-ttu-id="4a2da-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-118">Required.</span></span> <span data-ttu-id="4a2da-119">Muss <strong>MFMediaType_Audio</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="4a2da-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a2da-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="4a2da-121">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="4a2da-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="4a2da-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-122">Required.</span></span> <span data-ttu-id="4a2da-123">Muss <strong>MFAudioFormat_Dolby_AC3</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="4a2da-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a2da-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4a2da-125">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4a2da-125">Samples per second.</span></span></td>
<td><span data-ttu-id="4a2da-126">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-126">Required.</span></span> <span data-ttu-id="4a2da-127">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="4a2da-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="4a2da-128">32000</span><span class="sxs-lookup"><span data-stu-id="4a2da-128">32000</span></span></li>
<li><span data-ttu-id="4a2da-129">44100</span><span class="sxs-lookup"><span data-stu-id="4a2da-129">44100</span></span></li>
<li><span data-ttu-id="4a2da-130">48000</span><span class="sxs-lookup"><span data-stu-id="4a2da-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a2da-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="4a2da-132">Anzahl von Kanälen.</span><span class="sxs-lookup"><span data-stu-id="4a2da-132">Number of channels.</span></span></td>
<td><span data-ttu-id="4a2da-133">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-133">Required.</span></span> <span data-ttu-id="4a2da-134">Muss entweder 1 (Mono) oder 2 (Stereo) sein.</span><span class="sxs-lookup"><span data-stu-id="4a2da-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a2da-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="4a2da-136">Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an.</span><span class="sxs-lookup"><span data-stu-id="4a2da-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="4a2da-137">Optional.</span><span class="sxs-lookup"><span data-stu-id="4a2da-137">Optional.</span></span> <span data-ttu-id="4a2da-138">Wenn festgelegt, muss der Wert 0x3 Stereokanal (linker und rechter Vorderkanal) oder 0x4 Mono (Front-Center-Kanal) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4a2da-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a2da-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4a2da-140">Bitrate des codierten AC-3-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4a2da-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="4a2da-141">Optional.</span><span class="sxs-lookup"><span data-stu-id="4a2da-141">Optional.</span></span> <span data-ttu-id="4a2da-142">Gültige Werte finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="4a2da-142">See Remarks for valid values.</span></span> <span data-ttu-id="4a2da-143">Wenn dieses Attribut nicht festgelegt ist, verwendet der Encoder eine Standardbitrate, wie in Hinweise beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a2da-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4a2da-144">Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="4a2da-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="4a2da-145">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="4a2da-145">Input Types</span></span>

<span data-ttu-id="4a2da-146">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabemedientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a2da-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a2da-147">attribute</span><span class="sxs-lookup"><span data-stu-id="4a2da-147">Attribute</span></span></th>
<th><span data-ttu-id="4a2da-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a2da-148">Description</span></span></th>
<th><span data-ttu-id="4a2da-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a2da-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4a2da-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="4a2da-151">Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="4a2da-151">Major type.</span></span></td>
<td><span data-ttu-id="4a2da-152">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-152">Required.</span></span> <span data-ttu-id="4a2da-153">Muss <strong>MFMediaType_Audio.</strong></span><span class="sxs-lookup"><span data-stu-id="4a2da-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a2da-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="4a2da-155">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="4a2da-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="4a2da-156">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-156">Required.</span></span> <span data-ttu-id="4a2da-157">Muss <strong>MFAudioFormat_PCM</strong> <strong>oder</strong>MFAudioFormat_Float.</span><span class="sxs-lookup"><span data-stu-id="4a2da-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a2da-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="4a2da-159">Anzahl von Bits pro Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="4a2da-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="4a2da-160">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-160">Required.</span></span> <span data-ttu-id="4a2da-161">Der Wert muss 16 sein, wenn der Untertyp <strong>MFAudioFormat_PCM</strong>ist, oder 32, wenn der Untertyp <strong>MFAudioFormat_Float</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="4a2da-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a2da-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4a2da-163">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4a2da-163">Samples per second.</span></span></td>
<td><span data-ttu-id="4a2da-164">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-164">Required.</span></span> <span data-ttu-id="4a2da-165">Muss mit dem Ausgabetyp übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4a2da-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a2da-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="4a2da-167">Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="4a2da-167">Number of channels.</span></span></td>
<td><span data-ttu-id="4a2da-168">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-168">Required.</span></span> <span data-ttu-id="4a2da-169">Muss mit dem Ausgabetyp übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4a2da-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a2da-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="4a2da-171">Blockausrichtung in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4a2da-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="4a2da-172">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-172">Required.</span></span> <span data-ttu-id="4a2da-173">Berechnen Sie den Wert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4a2da-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="4a2da-174"><strong>MFAudioFormat_PCM:</strong>Anzahl der Kanäle × 2.</span><span class="sxs-lookup"><span data-stu-id="4a2da-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="4a2da-175"><strong>MFAudioFormat_Float:</strong>Anzahl der Kanäle × 4.</span><span class="sxs-lookup"><span data-stu-id="4a2da-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a2da-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4a2da-177">Bitrate des codierten AC3-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="4a2da-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="4a2da-178">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a2da-178">Required.</span></span> <span data-ttu-id="4a2da-179">Muss der Blockausrichtung × Stichproben pro Sekunde entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4a2da-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a2da-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="4a2da-181">Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an.</span><span class="sxs-lookup"><span data-stu-id="4a2da-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="4a2da-182">Optional.</span><span class="sxs-lookup"><span data-stu-id="4a2da-182">Optional.</span></span> <span data-ttu-id="4a2da-183">Wenn diese Einstellung festgelegt ist, muss der Wert mit dem Ausgabetyp übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4a2da-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a2da-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="4a2da-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="4a2da-185">Anzahl der gültigen Bits von Audiodaten in jedem Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="4a2da-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="4a2da-186">Optional.</span><span class="sxs-lookup"><span data-stu-id="4a2da-186">Optional.</span></span> <span data-ttu-id="4a2da-187">Wenn festgelegt, muss der Wert mit dem <a href="mf-mt-audio-bits-per-sample-attribute.md">Wert</a>MF_MT_AUDIO_BITS_PER_SAMPLE.</span><span class="sxs-lookup"><span data-stu-id="4a2da-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4a2da-188">Der Encoder unterstützt keine Abtastratenkonvertierung oder Stereo-/Monokonvertierung.</span><span class="sxs-lookup"><span data-stu-id="4a2da-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2da-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a2da-189">Remarks</span></span>

<span data-ttu-id="4a2da-190">Jeder Dolby AC-3-Audioframe enthält 1536 Audiobeispiele pro Kanal.</span><span class="sxs-lookup"><span data-stu-id="4a2da-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="4a2da-191">Jeder Eingabepuffer für den Encoder kann jedoch eine beliebige Anzahl von PCM-Stichproben enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a2da-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="4a2da-192">Die Größe jedes Eingabepuffers muss ein Vielfaches der Blockausrichtung sein.</span><span class="sxs-lookup"><span data-stu-id="4a2da-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="4a2da-193">Der Encoder speichert Eingabebeispiele zwischen, bis er für 1.536 Audiobeispiele pro Kanal ausreicht. An diesem Punkt gibt der Encoder einen AC-3-Frame aus.</span><span class="sxs-lookup"><span data-stu-id="4a2da-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="4a2da-194">Jeder Ausgabepuffer enthält einen unformatten AC-3-Frame.</span><span class="sxs-lookup"><span data-stu-id="4a2da-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="4a2da-195">Die Dauer entspricht der Dauer von 1.536 PCM-Stichproben bei der aktuellen Samplingrate (32 msec) bei einer Abtastrate von 48 kHz, 34,83 msec bei 44,1 kHz und 48 msec bei 32 kHz.</span><span class="sxs-lookup"><span data-stu-id="4a2da-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="4a2da-196">Die Größe der einzelnen Ausgabepuffer hängt von der Bitrate und der Abtastrate ab.</span><span class="sxs-lookup"><span data-stu-id="4a2da-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="4a2da-197">Um die Codierungsbitrate anzugeben, legen Sie das [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND-Attribut](mf-mt-audio-avg-bytes-per-second-attribute.md) im Ausgabetyp fest.</span><span class="sxs-lookup"><span data-stu-id="4a2da-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="4a2da-198">Die folgende Tabelle zeigt die Beziehung zwischen der Codierungsbitrate und MF \_ MT \_ AUDIO \_ AVG BYTES PER \_ \_ \_ SECOND.</span><span class="sxs-lookup"><span data-stu-id="4a2da-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="4a2da-199">Bitrate (KBit/s)</span><span class="sxs-lookup"><span data-stu-id="4a2da-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="4a2da-200">MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND</span><span class="sxs-lookup"><span data-stu-id="4a2da-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="4a2da-201">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a2da-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4a2da-202">64</span><span class="sxs-lookup"><span data-stu-id="4a2da-202">64</span></span>              | <span data-ttu-id="4a2da-203">8.000</span><span class="sxs-lookup"><span data-stu-id="4a2da-203">8000</span></span>                                                                                     | <span data-ttu-id="4a2da-204">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="4a2da-204">Mono only.</span></span>                                              |
| <span data-ttu-id="4a2da-205">80</span><span class="sxs-lookup"><span data-stu-id="4a2da-205">80</span></span>              | <span data-ttu-id="4a2da-206">10000</span><span class="sxs-lookup"><span data-stu-id="4a2da-206">10000</span></span>                                                                                    | <span data-ttu-id="4a2da-207">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="4a2da-207">Mono only.</span></span>                                              |
| <span data-ttu-id="4a2da-208">96</span><span class="sxs-lookup"><span data-stu-id="4a2da-208">96</span></span>              | <span data-ttu-id="4a2da-209">12000</span><span class="sxs-lookup"><span data-stu-id="4a2da-209">12000</span></span>                                                                                    | <span data-ttu-id="4a2da-210">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="4a2da-210">Mono only.</span></span>                                              |
| <span data-ttu-id="4a2da-211">112</span><span class="sxs-lookup"><span data-stu-id="4a2da-211">112</span></span>             | <span data-ttu-id="4a2da-212">14000</span><span class="sxs-lookup"><span data-stu-id="4a2da-212">14000</span></span>                                                                                    | <span data-ttu-id="4a2da-213">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="4a2da-213">Mono only.</span></span>                                              |
| <span data-ttu-id="4a2da-214">128</span><span class="sxs-lookup"><span data-stu-id="4a2da-214">128</span></span>             | <span data-ttu-id="4a2da-215">16000</span><span class="sxs-lookup"><span data-stu-id="4a2da-215">16000</span></span>                                                                                    | <span data-ttu-id="4a2da-216">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="4a2da-217">160</span><span class="sxs-lookup"><span data-stu-id="4a2da-217">160</span></span>             | <span data-ttu-id="4a2da-218">20000</span><span class="sxs-lookup"><span data-stu-id="4a2da-218">20000</span></span>                                                                                    | <span data-ttu-id="4a2da-219">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="4a2da-220">192</span><span class="sxs-lookup"><span data-stu-id="4a2da-220">192</span></span>             | <span data-ttu-id="4a2da-221">24.000</span><span class="sxs-lookup"><span data-stu-id="4a2da-221">24000</span></span>                                                                                    | <span data-ttu-id="4a2da-222">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-222">Mono or stereo.</span></span> <span data-ttu-id="4a2da-223">Dies ist die Standardeinstellung für Mono.</span><span class="sxs-lookup"><span data-stu-id="4a2da-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="4a2da-224">224</span><span class="sxs-lookup"><span data-stu-id="4a2da-224">224</span></span>             | <span data-ttu-id="4a2da-225">28000</span><span class="sxs-lookup"><span data-stu-id="4a2da-225">28000</span></span>                                                                                    | <span data-ttu-id="4a2da-226">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="4a2da-227">256</span><span class="sxs-lookup"><span data-stu-id="4a2da-227">256</span></span>             | <span data-ttu-id="4a2da-228">32000</span><span class="sxs-lookup"><span data-stu-id="4a2da-228">32000</span></span>                                                                                    | <span data-ttu-id="4a2da-229">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-229">Mono or stereo.</span></span> <span data-ttu-id="4a2da-230">Dies ist die Standardeinstellung für Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="4a2da-231">320</span><span class="sxs-lookup"><span data-stu-id="4a2da-231">320</span></span>             | <span data-ttu-id="4a2da-232">40.000</span><span class="sxs-lookup"><span data-stu-id="4a2da-232">40000</span></span>                                                                                    | <span data-ttu-id="4a2da-233">Nur Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="4a2da-234">384</span><span class="sxs-lookup"><span data-stu-id="4a2da-234">384</span></span>             | <span data-ttu-id="4a2da-235">48000</span><span class="sxs-lookup"><span data-stu-id="4a2da-235">48000</span></span>                                                                                    | <span data-ttu-id="4a2da-236">Nur Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="4a2da-237">448</span><span class="sxs-lookup"><span data-stu-id="4a2da-237">448</span></span>             | <span data-ttu-id="4a2da-238">56000</span><span class="sxs-lookup"><span data-stu-id="4a2da-238">56000</span></span>                                                                                    | <span data-ttu-id="4a2da-239">Nur Stereo.</span><span class="sxs-lookup"><span data-stu-id="4a2da-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="4a2da-240">Die Standardcodierungsbitrate ist auf 256 KBit/s für Stereo und 192 KBit/s für Mono festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a2da-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="4a2da-241">Die Standardeinstellungen werden in den Medientypen widergespiegelt, die von [**derENTransform::GetOutputAvailableType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) des Encoders zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a2da-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="4a2da-242">Beispielmedientypen</span><span class="sxs-lookup"><span data-stu-id="4a2da-242">Example Media Types</span></span>

<span data-ttu-id="4a2da-243">Hier sehen Sie ein Beispiel für die Medientypen, die zum Codieren von 16-Bit-Ganzzahl-PCM mit Stereoaudio mit 48 kHz mit der Standardbitrate von 256 KBit/s erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4a2da-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="4a2da-244">Ausgabemedientyp:</span><span class="sxs-lookup"><span data-stu-id="4a2da-244">Output media type:</span></span>

| <span data-ttu-id="4a2da-245">attribute</span><span class="sxs-lookup"><span data-stu-id="4a2da-245">Attribute</span></span>                                                                           | <span data-ttu-id="4a2da-246">Wert</span><span class="sxs-lookup"><span data-stu-id="4a2da-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="4a2da-247">MF \_ \_ MT-HAUPTTYP \_</span><span class="sxs-lookup"><span data-stu-id="4a2da-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="4a2da-248">**MFMediaType \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="4a2da-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="4a2da-249">MF \_ \_ MT-UNTERTYP</span><span class="sxs-lookup"><span data-stu-id="4a2da-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="4a2da-250">**MFAudioFormat \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="4a2da-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="4a2da-251">MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE</span><span class="sxs-lookup"><span data-stu-id="4a2da-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="4a2da-252">48000</span><span class="sxs-lookup"><span data-stu-id="4a2da-252">48000</span></span>                         |
| [<span data-ttu-id="4a2da-253">MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS</span><span class="sxs-lookup"><span data-stu-id="4a2da-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="4a2da-254">2</span><span class="sxs-lookup"><span data-stu-id="4a2da-254">2</span></span>                             |



 

<span data-ttu-id="4a2da-255">Eingabemedientyp:</span><span class="sxs-lookup"><span data-stu-id="4a2da-255">Input media type:</span></span>

| <span data-ttu-id="4a2da-256">attribute</span><span class="sxs-lookup"><span data-stu-id="4a2da-256">Attribute</span></span>                                                                                | <span data-ttu-id="4a2da-257">Wert</span><span class="sxs-lookup"><span data-stu-id="4a2da-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="4a2da-258">MF \_ \_ MT-HAUPTTYP \_</span><span class="sxs-lookup"><span data-stu-id="4a2da-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="4a2da-259">**MFMediaType-Audio \_**</span><span class="sxs-lookup"><span data-stu-id="4a2da-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="4a2da-260">MF \_ \_ MT-UNTERTYP</span><span class="sxs-lookup"><span data-stu-id="4a2da-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="4a2da-261">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="4a2da-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="4a2da-262">MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL</span><span class="sxs-lookup"><span data-stu-id="4a2da-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="4a2da-263">16</span><span class="sxs-lookup"><span data-stu-id="4a2da-263">16</span></span>                     |
| [<span data-ttu-id="4a2da-264">MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE</span><span class="sxs-lookup"><span data-stu-id="4a2da-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="4a2da-265">48000</span><span class="sxs-lookup"><span data-stu-id="4a2da-265">48000</span></span>                  |
| [<span data-ttu-id="4a2da-266">MF \_ MT AUDIO \_ \_ \_ NUM-KANÄLE</span><span class="sxs-lookup"><span data-stu-id="4a2da-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="4a2da-267">2</span><span class="sxs-lookup"><span data-stu-id="4a2da-267">2</span></span>                      |
| [<span data-ttu-id="4a2da-268">MF MT AUDIO BLOCK ALIGNMENT (MF \_ \_ MT-AUDIOBLOCKAUSRICHTUNG) \_ \_</span><span class="sxs-lookup"><span data-stu-id="4a2da-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="4a2da-269">4</span><span class="sxs-lookup"><span data-stu-id="4a2da-269">4</span></span>                      |
| [<span data-ttu-id="4a2da-270">MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND</span><span class="sxs-lookup"><span data-stu-id="4a2da-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="4a2da-271">192000</span><span class="sxs-lookup"><span data-stu-id="4a2da-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="4a2da-272">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a2da-272">Requirements</span></span>



| <span data-ttu-id="4a2da-273">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a2da-273">Requirement</span></span> | <span data-ttu-id="4a2da-274">Wert</span><span class="sxs-lookup"><span data-stu-id="4a2da-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2da-275">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a2da-275">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2da-276">Windows 8 \[ Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a2da-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="4a2da-277">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a2da-277">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2da-278">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4a2da-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4a2da-279">DLL</span><span class="sxs-lookup"><span data-stu-id="4a2da-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a2da-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a2da-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2da-281">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a2da-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2da-282">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="4a2da-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




