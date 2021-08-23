---
description: Das System sendet das DBT DEVICEQUERYREMOVEFAILED-Geräteereignis, wenn eine Anforderung zum Entfernen eines Geräts oder Medienstücks \_ abgebrochen wurde.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: DBT_DEVICEQUERYREMOVEFAILED -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605c2689d7d986b4e85fda6d8ce5f24fa6483641de46a6a84f3e4e96ba473897
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076304"
---
# <a name="dbt_devicequeryremovefailed-event"></a>DBT \_ DEVICEQUERYREMOVEFAILED-Ereignis

Das System sendet das DBT DEVICEQUERYREMOVEFAILED-Geräteereignis, wenn eine Anforderung zum Entfernen eines Geräts oder Medienstücks \_ abgebrochen wurde.

Um dieses Geräteereignis zu übertragen, verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) bei der *wParam* wie im Folgenden beschrieben auf DBT \_ DEVICEQUERYREMOVEFAILED und *lParam* festgelegt ist.


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

Legen Sie auf DBT \_ DEVICEQUERYREMOVEFAILED fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Struktur, die das Gerät identifiziert. Die -Struktur besteht aus einem ereignisunabhängigen Header, gefolgt von ereignisabhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die -Struktur als [**DEV \_ \_ BROADCAST-HDR-Struktur,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) und überprüfen Sie dann den **dbch \_ devicetype-Member,** um den Gerätetyp zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück.**

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Verarbeiten einer Anforderung zum Entfernen eines Geräts.](processing-a-request-to-remove-a-device.md)

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

 

 




