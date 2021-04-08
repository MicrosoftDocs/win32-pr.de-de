---
title: MOM_OPEN Meldung (MMSYSTEM. h)
description: Die MOM- \_ Öffnungs Nachricht wird an eine Funktion für die Funktion "MIDI-Ausgabe" gesendet, wenn ein Ausgabegerät von MIDI geöffnet wird.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- MOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743361"
---
# <a name="mom_open-message"></a>MOM- \_ Öffnungs Nachricht

Die **MOM- \_ Öffnungs** Nachricht wird an eine Funktion für die Funktion "MIDI-Ausgabe" gesendet, wenn ein Ausgabegerät von MIDI geöffnet wird.


```C++
MOM_OPEN 
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

 

 





