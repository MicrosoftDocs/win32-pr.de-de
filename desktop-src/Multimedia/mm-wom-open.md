---
title: MM_WOM_OPEN (Mmsystem.h)
description: Die MM \_ WOM \_ OPEN-Nachricht wird an ein Fenster gesendet, wenn das gegebene Waveform-Audio-Ausgabegerät geöffnet wird.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN von Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e770d03b847352152846d1095bc528bff8e8eacbcdbb1c9fc46450d21dc185bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065400"
---
# <a name="mm_wom_open-message"></a>MM \_ WOM \_ OPEN-Nachricht

Die **MM \_ WOM \_ OPEN-Nachricht** wird an ein Fenster gesendet, wenn das gegebene Waveform-Audio-Ausgabegerät geöffnet wird.


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle für das gerät, das geöffnet wurde.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Waveform-Audio](waveform-audio.md)
</dt> <dt>

[Waveform-Nachrichten](waveform-messages.md)
</dt> </dl>

 

 





