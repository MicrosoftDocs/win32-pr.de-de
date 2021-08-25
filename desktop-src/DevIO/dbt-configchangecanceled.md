---
description: Das System überträgt das DBT-Geräteereignis CONFIGCHANGECANCELED, wenn eine Anforderung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) \_ abgebrochen wurde.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: DBT_CONFIGCHANGECANCELED -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624144ccd5a87d983d453c8d6a3c0667376c2a1b9340bba83f229a29882bffe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874540"
---
# <a name="dbt_configchangecanceled-event"></a>DBT \_ CONFIGCHANGECANCELED-Ereignis

Das System überträgt das DBT-Geräteereignis CONFIGCHANGECANCELED, wenn eine Anforderung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) \_ abgebrochen wurde.

Um dieses Geräteereignis zu übertragen, verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) bei der *wParam* auf DBT \_ CONFIGCHANGECANCELED und *lParam* auf 0 (null) festgelegt ist.


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

Legen Sie auf DBT \_ CONFIGCHANGECANCELED fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Auf NULL festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück.**

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

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




