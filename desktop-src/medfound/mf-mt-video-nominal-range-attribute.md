---
description: Gibt den nominalen Bereich der Farbinformationen in einem Videomedientyp an.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: MF_MT_VIDEO_NOMINAL_RANGE Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b294ea3c63f845b51c9636f78ee78f04135e17929ae6e64d92ab85720f3c7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876720"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>MF \_ MT VIDEO NOMINAL \_ \_ \_ RANGE-Attribut

Gibt den nominalen Bereich der Farbinformationen in einem Videomedientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Member der [**MFNominalRange-Enumeration.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

**H.264/AVC-Encoder:**

Auf dem Ausgabemedientyp kann MF \_ MT VIDEO NOMINAL RANGE mit \_ \_ \_ **MFNominalRange \_ 0 \_ 255** und **MFNominalRange \_ 16 \_ 235** festgelegt werden.

Der H.264/AVC-Encoder muss **MFNominalRange \_ Unknown** als **MFNominalRange \_ 16 \_ 235** behandeln.

Der H.264/AVC-Encoder muss einen Ausgabemedientyp ablehnen, wenn MF \_ MT VIDEO NOMINAL RANGE auf \_ \_ \_ **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127** oder andere Werte festgelegt ist, die nicht für [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)definiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Erweiterte Farbinformationen](extended-color-information.md)
</dt> </dl>

 

 




