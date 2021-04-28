---
title: WM_INITMENUPOPUP-Nachricht (Winuser.h)
description: 'WM_INITMENUPOPUP Meldung: Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.'
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP Meldung Menüs und andere Ressourcen
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
ms.openlocfilehash: 6d850547d57596dd36b36b941d1782c2aee1f5b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092518"
---
# <a name="wm_initmenupopup-message"></a>WM \_ INITMENUPOPUP-Nachricht

Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Dropdownmenü oder untermenü.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt die nullbasierte relative Position des Menüelements an, das das Dropdownmenü oder Untermenü öffnet.

Das Wort in hoher Reihenfolge gibt an, ob das Dropdownmenü das Fenstermenü ist. Wenn das Menü das Fenstermenü ist, ist dieser Parameter **TRUE.** Andernfalls ist es **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ INITMENU**](wm-initmenu.md)
</dt> <dt>

**Konzept**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

