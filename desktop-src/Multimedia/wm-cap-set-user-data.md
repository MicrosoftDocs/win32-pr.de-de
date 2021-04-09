---
title: WM_CAP_SET_USER_DATA Meldung (VFW. h)
description: In der Benutzerdaten Meldung "WM-Cap-Datensatz" wird \_ \_ \_ \_ ein langer \_ ptr-Datenwert mit einem Aufzeichnungs Fenster verknüpft. Sie können diese Nachricht explizit oder mithilfe des capsetuserdata-Makros senden.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA-Nachricht (Multimedia)
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
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106107"
---
# <a name="wm_cap_set_user_data-message"></a>WM- \_ Cap- \_ \_ Benutzer \_ Daten Meldung festlegen

In **der \_ \_ \_ Benutzer \_ Daten** Meldung "WM-Cap-Datensatz" wird ein **langer \_ ptr** -Datenwert mit einem Aufzeichnungs Fenster verknüpft. Sie können diese Nachricht explizit oder mithilfe des [**capsetuserdata**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) -Makros senden.


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*luser*
</dt> <dd>

Datenwert, der einem Aufzeichnungs Fenster zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn die streamingerfassung ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

In der Regel wird diese Nachricht verwendet, um auf einen Datenblock zu verweisen, der mit einem Aufzeichnungs Fenster verknüpft ist.

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

 

 





