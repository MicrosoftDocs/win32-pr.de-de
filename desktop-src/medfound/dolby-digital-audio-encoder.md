---
description: Der Dolby-Audiodecoder ist eine Media Foundation Transformation (MFT), die Mono-oder Stereo-Audiodaten in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Dolby Digital-Audioencoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343022"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="1ee52-103">Dolby Digital-Audioencoder</span><span class="sxs-lookup"><span data-stu-id="1ee52-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="1ee52-104">Der Dolby-Audiodecoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT), die Mono-oder Stereo-Audiodaten in Dolby Digital codiert, auch als Dolby AC-3 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1ee52-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="1ee52-105">Der Encoder unterstützt keine multikanaleingaben, z. b. die 5,1-Kanal Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ee52-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ee52-106">Bei Windows-Versionen vor Windows 8 ist die Microsoft-Implementierung der Dolby Digital-Technologie gemäß den Bedingungen des Dolby Digital Licensing Program, das von Microsoft-Anwendungen verwendet werden soll, eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="1ee52-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="1ee52-107">Weitere Informationen zu Dolby Digital-Audiodaten finden Sie unter Advanced Television System Committee (ATSC) Document *Digital audiocompression Standard (AC-3, E-AC-3) Revision B*.</span><span class="sxs-lookup"><span data-stu-id="1ee52-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1ee52-108">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1ee52-108">Class Identifier</span></span>

<span data-ttu-id="1ee52-109">Der Klassen Bezeichner (CLSID) des Dolby-Audiodecoders ist **CLSID \_ cmsdolbydigitalencmft**, der in der Header Datei "wmcodecdsp. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ee52-109">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="1ee52-110">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="1ee52-110">Output Types</span></span>

<span data-ttu-id="1ee52-111">Der Ausgabetyp muss zuerst festgelegt werden, vor dem Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="1ee52-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="1ee52-112">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabe Medientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ee52-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ee52-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="1ee52-113">Attribute</span></span></th>
<th><span data-ttu-id="1ee52-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ee52-114">Description</span></span></th>
<th><span data-ttu-id="1ee52-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ee52-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ee52-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="1ee52-117">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="1ee52-117">Major type.</span></span></td>
<td><span data-ttu-id="1ee52-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-118">Required.</span></span> <span data-ttu-id="1ee52-119">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="1ee52-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ee52-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="1ee52-121">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="1ee52-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="1ee52-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-122">Required.</span></span> <span data-ttu-id="1ee52-123">Muss <strong>MFAudioFormat_Dolby_AC3</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="1ee52-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ee52-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="1ee52-125">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="1ee52-125">Samples per second.</span></span></td>
<td><span data-ttu-id="1ee52-126">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-126">Required.</span></span> <span data-ttu-id="1ee52-127">Die folgenden Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1ee52-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="1ee52-128">32000</span><span class="sxs-lookup"><span data-stu-id="1ee52-128">32000</span></span></li>
<li><span data-ttu-id="1ee52-129">44100</span><span class="sxs-lookup"><span data-stu-id="1ee52-129">44100</span></span></li>
<li><span data-ttu-id="1ee52-130">48000</span><span class="sxs-lookup"><span data-stu-id="1ee52-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ee52-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="1ee52-132">Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="1ee52-132">Number of channels.</span></span></td>
<td><span data-ttu-id="1ee52-133">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-133">Required.</span></span> <span data-ttu-id="1ee52-134">Muss entweder 1 (Mono) oder 2 (Stereo) sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ee52-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="1ee52-136">Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="1ee52-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="1ee52-137">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1ee52-137">Optional.</span></span> <span data-ttu-id="1ee52-138">Wenn festgelegt, muss der Wert 0x3 für Stereo (Front Left und Right Channels) oder 0x4 für Mono (Front-Center-Kanal) lauten.</span><span class="sxs-lookup"><span data-stu-id="1ee52-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ee52-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="1ee52-140">Die Bitrate des codierten AC-3-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="1ee52-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="1ee52-141">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1ee52-141">Optional.</span></span> <span data-ttu-id="1ee52-142">Gültige Werte finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="1ee52-142">See Remarks for valid values.</span></span> <span data-ttu-id="1ee52-143">Wenn dieses Attribut nicht festgelegt ist, verwendet der Encoder eine Standard Bitrate, wie unter Hinweise beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ee52-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1ee52-144">Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder Sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ee52-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="1ee52-145">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="1ee52-145">Input Types</span></span>

<span data-ttu-id="1ee52-146">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabe Medientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ee52-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ee52-147">Attribut</span><span class="sxs-lookup"><span data-stu-id="1ee52-147">Attribute</span></span></th>
<th><span data-ttu-id="1ee52-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ee52-148">Description</span></span></th>
<th><span data-ttu-id="1ee52-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ee52-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ee52-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="1ee52-151">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="1ee52-151">Major type.</span></span></td>
<td><span data-ttu-id="1ee52-152">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-152">Required.</span></span> <span data-ttu-id="1ee52-153">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="1ee52-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ee52-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="1ee52-155">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="1ee52-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="1ee52-156">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-156">Required.</span></span> <span data-ttu-id="1ee52-157">Muss <strong>MFAudioFormat_PCM</strong> oder <strong>MFAudioFormat_Float</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ee52-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="1ee52-159">Anzahl von Bits pro audiostich Probe.</span><span class="sxs-lookup"><span data-stu-id="1ee52-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="1ee52-160">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-160">Required.</span></span> <span data-ttu-id="1ee52-161">Der Wert muss 16 sein, wenn der Untertyp <strong>MFAudioFormat_PCM</strong>ist, oder 32, wenn der Untertyp <strong>MFAudioFormat_Float</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="1ee52-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ee52-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="1ee52-163">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="1ee52-163">Samples per second.</span></span></td>
<td><span data-ttu-id="1ee52-164">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-164">Required.</span></span> <span data-ttu-id="1ee52-165">Muss mit dem Ausgabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ee52-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="1ee52-167">Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="1ee52-167">Number of channels.</span></span></td>
<td><span data-ttu-id="1ee52-168">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-168">Required.</span></span> <span data-ttu-id="1ee52-169">Muss mit dem Ausgabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ee52-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="1ee52-171">Block Ausrichtung (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="1ee52-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="1ee52-172">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-172">Required.</span></span> <span data-ttu-id="1ee52-173">Berechnen Sie den Wert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1ee52-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="1ee52-174"><strong>MFAudioFormat_PCM</strong>: Anzahl der Kanäle × 2.</span><span class="sxs-lookup"><span data-stu-id="1ee52-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="1ee52-175"><strong>MFAudioFormat_Float</strong>: Anzahl der Kanäle × 4.</span><span class="sxs-lookup"><span data-stu-id="1ee52-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ee52-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="1ee52-177">Die Bitrate des codierten AC3-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="1ee52-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="1ee52-178">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ee52-178">Required.</span></span> <span data-ttu-id="1ee52-179">Muss die Block Ausrichtung × Samples pro Sekunde gleich sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ee52-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="1ee52-181">Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="1ee52-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="1ee52-182">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1ee52-182">Optional.</span></span> <span data-ttu-id="1ee52-183">Wenn festgelegt, muss der Wert mit dem Ausgabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ee52-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="1ee52-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="1ee52-185">Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="1ee52-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="1ee52-186">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1ee52-186">Optional.</span></span> <span data-ttu-id="1ee52-187">Wenn dieser Wert festgelegt ist, muss der Wert mit <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1ee52-188">Der Encoder unterstützt keine Stichproben Raten Konvertierung oder Stereo/Mono-Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="1ee52-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ee52-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ee52-189">Remarks</span></span>

<span data-ttu-id="1ee52-190">Jeder Dolby AC-3-audioframe enthält 1536 Audiobeispiele pro Kanal.</span><span class="sxs-lookup"><span data-stu-id="1ee52-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="1ee52-191">Jeder Eingabepuffer für den Encoder kann jedoch eine beliebige Anzahl von PCM-Stichproben enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ee52-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="1ee52-192">Die Größe jedes Eingabe Puffers muss ein Vielfaches der Block Ausrichtung sein.</span><span class="sxs-lookup"><span data-stu-id="1ee52-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="1ee52-193">Der Encoder speichert Eingabe Beispiele zwischen, bis er für 1536-Audiobeispiele pro Kanal genug ist. an diesem Punkt gibt der Encoder einen AC-3-Frame aus.</span><span class="sxs-lookup"><span data-stu-id="1ee52-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="1ee52-194">Jeder Ausgabepuffer enthält einen unformatierten AC-3-Frame.</span><span class="sxs-lookup"><span data-stu-id="1ee52-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="1ee52-195">Die Dauer entspricht der Dauer von 1536 PCM-Stichproben mit der aktuellen Samplingrate (32 MS) um 48 kHz Sample Rate, 34,83 ms bei 44,1 kHz und 48 ms bei 32 kHz).</span><span class="sxs-lookup"><span data-stu-id="1ee52-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="1ee52-196">Die Größe jedes Ausgabepuffers hängt von der Bitrate und der Stichprobenrate ab.</span><span class="sxs-lookup"><span data-stu-id="1ee52-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="1ee52-197">Um die Codierungs Bitrate anzugeben, legen Sie das Attribut [MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) im Ausgabetyp fest.</span><span class="sxs-lookup"><span data-stu-id="1ee52-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="1ee52-198">In der folgenden Tabelle wird die Beziehung zwischen der Codierungs Bitrate und den von MF \_ \_ -MT- \_ \_ Bytes pro Sekunde verfügbaren Bytes angezeigt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1ee52-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="1ee52-199">Bitrate (Kbit/s)</span><span class="sxs-lookup"><span data-stu-id="1ee52-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="1ee52-200">MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="1ee52-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="1ee52-201">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ee52-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1ee52-202">64</span><span class="sxs-lookup"><span data-stu-id="1ee52-202">64</span></span>              | <span data-ttu-id="1ee52-203">8.000</span><span class="sxs-lookup"><span data-stu-id="1ee52-203">8000</span></span>                                                                                     | <span data-ttu-id="1ee52-204">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="1ee52-204">Mono only.</span></span>                                              |
| <span data-ttu-id="1ee52-205">80</span><span class="sxs-lookup"><span data-stu-id="1ee52-205">80</span></span>              | <span data-ttu-id="1ee52-206">10000</span><span class="sxs-lookup"><span data-stu-id="1ee52-206">10000</span></span>                                                                                    | <span data-ttu-id="1ee52-207">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="1ee52-207">Mono only.</span></span>                                              |
| <span data-ttu-id="1ee52-208">96</span><span class="sxs-lookup"><span data-stu-id="1ee52-208">96</span></span>              | <span data-ttu-id="1ee52-209">12000</span><span class="sxs-lookup"><span data-stu-id="1ee52-209">12000</span></span>                                                                                    | <span data-ttu-id="1ee52-210">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="1ee52-210">Mono only.</span></span>                                              |
| <span data-ttu-id="1ee52-211">112</span><span class="sxs-lookup"><span data-stu-id="1ee52-211">112</span></span>             | <span data-ttu-id="1ee52-212">14000</span><span class="sxs-lookup"><span data-stu-id="1ee52-212">14000</span></span>                                                                                    | <span data-ttu-id="1ee52-213">Nur Mono.</span><span class="sxs-lookup"><span data-stu-id="1ee52-213">Mono only.</span></span>                                              |
| <span data-ttu-id="1ee52-214">128</span><span class="sxs-lookup"><span data-stu-id="1ee52-214">128</span></span>             | <span data-ttu-id="1ee52-215">16000</span><span class="sxs-lookup"><span data-stu-id="1ee52-215">16000</span></span>                                                                                    | <span data-ttu-id="1ee52-216">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="1ee52-217">160</span><span class="sxs-lookup"><span data-stu-id="1ee52-217">160</span></span>             | <span data-ttu-id="1ee52-218">20000</span><span class="sxs-lookup"><span data-stu-id="1ee52-218">20000</span></span>                                                                                    | <span data-ttu-id="1ee52-219">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="1ee52-220">192</span><span class="sxs-lookup"><span data-stu-id="1ee52-220">192</span></span>             | <span data-ttu-id="1ee52-221">24.000</span><span class="sxs-lookup"><span data-stu-id="1ee52-221">24000</span></span>                                                                                    | <span data-ttu-id="1ee52-222">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-222">Mono or stereo.</span></span> <span data-ttu-id="1ee52-223">Dies ist die Standardeinstellung für Mono.</span><span class="sxs-lookup"><span data-stu-id="1ee52-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="1ee52-224">224</span><span class="sxs-lookup"><span data-stu-id="1ee52-224">224</span></span>             | <span data-ttu-id="1ee52-225">28000</span><span class="sxs-lookup"><span data-stu-id="1ee52-225">28000</span></span>                                                                                    | <span data-ttu-id="1ee52-226">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="1ee52-227">256</span><span class="sxs-lookup"><span data-stu-id="1ee52-227">256</span></span>             | <span data-ttu-id="1ee52-228">32000</span><span class="sxs-lookup"><span data-stu-id="1ee52-228">32000</span></span>                                                                                    | <span data-ttu-id="1ee52-229">Mono oder Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-229">Mono or stereo.</span></span> <span data-ttu-id="1ee52-230">Dies ist die Standardeinstellung für Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="1ee52-231">320</span><span class="sxs-lookup"><span data-stu-id="1ee52-231">320</span></span>             | <span data-ttu-id="1ee52-232">40.000</span><span class="sxs-lookup"><span data-stu-id="1ee52-232">40000</span></span>                                                                                    | <span data-ttu-id="1ee52-233">Nur Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="1ee52-234">384</span><span class="sxs-lookup"><span data-stu-id="1ee52-234">384</span></span>             | <span data-ttu-id="1ee52-235">48000</span><span class="sxs-lookup"><span data-stu-id="1ee52-235">48000</span></span>                                                                                    | <span data-ttu-id="1ee52-236">Nur Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="1ee52-237">448</span><span class="sxs-lookup"><span data-stu-id="1ee52-237">448</span></span>             | <span data-ttu-id="1ee52-238">56000</span><span class="sxs-lookup"><span data-stu-id="1ee52-238">56000</span></span>                                                                                    | <span data-ttu-id="1ee52-239">Nur Stereo.</span><span class="sxs-lookup"><span data-stu-id="1ee52-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="1ee52-240">Die standardmäßige Codierungs Bitrate ist für Stereo und 192 Kbit/s für Mono auf 256 KBit/s festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ee52-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="1ee52-241">Die Standardeinstellungen werden in den von der [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode des Encoders zurückgegebenen Medientypen widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="1ee52-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="1ee52-242">Beispiel Medientypen</span><span class="sxs-lookup"><span data-stu-id="1ee52-242">Example Media Types</span></span>

<span data-ttu-id="1ee52-243">Im folgenden finden Sie ein Beispiel für die Medientypen, die zum Codieren von ganzzahligen 16-Bit-PCM, 48-kHz-Stereo Audiodaten mit der Standard Bitrate von 256 KBit/s erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1ee52-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="1ee52-244">Ausgabe Medientyp:</span><span class="sxs-lookup"><span data-stu-id="1ee52-244">Output media type:</span></span>

| <span data-ttu-id="1ee52-245">Attribut</span><span class="sxs-lookup"><span data-stu-id="1ee52-245">Attribute</span></span>                                                                           | <span data-ttu-id="1ee52-246">Wert</span><span class="sxs-lookup"><span data-stu-id="1ee52-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="1ee52-247">Haupt-Typ des MF- \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ee52-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="1ee52-248">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="1ee52-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="1ee52-249">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="1ee52-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="1ee52-250">**MF Audioformat \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="1ee52-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="1ee52-251">MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="1ee52-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="1ee52-252">48000</span><span class="sxs-lookup"><span data-stu-id="1ee52-252">48000</span></span>                         |
| [<span data-ttu-id="1ee52-253">MF \_ \_ -MT- \_ audionum- \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="1ee52-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="1ee52-254">2</span><span class="sxs-lookup"><span data-stu-id="1ee52-254">2</span></span>                             |



 

<span data-ttu-id="1ee52-255">Eingabe Medientyp:</span><span class="sxs-lookup"><span data-stu-id="1ee52-255">Input media type:</span></span>

| <span data-ttu-id="1ee52-256">Attribut</span><span class="sxs-lookup"><span data-stu-id="1ee52-256">Attribute</span></span>                                                                                | <span data-ttu-id="1ee52-257">Wert</span><span class="sxs-lookup"><span data-stu-id="1ee52-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="1ee52-258">Haupt-Typ des MF- \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ee52-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="1ee52-259">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="1ee52-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="1ee52-260">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="1ee52-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="1ee52-261">**MF Audioformat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="1ee52-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="1ee52-262">MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel</span><span class="sxs-lookup"><span data-stu-id="1ee52-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="1ee52-263">16</span><span class="sxs-lookup"><span data-stu-id="1ee52-263">16</span></span>                     |
| [<span data-ttu-id="1ee52-264">MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="1ee52-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="1ee52-265">48000</span><span class="sxs-lookup"><span data-stu-id="1ee52-265">48000</span></span>                  |
| [<span data-ttu-id="1ee52-266">MF \_ \_ -MT- \_ audionum- \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="1ee52-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="1ee52-267">2</span><span class="sxs-lookup"><span data-stu-id="1ee52-267">2</span></span>                      |
| [<span data-ttu-id="1ee52-268">MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="1ee52-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="1ee52-269">4</span><span class="sxs-lookup"><span data-stu-id="1ee52-269">4</span></span>                      |
| [<span data-ttu-id="1ee52-270">MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="1ee52-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="1ee52-271">192000</span><span class="sxs-lookup"><span data-stu-id="1ee52-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="1ee52-272">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ee52-272">Requirements</span></span>



| <span data-ttu-id="1ee52-273">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ee52-273">Requirement</span></span> | <span data-ttu-id="1ee52-274">Wert</span><span class="sxs-lookup"><span data-stu-id="1ee52-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee52-275">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ee52-275">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee52-276">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1ee52-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="1ee52-277">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ee52-277">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee52-278">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ee52-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1ee52-279">DLL</span><span class="sxs-lookup"><span data-stu-id="1ee52-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ee52-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ee52-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee52-281">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ee52-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee52-282">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="1ee52-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




