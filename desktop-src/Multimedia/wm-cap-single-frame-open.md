---
title: WM_CAP_SINGLE_FRAME_OPEN Meldung (VFW. h)
description: Die \_ Meldung zum Öffnen eines einzelnen Frames mit dem WM-Cap \_ \_ \_ öffnet die Erfassungs Datei für die Erfassung mit einem Frame. Alle vorherigen Informationen in der Erfassungs Datei werden überschrieben. Sie können diese Nachricht explizit oder mithilfe des capcapturesingleframeopen-Makros senden.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN-Nachricht (Multimedia)
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
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859249"
---
# <a name="wm_cap_single_frame_open-message"></a>WM- \_ Cap- \_ Nachricht zum Öffnen eines einzelnen \_ Frames \_

Die Meldung zum **\_ \_ \_ \_ Öffnen eines einzelnen Frames** mit dem WM-Cap öffnet die Erfassungs Datei für die Erfassung mit einem Frame. Alle vorherigen Informationen in der Erfassungs Datei werden überschrieben. Sie können diese Nachricht explizit oder mithilfe des [**capcapturesingleframeopen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) -Makros senden.


```C++
WM_CAP_SINGLE_FRAME_OPEN 
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

 

 





