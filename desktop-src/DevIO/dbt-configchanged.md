---
description: Das System überträgt das DBT \_ CONFIGCHANGED-Geräteereignis, um anzugeben, dass sich die aktuelle Konfiguration aufgrund eines Andockens oder Abdockens geändert hat. Eine Anwendung oder ein Treiber, die Daten in der Registrierung unter dem Schlüssel HKEY CURRENT CONFIG speichert, \_ \_ sollte die Daten aktualisieren.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e0d93b2a89793bb572a5c7563e54fa3114101443b43b8d6beac7955bdd6ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874515"
---
# <a name="dbt_configchanged-event"></a>DBT \_ CONFIGCHANGED-Ereignis

Das System überträgt das DBT \_ CONFIGCHANGED-Geräteereignis, um anzugeben, dass sich die aktuelle Konfiguration aufgrund eines Andockens oder Abdockens geändert hat. Eine Anwendung oder ein Treiber, die Daten in der Registrierung unter dem Schlüssel HKEY CURRENT CONFIG speichert, \_ \_ sollte die Daten aktualisieren.

Zum Übertragen dieses Geräteereignisses verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) wobei *wParam* auf DBT \_ CONFIGCHANGED und *lParam* auf 0 (null) festgelegt ist.


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

Legen Sie dbt \_ CONFIGCHANGED fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück.

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

[Geräteverwaltung-Ereignisse](device-management-events.md)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




