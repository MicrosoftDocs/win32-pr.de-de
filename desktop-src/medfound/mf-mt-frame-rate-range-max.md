---
description: Die maximale Bildfrequenz, die von einem Videoaufnahmegerät in Frames pro Sekunde unterstützt wird.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: MF_MT_FRAME_RATE_RANGE_MAX-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5988a6aee872489327707c7e87639f7467560014c5bdd29bc9b0bd9a136ccbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742042"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>MF \_ MT FRAME RATE RANGE \_ \_ \_ \_ MAX-Attribut

Die maximale Bildfrequenz, die von einem Videoaufnahmegerät in Frames pro Sekunde unterstützt wird.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)auf, um dieses Attribut abzurufen.

Um dieses Attribut festzulegen, rufen Sie [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio)auf.

## <a name="remarks"></a>Hinweise

Die Bildfrequenz wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attributwerts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner. Wenn die Bildfrequenz beispielsweise 30 Frames pro Sekunde (fps) beträgt, beträgt das Verhältnis 30/1.

Wenn das Erfassungsgerät eine maximale Bildfrequenz meldet, legt die Medienquelle dieses Attribut auf den Medientyp fest. Die mindeste Bildfrequenz wird im [MF MT FRAME RATE RANGE \_ \_ \_ \_ \_ MIN-Attribut](mf-mt-frame-rate-range-min.md) angegeben. Es ist nicht garantiert, dass das Gerät jedes Inkrement innerhalb dieses Bereichs unterstützt.

Um die Bildfrequenz des Geräts festzulegen, ändern Sie zunächst den Wert des [**MF \_ MT FRAME \_ \_ RATE-Attributs**](mf-mt-frame-rate-attribute.md) für den Medientyp. Legen Sie dann den Medientyp für die Medienquelle fest.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Festlegen der Videoaufnahme-Bildfrequenz](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




