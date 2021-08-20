---
title: MIM_DATA (Mmsystem.h)
description: Die MIM DATA-Nachricht wird an eine EINGABE-Rückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem \_ EINGABEGERÄT empfangen wird.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA von Windows Multimedia
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
ms.openlocfilehash: bebbb9ca6016706605de8fed29e5fa5ebaf6055f4a730fb563323f306606b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137289"
---
# <a name="mim_data-message"></a>\_MIM DATA-Nachricht

Die **MIM \_ DATA-Nachricht** wird an eine EINGABE-Rückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEGERÄT empfangen wird.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

DIE-Nachricht, die empfangen wurde. Die Nachricht wird wie folgt in einen Doubleword-Wert gepackt:



| Anforderung | Wert | Beschreibung |
|-----------|-----------------|-----------------------------------------------------|
| Hohes Wort | High-Order Byte | Wird nicht verwendet.                                           |
|           | Niedriges Byte  | Enthält (bei Bedarf) ein zweites Byte von DANN-Daten.  |
| Niedriges Wort  | High-Order Byte | Enthält (falls erforderlich) das erste Byte derTEN-Daten. |
|           | Niedriges Byte  | Enthält den STATUS DEST-Status.                           |



 

Die beiden BYTES der BYTES für DIE BYTES sind je nach STATUS-Byte optional.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Uhrzeit, zu der die Nachricht vom Eingabegerätetreiber empfangen wurde. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0 (null), als die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Ausführungsstatus von über einen EINGABE-Eingabeport empfangenen SMS-Nachrichten ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte zu enthalten.

Diese Nachricht wird nicht gesendet, wenn eine exklusive SYSTEM-EXCLUSIVE-Nachricht empfangen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Instrument Digital Interface (KEYBOARD)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MESSAGES-Meldungen](midi-messages.md)
</dt> </dl>

 

