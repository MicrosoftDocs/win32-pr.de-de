---
title: WM_CAP_SINGLE_FRAME_CLOSE-Nachricht (Vfw.h)
description: Die WM \_ CAP \_ SINGLE FRAME \_ \_ CLOSE-Meldung schließt die Erfassungsdatei, die von der WM \_ CAP SINGLE FRAME \_ \_ \_ OPEN-Nachricht geöffnet wurde. Sie können diese Nachricht explizit oder mithilfe des Makros capCaptureSingleFrameClose senden.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f304fd0c62818562e53c6129a15b266db6f1ac000de64fb779e5cdb3e437d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134964"
---
# <a name="wm_cap_single_frame_close-message"></a>WM \_ CAP SINGLE FRAME \_ \_ \_ CLOSE-Meldung

Die **WM CAP SINGLE FRAME \_ \_ \_ \_ CLOSE-Nachricht** schließt die Erfassungsdatei, die von der [**WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN-Nachricht**](wm-cap-single-frame-open.md) geöffnet wurde. Sie können diese Nachricht explizit oder mithilfe des [**Makros capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) senden.


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
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

 

 





