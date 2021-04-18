---
title: MM_MIM_LONGERROR Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm MIM \_ longerror wird an ein Fenster gesendet, wenn eine ungültige oder unvollständige, vom System exklusive System exklusive Nachricht empfangen wird.
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- MM_MIM_LONGERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344700"
---
# <a name="mm_mim_longerror-message"></a>MM \_ MIM \_ longerror-Nachricht

Die Meldung **mm \_ MIM \_ longerror** wird an ein Fenster gesendet, wenn eine ungültige oder unvollständige, vom System exklusive System exklusive Nachricht empfangen wird.


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*
</dt> <dd>

Handle für das MIDI-Eingabegerät, das die ungültige Nachricht empfangen hat.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*
</dt> <dd>

Ein Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Puffer identifiziert, der die ungültige Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Puffer ist möglicherweise nicht voll. Um die Anzahl der Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden, verwenden Sie den **dwbyteslock** -Member der von *lpmidihdr* angegebenen [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur.

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

 

