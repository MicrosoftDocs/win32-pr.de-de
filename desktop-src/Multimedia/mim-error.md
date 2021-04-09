---
title: MIM_ERROR Meldung (MMSYSTEM. h)
description: Die MIM- \_ Fehlermeldung wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- MIM_ERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103043"
---
# <a name="mim_error-message"></a>MIM- \_ Fehlermeldung

Die **MIM- \_ Fehler** Meldung wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwmidimessage*
</dt> <dd>

Es wurde eine ungültige MIDI-Nachricht empfangen. Die Nachricht wird in einem Double Word-Wert mit dem ersten Byte der Nachricht im nieder wertigen Byte verpackt.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwtimestamp*
</dt> <dd>

Der Zeitpunkt, zu dem die Nachricht vom Eingabegeräte Treiber empfangen wurde. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei Null, als die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion aufgerufen wurde.

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

 

