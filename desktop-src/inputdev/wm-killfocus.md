---
title: WM_KILLFOCUS Meldung (Winuser. h)
description: Wird sofort an ein Fenster gesendet, bevor es den Tastaturfokus verliert.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Tastatur-und Maus Eingaben für WM_KILLFOCUS Nachricht
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040471"
---
# <a name="wm_killfocus-message"></a>WM- \_ killfocus-Meldung

Wird sofort an ein Fenster gesendet, bevor es den Tastaturfokus verliert.


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, das den Tastaturfokus erhält. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung eine Einfügemarke anzeigt, sollte die Einfügemarke zu diesem Zeitpunkt zerstört werden.

Nehmen Sie bei der Verarbeitung dieser Nachricht keine Funktionsaufrufe vor, die ein Fenster anzeigen oder aktivieren. Dies bewirkt, dass der Thread die Steuerung übernimmt und dazu führt, dass die Anwendung nicht mehr auf Nachrichten reagiert. Weitere Informationen finden Sie unter [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).

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

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM- \_ SetFocus**](wm-setfocus.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastatureingabe](keyboard-input.md)
</dt> </dl>

 

