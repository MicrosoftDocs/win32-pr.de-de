---
description: MPEG-2-Splitter Medientypen
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2-Splitter Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355716"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="e18f3-103">MPEG-2-Splitter Medientypen</span><span class="sxs-lookup"><span data-stu-id="e18f3-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="e18f3-104">Der [MPEG-2-Splitter](mpeg-2-splitter.md) Filter unterstützt derzeit Audiodateien und Videos.</span><span class="sxs-lookup"><span data-stu-id="e18f3-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="e18f3-105">Dolby AC-3 wird als ein untergeordneter Stream unterstützt, wie von DVD definiert.</span><span class="sxs-lookup"><span data-stu-id="e18f3-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="e18f3-106">Der Filter unterstützt auch MPEG-2-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="e18f3-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="e18f3-107">Die Medientypen hängen davon ab, ob der MPEG-2-Splitter PE-Pakete oder PE-Nutzlasten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e18f3-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="e18f3-108">Video</span><span class="sxs-lookup"><span data-stu-id="e18f3-108">Video</span></span>

<span data-ttu-id="e18f3-109">Bei MPEG-2-Videos lauten die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e18f3-109">For MPEG-2 video, the media types are as follows.</span></span>



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="e18f3-110">Ausgabe von PES</span><span class="sxs-lookup"><span data-stu-id="e18f3-110">PES output</span></span>                               | <span data-ttu-id="e18f3-111">Nutz Last Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e18f3-111">Payload output</span></span>                 |
| <span data-ttu-id="e18f3-112">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-112">Major Type</span></span>       | <span data-ttu-id="e18f3-113">**MediaType \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="e18f3-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="e18f3-114">**MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="e18f3-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="e18f3-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="e18f3-115">Subtype</span></span>          | <span data-ttu-id="e18f3-116">**Video zu mediasubtype \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="e18f3-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="e18f3-117">**Video zu mediasubtype \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="e18f3-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="e18f3-118">Formattyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-118">Format Type</span></span>      | <span data-ttu-id="e18f3-119">**MPEG2Video formatieren \_**</span><span class="sxs-lookup"><span data-stu-id="e18f3-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="e18f3-120">**MPEG2Video formatieren \_**</span><span class="sxs-lookup"><span data-stu-id="e18f3-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="e18f3-121">Format Struktur</span><span class="sxs-lookup"><span data-stu-id="e18f3-121">Format Structure</span></span> | [<span data-ttu-id="e18f3-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="e18f3-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="e18f3-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="e18f3-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="e18f3-124">AC-3-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="e18f3-124">AC-3 Audio</span></span>

<span data-ttu-id="e18f3-125">Bei AC-3-Audiodaten lauten die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e18f3-125">For AC-3 audio, the media types are as follows.</span></span>



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="e18f3-126">Ausgabe von PES</span><span class="sxs-lookup"><span data-stu-id="e18f3-126">PES output</span></span>                           | <span data-ttu-id="e18f3-127">Nutz Last Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e18f3-127">Payload output</span></span>               |
| <span data-ttu-id="e18f3-128">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-128">Major Type</span></span>       | <span data-ttu-id="e18f3-129">MediaType \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e18f3-129">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="e18f3-130">**MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="e18f3-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="e18f3-131">Subtype</span><span class="sxs-lookup"><span data-stu-id="e18f3-131">Subtype</span></span>          | <span data-ttu-id="e18f3-132">Mediasubtype \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="e18f3-132">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="e18f3-133">**Mediasubtype \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="e18f3-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="e18f3-134">Formattyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-134">Format Type</span></span>      | <span data-ttu-id="e18f3-135">Formatieren von \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="e18f3-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="e18f3-136">**Formatieren von \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e18f3-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="e18f3-137">Format Struktur</span><span class="sxs-lookup"><span data-stu-id="e18f3-137">Format Structure</span></span> | <span data-ttu-id="e18f3-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e18f3-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="e18f3-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e18f3-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="e18f3-140">Das **wformattag** -Element der **WaveFormatEx** -Struktur für AC-3 ist zurzeit **\_ \_ unbekannt**. Dies kann sich jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="e18f3-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="e18f3-141">MPEG-2-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="e18f3-141">MPEG-2 Audio</span></span>

<span data-ttu-id="e18f3-142">Bei MPEG-2-Audiodaten lauten die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e18f3-142">For MPEG-2 audio, the media types are as follows.</span></span>



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="e18f3-143">Ausgabe von PES</span><span class="sxs-lookup"><span data-stu-id="e18f3-143">PES output</span></span>                    | <span data-ttu-id="e18f3-144">Nutz Last Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e18f3-144">Payload output</span></span>                 |
| <span data-ttu-id="e18f3-145">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-145">Major Type</span></span>       | <span data-ttu-id="e18f3-146">**MediaType \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="e18f3-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="e18f3-147">**MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="e18f3-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="e18f3-148">Subtype</span><span class="sxs-lookup"><span data-stu-id="e18f3-148">Subtype</span></span>          | <span data-ttu-id="e18f3-149">**Mediasubtye \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="e18f3-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="e18f3-150">**Mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="e18f3-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="e18f3-151">Formattyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-151">Format Type</span></span>      | <span data-ttu-id="e18f3-152">**Formatieren von \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e18f3-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="e18f3-153">**Formatieren von \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e18f3-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="e18f3-154">Format Struktur</span><span class="sxs-lookup"><span data-stu-id="e18f3-154">Format Structure</span></span> | <span data-ttu-id="e18f3-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e18f3-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="e18f3-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e18f3-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="e18f3-157">Das **wformattag** -Element der **WaveFormatEx** -Struktur für MPEG-2-Audiodaten ist zurzeit **\_ \_ unbekannt**, dies kann sich jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="e18f3-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="e18f3-158">Der MPEG-2-Splitter geht davon aus, dass Datenströme D0 bis DF für den Multichannel-Erweiterungs Datenstrom verwendet werden, wie Sie für die DVD MPEG-2-Audiodaten verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e18f3-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="e18f3-159">Daher leitet der Splitter, wenn Stream C *x* ausgewählt ist, auch die Pakete für Stream D *x* weiter.</span><span class="sxs-lookup"><span data-stu-id="e18f3-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="e18f3-160">LPCM-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="e18f3-160">LPCM Audio</span></span>

<span data-ttu-id="e18f3-161">Bei LPCM-Audiodaten lauten die Medientypen wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e18f3-161">For LPCM audio, the media types are as follows.</span></span>



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="e18f3-162">Ausgabe von PES</span><span class="sxs-lookup"><span data-stu-id="e18f3-162">PES output</span></span>                         | <span data-ttu-id="e18f3-163">Nutz Last Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e18f3-163">Payload output</span></span>                     |
| <span data-ttu-id="e18f3-164">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-164">Major Type</span></span>       | <span data-ttu-id="e18f3-165">**MediaType \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="e18f3-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="e18f3-166">**MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="e18f3-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="e18f3-167">Subtype</span><span class="sxs-lookup"><span data-stu-id="e18f3-167">Subtype</span></span>          | <span data-ttu-id="e18f3-168">**mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="e18f3-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="e18f3-169">**mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="e18f3-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="e18f3-170">Formattyp</span><span class="sxs-lookup"><span data-stu-id="e18f3-170">Format Type</span></span>      | <span data-ttu-id="e18f3-171">**Formatieren von \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e18f3-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="e18f3-172">**Formatieren von \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e18f3-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="e18f3-173">Format Struktur</span><span class="sxs-lookup"><span data-stu-id="e18f3-173">Format Structure</span></span> | <span data-ttu-id="e18f3-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e18f3-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="e18f3-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e18f3-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="e18f3-176">Das **wformattag** -Element der **WaveFormatEx** -Struktur für LPCM-Audiodaten ist zurzeit **\_ \_ unbekannt**, dies kann sich jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="e18f3-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e18f3-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e18f3-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e18f3-178">MPEG-2-Medientypen</span><span class="sxs-lookup"><span data-stu-id="e18f3-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
