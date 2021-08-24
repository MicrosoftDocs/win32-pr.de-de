---
title: ICM_COMPRESS_END (Vfw.h)
description: Die ICM COMPRESS END-Nachricht benachrichtigt einen Videokomprimierungstreiber, um die Komprimierung zu beenden und Ressourcen frei zu \_ \_ machen, die für die Komprimierung zugeordnet sind. Sie können diese Nachricht explizit oder mithilfe des ICCompressEnd-Makros senden.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END von Windows Multimedia
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
ms.openlocfilehash: 9c320190da37d286db1c20329a849ea09ac6d915087e9d3bdbb2333d31cec3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785040"
---
# <a name="icm_compress_end-message"></a>\_ICM COMPRESS \_ END-Nachricht

Die **ICM \_ COMPRESS \_ END-Nachricht** benachrichtigt einen Videokomprimierungstreiber, um die Komprimierung und die für die Komprimierung reservierten freien Ressourcen zu beenden. Sie können diese Nachricht explizit oder mithilfe des [**ICCompressEnd-Makros**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) senden.


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich oder andernfalls ein Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

VCM speichert die Einstellungen der letzten ICM [**\_ COMPRESS \_ BEGIN-Nachricht.**](icm-compress-begin.md) **ICM \_ COMPRESS \_ BEGIN und** ICM COMPRESS **\_ \_ END** werden nicht geschachtelt. Wenn Ihr Treiber ICM **\_ COMPRESS \_ BEGIN** empfängt, bevor die Komprimierung mit ICM COMPRESS **\_ \_ END** beendet wird, sollte die Komprimierung mit neuen Parametern neu gestartet werden.

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

 

 





