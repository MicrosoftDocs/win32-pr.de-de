---
title: MM_WIM_CLOSE Meldung (Mmsystem.h)
description: Die MM \_ WIM \_ CLOSE-Nachricht wird an ein Fenster gesendet, wenn ein Waveform-Audio-Eingabegerät geschlossen wird. Das Gerätehandle ist nach dem Senden dieser Nachricht nicht mehr gültig.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506311f9938198e2ceb99646670c954eaa433825855e31c036241df6be1b2491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807110"
---
# <a name="mm_wim_close-message"></a>MM \_ WIM \_ CLOSE-Nachricht

Die **MM \_ WIM \_ CLOSE-Nachricht** wird an ein Fenster gesendet, wenn ein Waveform-Audio-Eingabegerät geschlossen wird. Das Gerätehandle ist nach dem Senden dieser Nachricht nicht mehr gültig.


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Handle für das waveform-audio-Eingabegerät, das geschlossen wurde.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Waveform-Audio](waveform-audio.md)
</dt> <dt>

[Wellenformnachrichten](waveform-messages.md)
</dt> </dl>

 

 





