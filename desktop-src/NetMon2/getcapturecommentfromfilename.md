---
description: Die getcapturecommentfromfilename-Funktion extrahiert den Erfassungs Kommentar aus einer Erfassungs Datei.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Getcapturecommentfromfilename-Funktion (Netmon. h)
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
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345002"
---
# <a name="getcapturecommentfromfilename-function"></a>Getcapturecommentfromfilename-Funktion

Die **getcapturecommentfromfilename** -Funktion extrahiert den Erfassungs Kommentar aus einer [*Erfassungs Datei*](c.md).

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

*lpFileName* \[ in\]
</dt> <dd>

Zeiger auf den Namen der Erfassungs Datei.

</dd> <dt>

*lpcomment* \[ in\]
</dt> <dd>

Zeiger auf eine vorab zugeordnete Zeichenfolge für den Kommentar.

</dd> <dt>

*BufferSize* \[ in\]
</dt> <dd>

Größe der Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn der Kommentar gefunden und kopiert wird oder kein Kommentar in der Erfassungs Datei vorhanden ist), ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                                 | Beschreibung                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Datei \_ Lese \_ Fehler**</dt> </dl>     | Der Erfassungs Kommentar kann nicht gelesen werden.<br/>                               |
| <dl> <dt>**Ungültiges nmerr- \_ \_ Datei \_ Format**</dt> </dl> | Der Kommentar Rahmen ist kein gültiges Dateiformat.<br/>                     |
| <dl> <dt>**die nmerr- \_ Datei wurde \_ nicht \_ gefunden.**</dt> </dl>      | Die vom *lpFileName* -Parameter angegebene Datei kann nicht gefunden werden.<br/> |
| <dl> <dt>**Ungültiger nmerr- \_ \_ Parameter**</dt> </dl>    | Einer der Parameter ist falsch angegeben.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturecommentfromfilename** -Funktion aufrufen.

Um den Kommentar einer echt Zeiterfassung abzurufen, rufen Sie die [getcapturecomment](getcapturecomment.md) -Funktion auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Getcapturecomment](getcapturecomment.md)
</dt> </dl>

 

 




