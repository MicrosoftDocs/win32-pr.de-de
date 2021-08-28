---
title: ICM_DRAW_START-Nachricht (Vfw.h)
description: Die ICM \_ DRAW \_ START-Nachricht benachrichtigt einen Renderingtreiber, seine interne Uhr für die Zeitliche Steuerung von Zeichnungsframes zu starten. Sie können diese Nachricht explizit oder mithilfe des ICDrawStart-Makros senden.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START nachricht Windows Multimedia
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
ms.openlocfilehash: 720d8c2f919d2b00955892a42ba8fca95b2b426c3cbb396aa4ac71a5cf912307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690950"
---
# <a name="icm_draw_start-message"></a>\_ICM DRAW \_ START-Nachricht

Die **ICM \_ DRAW \_ START-Nachricht** benachrichtigt einen Renderingtreiber, seine interne Uhr für die Zeitliche Steuerung von Zeichnungsframes zu starten. Sie können diese Nachricht explizit oder mithilfe des [**ICDrawStart-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) senden.


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung wird von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.

Wenn der Treiber diese Nachricht empfängt, sollte er mit dem Rendern von Daten mit der mit der [**ICM \_ DRAW \_ BEGIN-Nachricht**](icm-draw-begin.md) angegebenen Rate beginnen.

Die **ICM \_ DRAW \_ START-** und [**ICM DRAW \_ \_ STOP-Meldungen**](icm-draw-stop.md) werden nicht geschachtelt. Wenn Ihr Treiber **ICM \_ DRAW \_ START** empfängt, bevor das Rendering mit **ICM DRAW \_ \_ STOP** beendet wird, sollte das Rendering mit neuen Parametern neu gestartet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





