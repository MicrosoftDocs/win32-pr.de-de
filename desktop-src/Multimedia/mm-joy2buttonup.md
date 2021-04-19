---
title: MM_JOY2BUTTONUP Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm JOY2BUTTONUP benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass eine Schaltfläche freigegeben wurde.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346772"
---
# <a name="mm_joy2buttonup-message"></a>MM \_ JOY2BUTTONUP Meldung

Die Meldung **mm \_ JOY2BUTTONUP** benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass eine Schaltfläche freigegeben wurde.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

**Schaltflächen** 
</dt> <dd>

Gibt die Schaltfläche an, die den Zustand geändert hat, und die gedrückten Schaltflächen. Folgende Werte sind möglich:



| Wert                                                                                                                                                            | Bedeutung                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**Freude \_ BUTTON1CHG**</dt> </dl> | Der erste Joystick Schaltfläche hat den Zustand geändert.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**Freude \_ BUTTON2CHG**</dt> </dl> | Die zweite Schaltfläche "Joystick" hat den Zustand geändert.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**Freude \_ BUTTON3CHG**</dt> </dl> | Die dritte Schaltfläche "Joystick" hat den Zustand geändert.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**Freude \_ BUTTON4CHG**</dt> </dl> | Der vierte Joystick Schaltfläche hat den Zustand geändert.<br/> |



 

und eine oder mehrere der folgenden Aktionen:



| Wert                                                                                                                                                   | Bedeutung                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**Freude \_ Button1**</dt> </dl> | Die erste Joystick Schaltfläche wird gedrückt.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**Freude \_ Button2**</dt> </dl> | Die zweite Joystick Schaltfläche wird gedrückt.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**Freude \_ BUTTON3**</dt> </dl> | Die dritte Joystick Schaltfläche wird gedrückt.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**Freude \_ BUTTON4**</dt> </dl> | Fourth Joystick Schaltfläche wird gedrückt.<br/> |



 

</dd> <dt>

**XPos** 
</dt> <dd>

Die x-Koordinaten des Joysticks in Relation zur oberen linken Ecke des Client Bereichs.

</dd> <dt>

**YPos** 
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

 

 





