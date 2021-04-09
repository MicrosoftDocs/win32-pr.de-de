---
title: WM_CAP_SINGLE_FRAME Meldung (VFW. h)
description: Die "WM \_ Cap \_ Single Frame"- \_ Nachricht fügt einen einzelnen Frame an eine Erfassungs Datei an, die mithilfe der Open-Message-Nachricht für das WM-Cap geöffnet wurde \_ \_ \_ \_ . Sie können diese Nachricht explizit oder mithilfe des capcapturesingleframe-Makros senden.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME-Nachricht (Multimedia)
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
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106100"
---
# <a name="wm_cap_single_frame-message"></a>WM- \_ Cap- \_ Einzel \_ Rahmen Nachricht

Die " **WM \_ Cap \_ Single \_ Frame** "-Nachricht fügt einen einzelnen Frame an eine Erfassungs Datei an, die mithilfe der [**\_ \_ \_ \_ Open**](wm-cap-single-frame-open.md) -Message-Nachricht für das WM-Cap geöffnet wurde. Sie können diese Nachricht explizit oder mithilfe des [**capcapturesingleframe**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) -Makros senden.


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

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

 

 





