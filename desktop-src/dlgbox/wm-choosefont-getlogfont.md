---
title: WM_CHOOSEFONT_GETLOGFONT Meldung (kommdlg. h)
description: Eine Anwendung sendet die WM \_ choosefont \_ getlogfont-Nachricht an ein Schriftart Dialogfeld, um Informationen über die aktuelle Schriftart Auswahl des Benutzers abzurufen.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Dialog Felder WM_CHOOSEFONT_GETLOGFONT Meldung
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339998"
---
# <a name="wm_choosefont_getlogfont-message"></a>WM- \_ Auswahl Schriftart \_ getlogfont

Eine Anwendung sendet die **WM \_ choosefont \_ getlogfont** -Nachricht an ein **Schriftart** Dialogfeld, um Informationen über die aktuelle Schriftart Auswahl des Benutzers abzurufen.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die aktuelle Schriftart Auswahl des Benutzers empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) erstellt ein Dialogfeld für die **Schriftart** . Wenn der Benutzer das Dialogfeld **Schriftart** schließt, gibt die **Auswahl Schriftart** Informationen über die Schriftart Auswahl des Benutzers in der [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) zurück. Der **lplogfont** -Member der **chooonfont** -Struktur ist ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.

Verwenden Sie die " **WM \_ choocfont \_ getlogfont** "-Meldung, um Informationen über die aktuelle Schriftart Auswahl des Benutzers zu erhalten, während das Dialogfeld **Schriftart** geöffnet ist. Wenn Sie z. b. die Schaltfläche **anwenden** im Dialogfeld **Schriftart** aktivieren, senden Sie die Nachricht, um die Schriftart Informationen zu erhalten, die auf die aktuelle Textauswahl angewendet werden sollen.

In der Regel aktivieren Sie eine [*cfhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) -Hook-Prozedur, um die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen für die Schaltfläche **anwenden** zu verarbeiten. Wenn **der Benutzer auf die Schalt** Fläche übernehmen klickt, sendet die Hook-Prozedur die Meldung **WM \_ choocfont \_ getlogfont** an das Dialogfeld.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommdlg. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Cfhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**"LogFont"**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

