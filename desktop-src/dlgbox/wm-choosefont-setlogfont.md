---
title: WM_CHOOSEFONT_SETLOGFONT Meldung (Commdlg.h)
description: Eine Anwendung sendet die \_ WM-Nachricht CHOOSEFONT \_ SETLOGFONT an ein Dialogfeld Schriftart, um die aktuellen logischen Schriftartinformationen festzulegen.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Dialogfelder für WM_CHOOSEFONT_SETLOGFONT Meldung
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d35c6f54679389b411417e5539382fd322c0873e6dba87fc90efb93b8be7ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503423"
---
# <a name="wm_choosefont_setlogfont-message"></a>WM \_ CHOOSEFONT \_ SETLOGFONT-Meldung

Eine Anwendung sendet die **\_ WM-Nachricht CHOOSEFONT \_ SETLOGFONT** an ein Dialogfeld **Schriftart,** um die aktuellen logischen Schriftartinformationen festzulegen.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**LOGFONT-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-logfonta) die Informationen zur aktuellen logischen Schriftart enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Hinweise

Wenn Sie die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) aufrufen, um **ein** Schriftartdialogfeld zu erstellen, können Sie den **lpLogFont-Member** der [**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) verwenden, um eine [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) anzugeben, die Anfangswerte für das Dialogfeld enthält. Verwenden Sie die **WM \_ CHOOSEFONT \_ SETLOGFONT-Meldung,** um eine **LOGFONT-Struktur** mit unterschiedlichen Werten anzugeben, während das Dialogfeld **Schriftart** geöffnet ist.

In der Regel senden Sie die **WM \_ CHOOSEFONT \_ SETLOGFONT-Nachricht** von einer [**CFHookProc-Hookprozedur.**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) Die Hookprozedur kann auch die [**WM \_ CHOOSEFONT \_ GETLOGFONT-**](wm-choosefont-getlogfont.md) und [**WM \_ CHOOSEFONT \_ SETFLAGS-Nachrichten**](wm-choosefont-setflags.md) senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

