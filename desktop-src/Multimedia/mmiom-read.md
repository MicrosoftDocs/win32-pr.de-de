---
title: MMIOM_READ Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Lese Meldung wird von der mmioread-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine angegebene Anzahl von Bytes aus einer geöffneten Datei gelesen werden soll.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479374"
---
# <a name="mmiom_read-message"></a>Mmiom- \_ Lese Meldung

Die **mmiom- \_ Lese** Meldung wird von der [**mmioread**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine angegebene Anzahl von Bytes aus einer geöffneten Datei gelesen werden soll.


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lbuffer*
</dt> <dd>

Zeiger auf den Puffer, der mit aus der Datei gelesenen Daten gefüllt werden soll.

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*CBRot*
</dt> <dd>

Anzahl der aus der Datei gelesenen Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der tatsächlich aus der Datei gelesenen Bytes zurück. Wenn keine weiteren Bytes gelesen werden können, ist der Rückgabewert 0. Wenn ein Fehler auftritt, ist der Rückgabewert 1.

## <a name="remarks"></a>Bemerkungen

Die e/a-Prozedur ist dafür verantwortlich, den **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur zu aktualisieren, um die neue Dateiposition nach dem Lesevorgang widerzuspiegeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



 

