---
title: MIM_DATA (Mmsystem.h)
description: Die MIM DATA-Nachricht wird an eine RÜCKRUF-Eingaberückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem \_ EINGABEGERÄT empfangen wird.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA Meldung Windows Multimedia
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
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118405"
---
# <a name="mim_data-message"></a>MIM \_ DATA-Nachricht

Die **MIM \_ DATA-Nachricht** wird an eine RÜCKRUF-Eingaberückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEGERÄT empfangen wird.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

DIE-Nachricht, die empfangen wurde. Die Nachricht wird wie folgt in einen Doublewordwert gepackt:



| Anforderung | Wert | Beschreibung |
|-----------|-----------------|-----------------------------------------------------|
| Hohes Wort | High-Order-Byte | Wird nicht verwendet.                                           |
|           | Niedriges Byte  | Enthält (bei Bedarf) ein zweites Byte von DANN-Daten.  |
| Niedriges Wort  | High-Order-Byte | Enthält (falls erforderlich) das erste Byte derTEN-Daten. |
|           | Niedriges Byte  | Enthält den STATUS DEST-Status.                           |



 

Die beiden BYTES der BYTES-DATEN sind je nach STATUS-Byte optional.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Uhrzeit, zu der die Nachricht vom Eingabegerätetreiber empfangen wurde. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0 (null), als die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Ausführungsstatus von über einen EINGABE-Eingabeport empfangenen SMS-Nachrichten ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte zu enthalten.

Diese Nachricht wird nicht gesendet, wenn eine exklusive SYSTEM-EXCLUSIVE-Nachricht empfangen wird.

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

 

