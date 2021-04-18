---
description: Der MPEG-2-Video Decoder ist eine Media Foundation Transformation, die MPEG-1-und MPEG-2-Videos decodiert.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: MPEG-2-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527902"
---
# <a name="mpeg-2-video-decoder"></a><span data-ttu-id="81693-103">MPEG-2-Video Decoder</span><span class="sxs-lookup"><span data-stu-id="81693-103">MPEG-2 Video Decoder</span></span>

<span data-ttu-id="81693-104">Der MPEG-2-Video Decoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die MPEG-1-und MPEG-2-Videos decodiert.</span><span class="sxs-lookup"><span data-stu-id="81693-104">The MPEG-2 Video Decoder is a [Media Foundation transform](media-foundation-transforms.md) that decodes MPEG-1 and MPEG-2 video.</span></span> <span data-ttu-id="81693-105">Der Decoder unterstützt MPEG-2-Videos mit einfachem und einem Hauptprofil (H. 262, ISO/IEC 13818-2) und MPEG-1-Video (ISO/IEC 11172-2).</span><span class="sxs-lookup"><span data-stu-id="81693-105">The decoder supports MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) and MPEG-1 video (ISO/IEC 11172-2).</span></span>

## <a name="input-types"></a><span data-ttu-id="81693-106">Eingabetypen</span><span class="sxs-lookup"><span data-stu-id="81693-106">Input Types</span></span>

<span data-ttu-id="81693-107">Der Decoder unterstützt die folgenden Eingabemedien Typen.</span><span class="sxs-lookup"><span data-stu-id="81693-107">The decoder supports the following input media types.</span></span>

| <span data-ttu-id="81693-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="81693-108">Attribute</span></span>                                                 | <span data-ttu-id="81693-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81693-109">Description</span></span>                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="81693-110">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81693-110">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="81693-111">**MF MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="81693-111">**MFMediaType\_Video**</span></span>                                                  |
| [<span data-ttu-id="81693-112">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="81693-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="81693-113">**MF-Format- \_ MPEG1**</span><span class="sxs-lookup"><span data-stu-id="81693-113">**MFVideoFormat\_MPEG1**</span></span><br/> <span data-ttu-id="81693-114">**MF-Format ( \_ MPEG2)**</span><span class="sxs-lookup"><span data-stu-id="81693-114">**MFVideoFormat\_MPEG2**</span></span><br/> |



 

## <a name="output-types"></a><span data-ttu-id="81693-115">Ausgabetypen</span><span class="sxs-lookup"><span data-stu-id="81693-115">Output Types</span></span>

<span data-ttu-id="81693-116">Der Decoder unterstützt die folgenden Ausgabetypen.</span><span class="sxs-lookup"><span data-stu-id="81693-116">The decoder supports the following output types.</span></span>

| <span data-ttu-id="81693-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="81693-117">Attribute</span></span>                                                 | <span data-ttu-id="81693-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81693-118">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81693-119">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81693-119">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="81693-120">**MF MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="81693-120">**MFMediaType\_Video**</span></span>                                                                                                                                                         |
| [<span data-ttu-id="81693-121">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="81693-121">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="81693-122">**MF-Format \_ I420**</span><span class="sxs-lookup"><span data-stu-id="81693-122">**MFVideoFormat\_I420**</span></span><br/> <span data-ttu-id="81693-123">**MF-Format ( \_ IYUV)**</span><span class="sxs-lookup"><span data-stu-id="81693-123">**MFVideoFormat\_IYUV**</span></span><br/> <span data-ttu-id="81693-124">**MF-Format \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="81693-124">**MFVideoFormat\_NV12**</span></span><br/> <span data-ttu-id="81693-125">**MF-Format \_ im YUY2**</span><span class="sxs-lookup"><span data-stu-id="81693-125">**MFVideoFormat\_YUY2**</span></span><br/> <span data-ttu-id="81693-126">**MF-Format \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="81693-126">**MFVideoFormat\_YV12**</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81693-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81693-127">Remarks</span></span>

<span data-ttu-id="81693-128">Der MPEG-2-Video Decoder macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="81693-128">The MPEG-2 video decoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="81693-129">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="81693-129">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="81693-130">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="81693-130">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="81693-131">**IMF-Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="81693-131">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="81693-132">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="81693-132">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="81693-133">**Imfratecontrol**</span><span class="sxs-lookup"><span data-stu-id="81693-133">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="81693-134">**Imfratesupport**</span><span class="sxs-lookup"><span data-stu-id="81693-134">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="81693-135">**Imfrealtimeclient**</span><span class="sxs-lookup"><span data-stu-id="81693-135">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="81693-136">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="81693-136">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="81693-137">Die Eingabe für den Decoder muss ein elementaren Stream sein.</span><span class="sxs-lookup"><span data-stu-id="81693-137">The input to the decoder must be an elementary stream.</span></span> <span data-ttu-id="81693-138">Die maximal unterstützte Auflösung beträgt 1920 × 1088 Pixel.</span><span class="sxs-lookup"><span data-stu-id="81693-138">The maximum supported resolution is 1920 × 1088 pixels.</span></span>

<span data-ttu-id="81693-139">Der Decoder unterstützt die DirectX-Video Beschleunigung (DXVA) mithilfe von Microsoft Direct3D 9 oder Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="81693-139">The decoder supports DirectX Video Acceleration (DXVA) using either Microsoft Direct3D 9 or Microsoft Direct3D 11.</span></span>

### <a name="special-decoding-modes"></a><span data-ttu-id="81693-140">Besondere Decodierungs Modi</span><span class="sxs-lookup"><span data-stu-id="81693-140">Special Decoding Modes</span></span>

-   <span data-ttu-id="81693-141">**Modus mit niedriger Latenz.**</span><span class="sxs-lookup"><span data-stu-id="81693-141">**Low latency mode.**</span></span> <span data-ttu-id="81693-142">Dieser Modus eignet sich für Szenarien wie z. b. die Echtzeitkommunikation.</span><span class="sxs-lookup"><span data-stu-id="81693-142">This mode is appropriate for scenarios such as real-time communications.</span></span> <span data-ttu-id="81693-143">Dies reduziert die Start Latenz, sodass der Decoder das erste Ausgabe Beispiel früher erzeugt.</span><span class="sxs-lookup"><span data-stu-id="81693-143">It reduces start-up latency, so the decoder produces the first output sample sooner.</span></span> <span data-ttu-id="81693-144">Der Decoder puffert jedoch weniger Beispiele in diesem Modus, was potenziell zu einem Fehler führen kann, da der Decoder nicht so viele Frames im Voraus decodiert.</span><span class="sxs-lookup"><span data-stu-id="81693-144">However, the decoder buffers fewer samples in this mode, which can potentially lead to glitches, because the decoder does not decode as many frames in advance.</span></span> <span data-ttu-id="81693-145">Um den Modus mit niedriger Latenz zu aktivieren, legen Sie das Attribut [codecapi \_ avlowlatencymode](codecapi-avlowlatencymode.md) fest.</span><span class="sxs-lookup"><span data-stu-id="81693-145">To enable low latency mode, set the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) attribute.</span></span>
-   <span data-ttu-id="81693-146">**Diejenigen.**</span><span class="sxs-lookup"><span data-stu-id="81693-146">**Seeking.**</span></span> <span data-ttu-id="81693-147">Zum exakten suchen müssen Sie die [**imftransform:: setoutputbounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="81693-147">For precise seeking, call the [**IMFTransform::SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) method.</span></span> <span data-ttu-id="81693-148">Wenn diese Methode aufgerufen wird, gibt der Decoder nur Frames aus, die innerhalb des vom Aufrufer angegebenen Zeitstempels liegen.</span><span class="sxs-lookup"><span data-stu-id="81693-148">When this method is called, the decoder outputs only frames that fall within the range of time stamps specified by the caller.</span></span>
-   <span data-ttu-id="81693-149">**Miniatur Generierungs Modus**.</span><span class="sxs-lookup"><span data-stu-id="81693-149">**Thumbnail generation mode**.</span></span> <span data-ttu-id="81693-150">Dieser Modus ist für die schnelle Generierung von Miniaturbildern vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="81693-150">This mode is intended for quick generation of thumbnail images.</span></span> <span data-ttu-id="81693-151">In diesem Modus decodiert der Decoder anfänglich nur I-Frames.</span><span class="sxs-lookup"><span data-stu-id="81693-151">In this mode, the decoder initially decodes only I frames.</span></span> <span data-ttu-id="81693-152">Wenn innerhalb einer bestimmten Anzahl von Frames kein Frame gefunden wird, startet der Decoder die Decodierung von P-Frames und gibt nicht-– I-Frames in einem festgelegten Intervall (einer pro *N* Bilder) aus, bis ein I-Frame erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="81693-152">If no I frame is found within a certain number of frames, the decoder starts decoding P frames and outputs non–I frames at a fixed interval (one per *N* pictures) until an I frame is reached.</span></span> <span data-ttu-id="81693-153">Legen Sie die [codecapi \_ avdecvideothumbnailgenerationmode](../directshow/avdecvideothumbnailgenerationmode-property.md) -Eigenschaft fest, um den Modus für die Miniatur Generierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="81693-153">To enable thumbnail generation mode, set the [CODECAPI\_AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) property.</span></span>
-   <span data-ttu-id="81693-154">**Trick Wiedergabe.**</span><span class="sxs-lookup"><span data-stu-id="81693-154">**Trick play.**</span></span> <span data-ttu-id="81693-155">Der Decoder kann bei Raten schneller als in Echtzeit decodieren.</span><span class="sxs-lookup"><span data-stu-id="81693-155">The decoder can decode at rates faster than real time.</span></span> <span data-ttu-id="81693-156">Bei höheren Wiedergabe Raten schaltet der Decoder zum Decodieren von I-Frames um.</span><span class="sxs-lookup"><span data-stu-id="81693-156">At higher playback rates, the decoder will switch to decoding only I frames.</span></span> <span data-ttu-id="81693-157">Bei umgekehrter Wiedergabe werden nur I-Frames decodiert.</span><span class="sxs-lookup"><span data-stu-id="81693-157">For reverse playback, only I frames are decoded.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="81693-158">Codec-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81693-158">Codec Properties</span></span>

<span data-ttu-id="81693-159">Der Decoder unterstützt die folgenden Eigenschaften durch die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="81693-159">The decoder supports the following properties through the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span>



| <span data-ttu-id="81693-160">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="81693-160">Property</span></span>                                                                                                      | <span data-ttu-id="81693-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81693-161">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81693-162">Codecapi \_ avdecvideothumbnailgenerationmode</span><span class="sxs-lookup"><span data-stu-id="81693-162">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)               | <span data-ttu-id="81693-163">Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="81693-163">Enables or disables thumbnail generation mode.</span></span>                                                             |
| [<span data-ttu-id="81693-164">Codecapi \_ avdecvideoacceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="81693-164">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | <span data-ttu-id="81693-165">Aktiviert oder deaktiviert die hardwarebeschleunigte Decodierung.</span><span class="sxs-lookup"><span data-stu-id="81693-165">Enables or disables hardware accelerated decoding.</span></span>                                                         |
| [<span data-ttu-id="81693-166">Codecapi \_ avlowlatencymode</span><span class="sxs-lookup"><span data-stu-id="81693-166">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="81693-167">Aktiviert oder deaktiviert den Modus mit niedriger Latenz.</span><span class="sxs-lookup"><span data-stu-id="81693-167">Enables or disables low-latency mode.</span></span>                                                                      |
| [<span data-ttu-id="81693-168">MFT- \_ Decoder macht \_ \_ Ausgabe \_ Typen \_ in \_ nativer \_ Reihenfolge verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81693-168">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="81693-169">Gibt an, ob der Decoder Ausgabetypen verfügbar macht, die für die Transcodierung vor anderen Formaten geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="81693-169">Specifies whether the decoder exposes output types that are suitable for transcoding before other formats.</span></span> |



 

<span data-ttu-id="81693-170">Die folgenden Eigenschaften können auch über die [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi) -Schnittstelle festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="81693-170">Of these properties, the following can also be set through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface:</span></span>

-   [<span data-ttu-id="81693-171">Codecapi \_ avdecvideothumbnailgenerationmode</span><span class="sxs-lookup"><span data-stu-id="81693-171">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="81693-172">Codecapi \_ avdecvideoacceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="81693-172">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [<span data-ttu-id="81693-173">Codecapi \_ avlowlatencymode</span><span class="sxs-lookup"><span data-stu-id="81693-173">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

### <a name="limitations"></a><span data-ttu-id="81693-174">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="81693-174">Limitations</span></span>

-   <span data-ttu-id="81693-175">Der Decoder wird auf IA-64 – basierten Plattformen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81693-175">The decoder is not supported on IA-64–based platforms.</span></span>
-   <span data-ttu-id="81693-176">Der Decoder unterstützt keine CSS-Entschlüsselung oder Wiedergabe verschlüsselter DVDs.</span><span class="sxs-lookup"><span data-stu-id="81693-176">The decoder does not support CSS decryption or playback of encrypted DVDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="81693-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81693-177">Requirements</span></span>



| <span data-ttu-id="81693-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81693-178">Requirement</span></span> | <span data-ttu-id="81693-179">Wert</span><span class="sxs-lookup"><span data-stu-id="81693-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="81693-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81693-180">Minimum supported client</span></span><br/> | <span data-ttu-id="81693-181">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81693-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="81693-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81693-182">Minimum supported server</span></span><br/> | <span data-ttu-id="81693-183">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81693-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="81693-184">DLL</span><span class="sxs-lookup"><span data-stu-id="81693-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81693-185"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81693-185"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81693-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81693-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81693-187">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="81693-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
