---
description: Wird von einer computerbasierten Schulungs Anwendung (CBT) zum Trennen von Benutzereingabe Nachrichten von anderen Nachrichten gesendet, die über die Prozedur "WH \_ journalplayback" gesendet werden.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: WM_QUEUESYNC Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348027"
---
# <a name="wm_queuesync-message"></a>WM \_ queuesync-Meldung

Wird von einer computerbasierten Schulungs Anwendung (CBT) zum Trennen von Benutzereingabe Nachrichten von anderen Nachrichten gesendet, die über die Prozedur " [**WH \_ journalplayback**](about-hooks.md) " gesendet werden.


```C++
#define WM_QUEUESYNC                    0x0023
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

Typ: **void**

Eine CBT-Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Wenn eine CBT-Anwendung die " [**WH \_ journalplayback**](about-hooks.md) "-Prozedur verwendet, sind die erste und die letzte Nachricht **WM \_ queuesync**. Dies ermöglicht es der CBT-Anwendung, vom Benutzer initiierte Nachrichten abzufangen und zu untersuchen, ohne dies für Ereignisse zu tun, die Sie sendet.

Wenn eine Anwendung ein **null** -Fenster Handle angibt, wird die Meldung in der Nachrichten Warteschlange des aktiven Fensters gepostet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[*Journalplaybackproc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Licher**
</dt> <dt>

[Hooks](hooks.md)
</dt> </dl>

 

 
