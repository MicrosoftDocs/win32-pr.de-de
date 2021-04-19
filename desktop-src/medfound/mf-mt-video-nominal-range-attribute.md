---
description: Gibt den nominalen Bereich der Farbinformationen in einem Video Medientyp an.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: MF_MT_VIDEO_NOMINAL_RANGE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355419"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>\_Attribut des \_ \_ \_ Attributs "MF MT-Video"

Gibt den nominalen Bereich der Farbinformationen in einem Video Medientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der [**mfnominalrange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) -Enumeration.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

**H. 264/AVC-Encoder:**

Für den Ausgabe Medientyp kann der \_ \_ \_ nominale Bereich des MF MT-Videos \_ mit **MF nominalrange \_ 0 \_ 255** und **MF nominalrange \_ 16 \_ 235** festgelegt werden.

Der H. 264/AVC-Encoder muss " **MF nominalrange \_ Unknown** " als " **MF nominalrange \_ 16 \_ 235**" behandeln.

Der H. 264/AVC-Encoder muss einen Ausgabe Medientyp ablehnen, wenn der \_ nominale Bereich des MF MT- \_ Videos \_ \_ auf **mfnominalrange \_ 48 \_ 208**, **mfnominalrange \_ 64 \_ 127** oder andere Werte, die nicht für [**mfnominalrange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)definiert sind, festgelegt ist.

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

 

 




