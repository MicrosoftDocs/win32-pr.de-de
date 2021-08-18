---
title: MM_MIM_LONGDATA (Mmsystem.h)
description: Die MM \_ MIM LONGDATA-Nachricht wird an ein Fenster gesendet, wenn entweder eine vollständige SYSTEM-exklusive NACHRICHT empfangen wird oder wenn ein Puffer mit system-exklusiven Daten \_ gefüllt wurde.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4748381500f42a5dc4f2bceae8ad862a64f237c9d5024e4b0b7cc96a694e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065520"
---
# <a name="mm_mim_longdata-message"></a>MM \_ MIM \_ LONGDATA-Nachricht

Die **MM \_ MIM \_ LONGDATA-Nachricht** wird an ein Fenster gesendet, wenn entweder eine vollständige, vom SYSTEM exklusive MELDUNG empfangen wird oder wenn ein Puffer mit system exklusiven Daten gefüllt wurde.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle für das EINGABE-Eingabegerät, das die Daten empfangen hat.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Zeiger auf eine [**DABEIHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) die den Puffer identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der zurückgegebene Puffer ist möglicherweise nicht voll. Um die Anzahl der in den zurückgegebenen Puffer aufgezeichneten Bytes zu bestimmen, verwenden Sie den **dwBytesRecorded-Member** [**derSKRIPTHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) auf die *lpMidiHdr zeigt.*

Für diese Nachricht ist kein Zeitstempel verfügbar. Für Eingabedaten mit Zeitstempel müssen Sie die Nachrichten verwenden, die an Rückruffunktionen gesendet werden.

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

 

