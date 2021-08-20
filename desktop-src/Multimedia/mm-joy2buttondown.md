---
title: MM_JOY2BUTTONDOWN (Mmsystem.h)
description: Die MELDUNG MM MM2BUTTONDOWN benachrichtigt das Fenster, in dem die 1000er-Idid2 erfasst wurde, dass eine \_ Schaltfläche gedrückt wurde.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- MM_JOY2BUTTONDOWN von Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e9ad78e914fb74e51f8ebe7a47a65677ac06d27d53eb8f64739ba641f235b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137201"
---
# <a name="mm_joy2buttondown-message"></a>MM \_ MM MM2BUTTONDOWN-Nachricht

Die **MELDUNG \_ MM MM2BUTTONDOWN** benachrichtigt das Fenster, in dem die 1000er-Idid2 erfasst wurde, dass eine Schaltfläche gedrückt wurde.


```C++
MM_JOY2BUTTONDOWN 
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

 

 





