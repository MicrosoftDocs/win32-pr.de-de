---
description: MPEG-2-Splittermedientypen
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2-Splittermedientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119975"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="5d17c-103">MPEG-2-Splittermedientypen</span><span class="sxs-lookup"><span data-stu-id="5d17c-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="5d17c-104">Der [MPEG-2-Splitterfilter](mpeg-2-splitter.md) unterstützt derzeit Audio und Video.</span><span class="sxs-lookup"><span data-stu-id="5d17c-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="5d17c-105">Dolby AC-3 wird als Unterstream unterstützt, wie von dvd definiert.</span><span class="sxs-lookup"><span data-stu-id="5d17c-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="5d17c-106">Der Filter unterstützt auch MPEG-2-Audio.</span><span class="sxs-lookup"><span data-stu-id="5d17c-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="5d17c-107">Die Medientypen hängen davon ab, ob der MPEG-2-Splitter PES-Pakete oder PES-Nutzlasten liefert.</span><span class="sxs-lookup"><span data-stu-id="5d17c-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="5d17c-108">Video</span><span class="sxs-lookup"><span data-stu-id="5d17c-108">Video</span></span>

<span data-ttu-id="5d17c-109">Für MPEG-2-Videos sind die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5d17c-109">For MPEG-2 video, the media types are as follows.</span></span>


|                | <span data-ttu-id="5d17c-110">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-110">PES output</span></span> | <span data-ttu-id="5d17c-111">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-111">Payload output</span></span>
|------------------|------------------------------------------|--------------------------------|
| <span data-ttu-id="5d17c-112">**Haupttyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-112">**Major type**</span></span>       | <span data-ttu-id="5d17c-113">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="5d17c-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="5d17c-114">**\_MEDIATYPE-Video**</span><span class="sxs-lookup"><span data-stu-id="5d17c-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="5d17c-115">**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-115">**Subtype**</span></span>          | <span data-ttu-id="5d17c-116">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="5d17c-117">**MEDIASUBTYPE \_ MPEG2 \_ VIDEO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="5d17c-118">**Formattyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-118">**Format type**</span></span>      | <span data-ttu-id="5d17c-119">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="5d17c-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="5d17c-120">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="5d17c-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="5d17c-121">**Formatstruktur**</span><span class="sxs-lookup"><span data-stu-id="5d17c-121">**Format structure**</span></span> | [<span data-ttu-id="5d17c-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="5d17c-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="5d17c-124">AC-3-Audio</span><span class="sxs-lookup"><span data-stu-id="5d17c-124">AC-3 Audio</span></span>

<span data-ttu-id="5d17c-125">Für AC-3-Audio sind die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5d17c-125">For AC-3 audio, the media types are as follows.</span></span>

| | <span data-ttu-id="5d17c-126">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-126">PES output</span></span> | <span data-ttu-id="5d17c-127">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-127">Payload output</span></span> |
|------------------|--------------------------------------|------------------------------|
| <span data-ttu-id="5d17c-128">**Haupttyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-128">**Major type**</span></span>       | <span data-ttu-id="5d17c-129">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="5d17c-129">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="5d17c-130">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="5d17c-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="5d17c-131">**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-131">**Subtype**</span></span>          | <span data-ttu-id="5d17c-132">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="5d17c-132">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>             | <span data-ttu-id="5d17c-133">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="5d17c-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="5d17c-134">**Formattyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-134">**Format type**</span></span>      | <span data-ttu-id="5d17c-135">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="5d17c-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="5d17c-136">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5d17c-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="5d17c-137">**Formatstruktur**</span><span class="sxs-lookup"><span data-stu-id="5d17c-137">**Format structure**</span></span> | <span data-ttu-id="5d17c-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d17c-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="5d17c-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5d17c-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="5d17c-140">Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für AC-3 ist derzeit **WAVE FORMAT \_ \_ UNKNOWN**, aber dies kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="5d17c-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="5d17c-141">MPEG-2-Audio</span><span class="sxs-lookup"><span data-stu-id="5d17c-141">MPEG-2 Audio</span></span>

<span data-ttu-id="5d17c-142">Für MPEG-2-Audio sind die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5d17c-142">For MPEG-2 audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="5d17c-143">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-143">PES output</span></span> | <span data-ttu-id="5d17c-144">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-144">Payload output</span></span> |
|------------------|-------------------------------|--------------------------------|
| <span data-ttu-id="5d17c-145">**Haupttyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-145">**Major type**</span></span>       | <span data-ttu-id="5d17c-146">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="5d17c-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="5d17c-147">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="5d17c-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="5d17c-148">**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-148">**Subtype**</span></span>          | <span data-ttu-id="5d17c-149">**MEDIASUBTYE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="5d17c-150">**MEDIASUBTYPE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="5d17c-151">**Formattyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-151">**Format type**</span></span>      | <span data-ttu-id="5d17c-152">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5d17c-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="5d17c-153">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5d17c-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="5d17c-154">**Formatstruktur**</span><span class="sxs-lookup"><span data-stu-id="5d17c-154">**Format structure**</span></span> | <span data-ttu-id="5d17c-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5d17c-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="5d17c-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5d17c-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="5d17c-157">Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für MPEG-2 Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN**, aber dies kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="5d17c-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="5d17c-158">Der MPEG-2-Splitter geht davon aus, dass Streams D0 über DF für den Multichannel-Erweiterungsstream verwendet werden, ebenso wie für DVD MPEG-2-Audio.</span><span class="sxs-lookup"><span data-stu-id="5d17c-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="5d17c-159">Daher leitet der Splitter immer dann, wenn Stream C *x* ausgewählt wird, die Pakete für Stream D *x* weiter.</span><span class="sxs-lookup"><span data-stu-id="5d17c-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="5d17c-160">LPCM-Audio</span><span class="sxs-lookup"><span data-stu-id="5d17c-160">LPCM Audio</span></span>

<span data-ttu-id="5d17c-161">Für LPCM-Audio sind die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="5d17c-161">For LPCM audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="5d17c-162">PES-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-162">PES output</span></span> | <span data-ttu-id="5d17c-163">Nutzlastausgabe</span><span class="sxs-lookup"><span data-stu-id="5d17c-163">Payload output</span></span> |
|------------------|------------------------------------|------------------------------------|
| <span data-ttu-id="5d17c-164">**Haupttyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-164">**Major type**</span></span>       | <span data-ttu-id="5d17c-165">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="5d17c-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="5d17c-166">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="5d17c-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="5d17c-167">**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-167">**Subtype**</span></span>          | <span data-ttu-id="5d17c-168">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="5d17c-169">**MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="5d17c-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="5d17c-170">**Formattyp**</span><span class="sxs-lookup"><span data-stu-id="5d17c-170">**Format type**</span></span>      | <span data-ttu-id="5d17c-171">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5d17c-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="5d17c-172">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5d17c-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="5d17c-173">**Formatstruktur**</span><span class="sxs-lookup"><span data-stu-id="5d17c-173">**Format structure**</span></span> | <span data-ttu-id="5d17c-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5d17c-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="5d17c-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5d17c-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="5d17c-176">Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für LPCM-Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN,** aber dies kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="5d17c-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d17c-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d17c-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d17c-178">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="5d17c-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
