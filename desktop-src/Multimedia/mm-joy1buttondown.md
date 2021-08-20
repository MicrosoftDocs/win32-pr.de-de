---
title: MM_JOY1BUTTONDOWN (Mmsystem.h)
description: Die MELDUNG MM MM1BUTTONDOWN benachrichtigt das Fenster, in dem die BER-ID1 erfasst wurde, dass eine \_ Schaltfläche gedrückt wurde.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- MM_JOY1BUTTONDOWN von Windows Multimedia
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
ms.openlocfilehash: 2d2399eca0de21014b97c9156e6a16349fc5b0b5407b64b022eb077fd59d0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137191"
---
# <a name="mm_joy1buttondown-message"></a>MM \_ MM MM1BUTTONDOWN-Meldung

Die **MELDUNG \_ MM MM1BUTTONDOWN** benachrichtigt das Fenster, in dem die BER-ID1 erfasst wurde, dass eine Schaltfläche gedrückt wurde.


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifiziert die Schaltfläche, die den Zustand geändert hat, und die schaltflächen, die gedrückt werden. Folgende Werte sind möglich:



| Anforderung | Wert |
|-----------------|-------------------------------------------|
| SCHALTFLÄCHE \_ "BUTTON1CHG" | Die erste Schaltfläche hat den Zustand geändert.  |
| SCHALTFLÄCHE \_ "BUTTON2CHG" | Die zweite Schaltfläche hat den Zustand geändert. |
| SCHALTFLÄCHE \_ "BUTTON3CHG" | Die dritte Schaltfläche hat den Zustand geändert.  |
| JOY \_ BUTTON4CHG | Die vierte Schaltfläche hat den Zustand geändert. |



 

und mindestens eines der folgenden:



| Anforderung | Wert |
|--------------|------------------------------------|
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 1" | Die erste Schaltfläche wird gedrückt.  |
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 2" | Die zweite Schaltfläche wird gedrückt. |
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 3" | Die dritte Schaltfläche wird gedrückt.  |
| SCHALTFLÄCHE \_ "SCHALTFLÄCHE 4" | Die vierte Schaltfläche wird gedrückt. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Die x-Koordinate der -Koordinate relativ zur oberen linken Ecke des Clientbereichs.

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

 

 





