---
title: MIM_LONGDATA (Mmsystem.h)
description: Die MIM LONGDATA-Nachricht wird an eine EINGABE-Rückruffunktion gesendet, wenn ein system exklusiver Puffer mit Daten gefüllt wurde und an \_ die Anwendung zurückgegeben wird.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- MIM_LONGDATA-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82605835ce8ac231346014215c854abfe9ae7a55fd81e81b8d6214fb8a230327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137211"
---
# <a name="mim_longdata-message"></a>\_MIM LONGDATA-Nachricht

Die **MIM \_ LONGDATA-Nachricht** wird an eine EINGABE-Rückruffunktion gesendet, wenn ein system exklusiver Puffer mit Daten gefüllt wurde und an die Anwendung zurückgegeben wird.


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Zeiger auf eine [**KEYBOARDHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) die den Eingabepuffer identifiziert.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Der Zeitpunkt, zu dem die Daten vom Eingabegerätetreiber empfangen wurden. Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0 (null), als die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) aufgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der zurückgegebene Puffer ist möglicherweise nicht voll. Um die Anzahl der in den zurückgegebenen Puffer aufgezeichneten Bytes zu bestimmen, verwenden Sie den **dwBytesRecorded-Member** der durch *lpMidiHdr* [**angegebenenSKRIPTHDR-Struktur.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

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

 

