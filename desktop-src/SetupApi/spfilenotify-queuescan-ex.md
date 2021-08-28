---
description: Die SPFILENOTIFY QUEUESCAN EX-Benachrichtigung wird von \_ SetupScanFileQueue für jeden Knoten in der Kopierunterwarteschlange der Dateiwarteschlange an eine \_ Rückrufroutine gesendet.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: SPFILENOTIFY_QUEUESCAN_EX (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d151a5172918e7a7dcb13e8c480aae82da0a3ec1ffb38d26db29d63143cbc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992590"
---
# <a name="spfilenotify_queuescan_ex-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ EX-Nachricht

Die **SPFILENOTIFY \_ QUEUESCAN \_ EX-Benachrichtigung** wird von [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopierunterwarteschlange der Dateiwarteschlange an eine Rückrufroutine gesendet. Dies tritt nur auf, wenn die **SetupScanFileQueue-Funktion** aufgerufen wurde und das Flag SPQ \_ SCAN USE \_ \_ CALLBACKEX angegeben wurde.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS-Struktur.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) Das **Zielmitglied** ist der Dateiname der Zieldatei auf dem System. Der **Source-Member** ist der erwartete Pfad der Quelldatei. Das **Win32Error-Element** ist der Signaturfehler.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückrufroutine sollte einen [Systemfehlercode zurückgeben.](/windows/desktop/Debug/system-error-codes)

Wenn die Rückrufroutine NO \_ ERROR zurückgibt, wird der Warteschlangenscan fortgesetzt. Wenn die Routine einen anderen Fehlercode zurückgibt, wird der Warteschlangenscan abgebrochen, und [**SetupScanFileQueue gibt**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) FALSE zurück.

> [!Note]  
> Diese Benachrichtigung wird nicht von der [**SetupDefaultQueueCallback-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) verarbeitet.

 

## <a name="requirements"></a>Anforderungen



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

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

