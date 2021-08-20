---
title: CDM_SETCONTROLTEXT Meldung (Commdlg.h)
description: Legt den Text für das angegebene Steuerelement im Explorer-Stil im Dialogfeld Öffnen oder Speichern unter fest.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- Dialogfelder für CDM_SETCONTROLTEXT Meldung
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75071d465d01be024a97047a134c080226f252a1bd1ffcd41dbecd4f0d469cff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721325"
---
# <a name="cdm_setcontroltext-message"></a>CDM \_ SETCONTROLTEXT-Nachricht

\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt. Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]

Legt den Text für das angegebene Steuerelement im Explorer-Stil im Dialogfeld **Öffnen** oder **Speichern unter** fest. Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner des Steuerelements, auf dessen Text festgelegt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Der neue Text für das Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das entsprechende Makro lautet wie folgt:

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

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

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Allgemeine Dialogfeldbibliothek](common-dialog-box-library.md)
</dt> </dl>

