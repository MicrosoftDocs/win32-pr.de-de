---
title: MM_JOY1BUTTONDOWN Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY1BUTTONDOWN benachrichtigt das Fenster, das den Joystick JOYSTICKID1 aufgezeichnet hat, dass eine Schaltfläche gedrückt wurde.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- MM_JOY1BUTTONDOWN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cefb70e5dd47fc14b39dcdeb59043b6827e7b89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475504"
---
# <a name="mm_joy1buttondown-message"></a>MM \_ JOY1BUTTONDOWN Meldung

Die Meldung **mm \_ JOY1BUTTONDOWN** benachrichtigt das Fenster, das den Joystick JOYSTICKID1 aufgezeichnet hat, dass eine Schaltfläche gedrückt wurde.


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*Schaltflächen*
</dt> <dd>

Gibt die Schaltfläche an, die den Zustand geändert hat, und die gedrückten Schaltflächen. Folgende Werte sind möglich:



| Anforderung | Wert |
|-----------------|-------------------------------------------|
| Freude \_ BUTTON1CHG | Der erste Joystick Schaltfläche hat den Zustand geändert.  |
| Freude \_ BUTTON2CHG | Die zweite Schaltfläche "Joystick" hat den Zustand geändert. |
| Freude \_ BUTTON3CHG | Die dritte Schaltfläche "Joystick" hat den Zustand geändert.  |
| Freude \_ BUTTON4CHG | Der vierte Joystick Schaltfläche hat den Zustand geändert. |



 

und eine oder mehrere der folgenden Aktionen:



| Anforderung | Wert |
|--------------|------------------------------------|
| Freude \_ Button1 | Die erste Joystick Schaltfläche wird gedrückt.  |
| Freude \_ Button2 | Die zweite Joystick Schaltfläche wird gedrückt. |
| Freude \_ BUTTON3 | Die dritte Joystick Schaltfläche wird gedrückt.  |
| Freude \_ BUTTON4 | Fourth Joystick Schaltfläche wird gedrückt. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*
</dt> <dd>

Die x-Koordinate des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.

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

 

 





