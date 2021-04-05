---
title: WM_CAP_GRAB_FRAME_NOSTOP Meldung (VFW. h)
description: Die " \_ WM \_ Cap \_ Capture Frame" \_ -nostoppmeldung füllt den Frame Puffer mit einem einzelnen unkomprimierten Frame aus dem Erfassungsgerät und zeigt ihn an.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP-Nachricht (Multimedia)
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
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859140"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>WM- \_ Obergrenze für \_ \_ Abbild \_ Ende-Nachricht

Die " **WM Cap Capture Frame"- \_ \_ \_ \_ nostoppmeldung** füllt den Frame Puffer mit einem einzelnen unkomprimierten Frame aus dem Erfassungsgerät und zeigt ihn an. Anders als bei der " [**WM Cap"- \_ \_ \_ Abbild**](wm-cap-grab-frame.md) Nachricht wird der Zustand der Überlagerung oder der Vorschau nicht von dieser Nachricht geändert. Sie können diese Nachricht explizit oder mithilfe des [**capgrabframenostop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) -Makros senden.


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
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

 

 





