---
title: WM_UNINITMENUPOPUP Meldung (Winuser. h)
description: Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü zerstört wurde.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519191"
---
# <a name="wm_uninitmenupopup-message"></a>\_Uninitmenupopup-Meldung der WM

Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü zerstört wurde.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Menü.

</dd> <dt>

*lParam* 
</dt> <dd>

Das hochwertige Wort identifiziert das Menü, das zerstört wurde. Dieser Parameter kann derzeit nur als **MF- \_ sysmenu** (Menü Fenster) angegeben werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung eine " [**WM \_ initmenupopup**](wm-initmenupopup.md) "-Meldung empfängt, wird eine " **WM \_ uninitmenupopup** "-Meldung empfangen.

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

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

