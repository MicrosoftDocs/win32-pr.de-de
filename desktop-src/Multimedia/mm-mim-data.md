---
title: MM_MIM_DATA Meldung (MMSYSTEM. h)
description: Die mm \_ MIM- \_ Daten Nachricht wird an ein Fenster gesendet, wenn von einem MIDI-Eingabegerät eine komplette MIDI-Nachricht empfangen wird.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA-Nachricht (Multimedia)
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
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040213"
---
# <a name="mm_mim_data-message"></a>MM \_ MIM- \_ Daten Nachricht

Die **mm \_ MIM- \_ Daten** Nachricht wird an ein Fenster gesendet, wenn von einem MIDI-Eingabegerät eine komplette MIDI-Nachricht empfangen wird.


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*
</dt> <dd>

Handle für das MIDI-Eingabegerät, das die MIDI-Nachricht empfangen hat.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lmidimessage*
</dt> <dd>

Die empfangene MIDI-Nachricht. Die Nachricht wird wie folgt in einem Double Word-Wert verpackt:



| Anforderung | Wert |
|-----------|-----------------|-----------------------------------------------------|
| Hohes Wort | Byte mit hoher Reihenfolge | Nicht verwendet.                                           |
|           | Byte mit niedriger Reihenfolge  | Enthält ein zweites Byte von MIDI-Daten (bei Bedarf).  |
| Niedriges Wort  | Byte mit hoher Reihenfolge | Enthält das erste Byte der MIDI-Daten (bei Bedarf). |
|           | Byte mit niedriger Reihenfolge  | Enthält den Status von MIDI.                           |



 

Die beiden Byte-Daten Bytes sind optional, abhängig vom Status Byte von MIDI.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bei den von einem MIDI-eingabeport empfangenen MIDI-Nachrichten ist der Status " jede Nachricht wird so erweitert, dass Sie das MIDI-Status Byte enthält.

Diese Meldung wird nicht gesendet, wenn eine vom System exklusive System exklusive Nachricht empfangen wird. Mit dieser Meldung ist kein Zeitstempel verfügbar. Für Zeitstempel-Eingabedaten müssen Sie die Nachrichten verwenden, die an Rückruf Funktionen gesendet werden.

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

 

 





