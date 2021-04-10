---
title: ICM_DRAW_STOP_PLAY Meldung (VFW. h)
description: Durch die ICM \_ Draw- \_ \_ Wiedergabe Meldung wird ein renderingerber benachrichtigt, wenn ein Wiedergabe Vorgang beendet ist. Sie können diese Nachricht explizit oder mithilfe des icdrawstopplay-Makros senden.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106551"
---
# <a name="icm_draw_stop_play-message"></a>ICM \_ Draw \_ - \_ Wiedergabe Meldung

Durch die **ICM \_ Draw- \_ \_ Wiedergabe** Meldung wird ein renderingerber benachrichtigt, wenn ein Wiedergabe Vorgang beendet ist. Sie können diese Nachricht explizit oder mithilfe des [**icdrawstopplay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) -Makros senden.


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung, wenn der Wiedergabe Vorgang beendet ist. Verwenden Sie die [**ICM \_ Draw \_**](icm-draw-stop.md) -Nachricht zum Beenden der zeitlichen Steuerung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





