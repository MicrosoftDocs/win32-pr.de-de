---
description: Gibt die Farb Primärwerte für einen Video Medientyp an.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359529"
---
# <a name="mf_mt_video_primaries-attribute"></a>MF \_ MT- \_ Video- \_ primär Attribut

Gibt die Farb Primärwerte für einen Video Medientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der [**mfvideoprimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) -Enumeration.

Die [**MF videoprimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) -Enumeration identifiziert Farb Replikate, die bestimmten gängigen Videostandards zugeordnet sind. Wenn der Medientyp Farb Replikate verwendet, die nicht in der **MF videoprimaries** -Enumeration identifiziert werden, legen Sie anstelle dieses Attributs das [**benutzerdefinierte Attribut "MF \_ MT \_ Custom \_ Video \_ Primaries**](mf-mt-custom-video-primaries-attribute.md) " fest.

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

 

 




