---
description: Beschreibt, wie Chroma für einen YCbCr-Video Medientyp getestet wurde.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: MF_MT_VIDEO_CHROMA_SITING-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347656"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a>MF \_ MT- \_ Video- \_ Chroma- \_ siting-Attribut

Beschreibt, wie Chroma für den Video Medientyp "y' cb' CR '" abgefragt wurde.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein bitweises **or** von Flags aus der [**MF videochromasubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) -Enumeration.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[Erweiterte Farbinformationen](extended-color-information.md)
</dt> </dl>

 

 




