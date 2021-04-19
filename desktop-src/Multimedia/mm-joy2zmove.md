---
title: MM_JOY2ZMOVE Meldung (MMSYSTEM. h)
description: Die mm \_ JOY2ZMOVE-Meldung benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks auf der z-Achse geändert hat.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- MM_JOY2ZMOVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342491"
---
# <a name="mm_joy2zmove-message"></a>MM \_ JOY2ZMOVE Meldung

Die **mm \_ JOY2ZMOVE** -Meldung benachrichtigt das Fenster, das den Joystick aufgezeichnet hat JOYSTICKID2, dass sich die Position des Joysticks auf der z-Achse geändert hat.


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*Schaltflächen*
</dt> <dd>

Gibt die Schaltflächen an, die gedrückt werden. Es kann sich um einen oder mehrere der folgenden Werte handeln:



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

 

 





