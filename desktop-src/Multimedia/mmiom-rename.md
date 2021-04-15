---
title: MMIOM_RENAME Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Umbenennungs Meldung wird von der mmiorename-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die angegebene Datei umbenannt wird.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478456"
---
# <a name="mmiom_rename-message"></a>Mmiom- \_ Umbenennungs Meldung

Die **mmiom- \_ Umbenennungs** Meldung wird von der [**mmiorename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die angegebene Datei umbenannt wird.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszoldfilename*
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Dateinamen der umzubenennenden Datei enthält.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpsznewfilename*
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den neuen Dateinamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Datei erfolgreich umbenannt wurde, ist der Rückgabewert 0 (null). Wenn die angegebene Datei nicht gefunden wurde, lautet der Rückgabewert mmioerr \_ fileotfound.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



 

