---
title: MM_MOM_OPEN Meldung (MMSYSTEM. h)
description: Die \_ Meldung zum \_ Öffnen von mm MOM wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geöffnet wird.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- MM_MOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475078"
---
# <a name="mm_mom_open-message"></a>Meldung zum Öffnen von mm \_ MOM \_

Die Meldung zum **\_ \_ Öffnen von mm MOM** wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geöffnet wird.


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*houtput*
</dt> <dd>

Handle für das MIDI-Ausgabegerät.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Bleiben Verwenden Sie nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MIDI-Nachrichten](midi-messages.md)
</dt> </dl>

 

 





