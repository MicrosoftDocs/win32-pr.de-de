---
title: MIM_MOREDATA (Mmsystem.h)
description: Die MIM MOREDATA-Nachricht wird an eine EINGABE-Rückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEEINGABE-Gerät empfangen wird, die Anwendung jedoch MIM DATA-Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu \_ \_ können.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA von Windows Multimedia
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
ms.openlocfilehash: 130a07d1d205e9944c7be6ab9ad1294e09d0ebdcdb81d5befc5468ff5a65218f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782970"
---
# <a name="mim_moredata-message"></a>\_MIM MOREDATA-Meldung

Die **MIM \_ MOREDATA-Nachricht** wird an eine EINGABE-Rückruffunktion gesendet, wenn eine EINGABE-Nachricht von einem EINGABEEINGABE-Gerät empfangen wird, die Anwendung jedoch MIM [**\_ DATA-Nachrichten**](mim-data.md) nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu können. Die Rückruffunktion empfängt diese Nachricht nur, wenn die Anwendung im Aufruf der \_ funktion "sollInOpen" den STATUS DESEID-E/A-Werts \_ [**angibt.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)


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
| Hohes Wort | High-Order Byte | Wird nicht verwendet.                                           |
|           | Niedriges Byte  | Enthält (bei Bedarf) ein zweites Byte von DANN-Daten.  |
| Niedriges Wort  | High-Order Byte | Enthält (falls erforderlich) das erste Byte derTEN-Daten. |
|           | Niedriges Byte  | Enthält den STATUS DEST-Status.                           |



 

Die beiden BYTES der BYTES für DIE BYTES sind je nach STATUS-Byte optional.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Gibt den Zeitpunkt an, zu dem die Nachricht vom Eingabegerätetreiber empfangen wurde. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0, als die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte nur einen minimalen Verarbeitungsaufwand für MIM \_ MOREDATA-Nachrichten verarbeiten. (Insbesondere sollten Anwendungen die [PostMessage-Funktion](/windows/win32/api/winuser/nf-winuser-postmessagea) nicht aufrufen, während sie MIM \_ MOREDATA.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.

Wenn eine Anwendung eine [**MIM \_ DATA-Nachricht**](mim-data.md) nach einer Reihe von MIM MOREDATA-Nachrichten empfängt, hat sie die \_ eingehenden NOTE-Ereignisse erfasst und kann zeitintensive Funktionen sicher aufrufen.

Der Ausführungsstatus von über einen EINGABE-Eingabeport empfangenen SMS-Nachrichten ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte zu enthalten.

Diese Nachricht wird nicht gesendet, wenn eine exklusive SYSTEM-EXCLUSIVE-Nachricht empfangen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Instrument Digital Interface (KEYBOARD)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MESSAGES-Meldungen](midi-messages.md)
</dt> </dl>

 

