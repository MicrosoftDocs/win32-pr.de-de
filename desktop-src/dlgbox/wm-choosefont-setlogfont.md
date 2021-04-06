---
title: WM_CHOOSEFONT_SETLOGFONT Meldung (kommdlg. h)
description: Eine Anwendung sendet die Meldung "WM \_ choosefont \_ setlogfont" an ein Schriftart Dialogfeld, um die aktuellen Informationen zur logischen Schriftart festzulegen.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Dialog Felder WM_CHOOSEFONT_SETLOGFONT Meldung
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
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742584"
---
# <a name="wm_choosefont_setlogfont-message"></a>WM \_ choosefont- \_ setlogfont-Meldung

Eine Anwendung sendet die Meldung " **WM \_ choosefont \_ setlogfont** " an ein **Schriftart** Dialogfeld, um die aktuellen Informationen zur logischen Schriftart festzulegen.


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

Ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die aktuelle logische Schriftart enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Wenn Sie zum Erstellen eines **Schriftart** Dialogfelds die [**choolfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Funktion aufzurufen, können Sie den **lplogfont** -Member der [**chooonfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur verwenden, um eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur anzugeben, die Anfangswerte für das Dialogfeld enthält. Verwenden Sie die " **WM \_ choosefont \_ setlogfont** "-Meldung, um eine **LOGFONT** -Struktur mit unterschiedlichen Werten anzugeben, während das Dialogfeld **Schriftart** geöffnet ist.

In der Regel würden Sie die **WM \_ choosefont- \_ setlogfont** -Nachricht von einer [**cfhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) -Hook-Prozedur senden. Die Hook-Prozedur kann auch die Nachrichten [**WM \_ choosefont \_ getlogfont**](wm-choosefont-getlogfont.md) und [**WM \_ choosefont \_ setFlags**](wm-choosefont-setflags.md) senden.

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

[**WM- \_ Auswahl Schriftart \_ getlogfont**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ choosefont- \_ setFlags**](wm-choosefont-setflags.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**"LogFont"**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

