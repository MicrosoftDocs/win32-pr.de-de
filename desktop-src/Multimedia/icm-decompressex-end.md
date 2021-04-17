---
title: ICM_DECOMPRESSEX_END Meldung (VFW. h)
description: Die ICM \_ decompressex- \_ Endnachricht benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung zu beenden und die für die Dekomprimierung zugewiesenen Ressourcen freizugeben. Sie können diese Nachricht explizit oder mithilfe des icdecompressexend-Makros senden.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518641"
---
# <a name="icm_decompressex_end-message"></a>ICM \_ decompressex- \_ Endmeldung

Die **ICM \_ decompressex- \_ Endnachricht** benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung zu beenden und die für die Dekomprimierung zugewiesenen Ressourcen freizugeben. Sie können diese Nachricht explizit oder mithilfe des [**icdecompressexend**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) -Makros senden.


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Der Treiber gibt alle Ressourcen frei, die für die [**ICM- \_ decompressex- \_ Begin**](icm-decompressex-begin.md) -Nachricht zugeordnet sind.

[**ICM \_ Das Beenden von "de CompressEx \_ Begin**](icm-decompressex-begin.md) " und " **ICM \_ \_** " wird nicht geschachtelt. Wenn Ihr Treiber **ICM \_ decompressex \_ Begin** empfängt, bevor die Dekomprimierung mit **ICM \_ decompressex \_ End** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.

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

 

 





