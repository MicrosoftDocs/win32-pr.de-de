---
title: FILEOKSTRING-Nachricht (Commdlg.h)
description: Ein Dialogfeld Öffnen oder Speichern unter sendet die registrierte FILEOKSTRING-Nachricht an die Hookprozedur OFNHookProc, wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche OK klickt.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- FILEOKSTRING-Meldungsdialogfelder
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
ms.openlocfilehash: 24dd07faecc66bc50c408eab36bcbd8c93c460ef
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549215"
---
# <a name="fileokstring-message"></a>FILEOKSTRING-Nachricht

\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt. Es wird empfohlen, die Dialogfeld-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]

Ein Dialogfeld **Öffnen** oder **Speichern unter** sendet die registrierte **FILEOKSTRING-Nachricht** an Die Hookprozedur [*OFNHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche **OK** klickt. Die Hookprozedur kann den Dateinamen akzeptieren und zulassen, dass das Dialogfeld geschlossen wird, oder den Dateinamen ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.


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

Ein Zeiger auf eine [**OPENFILENAME-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Der **lpstrFile-Member** dieser Struktur enthält das Laufwerk, den Pfad und den Dateinamen, die vom Benutzer angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Hookprozedur 0 (null) zurückgibt, akzeptiert das Dialogfeld **Öffnen** oder **Speichern unter** den angegebenen Dateinamen und wird geschlossen.

Wenn die Hookprozedur einen Wert ungleich 0 (null) zurückgibt, lehnt das Dialogfeld **Öffnen** oder **Speichern unter** den angegebenen Dateinamen ab und bleibt geöffnet.

## <a name="remarks"></a>Hinweise

Die Hookprozedur muss die **FILEOKSTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (windows.h einschließen)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **FILEOKSTRINGW** (Unicode) und **FILEOKSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CDN \_ FILEOK**](cdn-fileok.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

