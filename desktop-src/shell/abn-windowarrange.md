---
description: Benachrichtigt eine appbar, dass der Benutzer den Befehl Cascade, Tile horizontal oder Tile vertikal im Kontextmenü der Taskleiste ausgewählt hat.
title: ABN_WINDOWARRANGE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525421"
---
# <a name="abn_windowarrange-message"></a>ABN \_ windowarrange-Meldung

Benachrichtigt eine appbar, dass der Benutzer den Befehl Cascade, Tile horizontal oder Tile vertikal im Kontextmenü der Taskleiste ausgewählt hat.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

Ein Flag, das angibt, ob der Cascade-oder Tile-Vorgang beginnt. Dieser Parameter ist **true** , wenn der Vorgang beginnt und die Fenster noch nicht verschoben wurden. Dies ist **false** , wenn der Vorgang abgeschlossen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das System sendet diese Benachrichtigungs Meldung zunächst zweimal, wobei *LPARAM* auf **true** festgelegt ist, und wenn *LPARAM* auf **false** festgelegt ist. Die erste Benachrichtigung wird gesendet, bevor die Fenster kaskadiert oder gekachelt werden, und die zweite Benachrichtigung wird gesendet, nachdem der Cascade-oder Tile-Vorgang aufgetreten ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




