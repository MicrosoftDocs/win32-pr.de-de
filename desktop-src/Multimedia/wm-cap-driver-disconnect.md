---
title: WM_CAP_DRIVER_DISCONNECT Meldung (VFW. h)
description: Die "WM Cap Driver Disconnect"-Nachricht trennt die Verbindung \_ \_ \_ eines Aufzeichnungs Treibers von einem Aufzeichnungs Fenster. Sie können diese Nachricht explizit oder mithilfe des "capdriverdisconnect"-Makros senden.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949752"
---
# <a name="wm_cap_driver_disconnect-message"></a>WM- \_ Cap- \_ Treiber Disconnect- \_ Nachricht

Die " **WM \_ Cap \_ Driver \_ Disconnect** "-Nachricht trennt die Verbindung eines Aufzeichnungs Treibers von einem Aufzeichnungs Fenster. Sie können diese Nachricht explizit oder mithilfe des " [**capdriverdisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) "-Makros senden.


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.

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

 

 





