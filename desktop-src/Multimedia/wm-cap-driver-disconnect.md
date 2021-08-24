---
title: WM_CAP_DRIVER_DISCONNECT Meldung (Vfw.h)
description: Die MELDUNG WM \_ CAP DRIVER DISCONNECT trennt einen \_ \_ Erfassungstreiber von einem Erfassungsfenster. Sie können diese Nachricht explizit oder mithilfe des Makros capDriverDisconnect senden.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6365366c6ea37b36734262d1d7a8412a7729406ff3fcc12e10ae9ba55d9ba84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803860"
---
# <a name="wm_cap_driver_disconnect-message"></a>WM \_ CAP \_ DRIVER \_ DISCONNECT-Meldung

Die **MELDUNG WM CAP DRIVER \_ \_ \_ DISCONNECT** trennt einen Erfassungstreiber von einem Erfassungsfenster. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) senden.


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn das Erfassungsfenster nicht mit einem Erfassungstreiber verbunden ist.

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

 

 





