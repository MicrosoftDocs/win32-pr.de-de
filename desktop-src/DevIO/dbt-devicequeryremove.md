---
description: Das System überträgt das DBT DEVICEQUERYREMOVE-Geräteereignis, um die Berechtigung zum Entfernen eines Geräts \_ oder Medienstücks an fordern.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: DBT_DEVICEQUERYREMOVE -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec71d1e66675c8d26d02cc694e9f8243345a2c995a78166ff6a970b67e7558c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004655"
---
# <a name="dbt_devicequeryremove-event"></a>DBT \_ DEVICEQUERYREMOVE-Ereignis

Das System überträgt das DBT DEVICEQUERYREMOVE-Geräteereignis, um die Berechtigung zum Entfernen eines Geräts \_ oder Medienstücks an fordern. Diese Meldung ist die letzte Möglichkeit für Anwendungen und Treiber, sich auf diese Entfernung vorzubereiten. Allerdings kann jede Anwendung diese Anforderung verweigern und den Vorgang abbrechen.

Um dieses Geräteereignis zu übertragen, verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) bei der *wParam* wie im Folgenden beschrieben auf DBT \_ DEVICEQUERYREMOVE und *lParam* festgelegt ist.


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

Legen Sie auf DBT \_ DEVICEQUERYREMOVE fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Struktur, die das zu entfernende Gerät identifiziert. Die Struktur besteht aus einem ereignisunabhängigen Header, gefolgt von ereignisabhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die -Struktur als [**DEV \_ \_ BROADCAST-HDR-Struktur,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) und überprüfen Sie dann den **dbch \_ devicetype-Member,** um den Gerätetyp zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie **TRUE zurück,** um die Berechtigung zum Entfernen eines Geräts zu erteilen.

Geben Sie BROADCAST \_ QUERY \_ DENY zurück, um die Berechtigung zum Entfernen eines Geräts zu verweigern.

## <a name="remarks"></a>Hinweise

Sie müssen alle Handles für das Gerät schließen, da die Entfernung des Geräts fehlschlägt.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Verarbeiten einer Anforderung zum Entfernen eines Geräts.](processing-a-request-to-remove-a-device.md)

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

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




