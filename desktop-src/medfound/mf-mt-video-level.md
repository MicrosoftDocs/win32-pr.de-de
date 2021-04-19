---
description: Gibt die MPEG-2-oder H. 264-Ebene in einem Video Medientyp an. Hierbei handelt es sich um einen Alias der MF- \_ \_ \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: MF_MT_VIDEO_LEVEL-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363394"
---
# <a name="mf_mt_video_level-attribute"></a>MF- \_ MT- \_ Attribut auf Video \_ Ebene

Gibt die MPEG-2-oder H. 264-Ebene in einem Video Medientyp an. Hierbei handelt es sich um einen Alias der [MF \_ \_ \_ ](mf-mt-mpeg2-level-attribute.md)-.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

**H. 264-Encoder:**

Die unterstützten Ebenen werden um [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel)erweitert.

Standardwert: empfohlen wird empfohlen, die minimale Ebene für die Video Codierungs Konfiguration einschließlich Auflösung, Framerate usw. auszuwählen.

Empfohlene Standardeinstellung: Wählen Sie die minimale Ebene für die Video Codierungs Konfiguration aus, einschließlich Auflösung, Framerate usw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




