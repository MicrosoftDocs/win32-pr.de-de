---
description: Die SPFILENOTIFY \_ STARTQUEUE-Benachrichtigung wird an die Rückrufroutine gesendet, wenn der Warteschlangenverpflichtungsprozess gestartet wird.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: SPFILENOTIFY_STARTQUEUE (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40d4fedde850d975edd697423339c686fe697911b9bef2fdc252baffda0158f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073210"
---
# <a name="spfilenotify_startqueue-message"></a>SPFILENOTIFY \_ STARTQUEUE-Meldung

Die **SPFILENOTIFY \_ STARTQUEUE-Benachrichtigung** wird an die Rückrufroutine gesendet, wenn der Warteschlangenverpflichtungsprozess gestartet wird.


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Handle für das Fenster, das die Dialogfelder besitzen soll, die von der Rückrufroutine generiert werden.

</dd> <dt>

*Param2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, sollte die Rückrufroutine [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)aufrufen, den Fehler angeben und dann 0 (null) zurückgeben. Die [**SetupCommitFileQueue-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt **FALSE** zurück, und ein nachfolgender Aufruf von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den von der Rückrufroutine festgelegten Fehlercode zurück.

Wenn kein Fehler auftritt, sollte die Rückrufroutine einen Wert ungleich 0 (null) zurückgeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
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

 

