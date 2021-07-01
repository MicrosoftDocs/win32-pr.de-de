---
title: MM_MIM_DATA (Mmsystem.h)
description: Die MM MIM DATA-Nachricht wird an ein Fenster gesendet, wenn eine vollständige DANN-Nachricht von einem \_ \_ EINGABEGERÄT empfangen wird.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA Meldung Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119695"
---
# <a name="mm_mim_data-message"></a>MM \_ MIM \_ DATA-Nachricht

Die **MM \_ MIM \_ DATA-Nachricht** wird an ein Fenster gesendet, wenn eine vollständige DANN-Nachricht von einem EINGABEGERÄT empfangen wird.


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle für das EINGABE-Eingabegerät, das die FEHLERMELDUNG-Nachricht empfangen hat.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

DIE-Nachricht, die empfangen wurde. Die Nachricht wird wie folgt in einen Doublewordwert gepackt:



| Anforderung | Wert | Beschreibung |
|-----------|-----------------|-----------------------------------------------------|
| Hohes Wort | High-Order-Byte | Wird nicht verwendet.                                           |
|           | Niedriges Byte  | Enthält (bei Bedarf) ein zweites Byte von DANN-Daten.  |
| Niedriges Wort  | High-Order-Byte | Enthält (falls erforderlich) das erste Byte derTEN-Daten. |
|           | Niedriges Byte  | Enthält den STATUS DEST-Status.                           |



 

Die beiden BYTES der BYTES-DATEN sind je nach STATUS-Byte optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Ausführungsstatus von über einen EINGABE-Eingabeport empfangenen SMS-Nachrichten ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte zu enthalten.

Diese Nachricht wird nicht gesendet, wenn eine exklusive SYSTEM-EXCLUSIVE-Nachricht empfangen wird. Für diese Nachricht ist kein Zeitstempel verfügbar. Für Eingabedaten mit Zeitstempel müssen Sie die Nachrichten verwenden, die an Rückruffunktionen gesendet werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (einschließlich Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Instrument Digital Interface (KEYBOARD)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MESSAGES-Meldungen](midi-messages.md)
</dt> </dl>

 

 





