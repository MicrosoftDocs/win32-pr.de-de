---
description: Das System sendet das DBT \_ CUSTOMEVENT-Geräteereignis, wenn ein treiberdefiniertes benutzerdefiniertes Ereignis aufgetreten ist.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: DBT_CUSTOMEVENT -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75ec02262e4cf49a7b929f738acce94822aaf67a397a37d6237f4faa57ef7f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109040"
---
# <a name="dbt_customevent-event"></a>DBT \_ CUSTOMEVENT-Ereignis

Das System sendet das DBT \_ CUSTOMEVENT-Geräteereignis, wenn ein treiberdefiniertes benutzerdefiniertes Ereignis aufgetreten ist.

Zum Übertragen dieses Geräteereignisses verwendet das System die [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) wobei *wParam* wie folgt auf DBT \_ CUSTOMEVENT und *lParam* festgelegt ist.


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

Legen Sie auf DBT \_ CUSTOMEVENT fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Struktur, die das Gerät identifiziert. Die Struktur besteht aus einem ereignisunabhängigen Header, gefolgt von ereignisabhängigen Membern, die das Gerät beschreiben. Um diese Struktur zu verwenden, behandeln Sie die Struktur als [**DEV \_ BROADCAST \_ HDR-Struktur,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) und überprüfen Sie dann den **\_ dbch-Gerätetypmember,** um den Gerätetyp zu bestimmen.

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

[Geräteverwaltung Ereignisse](device-management-events.md)
</dt> <dt>

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




