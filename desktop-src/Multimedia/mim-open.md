---
title: MIM_OPEN Meldung (Mmsystem.h)
description: Die MIM \_ OPEN-Nachricht wird an eine RÜCKRUFFUNKTION für die EINGABEEINGABE gesendet, wenn ein EINGABEGERÄT geöffnet wird.
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- MIM_OPEN nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15cacc21fd31810adf3188cb1ba267c9727715a0426c98d18f231eeec19b9691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428120"
---
# <a name="mim_open-message"></a>\_MIM OPEN-Nachricht

Die **MIM \_ OPEN-Nachricht** wird an eine RÜCKRUFFUNKTION für die EINGABEEINGABE gesendet, wenn ein EINGABEGERÄT geöffnet wird.


```C++
MIM_OPEN 
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

 

 





