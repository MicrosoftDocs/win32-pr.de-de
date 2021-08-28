---
title: WM_CHOOSEFONT_SETFLAGS Meldung (Commdlg.h)
description: Eine Anwendung sendet die WM \_ CHOOSEFONT \_ SETFLAGS-Meldung an ein Dialogfeld Schriftart, um die Anzeigeoptionen für das Dialogfeld festzulegen.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Dialogfelder für WM_CHOOSEFONT_SETFLAGS Meldung
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d77290dfb3668e24d3586cf6d742b524e05fb07979de7c8d45f39998aca9708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726080"
---
# <a name="wm_choosefont_setflags-message"></a>WM \_ CHOOSEFONT \_ SETFLAGS-Meldung

Eine Anwendung sendet die **WM \_ CHOOSEFONT \_ SETFLAGS-Meldung** an ein Dialogfeld **Schriftart,** um die Anzeigeoptionen für das Dialogfeld festzulegen.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**CHOOSEFONT-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) die neue Einstellungen im **Flags-Member** enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die [**ChooseFont-Funktion**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) erstellt ein Dialogfeld **Schriftart** und verwendet eine [**CHOOSEFONT-Struktur,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) um die Anfangswerte für den **Flags-Member** anzugeben. Verwenden Sie die **WM \_ CHOOSEFONT \_ SETFLAGS-Meldung,** um unterschiedliche Werte für den **Flags-Member** anzugeben, während das Dialogfeld **Schriftart** geöffnet ist.

In der Regel sollten Sie die **WM \_ CHOOSEFONT \_ SETFLAGS-Nachricht** von einer [**CFHookProc-Hookprozedur**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) senden.

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

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

 

