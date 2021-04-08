---
description: Die spfilenotify \_ endsubqueue-Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange alle Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren abschließt.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: SPFILENOTIFY_ENDSUBQUEUE Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050518"
---
# <a name="spfilenotify_endsubqueue-message"></a>Spfilenotify- \_ endsubqueue-Nachricht

Die **spfilenotify \_ endsubqueue** -Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange alle Vorgänge in der unter Warteschlange löschen, umbenennen oder kopieren abschließt.


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Die unter Warteschlange wurde abgeschlossen. Dieser Parameter kann einer der folgenden Werte sein: fileOp \_ Delete, fileOp \_ Rename oder fileOp \_ Copy.

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

 

 




