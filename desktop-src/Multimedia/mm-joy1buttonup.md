---
title: MM_JOY1BUTTONUP Meldung (Mmsystem.h)
description: In \_ der MM-NACHRICHT "MMMAKER1BUTTONUP" wird das Fenster, das die Meldung "lapDID1" erfasst hat, darüber informiert, dass eine Schaltfläche losgelassen wurde.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- MM_JOY1BUTTONUP nachricht Windows Multimedia
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
ms.openlocfilehash: c70c7b8dda57d91e595bd65223a2fd33ef904679e35a38aaacbaf263b525258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065570"
---
# <a name="mm_joy1buttonup-message"></a>\_MM-NACHRICHT "TASTE1BUTTONUP"

In der **\_ MM-NACHRICHT "MMMAKER1BUTTONUP"** wird das Fenster, das die Meldung "lapDID1" erfasst hat, darüber informiert, dass eine Schaltfläche losgelassen wurde.


```C++
MM_JOY1BUTTONUP 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifiziert die Schaltfläche, deren Zustand geändert wurde, und die gedrückten Schaltflächen. Folgende Werte sind möglich:



| Anforderung | Wert |
|-----------------|-------------------------------------------|
| JOY \_ BUTTON1CHG | Der Zustand der ersten Schaltfläche wurde geändert.  |
| JOY \_ BUTTON2CHG | Der Zustand der zweiten Schaltfläche hat sich geändert. |
| BUTTON \_ BUTTON3CHG | Die dritte Schaltfläche "button" hat den Zustand geändert.  |
| JOY \_ BUTTON4CHG | Der Zustand der vierten Schaltfläche hat sich geändert. |



 

und mindestens eine der folgenden Angaben:



| Anforderung | Wert |
|--------------|------------------------------------|
| JOY \_ BUTTON1 | Die erste Schaltfläche wird gedrückt.  |
| JOY \_ BUTTON2 | Die zweite Schaltfläche wird gedrückt. |
| JOY \_ BUTTON3 | Die dritte Schaltfläche wird gedrückt.  |
| JOY \_ BUTTON4 | Die vierte Schaltfläche wird gedrückt. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Die x-Koordinaten des Bereichs relativ zur oberen linken Ecke des Clientbereichs.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Die y-Koordinate des Bereichs relativ zur oberen linken Ecke des Clientbereichs.

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

[Multimedia-Meldungen](multimedia-joystick-messages.md)
</dt> </dl>

 

 





