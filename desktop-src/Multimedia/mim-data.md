---
title: MIM_DATA Meldung (MMSYSTEM. h)
description: Die MIM- \_ Daten Nachricht wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859309"
---
# <a name="mim_data-message"></a>MIM- \_ Daten Nachricht

Die **MIM- \_ Daten** Nachricht wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwmidimessage*
</dt> <dd>

Die empfangene MIDI-Nachricht. Die Nachricht wird wie folgt in einem Double Word-Wert verpackt:



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

Der Zeitpunkt, zu dem die Nachricht vom Eingabegeräte Treiber empfangen wurde. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei Null, als die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

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

 

