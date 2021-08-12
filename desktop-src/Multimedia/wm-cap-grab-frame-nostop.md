---
title: WM_CAP_GRAB_FRAME_NOSTOP (Vfw.h)
description: Die MELDUNG WM CAP GRAB FRAME NOSTOP füllt den Framepuffer mit einem einzelnen \_ unkomprimierten Frame vom \_ \_ Erfassungsgerät und zeigt ihn \_ an.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81c581ad7e3913640271b32b18791ebf7b48ed09cd365af82ed263449f05471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622599"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>WM \_ CAP GRAB FRAME \_ \_ \_ NOSTOP message

Die **MELDUNG WM CAP GRAB FRAME \_ \_ \_ \_ NOSTOP** füllt den Framepuffer mit einem einzelnen unkomprimierten Frame vom Erfassungsgerät und zeigt ihn an. Im Gegensatz zur [**WM \_ CAP GRAB \_ \_ FRAME-Meldung**](wm-cap-grab-frame.md) wird der Status der Überlagerung oder Vorschau nicht durch diese Meldung geändert. Sie können diese Nachricht explizit oder mithilfe des [**Makros capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) senden.


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Informationen zum Installieren von Rückruffunktionen finden Sie in den [**Meldungen WM CAP SET \_ \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) und [**WM CAP SET \_ \_ \_ CALLBACK \_ FRAME.**](wm-cap-set-callback-frame.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





