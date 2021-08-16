---
title: WM_INITMENUPOPUP (Winuser.h)
description: 'WM_INITMENUPOPUP: Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.'
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP von Nachrichtenmenüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba23607dcb8da7fb282e380e87fe6a2cbb9a26a50850845a5877d036983665f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869599"
---
# <a name="wm_initmenupopup-message"></a>WM \_ INITMENUPOPUP-Meldung

Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Dropdownmenü oder Untermenü.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt die nullbasierte relative Position des Menüelements an, das das Dropdownmenü oder Untermenü öffnet.

Das obere Wort gibt an, ob das Dropdownmenü das Fenstermenü ist. Wenn das Menü das Fenstermenü ist, ist dieser Parameter **TRUE;** Andernfalls ist dies **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ INITMENU**](wm-initmenu.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

