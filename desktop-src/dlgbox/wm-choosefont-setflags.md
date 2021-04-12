---
title: WM_CHOOSEFONT_SETFLAGS Meldung (kommdlg. h)
description: Eine Anwendung sendet die WM \_ choosefont- \_ setFlags-Nachricht an ein Schriftart Dialogfeld, um die Anzeigeoptionen für das Dialogfeld festzulegen.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Dialog Felder WM_CHOOSEFONT_SETFLAGS Meldung
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
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104882"
---
# <a name="wm_choosefont_setflags-message"></a>WM \_ choosefont \_ setFlags-Nachricht

Eine Anwendung sendet die **WM \_ choosefont- \_ setFlags** -Nachricht an ein **Schriftart** Dialogfeld, um die Anzeigeoptionen für das Dialogfeld festzulegen.


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

Ein Zeiger auf eine [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Struktur, die neue Einstellungen im **Flags** -Member enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) erstellt ein Dialogfeld **Schriftart** und verwendet eine [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , um die Anfangswerte für den **Flags** -Member anzugeben. Verwenden Sie die " **WM \_ choosefont \_ setFlags** "-Meldung, um unterschiedliche Werte für den **Flags** -Member anzugeben, während das Dialogfeld **Schriftart** geöffnet ist.

Normalerweise sollten Sie die **WM \_ choosefont- \_ setFlags** -Nachricht von einer [**cfhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) -Hook-Prozedur senden.

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

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

