---
description: 'Der Microsoft Media Foundation AAC-Decoder ist eine Media Foundation Transformation, die die folgenden "Advanced audiocoding (AAC)"-und "High Efficiency AAC"-Profile decodiert:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: AAC-Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348989"
---
# <a name="aac-decoder"></a><span data-ttu-id="67af8-103">AAC-Decoder</span><span class="sxs-lookup"><span data-stu-id="67af8-103">AAC Decoder</span></span>

<span data-ttu-id="67af8-104">Der Microsoft Media Foundation AAC-Decoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die die folgenden "Advanced audiocoding (AAC)"-und "High Efficiency AAC"-Profile decodiert:</span><span class="sxs-lookup"><span data-stu-id="67af8-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="67af8-105">MPEG-2 AAC Low Komplexitäts Profil (LC) (Multichannel).</span><span class="sxs-lookup"><span data-stu-id="67af8-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="67af8-106">MPEG-4 HE-AAC v1 (Multichannel) mit AAC-LC Core.</span><span class="sxs-lookup"><span data-stu-id="67af8-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="67af8-107">MPEG-4 HE-AAC v2 (Stereo) mit AAC-LC Core.</span><span class="sxs-lookup"><span data-stu-id="67af8-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="67af8-108">Der AAC-Decoder unterstützt sowohl unformatierte AAC-Streams ohne Header und AAC in einem Audiodaten-Transportdaten Strom (ADTs).</span><span class="sxs-lookup"><span data-stu-id="67af8-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="67af8-109">Ab Windows 8 unterstützt der AAC-Decoder auch das Decodieren von MPEG-4-audiotransportstreams mit einer Multiplex Schicht (latm) und einer Synchronisierungs Schicht (LoAs).</span><span class="sxs-lookup"><span data-stu-id="67af8-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="67af8-110">Außerdem kann ein latm/LoAs-Stream in ADTs konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="67af8-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="media-types"></a><span data-ttu-id="67af8-111">Medientypen</span><span class="sxs-lookup"><span data-stu-id="67af8-111">Media Types</span></span>

<span data-ttu-id="67af8-112">Der AAC-Decoder unterstützt die folgenden Medientypen.</span><span class="sxs-lookup"><span data-stu-id="67af8-112">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="67af8-113">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="67af8-113">Input Types</span></span>

<span data-ttu-id="67af8-114">Der AAC-Decoder unterstützt die folgenden audiountertypen:</span><span class="sxs-lookup"><span data-stu-id="67af8-114">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="67af8-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="67af8-115">Subtype</span></span>                     | <span data-ttu-id="67af8-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67af8-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="67af8-117">Header</span><span class="sxs-lookup"><span data-stu-id="67af8-117">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="67af8-118">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="67af8-118">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="67af8-119">Unformatierte AAC-oder ADTs-AAC.</span><span class="sxs-lookup"><span data-stu-id="67af8-119">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="67af8-120">Für diesen Untertyp gibt der Medientyp die Samplingrate und die Anzahl der Kanäle vor der Anwendung von SBR (Spectral Band Replication) und den Parametern der parametrischen Stereo (PS) an, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="67af8-120">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="67af8-121">Der Effekt des SBR-Tools besteht darin, die decodierte Samplingrate in Relation zur Core AAC-LC-Stichprobenrate zu verdoppeln.</span><span class="sxs-lookup"><span data-stu-id="67af8-121">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="67af8-122">Der Effekt des PS-Tools besteht darin, Stereo von einem Mono-Channel-Kern-AAC-LC-Stream zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="67af8-122">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="67af8-123">Dieser Untertyp entspricht **MEDIASUBTYPE_MPEG_HEAAC**, die in wmcodecdsp. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="67af8-123">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="67af8-124">Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="67af8-124">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="67af8-125">Dieser Untertyp wird von der [MPEG-4-Datei Quelle](mpeg-4-file-source.md) und vom ADTs-Parser ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="67af8-125">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="67af8-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="67af8-126">mfapi.h</span></span>      |
| <span data-ttu-id="67af8-127">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="67af8-127">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="67af8-128">RAW-AAC.</span><span class="sxs-lookup"><span data-stu-id="67af8-128">Raw AAC.</span></span> <br/> <span data-ttu-id="67af8-129">Dieser Untertyp wird für AAC verwendet, der in einer AVI-Datei mit dem audioformattag gleich WAVE_FORMAT_RAW_AAC1 (0x00FF) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="67af8-129">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="67af8-130">Für diesen Untertyp gibt der Medientyp die Stichprobenrate und die Anzahl der Kanäle nach Anwendung der SBR-und PS-Tools an (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="67af8-130">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="67af8-131">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="67af8-131">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="67af8-132">Legen Sie zum Konfigurieren des AAC-Decoders die folgenden Attribute für den Eingabe Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="67af8-132">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67af8-133">Attribut</span><span class="sxs-lookup"><span data-stu-id="67af8-133">Attribute</span></span></th>
<th><span data-ttu-id="67af8-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67af8-134">Description</span></span></th>
<th><span data-ttu-id="67af8-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67af8-135">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67af8-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="67af8-137">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="67af8-137">Major type.</span></span></td>
<td><span data-ttu-id="67af8-138">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="67af8-138">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67af8-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="67af8-140">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="67af8-140">Audio subtype.</span></span></td>
<td><span data-ttu-id="67af8-141">Weitere Informationen finden Sie in der vorherigen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="67af8-141">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67af8-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="67af8-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="67af8-143">Audioprofil und-Ebene.</span><span class="sxs-lookup"><span data-stu-id="67af8-143">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="67af8-144">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="67af8-144">Optional.</span></span> <span data-ttu-id="67af8-145">Gilt nur für <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="67af8-145">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="67af8-146">Der Wert dieses Attributs ist das Feld <strong>audioprofilelevelindikation</strong> gemäß ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="67af8-146">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="67af8-147">Wenn unbekannt, legen Sie auf 0 (null) oder auf 0xFE ( &quot; kein Audioprofil angegeben &quot; ) fest.</span><span class="sxs-lookup"><span data-stu-id="67af8-147">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67af8-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="67af8-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="67af8-149">Der Nutzlasttyp.</span><span class="sxs-lookup"><span data-stu-id="67af8-149">Payload type.</span></span><br/></td>
<td><span data-ttu-id="67af8-150">Gilt nur für <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="67af8-150">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="67af8-151">Der Decoder unterstützt die folgenden Nutz Last Typen:</span><span class="sxs-lookup"><span data-stu-id="67af8-151">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="67af8-152">0: RAW-AAC.</span><span class="sxs-lookup"><span data-stu-id="67af8-152">0: Raw AAC.</span></span> <span data-ttu-id="67af8-153">Der Stream enthält nur raw_data_block ()-Elemente, wie in MPEG-2 definiert.</span><span class="sxs-lookup"><span data-stu-id="67af8-153">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="67af8-154">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="67af8-154">1: ADTS.</span></span> <span data-ttu-id="67af8-155">Der Stream enthält eine adts_sequence (), wie in MPEG-2 definiert.</span><span class="sxs-lookup"><span data-stu-id="67af8-155">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="67af8-156">Es ist nur ein raw_data_block () pro adts_frame () zulässig.</span><span class="sxs-lookup"><span data-stu-id="67af8-156">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="67af8-157">3: audiotransportstream mit einer Synchronisierungs Schicht (LoAs) und einer Multiplex Schicht (latm).</span><span class="sxs-lookup"><span data-stu-id="67af8-157">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="67af8-158">Von den drei Typen von LoAs wird nur <strong>audiosyncstream</strong> unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67af8-158">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="67af8-159">Die Multiplex Schicht ist <strong>audiomuxelement</strong>, das auf ein Audioprogramm und eine Ebene beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="67af8-159">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="67af8-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> ist optional.</span><span class="sxs-lookup"><span data-stu-id="67af8-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="67af8-161">Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream nur raw_data_block Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="67af8-161">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67af8-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="67af8-163">Gewünschte Bittiefe der decodierten PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="67af8-163">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="67af8-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="67af8-165">Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="67af8-165">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="67af8-166">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="67af8-166">Optional.</span></span> <span data-ttu-id="67af8-167">Weitere Informationen finden Sie unter <a href="#format-constraints">Format Einschränkungen</a>.</span><span class="sxs-lookup"><span data-stu-id="67af8-167">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67af8-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="67af8-169">Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="67af8-169">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="67af8-170">Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="67af8-170">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67af8-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="67af8-172">Abtastrate in Samplings pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="67af8-172">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="67af8-173">Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="67af8-173">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67af8-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="67af8-175">Zusätzliche Formatierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="67af8-175">Additional format information.</span></span></td>
<td><span data-ttu-id="67af8-176">Der Wert dieses Attributs hängt vom Untertyp ab.</span><span class="sxs-lookup"><span data-stu-id="67af8-176">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="67af8-177"><strong>MFAudioFormat_AAC</strong>: enthält den Teil der <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>heaacwaveinfo</strong></a> -Struktur, der nach der <strong>WaveFormatEx</strong> -Struktur angezeigt wird (d. h. nach dem <strong>wfx</strong> -Member).</span><span class="sxs-lookup"><span data-stu-id="67af8-177"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="67af8-178">Danach folgen die audiospecificconfig ()-Daten gemäß ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="67af8-178">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="67af8-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: enthält die audiospecificconfig ()-Daten.</span><span class="sxs-lookup"><span data-stu-id="67af8-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="67af8-180">Diese Daten müssen angezeigt werden. Andernfalls lehnt der Decoder den Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="67af8-180">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="67af8-181">Die Länge der audiospecificconfig ()-Daten beträgt 2 Bytes für AAC-LC oder den-AAC mit impliziter Signalisierung von SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="67af8-181">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="67af8-182">Es sind mehr als 2 Bytes für den-AAC mit expliziten Signalisierung von SBR/PS verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67af8-182">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="67af8-183">Der in audiospecificconfig () definierte Wert von <strong>audioobjecttype</strong> muss 2 sein, was AAC-LC angibt.</span><span class="sxs-lookup"><span data-stu-id="67af8-183">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="67af8-184">Der Wert von <strong>extensionaudioobjecttype</strong> muss für SBR oder 29 für PS den Wert 5 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="67af8-184">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="67af8-185">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="67af8-185">Output Types</span></span>

<span data-ttu-id="67af8-186">Der Decoder unterstützt die folgenden Ausgabetypen:</span><span class="sxs-lookup"><span data-stu-id="67af8-186">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67af8-187">Subtype</span><span class="sxs-lookup"><span data-stu-id="67af8-187">Subtype</span></span></th>
<th><span data-ttu-id="67af8-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67af8-188">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67af8-189"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="67af8-189"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="67af8-190">IEEE-Gleit Komma-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="67af8-190">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67af8-191"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="67af8-191"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="67af8-192">16-Bit-PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="67af8-192">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67af8-193"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="67af8-193"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="67af8-194">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="67af8-194">Requires Windows 8.</span></span> <br/> <span data-ttu-id="67af8-195">Dieser Ausgabetyp kann verwendet werden, um einen AAC-Datenstrom im LoAs/latm-Format in das ADTs-Format zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="67af8-195">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="67af8-196">Um einen LoAs/latm-Stream in einen ADTs-Stream zu konvertieren, legen Sie den Eingabetyp auf <strong>MFAudioFormat_AAC</strong> mit Payload Type 3 (LoAs) fest.</span><span class="sxs-lookup"><span data-stu-id="67af8-196">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="67af8-197">Legen Sie dann den Ausgabetyp auf <strong>MFAudioFormat_AAC</strong> mit Payload Type 1 (ADTs) fest.</span><span class="sxs-lookup"><span data-stu-id="67af8-197">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="67af8-198">Der Decoder formatiert die Konstante neu, ohne dass der Bitstream decodiert wird.</span><span class="sxs-lookup"><span data-stu-id="67af8-198">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="67af8-199">Der Decoder registriert <strong>MFAudioFormat_AAC</strong> nicht als Ausgabetyp.</span><span class="sxs-lookup"><span data-stu-id="67af8-199">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="67af8-200">Wenn die Anwendung den Eingabetyp jedoch wie beschrieben festlegt, gibt die <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>imftransform:: getoutputavailabletype</strong></a> -Methode <strong>MFAudioFormat_AAC</strong> in der Liste der verfügbaren Ausgabetypen zurück.</span><span class="sxs-lookup"><span data-stu-id="67af8-200">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="67af8-201">Wenn der Eingabedaten Strom mehr als zwei Kanäle enthält, stellt der AAC-Decoder zwei Optionen für das Ausgabeformat bereit:</span><span class="sxs-lookup"><span data-stu-id="67af8-201">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="67af8-202">Dieselbe Kanal Konfiguration wie der Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="67af8-202">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="67af8-203">Stereo-Fold.</span><span class="sxs-lookup"><span data-stu-id="67af8-203">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="67af8-204">Format Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="67af8-204">Format Constraints</span></span>

<span data-ttu-id="67af8-205">Die decodierte audiosamplingrate muss nach dem Anwenden von SBR (sofern vorhanden) einen der folgenden Punkte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="67af8-205">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="67af8-206">8 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-206">8 kHz</span></span>
-   <span data-ttu-id="67af8-207">11,025 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-207">11.025 kHz</span></span>
-   <span data-ttu-id="67af8-208">12 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-208">12 kHz</span></span>
-   <span data-ttu-id="67af8-209">16 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-209">16 kHz</span></span>
-   <span data-ttu-id="67af8-210">22,05 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-210">22.05 kHz</span></span>
-   <span data-ttu-id="67af8-211">24 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-211">24 kHz</span></span>
-   <span data-ttu-id="67af8-212">32 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-212">32 kHz</span></span>
-   <span data-ttu-id="67af8-213">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-213">44.1 kHz</span></span>
-   <span data-ttu-id="67af8-214">48 kHz</span><span class="sxs-lookup"><span data-stu-id="67af8-214">48 kHz</span></span>

<span data-ttu-id="67af8-215">Stichproben Raten oberhalb von 48 kHz werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67af8-215">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="67af8-216">Der Decoder unterstützt bis zu 6 Audiokanäle.</span><span class="sxs-lookup"><span data-stu-id="67af8-216">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="67af8-217">Für jede Sprecher Konfiguration erwartet der Decoder, dass die AAC-syntaktischen Elemente in einer bestimmten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="67af8-217">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="67af8-218">In der folgenden Tabelle sind die unterstützten Lautsprecherkonfigurationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="67af8-218">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="67af8-219">In der dritten Spalte der Tabelle sind die erwarteten syntaktischen Elemente und deren Reihenfolge mit der folgenden Notation aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="67af8-219">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="67af8-220"><SCE1>: Das single_channel_element (SCE), das mit dem Front-Center-Redner verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="67af8-220"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="67af8-221"><SCE2>: Der SCE, der dem Back-Center-Redner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67af8-221"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="67af8-222"><CPE1>: Die der Vorderseite zugeordneten channel_pair_element (CPE).</span><span class="sxs-lookup"><span data-stu-id="67af8-222"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="67af8-223"><CPE2>: Das CPE, das den zurück-oder Seiten-Referenten zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="67af8-223"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="67af8-224"><LFE>: Der lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="67af8-224"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="67af8-225">Weitere Informationen zu diesen syntaktischen Elementen finden Sie unter ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="67af8-225">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="67af8-226">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="67af8-226">Configuration</span></span>       | <span data-ttu-id="67af8-227">Kanalmaske</span><span class="sxs-lookup"><span data-stu-id="67af8-227">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="67af8-228">AAC-syntaktische Elemente</span><span class="sxs-lookup"><span data-stu-id="67af8-228">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="67af8-229">Mono</span><span class="sxs-lookup"><span data-stu-id="67af8-229">Mono</span></span>                | <span data-ttu-id="67af8-230">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="67af8-230">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="67af8-231">Stereo oder Dual Mono</span><span class="sxs-lookup"><span data-stu-id="67af8-231">Stereo or dual mono</span></span> | <span data-ttu-id="67af8-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="67af8-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="67af8-233">2/1</span><span class="sxs-lookup"><span data-stu-id="67af8-233">2/1</span></span>                 | <span data-ttu-id="67af8-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="67af8-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="67af8-235">2/2</span><span class="sxs-lookup"><span data-stu-id="67af8-235">2/2</span></span>                 | <span data-ttu-id="67af8-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="67af8-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="67af8-237">3/0</span><span class="sxs-lookup"><span data-stu-id="67af8-237">3/0</span></span>                 | <span data-ttu-id="67af8-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="67af8-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="67af8-239">3/1</span><span class="sxs-lookup"><span data-stu-id="67af8-239">3/1</span></span>                 | <span data-ttu-id="67af8-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="67af8-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="67af8-241">3/2</span><span class="sxs-lookup"><span data-stu-id="67af8-241">3/2</span></span>                 | <span data-ttu-id="67af8-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="67af8-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="67af8-243">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="67af8-243">3/2 + LFE</span></span>           | <span data-ttu-id="67af8-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="67af8-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="67af8-245">Für RAW AAC muss jedes Eingabe Beispiel genau einen vollständigen AAC-komprimierten Frame enthalten.</span><span class="sxs-lookup"><span data-stu-id="67af8-245">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="67af8-246">Bei ADTs kann jede Eingabe Stichprobe mehrere Audioframes und partielle Frames enthalten, bei denen es sich um Beispiel Grenzen mit Frames handelt.</span><span class="sxs-lookup"><span data-stu-id="67af8-246">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="67af8-247">Jedem ADTs-Header muss ein AAC-Frame folgen.</span><span class="sxs-lookup"><span data-stu-id="67af8-247">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="67af8-248">Der AAC-Decoder unterstützt keines der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="67af8-248">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="67af8-249">Hauptprofil, Sample-Rate skalierbares (SRS) Profil oder das LTP-Profil (Long Term Vorhersage).</span><span class="sxs-lookup"><span data-stu-id="67af8-249">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="67af8-250">Das Format für den audiodatenaustausch (ADIF).</span><span class="sxs-lookup"><span data-stu-id="67af8-250">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="67af8-251">Latm/Laos-Transportdaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="67af8-251">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="67af8-252">Kopplung von Kanal Elementen (CCES).</span><span class="sxs-lookup"><span data-stu-id="67af8-252">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="67af8-253">Der Decoder überspringt Audioframes mit CCES.</span><span class="sxs-lookup"><span data-stu-id="67af8-253">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="67af8-254">AAC-LC mit der Frame Größe 960-Sample.</span><span class="sxs-lookup"><span data-stu-id="67af8-254">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="67af8-255">Nur 1024-Sample Frames werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67af8-255">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="67af8-256">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="67af8-256">Transform Attributes</span></span>

<span data-ttu-id="67af8-257">Der AAC-Decoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="67af8-257">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="67af8-258">Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="67af8-258">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67af8-259">Attribut</span><span class="sxs-lookup"><span data-stu-id="67af8-259">Attribute</span></span></th>
<th><span data-ttu-id="67af8-260">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67af8-260">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67af8-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="67af8-262">Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.</span><span class="sxs-lookup"><span data-stu-id="67af8-262">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="67af8-263">Als schreibgeschützt behandeln.</span><span class="sxs-lookup"><span data-stu-id="67af8-263">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67af8-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="67af8-265">Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="67af8-265">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="67af8-266">Der Standardwert ist <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output CH1 auf der linken und rechten sprechenden Seite.</span><span class="sxs-lookup"><span data-stu-id="67af8-266">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="67af8-267">Anwendungen können diese Eigenschaft festlegen, um das Standardverhalten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="67af8-267">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67af8-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="67af8-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="67af8-269">Der AAC-Decoder verarbeitet keine dynamischen Formatänderungen und muss geleert oder entladen werden, bevor ein neuer Eingabe Medientyp festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="67af8-269">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="67af8-270">Behandeln Sie dieses Attribut als schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="67af8-270">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="67af8-271">Der AAC-Decoder meldet fälschlicherweise den Wert <strong>true</strong> für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="67af8-271">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="67af8-272">In Windows 7 meldet der Decoder fälschlicherweise den Wert <strong>true</strong> für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="67af8-272">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="67af8-273">In Windows 8 meldet der Decoder <strong>false</strong>, was der korrekte Wert ist.</span><span class="sxs-lookup"><span data-stu-id="67af8-273">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="67af8-274">Beispiel Medientypen</span><span class="sxs-lookup"><span data-stu-id="67af8-274">Example Media Types</span></span>

<span data-ttu-id="67af8-275">Im folgenden finden Sie ein Beispiel für den Eingabe Medientyp, der für einen 6-Kanal-AAC-LC-Stream mit 48-kHz benötigt wird</span><span class="sxs-lookup"><span data-stu-id="67af8-275">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="67af8-276">Attribut</span><span class="sxs-lookup"><span data-stu-id="67af8-276">Attribute</span></span>                                                                                      | <span data-ttu-id="67af8-277">Wert</span><span class="sxs-lookup"><span data-stu-id="67af8-277">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="67af8-278">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="67af8-278">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="67af8-279">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="67af8-279">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="67af8-280">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="67af8-280">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="67af8-281">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="67af8-281">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="67af8-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="67af8-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="67af8-283">48000</span><span class="sxs-lookup"><span data-stu-id="67af8-283">48000</span></span>                                                                                |
| [<span data-ttu-id="67af8-284">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="67af8-284">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="67af8-285">6</span><span class="sxs-lookup"><span data-stu-id="67af8-285">6</span></span>                                                                                    |
| [<span data-ttu-id="67af8-286">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="67af8-286">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="67af8-287">0</span><span class="sxs-lookup"><span data-stu-id="67af8-287">0</span></span>                                                                                    |
| [<span data-ttu-id="67af8-288">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="67af8-288">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="67af8-289">{0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="67af8-289">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="67af8-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="67af8-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="67af8-291">0x2A (optional)</span><span class="sxs-lookup"><span data-stu-id="67af8-291">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="67af8-292">Die ersten 12 Bytes [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) entsprechen den folgenden [**heaacwavin FO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) -Strukturmembern:</span><span class="sxs-lookup"><span data-stu-id="67af8-292">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="67af8-293">**wpayloadtype** = 0 (unformatierte AAC-Datei)</span><span class="sxs-lookup"><span data-stu-id="67af8-293">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="67af8-294">**waudioprofilelevelindikation** = 0x2A (AAC-Profil, Ebene 4)</span><span class="sxs-lookup"><span data-stu-id="67af8-294">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="67af8-295">**wstructtype** = 0</span><span class="sxs-lookup"><span data-stu-id="67af8-295">**wStructType** = 0</span></span>

<span data-ttu-id="67af8-296">Die letzten zwei Bytes [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) enthalten den Wert von audiospecificconfig (), wie in MPEG-4 definiert.</span><span class="sxs-lookup"><span data-stu-id="67af8-296">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="67af8-297">Audiospecificconfig. audioobjecttype = 2 (AAC LC) (5 Bits)</span><span class="sxs-lookup"><span data-stu-id="67af8-297">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="67af8-298">Audiospecificconfig. samplingfrequencyindex = 3 (4 Bits)</span><span class="sxs-lookup"><span data-stu-id="67af8-298">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="67af8-299">Audiospecificconfig. channelconfiguration = 6 (4 Bits)</span><span class="sxs-lookup"><span data-stu-id="67af8-299">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="67af8-300">"Gaspeer" config. framelengthflag = 0 (1 Bit)</span><span class="sxs-lookup"><span data-stu-id="67af8-300">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="67af8-301">"Gaspeer" config. dependsoncorecoder = 0 (1 Bit)</span><span class="sxs-lookup"><span data-stu-id="67af8-301">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="67af8-302">Gaspeer-Konfigurationsdatei. extensionflag = 0 (1 Bit)</span><span class="sxs-lookup"><span data-stu-id="67af8-302">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="67af8-303">Verwenden Sie für diesen Eingabetyp den folgenden Ausgabe Medientyp, um eine 6-Kanal-, 32-Bit-Gleit Komma-PCM-Audiodatei vom Decoder zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="67af8-303">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="67af8-304">Attribut</span><span class="sxs-lookup"><span data-stu-id="67af8-304">Attribute</span></span>                                                                                    | <span data-ttu-id="67af8-305">Wert</span><span class="sxs-lookup"><span data-stu-id="67af8-305">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="67af8-306">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="67af8-306">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="67af8-307">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="67af8-307">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="67af8-308">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="67af8-308">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="67af8-309">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="67af8-309">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="67af8-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="67af8-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="67af8-311">32</span><span class="sxs-lookup"><span data-stu-id="67af8-311">32</span></span>                       |
| [<span data-ttu-id="67af8-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="67af8-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="67af8-313">48000</span><span class="sxs-lookup"><span data-stu-id="67af8-313">48000</span></span>                    |
| [<span data-ttu-id="67af8-314">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="67af8-314">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="67af8-315">6</span><span class="sxs-lookup"><span data-stu-id="67af8-315">6</span></span>                        |
| [<span data-ttu-id="67af8-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="67af8-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="67af8-317">1152000 (optional)</span><span class="sxs-lookup"><span data-stu-id="67af8-317">1152000 (optional)</span></span>       |
| [<span data-ttu-id="67af8-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="67af8-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="67af8-319">24 (optional)</span><span class="sxs-lookup"><span data-stu-id="67af8-319">24 (optional)</span></span>            |
| [<span data-ttu-id="67af8-320">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="67af8-320">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="67af8-321">0x3f (optional)</span><span class="sxs-lookup"><span data-stu-id="67af8-321">0x3f (optional)</span></span>          |



 

<span data-ttu-id="67af8-322">Wenn die Ergänzung zum Platt Form Update für Windows Vista installiert ist, ist der AAC-Audiodecoder unter Windows Vista verfügbar, aber nur unter Windows Vista mit dem [Quell Leser](source-reader.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="67af8-322">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67af8-323">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67af8-323">Requirements</span></span>



| <span data-ttu-id="67af8-324">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67af8-324">Requirement</span></span> | <span data-ttu-id="67af8-325">Wert</span><span class="sxs-lookup"><span data-stu-id="67af8-325">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67af8-326">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67af8-326">Minimum supported client</span></span><br/> | <span data-ttu-id="67af8-327">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67af8-327">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="67af8-328">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67af8-328">Minimum supported server</span></span><br/> | <span data-ttu-id="67af8-329">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67af8-329">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="67af8-330">DLL</span><span class="sxs-lookup"><span data-stu-id="67af8-330">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67af8-331"><dt>Msmpeg2adec.dll unter Windows 7; </dt> <dt>MSAudDecMFT.dll unter Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="67af8-331"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67af8-332">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67af8-332">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67af8-333">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="67af8-333">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="67af8-334">AAC-Medientypen</span><span class="sxs-lookup"><span data-stu-id="67af8-334">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="67af8-335">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="67af8-335">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="67af8-336">**Microsoft MPEG-1/DD/AAC-Audiodecoder**</span><span class="sxs-lookup"><span data-stu-id="67af8-336">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="67af8-337">MPEG-4-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67af8-337">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="67af8-338">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67af8-338">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
