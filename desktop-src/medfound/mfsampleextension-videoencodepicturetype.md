---
description: Gibt den Bildtyp an, der von einem Videoencoder ausgegeben wird.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: MFSampleExtension_VideoEncodePictureType Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be87284be3b605e3af70d64df98e5d762aa7cc353bb83b5f61a110d1242ae1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973169"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a>MFSampleExtension \_ VideoEncodePictureType-Attribut

Gibt den Bildtyp an, der von einem Videoencoder ausgegeben wird.

## <a name="data-type"></a>Datentyp

**eAVEncH264PictureType \_ Als** **UINT32** gespeichertes B

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**DIESSAMPLE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

[**H.264 Video Encoder**](h-264-video-encoder.md) legt dieses Attribut für die generierten Ausgabebeispiele fest. Der Wert des Attributs ist ein Member der [**eAVEncH264PictureType-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**H.264 Video Encoder**](h-264-video-encoder.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> </dl>

 

 




