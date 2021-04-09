---
title: MMIOM_WRITE Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Schreib Nachricht wird von der mmiowrite-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957085"
---
# <a name="mmiom_write-message"></a>Mmiom- \_ Schreib Nachricht

Die **mmiom- \_ Schreib** Nachricht wird von der [**mmiowrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden.


```C++
MMIOM_WRITE 
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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



 

