---
title: WM_CAP_GRAB_FRAME-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ GRAB \_ FRAME-Nachricht ruft einen einzelnen Frame vom Erfassungstreiber ab und zeigt sie an. Nach der Erfassung sind Overlay und Vorschau deaktiviert. Sie können diese Nachricht explizit oder mithilfe des CapGrabFrame-Makros senden.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdccfc9df0f3abac7febfa78029b4ecb351ec3044c618dc4c811e91b433f0f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892040"
---
# <a name="wm_cap_grab_frame-message"></a>WM \_ CAP \_ GRAB \_ FRAME-Nachricht

Die **WM CAP GRAB \_ \_ \_ FRAME-Nachricht** ruft einen einzelnen Frame vom Erfassungstreiber ab und zeigt einen frame an. Nach der Erfassung sind Overlay und Vorschau deaktiviert. Sie können diese Nachricht explizit oder mithilfe des [**CapGrabFrame-Makros**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) senden.


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Informationen zum Installieren von Rückruffunktionen finden Sie in den Meldungen [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) und [**WM CAP SET \_ \_ \_ CALLBACK \_ FRAME.**](wm-cap-set-callback-frame.md)

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

 

 





