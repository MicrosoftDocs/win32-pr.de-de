---
description: Benachrichtigt eine appbar, dass sich der automatische Ausblenden der Taskleiste oder der Always on-Top-Status&8212 geändert hat, d \# . h., der Benutzer hat den &0034 ausgewählt oder gelöscht \# . Always on-&\# 0034; oder &\# 0034; Automatisches Ausblenden&\# 0034; Kontrollkästchen auf dem Eigenschaften Blatt der Taskleiste.
title: ABN_STATECHANGE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862135"
---
# <a name="abn_statechange-message"></a>ABN \_ StateChange-Nachricht

Benachrichtigt eine appbar, dass sich der Zustand der Auto-oder Always on-Top-Taskleiste geändert hat, d. h., der Benutzer hat das Kontrollkästchen "Always on-Top" oder "automatisch ausblenden" auf der Eigenschaften Seite der Taskleiste aktiviert oder deaktiviert.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Parameter

Diese Nachricht weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Eine appbar kann diese Benachrichtigungs Meldung verwenden, um den Status der Taskleiste, wenn gewünscht, auf die Konformität festzulegen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




