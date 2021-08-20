---
description: Das System überträgt das DBT \_ DEVICEREMOVECOMPLETE-Geräteereignis, wenn ein Gerät oder ein Medienelement physisch entfernt wurde.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: DBT_DEVICEREMOVECOMPLETE -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5998742d823d710bfb91cd10579a3fb1ec65bec42b615fc7fdac3ac35545b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539190"
---
# <a name="dbt_deviceremovecomplete-event"></a>DBT \_ DEVICEREMOVECOMPLETE-Ereignis

Das System überträgt das DBT \_ DEVICEREMOVECOMPLETE-Geräteereignis, wenn ein Gerät oder ein Medienelement physisch entfernt wurde.

Zum Übertragen dieses Geräteereignisses verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) wobei *wParam* wie folgt auf DBT \_ DEVICEREMOVECOMPLETE und *lParam* festgelegt ist.


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

Auf DBT \_ DEVICEREMOVECOMPLETE festlegen

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Struktur, die das entfernte Gerät identifiziert. Die Struktur besteht aus einem ereignisunabhängigen Header, gefolgt von ereignisabhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die Struktur als [**DEV \_ BROADCAST \_ HDR-Struktur,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) und überprüfen Sie dann den **\_ dbch-Gerätetypmember,** um den Gerätetyp zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück.

## <a name="remarks"></a>Hinweise

Das System kann eine DBT \_ DEVICEREMOVECOMPLETE-Nachricht senden, ohne entsprechende [DBT \_ DEVICEQUERYREMOVE-](dbt-devicequeryremove.md) und [DBT \_ DEVICEREMOVEPENDING-Nachrichten](dbt-deviceremovepending.md) zu senden. In solchen Fällen müssen die Anwendungen und Treiber nach möglichkeit nach dem Verlust des Geräts wiederhergestellt werden.

Wenn Medien entfernt werden, ist der Typ des eingehenden Geräts ein Volume (der **\_ dbch-Gerätetypmember** ist DBT \_ DEVTYP \_ VOLUME), und die Änderung wirkt sich auf das Medium aus (der **dbcv \_ flags-Member** ist DBTF \_ MEDIA).

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Detecting Media Insertion or Removal or](detecting-media-insertion-or-removal.md) Processing a Request to Remove a [Device](processing-a-request-to-remove-a-device.md).

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

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




