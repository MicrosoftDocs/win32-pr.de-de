---
title: MMIOM_WRITEFLUSH Meldung (Mmsystem.h)
description: Die MMIOM \_ WRITEFLUSH-Nachricht wird von der mmioWrite-Funktion an eine E/A-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden und dass alle internen Puffer, die von der E/A-Prozedur verwendet werden, auf den Datenträger geleert werden.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH nachricht Windows Multimedia
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
ms.openlocfilehash: b274536e934f426ef5e545e758c2f7bf918d552c42085650fc7c81a6a47c842e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807090"
---
# <a name="mmiom_writeflush-message"></a>MMIOM \_ WRITEFLUSH-Nachricht

Die **MMIOM \_ WRITEFLUSH-Nachricht** wird von der [**mmioWrite-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) an eine E/A-Prozedur gesendet, um anzufordern, dass Daten in eine geöffnete Datei geschrieben werden und dass alle internen Puffer, die von der E/A-Prozedur verwendet werden, auf den Datenträger geleert werden.


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

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Anzahl der Bytes, die in die Datei geschrieben werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Bytes zurück, die tatsächlich in die Datei geschrieben wurden. Wenn ein Fehler auftritt, ist der Rückgabewert 1.

## <a name="remarks"></a>Hinweise

Die E/A-Prozedur ist dafür verantwortlich, den **lDiskOffset-Member** der [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) zu aktualisieren, um die neue Dateiposition nach dem Schreibvorgang widerzuspiegeln.

Diese Meldung entspricht der [**MMIOM \_ WRITE-Nachricht,**](mmiom-write.md) mit der Ausnahme, dass sie anfordert, dass die E/A-Prozedur ggf. ihre internen Puffer leert. Sofern eine E/A-Prozedur keine interne Pufferung durchführt, kann diese Nachricht genau wie die **MMIOM \_ WRITE-Nachricht** verarbeitet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



 

