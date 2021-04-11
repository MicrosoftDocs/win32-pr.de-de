---
title: MM_JOY2MOVE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY2MOVE benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks geändert hat.
ms.assetid: 8dc1c092-3947-43d5-8504-a4e4e121fbcb
keywords:
- MM_JOY2MOVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY2MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8921f0ae76d05c429d6750944a26662c1276af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103035"
---
# <a name="mm_joy2move-message"></a>MM \_ JOY2MOVE Meldung

Die Meldung **mm \_ JOY2MOVE** benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks geändert hat.


```C++
MM_JOY2MOVE 
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

 

 





