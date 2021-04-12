---
title: MM_MIM_LONGDATA Meldung (MMSYSTEM. h)
description: Die mm \_ MIM \_ longdata-Nachricht wird an ein Fenster gesendet, wenn entweder eine vollständige, vom System exklusive System exklusive Nachricht empfangen wird oder wenn ein Puffer mit System exklusiven Daten aufgefüllt wurde.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA-Nachricht (Multimedia)
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
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105903"
---
# <a name="mm_mim_longdata-message"></a>MM \_ MIM \_ longdata-Nachricht

Die **mm \_ MIM \_ longdata** -Nachricht wird an ein Fenster gesendet, wenn entweder eine vollständige, vom System exklusive System exklusive Nachricht empfangen wird oder wenn ein Puffer mit System exklusiven Daten aufgefüllt wurde.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*
</dt> <dd>

Handle für das MIDI-Eingabegerät, das die Daten empfangen hat.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*
</dt> <dd>

Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Puffer identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Puffer ist möglicherweise nicht voll. Um die Anzahl von Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden, verwenden Sie den **dwbyteslock** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, auf die von *lpmidihdr* verwiesen wird.

Mit dieser Meldung ist kein Zeitstempel verfügbar. Für Zeitstempel-Eingabedaten müssen Sie die Nachrichten verwenden, die an Rückruf Funktionen gesendet werden.

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

 

