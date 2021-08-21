---
title: MMIOM_WRITE (Mmsystem.h)
description: Die MMIOM WRITE-Nachricht wird von der mmioWrite-Funktion an eine E/A-Prozedur gesendet, um an fordern, dass Daten \_ in eine geöffnete Datei geschrieben werden.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE-Nachricht Windows Multimedia
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
ms.openlocfilehash: 755b89d7e268e266b4761142dc3820bdd4d33d4bd4d86522ce5363b95e5be282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065270"
---
# <a name="mmiom_write-message"></a>MMIOM \_ WRITE-Nachricht

Die **MMIOM \_ WRITE-Nachricht** wird von der [**mmioWrite-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) an eine E/A-Prozedur gesendet, um an fordern, dass Daten in eine geöffnete Datei geschrieben werden.


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

Zeiger auf einen Puffer, der die in die Datei zu schreibenden Daten enthält.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Anzahl der Bytes, die in die Datei geschrieben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Bytes zurück, die tatsächlich in die Datei geschrieben wurden. Wenn ein Fehler auftritt, ist der Rückgabewert 1.

## <a name="remarks"></a>Hinweise

Die E/A-Prozedur ist dafür verantwortlich, das **lDiskOffset-Element** der [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) zu aktualisieren, um die neue Dateiposition nach dem Schreibvorgang widerzu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



 

