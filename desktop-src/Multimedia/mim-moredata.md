---
title: MIM_MOREDATA (Mmsystem.h)
description: Die MIM MOREDATA-Nachricht wird an eine EINGABE-Rückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEEINGABE-Gerät empfangen wird, die Anwendung mim-DATENnachrichten jedoch nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu \_ \_ können.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA Meldung Windows Multimedia
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
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119405"
---
# <a name="mim_moredata-message"></a>MIM \_ MOREDATA-Nachricht

Die **MIM \_ MOREDATA-Nachricht** wird an eine EINGABE-Rückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEEINGABE-Gerät empfangen wird, die Anwendung [**mim-DATENnachrichten \_**](mim-data.md) jedoch nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu können. Die Rückruffunktion empfängt diese Nachricht nur, wenn die Anwendung im Aufruf der \_ \_ funktion [**"eigenschaftInOpen"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) den STATUS DESEJO angibt.


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Gibt die empfangene MESSAGE-Nachricht an. Die Nachricht wird wie folgt in **einen DWORD-Wert** gepackt:



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

Gibt den Zeitpunkt an, zu dem die Nachricht vom Eingabegerätetreiber empfangen wurde. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0, als die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte nur einen minimalen Verarbeitungsaufwand für MIM \_ MOREDATA-Nachrichten verarbeiten. (Insbesondere sollten Anwendungen die [PostMessage-Funktion](/windows/win32/api/winuser/nf-winuser-postmessagea) bei der Verarbeitung von MIM nicht aufrufen. \_ MOREDATA.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.

Wenn eine Anwendung nach einer Reihe von MIM MOREDATA-Nachrichten eine [**MIM \_ DATA-Nachricht**](mim-data.md) empfängt, ist sie mit eingehenden ANMELDUNG-Ereignissen auf dem Auffangen und kann zeitintensive \_ Funktionen sicher aufrufen.

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

 

