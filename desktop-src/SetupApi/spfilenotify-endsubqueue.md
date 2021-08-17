---
description: Die SPFILENOTIFY \_ ENDSUBQUEUE-Benachrichtigung wird an die Rückruffunktion gesendet, wenn die Warteschlange alle Vorgänge in der Unterwarteschlange zum Löschen, Umbenennen oder Kopieren abschließt.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: SPFILENOTIFY_ENDSUBQUEUE Meldung (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72645aafbe94e3f90d11f8ccf65ed8c6006301db811bccd80936cadbf0478dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964549"
---
# <a name="spfilenotify_endsubqueue-message"></a>SPFILENOTIFY \_ ENDSUBQUEUE-Nachricht

Die **SPFILENOTIFY \_ ENDSUBQUEUE-Benachrichtigung** wird an die Rückruffunktion gesendet, wenn die Warteschlange alle Vorgänge in der Unterwarteschlange zum Löschen, Umbenennen oder Kopieren abschließt.


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Abgeschlossene Unterabfrage. Dieser Parameter kann einer der folgenden Werte sein: FILEOP \_ DELETE, FILEOP \_ RENAME oder FILEOP \_ COPY.

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
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

 

 




