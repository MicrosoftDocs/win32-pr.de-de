---
title: ICM_DECOMPRESS_END Meldung (Vfw.h)
description: Die ICM \_ DECOMPRESS \_ END-Nachricht benachrichtigt einen Videodekomprimierungstreiber über die Enddekomprimierung und kostenlose Ressourcen, die für die Dekomprimierung zugeordnet sind. Sie können diese Nachricht explizit oder mithilfe des IcDecompressEnd-Makros senden.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END Nachricht Windows Multimedia
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
ms.openlocfilehash: a0c877afac3db0e4cf4d7c476ca3806d2acd15bdf72764549b2958490574a4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691160"
---
# <a name="icm_decompress_end-message"></a>\_ICM DECOMPRESS \_ END-Nachricht

Die **ICM \_ DECOMPRESS \_ END-Nachricht** benachrichtigt einen Videodekomprimierungstreiber über die Enddekomprimierung und kostenlose Ressourcen, die für die Dekomprimierung zugeordnet sind. Sie können diese Nachricht explizit oder mithilfe des [**IcDecompressEnd-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) senden.


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Der Treiber sollte alle Ressourcen freigeben, die für die [**ICM \_ DECOMPRESS \_ BEGIN-Nachricht**](icm-decompress-begin.md) zugeordnet sind.

[**ICM \_ DECOMPRESS \_ BEGIN**](icm-decompress-begin.md) und **ICM \_ DECOMPRESS \_ END** werden nicht geschachtelt. Wenn Ihr Treiber **ICM \_ DECOMPRESS \_ BEGIN** empfängt, bevor die Dekomprimierung mit ICM **\_ DECOMPRESS \_ END** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.

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

 

 





