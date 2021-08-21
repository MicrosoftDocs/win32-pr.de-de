---
title: WM_CAP_SINGLE_FRAME_OPEN-Nachricht (Vfw.h)
description: Die \_ WM CAP \_ SINGLE FRAME \_ \_ OPEN-Nachricht öffnet die Erfassungsdatei für die Singleframe-Erfassung. Alle vorherigen Informationen in der Erfassungsdatei werden überschrieben. Sie können diese Nachricht explizit oder mithilfe des Makros capCaptureSingleFrameOpen senden.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a58df70bea8971e10a769efbbc98220c46897ff6979e66ab45ae8f2ba81b971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134835"
---
# <a name="wm_cap_single_frame_open-message"></a>WM \_ CAP SINGLE FRAME \_ \_ \_ OPEN-Nachricht

Die **WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN-Nachricht** öffnet die Erfassungsdatei für die Singleframe-Erfassung. Alle vorherigen Informationen in der Erfassungsdatei werden überschrieben. Sie können diese Nachricht explizit oder mithilfe des [**Makros capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) senden.


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
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

 

 





