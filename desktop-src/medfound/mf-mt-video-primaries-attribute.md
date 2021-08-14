---
description: Gibt die Farbprimärdateien für einen Videomedientyp an.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44b4e1c99dc9a4f288ebab36d413f7eed7c74881e7c10d3c7e9a8a4fe3f0bcf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876710"
---
# <a name="mf_mt_video_primaries-attribute"></a>MF \_ MT \_ VIDEO \_ PRIMARIES-Attribut

Gibt die Farbprimärdateien für einen Videomedientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Member der [**MFVideoPrimaries-Enumeration.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries)

Die [**MFVideoPrimaries-Enumeration**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifiziert Farbprimärdateien, die bestimmten allgemeinen Videostandards zugeordnet sind. Wenn der Medientyp Farbprimärdateien verwendet, die in der **MFVideoPrimaries-Enumeration** nicht identifiziert werden, legen Sie das [**MF MT CUSTOM VIDEO \_ \_ \_ \_ PRIMARIES-Attribut**](mf-mt-custom-video-primaries-attribute.md) anstelle dieses Attributs fest.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Erweiterte Farbinformationen](extended-color-information.md)
</dt> </dl>

 

 




