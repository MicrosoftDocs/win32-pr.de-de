---
title: ICM_DECOMPRESS_END Meldung (VFW. h)
description: Die ICM \_ -Dekomprimierungs \_ Nachricht benachrichtigt einen Video-Dekomprimierungs Treiber, um die Dekomprimierung und die für die Dekomprimierung zugeordneten Ressourcen freizugeben. Sie können diese Nachricht explizit oder mithilfe des icdecompressend-Makros senden.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742969"
---
# <a name="icm_decompress_end-message"></a>ICM- \_ Dekomprimierungs \_ Nachricht beenden

Die **ICM- \_ Dekomprimierungs \_** Nachricht benachrichtigt einen Video-Dekomprimierungs Treiber, um die Dekomprimierung und die für die Dekomprimierung zugeordneten Ressourcen freizugeben. Sie können diese Nachricht explizit oder mithilfe des [**icdecompressend**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) -Makros senden.


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Der Treiber sollte alle Ressourcen freigeben, die für die [**ICM- \_ Dekomprimierungs- \_ Begin**](icm-decompress-begin.md) -Nachricht reserviert wurden.

[**ICM \_ \_**](icm-decompress-begin.md) Das **\_ \_ Beenden** der BEGIN-und ICM-Debug wird nicht geschachtelt. Wenn der Treiber **ICM \_ Decompress \_** vor dem Beenden der Dekomprimierung mit **ICM \_ Decompress \_ Beenden** empfängt, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.

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

 

 





