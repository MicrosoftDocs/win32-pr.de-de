---
description: In diesem Thema wird beschrieben, wie das Format eines AAC-Streams (Advanced audiocoding) in Media Foundation angegeben wird.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: AAC-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961097"
---
# <a name="aac-media-types"></a><span data-ttu-id="163cc-103">AAC-Medientypen</span><span class="sxs-lookup"><span data-stu-id="163cc-103">AAC Media Types</span></span>

<span data-ttu-id="163cc-104">In diesem Thema wird beschrieben, wie das Format eines AAC-Streams (Advanced audiocoding) in Media Foundation angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="163cc-104">This topic describes how to specify the format of an Advanced Audio Coding (AAC) stream in Media Foundation.</span></span>

<span data-ttu-id="163cc-105">Zwei Untertypen werden für das AAC-Audioformat definiert:</span><span class="sxs-lookup"><span data-stu-id="163cc-105">Two subtypes are defined for AAC audio:</span></span>



| <span data-ttu-id="163cc-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="163cc-106">Subtype</span></span>                     | <span data-ttu-id="163cc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="163cc-107">Description</span></span>          | <span data-ttu-id="163cc-108">Header</span><span class="sxs-lookup"><span data-stu-id="163cc-108">Header</span></span>       |
|-----------------------------|----------------------|--------------|
| <span data-ttu-id="163cc-109">**MF Audioformat- \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="163cc-109">**MFAudioFormat\_AAC**</span></span>      | <span data-ttu-id="163cc-110">Unformatierte AAC-oder ADTs-AAC.</span><span class="sxs-lookup"><span data-stu-id="163cc-110">Raw AAC or ADTS AAC.</span></span> | <span data-ttu-id="163cc-111">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="163cc-111">mfapi.h</span></span>      |
| <span data-ttu-id="163cc-112">**Mediasubtype \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="163cc-112">**MEDIASUBTYPE\_RAW\_AAC1**</span></span> | <span data-ttu-id="163cc-113">RAW-AAC.</span><span class="sxs-lookup"><span data-stu-id="163cc-113">Raw AAC.</span></span>             | <span data-ttu-id="163cc-114">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="163cc-114">wmcodecdsp.h</span></span> |



 

<dl> <dt>

<span data-ttu-id="163cc-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MF Audioformat- \_ AAC</span><span class="sxs-lookup"><span data-stu-id="163cc-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat\_AAC</span></span>
</dt> <dd>

<span data-ttu-id="163cc-116">Für diesen Untertyp gibt der Medientyp die Samplingrate und die Anzahl der Kanäle vor der Anwendung von SBR (Spectral Band Replication) und den Parametern der parametrischen Stereo (PS) an, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="163cc-116">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="163cc-117">Der Effekt des SBR-Tools besteht darin, die decodierte Samplingrate in Relation zur Core AAC-LC-Stichprobenrate zu verdoppeln.</span><span class="sxs-lookup"><span data-stu-id="163cc-117">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="163cc-118">Der Effekt des PS-Tools besteht darin, Stereo von einem Mono-Channel-Kern-AAC-LC-Stream zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="163cc-118">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span>

<span data-ttu-id="163cc-119">Dieser Untertyp entspricht dem **mediasubtype \_ MPEG \_ heaac**, der in wmcodecdsp. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="163cc-119">This subtype is equivalent to **MEDIASUBTYPE\_MPEG\_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="163cc-120">Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="163cc-120">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="163cc-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>Mediasubtype \_ RAW \_ AAC1</span><span class="sxs-lookup"><span data-stu-id="163cc-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE\_RAW\_AAC1</span></span>
</dt> <dd>

<span data-ttu-id="163cc-122">Dieser Untertyp wird für AAC verwendet, der in einer AVI-Datei mit dem audioformattag gleich dem Wave- \_ Format \_ RAW \_ AAC1 (0x00FF) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="163cc-122">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE\_FORMAT\_RAW\_AAC1 (0x00FF).</span></span>

<span data-ttu-id="163cc-123">Für diesen Untertyp gibt der Medientyp die Stichprobenrate und die Anzahl der Kanäle nach Anwendung der SBR-und PS-Tools an (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="163cc-123">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span>

</dd> </dl>

<span data-ttu-id="163cc-124">Die folgenden Medientyp Attribute gelten für AAC-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="163cc-124">The following media type attributes apply to AAC audio.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="163cc-125">Attribut</span><span class="sxs-lookup"><span data-stu-id="163cc-125">Attribute</span></span></th>
<th><span data-ttu-id="163cc-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="163cc-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="163cc-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="163cc-128">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="163cc-128">Major type.</span></span> <span data-ttu-id="163cc-129">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="163cc-129">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="163cc-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="163cc-131">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="163cc-131">Audio subtype.</span></span> <span data-ttu-id="163cc-132">Weitere Informationen finden Sie in der vorherigen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="163cc-132">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="163cc-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="163cc-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="163cc-134">Audioprofil und-Ebene.</span><span class="sxs-lookup"><span data-stu-id="163cc-134">Audio profile and level.</span></span> <br/> <span data-ttu-id="163cc-135">Der Wert dieses Attributs ist das Feld <strong>audioprofilelevelindikation</strong> gemäß ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="163cc-135">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span><br/> <span data-ttu-id="163cc-136">Wenn unbekannt, legen Sie auf 0 (null) oder auf 0xFE ( &quot; kein Audioprofil angegeben &quot; ) fest.</span><span class="sxs-lookup"><span data-stu-id="163cc-136">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="163cc-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="163cc-138">Die Bitrate des codierten AAC-Streams in Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="163cc-138">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="163cc-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="163cc-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="163cc-140">Der Nutzlasttyp.</span><span class="sxs-lookup"><span data-stu-id="163cc-140">Payload type.</span></span><br/> <span data-ttu-id="163cc-141">Gilt nur für <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="163cc-141">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span><br/> <span data-ttu-id="163cc-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> ist optional.</span><span class="sxs-lookup"><span data-stu-id="163cc-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="163cc-143">Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream nur raw_data_block Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="163cc-143">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="163cc-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="163cc-145">Bittiefe der decodierten PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="163cc-145">Bit depth of the decoded PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="163cc-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="163cc-147">Zuweisung von Audiokanälen zu Redner Positionen.</span><span class="sxs-lookup"><span data-stu-id="163cc-147">Assignment of audio channels to speaker positions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="163cc-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="163cc-149">Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="163cc-149">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/> <span data-ttu-id="163cc-150">Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="163cc-150">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="163cc-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="163cc-152">Abtastrate in Samplings pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="163cc-152">Sample rate, in samples per second.</span></span><br/> <span data-ttu-id="163cc-153">Die Interpretation dieses Werts hängt vom Medien Untertyp ab, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="163cc-153">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="163cc-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="163cc-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="163cc-155">Der Wert dieses Attributs ist von dem Untertyp abhängig:</span><span class="sxs-lookup"><span data-stu-id="163cc-155">The value of this attribute depends on the subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="163cc-156"><strong>MFAudioFormat_AAC</strong>: enthält den Teil der <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>heaacwaveinfo</strong></a> -Struktur, der nach der <strong>WaveFormatEx</strong> -Struktur angezeigt wird (d. h. nach dem <strong>wfx</strong> -Member).</span><span class="sxs-lookup"><span data-stu-id="163cc-156"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="163cc-157">Danach folgen die audiospecificconfig ()-Daten gemäß ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="163cc-157">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="163cc-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: enthält die audiospecificconfig ()-Daten.</span><span class="sxs-lookup"><span data-stu-id="163cc-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="163cc-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="163cc-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="163cc-160">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="163cc-160">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="163cc-161">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="163cc-161">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="163cc-162">MPEG-4-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="163cc-162">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="163cc-163">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="163cc-163">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

