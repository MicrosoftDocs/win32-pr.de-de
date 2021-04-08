---
title: ICM_DRAW_END Meldung (VFW. h)
description: Die ICM- \_ Meldung zum Zeichnen des \_ Endes benachrichtigt einen renderingtreiber, das aktuelle Bild auf dem Bildschirm zu dekomprimieren und Ressourcen freizugeben, die für das Dekomprimieren und zeichnen reserviert wurden. Sie können diese Nachricht explizit oder mithilfe des icdrawend-Makros senden.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741961"
---
# <a name="icm_draw_end-message"></a>ICM \_ - \_ zeichenendenachricht

Die **ICM-Meldung zum \_ Zeichnen des \_ Endes** benachrichtigt einen renderingtreiber, das aktuelle Bild auf dem Bildschirm zu dekomprimieren und Ressourcen freizugeben, die für das Dekomprimieren und zeichnen reserviert wurden. Sie können diese Nachricht explizit oder mithilfe des [**icdrawend-**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) Makros senden.


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ICM \_ Draw- \_ Begin**](icm-draw-begin.md) -und **ICM \_ Draw \_** -Meldungen werden nicht geschachtelt. Wenn der Treiber den **ICM- \_ Zeichnen- \_ Anfang** erhält, bevor die Dekomprimierung mit dem **ICM- \_ Zeichnungs \_ Ende** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet

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

 

 





