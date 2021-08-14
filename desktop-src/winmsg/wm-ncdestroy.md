---
description: Benachrichtigt ein Fenster, dass sein Nicht-Clientbereich zerstört wird. Die DestroyWindow-Funktion sendet die WM \_ NCDESTROY-Nachricht an das Fenster nach der WM \_ DESTROY-Nachricht.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: WM_NCDESTROY (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2e74db0abf22fc2fb3d2a16b5cc63187514d1bee26079490c8d19eae13787e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200046"
---
# <a name="wm_ncdestroy-message"></a>WM \_ NCDESTROY-Meldung

Benachrichtigt ein Fenster, dass sein Nicht-Clientbereich zerstört wird. Die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) sendet die **WM \_ NCDESTROY-Nachricht** an das Fenster nach der [**WM \_ DESTROY-Nachricht.**](wm-destroy.md) [**WM \_ DESTROY wird**](wm-destroy.md) verwendet, um das zugeordnete Speicherobjekt frei zu geben, das dem Fenster zugeordnet ist.

Die **WM \_ NCDESTROY-Nachricht** wird gesendet, nachdem die untergeordneten Fenster zerstört wurden. Im Gegensatz dazu wird [**WM \_ DESTROY**](wm-destroy.md) gesendet, bevor die untergeordneten Fenster zerstört werden.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCDESTROY                    0x0082
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

Diese Meldung gibt jeglichen internen Speicher frei, der für das Fenster zugeordnet ist.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**WM \_ DESTROY**](wm-destroy.md)
</dt> <dt>

[**WM \_ NCCREATE**](wm-nccreate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
