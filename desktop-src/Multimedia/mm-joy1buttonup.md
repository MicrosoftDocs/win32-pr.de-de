---
title: MM_JOY1BUTTONUP Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY1BUTTONUP benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID1, dass eine Schaltfläche freigegeben wurde.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- MM_JOY1BUTTONUP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a5d954b9b879f87c5e8ffe2d0774d0d1d85a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106526"
---
# <a name="mm_joy1buttonup-message"></a>MM \_ JOY1BUTTONUP Meldung

Die Meldung **mm \_ JOY1BUTTONUP** benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID1, dass eine Schaltfläche freigegeben wurde.


```C++
MM_JOY1BUTTONUP 
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

 

 





