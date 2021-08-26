---
title: ICM_DRAW_STOP-Nachricht (Vfw.h)
description: Die ICM \_ DRAW \_ STOP-Nachricht benachrichtigt einen Renderingtreiber, seine interne Uhr für die Zeitsteuerung von Zeichnungsframes zu beenden. Sie können diese Nachricht explizit oder mithilfe des ICDrawStop-Makros senden.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP nachricht Windows Multimedia
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
ms.openlocfilehash: 41bdb8fbc9a0cddf470733fa35b2f25dc62675175cbb40c427d0b160074c5409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038790"
---
# <a name="icm_draw_stop-message"></a>\_ICM DRAW \_ STOP-Nachricht

Die **ICM \_ DRAW \_ STOP-Nachricht** benachrichtigt einen Renderingtreiber, seine interne Uhr für die Zeitsteuerung von Zeichnungsframes zu beenden. Sie können diese Nachricht explizit oder mithilfe des [**ICDrawStop-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) senden.


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung wird von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





