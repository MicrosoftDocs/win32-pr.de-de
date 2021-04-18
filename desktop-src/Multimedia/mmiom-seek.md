---
title: MMIOM_SEEK Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Suchmeldung wird von der mmioseek-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die aktuelle Dateiposition verschoben werden soll.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK-Nachricht (Multimedia)
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
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345513"
---
# <a name="mmiom_seek-message"></a>Mmiom- \_ Suchmeldung

Die **mmiom- \_ Such** Meldung wird von der [**mmioseek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass die aktuelle Dateiposition verschoben werden soll.


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lnewfilepos*
</dt> <dd>

Neue Dateiposition. Die Bedeutung dieses Werts hängt von dem in **lchangeflag** angegebenen Flag ab.

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lchangeflag*
</dt> <dd>

Flag, das angibt, wie die Dateiposition geändert wird. Die folgenden Werte sind definiert:



| Anforderung | Wert |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| \_cur suchen | Verschieben Sie die Dateiposition an der aktuellen Position in *lnewfilepos* bytes. *lnewfilepos* können positiv oder negativ sein. |
| \_Ende suchen | Verschieben Sie die Dateiposition als *lnewfilepos* Bytes vom Dateiende.                                             |
| \_Suchsatz | Verschieben Sie die Dateiposition vom Anfang der Datei in *lnewfilepos* bytes.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die neue Dateiposition zurück. Wenn ein Fehler auftritt, ist der Rückgabewert 1.

## <a name="remarks"></a>Bemerkungen

Die e/a-Prozedur ist dafür verantwortlich, die aktuelle Dateiposition im **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur beizubehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



 

