---
description: Das System überträgt das DBT \_ devicequeryremovefailed-Geräte Ereignis, wenn eine Anforderung zum Entfernen eines Geräts oder eines Mediums abgebrochen wurde.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: DBT_DEVICEQUERYREMOVEFAILED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861111"
---
# <a name="dbt_devicequeryremovefailed-event"></a>DBT \_ devicequeryremovefailed-Ereignis

Das System überträgt das DBT \_ devicequeryremovefailed-Geräte Ereignis, wenn eine Anforderung zum Entfernen eines Geräts oder eines Mediums abgebrochen wurde.

Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ devicequeryremovefailed und *LPARAM* festgelegt ist, wie im folgenden beschrieben.


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

Auf DBT \_ devicequeryremovefailed festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die das Gerät identifiziert. Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

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

 

 




