---
description: Das System überträgt das DBT \_ deviceremovepend-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums entfernt wird und nicht mehr zur Verwendung verfügbar ist.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: DBT_DEVICEREMOVEPENDING-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126793"
---
# <a name="dbt_deviceremovepending-event"></a>DBT \_ deviceremovepending-Ereignis

Das System überträgt das DBT \_ deviceremovepend-Geräte Ereignis, wenn ein Gerät oder ein Teil des Mediums entfernt wird und nicht mehr zur Verwendung verfügbar ist.

Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ deviceremovepending und *LPARAM* festgelegt ist, wie im folgenden beschrieben.


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

Legen Sie auf DBT \_ deviceremovepending fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die das Gerät identifiziert. Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="remarks"></a>Bemerkungen

Das System sendet möglicherweise eine DBT \_ deviceremovepend-Nachricht, ohne eine entsprechende [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -Nachricht zu senden. In solchen Fällen müssen die Anwendungen und Treiber nach dem Verlust des Geräts so optimal wie möglich wieder hergestellt werden.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Verarbeiten einer Anforderung zum Entfernen eines Geräts](processing-a-request-to-remove-a-device.md).

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

 

 




