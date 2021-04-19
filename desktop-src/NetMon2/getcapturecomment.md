---
description: Gibt einen Zeiger auf den Kommentar einer Aufzeichnung zurück.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Getcapturecomment-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346685"
---
# <a name="getcapturecomment-function"></a>Getcapturecomment-Funktion

Die **getcapturecomment** -Funktion gibt einen Zeiger auf den Kommentar einer Aufzeichnung zurück.

## <a name="syntax"></a>Syntax


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcapture* \[ in\]
</dt> <dd>

Ein Handle für die Erfassung. Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (d. h., wenn die Erfassung einen Kommentar enthält), ist der Rückgabewert ein Zeiger auf die Kommentar Zeichenfolge.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Ändern Sie die zurückgegebene Kommentar Zeichenfolge nicht, da es sich um die tatsächliche Kommentar Zeichenfolge in der geladenen Erfassung handelt. Alle Änderungen können die Erfassung beschädigen. Versuche, die Zeichenfolge zu ändern, führen zu einer Zugriffsverletzung.

Das Handle der Erfassung kann auf verschiedene Weise abgerufen werden, je nachdem, ob der-Befehl von einem Experten oder Parser aufgerufen wird. Für Experten wird das Handle im **hcapture** -Member der " [expertstartupinfo](expertstartupinfo.md) "-Struktur angegeben. Für Parser kann das Erfassungs Handle abgerufen werden, indem die [getframecapturehandle](getframecapturehandle.md) -Funktion aufgerufen wird.

Um den Kommentar einer Erfassung aus der Erfassungs Datei abzurufen, rufen Sie die [getcapturecommentfromfilename](getcapturecommentfromfilename.md) -Funktion auf.

[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturecomment** -Funktion aufrufen.

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

[Expertstartupinfo](expertstartupinfo.md)
</dt> <dt>

[Getcapturecommentfromfilename](getcapturecommentfromfilename.md)
</dt> <dt>

[Getframecapturehandle](getframecapturehandle.md)
</dt> </dl>

 

 




