---
title: WM_CAP_GET_USER_DATA Meldung (VFW. h)
description: Die WM- \_ Obergrenze \_ get \_ User \_ Data Ruft einen langen \_ ptr-Datenwert ab, der einem Aufzeichnungs Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des capgetuserdata-Makros senden.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518635"
---
# <a name="wm_cap_get_user_data-message"></a>WM- \_ Cap- \_ Meldung " \_ Benutzer \_ Daten erhalten"

Die **WM- \_ Obergrenze \_ get \_ User \_ Data** Ruft einen **langen \_ ptr** -Datenwert ab, der einem Aufzeichnungs Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**capgetuserdata**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) -Makros senden.


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der zuvor mit [**der \_ \_ \_ Benutzer \_ Daten**](wm-cap-set-user-data.md) Meldung für die WM-Abdeckung festgelegt wurde.

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

 

 





