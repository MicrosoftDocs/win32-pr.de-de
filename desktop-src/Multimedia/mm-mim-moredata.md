---
title: MM_MIM_MOREDATA Meldung (Mmsystem.h)
description: Die MM \_ MIM \_ MOREDATA-Nachricht wird an ein Rückruffenster gesendet, wenn eine RÜCKRUFNACHRICHT von einem EINGABEGERÄT empfangen wird, die Anwendung jedoch MIM \_ DATA-Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber Schritt zu halten.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA Meldung Windows Multimedia
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
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120025"
---
# <a name="mm_mim_moredata-message"></a>MM \_ MIM \_ MOREDATA-Nachricht

Die **MM \_ MIM \_ MOREDATA-Nachricht** wird an ein Rückruffenster gesendet, wenn eine RÜCKRUFNACHRICHT von einem INPUT-Eingabegerät empfangen wird, die Anwendung jedoch [**MIM \_ DATA-Nachrichten**](mim-data.md) nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber Schritt zu halten. Das Fenster empfängt diese Meldung nur, wenn die Anwendung IM \_ \_ Aufruf der funktion [**"arsInOpen"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) den STATUS DER IO-E/A-Funktion VON DER ANWENDUNG angibt.


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle für das EINGABEGERÄT, das die FEHLERMELDUNG erhalten hat.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Gibt die empfangene FEHLERMELDUNG AN. Die Nachricht wird wie folgt in einen Doubleword-Wert gepackt:



| Anforderung | Wert | Beschreibung |
|-----------|-----------------|-----------------------------------------------------|
| Hohes Wort | Hohe Bytereihenfolge | Wird nicht verwendet.                                           |
|           | Byte mit niedriger Reihenfolge  | Enthält bei Bedarf ein zweites Byte mit QUOTA-Daten.  |
| Niedriges Wort  | Hohe Bytereihenfolge | Enthält das erste Byte derDATENÜBERTRAGUNG-Daten (falls erforderlich). |
|           | Byte mit niedriger Reihenfolge  | Enthält den STATUS VON.                           |



 

Die beiden BYTES für DIE DATEN SIND optional, je nach STATUS-Byte DESINEs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Ihre Anwendung SCHNELLER ALS DIE DATEN verarbeiten kann, sollten Sie keinen Fensterrückrufmechanismus verwenden. Um die Geschwindigkeit zu maximieren, verwenden Sie eine Rückruffunktion und die [**MIM \_ MOREDATA-Nachricht**](mim-moredata.md) anstelle von MM \_ MIM \_ MOREDATA.

Eine Anwendung sollte nur eine minimale Verarbeitungsmenge von MM \_ MIM \_ MOREDATA-Nachrichten durchführen. (Insbesondere sollten Anwendungen die [PostMessage-Funktion](/windows/win32/api/winuser/nf-winuser-postmessagea) während der Verarbeitung von MM \_ nicht aufrufen. MIM \_ MOREDATA.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.

Wenn eine Anwendung nach einer Reihe von MM MIM MOREDATA-Nachrichten eine [**MM \_ MIM \_ DATA-Nachricht**](mm-mim-data.md) empfängt, \_ hat sie eingehende \_ CAB-Ereignisse aufholt und kann zeitintensive Funktionen sicher aufrufen.

DER STATUS von MELDUNGEN, die von einem PORTS empfangen werden, ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte ZU enthalten.

Diese Nachricht wird nicht gesendet, wenn eine vom SYSTEM exklusive MELDUNG empfangen wird. Für diese Nachricht ist kein Zeitstempel verfügbar. Für Eingabedaten mit Zeitstempel müssen Sie die Nachrichten verwenden, die an Rückruffunktionen gesendet werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Music Instrument Digital Interface (INSTRUMENTS)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[FEHLERMELDUNGEN](midi-messages.md)
</dt> </dl>

 

