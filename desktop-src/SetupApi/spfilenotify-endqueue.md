---
description: Die Benachrichtigung SPFILENOTIFY \_ ENDQUEUE wird an die Rückrufroutine gesendet, wenn alle Vorgänge in der Warteschlange abgeschlossen wurden.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: SPFILENOTIFY_ENDQUEUE Meldung (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6192ac867b47b3e5cf9d06806bfb6eb42743aee4d97a935035fd7b44ea0e79b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665140"
---
# <a name="spfilenotify_endqueue-message"></a>SPFILENOTIFY \_ ENDQUEUE-Nachricht

Die **Benachrichtigung SPFILENOTIFY \_ ENDQUEUE** wird an die Rückrufroutine gesendet, wenn alle Vorgänge in der Warteschlange abgeschlossen wurden.


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

**TRUE,** wenn die Warteschlange erfolgreich verarbeitet wurde, andernfalls **FALSE.**

</dd> <dt>

*Param2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




