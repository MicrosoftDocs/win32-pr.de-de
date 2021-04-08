---
description: Die spfilenotify-warteschlangenbenachrichtigungsinteschlange \_ \_ wird von setupscanfilequeue für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: SPFILENOTIFY_QUEUESCAN_EX Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864191"
---
# <a name="spfilenotify_queuescan_ex-message"></a>Spfilenotify \_ queuescan \_ Ex-Nachricht

Die **spfilenotify \_ \_** -warteschlangenbenachrichtigungsinteschlange wird von [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet. Dies ist nur der Fall, wenn die **setupscanfilequeue** -Funktion aufgerufen wurde, wobei das Flag SPQ \_ Scan \_ use \_ callbackex angegeben wurde.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur. Das **Zielmember** ist der Dateiname der Zieldatei im System. Der **Quell** Member ist der erwartete Pfad der Quelldatei. Der **Win32Error** -Member ist der Signatur Fehler.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückruf Routine sollte einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurückgeben.

Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , wird der Warteschlangen Scan fortgesetzt. Wenn die Routine einen anderen Fehlercode zurückgibt, wird der Warteschlangen Scan abgebrochen und [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) false zurückgegeben.

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

 

