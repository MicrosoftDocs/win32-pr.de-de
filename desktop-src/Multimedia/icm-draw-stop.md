---
title: ICM_DRAW_STOP Meldung (VFW. h)
description: Mit der ICM \_ Draw- \_ Meldung wird ein renderingertreiber benachrichtigt, um die interne Uhr für die zeitliche Steuerung von Zeichnungs Frames anzuhalten. Sie können diese Nachricht explizit oder mithilfe des icdrawstopemakros senden.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476245"
---
# <a name="icm_draw_stop-message"></a>ICM- \_ Zeichnungs \_ Ende (Meldung)

Mit der **ICM \_ Draw \_** -Meldung wird ein renderingertreiber benachrichtigt, um die interne Uhr für die zeitliche Steuerung von Zeichnungs Frames anzuhalten. Sie können diese Nachricht explizit oder mithilfe des [**icdrawstopemakros**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) senden.


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.

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

 

 





