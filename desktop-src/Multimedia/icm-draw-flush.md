---
title: ICM_DRAW_FLUSH Meldung (VFW. h)
description: Mit der ICM \_ Draw \_ Flush-Meldung wird ein renderingertreiber benachrichtigt, um den Inhalt aller Bild Puffer zu rendern, die darauf warten, gezeichnet zu werden. Sie können diese Nachricht explizit oder mithilfe des icdrawflush-Makros senden.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344676"
---
# <a name="icm_draw_flush-message"></a>ICM-Zeichnungs Leerungs \_ \_ Meldung

Mit der **ICM \_ Draw \_ Flush** -Meldung wird ein renderingertreiber benachrichtigt, um den Inhalt aller Bild Puffer zu rendern, die darauf warten, gezeichnet zu werden. Sie können diese Nachricht explizit oder mithilfe des [**icdrawflush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) -Makros senden.


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nur von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.

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

 

 





