---
title: Findmsgstring-Nachricht (kommdlg. h)
description: Im Dialogfeld Suchen oder ersetzen wird die registrierte Nachricht findmsgstring an die Fenster Prozedur des Besitzer Fensters gesendet, wenn der Benutzer auf die Schaltfläche weiter suchen, ersetzen oder alle ersetzen klickt oder das Dialogfeld schließt.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Dialog Felder für die findmsgstring-Meldung
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518875"
---
# <a name="findmsgstring-message"></a>Findmsgstring-Meldung

Im Dialogfeld **Suchen** oder **ersetzen** wird die registrierte Nachricht **findmsgstring** an die Fenster Prozedur des Besitzer Fensters gesendet, wenn der Benutzer auf die Schaltfläche **weiter suchen**, **ersetzen** oder **Alle ersetzen** klickt oder das Dialogfeld schließt.


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur. Die Elemente dieser Struktur enthalten die aktuelle Benutzereingabe, einschließlich der zu suchenden Zeichenfolge, der Ersetzungs Zeichenfolge (sofern vorhanden) und der Such-und Ersetzungs Optionen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Sie müssen die **findmsgstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.

Wenn Sie das Dialogfeld erstellen, verwenden Sie das **hwndOwner** -Element der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur, um das Fenster zum Empfangen von **findmsgstring** -Nachrichten zu identifizieren.

Der **Flags** -Member der [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) -Struktur enthält eines der folgenden Flags, um das Ereignis anzugeben, das die Meldung verursacht hat.



| Flag                            | Bedeutung                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ Dialogterm** (0x00000040) | Das Dialogfeld wird geschlossen. Nachdem das Besitzer Fenster diese Nachricht verarbeitet hat, ist ein Handle für das Dialogfeld nicht mehr gültig.                                                                                    |
| **Fr \_ FindNext** (0x00000008)   | Der Benutzer hat auf die Schaltfläche " **weiter suchen** " im Dialogfeld " **Suchen** oder **ersetzen** " geklickt. Der **lpstraufindwhat** -Member gibt die zu suchende Zeichenfolge an.                                                         |
| **Fr \_ Ersetzen** (0x00000010)    | Der Benutzer hat im Dialogfeld " **ersetzen** " auf die Schaltfläche " **ersetzen** " geklickt. Der **lpstraufindwhat** -Member gibt die zu ersetzende Zeichenfolge an, und der **lpstraureplacewith** -Member gibt die Ersatz Zeichenfolge an     |
| **Fr \_ ReplaceAll** (0x00000020) | Der Benutzer hat auf die Schaltfläche **Alle ersetzen** im Dialogfeld **ersetzen** geklickt. Der **lpstraufindwhat** -Member gibt die zu ersetzende Zeichenfolge an, und der **lpstraureplacewith** -Member gibt die Ersatz Zeichenfolge an |



 

Für eine " **weiter** suchen"-oder " **Alle ersetzen** "-Meldung kann das **Flags** -Element eines oder mehrere der folgenden Flags enthalten, um die Suchoptionen anzugeben.



| Flag                           | Bedeutung                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ Down** (0x00000001)      | Wenn festgelegt, wird die **nach-unten** -Taste der Optionsfeld Richtung ausgewählt und zeigt an, dass der Benutzer vom aktuellen Speicherort bis zum Ende des Dokuments suchen möchte. Wenn die Option " **\_ nach unten** " nicht festgelegt ist, wird die Schaltfläche "nach **oben** " ausgewählt, sodass der Benutzer am Anfang des Dokuments suchen möchte.       |
| **Fr \_ MatchCase** (0x00000004) | Wenn diese Option festgelegt ist, wird das Kontrollkästchen **Groß-/Kleinschreibung** aktivieren ausgewählt Wenn **fr \_ MatchCase** nicht festgelegt ist, wird das Kontrollkästchen deaktiviert, sodass bei der Suche die Groß-/Kleinschreibung nicht beachtet wird.                                                                         |
| **Fr \_ Wholeword** (0x00000002) | Wenn diese Option festgelegt ist, wird das Kontrollkästchen **Nur ganzes Wort** suchen aktiviert, das anzeigt, dass der Benutzer nur nach ganzen Wörtern suchen möchte, die der Such Zeichenfolge entsprechen. Wenn **fr \_ wholeword** nicht festgelegt ist, ist das Kontrollkästchen deaktiviert, sodass Sie auch nach Wortfragmenten suchen müssen, die der Such Zeichenfolge entsprechen. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Findmsgstringw** (Unicode) und **findmsgstrauinga** (ANSI)<br/>                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

