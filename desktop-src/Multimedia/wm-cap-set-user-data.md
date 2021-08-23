---
title: WM_CAP_SET_USER_DATA Meldung (Vfw.h)
description: Die \_ WM CAP \_ SET USER \_ \_ DATA-Meldung ordnet einen LONG \_ PTR-Datenwert einem Erfassungsfenster zu. Sie können diese Nachricht explizit oder mithilfe des CapSetUserData-Makros senden.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b4a192b774572ea374b08d4a4128389281e44ee00614806841b0b007d978b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803550"
---
# <a name="wm_cap_set_user_data-message"></a>\_WM CAP SET USER \_ \_ \_ DATA-Meldung

Die **WM CAP SET USER \_ \_ \_ \_ DATA-Meldung** ordnet einen **LONG \_ PTR-Datenwert** einem Erfassungsfenster zu. Sie können diese Nachricht explizit oder mithilfe des [**CapSetUserData-Makros**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) senden.


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

Datenwert, der einem Erfassungsfenster zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn die Streamingerfassung ausgeführt wird.

## <a name="remarks"></a>Hinweise

In der Regel wird diese Meldung verwendet, um auf einen Datenblock zu verweisen, der einem Erfassungsfenster zugeordnet ist.

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

 

 





