---
description: In diesem Abschnitt werden die Media Foundation Matroska Media Container-Dateien (MKV) beschrieben.
title: Matroska Media Container -Unterstützung (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154215"
---
# <a name="matroska-media-container-mkv-support"></a><span data-ttu-id="bd368-103">Matroska Media Container -Unterstützung (MKV)</span><span class="sxs-lookup"><span data-stu-id="bd368-103">Matroska Media Container (MKV) support</span></span>

<span data-ttu-id="bd368-104">In diesem Abschnitt werden die Media Foundation Matroska Media Container-Dateien (MKV) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd368-104">This section describes the Media Foundation support for Matroska Media Container (MKV) files.</span></span>

<span data-ttu-id="bd368-105">Das MKV-Format kann mehrere Video- und Audiocodecs unterstützen, z. B. H.264- und AAC-Audio.</span><span class="sxs-lookup"><span data-stu-id="bd368-105">The MKV format can support multiple video and audio codecs, such as H.264 and AAC audio.</span></span> <span data-ttu-id="bd368-106">Im Allgemeinen beschreiben Container, wie Video- und Audiodaten angelegt werden und welche ergänzenden Informationen verwendet werden, um diese A/V-Streams zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="bd368-106">In general, containers describe how video and audio data is laid out and what supplementary information is used to describe those A/V streams.</span></span> <span data-ttu-id="bd368-107">Container können auch Daten enthalten, die A/V-Streams ergänzen, z. B. Titel, Sprachen der Audiostreams, Untertitel- oder Untertiteltitel, Schriftarten für diese Untertitel, Bilder, Kapitelinformationen und Menüs.</span><span class="sxs-lookup"><span data-stu-id="bd368-107">Containers can also include data that complements A/V streams, such as the title, languages of the audio streams, subtitle or caption tracks, fonts for those subtitles, images, chapter information, and menus.</span></span> <span data-ttu-id="bd368-108">MKV ist ein äußerst flexibles Format, das viele dieser Containerfeatures unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd368-108">MKV is a highly flexible format that supports many of these container features.</span></span> <span data-ttu-id="bd368-109">Weitere Informationen zum MKV-Format finden Sie unter [https://matroska.org](https://matroska.org/)</span><span class="sxs-lookup"><span data-stu-id="bd368-109">For more info about the MKV format, see [https://matroska.org](https://matroska.org/)</span></span>


## <a name="mkv-container-feature-support"></a><span data-ttu-id="bd368-110">Unterstützung von MKV-Containerfeatures</span><span class="sxs-lookup"><span data-stu-id="bd368-110">MKV container feature support</span></span>
<span data-ttu-id="bd368-111">MKV-Containerfeatures werden auf der von Media Foundation wie folgt unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bd368-111">MKV container features are supported on the by Media Foundation in the following ways:</span></span>
- <span data-ttu-id="bd368-112">Wenn eine oder mehrere Videospuren vorhanden sind, wird der erste Titel abgespielt.</span><span class="sxs-lookup"><span data-stu-id="bd368-112">If one or more video tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="bd368-113">Wenn eine oder mehrere Audiospuren vorhanden sind, wird der erste Titel abgespielt.</span><span class="sxs-lookup"><span data-stu-id="bd368-113">If one or more audio tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="bd368-114">Untertiteltitel werden unterstützt, sind aber standardmäßig nicht ausgewählt (abgespielt).</span><span class="sxs-lookup"><span data-stu-id="bd368-114">Caption tracks are supported, but are not selected (played) by default.</span></span>
- <span data-ttu-id="bd368-115">Wenn eine oder mehrere Schriftarten oder Bilder vorhanden sind, werden Untertitel und Bilder nicht gerendert, obwohl die Datei geladen und wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd368-115">If one or more fonts or images are present, captions and images won’t render, although the file will load and play.</span></span>
- <span data-ttu-id="bd368-116">Menüinformationen werden nicht unterstützt und nicht angezeigt, aber die Datei wird geladen und abspielt.</span><span class="sxs-lookup"><span data-stu-id="bd368-116">Menu information is not supported and won’t be displayed, but the file will load and play.</span></span>
- <span data-ttu-id="bd368-117">Wenn Dateien mit Kapiteln auf ergänzende Dateien verweisen, werden die ergänzenden Dateien nicht wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd368-117">If files with chapters refer to supplemental files, the supplemental files won’t play.</span></span>
- <span data-ttu-id="bd368-118">Miniaturansichten sind verfügbar, wenn Sie mithilfe des Dateibrowsers nach Dateien auf USB-Laufwerken suchen.</span><span class="sxs-lookup"><span data-stu-id="bd368-118">Thumbnail images are available when browsing for files on USB drives using the file browser.</span></span>

<span data-ttu-id="bd368-119">Dieser Satz von Features sollte die Wiedergabe der meisten MKV-Dateien ermöglichen, wenn sie unterstützte Codecs enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd368-119">This set of features should allow playback of most MKV files if they contain supported codecs.</span></span>
<span data-ttu-id="bd368-120">MKV-Dateien, die Video- und Audiospuren enthalten, die mit den im folgenden Abschnitt aufgeführten Codecs codiert sind, werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd368-120">MKV files that contain video and audio tracks encoded with the codecs listed in the following section are supported.</span></span>

## <a name="supported-mkv-codecs"></a><span data-ttu-id="bd368-121">Unterstützte MKV-Codecs</span><span class="sxs-lookup"><span data-stu-id="bd368-121">Supported MKV codecs</span></span>

### <a name="video-codec-support-for-mkv"></a><span data-ttu-id="bd368-122">Videocodec-Unterstützung für MKV</span><span class="sxs-lookup"><span data-stu-id="bd368-122">Video codec support for MKV</span></span>

<span data-ttu-id="bd368-123">Matroska-ID: V_MPEG4/ISO/AVC</span><span class="sxs-lookup"><span data-stu-id="bd368-123">Matroska ID: V_MPEG4/ISO/AVC</span></span>

- <span data-ttu-id="bd368-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span><span class="sxs-lookup"><span data-stu-id="bd368-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span></span>
- <span data-ttu-id="bd368-125">Beschreibung: H.264-Video</span><span class="sxs-lookup"><span data-stu-id="bd368-125">Description: H.264 video</span></span>
- <span data-ttu-id="bd368-126">FourCC- oder WAV-Bezeichner: H264</span><span class="sxs-lookup"><span data-stu-id="bd368-126">FourCC or WAV identifiers: H264</span></span>

<span data-ttu-id="bd368-127">Matroska-ID: V_MPEG2</span><span class="sxs-lookup"><span data-stu-id="bd368-127">Matroska ID: V_MPEG2</span></span>

- <span data-ttu-id="bd368-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span><span class="sxs-lookup"><span data-stu-id="bd368-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span></span>
- <span data-ttu-id="bd368-129">Beschreibung: MPEG-2-Video</span><span class="sxs-lookup"><span data-stu-id="bd368-129">Description: MPEG-2 video</span></span>

<span data-ttu-id="bd368-130">Matroska-ID: V_MPEG1</span><span class="sxs-lookup"><span data-stu-id="bd368-130">Matroska ID: V_MPEG1</span></span>

- <span data-ttu-id="bd368-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span><span class="sxs-lookup"><span data-stu-id="bd368-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span></span>
- <span data-ttu-id="bd368-132">Beschreibung: MPEG-1-Video</span><span class="sxs-lookup"><span data-stu-id="bd368-132">Description: MPEG-1 video</span></span>
- <span data-ttu-id="bd368-133">FourCC- oder WAV-Bezeichner: MPG1</span><span class="sxs-lookup"><span data-stu-id="bd368-133">FourCC or WAV identifiers: MPG1</span></span>

<span data-ttu-id="bd368-134">Matroska-ID: V_MPEG4/MS/V3</span><span class="sxs-lookup"><span data-stu-id="bd368-134">Matroska ID: V_MPEG4/MS/V3</span></span>

- <span data-ttu-id="bd368-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span><span class="sxs-lookup"><span data-stu-id="bd368-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span></span>
- <span data-ttu-id="bd368-136">Beschreibung: Microsoft MPEG 4 Codec Version 3</span><span class="sxs-lookup"><span data-stu-id="bd368-136">Description: Microsoft MPEG 4 codec version 3</span></span>
- <span data-ttu-id="bd368-137">FourCC- oder WAV-Bezeichner: MP43</span><span class="sxs-lookup"><span data-stu-id="bd368-137">FourCC or WAV identifiers: MP43</span></span>

<span data-ttu-id="bd368-138">Matroska-ID: V_MPEG4/ISO/ASP</span><span class="sxs-lookup"><span data-stu-id="bd368-138">Matroska ID: V_MPEG4/ISO/ASP</span></span>

- <span data-ttu-id="bd368-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="bd368-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="bd368-140">Beschreibung: MPEG-4 Part 2 video (MPEG-4 Teil 2-Video)</span><span class="sxs-lookup"><span data-stu-id="bd368-140">Description: MPEG-4 part 2 video</span></span>
- <span data-ttu-id="bd368-141">FourCC- oder WAV-Bezeichner: MP4V</span><span class="sxs-lookup"><span data-stu-id="bd368-141">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="bd368-142">Matroska-ID: V_MS/VFW/FOURCC</span><span class="sxs-lookup"><span data-stu-id="bd368-142">Matroska ID: V_MS/VFW/FOURCC</span></span>

- <span data-ttu-id="bd368-143">Beschreibung: Wird mehreren Codecs im AVI-Format, die in der Konsole verfügbar sind, normalerweise unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd368-143">Description: Maps to several codecs usually supported in the AVI format that are available on the console.</span></span>

<span data-ttu-id="bd368-144">Matroska-ID: V_THEORA</span><span class="sxs-lookup"><span data-stu-id="bd368-144">Matroska ID: V_THEORA</span></span>

- <span data-ttu-id="bd368-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span><span class="sxs-lookup"><span data-stu-id="bd368-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span></span>
- <span data-ttu-id="bd368-146">Beschreibung: Theora</span><span class="sxs-lookup"><span data-stu-id="bd368-146">Description: Theora</span></span>
- <span data-ttu-id="bd368-147">FourCC- oder WAV-Bezeichner: theo</span><span class="sxs-lookup"><span data-stu-id="bd368-147">FourCC or WAV identifiers: theo</span></span>

<span data-ttu-id="bd368-148">Matroska-ID: V_MPEG4/ISO/SP</span><span class="sxs-lookup"><span data-stu-id="bd368-148">Matroska ID: V_MPEG4/ISO/SP</span></span>

- <span data-ttu-id="bd368-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="bd368-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="bd368-150">Beschreibung: MPEG4 ISO Simple Profile (DivX4)</span><span class="sxs-lookup"><span data-stu-id="bd368-150">Description: MPEG4 ISO simple profile (DivX4)</span></span>
- <span data-ttu-id="bd368-151">FourCC- oder WAV-Bezeichner: MP4V</span><span class="sxs-lookup"><span data-stu-id="bd368-151">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="bd368-152">Matroska-ID: V_MPEG4/ISO/AP</span><span class="sxs-lookup"><span data-stu-id="bd368-152">Matroska ID: V_MPEG4/ISO/AP</span></span>

- <span data-ttu-id="bd368-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="bd368-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="bd368-154">Beschreibung: MPEG4 ISO advanced simple profile (DivX5,IgenD, FFMPEG)</span><span class="sxs-lookup"><span data-stu-id="bd368-154">Description: MPEG4 ISO advanced simple profile (DivX5, XviD, FFMPEG)</span></span>
- <span data-ttu-id="bd368-155">FourCC- oder WAV-Bezeichner: MP4V</span><span class="sxs-lookup"><span data-stu-id="bd368-155">FourCC or WAV identifiers: MP4V</span></span>


<span data-ttu-id="bd368-156">Matroska-ID: V_MPEGH/ISO/HEVC</span><span class="sxs-lookup"><span data-stu-id="bd368-156">Matroska ID: V_MPEGH/ISO/HEVC</span></span> 

- <span data-ttu-id="bd368-157">MSFT-Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span><span class="sxs-lookup"><span data-stu-id="bd368-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span></span>
- <span data-ttu-id="bd368-158">Beschreibung: HEVC/H.265</span><span class="sxs-lookup"><span data-stu-id="bd368-158">Description: HEVC/H.265</span></span>
- <span data-ttu-id="bd368-159">FourCC- oder WAV-Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bd368-159">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="bd368-160">Matroska-ID: V_VP8</span><span class="sxs-lookup"><span data-stu-id="bd368-160">Matroska ID: V_VP8</span></span>

- <span data-ttu-id="bd368-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span><span class="sxs-lookup"><span data-stu-id="bd368-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span></span>
- <span data-ttu-id="bd368-162">Beschreibung: VP8-Codecformat</span><span class="sxs-lookup"><span data-stu-id="bd368-162">Description: VP8 Codec format</span></span>
- <span data-ttu-id="bd368-163">FourCC- oder WAV-Bezeichner: VP80</span><span class="sxs-lookup"><span data-stu-id="bd368-163">FourCC or WAV identifiers: VP80</span></span>

<span data-ttu-id="bd368-164">Matroska-ID: V_VP9</span><span class="sxs-lookup"><span data-stu-id="bd368-164">Matroska ID: V_VP9</span></span>

- <span data-ttu-id="bd368-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span><span class="sxs-lookup"><span data-stu-id="bd368-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span></span>
- <span data-ttu-id="bd368-166">Beschreibung: VP9-Codecformat</span><span class="sxs-lookup"><span data-stu-id="bd368-166">Description: VP9 Codec format</span></span>
- <span data-ttu-id="bd368-167">FourCC- oder WAV-Bezeichner: VP90</span><span class="sxs-lookup"><span data-stu-id="bd368-167">FourCC or WAV identifiers: VP90</span></span>

<span data-ttu-id="bd368-168">Matroska-ID: V_MJPEG</span><span class="sxs-lookup"><span data-stu-id="bd368-168">Matroska ID: V_MJPEG</span></span>

- <span data-ttu-id="bd368-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span><span class="sxs-lookup"><span data-stu-id="bd368-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span></span>
- <span data-ttu-id="bd368-170">Beschreibung: Motion JPEG</span><span class="sxs-lookup"><span data-stu-id="bd368-170">Description: Motion JPEG</span></span>
- <span data-ttu-id="bd368-171">FourCC- oder WAV-Bezeichner: MJPG</span><span class="sxs-lookup"><span data-stu-id="bd368-171">FourCC or WAV identifiers: MJPG</span></span>

<span data-ttu-id="bd368-172">Matroska-ID: V_AV1</span><span class="sxs-lookup"><span data-stu-id="bd368-172">Matroska ID: V_AV1</span></span>

- <span data-ttu-id="bd368-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span><span class="sxs-lookup"><span data-stu-id="bd368-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span></span>
- <span data-ttu-id="bd368-174">Beschreibung: AOMedia Video 1</span><span class="sxs-lookup"><span data-stu-id="bd368-174">Description: AOMedia Video 1</span></span>
- <span data-ttu-id="bd368-175">FourCC- oder WAV-Bezeichner: AV01</span><span class="sxs-lookup"><span data-stu-id="bd368-175">FourCC or WAV identifiers: AV01</span></span>

### <a name="audio-codec-support-for-mkv"></a><span data-ttu-id="bd368-176">Audiocodec-Unterstützung für MKV</span><span class="sxs-lookup"><span data-stu-id="bd368-176">Audio codec support for MKV</span></span>

<span data-ttu-id="bd368-177">Matroska-ID: A_AAC</span><span class="sxs-lookup"><span data-stu-id="bd368-177">Matroska ID: A_AAC</span></span>

- <span data-ttu-id="bd368-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="bd368-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="bd368-179">Beschreibung: Erweiterte Audiocodierung (Advanced Audio Coding, AAC)</span><span class="sxs-lookup"><span data-stu-id="bd368-179">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="bd368-180">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="bd368-180">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="bd368-181">Matroska-ID: A_AC3</span><span class="sxs-lookup"><span data-stu-id="bd368-181">Matroska ID: A_AC3</span></span>

- <span data-ttu-id="bd368-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span><span class="sxs-lookup"><span data-stu-id="bd368-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span></span>
- <span data-ttu-id="bd368-183">Beschreibung: Dolby AC3</span><span class="sxs-lookup"><span data-stu-id="bd368-183">Description: Dolby AC3</span></span>
- <span data-ttu-id="bd368-184">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="bd368-184">FourCC or WAV identifiers: WAVE_FORMAT_DOLBY_AC3_SPDIF</span></span>

<span data-ttu-id="bd368-185">Matroska-ID: A_MPEG/L3</span><span class="sxs-lookup"><span data-stu-id="bd368-185">Matroska ID: A_MPEG/L3</span></span>

- <span data-ttu-id="bd368-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span><span class="sxs-lookup"><span data-stu-id="bd368-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span></span>
- <span data-ttu-id="bd368-187">Beschreibung: MPEG Audio Layer-3 (MP3)</span><span class="sxs-lookup"><span data-stu-id="bd368-187">Description: MPEG Audio Layer-3 (MP3)</span></span>
- <span data-ttu-id="bd368-188">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="bd368-188">FourCC or WAV identifiers: WAVE_FORMAT_MPEGLAYER3</span></span>

<span data-ttu-id="bd368-189">Matroska-ID: A_MPEG/L1</span><span class="sxs-lookup"><span data-stu-id="bd368-189">Matroska ID: A_MPEG/L1</span></span>

- <span data-ttu-id="bd368-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="bd368-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="bd368-191">Beschreibung: MPEG-1-Audionutzlast</span><span class="sxs-lookup"><span data-stu-id="bd368-191">Description: MPEG-1 audio payload</span></span>
- <span data-ttu-id="bd368-192">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="bd368-192">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="bd368-193">Matroska-ID: A_PCM/INT/BIG</span><span class="sxs-lookup"><span data-stu-id="bd368-193">Matroska ID: A_PCM/INT/BIG</span></span>

- <span data-ttu-id="bd368-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="bd368-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="bd368-195">Beschreibung: Unkomprimierte PCM-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="bd368-195">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="bd368-196">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="bd368-196">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="bd368-197">Matroska-ID: A_PCM/INT/LIT</span><span class="sxs-lookup"><span data-stu-id="bd368-197">Matroska ID: A_PCM/INT/LIT</span></span>

- <span data-ttu-id="bd368-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="bd368-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="bd368-199">Beschreibung: Unkomprimierte PCM-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="bd368-199">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="bd368-200">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="bd368-200">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="bd368-201">Matroska-ID: A_PCM/FLOAT/IEEE</span><span class="sxs-lookup"><span data-stu-id="bd368-201">Matroska ID: A_PCM/FLOAT/IEEE</span></span>

- <span data-ttu-id="bd368-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span><span class="sxs-lookup"><span data-stu-id="bd368-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span></span>
- <span data-ttu-id="bd368-203">Beschreibung: Unkomprimierte IEEE-Gleitkommaaudio</span><span class="sxs-lookup"><span data-stu-id="bd368-203">Description: Uncompressed IEEE floating-point audio</span></span>
- <span data-ttu-id="bd368-204">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd368-204">FourCC or WAV identifiers: WAVE_FORMAT_IEEE_FLOAT</span></span>

<span data-ttu-id="bd368-205">Matroska-ID: A_ALAC</span><span class="sxs-lookup"><span data-stu-id="bd368-205">Matroska ID: A_ALAC</span></span>

- <span data-ttu-id="bd368-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span><span class="sxs-lookup"><span data-stu-id="bd368-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span></span>
- <span data-ttu-id="bd368-207">Beschreibung: Apple Lossless Audio Codec</span><span class="sxs-lookup"><span data-stu-id="bd368-207">Description: Apple Lossless Audio Codec</span></span>
- <span data-ttu-id="bd368-208">FourCC- oder WAV-Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bd368-208">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="bd368-209">Matroska-ID: A_MPEG/L2</span><span class="sxs-lookup"><span data-stu-id="bd368-209">Matroska ID: A_MPEG/L2</span></span>

- <span data-ttu-id="bd368-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="bd368-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="bd368-211">Beschreibung: MPEG Audio 1, 2 Layer II</span><span class="sxs-lookup"><span data-stu-id="bd368-211">Description: MPEG Audio 1, 2 Layer II</span></span>
- <span data-ttu-id="bd368-212">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="bd368-212">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="bd368-213">Matroska-ID: A_DTS</span><span class="sxs-lookup"><span data-stu-id="bd368-213">Matroska ID: A_DTS</span></span>

- <span data-ttu-id="bd368-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span><span class="sxs-lookup"><span data-stu-id="bd368-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span></span>
- <span data-ttu-id="bd368-215">Beschreibung: DigitalSchreibesystem</span><span class="sxs-lookup"><span data-stu-id="bd368-215">Description: Digital Theatre System</span></span>
- <span data-ttu-id="bd368-216">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_DTS</span><span class="sxs-lookup"><span data-stu-id="bd368-216">FourCC or WAV identifiers: WAVE_FORMAT_DTS</span></span>

<span data-ttu-id="bd368-217">Matroska-ID: A_OPUS</span><span class="sxs-lookup"><span data-stu-id="bd368-217">Matroska ID: A_OPUS</span></span>

- <span data-ttu-id="bd368-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span><span class="sxs-lookup"><span data-stu-id="bd368-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span></span>
- <span data-ttu-id="bd368-219">Beschreibung: Opus</span><span class="sxs-lookup"><span data-stu-id="bd368-219">Description: Opus</span></span>
- <span data-ttu-id="bd368-220">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_OPUS</span><span class="sxs-lookup"><span data-stu-id="bd368-220">FourCC or WAV identifiers: WAVE_FORMAT_OPUS</span></span>

<span data-ttu-id="bd368-221">Matroska-ID: A_VORBIS</span><span class="sxs-lookup"><span data-stu-id="bd368-221">Matroska ID: A_VORBIS</span></span>

- <span data-ttu-id="bd368-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span><span class="sxs-lookup"><span data-stu-id="bd368-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span></span>
- <span data-ttu-id="bd368-223">Beschreibung: Vorbis</span><span class="sxs-lookup"><span data-stu-id="bd368-223">Description: Vorbis</span></span>
- <span data-ttu-id="bd368-224">FourCC- oder WAV-Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bd368-224">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="bd368-225">Matroska-ID: A_FLAC</span><span class="sxs-lookup"><span data-stu-id="bd368-225">Matroska ID: A_FLAC</span></span>

- <span data-ttu-id="bd368-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span><span class="sxs-lookup"><span data-stu-id="bd368-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span></span>
- <span data-ttu-id="bd368-227">Beschreibung: Freier verlustfreier Audiocodec</span><span class="sxs-lookup"><span data-stu-id="bd368-227">Description: Free Lossless Audio Codec</span></span>
- <span data-ttu-id="bd368-228">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_FLAC</span><span class="sxs-lookup"><span data-stu-id="bd368-228">FourCC or WAV identifiers: WAVE_FORMAT_FLAC</span></span>

<span data-ttu-id="bd368-229">Matroska-ID: A_AAC/MAIN</span><span class="sxs-lookup"><span data-stu-id="bd368-229">Matroska ID: A_AAC/MAIN</span></span>

- <span data-ttu-id="bd368-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="bd368-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="bd368-231">Beschreibung: Erweiterte Audiocodierung (Advanced Audio Coding, AAC)</span><span class="sxs-lookup"><span data-stu-id="bd368-231">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="bd368-232">FourCC- oder WAV-Bezeichner: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="bd368-232">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="bd368-233">Matroska-ID: A_EAC3</span><span class="sxs-lookup"><span data-stu-id="bd368-233">Matroska ID: A_EAC3</span></span>

- <span data-ttu-id="bd368-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span><span class="sxs-lookup"><span data-stu-id="bd368-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span></span>
- <span data-ttu-id="bd368-235">Beschreibung: Erweiterte AC-3</span><span class="sxs-lookup"><span data-stu-id="bd368-235">Description: Enhanced AC-3</span></span>
- <span data-ttu-id="bd368-236">FourCC- oder WAV-Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bd368-236">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="bd368-237">Matroska-ID: A_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="bd368-237">Matroska ID: A_TRUEHD</span></span>

- <span data-ttu-id="bd368-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="bd368-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span></span>
- <span data-ttu-id="bd368-239">Beschreibung: Dolby TrueHD</span><span class="sxs-lookup"><span data-stu-id="bd368-239">Description: Dolby TrueHD</span></span>
- <span data-ttu-id="bd368-240">FourCC- oder WAV-Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bd368-240">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="bd368-241">Matroska-ID: A_MS/ACM</span><span class="sxs-lookup"><span data-stu-id="bd368-241">Matroska ID: A_MS/ACM</span></span>

- <span data-ttu-id="bd368-242">MSFT Media Foundation MF_MT_SUBTYPE: Wird mehreren in mmreg.h definierten WAVE_FORMAT Audiotypen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bd368-242">MSFT Media Foundation MF_MT_SUBTYPE: Maps to several WAVE_FORMAT audio types defined in mmreg.h</span></span>


### <a name="subtitles-codec-support-for-mkv"></a><span data-ttu-id="bd368-243">Unterstützung des Untertitelcodecs für MKV</span><span class="sxs-lookup"><span data-stu-id="bd368-243">Subtitles codec support for MKV</span></span>

<span data-ttu-id="bd368-244">Matroska-ID: S_TEXT/ASCII</span><span class="sxs-lookup"><span data-stu-id="bd368-244">Matroska ID: S_TEXT/ASCII</span></span>

- <span data-ttu-id="bd368-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="bd368-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="bd368-246">Beschreibung: ASCII-Text</span><span class="sxs-lookup"><span data-stu-id="bd368-246">Description: ASCII text</span></span>

<span data-ttu-id="bd368-247">Matroska-ID: S_TEXT/UTF8</span><span class="sxs-lookup"><span data-stu-id="bd368-247">Matroska ID: S_TEXT/UTF8</span></span>

- <span data-ttu-id="bd368-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="bd368-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="bd368-249">Beschreibung: UTF-8-Nur-Text</span><span class="sxs-lookup"><span data-stu-id="bd368-249">Description: UTF-8 Plain Text</span></span>

<span data-ttu-id="bd368-250">Matroska-ID: S_TEXT/SSA</span><span class="sxs-lookup"><span data-stu-id="bd368-250">Matroska ID: S_TEXT/SSA</span></span>

- <span data-ttu-id="bd368-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="bd368-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="bd368-252">Beschreibung: Untertitelformat</span><span class="sxs-lookup"><span data-stu-id="bd368-252">Description: Subtitles Format</span></span>

<span data-ttu-id="bd368-253">Matroska-ID: S_TEXT/ASS</span><span class="sxs-lookup"><span data-stu-id="bd368-253">Matroska ID: S_TEXT/ASS</span></span>

- <span data-ttu-id="bd368-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="bd368-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="bd368-255">Beschreibung: Erweitertes Untertitelformat</span><span class="sxs-lookup"><span data-stu-id="bd368-255">Description: Advanced Subtitles Format</span></span>

<span data-ttu-id="bd368-256">Matroska-ID: S_VOBSUB</span><span class="sxs-lookup"><span data-stu-id="bd368-256">Matroska ID: S_VOBSUB</span></span>

- <span data-ttu-id="bd368-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span><span class="sxs-lookup"><span data-stu-id="bd368-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span></span>
- <span data-ttu-id="bd368-258">Beschreibung: VobSub-Untertitel</span><span class="sxs-lookup"><span data-stu-id="bd368-258">Description: VobSub subtitles</span></span>

<span data-ttu-id="bd368-259">Matroska-ID: S_HDMV/PGS</span><span class="sxs-lookup"><span data-stu-id="bd368-259">Matroska ID: S_HDMV/PGS</span></span>

- <span data-ttu-id="bd368-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span><span class="sxs-lookup"><span data-stu-id="bd368-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span></span>
- <span data-ttu-id="bd368-261">Beschreibung: HDMV Presentation Graphics Untertitel (PGS)</span><span class="sxs-lookup"><span data-stu-id="bd368-261">Description: HDMV presentation graphics subtitles (PGS)</span></span>


## <a name="technical-details-regarding-codecs"></a><span data-ttu-id="bd368-262">Technische Details zu Codecs</span><span class="sxs-lookup"><span data-stu-id="bd368-262">Technical details regarding codecs</span></span>

<span data-ttu-id="bd368-263">Im Folgenden finden Sie technische Details zu Codecs.</span><span class="sxs-lookup"><span data-stu-id="bd368-263">See the following for technical details regarding codecs.</span></span>

- [<span data-ttu-id="bd368-264">Matroska-Codecspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bd368-264">Matroska Codec Specs</span></span>](http://www.matroska.org/technical/specs/codecid/index.html)
- [<span data-ttu-id="bd368-265">AudioUntertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="bd368-265">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
- [<span data-ttu-id="bd368-266">Video-Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="bd368-266">Video Subtype GUIDs</span></span>](video-subtype-guids.md)


## <a name="related-topics"></a><span data-ttu-id="bd368-267">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd368-267">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd368-268">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd368-268">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bd368-269">Media Foundation-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="bd368-269">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



