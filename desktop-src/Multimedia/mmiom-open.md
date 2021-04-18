---
title: MMIOM_OPEN Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Nachricht wird von der mmioopen-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geöffnet oder gelöscht wird.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345531"
---
# <a name="mmiom_open-message"></a>Meldung zum Öffnen von mmiom \_

Die **mmiom \_** -Nachricht wird von der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geöffnet oder gelöscht wird.


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszfilename*
</dt> <dd>

NULL-terminierte Zeichenfolge, die den Namen der zu öffnenden Datei enthält.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg "mmsyserr \_ noError" zurück oder andernfalls einen Fehler. Folgende Fehler Werte sind möglich:



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| mmiom \_ cannotopen  | Die Datei konnte nicht geöffnet werden.               |
| mmiom- \_ outo-Memory | Der Arbeitsspeicher reicht nicht aus, um den Vorgang auszuführen. |



 

## <a name="remarks"></a>Bemerkungen

Der **dwFlags** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur enthält Flags, die an die [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion übergeben werden.

Der **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur wird mit 0 (null) initialisiert. Wenn dieser Wert falsch ist, muss er von der e/a-Prozedur korrigiert werden.

Wenn die Anwendung eine [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur an [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)übergeben hat, wird der Rückgabewert im **werrorret** -Member zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



 

