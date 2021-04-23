---
description: MPEG-2-Splitter-Medientypen
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2-Splitter-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909427"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="6a6ca-103">MPEG-2-Splitter-Medientypen</span><span class="sxs-lookup"><span data-stu-id="6a6ca-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="6a6ca-104">Der [MPEG-2-Splitterfilter](mpeg-2-splitter.md) unterstützt derzeit Audio und Video.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="6a6ca-105">Dolby AC-3 wird als Teilstream unterstützt, wie von DVD definiert.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="6a6ca-106">Der Filter unterstützt auch MPEG-2-Audio.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="6a6ca-107">Die Medientypen hängen davon ab, ob der MPEG-2-Splitter PES-Pakete oder PES-Nutzlasten liefert.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="6a6ca-108">Video</span><span class="sxs-lookup"><span data-stu-id="6a6ca-108">Video</span></span>

<span data-ttu-id="6a6ca-109">Für MPEG-2-Videos lauten die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-109">For MPEG-2 video, the media types are as follows.</span></span>



| <span data-ttu-id="6a6ca-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="6a6ca-110">Label</span></span> | <span data-ttu-id="6a6ca-111">Wert</span><span class="sxs-lookup"><span data-stu-id="6a6ca-111">Value</span></span> |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="6a6ca-112">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-112">PES output</span></span>                               | <span data-ttu-id="6a6ca-113">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-113">Payload output</span></span>                 |
| <span data-ttu-id="6a6ca-114">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-114">Major Type</span></span>       | <span data-ttu-id="6a6ca-115">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-115">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="6a6ca-116">**\_MEDIATYPE-Video**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-116">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="6a6ca-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="6a6ca-117">Subtype</span></span>          | <span data-ttu-id="6a6ca-118">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-118">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="6a6ca-119">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-119">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="6a6ca-120">Formattyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-120">Format Type</span></span>      | <span data-ttu-id="6a6ca-121">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-121">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="6a6ca-122">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-122">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="6a6ca-123">Formatstruktur</span><span class="sxs-lookup"><span data-stu-id="6a6ca-123">Format Structure</span></span> | [<span data-ttu-id="6a6ca-124">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-124">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="6a6ca-125">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-125">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="6a6ca-126">AC-3-Audio</span><span class="sxs-lookup"><span data-stu-id="6a6ca-126">AC-3 Audio</span></span>

<span data-ttu-id="6a6ca-127">Für AC-3-Audio sind die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-127">For AC-3 audio, the media types are as follows.</span></span>



| <span data-ttu-id="6a6ca-128">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="6a6ca-128">Label</span></span> | <span data-ttu-id="6a6ca-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6a6ca-129">Value</span></span> |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="6a6ca-130">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-130">PES output</span></span>                           | <span data-ttu-id="6a6ca-131">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-131">Payload output</span></span>               |
| <span data-ttu-id="6a6ca-132">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-132">Major Type</span></span>       | <span data-ttu-id="6a6ca-133">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="6a6ca-133">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="6a6ca-134">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-134">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="6a6ca-135">Subtype</span><span class="sxs-lookup"><span data-stu-id="6a6ca-135">Subtype</span></span>          | <span data-ttu-id="6a6ca-136">MEDIASUBTYPE \_ DOLBY \_ AC3</span><span class="sxs-lookup"><span data-stu-id="6a6ca-136">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="6a6ca-137">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-137">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="6a6ca-138">Formattyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-138">Format Type</span></span>      | <span data-ttu-id="6a6ca-139">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="6a6ca-139">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="6a6ca-140">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-140">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="6a6ca-141">Formatstruktur</span><span class="sxs-lookup"><span data-stu-id="6a6ca-141">Format Structure</span></span> | <span data-ttu-id="6a6ca-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a6ca-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="6a6ca-143">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-143">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="6a6ca-144">Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für AC-3 ist derzeit **WAVE FORMAT \_ \_ UNKNOWN**, aber dies kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-144">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="6a6ca-145">MPEG-2-Audio</span><span class="sxs-lookup"><span data-stu-id="6a6ca-145">MPEG-2 Audio</span></span>

<span data-ttu-id="6a6ca-146">Für MPEG-2-Audio sind die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-146">For MPEG-2 audio, the media types are as follows.</span></span>



| <span data-ttu-id="6a6ca-147">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="6a6ca-147">Label</span></span> | <span data-ttu-id="6a6ca-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6a6ca-148">Value</span></span> |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="6a6ca-149">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-149">PES output</span></span>                    | <span data-ttu-id="6a6ca-150">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-150">Payload output</span></span>                 |
| <span data-ttu-id="6a6ca-151">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-151">Major Type</span></span>       | <span data-ttu-id="6a6ca-152">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-152">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="6a6ca-153">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-153">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="6a6ca-154">Subtype</span><span class="sxs-lookup"><span data-stu-id="6a6ca-154">Subtype</span></span>          | <span data-ttu-id="6a6ca-155">**MEDIASUBTYE \_ \_ MPEG2-AUDIO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-155">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="6a6ca-156">**MEDIASUBTYPE \_ \_ MPEG2-AUDIO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-156">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="6a6ca-157">Formattyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-157">Format Type</span></span>      | <span data-ttu-id="6a6ca-158">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-158">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="6a6ca-159">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-159">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="6a6ca-160">Formatstruktur</span><span class="sxs-lookup"><span data-stu-id="6a6ca-160">Format Structure</span></span> | <span data-ttu-id="6a6ca-161">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-161">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="6a6ca-162">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-162">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="6a6ca-163">Das **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für MPEG-2 Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN,** aber dies kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-163">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="6a6ca-164">Der MPEG-2-Splitter geht davon aus, dass datenströme D0 bis DF für den Multichannel-Erweiterungsstream verwendet werden, wie sie für MPEG-2-DVD-Audio verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-164">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="6a6ca-165">Daher werden die Pakete bei jeder Auswahl von Stream C *x* vom Splitter auch für Stream D *x* weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-165">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="6a6ca-166">LPCM-Audio</span><span class="sxs-lookup"><span data-stu-id="6a6ca-166">LPCM Audio</span></span>

<span data-ttu-id="6a6ca-167">Für LPCM-Audio lauten die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-167">For LPCM audio, the media types are as follows.</span></span>



| <span data-ttu-id="6a6ca-168">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="6a6ca-168">Label</span></span> | <span data-ttu-id="6a6ca-169">Wert</span><span class="sxs-lookup"><span data-stu-id="6a6ca-169">Value</span></span> |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="6a6ca-170">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-170">PES output</span></span>                         | <span data-ttu-id="6a6ca-171">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="6a6ca-171">Payload output</span></span>                     |
| <span data-ttu-id="6a6ca-172">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-172">Major Type</span></span>       | <span data-ttu-id="6a6ca-173">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-173">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="6a6ca-174">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-174">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="6a6ca-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="6a6ca-175">Subtype</span></span>          | <span data-ttu-id="6a6ca-176">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-176">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="6a6ca-177">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-177">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="6a6ca-178">Formattyp</span><span class="sxs-lookup"><span data-stu-id="6a6ca-178">Format Type</span></span>      | <span data-ttu-id="6a6ca-179">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-179">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="6a6ca-180">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-180">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="6a6ca-181">Formatstruktur</span><span class="sxs-lookup"><span data-stu-id="6a6ca-181">Format Structure</span></span> | <span data-ttu-id="6a6ca-182">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-182">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="6a6ca-183">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="6a6ca-183">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="6a6ca-184">Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für LPCM-Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN,** aber dies kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="6a6ca-184">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a6ca-185">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a6ca-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a6ca-186">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="6a6ca-186">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
