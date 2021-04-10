---
title: MM_MIM_MOREDATA Meldung (MMSYSTEM. h)
description: Die mm \_ MIM \_ MoreData-Nachricht wird an ein Rückruf Fenster gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird, die Anwendung jedoch MIM- \_ Daten Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabe-Gerätetreiber Schritt zu halten.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040581"
---
# <a name="mm_mim_moredata-message"></a>MM \_ MIM \_ MoreData-Nachricht

Die **mm \_ MIM \_ MoreData** -Nachricht wird an ein Rückruf Fenster gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird, die Anwendung jedoch [**MIM- \_ Daten**](mim-data.md) Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabe-Gerätetreiber Schritt zu halten. Das Fenster empfängt diese Meldung nur dann, wenn die Anwendung den Status der MIDI-e/a im-Befehl \_ \_ für die [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion angibt.


```C++
MM_MIM_MOREDATA 
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

Gibt die empfangene MIDI-Nachricht an. Die Nachricht wird wie folgt in einem Double Word-Wert verpackt:



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

Wenn Ihre Anwendung die Daten von MIDI schneller empfängt, als Sie verarbeiten kann, sollten Sie keinen Fenster Rückrufmechanismus verwenden. Verwenden Sie zum Maximieren der Geschwindigkeit eine Rückruffunktion, und verwenden Sie die [**MIM \_ MoreData**](mim-moredata.md) -Nachricht anstelle von mm \_ MIM \_ MoreData.

Eine Anwendung sollte nur eine minimale Menge an Verarbeitung von mm \_ MIM- \_ Daten Nachrichten verarbeiten. (Insbesondere sollten Anwendungen die [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion bei der Verarbeitung von mm \_ nicht aufzurufen. MIM \_ MoreData.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.

Wenn eine Anwendung eine [**mm \_ MIM- \_ Daten**](mm-mim-data.md) Nachricht nach einer Reihe von mm \_ MIM- \_ Daten Nachrichten empfängt, hat Sie eingehende MIDI-Ereignisse erfasst und kann zeitintensive Funktionen sicher aufzurufen.

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

 

