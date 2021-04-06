---
title: MMIOM_WRITEFLUSH Meldung (MMSYSTEM. h)
description: Die mmiom \_ -Nachricht zum Schreiben von Schreibvorgängen wird von der mmiowrite-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden und dass alle von der e/a-Prozedur verwendeten internen Puffer auf den Datenträger geleert werden.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743360"
---
# <a name="mmiom_writeflush-message"></a>Mmiom-Meldung zum Schreiben von \_ Schreibvorgang

Die **mmiom \_** -Nachricht zum Schreiben von Schreibvorgängen wird von der [**mmiowrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden und dass alle von der e/a-Prozedur verwendeten internen Puffer auf den Datenträger geleert werden.


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

Zeiger auf einen Puffer, der die Daten enthält, die in die Datei geschrieben werden sollen.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbwrite*
</dt> <dd>

Anzahl von Bytes, die in die Datei geschrieben werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Bytes zurück, die tatsächlich in die Datei geschrieben wurden. Wenn ein Fehler auftritt, ist der Rückgabewert 1.

## <a name="remarks"></a>Bemerkungen

Die e/a-Prozedur ist dafür verantwortlich, den **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur zu aktualisieren, um die neue Dateiposition nach dem Schreibvorgang widerzuspiegeln.

Diese Meldung entspricht der [**mmiom- \_ Schreib**](mmiom-write.md) Nachricht, mit der Ausnahme, dass Sie anfordert, dass die e/a-Prozedur ggf. die internen Puffer leert. Diese Nachricht kann genau wie die **mmiom- \_ Schreib** Nachricht verarbeitet werden, es sei denn, eine e/a-Prozedur führt eine interne Pufferung durch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



 

