---
title: WM_CAP_SINGLE_FRAME-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ SINGLE \_ FRAME-Nachricht fügt einen einzelnen Frame an eine Erfassungsdatei an, die mit der WM \_ CAP SINGLE FRAME \_ \_ \_ OPEN-Nachricht geöffnet wurde. Sie können diese Nachricht explizit oder mithilfe des CapCaptureSingleFrame-Makros senden.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2080c8471849d42c2260c1f4133c996ef31e65e8a20591df531fbd24c19bc85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891790"
---
# <a name="wm_cap_single_frame-message"></a>WM \_ CAP \_ SINGLE \_ FRAME-Nachricht

Die **WM CAP SINGLE \_ \_ \_ FRAME-Nachricht** fügt einen einzelnen Frame an eine Erfassungsdatei an, die mit der [**WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN-Nachricht**](wm-cap-single-frame-open.md) geöffnet wurde. Sie können diese Nachricht explizit oder mithilfe des [**CapCaptureSingleFrame-Makros**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) senden.


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

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

 

 





