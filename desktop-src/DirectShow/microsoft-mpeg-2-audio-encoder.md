---
description: Der Microsoft MPEG-2-audioencoderfilter codiert MPEG-1-Audioebenen I und II, einschließlich der Unterstützung für die MPEG-2-LSF-Erweiterungen (Low Sampling Frequency).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Microsoft MPEG-2-Audioencoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342727"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a><span data-ttu-id="1ec28-103">Microsoft MPEG-2-Audioencoder</span><span class="sxs-lookup"><span data-stu-id="1ec28-103">Microsoft MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="1ec28-104">Der Microsoft MPEG-2-audioencoderfilter codiert MPEG-1-Audioebenen I und II, einschließlich der Unterstützung für die MPEG-2-LSF-Erweiterungen (Low Sampling Frequency).</span><span class="sxs-lookup"><span data-stu-id="1ec28-104">The Microsoft MPEG-2 Audio Encoder filter encodes MPEG-1 audio layers I and II, including support for the MPEG-2 Low Sampling Frequency (LSF) extensions.</span></span>

<span data-ttu-id="1ec28-105">Verwenden Sie zum Codieren und multiplezieren von Audio-/Videostreams den [**Microsoft MPEG-2 Encoder-**](microsoft-mpeg-2-encoder.md) Filter, der die Funktionen dieses Filters und des [**Microsoft MPEG-2-Video Encoder-**](microsoft-mpeg-2-video-encoder.md) Filters kapselt.</span><span class="sxs-lookup"><span data-stu-id="1ec28-105">To encode and multiplex audio/video streams, use the [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) filter, which encapsulates the functions of both this filter and the [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="1ec28-106">Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ec28-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="1ec28-107">Filter Informationen</span><span class="sxs-lookup"><span data-stu-id="1ec28-107">Filter Information</span></span>

<span data-ttu-id="1ec28-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ec28-108">Filter Interfaces</span></span>

[<span data-ttu-id="1ec28-109">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="1ec28-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="1ec28-110">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="1ec28-110">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="1ec28-111">**Iencoderapi**</span><span class="sxs-lookup"><span data-stu-id="1ec28-111">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="1ec28-112">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="1ec28-112">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="1ec28-113">**Ivideoencoder**</span><span class="sxs-lookup"><span data-stu-id="1ec28-113">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="1ec28-114">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1ec28-114">Input Pin Media Types</span></span>

<span data-ttu-id="1ec28-115">**MediaType \_ Audiodatei**, **mediasubtype \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="1ec28-115">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="1ec28-116">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ec28-116">Input Pin Interfaces</span></span>

[<span data-ttu-id="1ec28-117">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="1ec28-117">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="1ec28-118">**IPin**</span><span class="sxs-lookup"><span data-stu-id="1ec28-118">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="1ec28-119">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="1ec28-119">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="1ec28-120">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1ec28-120">Output Pin Media Types</span></span>

<span data-ttu-id="1ec28-121">**MediaType \_ Audiodatei**, **mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="1ec28-121">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="1ec28-122">**MediaType \_ Stream**, **mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="1ec28-122">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="1ec28-123">**MediaType \_ Stream**, **mediasubtype \_ - \_ Programm**</span><span class="sxs-lookup"><span data-stu-id="1ec28-123">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span><br/> <span data-ttu-id="1ec28-124">**MediaType \_ Stream**, **mediasubtype \_ MPEG2- \_ Transport**</span><span class="sxs-lookup"><span data-stu-id="1ec28-124">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span><br/>

<span data-ttu-id="1ec28-125">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ec28-125">Output Pin Interfaces</span></span>

[<span data-ttu-id="1ec28-126">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="1ec28-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="1ec28-127">**IPin**</span><span class="sxs-lookup"><span data-stu-id="1ec28-127">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="1ec28-128">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="1ec28-128">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="1ec28-129">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="1ec28-129">Filter CLSID</span></span>

<span data-ttu-id="1ec28-130">**CLSID \_ CMPEG2EncoderAudioDS** (in wmcodecdsp. h deklariert)</span><span class="sxs-lookup"><span data-stu-id="1ec28-130">**CLSID\_CMPEG2EncoderAudioDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="1ec28-131">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="1ec28-131">Executable</span></span>

<span data-ttu-id="1ec28-132">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="1ec28-132">msmpeg2enc.dll</span></span>

[<span data-ttu-id="1ec28-133">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1ec28-133">Merit</span></span>](merit.md)

<span data-ttu-id="1ec28-134">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1ec28-134">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="1ec28-135">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="1ec28-135">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="1ec28-136">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="1ec28-136">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="1ec28-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ec28-137">Remarks</span></span>

<span data-ttu-id="1ec28-138">Der MPEG-2-Audioencoder kann die folgenden Arten der Ausgabe liefern:</span><span class="sxs-lookup"><span data-stu-id="1ec28-138">The MPEG-2 Audio Encoder can produce the following kinds of output:</span></span>

-   <span data-ttu-id="1ec28-139">Audioelementstream</span><span class="sxs-lookup"><span data-stu-id="1ec28-139">Audio elementary stream</span></span>
-   <span data-ttu-id="1ec28-140">Audiodaten in einem MPEG-2-Programm Datenstrom</span><span class="sxs-lookup"><span data-stu-id="1ec28-140">Audio in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="1ec28-141">Audiodaten in einem MPEG-2-Transportstream</span><span class="sxs-lookup"><span data-stu-id="1ec28-141">Audio in an MPEG-2 transport stream</span></span>

<span data-ttu-id="1ec28-142">Es werden MPEG-1-Ebenen I und II und MPEG-2 Low Sampling Frequency (LSF)-Erweiterungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ec28-142">It supports MPEG-1 layers I and II and MPEG-2 low sampling frequency (LSF) extensions</span></span>

<span data-ttu-id="1ec28-143">Eingabe Beispiele müssen 16 Bits pro Beispiel mit einer audiosamplingrate von 48, 44,1, 32, 22,05 oder 16 kHz sein.</span><span class="sxs-lookup"><span data-stu-id="1ec28-143">Input samples must 16 bits per sample, with an audio sampling rate of 48, 44.1, 32, 22.05, or 16 KHz.</span></span> <span data-ttu-id="1ec28-144">Der Encoder kann den Audiostream nicht neu einspielen. die codierte Audiodatei hat dieselbe Stichprobenrate wie die Eingabe.</span><span class="sxs-lookup"><span data-stu-id="1ec28-144">The encoder cannot resample the audio stream; the encoded audio has the same sample rate as the input.</span></span>

<span data-ttu-id="1ec28-145">Eingabe Beispiele müssen Mono oder Stereo sein.</span><span class="sxs-lookup"><span data-stu-id="1ec28-145">Input samples must be mono or stereo.</span></span> <span data-ttu-id="1ec28-146">Die codierte Audiodatei hat die Anzahl von Kanälen als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="1ec28-146">The encoded audio has the number of channels as the input.</span></span>

### <a name="limitations"></a><span data-ttu-id="1ec28-147">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="1ec28-147">Limitations</span></span>

<span data-ttu-id="1ec28-148">Der Encoder unterstützt Folgendes nicht:</span><span class="sxs-lookup"><span data-stu-id="1ec28-148">The encoder does not support the following:</span></span>

-   <span data-ttu-id="1ec28-149">MPEG Layer III-audiobitstreams.</span><span class="sxs-lookup"><span data-stu-id="1ec28-149">MPEG layer III audio bitstreams.</span></span>
-   <span data-ttu-id="1ec28-150">MPEG-2-multikanalerweiterungs-Bitstreams.</span><span class="sxs-lookup"><span data-stu-id="1ec28-150">MPEG-2 multi-channel extension bitstreams.</span></span>
-   <span data-ttu-id="1ec28-151">MPEG-4-AAC-Bitstreams.</span><span class="sxs-lookup"><span data-stu-id="1ec28-151">MPEG-4 AAC bitstreams.</span></span>
-   <span data-ttu-id="1ec28-152">Nicht rückwärtskompatible MPEG-2-Bitstreams (NBC).</span><span class="sxs-lookup"><span data-stu-id="1ec28-152">MPEG-2 non-backward compatible (NBC) bitstreams.</span></span>
-   <span data-ttu-id="1ec28-153">Generierung von Paketen, die mit packetisiert (Elementary Stream) generiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ec28-153">Generation of packetized elementary stream (PES) packets.</span></span>
-   <span data-ttu-id="1ec28-154">Dolby Digital Encoding.</span><span class="sxs-lookup"><span data-stu-id="1ec28-154">Dolby Digital encoding.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="1ec28-155">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ec28-155">Codec Properties</span></span>

<span data-ttu-id="1ec28-156">Der Filter unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="1ec28-156">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>

-   [<span data-ttu-id="1ec28-157">**Avaudiochannelcount**</span><span class="sxs-lookup"><span data-stu-id="1ec28-157">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)
-   [<span data-ttu-id="1ec28-158">**Avaudiosamplerate**</span><span class="sxs-lookup"><span data-stu-id="1ec28-158">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)
-   [<span data-ttu-id="1ec28-159">**Avencaudiointervaldecodecode**</span><span class="sxs-lookup"><span data-stu-id="1ec28-159">**AVEncAudioIntervalToEncode**</span></span>](avencaudiointervaltoencode-property.md)
-   [<span data-ttu-id="1ec28-160">**Avenccommonformateinschränkung**</span><span class="sxs-lookup"><span data-stu-id="1ec28-160">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
-   [<span data-ttu-id="1ec28-161">**Avenccommonmeanbitrate**</span><span class="sxs-lookup"><span data-stu-id="1ec28-161">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="1ec28-162">**Avencmpacodingmode**</span><span class="sxs-lookup"><span data-stu-id="1ec28-162">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)
-   [<span data-ttu-id="1ec28-163">**Avencmpacopyright**</span><span class="sxs-lookup"><span data-stu-id="1ec28-163">**AVEncMPACopyright**</span></span>](avencmpacopyright-property.md)
-   [<span data-ttu-id="1ec28-164">**Avencmpbetonung sType**</span><span class="sxs-lookup"><span data-stu-id="1ec28-164">**AVEncMPAEmphasisType**</span></span>](avencmpaemphasistype-property.md)
-   [<span data-ttu-id="1ec28-165">**Avencmpenableredundancyprotection**</span><span class="sxs-lookup"><span data-stu-id="1ec28-165">**AVEncMPAEnableRedundancyProtection**</span></span>](avencmpaenableredundancyprotection-property.md)
-   [<span data-ttu-id="1ec28-166">**Avencmpalayer**</span><span class="sxs-lookup"><span data-stu-id="1ec28-166">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
-   [<span data-ttu-id="1ec28-167">**Avencmporiginalbitstream**</span><span class="sxs-lookup"><span data-stu-id="1ec28-167">**AVEncMPAOriginalBitstream**</span></span>](avencmpaoriginalbitstream-property.md)
-   [<span data-ttu-id="1ec28-168">**Avencmpaprivateuserbit**</span><span class="sxs-lookup"><span data-stu-id="1ec28-168">**AVEncMPAPrivateUserBit**</span></span>](avencmpaprivateuserbit-property.md)

> [!Note]  
> <span data-ttu-id="1ec28-169">In einer früheren Version der Dokumentation wurden nicht ordnungsgemäß einige zusätzliche Eigenschaften aufgeführt, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1ec28-169">An earlier version of the documentation incorrectly listed some additional properties that are not supported.</span></span>

 

<span data-ttu-id="1ec28-170">Aus Gründen der Abwärtskompatibilität unterstützt der Filter die folgende Eigenschaft über die **iencoderapi** -Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="1ec28-170">For backward compatibility, the filter supports the following property through the **IEncoderAPI** interface:</span></span>



| <span data-ttu-id="1ec28-171">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ec28-171">Property</span></span>                 | <span data-ttu-id="1ec28-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ec28-172">Description</span></span>                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1ec28-173">**"endparam"- \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="1ec28-173">**ENCAPIPARAM\_BITRATE**</span></span> | <span data-ttu-id="1ec28-174">Äquivalent zu " [**avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md)".</span><span class="sxs-lookup"><span data-stu-id="1ec28-174">Equivalent to [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span></span> |



 

<span data-ttu-id="1ec28-175">Es wird empfohlen, die Eigenschaften in der folgenden Reihenfolge festzulegen:</span><span class="sxs-lookup"><span data-stu-id="1ec28-175">It is recommended to set properties in the following order:</span></span>

1.  [<span data-ttu-id="1ec28-176">**Avenccommonformateinschränkung**</span><span class="sxs-lookup"><span data-stu-id="1ec28-176">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
2.  [<span data-ttu-id="1ec28-177">**Avencmpalayer**</span><span class="sxs-lookup"><span data-stu-id="1ec28-177">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
3.  [<span data-ttu-id="1ec28-178">**Avenccommonmeanbitrate**</span><span class="sxs-lookup"><span data-stu-id="1ec28-178">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
4.  [<span data-ttu-id="1ec28-179">**Avencmpacodingmode**</span><span class="sxs-lookup"><span data-stu-id="1ec28-179">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)

<span data-ttu-id="1ec28-180">Legen Sie die restlichen Eigenschaften in beliebiger Reihenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="1ec28-180">Set the remaining properties in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec28-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ec28-181">Requirements</span></span>



| <span data-ttu-id="1ec28-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ec28-182">Requirement</span></span> | <span data-ttu-id="1ec28-183">Wert</span><span class="sxs-lookup"><span data-stu-id="1ec28-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec28-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ec28-184">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec28-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ec28-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1ec28-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ec28-186">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec28-187">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ec28-187">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="1ec28-188">Header</span><span class="sxs-lookup"><span data-stu-id="1ec28-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec28-189"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec28-189"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="1ec28-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ec28-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec28-191">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="1ec28-191">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="1ec28-192">**MPEG-2-Demultiplexer-Medientypen**</span><span class="sxs-lookup"><span data-stu-id="1ec28-192">**MPEG-2 Demultiplexer Media Types**</span></span>](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
