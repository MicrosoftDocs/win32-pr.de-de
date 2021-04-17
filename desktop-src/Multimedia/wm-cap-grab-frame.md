---
title: WM_CAP_GRAB_FRAME Meldung (VFW. h)
description: Die Sende \_ \_ \_ Rahmen Nachricht des WM-Abbilds Ruft einen einzelnen Frame aus dem Erfassungs Treiber ab und zeigt ihn an. Nach der Erfassung sind Overlay und Vorschau deaktiviert. Sie können diese Nachricht explizit oder mithilfe des capgrabframe-Makros senden.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME-Nachricht (Multimedia)
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
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477253"
---
# <a name="wm_cap_grab_frame-message"></a>WM- \_ Abdeckungs \_ \_ Nachricht zum Abbild

Die Sende Rahmen Nachricht des **WM- \_ \_ \_ Abbilds** Ruft einen einzelnen Frame aus dem Erfassungs Treiber ab und zeigt ihn an. Nach der Erfassung sind Overlay und Vorschau deaktiviert. Sie können diese Nachricht explizit oder mithilfe des [**capgrabframe**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) -Makros senden.


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
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

 

 





