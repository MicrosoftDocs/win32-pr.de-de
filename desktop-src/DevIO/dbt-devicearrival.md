---
description: Das System überträgt das DBT DEVICEARRARRARR-Geräteereignis, wenn ein Gerät oder ein Medienteil eingefügt wurde \_ und verfügbar wird.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: DBT_DEVICEARRIVAL -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 826d0b510ca76b829eb683396c99579c14a512a6773b76a2049ae7963ede54a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088150"
---
# <a name="dbt_devicearrival-event"></a>DBT \_ DEVICEARRARRARR-Ereignis

Das System überträgt das DBT DEVICEARRARRARR-Geräteereignis, wenn ein Gerät oder ein Medienteil eingefügt wurde \_ und verfügbar wird.

Um dieses Geräteereignis zu übertragen, verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) bei der *wParam* wie im Folgenden beschrieben auf DBT \_ DEVICEARRARR und *lParam* festgelegt ist.


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

Legen Sie auf DBT \_ DEVICEARRARRARR fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine -Struktur, die das eingefügte Gerät identifiziert. Die -Struktur besteht aus einem ereignisunabhängigen Header, gefolgt von ereignisabhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die -Struktur als [**DEV \_ \_ BROADCAST-HDR-Struktur,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) und überprüfen Sie dann den **dbch \_ devicetype-Member,** um den Gerätetyp zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück.**

## <a name="remarks"></a>Hinweise

Wenn Medien eingefügt werden, ist der Typ des eintreffenden Geräts ein Volume (das **dbch \_ devicetype-Member** ist DBT DEVTYP VOLUME), und die Änderung wirkt sich auf das Medium \_ aus \_ **(das dbcv-Flags-Member \_** ist DBTF \_ MEDIA).

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Erkennen des Einfügens oder Entfernens von Medien.](detecting-media-insertion-or-removal.md)

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

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




