---
description: Die spfilenotify- \_ EndCopy-Benachrichtigung wird an die Rückruffunktion übermittelt, wenn die Warteschlange einen Kopiervorgang abschließt. Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: SPFILENOTIFY_ENDCOPY Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354028"
---
# <a name="spfilenotify_endcopy-message"></a>Spfilenotify- \_ endkopier Nachricht

Die **spfilenotify- \_ EndCopy** -Benachrichtigung wird an die Rückruffunktion übermittelt, wenn die Warteschlange einen Kopiervorgang abschließt. Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur. Der **Win32Error** -Member der **FilePath** -Struktur gibt das Ergebnis des Kopiervorgangs an.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**Setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




