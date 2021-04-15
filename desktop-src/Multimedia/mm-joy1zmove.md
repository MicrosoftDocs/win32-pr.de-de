---
title: MM_JOY1ZMOVE Meldung (MMSYSTEM. h)
description: Die mm \_ JOY1ZMOVE-Meldung benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID1, dass sich die Position des Joysticks auf der z-Achse geändert hat.
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d4db3db8c1817f0502ce14cc5328ad666b32c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479383"
---
# <a name="mm_joy1zmove-message"></a>MM \_ JOY1ZMOVE Meldung

Die **mm \_ JOY1ZMOVE** -Meldung benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID1, dass sich die Position des Joysticks auf der z-Achse geändert hat.


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
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

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*ZPOS*
</dt> <dd>

Die z-Koordinate des Joysticks.

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

 

 





