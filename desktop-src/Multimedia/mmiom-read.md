---
title: MMIOM_READ Meldung (Mmsystem.h)
description: Die MMIOM \_ READ-Nachricht wird von der mmioRead-Funktion an eine E/A-Prozedur gesendet, um anzufordern, dass eine angegebene Anzahl von Bytes aus einer geöffneten Datei gelesen werden soll.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ Nachricht Windows Multimedia
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
ms.openlocfilehash: fcf5bbdbb20e2bc168f93857a7d59016197ccc4142d4ba18a2e6fd80842ff06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065350"
---
# <a name="mmiom_read-message"></a>MMIOM \_ READ-Nachricht

Die **MMIOM \_ READ-Nachricht** wird von der [**mmioRead-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) an eine E/A-Prozedur gesendet, um anzufordern, dass eine angegebene Anzahl von Bytes aus einer geöffneten Datei gelesen werden soll.


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*
</dt> <dd>

Zeiger auf den Puffer, der mit aus der Datei gelesenen Daten gefüllt werden soll.

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*
</dt> <dd>

Anzahl der Bytes, die aus der Datei gelesen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Bytes zurück, die tatsächlich aus der Datei gelesen werden. Wenn keine weiteren Bytes gelesen werden können, ist der Rückgabewert 0. Wenn ein Fehler auftritt, ist der Rückgabewert 1.

## <a name="remarks"></a>Hinweise

Die E/A-Prozedur ist für die Aktualisierung des **lDiskOffset-Members** der [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) verantwortlich, um die neue Dateiposition nach dem Lesevorgang widerzuspiegeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



 

