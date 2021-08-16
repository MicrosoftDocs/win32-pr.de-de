---
description: Wird gesendet, um bestimmte Modi abzubricht, z. B. Mauserfassung.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: WM_CANCELMODE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae26cef4919ed93bb2a1c60376ab450560cd2142cef7b3040032f791c45ab09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849299"
---
# <a name="wm_cancelmode-message"></a>WM \_ CANCELMODE-Nachricht

Wird gesendet, um bestimmte Modi abzubricht, z. B. Mauserfassung. Beispielsweise sendet das System diese Meldung an das aktive Fenster, wenn ein Dialogfeld oder Meldungsfeld angezeigt wird. Bestimmte Funktionen senden diese Nachricht auch explizit an das angegebene Fenster, unabhängig davon, ob es sich um das aktive Fenster handelt. Beispielsweise sendet die [**EnableWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-enablewindow) diese Meldung, wenn das angegebene Fenster deaktiviert wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn die **WM \_ CANCELMODE-Nachricht** gesendet wird, bricht die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die interne Verarbeitung der Standardmäßig-Scrollleisteneingabe ab, bricht die interne Menüverarbeitung ab und gibt die Mauserfassung frei.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
