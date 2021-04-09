---
description: Die maximale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: MF_MT_FRAME_RATE_RANGE_MAX-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959287"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>Maximal zulässige Größe des MF \_ MT- \_ Frame \_ Raten \_ Bereichs \_

Die maximale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Um dieses Attribut festzulegen, nennen Sie [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Bemerkungen

Die Framerate wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner. Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1.

Wenn das Erfassungsgerät eine maximale Framerate meldet, legt die Medienquelle dieses Attribut auf den Medientyp fest. Die minimale Framerate wird im " [MF \_ MT"- \_ Rahmen \_ Raten \_ Bereich " \_ Min](mf-mt-frame-rate-range-min.md) "-Attribut angegeben. Es ist nicht garantiert, dass das Gerät jedes Inkrement in diesem Bereich unterstützt.

Zum Festlegen der Framerate des Geräts ändern Sie zunächst den Wert des " [**MF MT"- \_ \_ Frame \_ Raten**](mf-mt-frame-rate-attribute.md) Attributs für den Medientyp. Legen Sie dann den Medientyp für die Medienquelle fest.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Festlegen der Frame Rate für die Video Erfassung](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Bereich für die Anzahl von MF \_ MT- \_ Frame \_ Raten \_ \_](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




