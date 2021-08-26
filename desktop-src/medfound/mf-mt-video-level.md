---
description: Gibt die MPEG-2- oder H.264-Ebene in einem Videomedientyp an. Dies ist ein Alias von MF \_ MT \_ MPEG2 \_ LEVEL.
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: MF_MT_VIDEO_LEVEL -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40f1ebc6834373e00253f494e3fc76c20c343af17d754c7c4fe642b802d16ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012770"
---
# <a name="mf_mt_video_level-attribute"></a>MF \_ MT \_ VIDEO \_ LEVEL-Attribut

Gibt die MPEG-2- oder H.264-Ebene in einem Videomedientyp an. Dies ist ein Alias von [MF \_ MT \_ MPEG2 \_ LEVEL](mf-mt-mpeg2-level-attribute.md).

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

**H.264-Encoder:**

Die unterstützten Ebenen werden um [**eAVEncH264VLevel5 \_ 2 erweitert.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel)

Standard: Die empfohlene Standardeinstellung ist die Auswahl der Mindeststufe für die Videocodierungskonfiguration, einschließlich Auflösung, Bildfrequenz usw.

Empfohlener Standardwert: Wählen Sie die Mindeststufe für die Videocodierungskonfiguration aus, einschließlich Auflösung, Bildfrequenz usw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




