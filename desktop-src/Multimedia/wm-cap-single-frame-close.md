---
title: WM_CAP_SINGLE_FRAME_CLOSE Meldung (VFW. h)
description: Die "WM \_ Cap \_ Single Frame Close"- \_ \_ Nachricht schließt die Erfassungs Datei, die von der Nachricht zum Öffnen des WM-Cap geöffnet wurde \_ \_ \_ \_ . Sie können diese Nachricht explizit oder mithilfe des capcapturesingleframeclose-Makros senden.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE-Nachricht (Multimedia)
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
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743545"
---
# <a name="wm_cap_single_frame_close-message"></a>WM- \_ Cap- \_ Nachricht zum Schließen eines einzelnen \_ Frames \_

Die " **WM \_ Cap \_ Single \_ Frame \_ Close** "-Nachricht schließt die Erfassungs Datei, die von der Nachricht zum [**\_ \_ \_ \_ Öffnen des WM-Cap**](wm-cap-single-frame-open.md) geöffnet wurde. Sie können diese Nachricht explizit oder mithilfe des [**capcapturesingleframeclose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) -Makros senden.


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Installieren von Rückruf Funktionen finden Sie in den Rückruf-und [**WM- \_ Cap \_ - \_ \_**](wm-cap-set-callback-frame.md) Set-Rückruf [**\_ \_ \_ \_ Fehlern**](wm-cap-set-callback-error.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





