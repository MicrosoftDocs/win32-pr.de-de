---
description: Wird gesendet, wenn ein Fenster, das zu einer anderen Anwendung als das aktive Fenster gehört, aktiviert wird. Die Meldung wird an die Anwendung gesendet, deren Fenster aktiviert wird, und an die Anwendung, deren Fenster deaktiviert wird.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: WM_ACTIVATEAPP Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9afeabe12dfcc36ae7bf2403a7757004847bcf58370f4a0a0904c9bf008e6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931890"
---
# <a name="wm_activateapp-message"></a>WM \_ ACTIVATEAPP-Nachricht

Wird gesendet, wenn ein Fenster, das zu einer anderen Anwendung als das aktive Fenster gehört, aktiviert wird. Die Meldung wird an die Anwendung gesendet, deren Fenster aktiviert wird, und an die Anwendung, deren Fenster deaktiviert wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob das Fenster aktiviert oder deaktiviert wird. Dieser Parameter ist **TRUE,** wenn das Fenster aktiviert wird. ist **FALSE,** wenn das Fenster deaktiviert wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Threadbezeichner. Wenn der *wParam-Parameter* **TRUE** ist, ist *lParam* der Bezeichner des Threads, der das zu deaktivierende Fenster besitzt. Wenn *wParam* **FALSE** ist, ist *lParam* der Bezeichner des Threads, der das aktivierte Fenster besitzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

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

[**WM \_ ACTIVATE**](../inputdev/wm-activate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
