---
description: Gibt für einen Videomedientyp an, wie 3D-Videoframes im Arbeitsspeicher gespeichert werden.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4100a605ecc7e8fe1c171b02341822972061363e7cd1b322162291dbd75b2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692069"
---
# <a name="mf_mt_video_3d_format-attribute"></a>MF \_ MT \_ VIDEO \_ 3D \_ FORMAT-Attribut

Gibt für einen Videomedientyp an, wie 3D-Videoframes im Arbeitsspeicher gespeichert werden.

## <a name="data-type"></a>Datentyp

**Als UINT32 gespeichertes MFVideo3DFormat** 

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Member der [**MFVideo3DFormat-Enumeration.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) Das Attribut gilt nur, wenn das [MF \_ MT VIDEO \_ \_ 3D-Attribut](mf-mt-video-3d.md) **TRUE ist.**

Dieses Attribut ist für unkomprimierte 3D-Videoformate erforderlich. Es ist optional für komprimierte 3D-Videos. Eine Medienquelle, die codierte Frames liefert, kann das Attribut möglicherweise basierend auf Informationen im Dateicontainer festlegen. Andernfalls sollte das Attribut vom Decoder im Ausgabemedientyp des Decoders festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




