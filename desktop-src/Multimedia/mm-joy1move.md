---
title: MM_JOY1MOVE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY1MOVE benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID1, dass sich die Position des Joysticks geändert hat.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE-Nachricht (Multimedia)
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
ms.openlocfilehash: a78753bd55f6682b3ac3f1514356d93cb455d162
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337713"
---
# <a name="mm_joy1move-message"></a>MM \_ JOY1MOVE Meldung

Die Meldung **mm \_ JOY1MOVE** benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID1, dass sich die Position des Joysticks geändert hat.


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*Schaltflächen*
</dt> <dd>

Gibt die Schaltflächen an, die gedrückt werden. Folgende Werte sind möglich:



| Anforderung | Wert |
|--------------|------------------------------------|
| Freude \_ Button1 | Die erste Joystick Schaltfläche wird gedrückt.  |
| Freude \_ Button2 | Die zweite Joystick Schaltfläche wird gedrückt. |
| Freude \_ BUTTON3 | Die dritte Joystick Schaltfläche wird gedrückt.  |
| Freude \_ BUTTON4 | Fourth Joystick Schaltfläche wird gedrückt. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*
</dt> <dd>

Die x-Koordinaten des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*
</dt> <dd>

Die y-Koordinate des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Joystick](joysticks.md)
</dt> <dt>

[Multimedia-Joystick Nachrichten](multimedia-joystick-messages.md)
</dt> </dl>

 

 





