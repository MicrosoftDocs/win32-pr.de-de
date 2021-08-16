---
title: MM_MIXM_LINE_CHANGE Nachricht (Mmsystem.h)
description: Die \_ MM MIXM \_ LINE \_ CHANGE-Nachricht wird von einem Mixergerät gesendet, um eine Anwendung darüber zu informieren, dass sich der Zustand einer Audiozeile auf dem angegebenen Gerät geändert hat. Die Anwendung sollte ihre Anzeige- und zwischengespeicherten Werte für die angegebene Audiozeile aktualisieren.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3bd1c122d5e0cf62aa39266da547cd3701e43e6afbf01b853c7d24040504d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373579"
---
# <a name="mm_mixm_line_change-message"></a>MM \_ MIXM \_ LINE \_ CHANGE-Meldung

Die **MM \_ MIXM LINE \_ \_ CHANGE-Nachricht** wird von einem Mixergerät gesendet, um eine Anwendung darüber zu informieren, dass sich der Zustand einer Audiozeile auf dem angegebenen Gerät geändert hat. Die Anwendung sollte ihre Anzeige- und zwischengespeicherten Werte für die angegebene Audiozeile aktualisieren.


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Handle für das Mixergerät, das die Benachrichtigungsmeldung gesendet hat.

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*
</dt> <dd>

Zeilenbezeichner für die Audiozeile, deren Status geändert wurde. Dieser Bezeichner entspricht dem **dwLineID-Member** der **MIXERLINE-Struktur,** die von der **mixerGetLineInfo-Funktion** zurückgegeben wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Anwendung muss ein Mixergerät öffnen und ein Rückruffenster angeben, um die **MM \_ MIXM \_ LINE \_ CHANGE-Meldung** zu empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Audiomixer](audio-mixers.md)
</dt> <dt>

[Audio Mixer Nachrichten](audio-mixer-messages.md)
</dt> </dl>

 

 





