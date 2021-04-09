---
description: Gibt die Drehung eines Video Frames in der Richtung gegen den Uhrzeigersinn an.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: MF_MT_VIDEO_ROTATION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868936"
---
# <a name="mf_mt_video_rotation-attribute"></a>MF- \_ MT- \_ Video- \_ Rotations Attribut

Gibt die Drehung eines Video Frames in der Richtung gegen den Uhrzeigersinn an.

## <a name="data-type"></a>Datentyp

**MF videorotationformat** , gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Video von einem Hand Held Gerät, z. b. ein Mobiltelefon, wird häufig um 90, 180 oder 270 Grad gedreht. Wenn die Kamera die Ausrichtung als Metadaten in der Videodatei speichert, kann das Bild zum Zeitpunkt der Wiedergabe angepasst werden.

Wenn dieses Attribut auf **mfvideorotationformat \_ 90** festgelegt ist, bedeutet dies, dass der Inhalt um 90 Grad in der Richtung gegen den Uhrzeigersinn gedreht wurde. Wenn der Inhalt 90 Grad in der Richtung im Uhrzeigersinn gedreht wurde, wäre der Attribut Wert **MF videorotationformat \_ 270**.

Die unterstützten Werte für dieses Attribut werden in [**MF videorotationformat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat)aufgelistet.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 




