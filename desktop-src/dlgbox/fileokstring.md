---
title: Fileokstring-Nachricht (kommdlg. h)
description: Ein Dialogfeld zum Öffnen oder speichern unter sendet die registrierte fileokstring-Nachricht an Ihre Hook-Prozedur, ofnhost-proc, wenn der Benutzer einen Dateinamen angibt, und klickt auf die Schaltfläche OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Fileokstring-Meldungs Dialogfelder
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61208ddebc63f1186c2947416e451231f0bea24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478981"
---
# <a name="fileokstring-message"></a>Fileokstring-Nachricht

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet die registrierte **fileokstring** -Nachricht an Ihre Hook-Prozedur, [*ofnhost-proc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), wenn der Benutzer einen Dateinamen angibt, und klickt auf die Schaltfläche **OK** . Die Hook-Prozedur kann den Dateinamen akzeptieren und das Dialogfeld schließen oder den Dateinamen ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur. Der **lpstraufile** -Member dieser Struktur enthält das Laufwerk, den Pfad und den Dateinamen, die vom Benutzer angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hook-Prozedur NULL zurückgibt, akzeptiert das Dialogfeld **Öffnen** oder **Speichern** unter den angegebenen Dateinamen und wird geschlossen.

Wenn die Hook-Prozedur einen Wert ungleich 0 (null) zurückgibt, lehnt das Dialogfeld **Öffnen** oder speichern unter den angegebenen Dateinamen **ab** und bleibt geöffnet.

## <a name="remarks"></a>Bemerkungen

Die Hook-Prozedur muss die **fileokstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Fileokstringw** (Unicode) und **fileokstraninga** (ANSI)<br/>                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CDN- \_ Datei OK**](cdn-fileok.md)
</dt> <dt>

[**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

