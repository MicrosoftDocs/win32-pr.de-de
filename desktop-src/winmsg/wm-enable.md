---
description: Wird gesendet, wenn eine Anwendung den aktivierten Zustand eines Fensters ändert.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: WM_ENABLE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348134"
---
# <a name="wm_enable-message"></a>WM- \_ Aktivierungs Nachricht

Wird gesendet, wenn eine Anwendung den aktivierten Zustand eines Fensters ändert. Er wird an das Fenster gesendet, dessen aktivierter Zustand geändert wird. Diese Nachricht wird gesendet, bevor die [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) -Funktion zurückgegeben wird, aber nachdem der aktivierte Zustand (das [**\_ Deaktivierte WS**](window-styles.md) -Stilbit) des Fensters geändert wurde.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob das Fenster aktiviert oder deaktiviert wurde. Dieser Parameter ist **true** , wenn das Fenster aktiviert wurde, oder **false** , wenn das Fenster deaktiviert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
