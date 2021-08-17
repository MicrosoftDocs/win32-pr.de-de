---
title: MIM_CLOSE Meldung (Mmsystem.h)
description: Die MIM \_ CLOSE-Nachricht wird an eine RÜCKRUFFUNKTION für die EINGABEEINGABE gesendet, wenn ein EINGABEGERÄT geschlossen wird.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- MIM_CLOSE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b1509573d5c69fd2e95cabeb8ba2c4059d5d37c9cfe3c957ec8b8f75f5abfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428170"
---
# <a name="mim_close-message"></a>\_MIM CLOSE-Nachricht

Die **MIM \_ CLOSE-Nachricht** wird an eine RÜCKRUFFUNKTION für die EINGABEEINGABE gesendet, wenn ein EINGABEGERÄT geschlossen wird.


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Reserviert; nicht verwenden.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reserviert; nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Gerätehandle ist nach dem Senden dieser Nachricht nicht mehr gültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Music Instrument Digital Interface (INSTRUMENTS)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MELDUNGSMELDUNGEN](midi-messages.md)
</dt> </dl>

 

 





