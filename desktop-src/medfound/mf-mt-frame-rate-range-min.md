---
description: Die minimale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: MF_MT_FRAME_RATE_RANGE_MIN-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867547"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a>"MF MT"- \_ \_ Frame \_ Raten \_ Bereich \_ Min-Attribut

Die minimale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Um dieses Attribut festzulegen, nennen Sie [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Bemerkungen

Die Framerate wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner. Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1.

Wenn das Erfassungsgerät eine minimale Framerate meldet, legt die Medienquelle dieses Attribut auf den Medientyp fest. Die maximale Framerate ist im [Bereich "MF \_ MT- \_ Rahmen \_ Raten Bereich ( \_ \_ Max](mf-mt-frame-rate-range-max.md) )" angegeben. Es ist nicht garantiert, dass das Gerät jedes Inkrement in diesem Bereich unterstützt.

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

[maximal zulässige Anzahl von MF- \_ MT- \_ Frame \_ Raten \_ \_](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 




