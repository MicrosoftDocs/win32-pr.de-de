---
description: Benachrichtigt ein Fenster, dass sein nicht-Client Bereich zerstört wird. Die DestroyWindow-Funktion sendet die WM \_ ncdestroy-Meldung an das Fenster nach der WM-Lösch \_ Nachricht.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: WM_NCDESTROY Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959812"
---
# <a name="wm_ncdestroy-message"></a>WM- \_ ncdestroy-Meldung

Benachrichtigt ein Fenster, dass sein nicht-Client Bereich zerstört wird. Die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion sendet die **WM \_ ncdestroy** -Meldung an das Fenster nach der WM-Lösch Nachricht. [**\_**](wm-destroy.md) [**Die WM- \_ Zerstörung**](wm-destroy.md) wird verwendet, um das zugeordnete Speicher Objekt freizugeben, das dem Fenster zugeordnet ist.

Die **WM \_ ncdestroy** -Nachricht wird gesendet, nachdem die untergeordneten Fenster zerstört wurden. Im Gegensatz dazu wird die [**WM- \_ Zerstörung**](wm-destroy.md) gesendet, bevor die untergeordneten Fenster zerstört werden.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Diese Meldung gibt den Arbeitsspeicher frei, der intern für das Fenster reserviert wurde.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**WM \_ zerstören**](wm-destroy.md)
</dt> <dt>

[**WM- \_ nccreate**](wm-nccreate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
