---
description: Der Microsoft MPEG-2 Encoder-Filter codiert MPEG-2-Audiodaten und-Videos und multiplediert die Streams, um einen MPEG-2-Programmstream oder einen Transportstream zu generieren.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Microsoft MPEG-2 Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745968"
---
# <a name="microsoft-mpeg-2-encoder"></a><span data-ttu-id="647a8-103">Microsoft MPEG-2-Encoder</span><span class="sxs-lookup"><span data-stu-id="647a8-103">Microsoft MPEG-2 Encoder</span></span>

<span data-ttu-id="647a8-104">Der Microsoft MPEG-2 Encoder-Filter codiert MPEG-2-Audiodaten und-Videos und multiplediert die Streams, um einen MPEG-2-Programmstream oder einen Transportstream zu generieren.</span><span class="sxs-lookup"><span data-stu-id="647a8-104">The Microsoft MPEG-2 Encoder filter encodes MPEG-2 audio and video and multiplexes the streams to generate an MPEG-2 program stream or transport stream.</span></span>

> [!Note]  
> <span data-ttu-id="647a8-105">Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="647a8-105">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="647a8-106">Filter Informationen</span><span class="sxs-lookup"><span data-stu-id="647a8-106">Filter Information</span></span>

<span data-ttu-id="647a8-107">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="647a8-107">Filter Interfaces</span></span>

[<span data-ttu-id="647a8-108">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="647a8-108">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="647a8-109">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="647a8-109">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="647a8-110">**Iencoderapi**</span><span class="sxs-lookup"><span data-stu-id="647a8-110">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="647a8-111">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="647a8-111">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="647a8-112">**Ivideoencoder**</span><span class="sxs-lookup"><span data-stu-id="647a8-112">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="647a8-113">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="647a8-113">Input Pin Media Types</span></span>

<span data-ttu-id="647a8-114">Siehe Hinweise</span><span class="sxs-lookup"><span data-stu-id="647a8-114">See Remarks</span></span>

<span data-ttu-id="647a8-115">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="647a8-115">Input Pin Interfaces</span></span>

[<span data-ttu-id="647a8-116">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="647a8-116">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="647a8-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="647a8-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="647a8-118">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="647a8-118">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="647a8-119">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="647a8-119">Output Pin Media Types</span></span>

<span data-ttu-id="647a8-120">Siehe Hinweise</span><span class="sxs-lookup"><span data-stu-id="647a8-120">See Remarks</span></span>

<span data-ttu-id="647a8-121">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="647a8-121">Output Pin Interfaces</span></span>

[<span data-ttu-id="647a8-122">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="647a8-122">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="647a8-123">**IPin**</span><span class="sxs-lookup"><span data-stu-id="647a8-123">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="647a8-124">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="647a8-124">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="647a8-125">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="647a8-125">Filter CLSID</span></span>

<span data-ttu-id="647a8-126">**CLSID \_ CMPEG2EncoderDS** (in wmcodecdsp. h deklariert)</span><span class="sxs-lookup"><span data-stu-id="647a8-126">**CLSID\_CMPEG2EncoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="647a8-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="647a8-127">Executable</span></span>

<span data-ttu-id="647a8-128">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="647a8-128">msmpeg2enc.dll</span></span>

[<span data-ttu-id="647a8-129">Verdienst</span><span class="sxs-lookup"><span data-stu-id="647a8-129">Merit</span></span>](merit.md)

<span data-ttu-id="647a8-130">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="647a8-130">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="647a8-131">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="647a8-131">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="647a8-132">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="647a8-132">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="647a8-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="647a8-133">Remarks</span></span>

<span data-ttu-id="647a8-134">Dieser Filter kombiniert die Codierungs Funktionen von zwei anderen Filtern:</span><span class="sxs-lookup"><span data-stu-id="647a8-134">This filter combines the encoding functionality of two other filters:</span></span>

-   [<span data-ttu-id="647a8-135">**Microsoft MPEG-2-Audioencoder**</span><span class="sxs-lookup"><span data-stu-id="647a8-135">**Microsoft MPEG-2 Audio Encoder**</span></span>](microsoft-mpeg-2-audio-encoder.md)
-   [<span data-ttu-id="647a8-136">**Microsoft MPEG-2-Video Encoder**</span><span class="sxs-lookup"><span data-stu-id="647a8-136">**Microsoft MPEG-2 Video Encoder**</span></span>](microsoft-mpeg-2-video-encoder.md)

<span data-ttu-id="647a8-137">Sofern nicht anders angegeben, unterstützt dieser Filter dieselben Codierungs Funktionen wie diese beiden Encoder.</span><span class="sxs-lookup"><span data-stu-id="647a8-137">Except as noted, this filter supports the same encoding features as those two encoders.</span></span>

<span data-ttu-id="647a8-138">Anfänglich hat der Filter eine Eingabe-PIN, die Audiodaten oder Videoeingaben akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="647a8-138">Initially the filter has one input pin, which can accept audio or video input.</span></span> <span data-ttu-id="647a8-139">Wenn diese Pin verbunden ist, erstellt der Filter eine zweite Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="647a8-139">When that pin is connected, the filter creates a second input pin.</span></span> <span data-ttu-id="647a8-140">Wenn die erste Eingabe-PIN Audiodaten empfängt, akzeptiert die zweite Eingabe-PIN nur Video und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="647a8-140">If the first input pin receives audio, the second input pin accepts only video, and vice versa.</span></span> <span data-ttu-id="647a8-141">Jede Eingabe-PIN unterstützt die gleichen Medientypen wie der entsprechende Codierungs Filter.</span><span class="sxs-lookup"><span data-stu-id="647a8-141">Each input pin supports the same media types as the corresponding encoder filter.</span></span>

<span data-ttu-id="647a8-142">Wenn nur eine Eingabe-PIN verbunden ist, unterstützt der Filter dieselben Ausgabetypen wie der entsprechende Audio-oder Video Encoder.</span><span class="sxs-lookup"><span data-stu-id="647a8-142">If only one input pin is connected, the filter supports the same output types as the corresponding audio or video encoder.</span></span> <span data-ttu-id="647a8-143">Wenn beide Pins verbunden sind, unterstützt der Filter die folgenden Arten der Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="647a8-143">If both pins are connected, the filter supports the following kinds of output:</span></span>

-   <span data-ttu-id="647a8-144">Audiovisualisierung in einem MPEG-2-Programmstream</span><span class="sxs-lookup"><span data-stu-id="647a8-144">Audio-visual in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="647a8-145">Audiovisualisierung in einem MPEG-2-Transportstream</span><span class="sxs-lookup"><span data-stu-id="647a8-145">Audio-visual in an MPEG-2 transport stream</span></span>

<span data-ttu-id="647a8-146">Diese entsprechen den folgenden Ausgabetypen:</span><span class="sxs-lookup"><span data-stu-id="647a8-146">These correspond to the following output types:</span></span>

-   <span data-ttu-id="647a8-147">**MediaType \_ Stream**, **mediasubtype \_ - \_ Programm**</span><span class="sxs-lookup"><span data-stu-id="647a8-147">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>
-   <span data-ttu-id="647a8-148">**MediaType \_ Stream**, **mediasubtype \_ MPEG2- \_ Transport**</span><span class="sxs-lookup"><span data-stu-id="647a8-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>

<span data-ttu-id="647a8-149">Dieser Filter kann keine zuvor codierten Datenströme Multiplexes.</span><span class="sxs-lookup"><span data-stu-id="647a8-149">This filter cannot multiplex streams that were previously encoded.</span></span> <span data-ttu-id="647a8-150">Die Eingabedaten Ströme müssen unkomprimierte Audiodaten und Videos sein, die vom Filter vor Multiplexing codiert werden.</span><span class="sxs-lookup"><span data-stu-id="647a8-150">The input streams must be uncompressed audio/video, which the filter encodes before multiplexing.</span></span> <span data-ttu-id="647a8-151">Der Multiplex-Stream ist auf ein Programm beschränkt, das bis zu einen Audiostream und einen Videostream enthält.</span><span class="sxs-lookup"><span data-stu-id="647a8-151">The multiplexed stream is limited to one program, containing up to one audio and one video stream.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="647a8-152">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="647a8-152">Codec Properties</span></span>

<span data-ttu-id="647a8-153">Der Filter unterstützt die kombinierten Eigenschaften des [**MPEG-2-Audioencoders**](microsoft-mpeg-2-audio-encoder.md) und [**MPEG-2-Video Encoder**](microsoft-mpeg-2-video-encoder.md) -Filter mit folgendem Unterschied:</span><span class="sxs-lookup"><span data-stu-id="647a8-153">The filter supports the combined properties of the [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) and [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filters, with the following difference:</span></span>

-   <span data-ttu-id="647a8-154">Mit der Eigenschaft " [**avenccommonmeanbitrate**](avenccommonmeanbitrate-property.md) " wird die durchschnittliche Bitrate für den Videostream festgelegt.</span><span class="sxs-lookup"><span data-stu-id="647a8-154">The [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property sets the average bit rate for the video stream.</span></span>
-   <span data-ttu-id="647a8-155">Mit der Eigenschaft " [**avencaudiomeanbitrate**](avencaudiomeanbitrate.md) " wird die durchschnittliche Bitrate für den Audiostream festgelegt.</span><span class="sxs-lookup"><span data-stu-id="647a8-155">The [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) property sets the average bit rate for the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="647a8-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="647a8-156">Requirements</span></span>



| <span data-ttu-id="647a8-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="647a8-157">Requirement</span></span> | <span data-ttu-id="647a8-158">Wert</span><span class="sxs-lookup"><span data-stu-id="647a8-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647a8-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="647a8-159">Minimum supported client</span></span><br/> | <span data-ttu-id="647a8-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]</span><span class="sxs-lookup"><span data-stu-id="647a8-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="647a8-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="647a8-161">Minimum supported server</span></span><br/> | <span data-ttu-id="647a8-162">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="647a8-162">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="647a8-163">Header</span><span class="sxs-lookup"><span data-stu-id="647a8-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="647a8-164"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="647a8-164"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="647a8-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="647a8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647a8-166">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="647a8-166">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
