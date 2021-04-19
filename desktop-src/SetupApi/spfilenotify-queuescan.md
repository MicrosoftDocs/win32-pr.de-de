---
description: Die spfilenotify- \_ Warteschlangen Benachrichtigung wird von setupscanfilequeue für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet. Dies tritt nur dann auf, wenn die Funktion setupscanfilequeue aufgerufen wurde, die das Flag SPQ \_ Scan \_ use \_ Callback angibt.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: SPFILENOTIFY_QUEUESCAN Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363293"
---
# <a name="spfilenotify_queuescan-message"></a>Spfilenotify- \_ queuescan-Nachricht

Die **spfilenotify- \_ Warteschlangen** Benachrichtigung wird von [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet. Dies tritt nur dann auf, wenn die Funktion **setupscanfilequeue** aufgerufen wurde, die das Flag SPQ \_ Scan \_ use \_ Callback angibt.


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

NULL-terminierte Zeichenfolge, die die Ziel Pfadinformationen für die Datei angibt, die im aktuellen Knoten in die Warteschlange gestellt wurde

</dd> <dt>

*Param2* 
</dt> <dd>

Wenn die Datei im aktuellen Knoten der Warteschlange verwendet wird, nimmt *Param2* den Wert der verzögerten SPQ- \_ Kopie an \_ . Wenn die Datei nicht verwendet wird, ist der Wert 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine sollte einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurückgeben.

Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , wird der Warteschlangen Scan fortgesetzt. Wenn die Routine einen anderen Fehlercode zurückgibt, wird der Warteschlangen Scan abgebrochen und [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) **false** zurückgegeben.

> [!Note]  
> Diese Benachrichtigung wird nicht von der [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) -Funktion verarbeitet.

 

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

[**Setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

