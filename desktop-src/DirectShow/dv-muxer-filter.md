---
description: DV-Muxer-Filter
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV-Muxer-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747400"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="23e1b-103">DV-Muxer-Filter</span><span class="sxs-lookup"><span data-stu-id="23e1b-103">DV Muxer Filter</span></span>

<span data-ttu-id="23e1b-104">Dieser Filter kombiniert einen –-codierten Videostream mit einem oder zwei Audiodatenströmen, um einen verschachtelten DV-Stream zu liefern.</span><span class="sxs-lookup"><span data-stu-id="23e1b-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="23e1b-105">Um den Stream in eine AVI-Datei zu schreiben, verbinden Sie diesen Filter mit dem [AVI MUX](avi-mux-filter.md) -Filter, und verbinden Sie die *AVI-MUX* mit dem [dateiwriter](file-writer-filter.md) -Filter.</span><span class="sxs-lookup"><span data-stu-id="23e1b-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="23e1b-106">Weitere Informationen finden Sie unter [digitales Video in DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="23e1b-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e1b-107">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="23e1b-107">Filter Interfaces</span></span>                        | <span data-ttu-id="23e1b-108">[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="23e1b-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="23e1b-109">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="23e1b-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="23e1b-110">**Video**: MediaType \_ Video, mediasubtype \_ DVSD, Format \_ videoinfo **-Audiodatei**: MediaType \_ -Audiodatei, mediasubtype \_ PCM, Format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="23e1b-110">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="23e1b-111">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="23e1b-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="23e1b-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="23e1b-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="23e1b-113">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="23e1b-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="23e1b-114">MediaType \_ interleaved, mediasubtype \_ DVSD, Format \_ dvinfo</span><span class="sxs-lookup"><span data-stu-id="23e1b-114">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="23e1b-115">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="23e1b-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="23e1b-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="23e1b-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="23e1b-117">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="23e1b-117">Filter CLSID</span></span>                             | <span data-ttu-id="23e1b-118">CLSID- \_ dvmux</span><span class="sxs-lookup"><span data-stu-id="23e1b-118">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="23e1b-119">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="23e1b-119">Property Page CLSID</span></span>                      | <span data-ttu-id="23e1b-120">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="23e1b-120">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="23e1b-121">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="23e1b-121">Executable</span></span>                               | <span data-ttu-id="23e1b-122">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="23e1b-122">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="23e1b-123">Verdienst</span><span class="sxs-lookup"><span data-stu-id="23e1b-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="23e1b-124">nicht \_ wahrscheinlich</span><span class="sxs-lookup"><span data-stu-id="23e1b-124">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="23e1b-125">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="23e1b-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="23e1b-126">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="23e1b-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="23e1b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23e1b-127">Remarks</span></span>

<span data-ttu-id="23e1b-128">Der DV-Muxer kann zwei audioeingabepins erstellen.</span><span class="sxs-lookup"><span data-stu-id="23e1b-128">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="23e1b-129">Die in der folgenden Tabelle gezeigten Audioformate werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23e1b-129">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="23e1b-130">Audiopin 1</span><span class="sxs-lookup"><span data-stu-id="23e1b-130">Audio Pin 1</span></span>

<span data-ttu-id="23e1b-131">Audiopin 2</span><span class="sxs-lookup"><span data-stu-id="23e1b-131">Audio Pin 2</span></span>

<span data-ttu-id="23e1b-132">Ausgabeformat</span><span class="sxs-lookup"><span data-stu-id="23e1b-132">Output Format</span></span>

<span data-ttu-id="23e1b-133">Stichproben Rate (kHz)</span><span class="sxs-lookup"><span data-stu-id="23e1b-133">Sample Rate (kHz)</span></span>

<span data-ttu-id="23e1b-134">Bits/Beispiel</span><span class="sxs-lookup"><span data-stu-id="23e1b-134">Bits/Sample</span></span>

<span data-ttu-id="23e1b-135">Channels</span><span class="sxs-lookup"><span data-stu-id="23e1b-135">Channels</span></span>

<span data-ttu-id="23e1b-136">Samplingrate</span><span class="sxs-lookup"><span data-stu-id="23e1b-136">Sample Rate</span></span>

<span data-ttu-id="23e1b-137">Bits/Beispiel</span><span class="sxs-lookup"><span data-stu-id="23e1b-137">Bits/Sample</span></span>

<span data-ttu-id="23e1b-138">Channels</span><span class="sxs-lookup"><span data-stu-id="23e1b-138">Channels</span></span>

<span data-ttu-id="23e1b-139">32</span><span class="sxs-lookup"><span data-stu-id="23e1b-139">32</span></span>

<span data-ttu-id="23e1b-140">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-140">16</span></span>

<span data-ttu-id="23e1b-141">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-141">Mono</span></span>

<span data-ttu-id="23e1b-142">Nicht verbundenen</span><span class="sxs-lookup"><span data-stu-id="23e1b-142">Unconnected</span></span>

<span data-ttu-id="23e1b-143">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-143">SD 2 Channel</span></span>

<span data-ttu-id="23e1b-144">32</span><span class="sxs-lookup"><span data-stu-id="23e1b-144">32</span></span>

<span data-ttu-id="23e1b-145">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-145">16</span></span>

<span data-ttu-id="23e1b-146">Stereo</span><span class="sxs-lookup"><span data-stu-id="23e1b-146">Stereo</span></span>

<span data-ttu-id="23e1b-147">Nicht verbundenen</span><span class="sxs-lookup"><span data-stu-id="23e1b-147">Unconnected</span></span>

<span data-ttu-id="23e1b-148">SD 4-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-148">SD 4 Channel</span></span>

<span data-ttu-id="23e1b-149">44,1 oder 48</span><span class="sxs-lookup"><span data-stu-id="23e1b-149">44.1 or 48</span></span>

<span data-ttu-id="23e1b-150">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-150">16</span></span>

<span data-ttu-id="23e1b-151">Stereo oder Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-151">Stereo or Mono</span></span>

<span data-ttu-id="23e1b-152">Nicht verbundenen</span><span class="sxs-lookup"><span data-stu-id="23e1b-152">Unconnected</span></span>

<span data-ttu-id="23e1b-153">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-153">SD 2 Channel</span></span>

<span data-ttu-id="23e1b-154">Nicht verbundenen</span><span class="sxs-lookup"><span data-stu-id="23e1b-154">Unconnected</span></span>

<span data-ttu-id="23e1b-155">32</span><span class="sxs-lookup"><span data-stu-id="23e1b-155">32</span></span>

<span data-ttu-id="23e1b-156">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-156">16</span></span>

<span data-ttu-id="23e1b-157">Stereo oder Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-157">Stereo or Mono</span></span>

<span data-ttu-id="23e1b-158">Unzulässig</span><span class="sxs-lookup"><span data-stu-id="23e1b-158">Disallowed</span></span>

<span data-ttu-id="23e1b-159">Nicht verbundenen</span><span class="sxs-lookup"><span data-stu-id="23e1b-159">Unconnected</span></span>

<span data-ttu-id="23e1b-160">44,1 oder 48</span><span class="sxs-lookup"><span data-stu-id="23e1b-160">44.1 or 48</span></span>

<span data-ttu-id="23e1b-161">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-161">16</span></span>

<span data-ttu-id="23e1b-162">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-162">Mono</span></span>

<span data-ttu-id="23e1b-163">Unzulässig</span><span class="sxs-lookup"><span data-stu-id="23e1b-163">Disallowed</span></span>

<span data-ttu-id="23e1b-164">Nicht verbundenen</span><span class="sxs-lookup"><span data-stu-id="23e1b-164">Unconnected</span></span>

<span data-ttu-id="23e1b-165">44,1 oder 48</span><span class="sxs-lookup"><span data-stu-id="23e1b-165">44.1 or 48</span></span>

<span data-ttu-id="23e1b-166">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-166">16</span></span>

<span data-ttu-id="23e1b-167">Stereo</span><span class="sxs-lookup"><span data-stu-id="23e1b-167">Stereo</span></span>

<span data-ttu-id="23e1b-168">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-168">SD 2 Channel</span></span>

<span data-ttu-id="23e1b-169">32</span><span class="sxs-lookup"><span data-stu-id="23e1b-169">32</span></span>

<span data-ttu-id="23e1b-170">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-170">16</span></span>

<span data-ttu-id="23e1b-171">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-171">Mono</span></span>

<span data-ttu-id="23e1b-172">32</span><span class="sxs-lookup"><span data-stu-id="23e1b-172">32</span></span>

<span data-ttu-id="23e1b-173">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-173">16</span></span>

<span data-ttu-id="23e1b-174">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-174">Mono</span></span>

<span data-ttu-id="23e1b-175">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-175">SD 2 Channel</span></span>

<span data-ttu-id="23e1b-176">32</span><span class="sxs-lookup"><span data-stu-id="23e1b-176">32</span></span>

<span data-ttu-id="23e1b-177">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-177">16</span></span>

<span data-ttu-id="23e1b-178">Stereo oder Mono\*</span><span class="sxs-lookup"><span data-stu-id="23e1b-178">Stereo or Mono\*</span></span>

<span data-ttu-id="23e1b-179">32</span><span class="sxs-lookup"><span data-stu-id="23e1b-179">32</span></span>

<span data-ttu-id="23e1b-180">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-180">16</span></span>

<span data-ttu-id="23e1b-181">Stereo oder Mono\*</span><span class="sxs-lookup"><span data-stu-id="23e1b-181">Stereo or Mono\*</span></span>

<span data-ttu-id="23e1b-182">SD 4-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-182">SD 4 Channel</span></span>

<span data-ttu-id="23e1b-183">44,1</span><span class="sxs-lookup"><span data-stu-id="23e1b-183">44.1</span></span>

<span data-ttu-id="23e1b-184">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-184">16</span></span>

<span data-ttu-id="23e1b-185">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-185">Mono</span></span>

<span data-ttu-id="23e1b-186">44,1</span><span class="sxs-lookup"><span data-stu-id="23e1b-186">44.1</span></span>

<span data-ttu-id="23e1b-187">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-187">16</span></span>

<span data-ttu-id="23e1b-188">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-188">Mono</span></span>

<span data-ttu-id="23e1b-189">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-189">SD 2 Channel</span></span>

<span data-ttu-id="23e1b-190">48</span><span class="sxs-lookup"><span data-stu-id="23e1b-190">48</span></span>

<span data-ttu-id="23e1b-191">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-191">16</span></span>

<span data-ttu-id="23e1b-192">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-192">Mono</span></span>

<span data-ttu-id="23e1b-193">48</span><span class="sxs-lookup"><span data-stu-id="23e1b-193">48</span></span>

<span data-ttu-id="23e1b-194">16</span><span class="sxs-lookup"><span data-stu-id="23e1b-194">16</span></span>

<span data-ttu-id="23e1b-195">Mono</span><span class="sxs-lookup"><span data-stu-id="23e1b-195">Mono</span></span>

<span data-ttu-id="23e1b-196">SD 2-Kanal</span><span class="sxs-lookup"><span data-stu-id="23e1b-196">SD 2 Channel</span></span>

<span data-ttu-id="23e1b-197">\* Wenn mindestens eine Eingabe-PIN Stereo ist.</span><span class="sxs-lookup"><span data-stu-id="23e1b-197">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="23e1b-198">Für diese Tabelle wird die audiopin 1 als erste Eingabe-PIN definiert, die mit einer Audioquelle verbunden ist, und audiopin 2 wird als zweite Eingabe-PIN definiert, die mit einer Audioquelle verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="23e1b-198">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="23e1b-199">Sobald eine audiopin verbunden ist, bleibt dieses Nummerierungschema wirksam, es sei denn, beide audiopins werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="23e1b-199">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="23e1b-200">Wenn Sie z. b. beide audiopins verbinden und dann die audiopin 1 trennen, wird die verbleibende Pin weiterhin als Pin 2 angesehen.</span><span class="sxs-lookup"><span data-stu-id="23e1b-200">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="23e1b-201">Audioinformationen für Pin 1 werden im ersten Audioblock der DV-Frames (CH1) aufgezeichnet, und für Pin 2 bereitgestellte Audiodaten werden im zweiten Audioblock (CH2) aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="23e1b-201">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="23e1b-202">Ausnahme: Wenn der Filter eine einzelne Stereo Eingabe bei 44,1 kHz oder 48 kHz hat, wird der linke Audiokanal im ersten Audioblock aufgezeichnet, und der Rechte Audiokanal wird im zweiten Audioblock aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="23e1b-202">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="23e1b-203">Für SD 4-Channel-Ausgabe: Wenn die Eingabe Stereo ist, wird der linke Titel in CHa oder CHC aufgezeichnet, und der richtige Titel wird in CHB oder CHD aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="23e1b-203">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="23e1b-204">Wenn die Eingabe Mono ist, wird die Audiodatei in CHa oder CHC aufgezeichnet, und CHB und CHD sind stumm.</span><span class="sxs-lookup"><span data-stu-id="23e1b-204">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="23e1b-205">Wenn Sie die audiopin 1 verbinden und trennen, kann ein unzulässiges Format erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="23e1b-205">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="23e1b-206">In diesem Fall gibt die [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) -Methode des Filters \_ \_ keine Verbindung mit VFW E zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="23e1b-206">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="23e1b-207">Diese Einschränkung verhindert eine Situation, in der der erste Audioblock keine Audiodaten aufweist, aber der zweite Audioblock über Audiodaten verfügt.</span><span class="sxs-lookup"><span data-stu-id="23e1b-207">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="23e1b-208">Der zweite Block sollte nur Audiodaten enthalten, wenn der erste Block auch Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="23e1b-208">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="23e1b-209">Der DV-Muxer lässt keine Audioeingaben mit unterschiedlichen Stichproben Raten zu.</span><span class="sxs-lookup"><span data-stu-id="23e1b-209">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="23e1b-210">Allerdings fügen Diagramm Erstellungs Methoden, wie z. b. [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , in der Regel den [ACM-Wrapper](acm-wrapper-filter.md) Filter hinzu, der den zweiten Audiostream entsprechend der Stichprobenrate des ersten Streams konvertiert.</span><span class="sxs-lookup"><span data-stu-id="23e1b-210">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="23e1b-211">Wenn die Audioeingabe 48 kHz oder 32 kHz ist, wird die Audioausgabe gesperrt.</span><span class="sxs-lookup"><span data-stu-id="23e1b-211">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="23e1b-212">(Es ist nicht möglich, 44,1-kHz-Audiodaten zu sperren.)</span><span class="sxs-lookup"><span data-stu-id="23e1b-212">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="23e1b-213">Wenn keine audiopins verbunden sind, enthält die Ausgabe die Audiodaten der eingehenden DV-Frames.</span><span class="sxs-lookup"><span data-stu-id="23e1b-213">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="23e1b-214">Dies kann ein schweige Wert oder gültige Audiodaten sein.</span><span class="sxs-lookup"><span data-stu-id="23e1b-214">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23e1b-215">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23e1b-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23e1b-216">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="23e1b-216">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="23e1b-217">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="23e1b-217">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



