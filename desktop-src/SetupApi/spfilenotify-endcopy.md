---
description: Die SPFILENOTIFY ENDCOPY-Benachrichtigung wird an die Rückruffunktion übergeben, wenn die \_ Warteschlange einen Kopiervorgang abgeschlossen hat. Diese Benachrichtigung wird auch gesendet, wenn der Benutzer abbricht oder ein Fehler auftritt.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: SPFILENOTIFY_ENDCOPY (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87b4a53e1dc88f8cdb7d2ec790cab82b66d8698c6f45abf97e2b5ac5b8511ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665130"
---
# <a name="spfilenotify_endcopy-message"></a>SPFILENOTIFY \_ ENDCOPY-Meldung

Die **SPFILENOTIFY \_ ENDCOPY-Benachrichtigung** wird an die Rückruffunktion übergeben, wenn die Warteschlange einen Kopiervorgang abgeschlossen hat. Diese Benachrichtigung wird auch gesendet, wenn der Benutzer abbricht oder ein Fehler auftritt.


```C++
SPFILENOTIFY_ENDCOPY
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

Der Rückgabecode wird ignoriert.

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

 

 




