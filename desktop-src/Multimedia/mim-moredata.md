---
title: MIM_MOREDATA Meldung (MMSYSTEM. h)
description: Die MIM \_ MoreData-Nachricht wird an eine Funktion für die Verwendung von MIDI-Eingaben gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird. die MIM-Daten Nachrichten werden von der Anwendung jedoch nicht \_ schnell genug verarbeitet, um mit dem Eingabegeräte Treiber zu arbeiten.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743929"
---
# <a name="mim_moredata-message"></a>MIM \_ MoreData-Nachricht

Die **MIM \_ MoreData** -Nachricht wird an eine Funktion für die Verwendung von MIDI-Eingaben gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird. die [**MIM- \_ Daten**](mim-data.md) Nachrichten werden von der Anwendung jedoch nicht schnell genug verarbeitet, um mit dem Eingabegeräte Treiber zu arbeiten. Die Rückruffunktion empfängt diese Nachricht nur dann, wenn die Anwendung den Status der MIDI-e/a \_ \_ im Aufrufs der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion angibt.


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwmidimessage*
</dt> <dd>

Gibt die empfangene MIDI-Nachricht an. Die Nachricht wird wie folgt in einem **DWORD**-Wert verpackt:



| Anforderung | Wert |
|-----------|-----------------|-----------------------------------------------------|
| Hohes Wort | Byte mit hoher Reihenfolge | Nicht verwendet.                                           |
|           | Byte mit niedriger Reihenfolge  | Enthält ein zweites Byte von MIDI-Daten (bei Bedarf).  |
| Niedriges Wort  | Byte mit hoher Reihenfolge | Enthält das erste Byte der MIDI-Daten (bei Bedarf). |
|           | Byte mit niedriger Reihenfolge  | Enthält den Status von MIDI.                           |



 

Die beiden Byte-Daten Bytes sind optional, abhängig vom Status Byte von MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwtimestamp*
</dt> <dd>

Gibt die Uhrzeit an, zu der die Nachricht vom Eingabegeräte Treiber empfangen wurde. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0, wenn die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte nur eine minimale Menge an Verarbeitung von MIM- \_ MoreData-Nachrichten durchführen. (Insbesondere sollten Anwendungen die [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion bei der Verarbeitung von MIM \_ nicht aufzurufen. MoreData.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.

Wenn eine Anwendung eine [**MIM- \_ Daten**](mim-data.md) Nachricht nach einer Reihe von MIM- \_ Daten Nachrichten empfängt, hat Sie eingehende MIDI-Ereignisse erfasst und kann zeitintensive Funktionen sicher aufzurufen.

Bei den von einem MIDI-eingabeport empfangenen MIDI-Nachrichten ist der Status " jede Nachricht wird so erweitert, dass Sie das MIDI-Status Byte enthält.

Diese Meldung wird nicht gesendet, wenn eine vom System exklusive System exklusive Nachricht empfangen wird.

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

 

