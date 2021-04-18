---
title: MMIOM_CLOSE Meldung (MMSYSTEM. h)
description: Die mmiom \_ Close-Nachricht wird von der mmioclose-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geschlossen wird.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519295"
---
# <a name="mmiom_close-message"></a>Mmiom- \_ Meldung schließen

Die **mmiom \_ Close** -Nachricht wird von der [**mmioclose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geschlossen wird.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lcloseflags*
</dt> <dd>

Flags, die im **wFlags**-Parameter von **mmioclose** enthalten sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn die Datei erfolgreich geschlossen wurde, andernfalls einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



 

