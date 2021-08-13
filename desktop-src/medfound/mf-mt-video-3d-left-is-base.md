---
description: Bei einem 3D-Videoformat gibt an, welche Ansicht die Basisansicht ist.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: MF_MT_VIDEO_3D_LEFT_IS_BASE-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb03bc12d32b96abc52999ef6a3b21580c4ac1c59125a076b9eb1d620e0bd362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741592"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>MF \_ MT \_ VIDEO \_ 3D \_ LEFT IS \_ \_ BASE-Attribut

Bei einem 3D-Videoformat gibt an, welche Ansicht die Basisansicht ist.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Standardmäßig ist die linke Ansicht in einer 3D-Videosequenz die Basisansicht. Wenn die rechte Ansicht die Basisansicht ist, legen Sie dieses Attribut auf **FALSE** fest.

Wenn Sie Stereovideos in 2D konvertieren möchten, behalten Sie die Basisansicht bei, und verwerfen Sie die andere Ansicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




