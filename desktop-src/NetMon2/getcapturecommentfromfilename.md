---
description: Die GetCaptureCommentFromFilename-Funktion extrahiert den Erfassungskommentar aus einer Aufzeichnungsdatei.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: GetCaptureCommentFromFilename-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1b92b81fa00834c3a4038a6a6bb9f295246a7c0b217c99779a5d2c569dbbf982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366811"
---
# <a name="getcapturecommentfromfilename-function"></a>GetCaptureCommentFromFilename-Funktion

Die **GetCaptureCommentFromFilename-Funktion** extrahiert den Aufzeichnungskommentar aus einer [*Aufzeichnungsdatei.*](c.md)

## <a name="syntax"></a>Syntax


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpFilename* \[ In\]
</dt> <dd>

Zeiger auf den Namen der Aufzeichnungsdatei.

</dd> <dt>

*lpComment* \[ In\]
</dt> <dd>

Zeiger auf eine vorab zugeordnete Zeichenfolge für den Kommentar.

</dd> <dt>

*BufferSize* \[ In\]
</dt> <dd>

Größe der Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h. wenn der Kommentar gefunden und kopiert wird oder kein Kommentar in der Aufzeichnungsdatei vorhanden ist), lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                                 | Beschreibung                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ FILE READ ERROR (NMERR-DATEILESEFEHLER) \_ \_**</dt> </dl>     | Der Aufzeichnungskommentar kann nicht gelesen werden.<br/>                               |
| <dl> <dt>**NMERR: \_ UNGÜLTIGES \_ \_ DATEIFORMAT**</dt> </dl> | Der Kommentarrahmen ist kein gültiges Dateiformat.<br/>                     |
| <dl> <dt>**\_NMERR-DATEI \_ NICHT \_ GEFUNDEN**</dt> </dl>      | Die durch den *lpFilename-Parameter* angegebene Datei kann nicht gefunden werden.<br/> |
| <dl> <dt>**NMERR \_ – UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Einer der Parameter wird falsch angegeben.<br/>                   |



 

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **GetCaptureCommentFromFilename-Funktion** aufrufen.

Um den Kommentar einer Echtzeiterfassung abzurufen, rufen Sie die [GetCaptureComment-Funktion](getcapturecomment.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




