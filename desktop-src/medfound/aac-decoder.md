---
description: 'Der Microsoft Media Foundation AAC-Decoder ist eine Media Foundation-Transformation, die die folgenden AAC-Profile (Advanced Audio Coding) und High Efficiency AAC (HE-AAC) decodiert:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: AAC-Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7554d6bc4a13fe1e4af4c51e75f1fe8a0bd38286
ms.sourcegitcommit: 3a0a8a8fdce560a81a27789a1c04172ed96147b1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "112436588"
---
# <a name="aac-decoder"></a><span data-ttu-id="e9536-103">AAC-Decoder</span><span class="sxs-lookup"><span data-stu-id="e9536-103">AAC Decoder</span></span>

<span data-ttu-id="e9536-104">Der Microsoft Media Foundation AAC-Decoder ist eine [Media Foundation-Transformation,](media-foundation-transforms.md) die die folgenden AAC-Profile (Advanced Audio Coding) und High Efficiency AAC -Profile (HE-AAC) decodiert:</span><span class="sxs-lookup"><span data-stu-id="e9536-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="e9536-105">MPEG-2 AAC Low Complexity (LC)-Profil (Multichannel).</span><span class="sxs-lookup"><span data-stu-id="e9536-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="e9536-106">MPEG-4 HE-AAC v1 (Multichannel) mit AAC-LC-Kern.</span><span class="sxs-lookup"><span data-stu-id="e9536-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="e9536-107">MPEG-4 HE-AAC v2 (Stereo) mit AAC-LC-Kern.</span><span class="sxs-lookup"><span data-stu-id="e9536-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="e9536-108">Der AAC-Decoder unterstützt sowohl unformatiert AAC-Streams ohne Header als auch AAC in einem Audiodatentransportstream (ADTS).</span><span class="sxs-lookup"><span data-stu-id="e9536-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="e9536-109">Ab Windows 8 unterstützt der AAC-Decoder auch das Decodieren von MPEG-4-Audiotransportstreams mit einer Multiplexebene (LATM) und Synchronisierungsschicht (LOAS).</span><span class="sxs-lookup"><span data-stu-id="e9536-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="e9536-110">Sie kann auch einen LATM/LOAS-Stream in ADTS konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e9536-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e9536-111">Klassenbezeichner</span><span class="sxs-lookup"><span data-stu-id="e9536-111">Class Identifier</span></span>

<span data-ttu-id="e9536-112">Der Klassenbezeichner (CLSID) des AAC-Encoders ist **CLSID \_ CMSAACDecMFT,** definiert in der Headerdatei wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="e9536-112">The class identifier (CLSID) of the AAC encoder is **CLSID\_CMSAACDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="e9536-113">Medientypen</span><span class="sxs-lookup"><span data-stu-id="e9536-113">Media Types</span></span>

<span data-ttu-id="e9536-114">Der AAC-Decoder unterstützt die folgenden Medientypen.</span><span class="sxs-lookup"><span data-stu-id="e9536-114">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="e9536-115">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="e9536-115">Input Types</span></span>

<span data-ttu-id="e9536-116">Der AAC-Decoder unterstützt die folgenden Audiountertypen:</span><span class="sxs-lookup"><span data-stu-id="e9536-116">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="e9536-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="e9536-117">Subtype</span></span>                     | <span data-ttu-id="e9536-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9536-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="e9536-119">Header</span><span class="sxs-lookup"><span data-stu-id="e9536-119">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="e9536-120">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="e9536-120">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="e9536-121">Unformatiert AAC oder ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="e9536-121">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="e9536-122">Für diesen Untertyp gibt der Medientyp die Abtastrate und die Anzahl der Kanäle vor der Anwendung von SBR-Tools (Mergereplikation) und parametrischen Stereotools (PS) an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9536-122">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="e9536-123">Das SBR-Tool hat den Effekt, dass die decodierte Abtastrate relativ zur AAC-LC-Kernabtastrate verdoppelt wird.</span><span class="sxs-lookup"><span data-stu-id="e9536-123">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="e9536-124">Der Effekt des PS-Tools besteht in der Decodierung von Stereo aus einem AAC-LC-Stream mit Monokanalkern.</span><span class="sxs-lookup"><span data-stu-id="e9536-124">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="e9536-125">Dieser Untertyp entspricht **MEDIASUBTYPE_MPEG_HEAAC**, definiert in wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="e9536-125">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="e9536-126">Weitere Informationen [finden Sie unter Audio Subtype GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e9536-126">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="e9536-127">Die [MPEG-4-Dateiquelle](mpeg-4-file-source.md) und der ADTS-Parser geben diesen Untertyp aus.</span><span class="sxs-lookup"><span data-stu-id="e9536-127">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="e9536-128">mfapi.h</span><span class="sxs-lookup"><span data-stu-id="e9536-128">mfapi.h</span></span>      |
| <span data-ttu-id="e9536-129">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="e9536-129">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="e9536-130">AAC-Rohdaten.</span><span class="sxs-lookup"><span data-stu-id="e9536-130">Raw AAC.</span></span> <br/> <span data-ttu-id="e9536-131">Dieser Untertyp wird für AAC in einer AVI-Datei verwendet, deren Audioformattag gleich WAVE_FORMAT_RAW_AAC1 (0x00FF.</span><span class="sxs-lookup"><span data-stu-id="e9536-131">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="e9536-132">Für diesen Untertyp gibt der Medientyp die Abtastrate und die Anzahl von Kanälen an, nachdem die SBR- und PS-Tools angewendet wurden(sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="e9536-132">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="e9536-133">wmcodecdsp.h</span><span class="sxs-lookup"><span data-stu-id="e9536-133">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="e9536-134">Legen Sie zum Konfigurieren des AAC-Decoders die folgenden Attribute für den Eingabemedientyp fest.</span><span class="sxs-lookup"><span data-stu-id="e9536-134">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9536-135">attribute</span><span class="sxs-lookup"><span data-stu-id="e9536-135">Attribute</span></span></th>
<th><span data-ttu-id="e9536-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9536-136">Description</span></span></th>
<th><span data-ttu-id="e9536-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9536-137">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9536-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="e9536-139">Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="e9536-139">Major type.</span></span></td>
<td><span data-ttu-id="e9536-140">Muss <strong>MFMediaType_Audio.</strong></span><span class="sxs-lookup"><span data-stu-id="e9536-140">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9536-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="e9536-142">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="e9536-142">Audio subtype.</span></span></td>
<td><span data-ttu-id="e9536-143">Weitere Informationen finden Sie in der vorherigen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="e9536-143">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9536-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="e9536-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="e9536-145">Audioprofil und -ebene.</span><span class="sxs-lookup"><span data-stu-id="e9536-145">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="e9536-146">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e9536-146">Optional.</span></span> <span data-ttu-id="e9536-147">Gilt nur für <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9536-147">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="e9536-148">Der Wert dieses Attributs ist das <strong>Feld audioProfileLevelIndication,</strong> wie in ISO/IEC 14496-3 definiert.</span><span class="sxs-lookup"><span data-stu-id="e9536-148">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="e9536-149">Wenn unbekannt, legen Sie auf 0 oder 0xFE fest &quot; (kein Audioprofil &quot; angegeben).</span><span class="sxs-lookup"><span data-stu-id="e9536-149">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9536-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="e9536-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="e9536-151">Der Nutzlasttyp.</span><span class="sxs-lookup"><span data-stu-id="e9536-151">Payload type.</span></span><br/></td>
<td><span data-ttu-id="e9536-152">Gilt nur für <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9536-152">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="e9536-153">Der Decoder unterstützt die folgenden Nutzlasttypen:</span><span class="sxs-lookup"><span data-stu-id="e9536-153">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="e9536-154">0: AAC-Rohdaten.</span><span class="sxs-lookup"><span data-stu-id="e9536-154">0: Raw AAC.</span></span> <span data-ttu-id="e9536-155">Der Stream enthält raw_data_block()-Elemente, wie durch MPEG-2 definiert.</span><span class="sxs-lookup"><span data-stu-id="e9536-155">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="e9536-156">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="e9536-156">1: ADTS.</span></span> <span data-ttu-id="e9536-157">Der Stream enthält eine adts_sequence(), wie durch MPEG-2 definiert.</span><span class="sxs-lookup"><span data-stu-id="e9536-157">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="e9536-158">Pro adts_frame() ist nur raw_data_block() zulässig.</span><span class="sxs-lookup"><span data-stu-id="e9536-158">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="e9536-159">3: Audiotransportstream mit einer Synchronisierungsschicht (SYNCHRONIZATION Layer, LOAS) und einer Multiplexebene (LATM).</span><span class="sxs-lookup"><span data-stu-id="e9536-159">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="e9536-160">Von den drei LOAS-Typen wird <strong>nur AudioSyncStream</strong> unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9536-160">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="e9536-161">Die Multiplexebene ist <strong>"AudioMuxElement",</strong>die auf ein Audioprogramm und eine Ebene beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="e9536-161">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="e9536-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> ist optional.</span><span class="sxs-lookup"><span data-stu-id="e9536-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="e9536-163">Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream nur raw_data_block enthält.</span><span class="sxs-lookup"><span data-stu-id="e9536-163">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9536-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="e9536-165">Gewünschte Bittiefe des decodierten PCM-Audios.</span><span class="sxs-lookup"><span data-stu-id="e9536-165">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e9536-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="e9536-167">Gibt die Zuweisung von Audiokanälen zu Sprecherpositionen an.</span><span class="sxs-lookup"><span data-stu-id="e9536-167">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="e9536-168">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e9536-168">Optional.</span></span> <span data-ttu-id="e9536-169">Weitere Informationen finden Sie unter <a href="#format-constraints">Formateinschränkungen.</a></span><span class="sxs-lookup"><span data-stu-id="e9536-169">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9536-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="e9536-171">Anzahl der Kanäle, einschließlich des Kanals mit niedriger Frequenz (Low Frequency, LFE), sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e9536-171">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="e9536-172">Die Interpretation dieses Werts hängt vom Medienuntertyp ab, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e9536-172">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9536-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="e9536-174">Stichprobenrate in Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="e9536-174">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="e9536-175">Die Interpretation dieses Werts hängt vom Medienuntertyp ab, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e9536-175">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9536-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="e9536-177">Zusätzliche Formatinformationen.</span><span class="sxs-lookup"><span data-stu-id="e9536-177">Additional format information.</span></span></td>
<td><span data-ttu-id="e9536-178">Der Wert dieses Attributs hängt vom Untertyp ab.</span><span class="sxs-lookup"><span data-stu-id="e9536-178">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="e9536-179"><strong>MFAudioFormat_AAC</strong>: Enthält den Teil der <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO-Struktur,</strong></a> der nach der <strong>WAVEFORMATEX-Struktur</strong> (d. h. nach dem <strong>wfx-Element) angezeigt</strong> wird.</span><span class="sxs-lookup"><span data-stu-id="e9536-179"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="e9536-180">Darauf folgen die AudioSpecificConfig()-Daten gemäß ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="e9536-180">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="e9536-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Enthält die AudioSpecificConfig()-Daten.</span><span class="sxs-lookup"><span data-stu-id="e9536-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="e9536-182">Diese Daten müssen angezeigt werden. Andernfalls lehnt der Decoder den Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="e9536-182">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="e9536-183">Die Länge der AudioSpecificConfig()-Daten beträgt 2 Byte für AAC-LC oder HE-AAC mit impliziter Signalisierung von SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="e9536-183">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="e9536-184">Es sind mehr als 2 Bytes für HE-AAC mit expliziter Signalisierung von SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="e9536-184">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="e9536-185">Der Wert von <strong>audioObjectType,</strong> wie in AudioSpecificConfig() definiert, muss 2 sein, was AAC-LC angibt.</span><span class="sxs-lookup"><span data-stu-id="e9536-185">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="e9536-186">Der Wert von <strong>extensionAudioObjectType</strong> muss 5 für SBR oder 29 für PS sein.</span><span class="sxs-lookup"><span data-stu-id="e9536-186">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="e9536-187">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="e9536-187">Output Types</span></span>

<span data-ttu-id="e9536-188">Der Decoder unterstützt die folgenden Ausgabetypen:</span><span class="sxs-lookup"><span data-stu-id="e9536-188">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9536-189">Subtype</span><span class="sxs-lookup"><span data-stu-id="e9536-189">Subtype</span></span></th>
<th><span data-ttu-id="e9536-190">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9536-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9536-191"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="e9536-191"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="e9536-192">IEEE-Gleitkommaaudio.</span><span class="sxs-lookup"><span data-stu-id="e9536-192">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9536-193"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="e9536-193"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="e9536-194">16-Bit-PCM-Audio.</span><span class="sxs-lookup"><span data-stu-id="e9536-194">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9536-195"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="e9536-195"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="e9536-196">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e9536-196">Requires Windows 8.</span></span> <br/> <span data-ttu-id="e9536-197">Dieser Ausgabetyp kann verwendet werden, um einen AAC-Stream im LOAS/LATM-Format in das ADTS-Format zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e9536-197">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="e9536-198">Um einen LOAS/LATM-Stream in einen ADTS-Stream <strong></strong> zu konvertieren, legen Sie den Eingabetyp auf MFAudioFormat_AAC Nutzlasttyp 3 (LOAS) fest.</span><span class="sxs-lookup"><span data-stu-id="e9536-198">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="e9536-199">Legen Sie dann den Ausgabetyp auf <strong>MFAudioFormat_AAC</strong> Nutzlasttyp 1 (ADTS) fest.</span><span class="sxs-lookup"><span data-stu-id="e9536-199">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="e9536-200">Der Decoder wird den Conainter neu umdekontieren, ohne den Bitstream zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="e9536-200">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e9536-201">Der Decoder registriert <strong>MFAudioFormat_AAC</strong> nicht als Ausgabetyp.</span><span class="sxs-lookup"><span data-stu-id="e9536-201">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="e9536-202">Wenn die Anwendung den Eingabetyp jedoch wie beschrieben festlegt, gibt die <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>METHODE DERTRANSFORM::GetOutputAvailableType</strong></a> <strong>MFAudioFormat_AAC</strong> in der Liste der verfügbaren Ausgabetypen zurück.</span><span class="sxs-lookup"><span data-stu-id="e9536-202">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e9536-203">Wenn der Eingabestream mehr als zwei Kanäle enthält, bietet der AAC-Decoder zwei Optionen für das Ausgabeformat:</span><span class="sxs-lookup"><span data-stu-id="e9536-203">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="e9536-204">Die gleiche Kanalkonfiguration wie der Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="e9536-204">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="e9536-205">Stereo-Fold-Down.</span><span class="sxs-lookup"><span data-stu-id="e9536-205">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="e9536-206">Formateinschränkungen</span><span class="sxs-lookup"><span data-stu-id="e9536-206">Format Constraints</span></span>

<span data-ttu-id="e9536-207">Die Samplingrate für decodierte Audiodaten muss eine der folgenden Sein, nachdem SBR angewendet wurde (sofern vorhanden):</span><span class="sxs-lookup"><span data-stu-id="e9536-207">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="e9536-208">8 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-208">8 kHz</span></span>
-   <span data-ttu-id="e9536-209">11,025 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-209">11.025 kHz</span></span>
-   <span data-ttu-id="e9536-210">12 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-210">12 kHz</span></span>
-   <span data-ttu-id="e9536-211">16 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-211">16 kHz</span></span>
-   <span data-ttu-id="e9536-212">22,05 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-212">22.05 kHz</span></span>
-   <span data-ttu-id="e9536-213">24 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-213">24 kHz</span></span>
-   <span data-ttu-id="e9536-214">32 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-214">32 kHz</span></span>
-   <span data-ttu-id="e9536-215">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-215">44.1 kHz</span></span>
-   <span data-ttu-id="e9536-216">48 kHz</span><span class="sxs-lookup"><span data-stu-id="e9536-216">48 kHz</span></span>

<span data-ttu-id="e9536-217">Samplingraten über 48 kHz werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9536-217">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="e9536-218">Der Decoder unterstützt bis zu 6 Audiokanäle.</span><span class="sxs-lookup"><span data-stu-id="e9536-218">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="e9536-219">Für jede Sprecherkonfiguration erwartet der Decoder, dass die syntaktischen AAC-Elemente in einer bestimmten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e9536-219">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="e9536-220">In der folgenden Tabelle sind die unterstützten Sprecherkonfigurationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9536-220">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="e9536-221">In der dritten Spalte der Tabelle werden die erwarteten syntaktischen Elemente und ihre Reihenfolge mithilfe der folgenden Notation aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="e9536-221">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="e9536-222"><SCE1>: Die dem Front-Center-Lautsprecher zugeordnete single_channel_element (SCE).</span><span class="sxs-lookup"><span data-stu-id="e9536-222"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="e9536-223"><SCE2>: Die dem Back-Center-Lautsprecher zugeordnete SCE.</span><span class="sxs-lookup"><span data-stu-id="e9536-223"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="e9536-224"><CPE1>: Die channel_pair_element (CPE), die den Vorderlautsprechern zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9536-224"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="e9536-225"><CPE2>: Die CPE, die den hinteren (oder seitlichen) Lautsprechern zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9536-225"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="e9536-226"><LFE>: Die lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="e9536-226"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="e9536-227">Weitere Informationen zu diesen syntaktischen Elementen finden Sie unter ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="e9536-227">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="e9536-228">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e9536-228">Configuration</span></span>       | <span data-ttu-id="e9536-229">Kanalmaske</span><span class="sxs-lookup"><span data-stu-id="e9536-229">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="e9536-230">Syntaktische AAC-Elemente</span><span class="sxs-lookup"><span data-stu-id="e9536-230">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="e9536-231">Mono</span><span class="sxs-lookup"><span data-stu-id="e9536-231">Mono</span></span>                | <span data-ttu-id="e9536-232">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e9536-232">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="e9536-233">Stereo oder Dual Mono</span><span class="sxs-lookup"><span data-stu-id="e9536-233">Stereo or dual mono</span></span> | <span data-ttu-id="e9536-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e9536-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="e9536-235">2/1</span><span class="sxs-lookup"><span data-stu-id="e9536-235">2/1</span></span>                 | <span data-ttu-id="e9536-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e9536-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="e9536-237">2/2</span><span class="sxs-lookup"><span data-stu-id="e9536-237">2/2</span></span>                 | <span data-ttu-id="e9536-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e9536-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="e9536-239">3/0</span><span class="sxs-lookup"><span data-stu-id="e9536-239">3/0</span></span>                 | <span data-ttu-id="e9536-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e9536-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="e9536-241">3/1</span><span class="sxs-lookup"><span data-stu-id="e9536-241">3/1</span></span>                 | <span data-ttu-id="e9536-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e9536-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="e9536-243">3/2</span><span class="sxs-lookup"><span data-stu-id="e9536-243">3/2</span></span>                 | <span data-ttu-id="e9536-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e9536-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="e9536-245">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="e9536-245">3/2 + LFE</span></span>           | <span data-ttu-id="e9536-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e9536-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="e9536-247">Für unformatierte AAC muss jedes Eingabebeispiel genau einen vollständigen komprimierten AAC-Frame enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9536-247">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="e9536-248">Für ADTS kann jedes Eingabebeispiel mehrere Audioframes sowie Teilframes enthalten, d. h., Frames können Sich über Beispielgrenzen erstrecken.</span><span class="sxs-lookup"><span data-stu-id="e9536-248">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="e9536-249">Auf jeden ADTS-Header muss ein AAC-Frame folgen.</span><span class="sxs-lookup"><span data-stu-id="e9536-249">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="e9536-250">Der AAC-Decoder unterstützt keine der folgenden Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="e9536-250">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="e9536-251">Hauptprofil, Sample-Rate SRS-Profil (Scalable) oder LTP-Profil (Long Term Prediction).</span><span class="sxs-lookup"><span data-stu-id="e9536-251">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="e9536-252">Audiodatenaustauschformat (ADIF).</span><span class="sxs-lookup"><span data-stu-id="e9536-252">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="e9536-253">LATM/CSV-Transportstreams.</span><span class="sxs-lookup"><span data-stu-id="e9536-253">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="e9536-254">Kopplungskanalelemente (CCEs).</span><span class="sxs-lookup"><span data-stu-id="e9536-254">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="e9536-255">Der Decoder überspringt Audioframes mit CCEs.</span><span class="sxs-lookup"><span data-stu-id="e9536-255">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="e9536-256">AAC-LC mit einer Framegröße von 960 Stichproben.</span><span class="sxs-lookup"><span data-stu-id="e9536-256">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="e9536-257">Nur 1024-Sample-Frames werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9536-257">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="e9536-258">Transformieren von Attributen</span><span class="sxs-lookup"><span data-stu-id="e9536-258">Transform Attributes</span></span>

<span data-ttu-id="e9536-259">Der AAC-Decoder implementiert die [**DECODERTransform::GetAttributes-Methode.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)</span><span class="sxs-lookup"><span data-stu-id="e9536-259">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="e9536-260">Anwendungen können diese Methode verwenden, um die folgenden Attribute abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e9536-260">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9536-261">attribute</span><span class="sxs-lookup"><span data-stu-id="e9536-261">Attribute</span></span></th>
<th><span data-ttu-id="e9536-262">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9536-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9536-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="e9536-264">Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.</span><span class="sxs-lookup"><span data-stu-id="e9536-264">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="e9536-265">Als schreibgeschützt behandeln.</span><span class="sxs-lookup"><span data-stu-id="e9536-265">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9536-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="e9536-267">Gibt an, wie der Decoder duale Mono-Audiodaten reproduziert.</span><span class="sxs-lookup"><span data-stu-id="e9536-267">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="e9536-268">Der Standardwert ist <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO:</strong>Ausgabe ch1 links und rechts.</span><span class="sxs-lookup"><span data-stu-id="e9536-268">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="e9536-269">Anwendungen können diese Eigenschaft festlegen, um das Standardverhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e9536-269">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9536-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e9536-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="e9536-271">Der AAC-Decoder verarbeitet keine dynamischen Formatänderungen und muss geleert oder entladen werden, bevor ein neuer Eingabemedientyp festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e9536-271">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="e9536-272">Behandeln Sie dieses Attribut als schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e9536-272">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e9536-273">Der AAC-Decoder meldet fälschlicherweise den Wert <strong>TRUE</strong> für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="e9536-273">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="e9536-274">In Windows 7 meldet der Decoder fälschlicherweise den Wert <strong>TRUE</strong> für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="e9536-274">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="e9536-275">In Windows 8 meldet der Decoder <strong>FALSE</strong>. Dies ist der richtige Wert.</span><span class="sxs-lookup"><span data-stu-id="e9536-275">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="e9536-276">Beispielmedientypen</span><span class="sxs-lookup"><span data-stu-id="e9536-276">Example Media Types</span></span>

<span data-ttu-id="e9536-277">Hier sehen Sie ein Beispiel für den Eingabemedientyp, der für einen 6-Kanal-AAC-LC-Stream mit 48 kHz und einer unformatierten AAC-Nutzlast benötigt wird:</span><span class="sxs-lookup"><span data-stu-id="e9536-277">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="e9536-278">attribute</span><span class="sxs-lookup"><span data-stu-id="e9536-278">Attribute</span></span>                                                                                      | <span data-ttu-id="e9536-279">Wert</span><span class="sxs-lookup"><span data-stu-id="e9536-279">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9536-280">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="e9536-280">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="e9536-281">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="e9536-281">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="e9536-282">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="e9536-282">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="e9536-283">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="e9536-283">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="e9536-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="e9536-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="e9536-285">48000</span><span class="sxs-lookup"><span data-stu-id="e9536-285">48000</span></span>                                                                                |
| [<span data-ttu-id="e9536-286">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="e9536-286">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="e9536-287">6</span><span class="sxs-lookup"><span data-stu-id="e9536-287">6</span></span>                                                                                    |
| [<span data-ttu-id="e9536-288">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="e9536-288">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="e9536-289">0</span><span class="sxs-lookup"><span data-stu-id="e9536-289">0</span></span>                                                                                    |
| [<span data-ttu-id="e9536-290">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="e9536-290">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="e9536-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="e9536-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="e9536-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="e9536-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="e9536-293">0x2a (optional)</span><span class="sxs-lookup"><span data-stu-id="e9536-293">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="e9536-294">Die ersten 12 Bytes von [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) entsprechen den folgenden [**HEAACWAVEINFO-Strukturmembern:**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)</span><span class="sxs-lookup"><span data-stu-id="e9536-294">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="e9536-295">**wPayloadType** = 0 (unformatierte AAC)</span><span class="sxs-lookup"><span data-stu-id="e9536-295">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="e9536-296">**wAudioProfileLevelIndication** = 0x2a (AAC-Profil, Ebene 4)</span><span class="sxs-lookup"><span data-stu-id="e9536-296">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="e9536-297">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="e9536-297">**wStructType** = 0</span></span>

<span data-ttu-id="e9536-298">Die letzten beiden Bytes von [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) den Wert von AudioSpecificConfig() enthalten, wie von MPEG-4 definiert.</span><span class="sxs-lookup"><span data-stu-id="e9536-298">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="e9536-299">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 Bits)</span><span class="sxs-lookup"><span data-stu-id="e9536-299">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="e9536-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 Bits)</span><span class="sxs-lookup"><span data-stu-id="e9536-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="e9536-301">AudioSpecificConfig.channelConfiguration = 6 (4 Bits)</span><span class="sxs-lookup"><span data-stu-id="e9536-301">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="e9536-302">GASpecificConfig.frameLengthFlag = 0 (1 Bit)</span><span class="sxs-lookup"><span data-stu-id="e9536-302">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="e9536-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 Bit)</span><span class="sxs-lookup"><span data-stu-id="e9536-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="e9536-304">GASpecificConfig.extensionFlag = 0 (1 Bit)</span><span class="sxs-lookup"><span data-stu-id="e9536-304">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="e9536-305">Verwenden Sie bei diesem Eingabetyp den folgenden Ausgabemedientyp, um 6-Kanal-PCM-Audio mit 32-Bit-Gleitkommadaten aus dem Decoder zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e9536-305">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="e9536-306">attribute</span><span class="sxs-lookup"><span data-stu-id="e9536-306">Attribute</span></span>                                                                                    | <span data-ttu-id="e9536-307">Wert</span><span class="sxs-lookup"><span data-stu-id="e9536-307">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="e9536-308">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="e9536-308">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="e9536-309">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="e9536-309">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="e9536-310">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="e9536-310">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="e9536-311">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="e9536-311">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="e9536-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="e9536-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="e9536-313">32</span><span class="sxs-lookup"><span data-stu-id="e9536-313">32</span></span>                       |
| [<span data-ttu-id="e9536-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="e9536-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="e9536-315">48000</span><span class="sxs-lookup"><span data-stu-id="e9536-315">48000</span></span>                    |
| [<span data-ttu-id="e9536-316">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="e9536-316">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="e9536-317">6</span><span class="sxs-lookup"><span data-stu-id="e9536-317">6</span></span>                        |
| [<span data-ttu-id="e9536-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="e9536-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="e9536-319">1152000 (optional)</span><span class="sxs-lookup"><span data-stu-id="e9536-319">1152000 (optional)</span></span>       |
| [<span data-ttu-id="e9536-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="e9536-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="e9536-321">24 (optional)</span><span class="sxs-lookup"><span data-stu-id="e9536-321">24 (optional)</span></span>            |
| [<span data-ttu-id="e9536-322">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="e9536-322">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="e9536-323">0x3f (optional)</span><span class="sxs-lookup"><span data-stu-id="e9536-323">0x3f (optional)</span></span>          |



 

<span data-ttu-id="e9536-324">Wenn die Plattformupdateergänzung für Windows Vista installiert ist, ist der AAC-Audiodecoder unter Windows Vista verfügbar, aber unter Windows Vista nur über den [Quellleser zugänglich.](source-reader.md)</span><span class="sxs-lookup"><span data-stu-id="e9536-324">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9536-325">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e9536-325">Requirements</span></span>



| <span data-ttu-id="e9536-326">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9536-326">Requirement</span></span> | <span data-ttu-id="e9536-327">Wert</span><span class="sxs-lookup"><span data-stu-id="e9536-327">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9536-328">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9536-328">Minimum supported client</span></span><br/> | <span data-ttu-id="e9536-329">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9536-329">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="e9536-330">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9536-330">Minimum supported server</span></span><br/> | <span data-ttu-id="e9536-331">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9536-331">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="e9536-332">DLL</span><span class="sxs-lookup"><span data-stu-id="e9536-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9536-333"><dt>Msmpeg2adec.dll unter Windows 7; </dt> <dt>MSAudDecMFT.dll auf Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="e9536-333"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9536-334">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9536-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9536-335">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="e9536-335">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="e9536-336">AAC-Medientypen</span><span class="sxs-lookup"><span data-stu-id="e9536-336">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="e9536-337">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="e9536-337">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="e9536-338">**Microsoft MPEG-1/DD/AAC-Audiodecoder**</span><span class="sxs-lookup"><span data-stu-id="e9536-338">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="e9536-339">MPEG-4-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9536-339">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e9536-340">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9536-340">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
