---
description: Definiert die geometrische Öffnung für einen Video Medientyp.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: MF_MT_GEOMETRIC_APERTURE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959286"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>\_ \_ Geometrische Aperture- \_ Attribut für MF MT

Definiert die geometrische Öffnung für einen Video Medientyp.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist eine [**MF Video Area**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) -Struktur.

Das Bildseiten Verhältnis wird relativ zur geometrischen Öffnung berechnet, wobei die folgende Formel verwendet wird: Bildseiten Verhältnis = (geometrische Aperture Width/geometrische Aperture Height) × Pixel Seitenverhältnis.

Wenn dieses Attribut nicht festgelegt ist, wird davon ausgegangen, dass es sich bei der geometrischen Öffnung um den gesamten Videorahmen handelt. Dieses Attribut sollte nur festgelegt werden, wenn der Medientyp einen Videostandard mit einem definierten aktiven Bereich beschreibt.

In NTSC TV lautet der Videorahmen beispielsweise 720 × 480 mit einem aktiven Bereich von 704 × 480 und einem Seitenverhältnis von 10:11 Pixel. Das resultierende Bild hat ein Seitenverhältnis von (704/480) × (10/11) = 4:3.

> [!Note]  
> Der Standard Presenter für den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) zeigt die geometrische Öffnung des Videos, falls angegeben.

 

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="examples"></a>Beispiele


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Bildseiten Verhältnis](picture-aspect-ratio.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




