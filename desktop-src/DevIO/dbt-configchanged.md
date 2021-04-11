---
description: Das System überträgt das DBT \_ ConfigChanged-Geräte Ereignis, um anzugeben, dass sich die aktuelle Konfiguration aufgrund eines Andocken oder abdostems geändert hat. Eine Anwendung oder ein Treiber, die Daten in der Registrierung unter dem aktuellen Konfigurationsschlüssel HKEY speichert, \_ \_ sollte die Daten aktualisieren.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214152"
---
# <a name="dbt_configchanged-event"></a>DBT \_ ConfigChanged-Ereignis

Das System überträgt das DBT \_ ConfigChanged-Geräte Ereignis, um anzugeben, dass sich die aktuelle Konfiguration aufgrund eines Andocken oder abdostems geändert hat. Eine Anwendung oder ein Treiber, die Daten in der Registrierung unter dem aktuellen Konfigurationsschlüssel HKEY speichert, \_ \_ sollte die Daten aktualisieren.

Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ ConfigChanged und *LPARAM* auf NULL festgelegt ist.


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

Auf DBT \_ ConfigChanged festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

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

 

 




