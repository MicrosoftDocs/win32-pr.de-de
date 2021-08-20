---
title: MMIOM_RENAME (Mmsystem.h)
description: Die MMIOM RENAME-Nachricht wird von der mmioRename-Funktion an eine E/A-Prozedur gesendet, um die Umbenennung \_ der angegebenen Datei an fordern.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME-Nachricht Windows Multimedia
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
ms.openlocfilehash: bcfd90b53f1cc42030bd00e6553d52de0f036ff274b3d4ff942c48667e4347b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065310"
---
# <a name="mmiom_rename-message"></a>MMIOM \_ RENAME-Meldung

Die **MMIOM \_ RENAME-Nachricht** wird von der [**mmioRename-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) an eine E/A-Prozedur gesendet, um die Umbenennung der angegebenen Datei an fordern.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Dateinamen der umzubenennenden Datei enthält.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den neuen Dateinamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Datei erfolgreich umbenannt wurde, ist der Rückgabewert 0 (null). Wenn die angegebene Datei nicht gefunden wurde, ist der Rückgabewert MMIOERR \_ FILENOTFOUND.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



 

