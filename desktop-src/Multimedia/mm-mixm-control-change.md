---
title: MM_MIXM_CONTROL_CHANGE (Mmsystem.h)
description: Die MELDUNG MM MIXM CONTROL CHANGE wird von einem Mixergerät gesendet, um eine Anwendung darüber zu informieren, dass sich der Zustand eines Steuerelements geändert hat, das einer \_ \_ \_ Audiozeile zugeordnet ist. Die Anwendung sollte ihre Anzeige- und zwischengespeicherten Werte für das angegebene Steuerelement aktualisieren.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44305a5a441e4d12a1b3f43029ae3a41f7642c13b15a50f74a1acab158c2ed58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807180"
---
# <a name="mm_mixm_control_change-message"></a>MELDUNG \_ "MM MIXM \_ CONTROL \_ CHANGE"

Die **MELDUNG \_ MM MIXM CONTROL \_ \_ CHANGE** wird von einem Mixergerät gesendet, um eine Anwendung darüber zu informieren, dass sich der Zustand eines Steuerelements geändert hat, das einer Audiozeile zugeordnet ist. Die Anwendung sollte ihre Anzeige- und zwischengespeicherten Werte für das angegebene Steuerelement aktualisieren.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Handle für das Mixergerät (**HMIXER**), das die Benachrichtigungsnachricht gesendet hat.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*
</dt> <dd>

Steuerelementbezeichner für das Mixer-Steuerelement, das den Zustand geändert hat. Dieser Bezeichner ist identisch mit dem **dwControlID-Member** der **MIXERCONTROL-Struktur,** die von der **mixerGetLineControls-Funktion zurückgegeben** wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Anwendung muss ein Mixergerät öffnen und ein Rückruffenster angeben, um die **MM \_ MIXM \_ CONTROL \_ CHANGE-Nachricht zu** empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Audiomixer](audio-mixers.md)
</dt> <dt>

[Audio Mixer Messages](audio-mixer-messages.md)
</dt> </dl>

 

 





