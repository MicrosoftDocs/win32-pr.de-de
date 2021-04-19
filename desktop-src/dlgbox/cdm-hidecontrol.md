---
title: CDM_HIDECONTROL Meldung (kommdlg. h)
description: Blendet das angegebene Steuerelement in einem Dialogfeld zum Öffnen oder speichern unter im Explorer-Format aus.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- Dialog Felder CDM_HIDECONTROL Meldung
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff632b7d1e3c24c84f73498846db9e6bfa68fd74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346718"
---
# <a name="cdm_hidecontrol-message"></a>CDM- \_ hidecontrol-Meldung

\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt. Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]

Blendet das angegebene Steuerelement in einem Dialogfeld zum **Öffnen** oder **Speichern** unter im Explorer-Format aus. Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner des Steuer Elements, das ausgeblendet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Nachricht weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Das entsprechende Makro lautet wie folgt:

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

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

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Licher**
</dt> <dt>

[Allgemeine Dialog Feld Bibliothek](common-dialog-box-library.md)
</dt> </dl>

 

