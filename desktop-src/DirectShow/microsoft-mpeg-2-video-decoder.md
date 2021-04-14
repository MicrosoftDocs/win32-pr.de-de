---
description: Mit diesem Filter wird das Video MPEG-1, MPEG-2, H. 264 decodiert.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Microsoft MPEG-2-Video Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392429"
---
# <a name="microsoft-mpeg-2-video-decoder"></a><span data-ttu-id="f25bf-103">Microsoft MPEG-2-Video Decoder</span><span class="sxs-lookup"><span data-stu-id="f25bf-103">Microsoft MPEG-2 Video Decoder</span></span>

<span data-ttu-id="f25bf-104">Mit diesem Filter wird das Video MPEG-1, MPEG-2, H. 264 decodiert.</span><span class="sxs-lookup"><span data-stu-id="f25bf-104">This filter decodes MPEG-1, MPEG-2, H.264 video.</span></span>

> [!Note]  
> <span data-ttu-id="f25bf-105">Das Decodieren von H. 264-Video erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f25bf-105">Decoding of H.264 video requires Windows 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f25bf-106">Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f25bf-106">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="f25bf-107">In der Registrierung lautet der Anzeige Name dieses Filters "Microsoft DTV-DVD Video Decoder".</span><span class="sxs-lookup"><span data-stu-id="f25bf-107">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Video Decoder".</span></span>



<span data-ttu-id="f25bf-108">Filter Informationen</span><span class="sxs-lookup"><span data-stu-id="f25bf-108">Filter Information</span></span>

<span data-ttu-id="f25bf-109">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f25bf-109">Filter Interfaces</span></span>

[<span data-ttu-id="f25bf-110">**Iamdecodercaps**</span><span class="sxs-lookup"><span data-stu-id="f25bf-110">**IAMDecoderCaps**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [<span data-ttu-id="f25bf-111">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="f25bf-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="f25bf-112">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="f25bf-112">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="f25bf-113">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="f25bf-113">Input Pin Media Types</span></span>

<span data-ttu-id="f25bf-114">Video Eingabe-PIN:</span><span class="sxs-lookup"><span data-stu-id="f25bf-114">Video input pin:</span></span>

-   <span data-ttu-id="f25bf-115">MediaType \_ DVD- \_ verschlüsseltes \_ Paket, mediasubtype \_ MPEG2- \_ Video</span><span class="sxs-lookup"><span data-stu-id="f25bf-115">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="f25bf-116">MediaType \_ MPEG2- \_ , mediasubtype \_ MPEG2- \_ Video</span><span class="sxs-lookup"><span data-stu-id="f25bf-116">MEDIATYPE\_MPEG2\_PES, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="f25bf-117">MediaType \_ Video, mediasubtype \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="f25bf-117">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Packet</span></span>
-   <span data-ttu-id="f25bf-118">MediaType \_ Video, mediasubtype \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="f25bf-118">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Payload</span></span>
-   <span data-ttu-id="f25bf-119">MediaType- \_ Video, mediasubtype \_ MPEG2- \_ Video</span><span class="sxs-lookup"><span data-stu-id="f25bf-119">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>

<span data-ttu-id="f25bf-120">Teilbild-Eingabe-PIN:</span><span class="sxs-lookup"><span data-stu-id="f25bf-120">Subpicture input pin:</span></span><br/>

-   <span data-ttu-id="f25bf-121">MediaType \_ DVD- \_ verschlüsseltes \_ Paket, mediasubtype \_ DVD- \_ subbild</span><span class="sxs-lookup"><span data-stu-id="f25bf-121">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_DVD\_SUBPICTURE</span></span>

<span data-ttu-id="f25bf-122">Ab Windows 7 unterstützt die Videoeingabe-PIN auch die folgenden Eingabetypen:</span><span class="sxs-lookup"><span data-stu-id="f25bf-122">Starting in Windows 7, the video input pin also supports the following input types:</span></span><br/>

-   <span data-ttu-id="f25bf-123">**MediaType \_ Video**, **mediasubtype \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="f25bf-123">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_AVC1**</span></span>
-   <span data-ttu-id="f25bf-124">**MediaType \_ Video**, **mediasubtype \_ H264**</span><span class="sxs-lookup"><span data-stu-id="f25bf-124">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_H264**</span></span>
-   <span data-ttu-id="f25bf-125">**MediaType \_ Video**, **mediasubtype \_ H264**</span><span class="sxs-lookup"><span data-stu-id="f25bf-125">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_h264**</span></span>
-   <span data-ttu-id="f25bf-126">**MediaType \_ Video**, **mediasubtype \_ X264**</span><span class="sxs-lookup"><span data-stu-id="f25bf-126">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_X264**</span></span>
-   <span data-ttu-id="f25bf-127">**MediaType \_ Video**, **mediasubtype \_ x264**</span><span class="sxs-lookup"><span data-stu-id="f25bf-127">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_x264**</span></span>

<span data-ttu-id="f25bf-128">Weitere Informationen finden Sie unter [H. 264-Video Typen](h-264-video-types.md) .</span><span class="sxs-lookup"><span data-stu-id="f25bf-128">See [H.264 Video Types](h-264-video-types.md) for more information.</span></span> <span data-ttu-id="f25bf-129">Der Eingabe Medientyp kann sich dynamisch zwischen den Typen "MPEG2" und "H. 264" ändern.</span><span class="sxs-lookup"><span data-stu-id="f25bf-129">The input media type can change dynamically between MPEG2 and H.264 types.</span></span><br/>

<span data-ttu-id="f25bf-130">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="f25bf-130">Input Pin Interfaces</span></span>

[<span data-ttu-id="f25bf-131">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="f25bf-131">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="f25bf-132">**"Ikspropertyset"**</span><span class="sxs-lookup"><span data-stu-id="f25bf-132">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="f25bf-133">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="f25bf-133">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="f25bf-134">**IMF Sample Protection**</span><span class="sxs-lookup"><span data-stu-id="f25bf-134">**IMFSampleProtection**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [<span data-ttu-id="f25bf-135">**IPin**</span><span class="sxs-lookup"><span data-stu-id="f25bf-135">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="f25bf-136">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="f25bf-136">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="f25bf-137">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="f25bf-137">Output Pin Media Types</span></span>

<span data-ttu-id="f25bf-138">Video Ausgabe-PIN:</span><span class="sxs-lookup"><span data-stu-id="f25bf-138">Video output pin:</span></span>

-   <span data-ttu-id="f25bf-139">MediaType- \_ Video, DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-139">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_A (DXVA 1.0)</span></span>
-   <span data-ttu-id="f25bf-140">MediaType- \_ Video, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-140">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_C (DXVA 1.0)</span></span>
-   <span data-ttu-id="f25bf-141">MediaType \_ Video, mediasubtype \_ I420 (Software Decodierung oder DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-141">MEDIATYPE\_Video, MEDIASUBTYPE\_I420 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="f25bf-142">MediaType \_ Video, mediasubtype \_ NV12 (Software Decodierung oder DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-142">MEDIATYPE\_Video, MEDIASUBTYPE\_NV12 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="f25bf-143">MediaType \_ Video, mediasubtype \_ im YUY2 (Software Decodierung oder DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-143">MEDIATYPE\_Video, MEDIASUBTYPE\_YUY2 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="f25bf-144">MediaType \_ Video, mediasubtype \_ IMC3 (nur DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-144">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC3 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="f25bf-145">MediaType \_ Video, mediasubtype \_ IMC4 (nur DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-145">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC4 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="f25bf-146">MediaType \_ Video, mediasubtype \_ S340 (nur DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-146">MEDIATYPE\_Video, MEDIASUBTYPE\_S340 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="f25bf-147">MediaType \_ Video, mediasubtype \_ YV12 (nur DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="f25bf-147">MEDIATYPE\_Video, MEDIASUBTYPE\_YV12 (DXVA2.0 only)</span></span>

<span data-ttu-id="f25bf-148">Zeilen-21-Ausgabe-PIN:</span><span class="sxs-lookup"><span data-stu-id="f25bf-148">Line-21 output pin:</span></span><br/>

-   <span data-ttu-id="f25bf-149">MediaType \_ AUXLine21Data, mediasubtype \_ Line21 \_ goppacket</span><span class="sxs-lookup"><span data-stu-id="f25bf-149">MEDIATYPE\_AUXLine21Data, MEDIASUBTYPE\_Line21\_GOPPacket</span></span>

<span data-ttu-id="f25bf-150">Ausgabepin für Teilbild:</span><span class="sxs-lookup"><span data-stu-id="f25bf-150">Subpicture output pin:</span></span><br/>

-   <span data-ttu-id="f25bf-151">MediaType \_ Video, mediasubtype \_ AI44</span><span class="sxs-lookup"><span data-stu-id="f25bf-151">MEDIATYPE\_Video, MEDIASUBTYPE\_AI44</span></span>
-   <span data-ttu-id="f25bf-152">MediaType \_ Video, mediasubtype \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="f25bf-152">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="f25bf-153">MediaType \_ Video, mediasubtype \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="f25bf-153">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="f25bf-154">MediaType- \_ Video, mediasubtype \_ ayuv</span><span class="sxs-lookup"><span data-stu-id="f25bf-154">MEDIATYPE\_Video, MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="f25bf-155">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f25bf-155">Output Pin Interfaces</span></span>

<span data-ttu-id="f25bf-156">[**Iamvideoacceleratornotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (nur Videoausgabe-PIN)</span><span class="sxs-lookup"><span data-stu-id="f25bf-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video output pin only)</span></span><br/> [<span data-ttu-id="f25bf-157">**"Ikspropertyset"**</span><span class="sxs-lookup"><span data-stu-id="f25bf-157">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="f25bf-158">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="f25bf-158">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="f25bf-159">**IPin**</span><span class="sxs-lookup"><span data-stu-id="f25bf-159">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="f25bf-160">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="f25bf-160">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [<span data-ttu-id="f25bf-161">**Ivpconfig**</span><span class="sxs-lookup"><span data-stu-id="f25bf-161">**IVPConfig**</span></span>](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

<span data-ttu-id="f25bf-162">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="f25bf-162">Filter CLSID</span></span>

<span data-ttu-id="f25bf-163">**CLSID \_ CMPEG2VidDecoderDS** (in wmcodecdsp. h definiert)</span><span class="sxs-lookup"><span data-stu-id="f25bf-163">**CLSID\_CMPEG2VidDecoderDS** (defined in wmcodecdsp.h)</span></span>

<span data-ttu-id="f25bf-164">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="f25bf-164">Executable</span></span>

<span data-ttu-id="f25bf-165">msmpeg2vdec.dll</span><span class="sxs-lookup"><span data-stu-id="f25bf-165">msmpeg2vdec.dll</span></span>

[<span data-ttu-id="f25bf-166">Verdienst</span><span class="sxs-lookup"><span data-stu-id="f25bf-166">Merit</span></span>](merit.md)

<span data-ttu-id="f25bf-167">**Verdienst \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="f25bf-167">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="f25bf-168">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="f25bf-168">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="f25bf-169">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="f25bf-169">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="f25bf-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f25bf-170">Remarks</span></span>

<span data-ttu-id="f25bf-171">Dieser Filter verfügt über zwei Eingabe Pins und drei Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="f25bf-171">This filter has two input pins and three output pins.</span></span>

<span data-ttu-id="f25bf-172">Eingabe Pins:</span><span class="sxs-lookup"><span data-stu-id="f25bf-172">Input pins:</span></span>

-   <span data-ttu-id="f25bf-173">Videoeingang</span><span class="sxs-lookup"><span data-stu-id="f25bf-173">Video input</span></span>
-   <span data-ttu-id="f25bf-174">Teil Bild Eingabe</span><span class="sxs-lookup"><span data-stu-id="f25bf-174">Subpicture input</span></span>

<span data-ttu-id="f25bf-175">Ausgabe Pins:</span><span class="sxs-lookup"><span data-stu-id="f25bf-175">Output pins:</span></span>

-   <span data-ttu-id="f25bf-176">Videoausgang</span><span class="sxs-lookup"><span data-stu-id="f25bf-176">Video output</span></span>
-   <span data-ttu-id="f25bf-177">Zeile-21-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f25bf-177">Line-21 output</span></span>
-   <span data-ttu-id="f25bf-178">Teil Bild Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f25bf-178">Subpicture output</span></span>

<span data-ttu-id="f25bf-179">Der Filter erstellt nicht die Ausgabe-PIN für das Teil Bild, es sei denn, die Videoeingabe-PIN ist mit einem MediaType-Dateityp mit **\_ DVD \_ verschlüsselt \_** .</span><span class="sxs-lookup"><span data-stu-id="f25bf-179">The filter does not create the subpicture output pin unless the video input pin is connected with a **MEDIATYPE\_DVD\_ENCRYPTED\_PACK** media type.</span></span>

### <a name="mpeg-12-support"></a><span data-ttu-id="f25bf-180">MPEG-1/2-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f25bf-180">MPEG-1/2 Support</span></span>

<span data-ttu-id="f25bf-181">Für MPEG-1 und MPEG-2 unterstützt der Decoder die folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="f25bf-181">For MPEG-1 and MPEG-2, the decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f25bf-182">Profile/Ebenen</span><span class="sxs-lookup"><span data-stu-id="f25bf-182">Profiles/Levels</span></span></td>
<td><span data-ttu-id="f25bf-183">Eine beliebige Kombination der folgenden Profile und Ebenen:</span><span class="sxs-lookup"><span data-stu-id="f25bf-183">Any combination of the following profiles and levels:</span></span><br/>
<ul>
<li><span data-ttu-id="f25bf-184">Profile: einfach, Main</span><span class="sxs-lookup"><span data-stu-id="f25bf-184">Profiles: Simple, Main</span></span></li>
<li><span data-ttu-id="f25bf-185">Ebenen: niedrig, Main, hoch, hoch 1440</span><span class="sxs-lookup"><span data-stu-id="f25bf-185">Levels: Low, Main, High, High 1440</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f25bf-186">Chroma-Formate</span><span class="sxs-lookup"><span data-stu-id="f25bf-186">Chroma Formats</span></span></td>
<td><span data-ttu-id="f25bf-187">4:2:0 Chroma</span><span class="sxs-lookup"><span data-stu-id="f25bf-187">4:2:0 chroma</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f25bf-188">Maximale Auflösung</span><span class="sxs-lookup"><span data-stu-id="f25bf-188">Maximum Resolution</span></span></td>
<td><span data-ttu-id="f25bf-189">1920 × 1088 Pixel</span><span class="sxs-lookup"><span data-stu-id="f25bf-189">1920 × 1088 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f25bf-190">DXVA</span><span class="sxs-lookup"><span data-stu-id="f25bf-190">DXVA</span></span></td>
<td><span data-ttu-id="f25bf-191">Der Decoder unterstützt die DirectX-Video Beschleunigung (DXVA) Version 1 und Version 2.</span><span class="sxs-lookup"><span data-stu-id="f25bf-191">The decoder supports DirectX Video Acceleration (DXVA) version 1 and version 2.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f25bf-192">Der Decoder unterstützt keine skalierbaren Bitstreams.</span><span class="sxs-lookup"><span data-stu-id="f25bf-192">The decoder does not support scalable bitstreams.</span></span> <span data-ttu-id="f25bf-193">Die Eingabe muss ein grundlegender Videostream sein.</span><span class="sxs-lookup"><span data-stu-id="f25bf-193">The input must be an elementary video stream.</span></span>

<span data-ttu-id="f25bf-194">Der Decoder unterstützt keine 4:2:2 Chroma-Formate.</span><span class="sxs-lookup"><span data-stu-id="f25bf-194">The decoder does not support 4:2:2 chroma formats.</span></span>

### <a name="h264-support"></a><span data-ttu-id="f25bf-195">H. 264-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f25bf-195">H.264 Support</span></span>

<span data-ttu-id="f25bf-196">Für H. 264 unterstützt der Decoder die folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="f25bf-196">For H.264, the decoder supports the following formats:</span></span>



| <span data-ttu-id="f25bf-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f25bf-197">Requirement</span></span> | <span data-ttu-id="f25bf-198">Wert</span><span class="sxs-lookup"><span data-stu-id="f25bf-198">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f25bf-199">Profile/Ebenen</span><span class="sxs-lookup"><span data-stu-id="f25bf-199">Profiles/Levels</span></span>    | <span data-ttu-id="f25bf-200">Baseline, Main und High Profile, bis zu Ebene 5,1.</span><span class="sxs-lookup"><span data-stu-id="f25bf-200">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="f25bf-201">(Ausführliche Informationen finden Sie in der ITU-T H. 264-Spezifikation.)</span><span class="sxs-lookup"><span data-stu-id="f25bf-201">(See ITU-T H.264 specification for details.)</span></span>                                                                                                                                                                          |
| <span data-ttu-id="f25bf-202">Chroma-Formate</span><span class="sxs-lookup"><span data-stu-id="f25bf-202">Chroma Formats</span></span>     | <span data-ttu-id="f25bf-203">4:2:0 Chroma oder Monochrom</span><span class="sxs-lookup"><span data-stu-id="f25bf-203">4:2:0 chroma or monochrome</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="f25bf-204">Minimale Auflösung</span><span class="sxs-lookup"><span data-stu-id="f25bf-204">Minimum Resolution</span></span> | <span data-ttu-id="f25bf-205">48 × 48 Pixel</span><span class="sxs-lookup"><span data-stu-id="f25bf-205">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f25bf-206">Maximale Auflösung</span><span class="sxs-lookup"><span data-stu-id="f25bf-206">Maximum Resolution</span></span> | <span data-ttu-id="f25bf-207">1920 × 1088 Pixel</span><span class="sxs-lookup"><span data-stu-id="f25bf-207">1920 × 1088 pixels</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f25bf-208">DXVA</span><span class="sxs-lookup"><span data-stu-id="f25bf-208">DXVA</span></span>               | <span data-ttu-id="f25bf-209">Der Decoder unterstützt DXVA Version 2, aber nicht DXVA Version 1.</span><span class="sxs-lookup"><span data-stu-id="f25bf-209">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="f25bf-210">DXVA-Decodierung wird nur für Haupt kompatible Bitstreams, Main und High Profile unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f25bf-210">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="f25bf-211">(Haupt-kompatible Baseline-Bitstreams werden als **Profil \_ IDC**= 66 und **eingeschränkter \_ set1- \_ Flag**= 1 definiert.)</span><span class="sxs-lookup"><span data-stu-id="f25bf-211">(Main-compatible Baseline bitstreams are defined as **profile\_idc**=66 and **constrained\_set1\_flag**=1.)</span></span> |



 

<span data-ttu-id="f25bf-212">Der Decoder bietet keine Unterstützung für die Technologie zum Filmen von Folien.</span><span class="sxs-lookup"><span data-stu-id="f25bf-212">The decoder does not support Film Grain Technology.</span></span>

<span data-ttu-id="f25bf-213">Weitere Informationen zu den h. 264-Medientypen finden Sie unter [h. 264-Video Typen](h-264-video-types.md).</span><span class="sxs-lookup"><span data-stu-id="f25bf-213">For information about the H.264 media types, see [H.264 Video Types](h-264-video-types.md).</span></span>

### <a name="codec-properties"></a><span data-ttu-id="f25bf-214">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f25bf-214">Codec Properties</span></span>

<span data-ttu-id="f25bf-215">Die Eingabe-Pins unterstützen die folgenden Eigenschaften Sätze über " [**ikspropertyset**](ikspropertyset.md)":</span><span class="sxs-lookup"><span data-stu-id="f25bf-215">The input pins support the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="f25bf-216">**Eigenschaften Satz für den DVD-Kopierschutz**</span><span class="sxs-lookup"><span data-stu-id="f25bf-216">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="f25bf-217">[**Eigenschaft des DVD-Teil Bilds**](dvd-subpicture-property-set.md) (nur unter Bild-PIN)</span><span class="sxs-lookup"><span data-stu-id="f25bf-217">[**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (subpicture pin only)</span></span>

<span data-ttu-id="f25bf-218">Die Eingabe-Pins unterstützen die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="f25bf-218">The input pins support the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="f25bf-219">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f25bf-219">Property</span></span>                                                                  | <span data-ttu-id="f25bf-220">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f25bf-220">Requires</span></span>      |
|---------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="f25bf-221">**Avdeccommoninputformat**</span><span class="sxs-lookup"><span data-stu-id="f25bf-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md)         | <span data-ttu-id="f25bf-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f25bf-222">Windows Vista</span></span> |
| [<span data-ttu-id="f25bf-223">**Avdecvideoinputscantype**</span><span class="sxs-lookup"><span data-stu-id="f25bf-223">**AVDecVideoInputScanType**</span></span>](avdecvideoinputscantype-property.md)       | <span data-ttu-id="f25bf-224">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f25bf-224">Windows Vista</span></span> |
| [<span data-ttu-id="f25bf-225">**Avdecvideopixelaspectratio**</span><span class="sxs-lookup"><span data-stu-id="f25bf-225">**AVDecVideoPixelAspectRatio**</span></span>](avdecvideopixelaspectratio-property.md) | <span data-ttu-id="f25bf-226">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f25bf-226">Windows Vista</span></span> |



 

<span data-ttu-id="f25bf-227">Der Filter unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="f25bf-227">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="f25bf-228">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f25bf-228">Property</span></span>                                                                                | <span data-ttu-id="f25bf-229">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f25bf-229">Requires</span></span>      |
|-----------------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="f25bf-230">**Avdecmmcssclass**</span><span class="sxs-lookup"><span data-stu-id="f25bf-230">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                          | <span data-ttu-id="f25bf-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f25bf-231">Windows Vista</span></span> |
| [<span data-ttu-id="f25bf-232">**Avdecvideoacceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="f25bf-232">**AVDecVideoAcceleration\_H264**</span></span>](avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="f25bf-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25bf-233">Windows 7</span></span>     |
| [<span data-ttu-id="f25bf-234">**Avdecvideoacceleration- \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="f25bf-234">**AVDecVideoAcceleration\_MPEG2**</span></span>](avdecvideoacceleration-mpeg2-property.md)          | <span data-ttu-id="f25bf-235">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25bf-235">Windows 7</span></span>     |
| [<span data-ttu-id="f25bf-236">**Avdecvideodroppicwithmissingref**</span><span class="sxs-lookup"><span data-stu-id="f25bf-236">**AVDecVideoDropPicWithMissingRef**</span></span>](avdecvideodroppicwithmissingref-property.md)     | <span data-ttu-id="f25bf-237">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25bf-237">Windows 7</span></span>     |
| [<span data-ttu-id="f25bf-238">**Avdecvideofastdecodemode**</span><span class="sxs-lookup"><span data-stu-id="f25bf-238">**AVDecVideoFastDecodeMode**</span></span>](avdecvideofastdecodemode.md)                            | <span data-ttu-id="f25bf-239">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25bf-239">Windows 7</span></span>     |
| [<span data-ttu-id="f25bf-240">**Avdecvideoimagesize**</span><span class="sxs-lookup"><span data-stu-id="f25bf-240">**AVDecVideoImageSize**</span></span>](avdecvideoimagesize.md)                                      | <span data-ttu-id="f25bf-241">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25bf-241">Windows 7</span></span>     |
| [<span data-ttu-id="f25bf-242">**Avdecvideosoftwaredeingeterlacemode**</span><span class="sxs-lookup"><span data-stu-id="f25bf-242">**AVDecVideoSoftwareDeinterlaceMode**</span></span>](avdecvideosoftwaredeinterlacemode-property.md) | <span data-ttu-id="f25bf-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25bf-243">Windows 7</span></span>     |
| [<span data-ttu-id="f25bf-244">**Avdecvideothumbnailgenerationmode**</span><span class="sxs-lookup"><span data-stu-id="f25bf-244">**AVDecVideoThumbnailGenerationMode**</span></span>](avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="f25bf-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f25bf-245">Windows 7</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="f25bf-246">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f25bf-246">Requirements</span></span>



| <span data-ttu-id="f25bf-247">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f25bf-247">Requirement</span></span> | <span data-ttu-id="f25bf-248">Wert</span><span class="sxs-lookup"><span data-stu-id="f25bf-248">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f25bf-249">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f25bf-249">Minimum supported client</span></span><br/> | <span data-ttu-id="f25bf-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]</span><span class="sxs-lookup"><span data-stu-id="f25bf-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f25bf-251">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f25bf-251">Minimum supported server</span></span><br/> | <span data-ttu-id="f25bf-252">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f25bf-252">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="f25bf-253">Header</span><span class="sxs-lookup"><span data-stu-id="f25bf-253">Header</span></span><br/>                   | <dl> <span data-ttu-id="f25bf-254"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f25bf-254"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="f25bf-255">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f25bf-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25bf-256">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="f25bf-256">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f25bf-257">**DVD-Medientypen**</span><span class="sxs-lookup"><span data-stu-id="f25bf-257">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> <dt>

[<span data-ttu-id="f25bf-258">H. 264-Video Typen</span><span class="sxs-lookup"><span data-stu-id="f25bf-258">H.264 Video Types</span></span>](h-264-video-types.md)
</dt> </dl>

 

 
