---
title: MM_MOM_CLOSE Meldung (MMSYSTEM. h)
description: Die \_ Meldung zum \_ Schließen von mm MOM wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475501"
---
# <a name="mm_mom_close-message"></a>Meldung zum Schließen von mm \_ MOM \_

Die Meldung zum **\_ \_ Schließen von mm MOM** wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.


```C++
MM_MOM_CLOSE 
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

## <a name="remarks"></a>Bemerkungen

Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.

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

 

 





