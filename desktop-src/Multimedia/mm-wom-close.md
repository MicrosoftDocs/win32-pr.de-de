---
title: MM_WOM_CLOSE (Mmsystem.h)
description: Die MM \_ WOM \_ CLOSE-Nachricht wird an ein Fenster gesendet, wenn ein Waveform-Audio-Ausgabegerät geschlossen wird. Das Gerätehandy ist nach dem Senden dieser Nachricht nicht mehr gültig.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- MM_WOM_CLOSE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7624c85554fca997ce9542170e370711f8b3c3cefc22cf0e8d2fe9ea3e88687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065450"
---
# <a name="mm_wom_close-message"></a>MM \_ WOM \_ CLOSE-Meldung

Die **MM \_ WOM \_ CLOSE-Nachricht** wird an ein Fenster gesendet, wenn ein Waveform-Audio-Ausgabegerät geschlossen wird. Das Gerätehandy ist nach dem Senden dieser Nachricht nicht mehr gültig.


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle für das gerät, das geschlossen wurde.

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

 

 





