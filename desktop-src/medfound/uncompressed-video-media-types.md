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
# <a name="uncompressed-video-media-types"></a>Nicht komprimierte Video Medientypen

In diesem Thema wird beschrieben, wie ein Medientyp erstellt wird, der ein unkomprimiertes Videoformat beschreibt. Weitere Informationen zu Medientypen finden Sie unter Informationen [zu Medientypen](about-media-types.md).

Legen Sie zum Erstellen eines kompletten unkomprimierten Video Typs die folgenden Attribute für den [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstellen Zeiger fest.



| Attribut                                                                            | BESCHREIBUNG                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                            | Der Haupttyp. Legen Sie auf **mfmediatype- \_ Video** fest.                                                                                                                                                                                          |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                   | Untertyp. Siehe [Video Untertyp-GUIDs](video-subtype-guids.md).                                                                                                                                                                        |
| [**MF- \_ MT- \_ Standard \_ Schritt**](mf-mt-default-stride-attribute.md)                    | Surface Stride. Der *Stride* -Wert ist die Anzahl der Bytes, die erforderlich sind, um von einer Zeile aus Pixel zum nächsten zu wechseln. Legen Sie dieses Attribut fest, wenn der Schritt in Bytes nicht mit der Breite des Videos in Bytes übereinstimmt. Andernfalls können Sie dieses Attribut weglassen. |
| [**MF- \_ MT- \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md)                            | Die Framerate.                                                                                                                                                                                                                         |
| [**MF- \_ MT- \_ Frame \_ Größe**](mf-mt-frame-size-attribute.md)                            | Frame Größe.                                                                                                                                                                                                                         |
| [**MF- \_ MT- \_ Interlace- \_ Modus**](mf-mt-interlace-mode-attribute.md)                    | Der interschnür Modus.                                                                                                                                                                                                                   |
| [**\_ \_ alle \_ Beispiele \_ unabhängig von MF**](mf-mt-all-samples-independent-attribute.md) | Gibt an, ob jede Stichprobe unabhängig ist. Legen Sie für nicht komprimierte Formate auf **true** fest.                                                                                                                                             |
| [**Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_**](mf-mt-pixel-aspect-ratio-attribute.md)           | Pixel Seitenverhältnis.                                                                                                                                                                                                                 |



 

Legen Sie außerdem die folgenden Attribute fest, wenn Sie die richtigen Werte kennen. (Andernfalls lassen Sie diese Attribute Weg.)



| Attribut                                                                    | BESCHREIBUNG        |
|------------------------------------------------------------------------------|--------------------|
| [**MF- \_ MT- \_ Video- \_ primär**](mf-mt-video-primaries-attribute.md)          | Farb Replikate.   |
| [**MF- \_ MT- \_ Übertragungs \_ Funktion**](mf-mt-transfer-function-attribute.md)      | Übertragungsfunktion. |
| [**MF \_ MT \_ YUV \_ Matrix**](mf-mt-yuv-matrix-attribute.md)                    | Matrix übertragen.   |
| [**MF- \_ MT- \_ Video- \_ Chroma- \_ siting**](mf-mt-video-chroma-siting-attribute.md) | Chroma-siting.     |
| [**\_ \_ \_ nominaler Bereich von MF MT-Video \_**](mf-mt-video-nominal-range-attribute.md) | Der nominale Bereich.     |



 

Weitere Informationen finden Sie unter [Erweiterte Farbinformationen](extended-color-information.md). Wenn Sie z. b. einen Medientyp erstellen, der einen Videostandard beschreibt, und der Standard die Chroma-siting definiert, fügen Sie diese Informationen dem Medientyp hinzu. Dies trägt dazu bei, die Farb Treue in der Pipeline beizubehalten.

Die folgenden Funktionen sind möglicherweise nützlich, wenn Sie einen Video Medientyp erstellen.



| Funktion                                                                     | BESCHREIBUNG                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mfaveragetimeperframeumframerate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Berechnet die Framerate, wenn die durchschnittliche Frame Dauer angegeben wird.                                                                                                                         |
| [**MF calculateimagesize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Berechnet die Bildgröße für ein unkomprimiertes Videoformat.                                                                                                                          |
| [**Mfframerateesaveragetimeperframe**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Berechnet die durchschnittliche Dauer eines Video Frames, wenn die Framerate angegeben ist.                                                                                                              |
| [**Mfgetstrideforbitmapinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Gibt den minimalen Oberflächen Schritt für ein Videoformat zurück. Weitere Informationen finden Sie unter [Image Stride](image-stride.md).                                                                   |
| [**Mfinitvideoformat**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | Initialisiert eine [**MF Videoformat**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) -Struktur für einige Standard Videoformate, wie z. b. NTSC-Fernsehgeräte. Anschließend können Sie die-Struktur verwenden, um einen Medientyp zu initialisieren. |
| [**Mfisformatyuv**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Fragt ab, ob ein Videoformat ein YUV-Format ist.                                                                                                                                      |



 

## <a name="examples"></a>Beispiele

Dieses Beispiel zeigt eine Funktion, die die gängigsten Informationen für ein unkomprimiertes Videoformat ausfüllt. Die-Funktion gibt einen [**imbomediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstellen Zeiger zurück. Anschließend können Sie dem Medientyp nach Bedarf weitere Attribute hinzufügen.


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



Im nächsten Beispiel wird ein codiertes Videoformat als Eingabe angenommen, und es wird ein entsprechender unkomprimierter Videotyp erstellt. Dieser Typ kann beispielsweise für einen Encoder oder Decoder festgelegt werden.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Farbinformationen](extended-color-information.md)
</dt> <dt>

[Bild Schritt](image-stride.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[Video Untertyp-GUIDs](video-subtype-guids.md)
</dt> </dl>

 

 



