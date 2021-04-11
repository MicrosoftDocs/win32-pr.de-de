---
description: Das System sendet das \_ geänderte Geräte Ereignis DBT Devnodes \_ , wenn ein Gerät dem System hinzugefügt oder daraus entfernt wurde. Anwendungen, die Listen von Geräten im System verwalten, sollten Ihre Listen aktualisieren.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126788"
---
# <a name="dbt_devnodes_changed-event"></a>Geändertes DBT- \_ Devnodes- \_ Ereignis

Das System sendet das \_ geänderte Geräte Ereignis DBT Devnodes \_ , wenn ein Gerät dem System hinzugefügt oder daraus entfernt wurde. Anwendungen, die Listen von Geräten im System verwalten, sollten Ihre Listen aktualisieren.

Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ Devnodes \_ geändert und *LPARAM* auf NULL festgelegt ist.


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

*HWND* 
</dt> <dd>

Das Fensterhandle

</dd> <dt>

*Umschlag* 
</dt> <dd>

Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.

</dd> <dt>

*wParam* 
</dt> <dd>

Legen Sie fest, dass DBT \_ Devnodes \_ geändert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="remarks"></a>Bemerkungen

Es gibt keine zusätzlichen Informationen darüber, welches Gerät dem System hinzugefügt oder daraus entfernt wurde. Anwendungen, für die weitere Informationen erforderlich sind, sollten sich mithilfe der [**registerdevicenotifi-**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Funktion für die Geräte Benachrichtigung registrieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>DBT. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Geräte Ereignisse](device-events.md)
</dt> <dt>

[Geräte Verwaltungs Ereignisse](device-management-events.md)
</dt> <dt>

[**Entwickler- \_ Broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM- \_ devicechange**](wm-devicechange.md)
</dt> </dl>

 

 




