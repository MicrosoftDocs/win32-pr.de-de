---
title: ICM_DRAW_START Meldung (VFW. h)
description: Die ICM \_ Draw- \_ Start Meldung benachrichtigt einen renderingtreiber, seine interne Uhr für die zeitliche Steuerung von Zeichnungs Frames zu starten. Sie können diese Nachricht explizit oder mithilfe des icdrawstart-Makros senden.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391824"
---
# <a name="icm_draw_start-message"></a>ICM- \_ Zeichnen- \_ Start Meldung

Die **ICM \_ Draw- \_ Start** Meldung benachrichtigt einen renderingtreiber, seine interne Uhr für die zeitliche Steuerung von Zeichnungs Frames zu starten. Sie können diese Nachricht explizit oder mithilfe des [**icdrawstart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) -Makros senden.


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.

Wenn der Treiber diese Nachricht empfängt, sollte er mit dem Rendern von Daten mit der Rate beginnen, die mit der [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Meldung angegeben wird.

Die **ICM \_ Draw- \_ Start** -und [**ICM \_ Draw- \_ halte**](icm-draw-stop.md) Meldungen werden nicht geschachtelt. Wenn Ihr Treiber den **ICM- \_ Zeichnen- \_ Start** empfängt, bevor das Rendering mit **ICM \_ Draw- \_ Stopp** beendet wird, sollte das Rendering mit neuen Parametern neu gestartet werden.

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

 

 





