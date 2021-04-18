---
description: Der Video Decoder Media Foundation H. 264 ist eine Media Foundation Transformation, die die Decodierung von Baseline, Main und High Profile bis zu Ebene 5,1 unterstützt.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: H. 264-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484054"
---
# <a name="h264-video-decoder"></a><span data-ttu-id="eeb38-103">H. 264-Video Decoder</span><span class="sxs-lookup"><span data-stu-id="eeb38-103">H.264 Video Decoder</span></span>

<span data-ttu-id="eeb38-104">Der Video Decoder Media Foundation H. 264 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die die Decodierung von Baseline, Main und High Profile bis zu Ebene 5,1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eeb38-104">The Media Foundation H.264 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span>

<span data-ttu-id="eeb38-105">Der H. 264-Video Decoder macht die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eeb38-105">The H.264 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="eeb38-106">[**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) (unterstützt in Windows 8)</span><span class="sxs-lookup"><span data-stu-id="eeb38-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="eeb38-107">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="eeb38-107">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="eeb38-108">**IMF-Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="eeb38-108">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="eeb38-109">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="eeb38-109">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="eeb38-110">**Imfratecontrol**</span><span class="sxs-lookup"><span data-stu-id="eeb38-110">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="eeb38-111">**Imfratesupport**</span><span class="sxs-lookup"><span data-stu-id="eeb38-111">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="eeb38-112">**Imfrealtimeclient**</span><span class="sxs-lookup"><span data-stu-id="eeb38-112">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="eeb38-113">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="eeb38-113">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="eeb38-114">Führen Sie eine der folgenden Aktionen aus, um eine Instanz des Decoders zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="eeb38-114">To create an instance of the decoder, do one of the following:</span></span>

-   <span data-ttu-id="eeb38-115">Ruft die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="eeb38-115">Call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>
-   <span data-ttu-id="eeb38-116">[**Cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eeb38-116">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="eeb38-117">Die CLSID für den Decoder ist **CLSID \_ CMSH264DecoderMFT**, deklariert in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="eeb38-117">The CLSID for the decoder is **CLSID\_CMSH264DecoderMFT**, declared in wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="eeb38-118">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="eeb38-118">Input Types</span></span>

<span data-ttu-id="eeb38-119">Der Eingabetyp muss mindestens die beiden folgenden Attribute enthalten:</span><span class="sxs-lookup"><span data-stu-id="eeb38-119">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="eeb38-120">Attribut</span><span class="sxs-lookup"><span data-stu-id="eeb38-120">Attribute</span></span>                                                 | <span data-ttu-id="eeb38-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb38-121">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeb38-122">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eeb38-122">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="eeb38-123">**MF MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="eeb38-123">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="eeb38-124">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="eeb38-124">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="eeb38-125">[MF-Format \_ H264 oder](video-subtype-guids.md) MF-Format \_ H264 \_ es</span><span class="sxs-lookup"><span data-stu-id="eeb38-125">[MFVideoFormat\_H264](video-subtype-guids.md) or MFVideoFormat\_H264\_ES</span></span> |



 

<span data-ttu-id="eeb38-126">Wenn der Eingabetyp nur diese beiden Attribute enthält, bietet der Decoder einen Standard Ausgabetyp an, der als Platzhalter fungiert.</span><span class="sxs-lookup"><span data-stu-id="eeb38-126">If the input type contains only these two attributes, the decoder will offer a default output type, which acts as a placeholder.</span></span> <span data-ttu-id="eeb38-127">Wenn der Decoder genügend Eingabe Beispiele empfängt, um einen Ausgabe Rahmen zu schaffen, signalisiert er eine Formatänderung, indem er die **Änderung von MF \_ E \_ Transform \_ \_ Stream** von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eeb38-127">When the decoder receives enough input samples to produce an output frame, it signals a format change by returning **MF\_E\_TRANSFORM\_STREAM\_CHANGE** from [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="eeb38-128">Ausführliche Informationen zur Behandlung von Formatänderungen finden Sie in der **ProcessOutput** -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="eeb38-128">See the **ProcessOutput** documentation for details about handling format changes.</span></span>

<span data-ttu-id="eeb38-129">Um eine anfängliche Formatänderung zu vermeiden, geben Sie so viele Informationen wie möglich im Eingabetyp an, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="eeb38-129">To avoid an initial format change, provide as much information in the input type as possible, including:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eeb38-130">Attribut</span><span class="sxs-lookup"><span data-stu-id="eeb38-130">Attribute</span></span></th>
<th><span data-ttu-id="eeb38-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb38-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eeb38-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeb38-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="eeb38-133">Die Framerate.</span><span class="sxs-lookup"><span data-stu-id="eeb38-133">Frame rate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeb38-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeb38-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="eeb38-135">Frame Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="eeb38-135">Frame dimensions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeb38-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeb38-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="eeb38-137">Interlace-Modus.</span><span class="sxs-lookup"><span data-stu-id="eeb38-137">Interlace mode.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="eeb38-138">In H. 264-Video kann sich die damit-Struktur dynamisch ändern, sodass der empfohlene Wert dieses Attributs <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="eeb38-138">In H.264 video, the interlace structure can change dynamically, so the recommended value of this attribute is <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span></span> <span data-ttu-id="eeb38-139">Interlace-Informationen im Video-elementaren Stream haben Vorrang vor dem Medientyp.</span><span class="sxs-lookup"><span data-stu-id="eeb38-139">Interlace information in the video elementary stream takes precedence over the media type.</span></span> <span data-ttu-id="eeb38-140">Weitere Informationen finden Sie unter <a href="video-interlacing.md">Video Interlacing</a>.</span><span class="sxs-lookup"><span data-stu-id="eeb38-140">For more information, see <a href="video-interlacing.md">Video Interlacing</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeb38-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeb38-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="eeb38-142">Pixel Seitenverhältnis.</span><span class="sxs-lookup"><span data-stu-id="eeb38-142">Pixel aspect ratio.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="eeb38-143">Der Eingabetyp muss vor dem Ausgabetyp festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eeb38-143">The input type must be set before the output type.</span></span> <span data-ttu-id="eeb38-144">Bis der Eingabetyp festgelegt ist, gibt die [**IMF Transform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode des Encoders einen **\_ \_ \_ \_ nicht \_ festgelegten MF E-Transformationstyp** zurück.</span><span class="sxs-lookup"><span data-stu-id="eeb38-144">Until the input type is set, the encoder's [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="eeb38-145">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="eeb38-145">Output Types</span></span>

<span data-ttu-id="eeb38-146">Der Decoder unterstützt die folgenden Ausgabe Untertypen:</span><span class="sxs-lookup"><span data-stu-id="eeb38-146">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="eeb38-147">**MF-Format \_ I420**</span><span class="sxs-lookup"><span data-stu-id="eeb38-147">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="eeb38-148">**MF-Format ( \_ IYUV)**</span><span class="sxs-lookup"><span data-stu-id="eeb38-148">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="eeb38-149">**MF-Format \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="eeb38-149">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="eeb38-150">**MF-Format \_ im YUY2**</span><span class="sxs-lookup"><span data-stu-id="eeb38-150">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="eeb38-151">**MF-Format \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="eeb38-151">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="eeb38-152">Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="eeb38-152">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="eeb38-153">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="eeb38-153">Transform Attributes</span></span>

<span data-ttu-id="eeb38-154">Der H. 264-Decoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eeb38-154">The H.264 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="eeb38-155">Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="eeb38-155">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="eeb38-156">Attribut</span><span class="sxs-lookup"><span data-stu-id="eeb38-156">Attribute</span></span>                                                                                       | <span data-ttu-id="eeb38-157">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb38-157">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeb38-158">Codecapi \_ avdecvideoacceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="eeb38-158">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="eeb38-159">Aktiviert oder deaktiviert die Hardwarebeschleunigung.</span><span class="sxs-lookup"><span data-stu-id="eeb38-159">Enables or disables hardware acceleration.</span></span>                                                 |
| [<span data-ttu-id="eeb38-160">Codecapi \_ avdecvideothumbnailgenerationmode</span><span class="sxs-lookup"><span data-stu-id="eeb38-160">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="eeb38-161">Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="eeb38-161">Enables or disables thumbnail generation mode.</span></span>                                             |
| [<span data-ttu-id="eeb38-162">MF \_ sa \_ D3D \_</span><span class="sxs-lookup"><span data-stu-id="eeb38-162">MF\_SA\_D3D\_AWARE</span></span>](mf-sa-d3d-aware-attribute.md)                                             | <span data-ttu-id="eeb38-163">Gibt an, dass der Decoder die DirectX-Video Beschleunigung (DXVA) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eeb38-163">Indicates that the decoder supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="eeb38-164">Als schreibgeschützt behandeln.</span><span class="sxs-lookup"><span data-stu-id="eeb38-164">Treat as read-only.</span></span> |



 

<span data-ttu-id="eeb38-165">In Windows 8 unterstützt der H. 264-Decoder auch die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="eeb38-165">In Windows 8, the H.264 decoder also supports the following attributes.</span></span>



| <span data-ttu-id="eeb38-166">Attribut</span><span class="sxs-lookup"><span data-stu-id="eeb38-166">Attribute</span></span>                                                                                                     | <span data-ttu-id="eeb38-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb38-167">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeb38-168">Codecapi \_ avlowlatencymode</span><span class="sxs-lookup"><span data-stu-id="eeb38-168">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="eeb38-169">Aktiviert oder deaktiviert den Decodierungs Modus mit niedriger Latenz.</span><span class="sxs-lookup"><span data-stu-id="eeb38-169">Enables or disables low-latency decoding mode.</span></span>                                                              |
| [<span data-ttu-id="eeb38-170">Codecapi \_ avdecnumworkerthreads</span><span class="sxs-lookup"><span data-stu-id="eeb38-170">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                                         | <span data-ttu-id="eeb38-171">Legt die Anzahl von Arbeitsthreads fest, die vom Decoder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eeb38-171">Sets the number of worker threads used by the decoder.</span></span>                                                      |
| [<span data-ttu-id="eeb38-172">Codecapi \_ avdecvideomaxcodedwidth</span><span class="sxs-lookup"><span data-stu-id="eeb38-172">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)                                     | <span data-ttu-id="eeb38-173">Legt die maximale Bildbreite fest, die der Decoder als Eingabetyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="eeb38-173">Sets the maximum picture width that the decoder will accept as an input type.</span></span>                               |
| [<span data-ttu-id="eeb38-174">Codecapi \_ avdecvideomaxcodedheight</span><span class="sxs-lookup"><span data-stu-id="eeb38-174">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)                                   | <span data-ttu-id="eeb38-175">Legt die maximale Bildhöhe fest, die der Decoder als Eingabetyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="eeb38-175">Sets the maximum picture height that the decoder will accept as an input type.</span></span>                              |
| [<span data-ttu-id="eeb38-176">\_Anzahl der \_ minimalen \_ Ausgabe \_ Beispiele \_ für MF-SA</span><span class="sxs-lookup"><span data-stu-id="eeb38-176">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                               | <span data-ttu-id="eeb38-177">Gibt die maximale Anzahl von Ausgabe Beispielen an.</span><span class="sxs-lookup"><span data-stu-id="eeb38-177">Specifies the maximum number of output samples.</span></span>                                                             |
| [<span data-ttu-id="eeb38-178">MFT- \_ Decoder macht \_ \_ Ausgabe \_ Typen \_ in \_ nativer \_ Reihenfolge verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eeb38-178">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="eeb38-179">Gibt an, ob ein Decoder vor anderen Formaten IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="eeb38-179">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span> |



 

<span data-ttu-id="eeb38-180">In Windows 8 unterstützt der H. 264-Decoder die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eeb38-180">In Windows 8, the H.264 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="eeb38-181">Diese Schnittstelle bietet eine alternativate-API zum Festlegen der folgenden Codec-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eeb38-181">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="eeb38-182">Codecapi \_ avdecvideomaxcodedwidth</span><span class="sxs-lookup"><span data-stu-id="eeb38-182">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="eeb38-183">Codecapi \_ avdecvideoacceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="eeb38-183">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)
-   [<span data-ttu-id="eeb38-184">Codecapi \_ avdecvideomaxcodedheight</span><span class="sxs-lookup"><span data-stu-id="eeb38-184">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)
-   [<span data-ttu-id="eeb38-185">Codecapi \_ avdecvideomaxcodedwidth</span><span class="sxs-lookup"><span data-stu-id="eeb38-185">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="eeb38-186">Codecapi \_ avdecvideothumbnailgenerationmode</span><span class="sxs-lookup"><span data-stu-id="eeb38-186">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a><span data-ttu-id="eeb38-187">Format Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="eeb38-187">Format Constraints</span></span>

<span data-ttu-id="eeb38-188">Der Decoder unterstützt die folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="eeb38-188">The decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eeb38-189">Profile/Ebenen</span><span class="sxs-lookup"><span data-stu-id="eeb38-189">Profiles/Levels</span></span></td>
<td><span data-ttu-id="eeb38-190">Baseline, Main und High Profile, bis zu Ebene 5,1.</span><span class="sxs-lookup"><span data-stu-id="eeb38-190">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="eeb38-191">(Ausführliche Informationen finden Sie in der ITU-T H. 264-Spezifikation.)</span><span class="sxs-lookup"><span data-stu-id="eeb38-191">(See ITU-T H.264 specification for details.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeb38-192">Chroma-Formate</span><span class="sxs-lookup"><span data-stu-id="eeb38-192">Chroma Formats</span></span></td>
<td><span data-ttu-id="eeb38-193">4:2:0 Chroma oder Monochrom</span><span class="sxs-lookup"><span data-stu-id="eeb38-193">4:2:0 chroma or monochrome</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeb38-194">Minimale Auflösung</span><span class="sxs-lookup"><span data-stu-id="eeb38-194">Minimum Resolution</span></span></td>
<td><span data-ttu-id="eeb38-195">48 × 48 Pixel</span><span class="sxs-lookup"><span data-stu-id="eeb38-195">48 × 48 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeb38-196">Maximale Auflösung</span><span class="sxs-lookup"><span data-stu-id="eeb38-196">Maximum Resolution</span></span></td>
<td><span data-ttu-id="eeb38-197">4096 × 2304 Pixel</span><span class="sxs-lookup"><span data-stu-id="eeb38-197">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="eeb38-198">Die maximale garantierte Auflösung der DXVA-Beschleunigung beträgt 1920 × 1088 Pixel. bei höherer Auflösung erfolgt die Decodierung mit DXVA, wenn Sie von der zugrunde liegenden Hardware unterstützt wird. andernfalls erfolgt die Decodierung mit Software.</span><span class="sxs-lookup"><span data-stu-id="eeb38-198">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eeb38-199">In Windows 7 ist die maximal unterstützte Auflösung 1920 × 1088 Pixel für die Software-und DXVA-Decodierung.</span><span class="sxs-lookup"><span data-stu-id="eeb38-199">In Windows 7, the maximum supported resolution is 1920 × 1088 pixels for both software and DXVA decoding.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeb38-200">DXVA</span><span class="sxs-lookup"><span data-stu-id="eeb38-200">DXVA</span></span></td>
<td><span data-ttu-id="eeb38-201">Der Decoder unterstützt DXVA Version 2, aber nicht DXVA Version 1.</span><span class="sxs-lookup"><span data-stu-id="eeb38-201">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="eeb38-202">DXVA-Decodierung wird nur für Haupt kompatible Bitstreams, Main und High Profile unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eeb38-202">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="eeb38-203">(Haupt-kompatible Baseline-Bitstreams werden als <strong>profile_idc</strong>= 66 und <strong>constrained_set1_flag</strong>= 1 definiert.)</span><span class="sxs-lookup"><span data-stu-id="eeb38-203">(Main-compatible Baseline bitstreams are defined as <strong>profile_idc</strong>=66 and <strong>constrained_set1_flag</strong>=1.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="eeb38-204">Eingabedaten müssen dem Anhang B ISO/IEC 14496-10 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="eeb38-204">Input data must conform to Annex B of ISO/IEC 14496-10.</span></span> <span data-ttu-id="eeb38-205">Die Daten müssen die Start Codes enthalten.</span><span class="sxs-lookup"><span data-stu-id="eeb38-205">The data must include the start codes.</span></span> <span data-ttu-id="eeb38-206">Der Decoder überspringt bytes, bis ein gültiger Sequenz Parametersatz (SPS) und ein Bildparameter Satz (PPS) im Bytestream gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="eeb38-206">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

<span data-ttu-id="eeb38-207">Der Decoder bietet keine Unterstützung für die Technologie zum Filmen von Folien.</span><span class="sxs-lookup"><span data-stu-id="eeb38-207">The decoder does not support Film Grain Technology.</span></span>

> [!Note]  
> <span data-ttu-id="eeb38-208">In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass der Decoder auf Windows Server 2008 R2 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="eeb38-208">A previous version of the documentation incorrectly stated that the decoder is supported on Windows Server 2008 R2.</span></span>

 

<span data-ttu-id="eeb38-209">Wenn die Ergänzung zum Platt Form Update für Windows Vista installiert ist, steht der H. 264-Video Decoder unter Windows Vista zur Verfügung. der Zugriff auf Windows Vista ist jedoch nur mithilfe des [Quell Readers](source-reader.md)möglich.</span><span class="sxs-lookup"><span data-stu-id="eeb38-209">If Platform Update Supplement for Windows Vista is installed, the H.264 video decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb38-210">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eeb38-210">Requirements</span></span>



| <span data-ttu-id="eeb38-211">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eeb38-211">Requirement</span></span> | <span data-ttu-id="eeb38-212">Wert</span><span class="sxs-lookup"><span data-stu-id="eeb38-212">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb38-213">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eeb38-213">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb38-214">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eeb38-214">Windows 7 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eeb38-215">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eeb38-215">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb38-216">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eeb38-216">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="eeb38-217">DLL</span><span class="sxs-lookup"><span data-stu-id="eeb38-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeb38-218"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeb38-218"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeb38-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eeb38-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb38-220">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="eeb38-220">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="eeb38-221">MPEG-4-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eeb38-221">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="eeb38-222">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eeb38-222">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="eeb38-223">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="eeb38-223">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
