---
title: WM_KILLFOCUS Meldung (Winuser.h)
description: Wird direkt vor dem Verlust des Tastaturfokus an ein Fenster gesendet.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS Meldung Tastatur- und Mauseingabe
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
ms.openlocfilehash: 644ea7d82a2ae3f316985a882c284d77f3869a75341142d4372b612d66ada1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757454"
---
# <a name="wm_killfocus-message"></a>WM \_ KILLFOCUS-Nachricht

Wird direkt vor dem Verlust des Tastaturfokus an ein Fenster gesendet.


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

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung ein Caretzeichen anzeigt, sollte das Caretzeichen an diesem Punkt zerstört werden.

Nehmen Sie während der Verarbeitung dieser Nachricht keine Funktionsaufrufe vor, die ein Fenster anzeigen oder aktivieren. Dies führt dazu, dass der Thread die Kontrolle übergibt und die Anwendung nicht mehr auf Nachrichten reagiert. Weitere Informationen finden Sie unter [Nachrichten-Deadlocks.](/windows/desktop/winmsg/about-messages-and-message-queues)

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

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ SETFOCUS**](wm-setfocus.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastatureingaben](keyboard-input.md)
</dt> </dl>

 

