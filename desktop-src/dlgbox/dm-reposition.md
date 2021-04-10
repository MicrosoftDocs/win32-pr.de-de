---
title: DM_REPOSITION Meldung (Winuser. h)
description: Positioniert ein Dialogfeld der obersten Ebene neu, sodass es in den Desktop Bereich passt. Eine Anwendung kann diese Nachricht nach der Größe der Größe an ein Dialogfeld senden, um sicherzustellen, dass das gesamte Dialogfeld sichtbar bleibt.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Dialog Felder DM_REPOSITION Meldung
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040963"
---
# <a name="dm_reposition-message"></a>DM- \_ neupositions Meldung

Positioniert ein Dialogfeld der obersten Ebene neu, sodass es in den Desktop Bereich passt. Eine Anwendung kann diese Nachricht nach der Größe der Größe an ein Dialogfeld senden, um sicherzustellen, dass das gesamte Dialogfeld sichtbar bleibt.


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Diese Meldung hat keine Auswirkung, wenn das Dialogfeld ein untergeordnetes Fenster ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Dialogfelder](dialog-boxes.md)
</dt> </dl>

 

 





