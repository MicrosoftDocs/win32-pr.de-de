---
description: Das System sendet das DBT \_ CustomEvent-Geräte Ereignis, wenn ein Treiber definiertes benutzerdefiniertes Ereignis aufgetreten ist.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: DBT_CUSTOMEVENT-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777049a0a94b16450ed9ee8567f3fc6506e47174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748361"
---
# <a name="dbt_customevent-event"></a>DBT \_ CustomEvent-Ereignis

Das System sendet das DBT \_ CustomEvent-Geräte Ereignis, wenn ein Treiber definiertes benutzerdefiniertes Ereignis aufgetreten ist.

Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ CustomEvent und *LPARAM* festgelegt ist, wie im folgenden beschrieben.


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

Legen Sie auf DBT \_ CustomEvent fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die das Gerät identifiziert. Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.

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

[**Entwickler- \_ Broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM- \_ devicechange**](wm-devicechange.md)
</dt> </dl>

 

 




