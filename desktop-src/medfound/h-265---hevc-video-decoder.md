---
description: Der Video Decoder Media Foundation H. 265 ist eine Media Foundation Transformation, die das Decodieren von H. 265/hevc-Inhalten im Anhang B-Format unterstützt und für die Wiedergabe von MP4-und M2TS-Dateien verwendet werden kann.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: H. 265/hevc-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527698"
---
# <a name="h265--hevc-video-decoder"></a><span data-ttu-id="7348a-103">H. 265/hevc-Video Decoder</span><span class="sxs-lookup"><span data-stu-id="7348a-103">H.265 / HEVC Video Decoder</span></span>

<span data-ttu-id="7348a-104">Der Video Decoder Media Foundation H. 265 ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die das Decodieren von H. 265/hevc-Inhalten im Anhang B-Format unterstützt und für die Wiedergabe von MP4-und M2TS-Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7348a-104">The Media Foundation H.265 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span>

<span data-ttu-id="7348a-105">Der H. 265-Video Decoder macht die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7348a-105">The H.265 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="7348a-106">[**Icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) (unterstützt in Windows 8)</span><span class="sxs-lookup"><span data-stu-id="7348a-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="7348a-107">**Imfattributes**</span><span class="sxs-lookup"><span data-stu-id="7348a-107">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="7348a-108">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="7348a-108">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="7348a-109">**IMF-Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="7348a-109">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="7348a-110">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="7348a-110">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="7348a-111">**Imfratecontrol**</span><span class="sxs-lookup"><span data-stu-id="7348a-111">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="7348a-112">**Imfratesupport**</span><span class="sxs-lookup"><span data-stu-id="7348a-112">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="7348a-113">**Imfrealtimeclient**</span><span class="sxs-lookup"><span data-stu-id="7348a-113">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="7348a-114">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="7348a-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="7348a-115">Um eine Instanz des Decoders zu erstellen, rufen Sie die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="7348a-115">To create an instance of the decoder call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="input-types"></a><span data-ttu-id="7348a-116">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="7348a-116">Input Types</span></span>

<span data-ttu-id="7348a-117">Der Eingabetyp muss mindestens die beiden folgenden Attribute enthalten:</span><span class="sxs-lookup"><span data-stu-id="7348a-117">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="7348a-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="7348a-118">Attribute</span></span>                                                 | <span data-ttu-id="7348a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7348a-119">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7348a-120">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7348a-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="7348a-121">**MF MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="7348a-121">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="7348a-122">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="7348a-122">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="7348a-123">[MF-Format \_ Hevc oder](video-subtype-guids.md) MF-Format \_ hevc \_ es</span><span class="sxs-lookup"><span data-stu-id="7348a-123">[MFVideoFormat\_HEVC](video-subtype-guids.md) or MFVideoFormat\_HEVC\_ES</span></span> |



 

<span data-ttu-id="7348a-124">Der erste Medien Untertyp, MF Videoformat \_ hevc, gibt an, dass die Medien Beispiele den H. 265-Bitstrom mit Start Codes enthalten und der Stream überlappende SPS/PPS verfügt.</span><span class="sxs-lookup"><span data-stu-id="7348a-124">The first media subtype, MFVideoFormat\_HEVC, indicates that the media samples carry H.265 bitstream with start codes, and the stream has interleaved SPS/PPS.</span></span> <span data-ttu-id="7348a-125">Es wird von einem Frame pro Stichprobe ausgegangen.</span><span class="sxs-lookup"><span data-stu-id="7348a-125">It assumes one frame per sample.</span></span>

<span data-ttu-id="7348a-126">Der Medien Untertyp mfvideoformat \_ hevc \_ es gibt an, dass die Medien Beispiele einen elementaren H. 265-Bitstream enthalten, wobei jedes Beispiel ein partielles Bild, mehrere Bilder, einige Bilder und ein partielles Bild enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="7348a-126">The media subtype MFVideoFormat\_ HEVC\_ES is to indicate the media samples carry elementary H.265 bitstream, where each sample may contain a partial picture, multiple pictures, some pictures plus a partial picture.</span></span>

<span data-ttu-id="7348a-127">Die Eingabemedien Typen können sich nicht dynamisch zwischen zwei Typen ändern.</span><span class="sxs-lookup"><span data-stu-id="7348a-127">The input media types cannot change dynamically between two types.</span></span> <span data-ttu-id="7348a-128">Der Decoder kann in-Flight-Ausgabeformat Änderungen auf der Grundlage der elementaren Datenstrom Syntax (Seitenverhältnis, Dimension, damit-Flags, farbige metrieinformationen) erkennen und entsprechende Änderungen des Ausgabemedien Typs auslöst.</span><span class="sxs-lookup"><span data-stu-id="7348a-128">The decoder can detect in-flight output format changes based on the elementary stream syntax (aspect ratio, dimension, interlace flags, colorimetry information) and trigger corresponding output media type changes.</span></span>

<span data-ttu-id="7348a-129">Für den Eingabe Medientyp erwartet der Decoder, dass die Quelle das korrekte Profil festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="7348a-129">For input media type, the decoder expects the source to set the correct Profile.</span></span> <span data-ttu-id="7348a-130">Wenn der Inhalt beispielsweise 10bit sein wird, sollte der Eingabe Medientyp das Profil als Main10 angeben.</span><span class="sxs-lookup"><span data-stu-id="7348a-130">For example if the content is going to be 10bit, input media type should specify the profile as Main10.</span></span>

## <a name="output-types"></a><span data-ttu-id="7348a-131">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="7348a-131">Output Types</span></span>

<span data-ttu-id="7348a-132">Der Decoder unterstützt die folgenden Ausgabe Untertypen:</span><span class="sxs-lookup"><span data-stu-id="7348a-132">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="7348a-133">**MF-Format \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="7348a-133">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="7348a-134">**MF-Format \_ P010**</span><span class="sxs-lookup"><span data-stu-id="7348a-134">**MFVideoFormat\_P010**</span></span>

<span data-ttu-id="7348a-135">Weitere Informationen zu diesen Untertypen finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7348a-135">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="7348a-136">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="7348a-136">Transform Attributes</span></span>

<span data-ttu-id="7348a-137">Der H. 265-Decoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7348a-137">The H.265 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="7348a-138">Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7348a-138">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="7348a-139">Attribut</span><span class="sxs-lookup"><span data-stu-id="7348a-139">Attribute</span></span>                                                                                       | <span data-ttu-id="7348a-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7348a-140">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7348a-141">Codecapi \_ avlowlatencymode</span><span class="sxs-lookup"><span data-stu-id="7348a-141">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                     | <span data-ttu-id="7348a-142">Aktiviert oder deaktiviert den Decodierungs Modus mit niedriger Latenz.</span><span class="sxs-lookup"><span data-stu-id="7348a-142">Enables or disables low-latency decoding mode.</span></span>                                                                                |
| [<span data-ttu-id="7348a-143">Codecapi \_ avdecnumworkerthreads</span><span class="sxs-lookup"><span data-stu-id="7348a-143">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                           | <span data-ttu-id="7348a-144">Legt die Anzahl von Arbeitsthreads fest, die vom Decoder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7348a-144">Sets the number of worker threads used by the decoder.</span></span>                                                                        |
| [<span data-ttu-id="7348a-145">Codecapi \_ avdecvideothumbnailgenerationmode</span><span class="sxs-lookup"><span data-stu-id="7348a-145">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="7348a-146">Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="7348a-146">Enables or disables thumbnail generation mode.</span></span>                                                                                |
| [<span data-ttu-id="7348a-147">Länge der MF- \_ Nalu- \_ Länge \_</span><span class="sxs-lookup"><span data-stu-id="7348a-147">MF\_NALU\_LENGTH\_SET</span></span>](mf-nalu-length-set.md)                                                 | <span data-ttu-id="7348a-148">Gibt an, dass Nalu-Längen Informationen als BLOB mit jedem komprimierten H. 265-Beispiel gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7348a-148">Indicates that NALU length information will be sent as a BLOB with each compressed H.265 sample.</span></span>                              |
| [<span data-ttu-id="7348a-149">Informationen zur Länge der MF- \_ Nalu \_ \_</span><span class="sxs-lookup"><span data-stu-id="7348a-149">MF\_NALU\_LENGTH\_INFORMATION</span></span>](mf-nalu-length-information.md)                                 | <span data-ttu-id="7348a-150">Gibt die Länge von nalus in der Stichprobe an.</span><span class="sxs-lookup"><span data-stu-id="7348a-150">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="7348a-151">Hierbei handelt es sich um ein MF-BLOB, das auf komprimierte Eingabe Beispiele für den H. 265-Decoder festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7348a-151">This is a MF BLOB that is set on compressed input samples to the H.265 decoder.</span></span> |
| [<span data-ttu-id="7348a-152">\_Anzahl der \_ minimalen \_ Ausgabe \_ Beispiele \_ für MF-SA</span><span class="sxs-lookup"><span data-stu-id="7348a-152">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                 | <span data-ttu-id="7348a-153">Gibt die maximale Anzahl von Ausgabe Beispielen an.</span><span class="sxs-lookup"><span data-stu-id="7348a-153">Specifies the maximum number of output samples.</span></span>                                                                               |



 

<span data-ttu-id="7348a-154">Der H. 265-Decoder unterstützt die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7348a-154">The H.265 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="7348a-155">Diese Schnittstelle bietet eine alternativate-API zum Festlegen der folgenden Codec-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7348a-155">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="7348a-156">Codecapi \_ avdecnumworkerthreads</span><span class="sxs-lookup"><span data-stu-id="7348a-156">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)
-   [<span data-ttu-id="7348a-157">Codecapi \_ avdecvideothumbnailgenerationmode</span><span class="sxs-lookup"><span data-stu-id="7348a-157">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="7348a-158">Codecapi \_ avlowlatencymode</span><span class="sxs-lookup"><span data-stu-id="7348a-158">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a><span data-ttu-id="7348a-159">Format Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="7348a-159">Format Constraints</span></span>

<span data-ttu-id="7348a-160">Der Decoder unterstützt die folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="7348a-160">The decoder supports the following formats:</span></span>



| <span data-ttu-id="7348a-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7348a-161">Requirement</span></span> | <span data-ttu-id="7348a-162">Wert</span><span class="sxs-lookup"><span data-stu-id="7348a-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7348a-163">Profile/Ebenen</span><span class="sxs-lookup"><span data-stu-id="7348a-163">Profiles/Levels</span></span>    | <span data-ttu-id="7348a-164">Haupt-, Haupt Bild-und Main10-profile</span><span class="sxs-lookup"><span data-stu-id="7348a-164">Main, Main Still Picture, and Main10 profiles</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="7348a-165">Chroma-Formate</span><span class="sxs-lookup"><span data-stu-id="7348a-165">Chroma Formats</span></span>     | <span data-ttu-id="7348a-166">4:2:0 Chroma</span><span class="sxs-lookup"><span data-stu-id="7348a-166">4:2:0 chroma</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7348a-167">Minimale Auflösung</span><span class="sxs-lookup"><span data-stu-id="7348a-167">Minimum Resolution</span></span> | <span data-ttu-id="7348a-168">48 × 48 Pixel</span><span class="sxs-lookup"><span data-stu-id="7348a-168">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7348a-169">Maximale Auflösung</span><span class="sxs-lookup"><span data-stu-id="7348a-169">Maximum Resolution</span></span> | <span data-ttu-id="7348a-170">4096 × 2304 Pixel</span><span class="sxs-lookup"><span data-stu-id="7348a-170">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="7348a-171">Die maximale garantierte Auflösung der DXVA-Beschleunigung beträgt 1920 × 1088 Pixel. bei höherer Auflösung erfolgt die Decodierung mit DXVA, wenn Sie von der zugrunde liegenden Hardware unterstützt wird. andernfalls erfolgt die Decodierung mit Software.</span><span class="sxs-lookup"><span data-stu-id="7348a-171">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/> |
| <span data-ttu-id="7348a-172">DXVA</span><span class="sxs-lookup"><span data-stu-id="7348a-172">DXVA</span></span>               | <span data-ttu-id="7348a-173">Der Decoder unterstützt DX11 und DX12 DXVA, aber nicht DXVA Version 2 oder DXVA Version 1.</span><span class="sxs-lookup"><span data-stu-id="7348a-173">The decoder supports DX11 and DX12 DXVA, but not DXVA version 2 or DXVA version 1.</span></span>                                                                                                                                                                                                         |



 

<span data-ttu-id="7348a-174">Eingabedaten müssen dem Anhang B des ITU-T H. 265 \| ISO/IEC 23008-2 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7348a-174">Input data must conform to Annex B of ITU-T H.265 \| ISO/IEC 23008-2.</span></span> <span data-ttu-id="7348a-175">Die Daten müssen die Start Codes enthalten.</span><span class="sxs-lookup"><span data-stu-id="7348a-175">The data must include the start codes.</span></span> <span data-ttu-id="7348a-176">Der Decoder überspringt bytes, bis ein gültiger Sequenz Parametersatz (SPS) und ein Bildparameter Satz (PPS) im Bytestream gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7348a-176">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="7348a-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7348a-177">Requirements</span></span>



| <span data-ttu-id="7348a-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7348a-178">Requirement</span></span> | <span data-ttu-id="7348a-179">Wert</span><span class="sxs-lookup"><span data-stu-id="7348a-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7348a-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7348a-180">Minimum supported client</span></span><br/> | <span data-ttu-id="7348a-181">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7348a-181">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7348a-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7348a-182">Minimum supported server</span></span><br/> | <span data-ttu-id="7348a-183">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7348a-183">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7348a-184">DLL</span><span class="sxs-lookup"><span data-stu-id="7348a-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7348a-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7348a-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7348a-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7348a-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7348a-187">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="7348a-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
