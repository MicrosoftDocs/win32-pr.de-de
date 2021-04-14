---
title: ICM_COMPRESS_END Meldung (VFW. h)
description: Die ICM \_ -Komprimierungs \_ Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Komprimierung zu beenden und die für die Komprimierung zugewiesenen Ressourcen freizugeben Sie können diese Nachricht explizit oder mithilfe des iccompressend-Makros senden.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476008"
---
# <a name="icm_compress_end-message"></a>ICM- \_ Komprimierungs \_ Nachricht beenden

Die **ICM \_ - \_** Komprimierungs Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Komprimierung zu beenden und die für die Komprimierung zugewiesenen Ressourcen freizugeben Sie können diese Nachricht explizit oder mithilfe des [**iccompressend**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) -Makros senden.


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

VCM speichert die Einstellungen der letzten [**ICM- \_ Komprimierungs \_ Begin**](icm-compress-begin.md) -Nachricht. **ICM \_ Das Komprimieren von \_ Begin** und **ICM- \_ Komprimierung \_** wird nicht geschachtelt. Wenn der Treiber **ICM \_ Compress \_ Begin** empfängt, bevor die Komprimierung mit **ICM- \_ Komprimierung \_ beendet** wird, sollte die Komprimierung mit neuen Parametern neu gestartet werden.

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

 

 





