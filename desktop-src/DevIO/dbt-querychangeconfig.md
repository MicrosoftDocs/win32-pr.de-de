---
description: Das System überträgt das DBT QUERYCHANGECONFIG-Geräteereignis, um die Berechtigung zum Ändern der aktuellen Konfiguration (Dock oder \_ Abdocken) an fordern. Jede Anwendung kann diese Anforderung verweigern und die Änderung abbrechen.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e9c222fdc29f635263b45b5fd7e54ee229a33d7dee1ff31cd1e3072bfe6e84f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318420"
---
# <a name="dbt_querychangeconfig-event"></a>DBT \_ QUERYCHANGECONFIG-Ereignis

Das System überträgt das DBT QUERYCHANGECONFIG-Geräteereignis, um die Berechtigung zum Ändern der aktuellen Konfiguration (Dock oder \_ Abdocken) an fordern. Jede Anwendung kann diese Anforderung verweigern und die Änderung abbrechen.

Um dieses Geräteereignis zu übertragen, verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) bei der *wParam* auf DBT \_ QUERYCHANGECONFIG und *lParam auf* 0 (null) festgelegt ist.


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

Legen Sie auf DBT \_ QUERYCHANGECONFIG fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** um die Berechtigung zum Ändern der Konfiguration zu erteilen.

Geben Sie BROADCAST \_ QUERY \_ DENY zurück, um die Berechtigung zum Ändern der Konfiguration zu verweigern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Geräteereignisse](device-events.md)
</dt> <dt>

[Geräteverwaltung Ereignisse](device-management-events.md)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




