---
description: Nicht komprimierte Video Medientypen
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Nicht komprimierte Video Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c90a48aed62f22a492ac22dae93761c1046750a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530488"
---
# <a name="uncompressed-video-media-types"></a><span data-ttu-id="15d18-103">Nicht komprimierte Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="15d18-103">Uncompressed Video Media Types</span></span>

<span data-ttu-id="15d18-104">In diesem Thema wird beschrieben, wie ein Medientyp erstellt wird, der ein unkomprimiertes Videoformat beschreibt.</span><span class="sxs-lookup"><span data-stu-id="15d18-104">This topic describes how to create a media type that describes an uncompressed video format.</span></span> <span data-ttu-id="15d18-105">Weitere Informationen zu Medientypen finden Sie unter Informationen [zu Medientypen](about-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="15d18-105">For more information about media types generally, see [About Media Types](about-media-types.md).</span></span>

<span data-ttu-id="15d18-106">Legen Sie zum Erstellen eines kompletten unkomprimierten Video Typs die folgenden Attribute für den [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstellen Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="15d18-106">To create a complete uncompressed video type, set the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="15d18-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="15d18-107">Attribute</span></span>                                                                            | <span data-ttu-id="15d18-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15d18-108">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15d18-109">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15d18-109">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="15d18-110">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="15d18-110">Major type.</span></span> <span data-ttu-id="15d18-111">Legen Sie auf **mfmediatype- \_ Video** fest.</span><span class="sxs-lookup"><span data-stu-id="15d18-111">Set to **MFMediaType\_Video**.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="15d18-112">**MF- \_ MT- \_ Untertyp**</span><span class="sxs-lookup"><span data-stu-id="15d18-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                   | <span data-ttu-id="15d18-113">Untertyp.</span><span class="sxs-lookup"><span data-stu-id="15d18-113">Subtype.</span></span> <span data-ttu-id="15d18-114">Siehe [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="15d18-114">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="15d18-115">**MF- \_ MT- \_ Standard \_ Schritt**</span><span class="sxs-lookup"><span data-stu-id="15d18-115">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)                    | <span data-ttu-id="15d18-116">Surface Stride.</span><span class="sxs-lookup"><span data-stu-id="15d18-116">Surface stride.</span></span> <span data-ttu-id="15d18-117">Der *Stride* -Wert ist die Anzahl der Bytes, die erforderlich sind, um von einer Zeile aus Pixel zum nächsten zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="15d18-117">The *stride* is the number of bytes needed to go from one row of pixels to the next.</span></span> <span data-ttu-id="15d18-118">Legen Sie dieses Attribut fest, wenn der Schritt in Bytes nicht mit der Breite des Videos in Bytes übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="15d18-118">Set this attribute if the stride in bytes is not the same as the video width in bytes.</span></span> <span data-ttu-id="15d18-119">Andernfalls können Sie dieses Attribut weglassen.</span><span class="sxs-lookup"><span data-stu-id="15d18-119">Otherwise, you can omit this attribute.</span></span> |
| [<span data-ttu-id="15d18-120">**MF- \_ MT- \_ Frame \_ Rate**</span><span class="sxs-lookup"><span data-stu-id="15d18-120">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)                            | <span data-ttu-id="15d18-121">Die Framerate.</span><span class="sxs-lookup"><span data-stu-id="15d18-121">Frame rate.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="15d18-122">**MF- \_ MT- \_ Frame \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="15d18-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                            | <span data-ttu-id="15d18-123">Frame Größe.</span><span class="sxs-lookup"><span data-stu-id="15d18-123">Frame size.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="15d18-124">**MF- \_ MT- \_ Interlace- \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="15d18-124">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                    | <span data-ttu-id="15d18-125">Der interschnür Modus.</span><span class="sxs-lookup"><span data-stu-id="15d18-125">Interlacing mode.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="15d18-126">**\_ \_ alle \_ Beispiele \_ unabhängig von MF**</span><span class="sxs-lookup"><span data-stu-id="15d18-126">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="15d18-127">Gibt an, ob jede Stichprobe unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="15d18-127">Specifies whether each sample is independent.</span></span> <span data-ttu-id="15d18-128">Legen Sie für nicht komprimierte Formate auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="15d18-128">Set to **TRUE** for uncompressed formats.</span></span>                                                                                                                                             |
| [<span data-ttu-id="15d18-129">**Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_**</span><span class="sxs-lookup"><span data-stu-id="15d18-129">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)           | <span data-ttu-id="15d18-130">Pixel Seitenverhältnis.</span><span class="sxs-lookup"><span data-stu-id="15d18-130">Pixel aspect ratio.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="15d18-131">Legen Sie außerdem die folgenden Attribute fest, wenn Sie die richtigen Werte kennen.</span><span class="sxs-lookup"><span data-stu-id="15d18-131">In addition, set the following attributes if you know the correct values.</span></span> <span data-ttu-id="15d18-132">(Andernfalls lassen Sie diese Attribute Weg.)</span><span class="sxs-lookup"><span data-stu-id="15d18-132">(Otherwise, omit these attributes.)</span></span>



| <span data-ttu-id="15d18-133">Attribut</span><span class="sxs-lookup"><span data-stu-id="15d18-133">Attribute</span></span>                                                                    | <span data-ttu-id="15d18-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15d18-134">Description</span></span>        |
|------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="15d18-135">**MF- \_ MT- \_ Video- \_ primär**</span><span class="sxs-lookup"><span data-stu-id="15d18-135">**MF\_MT\_VIDEO\_PRIMARIES**</span></span>](mf-mt-video-primaries-attribute.md)          | <span data-ttu-id="15d18-136">Farb Replikate.</span><span class="sxs-lookup"><span data-stu-id="15d18-136">Color primaries.</span></span>   |
| [<span data-ttu-id="15d18-137">**MF- \_ MT- \_ Übertragungs \_ Funktion**</span><span class="sxs-lookup"><span data-stu-id="15d18-137">**MF\_MT\_TRANSFER\_FUNCTION**</span></span>](mf-mt-transfer-function-attribute.md)      | <span data-ttu-id="15d18-138">Übertragungsfunktion.</span><span class="sxs-lookup"><span data-stu-id="15d18-138">Transfer function.</span></span> |
| [<span data-ttu-id="15d18-139">**MF \_ MT \_ YUV \_ Matrix**</span><span class="sxs-lookup"><span data-stu-id="15d18-139">**MF\_MT\_YUV\_MATRIX**</span></span>](mf-mt-yuv-matrix-attribute.md)                    | <span data-ttu-id="15d18-140">Matrix übertragen.</span><span class="sxs-lookup"><span data-stu-id="15d18-140">Transfer matrix.</span></span>   |
| [<span data-ttu-id="15d18-141">**MF- \_ MT- \_ Video- \_ Chroma- \_ siting**</span><span class="sxs-lookup"><span data-stu-id="15d18-141">**MF\_MT\_VIDEO\_CHROMA\_SITING**</span></span>](mf-mt-video-chroma-siting-attribute.md) | <span data-ttu-id="15d18-142">Chroma-siting.</span><span class="sxs-lookup"><span data-stu-id="15d18-142">Chroma siting.</span></span>     |
| [<span data-ttu-id="15d18-143">**\_ \_ \_ nominaler Bereich von MF MT-Video \_**</span><span class="sxs-lookup"><span data-stu-id="15d18-143">**MF\_MT\_VIDEO\_NOMINAL\_RANGE**</span></span>](mf-mt-video-nominal-range-attribute.md) | <span data-ttu-id="15d18-144">Der nominale Bereich.</span><span class="sxs-lookup"><span data-stu-id="15d18-144">Nominal range.</span></span>     |



 

<span data-ttu-id="15d18-145">Weitere Informationen finden Sie unter [Erweiterte Farbinformationen](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="15d18-145">For more information, see [Extended Color Information](extended-color-information.md).</span></span> <span data-ttu-id="15d18-146">Wenn Sie z. b. einen Medientyp erstellen, der einen Videostandard beschreibt, und der Standard die Chroma-siting definiert, fügen Sie diese Informationen dem Medientyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="15d18-146">For example, if you create a media type that describes a video standard, and the standard defines the chroma siting, add this information to the media type.</span></span> <span data-ttu-id="15d18-147">Dies trägt dazu bei, die Farb Treue in der Pipeline beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="15d18-147">Doing so helps to preserve color fidelity throughout the pipeline.</span></span>

<span data-ttu-id="15d18-148">Die folgenden Funktionen sind möglicherweise nützlich, wenn Sie einen Video Medientyp erstellen.</span><span class="sxs-lookup"><span data-stu-id="15d18-148">The following functions might be useful when creating a video media type.</span></span>



| <span data-ttu-id="15d18-149">Funktion</span><span class="sxs-lookup"><span data-stu-id="15d18-149">Function</span></span>                                                                     | <span data-ttu-id="15d18-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15d18-150">Description</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15d18-151">**Mfaveragetimeperframeumframerate**</span><span class="sxs-lookup"><span data-stu-id="15d18-151">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="15d18-152">Berechnet die Framerate, wenn die durchschnittliche Frame Dauer angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="15d18-152">Calculates the frame rate, given the average frame duration.</span></span>                                                                                                                         |
| [<span data-ttu-id="15d18-153">**MF calculateimagesize**</span><span class="sxs-lookup"><span data-stu-id="15d18-153">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="15d18-154">Berechnet die Bildgröße für ein unkomprimiertes Videoformat.</span><span class="sxs-lookup"><span data-stu-id="15d18-154">Calculates the image size for an uncompressed video format.</span></span>                                                                                                                          |
| [<span data-ttu-id="15d18-155">**Mfframerateesaveragetimeperframe**</span><span class="sxs-lookup"><span data-stu-id="15d18-155">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="15d18-156">Berechnet die durchschnittliche Dauer eines Video Frames, wenn die Framerate angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="15d18-156">Calculates the average duration of a video frame, given the frame rate.</span></span>                                                                                                              |
| [<span data-ttu-id="15d18-157">**Mfgetstrideforbitmapinfoheader**</span><span class="sxs-lookup"><span data-stu-id="15d18-157">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="15d18-158">Gibt den minimalen Oberflächen Schritt für ein Videoformat zurück.</span><span class="sxs-lookup"><span data-stu-id="15d18-158">Returns the minimum surface stride for a video format.</span></span> <span data-ttu-id="15d18-159">Weitere Informationen finden Sie unter [Image Stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="15d18-159">For more information, see [Image Stride](image-stride.md).</span></span>                                                                   |
| [<span data-ttu-id="15d18-160">**Mfinitvideoformat**</span><span class="sxs-lookup"><span data-stu-id="15d18-160">**MFInitVideoFormat**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | <span data-ttu-id="15d18-161">Initialisiert eine [**MF Videoformat**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) -Struktur für einige Standard Videoformate, wie z. b. NTSC-Fernsehgeräte.</span><span class="sxs-lookup"><span data-stu-id="15d18-161">Initializes an [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) structure for some standard video formats, such as NTSC television.</span></span> <span data-ttu-id="15d18-162">Anschließend können Sie die-Struktur verwenden, um einen Medientyp zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="15d18-162">You can then use the structure to initialize a media type.</span></span> |
| [<span data-ttu-id="15d18-163">**Mfisformatyuv**</span><span class="sxs-lookup"><span data-stu-id="15d18-163">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="15d18-164">Fragt ab, ob ein Videoformat ein YUV-Format ist.</span><span class="sxs-lookup"><span data-stu-id="15d18-164">Queries whether a video format is a YUV format.</span></span>                                                                                                                                      |



 

## <a name="examples"></a><span data-ttu-id="15d18-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15d18-165">Examples</span></span>

<span data-ttu-id="15d18-166">Dieses Beispiel zeigt eine Funktion, die die gängigsten Informationen für ein unkomprimiertes Videoformat ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="15d18-166">This example shows a function that fills in the most common information for an uncompressed video format.</span></span> <span data-ttu-id="15d18-167">Die-Funktion gibt einen [**imbomediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="15d18-167">The function returns an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span> <span data-ttu-id="15d18-168">Anschließend können Sie dem Medientyp nach Bedarf weitere Attribute hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="15d18-168">You can then add additional attributes to the media type as needed.</span></span>


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="15d18-169">Im nächsten Beispiel wird ein codiertes Videoformat als Eingabe angenommen, und es wird ein entsprechender unkomprimierter Videotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="15d18-169">The next example takes an encoded video format as input, and creates a matching uncompressed video type.</span></span> <span data-ttu-id="15d18-170">Dieser Typ kann beispielsweise für einen Encoder oder Decoder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="15d18-170">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="15d18-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15d18-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15d18-172">Erweiterte Farbinformationen</span><span class="sxs-lookup"><span data-stu-id="15d18-172">Extended Color Information</span></span>](extended-color-information.md)
</dt> <dt>

[<span data-ttu-id="15d18-173">Bild Schritt</span><span class="sxs-lookup"><span data-stu-id="15d18-173">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="15d18-174">Medientypen</span><span class="sxs-lookup"><span data-stu-id="15d18-174">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="15d18-175">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="15d18-175">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="15d18-176">Video Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="15d18-176">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



