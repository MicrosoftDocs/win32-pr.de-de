---
title: WM_INITMENUPOPUP Meldung (Winuser. h)
description: Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP von Meldungs Menüs und anderen Ressourcen
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
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040324"
---
# <a name="wm_initmenupopup-message"></a>"WM \_ initmenupopup"-Meldung

Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Dropdown Menü oder Untermenü.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt die null basierte relative Position des Menü Elements an, das das Dropdown Menü oder Untermenü öffnet.

Das höchst wertige Wort gibt an, ob das Dropdown Menü das Fenstermenü ist. Wenn das Menü das Menü "Fenster" ist, ist dieser Parameter " **true**". Andernfalls ist Sie **false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ InitMenu**](wm-initmenu.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

