---
description: Das System überträgt das DBT \_ DEVNODES CHANGED-Geräteereignis, wenn ein Gerät dem System hinzugefügt \_ oder daraus entfernt wurde. Anwendungen, die Listen von Geräten im System verwalten, sollten ihre Listen aktualisieren.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d43873241c3f72336dd996fb9fa3486229d9ffcf522923d68ab606313afb7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539160"
---
# <a name="dbt_devnodes_changed-event"></a>DBT \_ DEVNODES \_ CHANGED-Ereignis

Das System überträgt das DBT \_ DEVNODES CHANGED-Geräteereignis, wenn ein Gerät dem System hinzugefügt \_ oder daraus entfernt wurde. Anwendungen, die Listen von Geräten im System verwalten, sollten ihre Listen aktualisieren.

Um dieses Geräteereignis zu übertragen, verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) bei der *wParam* auf DBT \_ DEVNODES CHANGED und \_ *lParam auf* 0 (null) festgelegt ist.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Das Fensterhandle

</dd> <dt>

*uMsg* 
</dt> <dd>

Der [**WM \_ DEVICECHANGE-Nachrichtenbezeichner.**](wm-devicechange.md)

</dd> <dt>

*wParam* 
</dt> <dd>

Legen Sie auf DBT \_ DEVNODES \_ CHANGED fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Es gibt keine zusätzlichen Informationen darüber, welches Gerät dem System hinzugefügt oder daraus entfernt wurde. Anwendungen, die weitere Informationen benötigen, sollten sich mithilfe der [**RegisterDeviceNotification-Funktion für Gerätebenachrichtigungen**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) registrieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Geräteereignisse](device-events.md)
</dt> <dt>

[Geräteverwaltung Ereignisse](device-management-events.md)
</dt> <dt>

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




