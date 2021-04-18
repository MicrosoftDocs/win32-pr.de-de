---
description: 'Dieser Filter decodiert die folgenden Audioformate:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Microsoft MPEG-1/DD/AAC-Audiodecoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338863"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a><span data-ttu-id="51577-103">Microsoft MPEG-1/DD/AAC-Audiodecoder</span><span class="sxs-lookup"><span data-stu-id="51577-103">Microsoft MPEG-1/DD/AAC Audio Decoder</span></span>

<span data-ttu-id="51577-104">Dieser Filter decodiert die folgenden Audioformate:</span><span class="sxs-lookup"><span data-stu-id="51577-104">This filter decodes the following audio formats:</span></span>

-   <span data-ttu-id="51577-105">MPEG-1-Audioebenen I und II.</span><span class="sxs-lookup"><span data-stu-id="51577-105">MPEG-1 audio layers I and II.</span></span>
-   <span data-ttu-id="51577-106">Rückwärtskompatible MPEG-2-Audiodaten, Schichten I und II (ISO/IEC 13818-3), Mono und Stereo.</span><span class="sxs-lookup"><span data-stu-id="51577-106">Backward-compatible MPEG-2 audio, layers I and II (ISO/IEC 13818-3), mono and stereo only.</span></span>
-   <span data-ttu-id="51577-107">LC-Profil (Advanced audiocoding) mit geringer Komplexität.</span><span class="sxs-lookup"><span data-stu-id="51577-107">Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span>
-   <span data-ttu-id="51577-108">High-Efficiency AAC (HE-AAC) Version 1 und Version 2.</span><span class="sxs-lookup"><span data-stu-id="51577-108">High-Efficiency AAC (HE-AAC) version 1 and version 2.</span></span>
-   <span data-ttu-id="51577-109">Pass-Through Digital Theater Systems (DTS) für die digitale Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="51577-109">Pass-through Digital Theater Systems (DTS) for digital output.</span></span>
-   <span data-ttu-id="51577-110">Nur LPCM, Mono und Stereo, mit oder ohne PES-Header.</span><span class="sxs-lookup"><span data-stu-id="51577-110">LPCM, mono and stereo only, with or without PES headers.</span></span>
-   <span data-ttu-id="51577-111">Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="51577-111">Dolby Digital.</span></span>
-   <span data-ttu-id="51577-112">Dolby Digital Plus, einschließlich der Konvertierung von Dolby Digital Plus in Dolby Digital for Digital Output.</span><span class="sxs-lookup"><span data-stu-id="51577-112">Dolby Digital Plus, including conversion from Dolby Digital Plus to Dolby Digital for digital output.</span></span>

> [!Note]  
> <span data-ttu-id="51577-113">Die Microsoft-Implementierung der Dolby Digital-Technologie ist gemäß den Bedingungen des Dolby Digital Licensing Program eingeschränkt, das von Microsoft-Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51577-113">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="51577-114">Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51577-114">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="51577-115">Für das Decodieren von Dolby Digital Plus-, AAC-und HE-AAC-Formaten ist Windows 7 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="51577-115">Decoding of Dolby Digital Plus, AAC, and HE-AAC formats requires Windows 7.</span></span> <span data-ttu-id="51577-116">Das Decodieren von Dolby Digital oder Dolby Digital Plus wird unter Windows 7 Home Basic oder Windows 7 Starter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51577-116">Decoding of Dolby Digital or Dolby Digital Plus is not supported on Windows 7 Home Basic or Windows 7 Starter.</span></span>

<span data-ttu-id="51577-117">In der Registrierung lautet der Anzeige Name dieses Filters "Microsoft DTV-DVD-Audiodecoder".</span><span class="sxs-lookup"><span data-stu-id="51577-117">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Audio Decoder".</span></span>



<span data-ttu-id="51577-118">Filter Informationen</span><span class="sxs-lookup"><span data-stu-id="51577-118">Filter Information</span></span>

<span data-ttu-id="51577-119">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="51577-119">Filter Interfaces</span></span>

[<span data-ttu-id="51577-120">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="51577-120">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="51577-121">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="51577-121">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="51577-122">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="51577-122">Input Pin Media Types</span></span>

<span data-ttu-id="51577-123">In Windows Vista und höher unterstützt der Filter die folgenden Eingabetypen:</span><span class="sxs-lookup"><span data-stu-id="51577-123">In Windows Vista and later, the filter supports the following input types:</span></span><br/>

-   <span data-ttu-id="51577-124">**MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)</span><span class="sxs-lookup"><span data-stu-id="51577-124">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="51577-125">**MediaType \_ Audiodaten**, **mediasubtype \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="51577-125">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="51577-126">**MediaType \_ Audiodaten**, **mediasubtype \_ MPEG1Payload**</span><span class="sxs-lookup"><span data-stu-id="51577-126">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Payload**</span></span>
-   <span data-ttu-id="51577-127">**MediaType \_ Audiodatei**, **mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="51577-127">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="51577-128">**MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)</span><span class="sxs-lookup"><span data-stu-id="51577-128">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="51577-129">**MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ DTS** (siehe Hinweis 2)</span><span class="sxs-lookup"><span data-stu-id="51577-129">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="51577-130">**MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="51577-130">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="51577-131">**MediaType \_ DVD- \_ verschlüsseltes \_ Paket**, **mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="51577-131">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="51577-132">**MediaType \_ MPEG2 \_ PES**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)</span><span class="sxs-lookup"><span data-stu-id="51577-132">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="51577-133">**MediaType \_ MPEG2 \_ PES**, **mediasubtype \_ DTS** (siehe Hinweis 2)</span><span class="sxs-lookup"><span data-stu-id="51577-133">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="51577-134">**MediaType \_ MPEG2- \_ PES**, **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="51577-134">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="51577-135">**MediaType \_ MPEG2- \_ PES**, **mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="51577-135">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="51577-136">**MediaType \_ Stream**, **mediasubtype \_ Dolby \_ AC3** (siehe Hinweis 1)</span><span class="sxs-lookup"><span data-stu-id="51577-136">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="51577-137">**MediaType \_ Stream**, **mediasubtype \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="51577-137">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="51577-138">**MediaType \_ Stream**, **mediasubtype \_ \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="51577-138">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>

<span data-ttu-id="51577-139">Ab Windows 7 unterstützt der Filter auch die folgenden Eingabetypen:</span><span class="sxs-lookup"><span data-stu-id="51577-139">Starting in Windows 7, the filter also supports the following input types:</span></span><br/>

-   <span data-ttu-id="51577-140">**MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ ddplus** (siehe Hinweis 1)</span><span class="sxs-lookup"><span data-stu-id="51577-140">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="51577-141">**MediaType \_ Audiodatei**, **mediasubtype \_ DTS2** (siehe Hinweis 2)</span><span class="sxs-lookup"><span data-stu-id="51577-141">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DTS2** (See Note 2.)</span></span>
-   <span data-ttu-id="51577-142">**MediaType \_ Audiodatei**, **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="51577-142">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="51577-143">**MediaType \_ Audiodatei**, **mediasubtype \_ DVM** (siehe Hinweis 1)</span><span class="sxs-lookup"><span data-stu-id="51577-143">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVM** (See Note 1.)</span></span>
-   <span data-ttu-id="51577-144">**MediaType \_ Audiodatei**, **mediasubtype \_ MPEG \_ ADTs \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="51577-144">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="51577-145">**MediaType \_ Audiodatei**, **mediasubtype \_ MPEG \_ LoAs**</span><span class="sxs-lookup"><span data-stu-id="51577-145">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>
-   <span data-ttu-id="51577-146">**MediaType \_ Audiodaten**, **mediasubtype \_ MPEG1AudioPayload**</span><span class="sxs-lookup"><span data-stu-id="51577-146">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1AudioPayload**</span></span>
-   <span data-ttu-id="51577-147">**MediaType \_ Audiodatei**, **mediasubtype \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="51577-147">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_RAW\_AAC1**</span></span>
-   <span data-ttu-id="51577-148">**MediaType \_ Stream**, **mediasubtype \_ Dolby \_ ddplus** (siehe Hinweis 1)</span><span class="sxs-lookup"><span data-stu-id="51577-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="51577-149">**MediaType \_ Stream**, **mediasubtype \_ MPEG \_ ADTs \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="51577-149">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="51577-150">**MediaType \_ Stream**, **mediasubtype \_ MPEG \_ LoAs**</span><span class="sxs-lookup"><span data-stu-id="51577-150">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>

<span data-ttu-id="51577-151">Der Eingabetyp kann beim Streaming dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="51577-151">The input type can change dynamically during streaming.</span></span><br/> <span data-ttu-id="51577-152">Weitere Informationen zu diesen Medientypen finden Sie unter [**audiountertypen**](audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="51577-152">For more information about these media types, see [**Audio Subtypes**](audio-subtypes.md).</span></span><br/>

> [!Note]  
> 1. <span data-ttu-id="51577-153">Die Microsoft-Implementierung der Dolby Digital-Technologie ist gemäß den Bedingungen des Dolby Digital Licensing Program eingeschränkt, das von Microsoft-Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51577-153">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

<br/>

> [!Note]  
> 2. <span data-ttu-id="51577-154">Bei der Eingabe von Digital Theater Systems (DTS) werden nur die S/PDIF-Ausgabe unterstützt (DTS over s/PDIF).</span><span class="sxs-lookup"><span data-stu-id="51577-154">For Digital Theater Systems (DTS) input, only S/PDIF output is supported (DTS over S/PDIF).</span></span> <span data-ttu-id="51577-155">Audiodecodierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51577-155">Audio decoding is not supported.</span></span>

<br/>

<span data-ttu-id="51577-156">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="51577-156">Input Pin Interfaces</span></span>

[<span data-ttu-id="51577-157">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="51577-157">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="51577-158">**"Ikspropertyset"**</span><span class="sxs-lookup"><span data-stu-id="51577-158">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="51577-159">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="51577-159">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="51577-160">**IPin**</span><span class="sxs-lookup"><span data-stu-id="51577-160">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="51577-161">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="51577-161">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="51577-162">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="51577-162">Output Pin Media Types</span></span>

<span data-ttu-id="51577-163">In Windows Vista und höher unterstützt der Filter die folgenden Ausgabetypen:</span><span class="sxs-lookup"><span data-stu-id="51577-163">In Windows Vista and later, the filter supports the following output types:</span></span><br/>

-   <span data-ttu-id="51577-164">**MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ AC3 \_ SPDIF** (identisch mit dem **ksdataformat- \_ Untertyp \_ IEC61937 \_ Dolby \_ Digital**)</span><span class="sxs-lookup"><span data-stu-id="51577-164">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3\_SPDIF** (same as **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL**)</span></span>
-   <span data-ttu-id="51577-165">**MediaType \_ Audiodatei**, **mediasubtype \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="51577-165">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="51577-166">Ab Windows 7 unterstützt der Filter auch die folgenden Ausgabetypen:</span><span class="sxs-lookup"><span data-stu-id="51577-166">Starting in Windows 7, the filter also supports the following output types:</span></span><br/>

-   <span data-ttu-id="51577-167">**MediaType \_ Audiotyp**, **ksdataformat- \_ Untertyp \_ IEC61937 \_ DTS**</span><span class="sxs-lookup"><span data-stu-id="51577-167">**MEDIATYPE\_Audio**, **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS**</span></span>
-   <span data-ttu-id="51577-168">**MediaType \_ Audiodatei**, **mediasubtype \_ IEEE \_ float**</span><span class="sxs-lookup"><span data-stu-id="51577-168">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>

<span data-ttu-id="51577-169">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="51577-169">Output Pin Interfaces</span></span>

[<span data-ttu-id="51577-170">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="51577-170">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="51577-171">**IPin**</span><span class="sxs-lookup"><span data-stu-id="51577-171">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="51577-172">**Iqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="51577-172">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="51577-173">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="51577-173">Filter CLSID</span></span>

<span data-ttu-id="51577-174">**CLSID \_ CMPEG2AudDecoderDS** (in wmcodecdsp. h deklariert)</span><span class="sxs-lookup"><span data-stu-id="51577-174">**CLSID\_CMPEG2AudDecoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="51577-175">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="51577-175">Executable</span></span>

<span data-ttu-id="51577-176">msmpeg2adec.dll</span><span class="sxs-lookup"><span data-stu-id="51577-176">msmpeg2adec.dll</span></span>

[<span data-ttu-id="51577-177">Verdienst</span><span class="sxs-lookup"><span data-stu-id="51577-177">Merit</span></span>](merit.md)

<span data-ttu-id="51577-178">**Verdienst \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="51577-178">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="51577-179">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="51577-179">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="51577-180">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="51577-180">**CLSID\_LegacyAmFilterCategory**</span></span>



 

> [!Note]  
> <span data-ttu-id="51577-181">In einer früheren Version der Dokumentation wurde angegeben, dass dieser Filter "MPEG-2-Audiodatei" decodieren kann.</span><span class="sxs-lookup"><span data-stu-id="51577-181">An earlier version of the documentation stated that this filter can decode "MPEG-2 audio."</span></span> <span data-ttu-id="51577-182">Der Filter decodiert nur abwärts kompatible MPEG-2-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="51577-182">The filter decodes only backward-compatible MPEG-2 audio.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="51577-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51577-183">Remarks</span></span>

<span data-ttu-id="51577-184">Mono-Streams werden immer in Stereo decodiert.</span><span class="sxs-lookup"><span data-stu-id="51577-184">Mono streams are always decoded to stereo.</span></span>

<span data-ttu-id="51577-185">Für Streams mit einer Kanal Konfiguration von zwei oder mehr Referenten führt der Decoder einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="51577-185">For streams with a channel configuration of two or more speakers, the decoder does one of the following:</span></span>

-   <span data-ttu-id="51577-186">Up: kombiniert mit der Common 5,1-sprecherkonfiguration für sechs Kanäle.</span><span class="sxs-lookup"><span data-stu-id="51577-186">Up-mixes to six channels, using the common 5.1 speaker configuration.</span></span>
-   <span data-ttu-id="51577-187">Downmix auf Stereo.</span><span class="sxs-lookup"><span data-stu-id="51577-187">Downmixes to stereo.</span></span>

<span data-ttu-id="51577-188">Um zwischen diesen beiden Optionen auszuwählen, legen Sie mit der [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle die [**avdeccommonoutputformat**](avdeccommonoutputformat-property.md) -Eigenschaft fest, bevor Sie die Pins verbinden.</span><span class="sxs-lookup"><span data-stu-id="51577-188">To select between these two options, use the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to set the [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property, before connecting the pins.</span></span> <span data-ttu-id="51577-189">Wenn die Anwendung das Filter Diagramm erstellt, kann Sie alternativ den gewünschten Medientyp in der Ausgabe-PIN festlegen.</span><span class="sxs-lookup"><span data-stu-id="51577-189">Alternatively, when the application builds the filter graph, it can set the desired media type on the output pin.</span></span>

### <a name="aac-decoding"></a><span data-ttu-id="51577-190">AAC-Decodierung</span><span class="sxs-lookup"><span data-stu-id="51577-190">AAC Decoding</span></span>

<span data-ttu-id="51577-191">Bei AAC hat der Decoder bestimmte Format Einschränkungen für die komprimierte AAC-Eingabe.</span><span class="sxs-lookup"><span data-stu-id="51577-191">For AAC, the decoder has certain format constraints on the compressed AAC input.</span></span> <span data-ttu-id="51577-192">Diese Format Einschränkungen sind identisch mit dem Media Foundation [**AAC-Decoder**](../medfound/aac-decoder.md)und sind im Abschnitt "[**Format Einschränkungen**](../medfound/aac-decoder.md)" dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="51577-192">These format constraints are the same as the Media Foundation [**AAC Decoder**](../medfound/aac-decoder.md), and are documented in the section "[**Format Constraints**](../medfound/aac-decoder.md)".</span></span>

<span data-ttu-id="51577-193">Der DirectShow-Decoder akzeptiert auch andere Eingabetypen als der Media Foundation Decoder.</span><span class="sxs-lookup"><span data-stu-id="51577-193">The DirectShow decoder also accepts different input types than the Media Foundation decoder.</span></span> <span data-ttu-id="51577-194">Der DirectShow-Decoder unterstützt die folgenden AAC-Eingabetypen:</span><span class="sxs-lookup"><span data-stu-id="51577-194">The DirectShow decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="51577-195">**Mediasubtype \_ RAW \_ AAC1**: RAW AAC, in der Regel in AVI oder Matroska (. MKV-Dateien).</span><span class="sxs-lookup"><span data-stu-id="51577-195">**MEDIASUBTYPE\_RAW\_AAC1**: Raw AAC, typically found in AVI or Matroska (.MKV) files.</span></span>
-   <span data-ttu-id="51577-196">**Mediasubtype \_ MPEG \_ ADTs \_ AAC**: AAC in einem audiodatentransport-Stream (ADTs) für das Streaming.</span><span class="sxs-lookup"><span data-stu-id="51577-196">**MEDIASUBTYPE\_MPEG\_ADTS\_AAC**: AAC in an Audio Data Transport Stream (ADTS) for streaming.</span></span>
-   <span data-ttu-id="51577-197">**Mediasubtype \_ MPEG \_ LoAs**: Transportstream mit einer Synchronisierungs Schicht (LoAs) und einer Multiplex Schicht (latm).</span><span class="sxs-lookup"><span data-stu-id="51577-197">**MEDIASUBTYPE\_MPEG\_LOAS**: Transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span>

<span data-ttu-id="51577-198">Der Media Foundation-Decoder unterstützt die folgenden AAC-Eingabetypen:</span><span class="sxs-lookup"><span data-stu-id="51577-198">The Media Foundation decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="51577-199">MF Audioformat \_ AAC (identisch mit **mediasubtype \_ MPEG \_ heaac**) für die Wiedergabe von MP4-Dateien.</span><span class="sxs-lookup"><span data-stu-id="51577-199">MFAudioFormat\_AAC (same as **MEDIASUBTYPE\_MPEG\_HEAAC**) for MP4 file playback.</span></span>
-   <span data-ttu-id="51577-200">**Mediasubtype \_ RAW \_ AAC1**.</span><span class="sxs-lookup"><span data-stu-id="51577-200">**MEDIASUBTYPE\_RAW\_AAC1**.</span></span>

### <a name="property-sets"></a><span data-ttu-id="51577-201">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="51577-201">Property Sets</span></span>

<span data-ttu-id="51577-202">Die Eingabe-PIN des Decoders unterstützt die folgenden Eigenschaften Sätze über " [**ikspropertyset**](ikspropertyset.md)":</span><span class="sxs-lookup"><span data-stu-id="51577-202">The decoder's input pin supports the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="51577-203">**Eigenschaften Satz für den DVD-Kopierschutz**</span><span class="sxs-lookup"><span data-stu-id="51577-203">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="51577-204">[**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="51577-204">[**Rate-Change Property Set**](rate-change-property-set.md).</span></span>

> [!Note]  
> <span data-ttu-id="51577-205">Ab Windows 7 unterstützt der Decoder den Trick Modus über den Satz von Eigenschaften für die Raten Änderung.</span><span class="sxs-lookup"><span data-stu-id="51577-205">Starting in Windows 7, the decoder supports trick mode through the rate-change property set.</span></span> <span data-ttu-id="51577-206">Sie unterstützt Wiedergabe Raten im Bereich von \[ 0,501 – 2,0 \] , wobei 1,0 eine normale Wiedergabe Rate und 2,0 den doppelten Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="51577-206">It supports playback rates in the range \[0.501 – 2.0\], where 1.0 is normal playback rate, and 2.0 is twice the normal rate.</span></span>

 

### <a name="codec-properties"></a><span data-ttu-id="51577-207">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51577-207">Codec Properties</span></span>

<span data-ttu-id="51577-208">Die Eingabe-PIN des Decoders unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="51577-208">The decoder's input pin supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="51577-209">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51577-209">Property</span></span>                                                          | <span data-ttu-id="51577-210">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="51577-210">Requires</span></span>                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="51577-211">**Avaudiochannelconfig**</span><span class="sxs-lookup"><span data-stu-id="51577-211">**AVAudioChannelConfig**</span></span>](avaudiochannelconfig-property.md)     | <span data-ttu-id="51577-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-212">Windows Vista</span></span>                                            |
| [<span data-ttu-id="51577-213">**Avaudiochannelcount**</span><span class="sxs-lookup"><span data-stu-id="51577-213">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)       | <span data-ttu-id="51577-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-214">Windows Vista</span></span>                                            |
| [<span data-ttu-id="51577-215">**Avaudiosamplerate**</span><span class="sxs-lookup"><span data-stu-id="51577-215">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)           | <span data-ttu-id="51577-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-216">Windows Vista</span></span>                                            |
| [<span data-ttu-id="51577-217">**Avddsurroundmode**</span><span class="sxs-lookup"><span data-stu-id="51577-217">**AVDDSurroundMode**</span></span>](avddsurroundmode-property.md)             | <span data-ttu-id="51577-218">Nur Windows Vista; wird in Windows 7 oder höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51577-218">Windows Vista only; not supported in Windows 7 or later.</span></span> |
| [<span data-ttu-id="51577-219">**Avdecaudiodualmono**</span><span class="sxs-lookup"><span data-stu-id="51577-219">**AVDecAudioDualMono**</span></span>](avdecaudiodualmono-property.md)         | <span data-ttu-id="51577-220">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-220">Windows Vista</span></span>                                            |
| [<span data-ttu-id="51577-221">**Avdeccommoninputformat**</span><span class="sxs-lookup"><span data-stu-id="51577-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md) | <span data-ttu-id="51577-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-222">Windows Vista</span></span>                                            |
| [<span data-ttu-id="51577-223">**Avdeccommonmeanbitrate**</span><span class="sxs-lookup"><span data-stu-id="51577-223">**AVDecCommonMeanBitRate**</span></span>](avdeccommonmeanbitrate.md)          | <span data-ttu-id="51577-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51577-224">Windows 7</span></span>                                                |



 

<span data-ttu-id="51577-225">Der Filter unterstützt die folgenden Eigenschaften über [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="51577-225">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="51577-226">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51577-226">Property</span></span>                                                                          | <span data-ttu-id="51577-227">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="51577-227">Requires</span></span>      |
|-----------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="51577-228">**Avdecaacdownmixmode**</span><span class="sxs-lookup"><span data-stu-id="51577-228">**AVDecAACDownmixMode**</span></span>](avdecaacdownmixmode-property.md)                       | <span data-ttu-id="51577-229">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51577-229">Windows 7</span></span>     |
| [<span data-ttu-id="51577-230">**Avdecaudiodualmonorepromode**</span><span class="sxs-lookup"><span data-stu-id="51577-230">**AVDecAudioDualMonoReproMode**</span></span>](avdecaudiodualmonorepromode-property.md)       | <span data-ttu-id="51577-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-231">Windows Vista</span></span> |
| <span data-ttu-id="51577-232">[**Avdeccommonoutputformat**](avdeccommonoutputformat-property.md) (siehe Hinweis 3)</span><span class="sxs-lookup"><span data-stu-id="51577-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (See Note 3.)</span></span> | <span data-ttu-id="51577-233">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-233">Windows Vista</span></span> |
| [<span data-ttu-id="51577-234">**Avdecdddynamicrangescalehigh**</span><span class="sxs-lookup"><span data-stu-id="51577-234">**AVDecDDDynamicRangeScaleHigh**</span></span>](avdecdddynamicrangescalehigh-property.md)     | <span data-ttu-id="51577-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-235">Windows Vista</span></span> |
| [<span data-ttu-id="51577-236">**Avdecdddynamicrangescalelow**</span><span class="sxs-lookup"><span data-stu-id="51577-236">**AVDecDDDynamicRangeScaleLow**</span></span>](avdecdddynamicrangescalelow-property.md)       | <span data-ttu-id="51577-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-237">Windows Vista</span></span> |
| [<span data-ttu-id="51577-238">**Avdecddoperationalmode**</span><span class="sxs-lookup"><span data-stu-id="51577-238">**AVDecDDOperationalMode**</span></span>](avdecddoperationalmode-property.md)                 | <span data-ttu-id="51577-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-239">Windows Vista</span></span> |
| [<span data-ttu-id="51577-240">**Avdecmmcssclass**</span><span class="sxs-lookup"><span data-stu-id="51577-240">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                    | <span data-ttu-id="51577-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51577-241">Windows Vista</span></span> |
| [<span data-ttu-id="51577-242">**Avdsploudnesabqualization**</span><span class="sxs-lookup"><span data-stu-id="51577-242">**AVDSPLoudnessEqualization**</span></span>](avdsploudnessequalization-property.md)           | <span data-ttu-id="51577-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51577-243">Windows 7</span></span>     |
| [<span data-ttu-id="51577-244">**Avdspspeakerfill**</span><span class="sxs-lookup"><span data-stu-id="51577-244">**AVDSPSpeakerFill**</span></span>](avdspspeakerfill-property.md)                             | <span data-ttu-id="51577-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51577-245">Windows 7</span></span>     |



 

> [!Note]  
> 3. <span data-ttu-id="51577-246">Die [**avdeccommonoutputformat**](avdeccommonoutputformat-property.md) -Eigenschaft muss festgelegt werden, bevor die Ausgabe-PIN des Decoders verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="51577-246">The [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property must be set before the decoder's output pin is connected.</span></span> <span data-ttu-id="51577-247">Andernfalls hat die Änderung keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="51577-247">Otherwise, the change has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51577-248">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51577-248">Requirements</span></span>



| <span data-ttu-id="51577-249">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51577-249">Requirement</span></span> | <span data-ttu-id="51577-250">Wert</span><span class="sxs-lookup"><span data-stu-id="51577-250">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51577-251">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51577-251">Minimum supported client</span></span><br/> | <span data-ttu-id="51577-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51577-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51577-253">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51577-253">Minimum supported server</span></span><br/> | <span data-ttu-id="51577-254">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="51577-254">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="51577-255">Header</span><span class="sxs-lookup"><span data-stu-id="51577-255">Header</span></span><br/>                   | <dl> <span data-ttu-id="51577-256"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="51577-256"><dt>Wmcodecdsp.h</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="51577-257">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51577-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51577-258">**Audiountertypen**</span><span class="sxs-lookup"><span data-stu-id="51577-258">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="51577-259">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="51577-259">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="51577-260">**DVD-Medientypen**</span><span class="sxs-lookup"><span data-stu-id="51577-260">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> </dl>

 

 
