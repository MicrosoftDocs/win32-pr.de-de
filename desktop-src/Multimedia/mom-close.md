---
title: MOM_CLOSE Meldung (MMSYSTEM. h)
description: Die MOM- \_ Schließen-Nachricht wird an eine Funktion für die Ausgabe Rückruffunktion von MIDI gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957086"
---
# <a name="mom_close-message"></a>Meldung zum Schließen der MOM \_

Die **MOM- \_ Schließen** -Nachricht wird an eine Funktion für die Ausgabe Rückruffunktion von MIDI gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Bleiben Verwenden Sie nicht.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
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

 

 





