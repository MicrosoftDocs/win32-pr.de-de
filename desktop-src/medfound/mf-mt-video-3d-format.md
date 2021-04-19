---
description: Gibt bei einem Video Medientyp an, wie 3D-Videorahmen im Arbeitsspeicher gespeichert werden.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359453"
---
# <a name="mf_mt_video_3d_format-attribute"></a>\_Format Attribut für MF MT \_ \_ -Video 3D \_

Gibt bei einem Video Medientyp an, wie 3D-Videorahmen im Arbeitsspeicher gespeichert werden.

## <a name="data-type"></a>Datentyp

**MFVideo3DFormat** als **UInt32** gespeichert

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) -Enumeration. Das-Attribut wird nur angewendet, wenn das [MF \_ MT \_ \_ -Video 3D-](mf-mt-video-3d.md) Attribut den Wert **true** hat.

Dieses Attribut ist für unkomprimierte 3D-Videoformate erforderlich. Es ist optional für komprimierte 3D-Videos. Eine Medienquelle, die codierte Frames bereitstellt, kann das-Attribut möglicherweise basierend auf Informationen im Datei Container festlegen. Andernfalls sollte das Attribut vom Decoder im Ausgabe Medientyp des Decoders festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




