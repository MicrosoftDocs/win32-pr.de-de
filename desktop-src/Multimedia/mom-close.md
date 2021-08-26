---
title: MOM_CLOSE (Mmsystem.h)
description: Die MOM \_ CLOSE-Nachricht wird an eine RÜCKRUF-Ausgaberückruffunktion gesendet, wenn ein OUTPUT-Ausgabegerät geschlossen wird.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE-Nachricht Windows Multimedia
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
ms.openlocfilehash: dbabd0cae61c1b1ea3d88df3cd2e52524b779eb7cdb5ac2c1e1a371546724f44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038870"
---
# <a name="mom_close-message"></a>MOM \_ CLOSE-Nachricht

Die **MOM \_ CLOSE-Nachricht** wird an eine RÜCKRUF-Ausgaberückruffunktion gesendet, wenn ein OUTPUT-Ausgabegerät geschlossen wird.


```C++
MOM_CLOSE 
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

Das Gerätehandy ist nach dem Senden dieser Nachricht nicht mehr gültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MESSAGES-Meldungen](midi-messages.md)
</dt> </dl>

 

 





