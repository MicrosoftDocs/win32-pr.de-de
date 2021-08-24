---
title: MM_MIM_DATA Meldung (Mmsystem.h)
description: Die MM \_ MIM \_ DATA-Nachricht wird an ein Fenster gesendet, wenn eine vollständige CSV-Nachricht von einem INPUT-Gerät empfangen wird.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA nachricht Windows Multimedia
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
ms.openlocfilehash: 4309149c8b69fd4396de3a4e67ab18c49008dd7051ed52d4fe992867d1262fe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807380"
---
# <a name="mm_mim_data-message"></a>MM \_ MIM \_ DATA-Nachricht

Die **MM \_ MIM \_ DATA-Nachricht** wird an ein Fenster gesendet, wenn eine vollständige CSV-Nachricht von einem INPUT-Gerät empfangen wird.


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle für das INPUT-Gerät, das die FEHLERMELDUNG empfangen hat.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

MELDUNG, die empfangen wurde. Die Nachricht wird wie folgt in einen Doubleword-Wert gepackt:



| Anforderung | Wert | Beschreibung |
|-----------|-----------------|-----------------------------------------------------|
| Oberes Wort | High-Order Byte | Wird nicht verwendet.                                           |
|           | Byte mit niedriger Reihenfolge  | Enthält bei Bedarf ein zweites Byte mit DEN DATEN.  |
| Niedriges Wort  | High-Order Byte | Enthält das erste Byte derDATENÜBERTRAGUNG-Daten (falls erforderlich). |
|           | Byte mit niedriger Reihenfolge  | Enthält den STATUS VON.                           |



 

Die beiden BYTES für DIE DATEN SIND optional, je nach STATUS-Byte DESINEs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

DER STATUS von MELDUNGEN, die von einem PORTS empfangen werden, ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte ZU enthalten.

Diese Nachricht wird nicht gesendet, wenn eine vom SYSTEM exklusive MELDUNG empfangen wird. Für diese Nachricht ist kein Zeitstempel verfügbar. Für Eingabedaten mit Zeitstempel müssen Sie die Nachrichten verwenden, die an Rückruffunktionen gesendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Music Instrument Digital Interface (INSTRUMENTS)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MELDUNGSMELDUNGEN](midi-messages.md)
</dt> </dl>

 

 





