---
description: DV Muxer-Filter
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV Muxer-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908598"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="d98d7-103">DV Muxer-Filter</span><span class="sxs-lookup"><span data-stu-id="d98d7-103">DV Muxer Filter</span></span>

<span data-ttu-id="d98d7-104">Dieser Filter kombiniert ein digitales Video (DV) – codierter Videodatenstrom mit einem oder zwei Audiostreams, um einen überlappende DV-Datenstrom zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="d98d7-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="d98d7-105">Um den Stream in eine AVI-Datei zu schreiben, verbinden Sie diesen Filter mit dem [AVI Mux-Filter](avi-mux-filter.md) und den *AVI Mux* mit dem [File Writer-Filter.](file-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="d98d7-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="d98d7-106">Weitere Informationen finden Sie unter [Digitales Video in DirectShow.](digital-video-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="d98d7-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



| <span data-ttu-id="d98d7-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d98d7-107">Label</span></span> | <span data-ttu-id="d98d7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d98d7-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98d7-109">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d98d7-109">Filter Interfaces</span></span>                        | <span data-ttu-id="d98d7-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="d98d7-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="d98d7-111">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="d98d7-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="d98d7-112">**Video**: MEDIATYPE \_ Video, MEDIASUBTYPE \_ dvsd, FORMAT \_ VideoInfo **Audio**: MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="d98d7-112">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="d98d7-113">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d98d7-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d98d7-114">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d98d7-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="d98d7-115">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="d98d7-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="d98d7-116">MEDIATYPE \_ Interleaved, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="d98d7-116">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="d98d7-117">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d98d7-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d98d7-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d98d7-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="d98d7-119">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="d98d7-119">Filter CLSID</span></span>                             | <span data-ttu-id="d98d7-120">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="d98d7-120">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="d98d7-121">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="d98d7-121">Property Page CLSID</span></span>                      | <span data-ttu-id="d98d7-122">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="d98d7-122">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="d98d7-123">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="d98d7-123">Executable</span></span>                               | <span data-ttu-id="d98d7-124">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="d98d7-124">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="d98d7-125">Verdienst</span><span class="sxs-lookup"><span data-stu-id="d98d7-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="d98d7-126">WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH</span><span class="sxs-lookup"><span data-stu-id="d98d7-126">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="d98d7-127">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="d98d7-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d98d7-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="d98d7-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d98d7-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d98d7-129">Remarks</span></span>

<span data-ttu-id="d98d7-130">Der DV Muxer kann zwei Audioeingabepins erstellen.</span><span class="sxs-lookup"><span data-stu-id="d98d7-130">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="d98d7-131">Sie unterstützt die in der folgenden Tabelle gezeigten Audioformate.</span><span class="sxs-lookup"><span data-stu-id="d98d7-131">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="d98d7-132">Audiopin 1</span><span class="sxs-lookup"><span data-stu-id="d98d7-132">Audio Pin 1</span></span>

<span data-ttu-id="d98d7-133">Audiopin 2</span><span class="sxs-lookup"><span data-stu-id="d98d7-133">Audio Pin 2</span></span>

<span data-ttu-id="d98d7-134">Ausgabeformat</span><span class="sxs-lookup"><span data-stu-id="d98d7-134">Output Format</span></span>

<span data-ttu-id="d98d7-135">Abtastrate (kHz)</span><span class="sxs-lookup"><span data-stu-id="d98d7-135">Sample Rate (kHz)</span></span>

<span data-ttu-id="d98d7-136">Bits/Beispiel</span><span class="sxs-lookup"><span data-stu-id="d98d7-136">Bits/Sample</span></span>

<span data-ttu-id="d98d7-137">Channels</span><span class="sxs-lookup"><span data-stu-id="d98d7-137">Channels</span></span>

<span data-ttu-id="d98d7-138">Samplingrate</span><span class="sxs-lookup"><span data-stu-id="d98d7-138">Sample Rate</span></span>

<span data-ttu-id="d98d7-139">Bits/Beispiel</span><span class="sxs-lookup"><span data-stu-id="d98d7-139">Bits/Sample</span></span>

<span data-ttu-id="d98d7-140">Channels</span><span class="sxs-lookup"><span data-stu-id="d98d7-140">Channels</span></span>

<span data-ttu-id="d98d7-141">32</span><span class="sxs-lookup"><span data-stu-id="d98d7-141">32</span></span>

<span data-ttu-id="d98d7-142">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-142">16</span></span>

<span data-ttu-id="d98d7-143">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-143">Mono</span></span>

<span data-ttu-id="d98d7-144">Unverbunden</span><span class="sxs-lookup"><span data-stu-id="d98d7-144">Unconnected</span></span>

<span data-ttu-id="d98d7-145">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-145">SD 2 Channel</span></span>

<span data-ttu-id="d98d7-146">32</span><span class="sxs-lookup"><span data-stu-id="d98d7-146">32</span></span>

<span data-ttu-id="d98d7-147">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-147">16</span></span>

<span data-ttu-id="d98d7-148">Stereo</span><span class="sxs-lookup"><span data-stu-id="d98d7-148">Stereo</span></span>

<span data-ttu-id="d98d7-149">Unverbunden</span><span class="sxs-lookup"><span data-stu-id="d98d7-149">Unconnected</span></span>

<span data-ttu-id="d98d7-150">SD 4-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-150">SD 4 Channel</span></span>

<span data-ttu-id="d98d7-151">44.1 oder 48</span><span class="sxs-lookup"><span data-stu-id="d98d7-151">44.1 or 48</span></span>

<span data-ttu-id="d98d7-152">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-152">16</span></span>

<span data-ttu-id="d98d7-153">Stereo oder Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-153">Stereo or Mono</span></span>

<span data-ttu-id="d98d7-154">Unverbunden</span><span class="sxs-lookup"><span data-stu-id="d98d7-154">Unconnected</span></span>

<span data-ttu-id="d98d7-155">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-155">SD 2 Channel</span></span>

<span data-ttu-id="d98d7-156">Unverbunden</span><span class="sxs-lookup"><span data-stu-id="d98d7-156">Unconnected</span></span>

<span data-ttu-id="d98d7-157">32</span><span class="sxs-lookup"><span data-stu-id="d98d7-157">32</span></span>

<span data-ttu-id="d98d7-158">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-158">16</span></span>

<span data-ttu-id="d98d7-159">Stereo oder Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-159">Stereo or Mono</span></span>

<span data-ttu-id="d98d7-160">Unzulässig</span><span class="sxs-lookup"><span data-stu-id="d98d7-160">Disallowed</span></span>

<span data-ttu-id="d98d7-161">Unverbunden</span><span class="sxs-lookup"><span data-stu-id="d98d7-161">Unconnected</span></span>

<span data-ttu-id="d98d7-162">44.1 oder 48</span><span class="sxs-lookup"><span data-stu-id="d98d7-162">44.1 or 48</span></span>

<span data-ttu-id="d98d7-163">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-163">16</span></span>

<span data-ttu-id="d98d7-164">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-164">Mono</span></span>

<span data-ttu-id="d98d7-165">Unzulässig</span><span class="sxs-lookup"><span data-stu-id="d98d7-165">Disallowed</span></span>

<span data-ttu-id="d98d7-166">Unverbunden</span><span class="sxs-lookup"><span data-stu-id="d98d7-166">Unconnected</span></span>

<span data-ttu-id="d98d7-167">44.1 oder 48</span><span class="sxs-lookup"><span data-stu-id="d98d7-167">44.1 or 48</span></span>

<span data-ttu-id="d98d7-168">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-168">16</span></span>

<span data-ttu-id="d98d7-169">Stereo</span><span class="sxs-lookup"><span data-stu-id="d98d7-169">Stereo</span></span>

<span data-ttu-id="d98d7-170">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-170">SD 2 Channel</span></span>

<span data-ttu-id="d98d7-171">32</span><span class="sxs-lookup"><span data-stu-id="d98d7-171">32</span></span>

<span data-ttu-id="d98d7-172">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-172">16</span></span>

<span data-ttu-id="d98d7-173">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-173">Mono</span></span>

<span data-ttu-id="d98d7-174">32</span><span class="sxs-lookup"><span data-stu-id="d98d7-174">32</span></span>

<span data-ttu-id="d98d7-175">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-175">16</span></span>

<span data-ttu-id="d98d7-176">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-176">Mono</span></span>

<span data-ttu-id="d98d7-177">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-177">SD 2 Channel</span></span>

<span data-ttu-id="d98d7-178">32</span><span class="sxs-lookup"><span data-stu-id="d98d7-178">32</span></span>

<span data-ttu-id="d98d7-179">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-179">16</span></span>

<span data-ttu-id="d98d7-180">Stereo oder Mono\*</span><span class="sxs-lookup"><span data-stu-id="d98d7-180">Stereo or Mono\*</span></span>

<span data-ttu-id="d98d7-181">32</span><span class="sxs-lookup"><span data-stu-id="d98d7-181">32</span></span>

<span data-ttu-id="d98d7-182">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-182">16</span></span>

<span data-ttu-id="d98d7-183">Stereo oder Mono\*</span><span class="sxs-lookup"><span data-stu-id="d98d7-183">Stereo or Mono\*</span></span>

<span data-ttu-id="d98d7-184">SD 4-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-184">SD 4 Channel</span></span>

<span data-ttu-id="d98d7-185">44.1</span><span class="sxs-lookup"><span data-stu-id="d98d7-185">44.1</span></span>

<span data-ttu-id="d98d7-186">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-186">16</span></span>

<span data-ttu-id="d98d7-187">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-187">Mono</span></span>

<span data-ttu-id="d98d7-188">44.1</span><span class="sxs-lookup"><span data-stu-id="d98d7-188">44.1</span></span>

<span data-ttu-id="d98d7-189">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-189">16</span></span>

<span data-ttu-id="d98d7-190">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-190">Mono</span></span>

<span data-ttu-id="d98d7-191">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-191">SD 2 Channel</span></span>

<span data-ttu-id="d98d7-192">48</span><span class="sxs-lookup"><span data-stu-id="d98d7-192">48</span></span>

<span data-ttu-id="d98d7-193">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-193">16</span></span>

<span data-ttu-id="d98d7-194">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-194">Mono</span></span>

<span data-ttu-id="d98d7-195">48</span><span class="sxs-lookup"><span data-stu-id="d98d7-195">48</span></span>

<span data-ttu-id="d98d7-196">16</span><span class="sxs-lookup"><span data-stu-id="d98d7-196">16</span></span>

<span data-ttu-id="d98d7-197">Mono</span><span class="sxs-lookup"><span data-stu-id="d98d7-197">Mono</span></span>

<span data-ttu-id="d98d7-198">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="d98d7-198">SD 2 Channel</span></span>

<span data-ttu-id="d98d7-199">\* Wenn mindestens ein Eingabepin stereo ist.</span><span class="sxs-lookup"><span data-stu-id="d98d7-199">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="d98d7-200">Für diese Tabelle wird Audiopin 1 als erster Eingabepin definiert, der mit einer Audioquelle verbunden ist, und Audiopin 2 ist als zweiter Eingabepin definiert, der mit einer Audioquelle verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d98d7-200">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="d98d7-201">Sobald eine Audiostecknadel verbunden ist, bleibt dieses Nummerierungsschema wirksam, es sei denn, beide Audiopins werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="d98d7-201">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="d98d7-202">Wenn Sie beispielsweise beide Audiopins verbinden und dann audio pin 1 trennen, wird der verbleibende Pin weiterhin als Pin 2 betrachtet.</span><span class="sxs-lookup"><span data-stu-id="d98d7-202">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="d98d7-203">Audiodaten, die an Pin 1 übermittelt werden, werden im ersten Audioblock der DV-Frames (CH1) aufgezeichnet, und Audiodaten, die an Pin 2 übermittelt werden, werden im zweiten Audioblock (CH2) aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d98d7-203">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="d98d7-204">Ausnahme: Wenn der Filter über eine einzelne Stereoeingabe mit 44,1 kHz oder 48 kHz verfügt, wird der linke Audiokanal im ersten Audioblock aufgezeichnet, und der rechte Audiokanal wird im zweiten Audioblock aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d98d7-204">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="d98d7-205">Für SD 4-Kanal-Ausgabe: Wenn die Eingabe Stereo ist, wird die linke Spur in CHa oder CHc aufgezeichnet, und die rechte Spur wird in CHb oder CHd aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d98d7-205">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="d98d7-206">Wenn die Eingabe mono ist, wird die Audiodatei in CHa oder CHc aufgezeichnet, und CHb und CHd sind im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="d98d7-206">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="d98d7-207">Durch das Verbinden und Trennen von Audiopin 1 ist es möglich, ein nicht zu verwendendes Format zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="d98d7-207">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="d98d7-208">In diesem Fall gibt die [**IMediaFilter::P ause-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) des Filters VFW \_ E NOT CONNECTED \_ \_ zurück.</span><span class="sxs-lookup"><span data-stu-id="d98d7-208">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="d98d7-209">Diese Einschränkung verhindert eine Situation, in der der erste Audioblock über keine Audiodaten verfügt, der zweite Audioblock jedoch über Audiodaten verfügt.</span><span class="sxs-lookup"><span data-stu-id="d98d7-209">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="d98d7-210">Der zweite Block sollte nur Audiodaten haben, wenn der erste Block auch Audio enthält.</span><span class="sxs-lookup"><span data-stu-id="d98d7-210">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="d98d7-211">Der DV Muxer lässt keine Audioeingaben mit unterschiedlichen Samplingraten zu.</span><span class="sxs-lookup"><span data-stu-id="d98d7-211">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="d98d7-212">Graph-Building-Methoden wie [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) fügen jedoch in der Regel den [ACM-Wrapperfilter](acm-wrapper-filter.md) hinzu, der den zweiten Audiostream so konvertiert, dass er mit der Samplingrate des ersten Streams übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="d98d7-212">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="d98d7-213">Wenn die Audioeingabe 48 kHz oder 32 kHz beträgt, wird die Audioausgabe gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d98d7-213">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="d98d7-214">(Es ist nicht möglich, Audio mit 44,1 kHz zu sperren.)</span><span class="sxs-lookup"><span data-stu-id="d98d7-214">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="d98d7-215">Wenn keine Audiopins verbunden sind, enthält die Ausgabe die Audiodaten aus den eingehenden DV-Frames.</span><span class="sxs-lookup"><span data-stu-id="d98d7-215">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="d98d7-216">Dies können Stille oder gültige Audiodaten sein.</span><span class="sxs-lookup"><span data-stu-id="d98d7-216">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d98d7-217">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d98d7-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d98d7-218">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="d98d7-218">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d98d7-219">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d98d7-219">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



