---
title: WIM_OPEN Meldung (Mmsystem.h)
description: Die WIM \_ OPEN-Nachricht wird an eine Waveform-Audio-Eingaberückruffunktion gesendet, wenn ein Waveform-Audio-Eingabegerät geöffnet wird.
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- WIM_OPEN Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337d86c7c1262094993bbac4973b96f1d442149b07d3a48a3e88bd384fee2997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369753"
---
# <a name="wim_open-message"></a>WIM \_ OPEN-Nachricht

Die **WIM \_ OPEN-Nachricht** wird an eine Waveform-Audio-Eingaberückruffunktion gesendet, wenn ein Waveform-Audio-Eingabegerät geöffnet wird.


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reserviert; muss 0 (null) sein.

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

[Waveform-Audio](waveform-audio.md)
</dt> <dt>

[Wellenformnachrichten](waveform-messages.md)
</dt> </dl>

 

 





