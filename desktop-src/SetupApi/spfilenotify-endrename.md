---
description: Die Benachrichtigung SPFILENOTIFY ENDRENAME wird an die Rückrufroutine gesendet, wenn die \_ Warteschlange einen Umbenennungsvorgang abgeschlossen hat. Diese Benachrichtigung wird auch gesendet, wenn der Benutzer abbricht oder ein Fehler auftritt.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: SPFILENOTIFY_ENDRENAME (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f34ad30cc103e8a13277d3383bad8c2e46409eaabe6f957ace27aebc9759990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683120"
---
# <a name="spfilenotify_endrename-message"></a>SPFILENOTIFY \_ ENDRENAME-Meldung

Die **Benachrichtigung SPFILENOTIFY \_ ENDRENAME** wird an die Rückrufroutine gesendet, wenn die Warteschlange einen Umbenennungsvorgang abgeschlossen hat. Diese Benachrichtigung wird auch gesendet, wenn der Benutzer abbricht oder ein Fehler auftritt.


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FILEPATHS-Struktur.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) Das **Win32Error-Element** der **FILEPATHS-Struktur** gibt das Ergebnis des Kopiervorgang an.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**Filepaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




