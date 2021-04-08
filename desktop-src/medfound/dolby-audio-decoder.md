---
description: Der Dolby-Audiodecoder ist ein MFT, das Dolby Digital (AC-3) und Dolby Digital Plus decodiert.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Dolby-Audiodecoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749264"
---
# <a name="dolby-audio-decoder"></a><span data-ttu-id="e3571-103">Dolby-Audiodecoder</span><span class="sxs-lookup"><span data-stu-id="e3571-103">Dolby Audio Decoder</span></span>

<span data-ttu-id="e3571-104">Der Dolby-Audiodecoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT), mit der die folgenden Streamtypen decodiert werden:</span><span class="sxs-lookup"><span data-stu-id="e3571-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that decodes the following stream types:</span></span>

-   <span data-ttu-id="e3571-105">Dolby Digital, auch Dolby AC-3 genannt</span><span class="sxs-lookup"><span data-stu-id="e3571-105">Dolby Digital, also called Dolby AC-3</span></span>
-   <span data-ttu-id="e3571-106">Dolby Digital Plus, auch Enhanced AC-3 (E-AC-3) genannt</span><span class="sxs-lookup"><span data-stu-id="e3571-106">Dolby Digital Plus, also called Enhanced AC-3 (E-AC-3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3571-107">Bei Windows-Versionen vor Windows 8 ist die Microsoft-Implementierung der Dolby Digital-Technologie gemäß den Bedingungen des Dolby Digital Licensing Program, das von Microsoft-Anwendungen verwendet werden soll, eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="e3571-107">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="e3571-108">Weitere Informationen zu diesen Formaten finden Sie im Advanced TV Systems Committee (ATSC) Document *Digital audiocompression Standard (AC-3, E-AC-3) Revision B*.</span><span class="sxs-lookup"><span data-stu-id="e3571-108">For more information about these formats, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

<span data-ttu-id="e3571-109">Der Decoder kann auch einen Dolby Digital Plus-Datenstrom in ein Dolby Digital-Format für die AC-3 S/pidf-Ausgabe konvertieren oder einen Dolby Digital Plus-Datenstrom für die digitale HDMI-Ausgabe formatieren.</span><span class="sxs-lookup"><span data-stu-id="e3571-109">The decoder can also convert a Dolby Digital Plus stream to Dolby Digital format for AC-3 S/PIDF output, or format a Dolby Digital Plus stream for HDMI digital output.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e3571-110">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e3571-110">Class Identifier</span></span>

<span data-ttu-id="e3571-111">Die Klassen-ID (CLSID) des Dolby-Audiodecoders ist **CLSID \_ cmsddplusdecmft**, die in der Header Datei "wmcodecdsp. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e3571-111">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDDPlusDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="e3571-112">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="e3571-112">Input Types</span></span>

<span data-ttu-id="e3571-113">Der Dolby Audiodecoder unterstützt die folgenden Eingabe Untertypen.</span><span class="sxs-lookup"><span data-stu-id="e3571-113">The Dolby audio decoder supports the following input subtypes.</span></span>



| <span data-ttu-id="e3571-114">Subtype</span><span class="sxs-lookup"><span data-stu-id="e3571-114">Subtype</span></span>                                 | <span data-ttu-id="e3571-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3571-115">Description</span></span>                                                                                                                                                 | <span data-ttu-id="e3571-116">Header</span><span class="sxs-lookup"><span data-stu-id="e3571-116">Header</span></span>       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="e3571-117">**Mediasubtype \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="e3571-117">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>            | <span data-ttu-id="e3571-118">Dolby Digital-Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="e3571-118">Dolby Digital audio.</span></span>                                                                                                                                        | <span data-ttu-id="e3571-119">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="e3571-119">mfapi.h</span></span>      |
| <span data-ttu-id="e3571-120">**mediasubtype \_ DVM**</span><span class="sxs-lookup"><span data-stu-id="e3571-120">**MEDIASUBTYPE\_DVM**</span></span>                   | <span data-ttu-id="e3571-121">Dolby Digital-Audiodatei; siehe [**audiountertypen**](../directshow/audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="e3571-121">Dolby Digital audio; see [**Audio Subtypes**](../directshow/audio-subtypes.md).</span></span> <span data-ttu-id="e3571-122">Dieser Untertyp kann austauschbar mit **mediasubtype \_ Dolby \_ AC3** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3571-122">This subtype can be used interchangeably with **MEDIASUBTYPE\_DOLBY\_AC3**.</span></span><br/> | <span data-ttu-id="e3571-123">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="e3571-123">wmcodecdsp.h</span></span> |
| <span data-ttu-id="e3571-124">**MF Audioformat \_ Dolby \_ Digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="e3571-124">**MFAudioFormat\_Dolby\_Digital\_Plus**</span></span> | <span data-ttu-id="e3571-125">Dolby Digital Plus-Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="e3571-125">Dolby Digital Plus audio.</span></span>                                                                                                                                   | <span data-ttu-id="e3571-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="e3571-126">mfapi.h</span></span>      |



 

<span data-ttu-id="e3571-127">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Eingabe Medientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3571-127">The following table lists the requires and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3571-128">Attribut</span><span class="sxs-lookup"><span data-stu-id="e3571-128">Attribute</span></span></th>
<th><span data-ttu-id="e3571-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3571-129">Description</span></span></th>
<th><span data-ttu-id="e3571-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3571-130">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3571-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="e3571-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="e3571-132">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="e3571-132">Major type.</span></span></td>
<td><span data-ttu-id="e3571-133">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-133">Required.</span></span> <span data-ttu-id="e3571-134">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="e3571-134">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="e3571-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="e3571-136">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="e3571-136">Audio subtype.</span></span></td>
<td><span data-ttu-id="e3571-137">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-137">Required.</span></span> <span data-ttu-id="e3571-138">Weitere Informationen finden Sie in der vorherigen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3571-138">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="e3571-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="e3571-140">Abtastrate in Samplings pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="e3571-140">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="e3571-141">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e3571-141">Optional.</span></span> <span data-ttu-id="e3571-142">Gültige Werte sind: 48000, 44100, 32000, 24000, 22050 und 16000.</span><span class="sxs-lookup"><span data-stu-id="e3571-142">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="e3571-143">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 48000.</span><span class="sxs-lookup"><span data-stu-id="e3571-143">If this attribute is not set, the default value is 48000.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e3571-144">Dolby AC-3-Streams sind auf die drei höchsten Sätze in dieser Liste beschränkt.</span><span class="sxs-lookup"><span data-stu-id="e3571-144">Dolby AC-3 streams are limited to the three highest rates in this list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="e3571-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="e3571-146">Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3571-146">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="e3571-147">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e3571-147">Optional.</span></span> <span data-ttu-id="e3571-148">Gültige Werte liegen im Bereich von 1 (Mono) bis 8 (7,1 Channel-Konfiguration).</span><span class="sxs-lookup"><span data-stu-id="e3571-148">Valid values are in the range 1 (mono) to 8 (7.1 channel configuration).</span></span> <span data-ttu-id="e3571-149">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 2 (Stereo).</span><span class="sxs-lookup"><span data-stu-id="e3571-149">If this attribute is not set, the default value is 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="e3571-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="e3571-151">Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="e3571-151">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="e3571-152">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e3571-152">Optional.</span></span> <span data-ttu-id="e3571-153">Wenn angegeben, muss der Wert mit der Anzahl der Audiokanäle konsistent sein.</span><span class="sxs-lookup"><span data-stu-id="e3571-153">If specified, the value must be consistent with the number of audio channels.</span></span> <span data-ttu-id="e3571-154">Wenn das-Attribut nicht festgelegt ist, verwendet der Decoder eine Standard Kanalmaske, basierend auf der Anzahl der Kanäle.</span><span class="sxs-lookup"><span data-stu-id="e3571-154">If the attribute is not set, the decoder uses a default channel mask, based on the number of channels.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e3571-155">In der folgenden Tabelle sind die unterstützten Dolby Channel-Konfigurationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3571-155">The following table lists the supported Dolby channel configurations.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3571-156">Kanal Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e3571-156">Channel configuration</span></span></th>
<th><span data-ttu-id="e3571-157">Anzahl von Kanälen</span><span class="sxs-lookup"><span data-stu-id="e3571-157">Number of channels</span></span></th>
<th><span data-ttu-id="e3571-158">Kanalmasken</span><span class="sxs-lookup"><span data-stu-id="e3571-158">Channel masks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3571-159">1/0 (Mono)</span><span class="sxs-lookup"><span data-stu-id="e3571-159">1/0 (mono)</span></span></td>
<td><span data-ttu-id="e3571-160">1</span><span class="sxs-lookup"><span data-stu-id="e3571-160">1</span></span></td>
<td><span data-ttu-id="e3571-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-162">2/0 (Stereo) oder 1 + 1 (Dual Mono)</span><span class="sxs-lookup"><span data-stu-id="e3571-162">2/0 (stereo) or 1+1 (dual mono)</span></span></td>
<td><span data-ttu-id="e3571-163">2</span><span class="sxs-lookup"><span data-stu-id="e3571-163">2</span></span></td>
<td><span data-ttu-id="e3571-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-165">3/0</span><span class="sxs-lookup"><span data-stu-id="e3571-165">3/0</span></span></td>
<td><span data-ttu-id="e3571-166">3</span><span class="sxs-lookup"><span data-stu-id="e3571-166">3</span></span></td>
<td><span data-ttu-id="e3571-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span><span class="sxs-lookup"><span data-stu-id="e3571-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-168">2/1</span><span class="sxs-lookup"><span data-stu-id="e3571-168">2/1</span></span></td>
<td><span data-ttu-id="e3571-169">3</span><span class="sxs-lookup"><span data-stu-id="e3571-169">3</span></span></td>
<td><span data-ttu-id="e3571-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-171">3/1</span><span class="sxs-lookup"><span data-stu-id="e3571-171">3/1</span></span></td>
<td><span data-ttu-id="e3571-172">4</span><span class="sxs-lookup"><span data-stu-id="e3571-172">4</span></span></td>
<td><span data-ttu-id="e3571-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-174">2/2</span><span class="sxs-lookup"><span data-stu-id="e3571-174">2/2</span></span></td>
<td><span data-ttu-id="e3571-175">4</span><span class="sxs-lookup"><span data-stu-id="e3571-175">4</span></span></td>
<td><span data-ttu-id="e3571-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="e3571-177">oder</span><span class="sxs-lookup"><span data-stu-id="e3571-177">or</span></span><br/> <span data-ttu-id="e3571-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-179">3/2</span><span class="sxs-lookup"><span data-stu-id="e3571-179">3/2</span></span></td>
<td><span data-ttu-id="e3571-180">5</span><span class="sxs-lookup"><span data-stu-id="e3571-180">5</span></span></td>
<td><span data-ttu-id="e3571-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="e3571-182">oder</span><span class="sxs-lookup"><span data-stu-id="e3571-182">or</span></span><br/> <span data-ttu-id="e3571-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-184">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="e3571-184">3/2 + LFE</span></span></td>
<td><span data-ttu-id="e3571-185">6</span><span class="sxs-lookup"><span data-stu-id="e3571-185">6</span></span></td>
<td><span data-ttu-id="e3571-186">0x3f (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="e3571-187">oder</span><span class="sxs-lookup"><span data-stu-id="e3571-187">or</span></span><br/> <span data-ttu-id="e3571-188">0x60f (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="e3571-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-189">3/2/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="e3571-189">3/2/2 + LFE</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e3571-190">Nur Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="e3571-190">Dolby Digital Plus only.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="e3571-191">8</span><span class="sxs-lookup"><span data-stu-id="e3571-191">8</span></span></td>
<td><span data-ttu-id="e3571-192">0x63f (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span><span class="sxs-lookup"><span data-stu-id="e3571-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e3571-193">Außerdem können die Kanal Konfigurationen 1/0, 2/0, 3/0, 2/1, 3/1 und 2/2 ebenfalls mit einem LFE-Kanal angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e3571-193">In addition, channel configurations 1/0, 2/0, 3/0, 2/1, 3/1, and 2/2 may also appear with an LFE channel.</span></span>

## <a name="output-types"></a><span data-ttu-id="e3571-194">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="e3571-194">Output Types</span></span>

<span data-ttu-id="e3571-195">Der Dolby-Audiodecoder unterstützt die folgenden Ausgabe Untertypen.</span><span class="sxs-lookup"><span data-stu-id="e3571-195">The Dolby audio decoder supports the following output subtypes.</span></span>



| <span data-ttu-id="e3571-196">Subtype</span><span class="sxs-lookup"><span data-stu-id="e3571-196">Subtype</span></span>                                                   | <span data-ttu-id="e3571-197">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3571-197">Description</span></span>                                                                                                                               | <span data-ttu-id="e3571-198">Header</span><span class="sxs-lookup"><span data-stu-id="e3571-198">Header</span></span>    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e3571-199">**MF Audioformat \_ Dolby \_ AC3 \_ SPDIF**</span><span class="sxs-lookup"><span data-stu-id="e3571-199">**MFAudioFormat\_Dolby\_AC3\_SPDIF**</span></span>                      | <span data-ttu-id="e3571-200">Dolby AC-3-audioformatierung für die digitale S/PDIF-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3571-200">Dolby AC-3 audio formatted for S/PDIF digital output.</span></span>                                                                                     | <span data-ttu-id="e3571-201">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="e3571-201">mfapi.h</span></span>   |
| <span data-ttu-id="e3571-202">**Ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="e3571-202">**KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**</span></span> | <span data-ttu-id="e3571-203">Dolby Digital Plus-Audiodatei für die digitale Codec-Ausgabe formatiert.</span><span class="sxs-lookup"><span data-stu-id="e3571-203">Dolby Digital Plus audio formatted for HDMI digital output.</span></span>                                                                               | <span data-ttu-id="e3571-204">ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="e3571-204">ksmedia.h</span></span> |
| <span data-ttu-id="e3571-205">**MF Audioformat ( \_ float)**</span><span class="sxs-lookup"><span data-stu-id="e3571-205">**MFAudioFormat\_Float**</span></span>                                  | <span data-ttu-id="e3571-206">IEEE 32-Bit-PCM für Gleit Komma-PCM</span><span class="sxs-lookup"><span data-stu-id="e3571-206">IEEE 32-bit floating-point PCM audio</span></span><br/> <span data-ttu-id="e3571-207">**Windows 10**: Stereo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="e3571-207">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="e3571-208">**Vorherige Versionen**: Stereo, 5,1</span><span class="sxs-lookup"><span data-stu-id="e3571-208">**Previous versions**: stereo, 5.1</span></span><br/> | <span data-ttu-id="e3571-209">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="e3571-209">mfapi.h</span></span>   |
| <span data-ttu-id="e3571-210">**MF Audioformat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="e3571-210">**MFAudioFormat\_PCM**</span></span>                                    | <span data-ttu-id="e3571-211">16-Bit-PCM-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="e3571-211">16-bit PCM audio</span></span><br/> <span data-ttu-id="e3571-212">**Windows 10**: Stereo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="e3571-212">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="e3571-213">**Vorherige Versionen**: Stereo, 5,1</span><span class="sxs-lookup"><span data-stu-id="e3571-213">**Previous versions**: stereo, 5.1</span></span><br/>                     | <span data-ttu-id="e3571-214">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="e3571-214">mfapi.h</span></span>   |



 

<span data-ttu-id="e3571-215">In der folgenden Tabelle sind die erforderlichen und optionalen Attribute für den Ausgabe Medientyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3571-215">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3571-216">Attribut</span><span class="sxs-lookup"><span data-stu-id="e3571-216">Attribute</span></span></th>
<th><span data-ttu-id="e3571-217">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3571-217">Description</span></span></th>
<th><span data-ttu-id="e3571-218">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3571-218">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3571-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="e3571-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="e3571-220">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="e3571-220">Major type.</span></span></td>
<td><span data-ttu-id="e3571-221">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-221">Required.</span></span> <span data-ttu-id="e3571-222">Muss <strong>MFMediaType_Audio</strong>werden.</span><span class="sxs-lookup"><span data-stu-id="e3571-222">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="e3571-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="e3571-224">Audiountertyp.</span><span class="sxs-lookup"><span data-stu-id="e3571-224">Audio subtype.</span></span></td>
<td><span data-ttu-id="e3571-225">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-225">Required.</span></span> <span data-ttu-id="e3571-226">Weitere Informationen finden Sie in der vorherigen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3571-226">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="e3571-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="e3571-228">Abtastrate in Samplings pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="e3571-228">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="e3571-229">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-229">Required.</span></span> <span data-ttu-id="e3571-230">Gültige Werte sind: 48000, 44100, 32000, 24000, 22050 und 16000.</span><span class="sxs-lookup"><span data-stu-id="e3571-230">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="e3571-231">Die Ausgabe Stichproben Rate muss mit der Eingabe Stichproben Rate identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e3571-231">The output sample rate must be identical to the input sample rate.</span></span> <span data-ttu-id="e3571-232">Der Decoder kann die Samplingrate des Streams nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e3571-232">The decoder cannot change the sampling rate of the stream.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="e3571-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="e3571-234">Anzahl der Kanäle, einschließlich des LFE-Kanals (Low Frequency), falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3571-234">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="e3571-235">Erforderlich für die PCM-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3571-235">Required for PCM output.</span></span> <br/> <span data-ttu-id="e3571-236">Bei digitaler Ausgabe nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-236">Not needed for digital output.</span></span> <br/> <span data-ttu-id="e3571-237">Wenn der Eingabetyp Mono, Stereo oder Dual-Mono (alle ohne LFE-Kanal) ist, ist der einzige gültige Wert 2 für die Stereoausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3571-237">If the input type is mono, stereo, or dual-mono (all without LFE channel), the only valid value is 2, for stereo output.</span></span> <span data-ttu-id="e3571-238">Andernfalls kann der Wert wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="e3571-238">Otherwise, the value can be:</span></span> <br/>
<ul>
<li><span data-ttu-id="e3571-239">2 für Stereo Downmix</span><span class="sxs-lookup"><span data-stu-id="e3571-239">2 for stereo downmix</span></span></li>
<li><span data-ttu-id="e3571-240">6 für 5,1-Kanal Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="e3571-240">6 for 5.1 channel configurations</span></span></li>
<li><span data-ttu-id="e3571-241">8 für 7,1-Kanal Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="e3571-241">8 for 7.1 channel configurations</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="e3571-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="e3571-243">Gibt die Zuweisung von Audiokanälen zu Redner Positionen an.</span><span class="sxs-lookup"><span data-stu-id="e3571-243">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="e3571-244">Erforderlich für die PCM-Ausgabe, wenn die Anzahl der Kanäle größer als 2 ist.</span><span class="sxs-lookup"><span data-stu-id="e3571-244">Required for PCM output if the number of channels is greater than 2.</span></span> <span data-ttu-id="e3571-245">Der Wert muss wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="e3571-245">The value must be:</span></span><br/>
<ul>
<li><span data-ttu-id="e3571-246">0x3 für Stereoausgabe</span><span class="sxs-lookup"><span data-stu-id="e3571-246">0x3 for stereo output</span></span></li>
<li><span data-ttu-id="e3571-247">0x3f für 5,1-Kanal Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e3571-247">0x3F for 5.1 channel output</span></span></li>
<li><span data-ttu-id="e3571-248">0x63f für 7,1-Kanal Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e3571-248">0x63F for 7.1 channel output</span></span></li>
</ul>
<span data-ttu-id="e3571-249">Bei digitaler Ausgabe nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-249">Not needed for digital output.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="e3571-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="e3571-251">Anzahl von Bits pro audiostich Probe.</span><span class="sxs-lookup"><span data-stu-id="e3571-251">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="e3571-252">Erforderlich für die PCM-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3571-252">Required for PCM output.</span></span> <span data-ttu-id="e3571-253">Der Wert muss 32 für <strong>MFAudioFormat_Float</strong>und 16 für <strong>MFAudioFormat_PCM</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="e3571-253">The value must be 32 for <strong>MFAudioFormat_Float</strong>, and 16 for <strong>MFAudioFormat_PCM</strong>.</span></span><br/> <span data-ttu-id="e3571-254">Bei digitaler Ausgabe nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-254">Not needed for digital output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="e3571-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="e3571-256">Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="e3571-256">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="e3571-257">Optional für die PCM-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3571-257">Optional for PCM output.</span></span> <span data-ttu-id="e3571-258">Wenn dieser Wert festgelegt ist, muss der Wert mit <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e3571-258">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span><br/> <span data-ttu-id="e3571-259">Für die digitalen Ausgabe Untertypen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-259">Not needed for the digital output subtypes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3571-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="e3571-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="e3571-261">Block Ausrichtung (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="e3571-261">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="e3571-262">Optional für die PCM-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3571-262">Optional for PCM output.</span></span> <span data-ttu-id="e3571-263">Bei digitaler Ausgabe nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-263">Not needed for digital output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3571-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="e3571-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="e3571-265">Die durchschnittliche Anzahl von Bytes pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="e3571-265">Average number of bytes per second.</span></span></td>
<td><span data-ttu-id="e3571-266">Optional für die PCM-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3571-266">Optional for PCM output.</span></span> <span data-ttu-id="e3571-267">Bei digitaler Ausgabe nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3571-267">Not needed for digital output.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a><span data-ttu-id="e3571-268">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="e3571-268">Transform Attributes</span></span>

<span data-ttu-id="e3571-269">Der Dolby-Audiodecoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e3571-269">The Dolby audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="e3571-270">Die Anwendung kann diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e3571-270">The application can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="e3571-271">Attribut</span><span class="sxs-lookup"><span data-stu-id="e3571-271">Attribute</span></span>                                                                                | <span data-ttu-id="e3571-272">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3571-272">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3571-273">Codecapi \_ avdecaudiodualmono</span><span class="sxs-lookup"><span data-stu-id="e3571-273">CODECAPI\_AVDecAudioDualMono</span></span>](../directshow/avdecaudiodualmono-property.md)                        | <span data-ttu-id="e3571-274">Gibt an, ob ein Dolby-Audiostream mit zwei Kanälen als Stereo-oder Dual-Mono-codiert wird.</span><span class="sxs-lookup"><span data-stu-id="e3571-274">Specifies whether a 2-channel Dolby audio stream is encoded as stereo or dual-mono.</span></span> <span data-ttu-id="e3571-275">Bevor der erste Dolby-Frame decodiert wird, ist **eavdecaudiodualmono \_ nicht angegeben**.</span><span class="sxs-lookup"><span data-stu-id="e3571-275">Before the first Dolby frame is decoded, the value is **eAVDecAudioDualMono\_UnSpecified**.</span></span> <span data-ttu-id="e3571-276">Nachdem das Decodieren begonnen hat, spiegelt der Wert den letzten Dolby-Frame wider.</span><span class="sxs-lookup"><span data-stu-id="e3571-276">After decoding begins, the value reflects the most recent Dolby frame.</span></span><br/> <span data-ttu-id="e3571-277">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e3571-277">Read-only.</span></span> <br/> |
| [<span data-ttu-id="e3571-278">Codecapi \_ avdecaudiodualmonorepromode</span><span class="sxs-lookup"><span data-stu-id="e3571-278">CODECAPI\_AVDecAudioDualMonoReproMode</span></span>](../directshow/avdecaudiodualmonorepromode-property.md)      | <span data-ttu-id="e3571-279">Gibt an, wie der Decoder Dual-Mono-Audiodaten wiederherstellt.</span><span class="sxs-lookup"><span data-stu-id="e3571-279">Specifies how the decoder reproduces dual-mono audio.</span></span> <span data-ttu-id="e3571-280">Der Standardwert ist **eavdecaudiodualmonorepromode \_ left \_ Mono**.</span><span class="sxs-lookup"><span data-stu-id="e3571-280">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span> <span data-ttu-id="e3571-281">Diese Eigenschaft kann von der Anwendung jederzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3571-281">The application can set this property at any time.</span></span><br/> <span data-ttu-id="e3571-282">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e3571-282">Read/write.</span></span><br/>                                                                            |
| [<span data-ttu-id="e3571-283">Codecapi \_ avdeccommonmeanbitrate</span><span class="sxs-lookup"><span data-stu-id="e3571-283">CODECAPI\_AVDecCommonMeanBitRate</span></span>](../directshow/avdeccommonmeanbitrate.md)                         | <span data-ttu-id="e3571-284">Gibt für Dolby Digital (AC-3)-Streams die Bitrate des Eingabedaten Stroms in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="e3571-284">For Dolby Digital (AC-3) streams, specifies the bit rate of the input stream in bits per second.</span></span> <span data-ttu-id="e3571-285">Für Dolby Digital Plus (E-AC3) ist der Wert immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e3571-285">For Dolby Digital Plus (E-AC3), the value is always zero.</span></span><br/> <span data-ttu-id="e3571-286">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e3571-286">Read only.</span></span><br/>                                                                                              |
| [<span data-ttu-id="e3571-287">Codecapi \_ avdecdddynamicrangescalehigh</span><span class="sxs-lookup"><span data-stu-id="e3571-287">CODECAPI\_AVDecDDDynamicRangeScaleHigh</span></span>](../directshow/avdecdddynamicrangescalehigh-property.md)    | <span data-ttu-id="e3571-288">Der auf hoher Ebene ausgeschnittene, wenn der Decoder das dynamische Bereichs Steuerelement ausführt.</span><span class="sxs-lookup"><span data-stu-id="e3571-288">The high-level cut when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="e3571-289">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e3571-289">Read/write.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="e3571-290">Codecapi \_ avdecdddynamicrangescalelow</span><span class="sxs-lookup"><span data-stu-id="e3571-290">CODECAPI\_AVDecDDDynamicRangeScaleLow</span></span>](../directshow/avdecdddynamicrangescalelow-property.md)      | <span data-ttu-id="e3571-291">Die Verstärkung auf niedriger Ebene, wenn der Decoder das dynamische Bereichs Steuerelement ausführt.</span><span class="sxs-lookup"><span data-stu-id="e3571-291">The low-level boost when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="e3571-292">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e3571-292">Read/write.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="e3571-293">Codecapi \_ avdecddoperationalmode</span><span class="sxs-lookup"><span data-stu-id="e3571-293">CODECAPI\_AVDecDDOperationalMode</span></span>](../directshow/avdecddoperationalmode-property.md)                | <span data-ttu-id="e3571-294">Der Komprimierungs Steuerelement Modus.</span><span class="sxs-lookup"><span data-stu-id="e3571-294">The compression control mode.</span></span><br/> <span data-ttu-id="e3571-295">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e3571-295">Read/write.</span></span><br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="e3571-296">Codecapi \_ avdecddstereodownmixmode</span><span class="sxs-lookup"><span data-stu-id="e3571-296">CODECAPI\_AVDecDDStereoDownMixMode</span></span>](codecapi-avdecddstereodownmixmode.md)              | <span data-ttu-id="e3571-297">Der Typ der Stereo downmischung.</span><span class="sxs-lookup"><span data-stu-id="e3571-297">The type of stereo downmix.</span></span> <span data-ttu-id="e3571-298">Diese Eigenschaft ist gültig, wenn es sich bei der Eingabe um einen Multichannel-Stream handelt und die Ausgabe ein Stereodaten Strom ist</span><span class="sxs-lookup"><span data-stu-id="e3571-298">This property applies when the input is a multichannel stream and the output is a stereo stream.</span></span><br/> <span data-ttu-id="e3571-299">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e3571-299">Read/write.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="e3571-300">MFT- \_ Unterstützung für \_ dynamisches \_ Format \_ ändern</span><span class="sxs-lookup"><span data-stu-id="e3571-300">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="e3571-301">Dieses Attribut gibt **false** zurück, um anzugeben, dass der Decoder vor dem Festlegen eines neuen Eingabetyps entladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="e3571-301">This attribute returns **FALSE**, indicating that the decoder must be drained before a new input type is set.</span></span><br/> <span data-ttu-id="e3571-302">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e3571-302">Read/write.</span></span><br/>                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="e3571-303">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3571-303">Remarks</span></span>

<span data-ttu-id="e3571-304">Der Decoder akzeptiert nur unformatierte Dolby Streams, wie von A/52b definiert.</span><span class="sxs-lookup"><span data-stu-id="e3571-304">The decoder accepts only raw Dolby streams, as defined by A/52B.</span></span> <span data-ttu-id="e3571-305">Nutzlasten, wie z. b. "packetisiert Elementary Streams" (PES) werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3571-305">Payloads such as Packetized Elementary Streams (PES) are not supported.</span></span> <span data-ttu-id="e3571-306">Für Dolby Digital Plus decodiert der Decoder bis zu 5,1 Kanäle.</span><span class="sxs-lookup"><span data-stu-id="e3571-306">For Dolby Digital Plus, the decoder decodes up to 5.1 channels.</span></span> <span data-ttu-id="e3571-307">Unter Windows 10 werden 7,1-kanalstreams ohne Downmix decodiert.</span><span class="sxs-lookup"><span data-stu-id="e3571-307">On Windows 10, 7.1 channel streams are decoded without downmix.</span></span> <span data-ttu-id="e3571-308">Bei früheren Betriebssystemversionen, wenn der Stream 7,1-Kanäle ist, wird nur die 5,1-kanaldownmischung decodiert.</span><span class="sxs-lookup"><span data-stu-id="e3571-308">On previous OS versions, if the stream is 7.1 channels, only the 5.1 channel downmix will be decoded.</span></span> <span data-ttu-id="e3571-309">Wenn der Stream Dolby Digital Plus mit mehr als einem unabhängigen untergeordneten Stream ist, wird nur der unabhängige unter Datenstrom 0 decodiert.</span><span class="sxs-lookup"><span data-stu-id="e3571-309">If the stream is Dolby Digital Plus with more than one independent substream, only independent substream 0 is decoded.</span></span> <span data-ttu-id="e3571-310">Der Decoder überspringt andere unabhängige unter Ströme.</span><span class="sxs-lookup"><span data-stu-id="e3571-310">The decoder skips other independent substreams.</span></span> <span data-ttu-id="e3571-311">Außerdem überspringt der Decoder alle abhängigen unter Ströme.</span><span class="sxs-lookup"><span data-stu-id="e3571-311">In addition, the decoder skips all dependent substreams.</span></span> <span data-ttu-id="e3571-312">Der Decoder unterstützt das Entschlüsseln und Decodieren von Streams, die durch Digital Rights Management-Technologie (DRM) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="e3571-312">The decoder supports decryption and decoding of streams that are protected by Digital Rights Management (DRM) technology.</span></span>

<span data-ttu-id="e3571-313">Wenn der Eingabe Medientyp über eine andere Kanal Konfiguration als Mono, Stereo oder Dual-Mono (ohne LFE-Kanal) verfügt, stellt der Decoder zwei Optionen für die Ausgabekanal Konfigurationen bereit:</span><span class="sxs-lookup"><span data-stu-id="e3571-313">If the input media type has a channel configuration other than mono, stereo, or dual-mono (all without LFE channel), the decoder provides two options for the output channel configurations:</span></span>

-   <span data-ttu-id="e3571-314">8-Kanal-Ausgabe (7,1-Kanal Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="e3571-314">8-channel output (7.1 channel configuration)</span></span>
-   <span data-ttu-id="e3571-315">6-Kanal-Ausgabe (5,1-Kanal Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="e3571-315">6-channel output (5.1 channel configuration)</span></span>
-   <span data-ttu-id="e3571-316">Stereo-Downmix</span><span class="sxs-lookup"><span data-stu-id="e3571-316">Stereo downmix</span></span>

<span data-ttu-id="e3571-317">Wenn Stereo Downmix ausgewählt ist, kann der Typ von Downmix auf der MFT mithilfe der [codecapi \_ avdecddstereodownmixmode](codecapi-avdecddstereodownmixmode.md) -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3571-317">If stereo downmix is selected, the type of downmix can be set on the MFT by using the [CODECAPI\_AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) property.</span></span>

<span data-ttu-id="e3571-318">Wenn der Ausgabetyp **MF Audioformat \_ Dolby \_ AC3 \_ SPDIF** ist, enthält jeder Ausgabepuffer 6.144 bytes.</span><span class="sxs-lookup"><span data-stu-id="e3571-318">If the output type is **MFAudioFormat\_Dolby\_AC3\_SPDIF**, each output buffer contains 6,144 bytes.</span></span> <span data-ttu-id="e3571-319">Der Puffer beginnt mit einem 8-Byte-S/PDIF-Header, gefolgt von einem komprimierten AC-3-Frame, gefolgt von 0 (null) bis 6.144 bytes.</span><span class="sxs-lookup"><span data-stu-id="e3571-319">The buffer starts with an 8-byte S/PDIF header, followed by a compressed AC-3 frame, followed by zero padding to 6,144 bytes.</span></span>

<span data-ttu-id="e3571-320">Wenn der Ausgabetyp **ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital \_ plus** ist, enthält jeder Ausgabepuffer 24.576 Bytes.</span><span class="sxs-lookup"><span data-stu-id="e3571-320">If the output type is **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**, each output buffer contains 24,576 bytes.</span></span> <span data-ttu-id="e3571-321">Der Puffer beginnt mit einem 8-Byte-S/PDIF-Header, gefolgt von 1 – 6 komprimierten Dolby Digital Plus-Frames, die 1.536 PCM-Stichproben entsprechen, gefolgt von einer NULL-Auffüll Funktion auf 24.576 Bytes.</span><span class="sxs-lookup"><span data-stu-id="e3571-321">The buffer starts with an 8-byte S/PDIF header, followed by 1–6 compressed Dolby Digital Plus frames corresponding to 1,536 PCM samples, followed by zero padding to 24,576 bytes.</span></span> <span data-ttu-id="e3571-322">Bei der HDMI-Ausgabe wird nur der unabhängige unter Datenstrom 0 gepackt.</span><span class="sxs-lookup"><span data-stu-id="e3571-322">For HDMI output, only independent substream 0 is packed.</span></span>

<span data-ttu-id="e3571-323">Der Decoder-MFT ist mit dem Flag " **MFT \_ Enum \_ Flag \_ fieldofuse**" registriert, das angibt, dass die MFT von der Anwendung vor der Verwendung entsperrt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e3571-323">The decoder MFT is registered with the flag **MFT\_ENUM\_FLAG\_FIELDOFUSE**, which indicates that the MFT that must be unlocked by the application before use.</span></span> <span data-ttu-id="e3571-324">Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung".</span><span class="sxs-lookup"><span data-stu-id="e3571-324">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3571-325">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3571-325">Requirements</span></span>



| <span data-ttu-id="e3571-326">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3571-326">Requirement</span></span> | <span data-ttu-id="e3571-327">Wert</span><span class="sxs-lookup"><span data-stu-id="e3571-327">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3571-328">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3571-328">Minimum supported client</span></span><br/> | <span data-ttu-id="e3571-329">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e3571-329">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="e3571-330">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3571-330">Minimum supported server</span></span><br/> | <span data-ttu-id="e3571-331">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e3571-331">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="e3571-332">DLL</span><span class="sxs-lookup"><span data-stu-id="e3571-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3571-333"><dt>Msauddecmft.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3571-333"><dt>Msauddecmft.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3571-334">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3571-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3571-335">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="e3571-335">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
