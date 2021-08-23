---
title: MM_JOY1ZMOVE Meldung (Mmsystem.h)
description: In \_ der MM-NACHRICHTMAKER1ZMOVE wird das Fenster benachrichtigt, in dem das Fenster erfasst wurde, dass sich die Position des Doppelbands auf der Z-Achse geändert hat.
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE nachricht Windows Multimedia
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
ms.openlocfilehash: b6b0efe11870ac822f7fe8aa0f7aa1deb4856bd8f1394bd1533362d78a3aee00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065540"
---
# <a name="mm_joy1zmove-message"></a>\_MM-NACHRICHT "OVE1ZMOVE"

In der **\_ MM-NACHRICHTMAKER1ZMOVE** wird das Fenster benachrichtigt, in dem das Fenster erfasst wurde, dass sich die Position des Doppelbands auf der Z-Achse geändert hat.


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifiziert die gedrückten Schaltflächen. Dies kann mindestens einer der folgenden Werte sein:



| Anforderung | Wert |
|--------------|------------------------------------|
| JOY \_ BUTTON1 | Die erste Schaltfläche wird gedrückt.  |
| JOY \_ BUTTON2 | Die zweite Schaltfläche wird gedrückt. |
| JOY \_ BUTTON3 | Die dritte Schaltfläche wird gedrückt.  |
| JOY \_ BUTTON4 | Die vierte Schaltfläche wird gedrückt. |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

Die Z-Koordinate des Doppels.

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

 

 





