---
description: Der Microsoft Media Foundation MPEG-2-Audioencoder ist eine Media Foundation Transformation, die Mono-oder Stereo-Audiodaten in MPEG-1-Audiodaten (ISO/IEC 11172-3) oder MPEG-2-Audiodaten (ISO/IEC 13818-3) codiert.
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: MPEG-2-Audioencoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863423"
---
# <a name="mpeg-2-audio-encoder"></a><span data-ttu-id="8ee94-103">MPEG-2-Audioencoder</span><span class="sxs-lookup"><span data-stu-id="8ee94-103">MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="8ee94-104">Der Microsoft Media Foundation MPEG-2-Audioencoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die Mono-oder Stereo-Audiodaten in MPEG-1-Audiodaten (ISO/IEC 11172-3) oder MPEG-2-Audiodaten (ISO/IEC 13818-3) codiert.</span><span class="sxs-lookup"><span data-stu-id="8ee94-104">The Microsoft Media Foundation MPEG-2 audio encoder is a [Media Foundation transform](media-foundation-transforms.md) that encodes mono or stereo audio to MPEG-1 audio (ISO/IEC 11172-3) or MPEG-2 audio (ISO/IEC 13818-3).</span></span>

<span data-ttu-id="8ee94-105">Der Encoder unterstützt Layer 1-und Layer 2-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-105">The encoder supports Layer 1 and Layer 2 audio.</span></span> <span data-ttu-id="8ee94-106">MPEG-Layer 3-Audiodatei (MP3) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ee94-106">It does not support MPEG-Layer 3 (MP3) audio.</span></span> <span data-ttu-id="8ee94-107">Für MPEG-2 unterstützt der Encoder den LSF-Teil (Low Sampling Häufigkeits) von MPEG-2-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-107">For MPEG-2, the encoder supports the Low Sampling Frequencies (LSF) portion of MPEG-2 audio.</span></span> <span data-ttu-id="8ee94-108">Die Multichannel-Erweiterungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ee94-108">It does not support the multichannel extensions.</span></span> <span data-ttu-id="8ee94-109">Der MFT gibt einen MPEG-elementaren Stream aus.</span><span class="sxs-lookup"><span data-stu-id="8ee94-109">The MFT outputs an MPEG elementary stream.</span></span> <span data-ttu-id="8ee94-110">Es können keine Legenden Datenströme, Programmstreams oder Transportdaten Ströme erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8ee94-110">It cannot generate packetized elementary streams, program streams, or transport streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="8ee94-111">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8ee94-111">Class Identifier</span></span>

<span data-ttu-id="8ee94-112">Der Klassen Bezeichner (CLSID) des mepg-2-Audioencoders ist **CLSID- \_ CMPEG2AudioEncoderMFT**, die in der Header Datei "wmcodecdsp. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8ee94-112">The class identifier (CLSID) of the MEPG-2 audio encoder is **CLSID\_CMPEG2AudioEncoderMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="8ee94-113">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="8ee94-113">Output Types</span></span>

<span data-ttu-id="8ee94-114">Der Ausgabetyp muss zuerst festgelegt werden, vor dem Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="8ee94-114">The output type must be set first, before the input type.</span></span> <span data-ttu-id="8ee94-115">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabe Medientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ee94-115">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ee94-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="8ee94-116">Attribute</span></span></th>
<th><span data-ttu-id="8ee94-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ee94-117">Description</span></span></th>
<th><span data-ttu-id="8ee94-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee94-118">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ee94-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="8ee94-120">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="8ee94-120">Major type.</span></span></td>
<td><span data-ttu-id="8ee94-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-121">Required.</span></span> <span data-ttu-id="8ee94-122">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="8ee94-122">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee94-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="8ee94-124">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="8ee94-124">Audio subtype.</span></span></td>
<td><span data-ttu-id="8ee94-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-125">Required.</span></span> <span data-ttu-id="8ee94-126">Muss <strong>MFAudioFormat_MPEG</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="8ee94-126">Must be <strong>MFAudioFormat_MPEG</strong>.</span></span> <span data-ttu-id="8ee94-127">Dieser Untertyp wird sowohl für MPEG-1-als auch für MPEG-2-Audiodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ee94-127">This subtype is used for both MPEG-1 and MPEG-2 audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee94-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="8ee94-129">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-129">Samples per second.</span></span></td>
<td><span data-ttu-id="8ee94-130">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-130">Required.</span></span> <span data-ttu-id="8ee94-131">Die folgenden Werte werden sowohl für MPEG-1 als auch für MPEG-2 unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8ee94-131">The following values are supported for both MPEG-1 and MPEG-2:</span></span>
<ul>
<li><span data-ttu-id="8ee94-132">32000</span><span class="sxs-lookup"><span data-stu-id="8ee94-132">32000</span></span></li>
<li><span data-ttu-id="8ee94-133">44100</span><span class="sxs-lookup"><span data-stu-id="8ee94-133">44100</span></span></li>
<li><span data-ttu-id="8ee94-134">48000</span><span class="sxs-lookup"><span data-stu-id="8ee94-134">48000</span></span></li>
</ul>
<span data-ttu-id="8ee94-135">Außerdem werden die folgenden Werte für MPEG-2 LSF unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8ee94-135">In addition, the following values are supported for MPEG-2 LSF:</span></span> <br/>
<ul>
<li><span data-ttu-id="8ee94-136">16000</span><span class="sxs-lookup"><span data-stu-id="8ee94-136">16000</span></span></li>
<li><span data-ttu-id="8ee94-137">22050</span><span class="sxs-lookup"><span data-stu-id="8ee94-137">22050</span></span></li>
<li><span data-ttu-id="8ee94-138">24.000</span><span class="sxs-lookup"><span data-stu-id="8ee94-138">24000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee94-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="8ee94-140">Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="8ee94-140">Number of channels.</span></span></td>
<td><span data-ttu-id="8ee94-141">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-141">Required.</span></span> <span data-ttu-id="8ee94-142">Muss entweder 1 (Mono) oder 2 (Stereo) sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-142">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee94-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="8ee94-144">Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="8ee94-144">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="8ee94-145">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ee94-145">Optional.</span></span> <span data-ttu-id="8ee94-146">Wenn festgelegt, muss der Wert 0x3 für Stereo (Front Left und Right Channels) oder 0x4 für Mono (Front-Center-Kanal) lauten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-146">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee94-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="8ee94-148">Die Bitrate des codierten MPEG-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-148">Bit rate of the encoded MPEG stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="8ee94-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ee94-149">Optional.</span></span><br/> <span data-ttu-id="8ee94-150">Die Spezifikationen ISO/IEC 11172-3 und ISO/IEC 13818-3 (LSF) definieren verschiedene Bitraten, abhängig von der Abtastrate, der Anzahl der Kanäle und der Audioschicht (1 oder 2).</span><span class="sxs-lookup"><span data-stu-id="8ee94-150">The ISO/IEC 11172-3 and ISO/IEC 13818-3 (LSF) specifications define several bit rates, depending on the sampling rate, the number of channels, and the audio layer (1 or 2).</span></span> <br/> <span data-ttu-id="8ee94-151">Der Encoder verwendet standardmäßig Layer 2-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-151">The encoder defaults to Layer 2 audio.</span></span> <span data-ttu-id="8ee94-152">Wenn das <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> -Attribut nicht festgelegt ist, verwendet der Encoder die folgenden Standard Bitraten:</span><span class="sxs-lookup"><span data-stu-id="8ee94-152">If the <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> attribute is not set, the encoder uses the following default bit rates:</span></span><br/>
<ul>
<li><span data-ttu-id="8ee94-153">MPEG-1 Stereo: 224.000 Bits pro Sekunde (Bit/s) = 28.000 Byte pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-153">MPEG-1 stereo: 224,000 bits per second (bps) = 28,000 bytes per second.</span></span></li>
<li><span data-ttu-id="8ee94-154">MPEG-1 Mono: 192.000 Bit/s = 24.000 Byte pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-154">MPEG-1 mono: 192,000 bps = 24,000 bytes per second.</span></span></li>
<li><span data-ttu-id="8ee94-155">MPEG-2 LSF, Mono oder Stereo: 160.000 Bit/s = 20.000 Byte pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-155">MPEG-2 LSF, mono or stereo: 160,000 bps = 20,000 bytes per second.</span></span></li>
</ul>
<span data-ttu-id="8ee94-156">Dieses Attribut kann auf andere Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8ee94-156">This attribute can be set to other values.</span></span> <span data-ttu-id="8ee94-157">Wenn der Wert gemäß den MPEG-Spezifikationen ungültig ist, lehnt der MFT den Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="8ee94-157">If the value is not valid according to MPEG specifications, the MFT will reject the media type.</span></span><br/> <span data-ttu-id="8ee94-158">Sie können auch die Bitrate mithilfe der <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>icodecapi</strong></a> -Schnittstelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ee94-158">You can also set the bit rate by using the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> interface.</span></span> <span data-ttu-id="8ee94-159">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8ee94-159">See Remarks for more information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8ee94-160">Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder Sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-160">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="8ee94-161">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="8ee94-161">Input Types</span></span>

<span data-ttu-id="8ee94-162">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabe Medientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ee94-162">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ee94-163">Attribut</span><span class="sxs-lookup"><span data-stu-id="8ee94-163">Attribute</span></span></th>
<th><span data-ttu-id="8ee94-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ee94-164">Description</span></span></th>
<th><span data-ttu-id="8ee94-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee94-165">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ee94-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="8ee94-167">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="8ee94-167">Major type.</span></span></td>
<td><span data-ttu-id="8ee94-168">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-168">Required.</span></span> <span data-ttu-id="8ee94-169">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="8ee94-169">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee94-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="8ee94-171">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="8ee94-171">Audio subtype.</span></span></td>
<td><span data-ttu-id="8ee94-172">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-172">Required.</span></span> <span data-ttu-id="8ee94-173">Muss <strong>MFAudioFormat_PCM</strong> oder <strong>MFAudioFormat_Float</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-173">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee94-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="8ee94-175">Anzahl von Bits pro audiostich Probe.</span><span class="sxs-lookup"><span data-stu-id="8ee94-175">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="8ee94-176">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-176">Required.</span></span> <span data-ttu-id="8ee94-177">Der Wert muss 16 sein, wenn der Untertyp <strong>MFAudioFormat_PCM</strong>ist, oder 32, wenn der Untertyp <strong>MFAudioFormat_Float</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="8ee94-177">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee94-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="8ee94-179">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-179">Samples per second.</span></span></td>
<td><span data-ttu-id="8ee94-180">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-180">Required.</span></span> <span data-ttu-id="8ee94-181">Muss mit dem Ausgabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-181">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee94-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="8ee94-183">Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="8ee94-183">Number of channels.</span></span></td>
<td><span data-ttu-id="8ee94-184">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-184">Required.</span></span> <span data-ttu-id="8ee94-185">Muss mit dem Ausgabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-185">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee94-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="8ee94-187">Block Ausrichtung (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="8ee94-187">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="8ee94-188">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-188">Required.</span></span> <span data-ttu-id="8ee94-189">Berechnen Sie den Wert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8ee94-189">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="8ee94-190"><strong>MFAudioFormat_PCM</strong>: Anzahl der Kanäle × 2.</span><span class="sxs-lookup"><span data-stu-id="8ee94-190"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="8ee94-191"><strong>MFAudioFormat_Float</strong>: Anzahl der Kanäle × 4.</span><span class="sxs-lookup"><span data-stu-id="8ee94-191"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee94-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="8ee94-193">Die Bitrate des codierten AC3-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-193">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="8ee94-194">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ee94-194">Required.</span></span> <span data-ttu-id="8ee94-195">Muss die Block Ausrichtung × Samples pro Sekunde gleich sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-195">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee94-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="8ee94-197">Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="8ee94-197">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="8ee94-198">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ee94-198">Optional.</span></span> <span data-ttu-id="8ee94-199">Wenn festgelegt, muss der Wert mit dem Ausgabetyp identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-199">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee94-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="8ee94-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="8ee94-201">Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="8ee94-201">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="8ee94-202">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ee94-202">Optional.</span></span> <span data-ttu-id="8ee94-203">Wenn dieser Wert festgelegt ist, muss der Wert mit <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-203">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8ee94-204">Der Encoder unterstützt keine Stichproben Raten Konvertierung oder Stereo/Mono-Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="8ee94-204">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span> <span data-ttu-id="8ee94-205">Wenn die optionalen Attribute nicht festgelegt sind, fügt der Encoder Sie dem Medientyp hinzu, nachdem der Typ festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8ee94-205">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="8ee94-206">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ee94-206">Codec Properties</span></span>

<span data-ttu-id="8ee94-207">Der Encoder unterstützt die folgenden Eigenschaften über die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8ee94-207">The encoder supports the following properties through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>



| <span data-ttu-id="8ee94-208">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ee94-208">Property</span></span>                                                                                | <span data-ttu-id="8ee94-209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ee94-209">Description</span></span>                                                                                      | <span data-ttu-id="8ee94-210">Standardwert</span><span class="sxs-lookup"><span data-stu-id="8ee94-210">Default value</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ee94-211">Codecapi \_ avenccommonmeanbitrate</span><span class="sxs-lookup"><span data-stu-id="8ee94-211">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)               | <span data-ttu-id="8ee94-212">Gibt die durchschnittliche codierte Bitrate in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="8ee94-212">Specifies the average encoded bit rate, in bits per second.</span></span>                                      | <span data-ttu-id="8ee94-213">Wie für das Attribut [MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) im Ausgabe Medientyp beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8ee94-213">As described for the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output media type.</span></span>                      |
| [<span data-ttu-id="8ee94-214">Codecapi \_ avencmpacodingmode</span><span class="sxs-lookup"><span data-stu-id="8ee94-214">CODECAPI\_AVEncMPACodingMode</span></span>](../directshow/avencmpacodingmode-property.md)                       | <span data-ttu-id="8ee94-215">Gibt den MPEG-audiocodierungs Modus an.</span><span class="sxs-lookup"><span data-stu-id="8ee94-215">Specifies the MPEG audio encoding mode.</span></span>                                                          | <span data-ttu-id="8ee94-216">Stereo für 2-Kanal-Audiodaten oder einzelner Kanal für 1-Kanal-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-216">Stereo for 2-channel audio, or single channel for 1-channel audio.</span></span><br/> <span data-ttu-id="8ee94-217">Für zweistufige Audiodaten unterstützt der Encoder auch Dual Kanäle und Joint Stereo.</span><span class="sxs-lookup"><span data-stu-id="8ee94-217">For 2-channel audio, the encoder also supports dual channel and joint stereo.</span></span><br/> |
| [<span data-ttu-id="8ee94-218">Codecapi \_ avencmpacopyright</span><span class="sxs-lookup"><span data-stu-id="8ee94-218">CODECAPI\_AVEncMPACopyright</span></span>](../directshow/avencmpacopyright-property.md)                         | <span data-ttu-id="8ee94-219">Gibt an, ob das Copyright-Bit im MPEG-Audiostream festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8ee94-219">Specifies whether to set the copyright bit in the MPEG audio stream.</span></span>                             | <span data-ttu-id="8ee94-220">Kein Copyright.</span><span class="sxs-lookup"><span data-stu-id="8ee94-220">No copyright.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="8ee94-221">Codecapi \_ avencmpbetonung sType</span><span class="sxs-lookup"><span data-stu-id="8ee94-221">CODECAPI\_AVEncMPAEmphasisType</span></span>](../directshow/avencmpaemphasistype-property.md)                   | <span data-ttu-id="8ee94-222">Gibt den Typ des deduplizierungsfilters an, der verwendet werden soll, wenn der codierte Stream decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="8ee94-222">Specifies the type of de-emphasis filter that should be used when the encoded stream is decoded.</span></span> | <span data-ttu-id="8ee94-223">Es wurde kein Schwerpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ee94-223">No emphasis specified.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="8ee94-224">Avencmpenableredundancyprotection</span><span class="sxs-lookup"><span data-stu-id="8ee94-224">AVEncMPAEnableRedundancyProtection</span></span>](../directshow/avencmpaenableredundancyprotection-property.md) | <span data-ttu-id="8ee94-225">Gibt an, ob dem Frame Header eine zyklische Redundanz Überprüfung (CRC) hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee94-225">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span>                    | <span data-ttu-id="8ee94-226">Eine CRC-Prüfsumme wird in den Bitstream geschrieben.</span><span class="sxs-lookup"><span data-stu-id="8ee94-226">A CRC checksum is written to the bit stream.</span></span>                                                                                                                           |
| [<span data-ttu-id="8ee94-227">Codecapi \_ avencmpalayer</span><span class="sxs-lookup"><span data-stu-id="8ee94-227">CODECAPI\_AVEncMPALayer</span></span>](../directshow/avencmpalayer-property.md)                                 | <span data-ttu-id="8ee94-228">Gibt die MPEG-Audioschicht an.</span><span class="sxs-lookup"><span data-stu-id="8ee94-228">Specifies the MPEG audio layer.</span></span>                                                                  | <span data-ttu-id="8ee94-229">Layer 2-Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="8ee94-229">Layer 2 audio.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="8ee94-230">Codecapi \_ avencmporiginalbitstream</span><span class="sxs-lookup"><span data-stu-id="8ee94-230">CODECAPI\_AVEncMPAOriginalBitstream</span></span>](../directshow/avencmpaoriginalbitstream-property.md)         | <span data-ttu-id="8ee94-231">Gibt an, ob für das ursprüngliche Bit im MPEG-Audiostream festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee94-231">Specifies whether to set for the original bit in the MPEG audio stream.</span></span>                          | <span data-ttu-id="8ee94-232">"Ursprüngliches" Bit ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8ee94-232">"Original" bit is off.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="8ee94-233">Codecapi \_ avencmpaprivateuserbit</span><span class="sxs-lookup"><span data-stu-id="8ee94-233">CODECAPI\_AVEncMPAPrivateUserBit</span></span>](../directshow/avencmpaprivateuserbit-property.md)               | <span data-ttu-id="8ee94-234">Gibt an, ob für das private Benutzer Bit im MPEG-Audiostream festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee94-234">Specifies whether to set for the private user bit in the MPEG audio stream.</span></span>                      | <span data-ttu-id="8ee94-235">Privates Benutzer Bit ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8ee94-235">Private user bit is off.</span></span>                                                                                                                                               |



 

<span data-ttu-id="8ee94-236">Um einen Zeiger auf die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle abzurufen, nennen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der MFT.</span><span class="sxs-lookup"><span data-stu-id="8ee94-236">To get a pointer to the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the MFT.</span></span>

<span data-ttu-id="8ee94-237">Die MFT implementiert die folgenden [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="8ee94-237">The MFT implements the following [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods:</span></span>

-   [<span data-ttu-id="8ee94-238">**Getparameterrange**</span><span class="sxs-lookup"><span data-stu-id="8ee94-238">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="8ee94-239">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="8ee94-239">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [<span data-ttu-id="8ee94-240">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="8ee94-240">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="8ee94-241">**Ismodifizierbar**</span><span class="sxs-lookup"><span data-stu-id="8ee94-241">**IsModifiable**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [<span data-ttu-id="8ee94-242">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="8ee94-242">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="8ee94-243">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="8ee94-243">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

<span data-ttu-id="8ee94-244">Alle anderen [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Methoden geben **E \_ notimpl** zurück.</span><span class="sxs-lookup"><span data-stu-id="8ee94-244">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods return **E\_NOTIMPL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee94-245">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee94-245">Remarks</span></span>

<span data-ttu-id="8ee94-246">Jeder MPEG-audioframe enthält entweder 384 (Layer 1)-oder 1152 (Layer 2)-Audiobeispiele pro Kanal.</span><span class="sxs-lookup"><span data-stu-id="8ee94-246">Each MPEG audio frame contains either 384 (Layer 1) or 1152 (Layer 2) audio samples per channel.</span></span> <span data-ttu-id="8ee94-247">Jeder Eingabepuffer für den Encoder kann jedoch eine beliebige Anzahl von PCM-Stichproben enthalten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-247">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="8ee94-248">Die Größe jedes Eingabe Puffers muss ein Vielfaches der Block Ausrichtung sein.</span><span class="sxs-lookup"><span data-stu-id="8ee94-248">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="8ee94-249">Der Encoder speichert Eingabe Beispiele zwischen, bis er für einen MPEG-audioframe ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="8ee94-249">The encoder caches input samples until it has enough for an MPEG audio frame.</span></span>

<span data-ttu-id="8ee94-250">Jeder Ausgabepuffer enthält einen unformatierten MPEG-Frame.</span><span class="sxs-lookup"><span data-stu-id="8ee94-250">Each output buffer contains one raw MPEG frame.</span></span> <span data-ttu-id="8ee94-251">Die Größe jedes Ausgabepuffers hängt von der Bitrate und der Stichprobenrate ab.</span><span class="sxs-lookup"><span data-stu-id="8ee94-251">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

### <a name="configuring-the-encoder"></a><span data-ttu-id="8ee94-252">Konfigurieren des Encoders</span><span class="sxs-lookup"><span data-stu-id="8ee94-252">Configuring the Encoder</span></span>

<span data-ttu-id="8ee94-253">Um die Standardeinstellungen für den Encoder zu ändern, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8ee94-253">To change any of the default settings on the encoder, perform the following steps:</span></span>

1.  <span data-ttu-id="8ee94-254">Erstellen Sie eine Instanz des MFT-Encoders.</span><span class="sxs-lookup"><span data-stu-id="8ee94-254">Create an instance of the encoder MFT.</span></span>
2.  <span data-ttu-id="8ee94-255">Aufrufen von [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , um die Liste der bevorzugten Ausgabetypen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-255">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of the preferred output types.</span></span> <span data-ttu-id="8ee94-256">Der Encoder listet alle Stichproben Raten für Mono und Stereo auf.</span><span class="sxs-lookup"><span data-stu-id="8ee94-256">The encoder enumerates all sample rates for both mono and stereo.</span></span> <span data-ttu-id="8ee94-257">Wählen Sie basierend auf der Samplingrate und der Anzahl der Kanäle einen der folgenden Medientypen aus.</span><span class="sxs-lookup"><span data-stu-id="8ee94-257">Select one of these media types, based on the sample rate and number of channels.</span></span> <span data-ttu-id="8ee94-258">Das Attribut " [MF \_ MT \_ audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) " gibt die Standard Bitrate in Byte pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="8ee94-258">The [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute indicates the default bit rate, in bytes per second.</span></span>
3.  <span data-ttu-id="8ee94-259">Optional: Sie können die standardbitrate überschreiben, indem Sie für den Ausgabe Medientyp einen neuen Wert für " [MF \_ MT \_ -audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ee94-259">Optional: You can override the default bit rate by setting a new value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) on the output media type.</span></span> <span data-ttu-id="8ee94-260">Gültige Bitraten sind abhängig von der Abtastrate, der Anzahl der Kanäle und der Audioschicht.</span><span class="sxs-lookup"><span data-stu-id="8ee94-260">Valid bit rates depend on the sample rate, number of channels, and audio layer.</span></span>
    > [!Note]  
    > <span data-ttu-id="8ee94-261">An dieser Stelle im Konfigurationsprozess verwendet der Encoder standardmäßig Layer 2-Audiodaten und akzeptiert nur Layer 2-Bitraten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-261">At this point in the configuration process, the encoder defaults to Layer 2 audio and will only accept Layer 2 bit rates.</span></span> <span data-ttu-id="8ee94-262">In einem späteren Schritt können Sie den Encoder auf Schicht 1 umstellen (siehe Schritt 7).</span><span class="sxs-lookup"><span data-stu-id="8ee94-262">You will be able to switch the encoder to Layer 1 in a later step (see step 7).</span></span> <span data-ttu-id="8ee94-263">Überlassen Sie in diesem Fall die Standard Bitrate für jetzt. Sie können Sie in Schritt 8 wieder ändern.</span><span class="sxs-lookup"><span data-stu-id="8ee94-263">In that case, leave the default bit rate for now; you can change it again in step 8.</span></span>

     

4.  <span data-ttu-id="8ee94-264">Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) zum Festlegen des Ausgabemedien Typs.</span><span class="sxs-lookup"><span data-stu-id="8ee94-264">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the output media type.</span></span> <span data-ttu-id="8ee94-265">Wenn Sie einen eigenen Wert für " [MF \_ MT \_ -audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde](mf-mt-audio-avg-bytes-per-second-attribute.md) " festlegen und der MFT den Ausgabe Medientyp ablehnt, liegt dies wahrscheinlich daran, dass Sie eine ungültige Bitrate angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="8ee94-265">If you set your own value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) and the MFT rejects the output media type, it is likely because you specified an invalid bit rate.</span></span>
5.  <span data-ttu-id="8ee94-266">Aufrufen von [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) zum Aufzählen des Eingabemedien Typs.</span><span class="sxs-lookup"><span data-stu-id="8ee94-266">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to enumerate the input media type.</span></span> <span data-ttu-id="8ee94-267">Da die Stichprobenrate und die Anzahl der Kanäle mit dem Ausgabetyp identisch sein müssen, werden nur zwei Optionen aufgelistet: 32-Bit-Gleit Komma-PCM-Eingabe und 32-Bit-ganzzahlige PCM-Eingabe.</span><span class="sxs-lookup"><span data-stu-id="8ee94-267">Because the sample rate and number of channels must be identical to the output type, only two options are enumerated: 32-bit floating-point PCM input and 16-bit integer PCM input.</span></span> <span data-ttu-id="8ee94-268">Wählen Sie eine der folgenden aus.</span><span class="sxs-lookup"><span data-stu-id="8ee94-268">Select one of these.</span></span>
6.  <span data-ttu-id="8ee94-269">Greifen Sie auf [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) zu, um den Eingabe Medientyp festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8ee94-269">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the input media type.</span></span>
7.  <span data-ttu-id="8ee94-270">Optional: Legen Sie zum Codieren von Layer-1-Audiodaten die [codecapi-Eigenschaft " \_ avencmpalayer](../directshow/avencmpalayer-property.md) " auf **eavencmpalayer \_ 1** fest.</span><span class="sxs-lookup"><span data-stu-id="8ee94-270">Optional: To encode Layer 1 audio, set the [CODECAPI\_AVEncMPALayer](../directshow/avencmpalayer-property.md) property to **eAVEncMPALayer\_1**.</span></span>
8.  <span data-ttu-id="8ee94-271">Optional: um die Bitrate zu ändern, legen Sie die [codecapi-Eigenschaft " \_ avenccommonmeanbitrate](../directshow/avenccommonmeanbitrate-property.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="8ee94-271">Optional: To change the bit rate, set the [CODECAPI\_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <span data-ttu-id="8ee94-272">Die Bitrate muss eine der gültigen Bitraten sein, die in den LSF-Spezifikationen MPEG-1 oder MPEG-2 aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8ee94-272">The bit rate must be one of the valid bit rates listed in the MPEG-1 or MPEG-2 LSF specifications.</span></span> <span data-ttu-id="8ee94-273">Alternativ können Sie [**icodecapi:: getParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) aufrufen, um eine Liste gültiger Bitraten basierend auf den aktuellen Einstellungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8ee94-273">Alternatively, you can call [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) to get a list of valid bit rates, based on the current settings.</span></span>
9.  <span data-ttu-id="8ee94-274">Optional: mit der 2-Kanal-Audiodatei können Sie die [codecapi-Eigenschaft " \_ avencmpacodingmode](../directshow/avencmpacodingmode-property.md) " festlegen, um den Codierungs Modus in den dualen Kanal oder den gemeinsamen Stereo zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8ee94-274">Optional: With 2-channel audio, you can set the [CODECAPI\_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) property to change the coding mode to dual channel or joint stereo.</span></span> <span data-ttu-id="8ee94-275">Sie können [**icodecapi:: getparameterrange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) aufrufen, um die gültigen Optionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-275">You can call [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) to get the valid options.</span></span> <span data-ttu-id="8ee94-276">(Für eine audioaudioschnittstelle ist die einzige Option Mono.)</span><span class="sxs-lookup"><span data-stu-id="8ee94-276">(For 1-channel audio, the only option is mono.)</span></span>
10. <span data-ttu-id="8ee94-277">Optional: Legen Sie alle anderen zuvor aufgeführten [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="8ee94-277">Optional: Set any of the other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties listed previously.</span></span>

<span data-ttu-id="8ee94-278">Es ist wichtig, die Reihenfolge dieser Schritte zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="8ee94-278">It is important to follow the order of these steps.</span></span> <span data-ttu-id="8ee94-279">Legen Sie insbesondere den Ausgabe Medientyp vor dem Ändern von [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="8ee94-279">In particular, set the output media type before changing any [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties.</span></span> <span data-ttu-id="8ee94-280">Außerdem müssen Sie die **icodecapi** -Eigenschaften festlegen, bevor das erste Eingabe Beispiel vom MFT empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="8ee94-280">Also, you must set **ICodecAPI** properties before the MFT receives the first input sample.</span></span> <span data-ttu-id="8ee94-281">Nachdem die MFT Eingaben empfangen hat, sind die Codec-Eigenschaften schreibgeschützt, und [**icodecapi:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) gibt den Wert **S \_ false** zurück.</span><span class="sxs-lookup"><span data-stu-id="8ee94-281">After the MFT receives input, the codec properties are read-only, and [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) returns the value **S\_FALSE**.</span></span>

### <a name="supported-bit-rates"></a><span data-ttu-id="8ee94-282">Unterstützte Bitraten</span><span class="sxs-lookup"><span data-stu-id="8ee94-282">Supported Bit Rates</span></span>

<span data-ttu-id="8ee94-283">Der Encoder unterstützt die folgenden Bitraten.</span><span class="sxs-lookup"><span data-stu-id="8ee94-283">The encoder supports the following bit rates.</span></span>



<span data-ttu-id="8ee94-284">MPEG-1</span><span class="sxs-lookup"><span data-stu-id="8ee94-284">MPEG-1</span></span>

<span data-ttu-id="8ee94-285">MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8ee94-285">MPEG-2</span></span>

<span data-ttu-id="8ee94-286">Ebene 1</span><span class="sxs-lookup"><span data-stu-id="8ee94-286">Layer 1</span></span>

<span data-ttu-id="8ee94-287">Layer 2-</span><span class="sxs-lookup"><span data-stu-id="8ee94-287">Layer 2</span></span>

<span data-ttu-id="8ee94-288">Ebene 1</span><span class="sxs-lookup"><span data-stu-id="8ee94-288">Layer 1</span></span>

<span data-ttu-id="8ee94-289">Layer 2-</span><span class="sxs-lookup"><span data-stu-id="8ee94-289">Layer 2</span></span>

<span data-ttu-id="8ee94-290">32</span><span class="sxs-lookup"><span data-stu-id="8ee94-290">32</span></span>

<span data-ttu-id="8ee94-291">32\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-291">32\*</span></span>

<span data-ttu-id="8ee94-292">32</span><span class="sxs-lookup"><span data-stu-id="8ee94-292">32</span></span>

<span data-ttu-id="8ee94-293">8</span><span class="sxs-lookup"><span data-stu-id="8ee94-293">8</span></span>

<span data-ttu-id="8ee94-294">64</span><span class="sxs-lookup"><span data-stu-id="8ee94-294">64</span></span>

<span data-ttu-id="8ee94-295">48\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-295">48\*</span></span>

<span data-ttu-id="8ee94-296">38</span><span class="sxs-lookup"><span data-stu-id="8ee94-296">38</span></span>

<span data-ttu-id="8ee94-297">16</span><span class="sxs-lookup"><span data-stu-id="8ee94-297">16</span></span>

<span data-ttu-id="8ee94-298">96</span><span class="sxs-lookup"><span data-stu-id="8ee94-298">96</span></span>

<span data-ttu-id="8ee94-299">56\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-299">56\*</span></span>

<span data-ttu-id="8ee94-300">56</span><span class="sxs-lookup"><span data-stu-id="8ee94-300">56</span></span>

<span data-ttu-id="8ee94-301">24</span><span class="sxs-lookup"><span data-stu-id="8ee94-301">24</span></span>

<span data-ttu-id="8ee94-302">128</span><span class="sxs-lookup"><span data-stu-id="8ee94-302">128</span></span>

<span data-ttu-id="8ee94-303">64</span><span class="sxs-lookup"><span data-stu-id="8ee94-303">64</span></span>

<span data-ttu-id="8ee94-304">64</span><span class="sxs-lookup"><span data-stu-id="8ee94-304">64</span></span>

<span data-ttu-id="8ee94-305">32</span><span class="sxs-lookup"><span data-stu-id="8ee94-305">32</span></span>

<span data-ttu-id="8ee94-306">160</span><span class="sxs-lookup"><span data-stu-id="8ee94-306">160</span></span>

<span data-ttu-id="8ee94-307">80\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-307">80\*</span></span>

<span data-ttu-id="8ee94-308">80</span><span class="sxs-lookup"><span data-stu-id="8ee94-308">80</span></span>

<span data-ttu-id="8ee94-309">40</span><span class="sxs-lookup"><span data-stu-id="8ee94-309">40</span></span>

<span data-ttu-id="8ee94-310">192</span><span class="sxs-lookup"><span data-stu-id="8ee94-310">192</span></span>

<span data-ttu-id="8ee94-311">96</span><span class="sxs-lookup"><span data-stu-id="8ee94-311">96</span></span>

<span data-ttu-id="8ee94-312">96</span><span class="sxs-lookup"><span data-stu-id="8ee94-312">96</span></span>

<span data-ttu-id="8ee94-313">48</span><span class="sxs-lookup"><span data-stu-id="8ee94-313">48</span></span>

<span data-ttu-id="8ee94-314">224</span><span class="sxs-lookup"><span data-stu-id="8ee94-314">224</span></span>

<span data-ttu-id="8ee94-315">112</span><span class="sxs-lookup"><span data-stu-id="8ee94-315">112</span></span>

<span data-ttu-id="8ee94-316">112</span><span class="sxs-lookup"><span data-stu-id="8ee94-316">112</span></span>

<span data-ttu-id="8ee94-317">56</span><span class="sxs-lookup"><span data-stu-id="8ee94-317">56</span></span>

<span data-ttu-id="8ee94-318">256</span><span class="sxs-lookup"><span data-stu-id="8ee94-318">256</span></span>

<span data-ttu-id="8ee94-319">128</span><span class="sxs-lookup"><span data-stu-id="8ee94-319">128</span></span>

<span data-ttu-id="8ee94-320">128</span><span class="sxs-lookup"><span data-stu-id="8ee94-320">128</span></span>

<span data-ttu-id="8ee94-321">64</span><span class="sxs-lookup"><span data-stu-id="8ee94-321">64</span></span>

<span data-ttu-id="8ee94-322">288</span><span class="sxs-lookup"><span data-stu-id="8ee94-322">288</span></span>

<span data-ttu-id="8ee94-323">160</span><span class="sxs-lookup"><span data-stu-id="8ee94-323">160</span></span>

<span data-ttu-id="8ee94-324">144</span><span class="sxs-lookup"><span data-stu-id="8ee94-324">144</span></span>

<span data-ttu-id="8ee94-325">80</span><span class="sxs-lookup"><span data-stu-id="8ee94-325">80</span></span>

<span data-ttu-id="8ee94-326">320</span><span class="sxs-lookup"><span data-stu-id="8ee94-326">320</span></span>

<span data-ttu-id="8ee94-327">192</span><span class="sxs-lookup"><span data-stu-id="8ee94-327">192</span></span>

<span data-ttu-id="8ee94-328">160</span><span class="sxs-lookup"><span data-stu-id="8ee94-328">160</span></span>

<span data-ttu-id="8ee94-329">96</span><span class="sxs-lookup"><span data-stu-id="8ee94-329">96</span></span>

<span data-ttu-id="8ee94-330">352</span><span class="sxs-lookup"><span data-stu-id="8ee94-330">352</span></span>

<span data-ttu-id="8ee94-331">224\*\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-331">224\*\*</span></span>

<span data-ttu-id="8ee94-332">176</span><span class="sxs-lookup"><span data-stu-id="8ee94-332">176</span></span>

<span data-ttu-id="8ee94-333">112</span><span class="sxs-lookup"><span data-stu-id="8ee94-333">112</span></span>

<span data-ttu-id="8ee94-334">384</span><span class="sxs-lookup"><span data-stu-id="8ee94-334">384</span></span>

<span data-ttu-id="8ee94-335">256\*\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-335">256\*\*</span></span>

<span data-ttu-id="8ee94-336">192</span><span class="sxs-lookup"><span data-stu-id="8ee94-336">192</span></span>

<span data-ttu-id="8ee94-337">128</span><span class="sxs-lookup"><span data-stu-id="8ee94-337">128</span></span>

<span data-ttu-id="8ee94-338">416</span><span class="sxs-lookup"><span data-stu-id="8ee94-338">416</span></span>

<span data-ttu-id="8ee94-339">230\*\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-339">230\*\*</span></span>

<span data-ttu-id="8ee94-340">224</span><span class="sxs-lookup"><span data-stu-id="8ee94-340">224</span></span>

<span data-ttu-id="8ee94-341">144</span><span class="sxs-lookup"><span data-stu-id="8ee94-341">144</span></span>

<span data-ttu-id="8ee94-342">448</span><span class="sxs-lookup"><span data-stu-id="8ee94-342">448</span></span>

<span data-ttu-id="8ee94-343">384\*\*</span><span class="sxs-lookup"><span data-stu-id="8ee94-343">384\*\*</span></span>

<span data-ttu-id="8ee94-344">256</span><span class="sxs-lookup"><span data-stu-id="8ee94-344">256</span></span>

<span data-ttu-id="8ee94-345">160</span><span class="sxs-lookup"><span data-stu-id="8ee94-345">160</span></span>



 

<dl> <span data-ttu-id="8ee94-346">\* Nur Mono</span><span class="sxs-lookup"><span data-stu-id="8ee94-346">\* Mono only</span></span>  
<span data-ttu-id="8ee94-347">\*\* Nur Stereo</span><span class="sxs-lookup"><span data-stu-id="8ee94-347">\*\* Stereo only</span></span>  
</dl>

### <a name="example-media-types"></a><span data-ttu-id="8ee94-348">Beispiel Medientypen</span><span class="sxs-lookup"><span data-stu-id="8ee94-348">Example Media Types</span></span>

<span data-ttu-id="8ee94-349">Im folgenden finden Sie ein Beispiel für die Medientypen, die zum Codieren von ganzzahligen 16-Bit-PCM, 48-kHz-Stereo Audiodaten mit der Standard Bitrate benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ee94-349">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate.</span></span>

<span data-ttu-id="8ee94-350">Ausgabe Medientyp:</span><span class="sxs-lookup"><span data-stu-id="8ee94-350">Output media type:</span></span>

| <span data-ttu-id="8ee94-351">Attribut</span><span class="sxs-lookup"><span data-stu-id="8ee94-351">Attribute</span></span>                                                                           | <span data-ttu-id="8ee94-352">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee94-352">Value</span></span>                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [<span data-ttu-id="8ee94-353">Haupt-Typ des MF- \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ee94-353">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="8ee94-354">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="8ee94-354">**MFMediaType\_Audio**</span></span>  |
| [<span data-ttu-id="8ee94-355">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="8ee94-355">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="8ee94-356">**MF Audioformat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="8ee94-356">**MFAudioFormat\_MPEG**</span></span> |
| [<span data-ttu-id="8ee94-357">MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="8ee94-357">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="8ee94-358">48000</span><span class="sxs-lookup"><span data-stu-id="8ee94-358">48000</span></span>                   |
| [<span data-ttu-id="8ee94-359">MF \_ \_ -MT- \_ audionum- \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="8ee94-359">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="8ee94-360">2</span><span class="sxs-lookup"><span data-stu-id="8ee94-360">2</span></span>                       |



 

<span data-ttu-id="8ee94-361">Eingabe Medientyp:</span><span class="sxs-lookup"><span data-stu-id="8ee94-361">Input media type:</span></span>

| <span data-ttu-id="8ee94-362">Attribut</span><span class="sxs-lookup"><span data-stu-id="8ee94-362">Attribute</span></span>                                                                                | <span data-ttu-id="8ee94-363">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee94-363">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="8ee94-364">Haupt-Typ des MF- \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ee94-364">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="8ee94-365">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="8ee94-365">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="8ee94-366">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="8ee94-366">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="8ee94-367">**MF Audioformat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="8ee94-367">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="8ee94-368">MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ee94-368">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="8ee94-369">16</span><span class="sxs-lookup"><span data-stu-id="8ee94-369">16</span></span>                     |
| [<span data-ttu-id="8ee94-370">MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="8ee94-370">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="8ee94-371">48000</span><span class="sxs-lookup"><span data-stu-id="8ee94-371">48000</span></span>                  |
| [<span data-ttu-id="8ee94-372">MF \_ \_ -MT- \_ audionum- \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="8ee94-372">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="8ee94-373">2</span><span class="sxs-lookup"><span data-stu-id="8ee94-373">2</span></span>                      |
| [<span data-ttu-id="8ee94-374">MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="8ee94-374">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="8ee94-375">4</span><span class="sxs-lookup"><span data-stu-id="8ee94-375">4</span></span>                      |
| [<span data-ttu-id="8ee94-376">MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="8ee94-376">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="8ee94-377">192000</span><span class="sxs-lookup"><span data-stu-id="8ee94-377">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="8ee94-378">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ee94-378">Requirements</span></span>



| <span data-ttu-id="8ee94-379">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ee94-379">Requirement</span></span> | <span data-ttu-id="8ee94-380">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee94-380">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee94-381">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ee94-381">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee94-382">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ee94-382">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8ee94-383">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ee94-383">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee94-384">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8ee94-384">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8ee94-385">DLL</span><span class="sxs-lookup"><span data-stu-id="8ee94-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ee94-386"><dt>Msmpeg2enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ee94-386"><dt>Msmpeg2enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee94-387">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ee94-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee94-388">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="8ee94-388">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
