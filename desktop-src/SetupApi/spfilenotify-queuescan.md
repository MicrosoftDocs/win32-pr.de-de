---
description: Die Benachrichtigung SPFILENOTIFY QUEUESCAN wird von SetupScanFileQueue für jeden Knoten in der Kopierunterwarteschlange der Dateiwarteschlange an eine \_ Rückrufroutine gesendet. Dies tritt nur auf, wenn die SetupScanFileQueue-Funktion aufgerufen wurde, und das Flag SPQ \_ SCAN \_ USE \_ CALLBACK angegeben wird.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: SPFILENOTIFY_QUEUESCAN (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab9c680ff2aaa3056ab74db741a34bb9f0379ec7123821b1de4c20200997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664850"
---
# <a name="spfilenotify_queuescan-message"></a>SPFILENOTIFY \_ QUEUESCAN-Nachricht

Die **Benachrichtigung SPFILENOTIFY \_ QUEUESCAN** wird von [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopierunterwarteschlange der Dateiwarteschlange an eine Rückrufroutine gesendet. Dies tritt nur auf, wenn die **SetupScanFileQueue-Funktion** aufgerufen wurde, und das Flag SPQ \_ SCAN USE \_ \_ CALLBACK angegeben wird.


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Auf NULL beendete Zeichenfolge, die die Zielpfadinformationen für die Datei angibt, die sich in der Warteschlange des aktuellen Knotens befindet.

</dd> <dt>

*Param2* 
</dt> <dd>

Wenn die Datei im aktuellen Knoten der Warteschlange verwendet wird, verwendet *Param2* den Wert SPQ \_ DELAYED \_ COPY. Wenn die Datei nicht verwendet wird, ist der Wert 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Rückrufroutine sollte einen [Systemfehlercode zurückgeben.](/windows/desktop/Debug/system-error-codes)

Wenn die Rückrufroutine NO \_ ERROR zurückgibt, wird der Warteschlangenscan fortgesetzt. Wenn die Routine einen anderen Fehlercode zurückgibt, wird der Warteschlangenscan abgebrochen, und [**SetupScanFileQueue gibt**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) **FALSE zurück.**

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

 

