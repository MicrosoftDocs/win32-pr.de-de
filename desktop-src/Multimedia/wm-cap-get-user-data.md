---
title: WM_CAP_GET_USER_DATA-Nachricht (Vfw.h)
description: Die \_ WM CAP \_ GET USER \_ \_ DATA-Nachricht ruft einen LONG PTR-Datenwert ab, der \_ einem Erfassungsfenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des Makros capGetUserData senden.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a79a513d415d166ab2715a181a6d8fc366b60480caf2982f6bbc53eadf90d96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892030"
---
# <a name="wm_cap_get_user_data-message"></a>WM \_ CAP GET USER DATA \_ \_ \_ message

Die **WM CAP GET USER \_ \_ \_ \_ DATA-Nachricht** ruft einen **LONG \_ PTR-Datenwert** ab, der einem Erfassungsfenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**Makros capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) senden.


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der zuvor mithilfe der [**WM CAP SET USER \_ \_ \_ \_ DATA-Meldung**](wm-cap-set-user-data.md) gespeichert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





