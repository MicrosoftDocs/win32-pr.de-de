---
title: MM_JOY1MOVE (Mmsystem.h)
description: Die MM-MELDUNG VOM 1MOVE-Fenster benachrichtigt das Fenster, in dem die 30%000%000er-IdID1 erfasst wurde, dass sich die Position des 500-00-000-Automaten \_ geändert hat.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8c8a71bc91b541bc17017fc2673bb6c0ed7e84a2de44ff312954b8f9915dc57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802445"
---
# <a name="mm_joy1move-message"></a>MM \_ MM MM1MOVE-Nachricht

Die **\_ MM-MELDUNG VOM 1MOVE-Fenster** benachrichtigt das Fenster, in dem die 30%000%000er-IdID1 erfasst wurde, dass sich die Position des 500-00-000-Automaten geändert hat.


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifiziert die schaltflächen, die gedrückt werden. Dies kann einer oder mehrere der folgenden Werte sein:



| Anforderung | Wert |
|--------------|------------------------------------|
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 1" | Die erste Schaltfläche wird gedrückt.  |
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 2" | Die zweite Schaltfläche wird gedrückt. |
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 3" | Die dritte Schaltfläche wird gedrückt.  |
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 4" | Die vierte Schaltfläche wird gedrückt. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Die x-Koordinaten des -Bereichs relativ zur oberen linken Ecke des Clientbereichs.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Die y-Koordinate des -Bereichs relativ zur oberen linken Ecke des Clientbereichs.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Multimediameldungen](multimedia-joystick-messages.md)
</dt> </dl>

 

 





