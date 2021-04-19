---
description: Die spfilenotify- \_ Benachrichtigung startsubqueue wird an die Rückruffunktion gesendet, wenn die Warteschlange mit der Verarbeitung der Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren beginnt.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: SPFILENOTIFY_STARTSUBQUEUE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355392"
---
# <a name="spfilenotify_startsubqueue-message"></a>Spfilenotify- \_ startsubqueue-Nachricht

Die **spfilenotify-Benachrichtigung \_ startsubqueue** wird an die Rückruffunktion gesendet, wenn die Warteschlange mit der Verarbeitung der Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren beginnt.


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Unter Warteschlange, die gestartet wurde. Dieser Parameter kann einer der Werte fileOp \_ Delete, fileOp \_ Rename oder fileOp \_ Copy sein.

</dd> <dt>

*Param2* 
</dt> <dd>

Anzahl der Datei Kopier-, Umbenennungs-oder Löschvorgänge in der unter Warteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, sollte die Rückruf Routine [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)aufrufen und den Fehler angeben und dann 0 (null) zurückgeben. Die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion gibt " **false** " zurück, und ein nachfolgendes Aufrufen von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt den von der Rückruf Routine festgelegten Fehlercode zurück.

Wenn kein Fehler auftritt, sollte die Rückruf Routine einen Wert ungleich 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**Setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

