---
description: Gibt für ein 3D-Videoformat an, welche Sicht die Basis Ansicht ist.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: MF_MT_VIDEO_3D_LEFT_IS_BASE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363313"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>MF \_ \_ -MT \_ -Video 3D \_ ist das \_ \_ Basis Attribut

Gibt für ein 3D-Videoformat an, welche Sicht die Basis Ansicht ist.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Standardmäßig ist die linke Ansicht in einer 3D-Videosequenz die Basis Ansicht. Wenn die Rechte Ansicht die Basis Ansicht ist, legen Sie dieses Attribut auf " **false**" fest.

Um das Stereovideo in 2D zu konvertieren, behalten Sie die Basis Ansicht bei und verwerfen die andere Sicht.

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

 

 




