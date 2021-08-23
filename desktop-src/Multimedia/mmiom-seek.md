---
title: MMIOM_SEEK (Mmsystem.h)
description: Die MMIOM SEEK-Nachricht wird von der mmioSeek-Funktion an eine E/A-Prozedur gesendet, um an fordern, dass die aktuelle \_ Dateiposition verschoben wird.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea33db15de3a4617561c437f2d5086afbf4bff2155e657677b171b1413b1c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065300"
---
# <a name="mmiom_seek-message"></a>MMIOM \_ SEEK-Nachricht

Die **MMIOM \_ SEEK-Nachricht** wird von der [**mmioSeek-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) an eine E/A-Prozedur gesendet, um an fordern, dass die aktuelle Dateiposition verschoben wird.


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*
</dt> <dd>

Neue Dateiposition. Die Bedeutung dieses Werts hängt von dem in **lChangeFlag angegebenen Flag ab.**

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*
</dt> <dd>

Flag, das an gibt, wie die Dateiposition geändert wird. Die folgenden Werte sind definiert:



| Anforderung | Wert |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| SEEK \_ CUR | Verschieben Sie die Dateiposition von der aktuellen Position in *lNewFilePos* Bytes. *lNewFilePos kann* positiv oder negativ sein. |
| SEEK \_ END | Verschieben Sie die Dateiposition in *lNewFilePos* bytes vom Ende der Datei.                                             |
| SEEK \_ SET | Verschieben Sie die Dateiposition vom Anfang der Datei in *lNewFilePos* Bytes.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die neue Dateiposition zurück. Wenn ein Fehler auftritt, ist der Rückgabewert 1.

## <a name="remarks"></a>Hinweise

Die E/A-Prozedur ist für die Beibehaltung der aktuellen Dateiposition im **lDiskOffset-Element** der [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) verantwortlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



 

