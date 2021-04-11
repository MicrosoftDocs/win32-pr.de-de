---
description: Wird an ein Symbol gesendet, wenn der Benutzer anfordert, dass das Fenster bis zur vorherigen Größe und Position wieder hergestellt wird.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: WM_QUERYOPEN Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042279"
---
# <a name="wm_queryopen-message"></a>WM- \_ Meldung "queryopen"

Wird an ein Symbol gesendet, wenn der Benutzer anfordert, dass das Fenster bis zur vorherigen Größe und Position wieder hergestellt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_QUERYOPEN                    0x0013
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

Wenn das Symbol geöffnet werden kann, sollte eine Anwendung, die diese Nachricht verarbeitet, **true** zurückgeben. Andernfalls sollte **false** zurückgegeben werden, um zu verhindern, dass das Symbol geöffnet wird.

## <a name="remarks"></a>Bemerkungen

Standardmäßig gibt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion **true** zurück.

Bei der Verarbeitung dieser Nachricht sollte die Anwendung keine Aktionen ausführen, die eine Aktivierung oder eine Fokus Änderung verursachen (z. b. das Erstellen eines Dialog Felds).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
