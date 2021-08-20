---
description: Benachrichtigt eine Appbar darüber, dass sich der Automatischehide- oder Always On-Top-Zustand der Taskleiste&\# 8212 geändert hat. Das heißt, der Benutzer hat die &\# 0034 ausgewählt oder gelöscht. Always On top&\# 0034; oder &\# 0034; Automatisches Ausblenden&\# 0034;-Kontrollkästchen auf dem Eigenschaftenblatt der Taskleiste.
title: ABN_STATECHANGE-Nachricht (Shellapi.h)
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
ms.openlocfilehash: b0017930bd3cf4c8cba356206cfa2207df04ea9c203018703a5f3064d0abb11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861582"
---
# <a name="abn_statechange-message"></a>ABN \_ STATECHANGE-Nachricht

Benachrichtigt eine Appbar, dass sich der automatische Oder der Always On-Top-Zustand der Taskleiste geändert hat, d. h., der Benutzer hat das Kontrollkästchen "Immer oben" oder "Automatisch ausblenden" auf dem Eigenschaftenblatt der Taskleiste aktiviert oder gelöscht.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Parameter

Diese Nachricht enthält keine Parameter.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Appbar kann diese Benachrichtigung verwenden, um bei Bedarf ihren Zustand so festzulegen, dass er dem Zustand der Taskleiste entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




