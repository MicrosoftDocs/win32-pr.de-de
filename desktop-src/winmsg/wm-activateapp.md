---
description: Wird gesendet, wenn ein Fenster, das zu einer anderen Anwendung als das aktive Fenster gehört, aktiviert wird. Die Nachricht wird an die Anwendung gesendet, deren Fenster aktiviert wird, und an die Anwendung, deren Fenster deaktiviert wird.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: WM_ACTIVATEAPP Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363595"
---
# <a name="wm_activateapp-message"></a>WM \_ activateapp-Meldung

Wird gesendet, wenn ein Fenster, das zu einer anderen Anwendung als das aktive Fenster gehört, aktiviert wird. Die Nachricht wird an die Anwendung gesendet, deren Fenster aktiviert wird, und an die Anwendung, deren Fenster deaktiviert wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob das Fenster aktiviert oder deaktiviert wird. Dieser Parameter ist **true** , wenn das Fenster aktiviert wird. der Wert ist **false** , wenn das Fenster deaktiviert wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Threadbezeichner. Wenn der *wParam* -Parameter **true** ist, ist *LPARAM* der Bezeichner des Threads, der das Fenster besitzt, das deaktiviert wird. Wenn *wParam* den Wert **false** hat, ist *LPARAM* der Bezeichner des Threads, der das Fenster besitzt, das aktiviert wird.

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

[**WM \_ aktivieren**](../inputdev/wm-activate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
