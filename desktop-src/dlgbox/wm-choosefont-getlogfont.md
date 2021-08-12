---
title: WM_CHOOSEFONT_GETLOGFONT Meldung (Commdlg.h)
description: Eine Anwendung sendet die WM \_ CHOOSEFONT \_ GETLOGFONT-Nachricht an ein Dialogfeld Schriftart, um Informationen zur aktuellen Schriftartauswahl des Benutzers abzurufen.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Dialogfelder für WM_CHOOSEFONT_GETLOGFONT Meldung
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
ms.openlocfilehash: 1fb429c3cd66af28485edf2979d2efbe50b3205a2142e963c8c3bb51ef5713f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280432"
---
# <a name="wm_choosefont_getlogfont-message"></a>WM \_ CHOOSEFONT \_ GETLOGFONT-Nachricht

Eine Anwendung sendet die **WM \_ CHOOSEFONT \_ GETLOGFONT-Nachricht** an ein Dialogfeld **Schriftart,** um Informationen zur aktuellen Schriftartauswahl des Benutzers abzurufen.


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

Ein Zeiger auf eine LOGFONT-Struktur, die Informationen zur aktuellen Schriftartauswahl des Benutzers [**empfängt.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**Funktion ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) erstellt ein Dialogfeld **Schriftart.** Wenn der Benutzer das Dialogfeld **Schriftart** schließt, gibt die **ChooseFont-Funktion** Informationen zur Schriftartauswahl des Benutzers in der [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) zurück. Der **lpLogFont-Member** der **CHOOSEFONT-Struktur** ist ein Zeiger auf eine [**LOGFONT-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

Verwenden Sie die **WM \_ CHOOSEFONT \_ GETLOGFONT-Meldung,** um Informationen zur aktuellen Schriftartauswahl des Benutzers abzurufen, während das Dialogfeld **Schriftart** geöffnet ist. Wenn Sie beispielsweise die Schaltfläche **Anwenden** im Dialogfeld **Schriftart** aktivieren, senden Sie die Meldung, um die Schriftartinformationen abzurufen, die auf die aktuelle Textauswahl angewendet werden sollen.

In der Regel aktivieren Sie eine [*CFHookProc-Hookprozedur,*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) um [**WM \_ COMMAND-Meldungen**](/windows/desktop/menurc/wm-command) für die Schaltfläche **Anwenden** zu verarbeiten. Wenn der Benutzer auf die Schaltfläche **Anwenden** klickt, sendet die Hookprozedur die **WM \_ CHOOSEFONT \_ GETLOGFONT-Meldung** an das Dialogfeld.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

