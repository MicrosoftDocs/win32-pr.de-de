---
title: MM_MIM_ERROR Meldung (MMSYSTEM. h)
description: Die mm \_ MIM- \_ Fehlermeldung wird an ein Fenster gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- MM_MIM_ERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103034"
---
# <a name="mm_mim_error-message"></a>MM \_ MIM- \_ Fehlermeldung

Die **mm \_ MIM- \_ Fehler** Meldung wird an ein Fenster gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*
</dt> <dd>

Handle für das MIDI-Eingabegerät, das die ungültige Nachricht empfangen hat.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lmidimessage*
</dt> <dd>

Ungültige MIDI-Nachricht. Die Nachricht wird in einem **DWORD** -Wert mit dem ersten Byte der Nachricht im nieder wertigen Byte verpackt.

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

[Digital Instrumentation Digital Interface (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MIDI-Nachrichten](midi-messages.md)
</dt> </dl>

 

 





