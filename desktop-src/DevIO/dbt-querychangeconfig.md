---
description: Das System überträgt das DBT \_ querychangeconfig-Geräte Ereignis, um die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) anzufordern. Jede Anwendung kann diese Anforderung verweigern und die Änderung abbrechen.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523651"
---
# <a name="dbt_querychangeconfig-event"></a>DBT \_ querychangeconfig-Ereignis

Das System überträgt das DBT \_ querychangeconfig-Geräte Ereignis, um die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) anzufordern. Jede Anwendung kann diese Anforderung verweigern und die Änderung abbrechen.

Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ querychangeconfig und *LPARAM* auf NULL festgelegt ist.


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

Legen Sie auf DBT \_ querychangeconfig fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie **true** zurück, um die Berechtigung zum Ändern der Konfiguration zu erteilen.

Rückgabe \_ der Broadcast Abfrage \_ ablehnen, um die Berechtigung zum Ändern der Konfiguration abzulehnen.

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

[**WM- \_ devicechange**](wm-devicechange.md)
</dt> </dl>

 

 




