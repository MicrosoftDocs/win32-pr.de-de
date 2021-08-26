---
description: Das DBT \_ USERDEFINED-Geräteereignis identifiziert ein benutzerdefiniertes Ereignis.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: DBT_USERDEFINED -Ereignis (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49eca726ea9c4336a36f30872ad068e45062a67189192154374d5d5b21e578ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103870"
---
# <a name="dbt_userdefined-event"></a>DBT \_ USERDEFINED-Ereignis

Das DBT \_ USERDEFINED-Geräteereignis identifiziert ein benutzerdefiniertes Ereignis.

Um dieses Geräteereignis zu übertragen, rufen Sie die [**BroadcastSystemMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) mit der [**WM \_ DEVICECHANGE-Nachricht**](wm-devicechange.md) auf. Legen Sie *wParam* auf DBT \_ USERDEFINED und *lParam* wie folgt fest.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
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

Legen Sie diese Einstellung auf DBT \_ USERDEFINED fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**\_ DEV BROADCAST \_ \_ USERDEFINED-Struktur,**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) die die benutzerdefinierte Broadcast in Bearbeitung beschreibt. Das **dbud \_ szName-Element** enthält den Namen der benutzerdefinierten Nachricht gefolgt von allen benutzerdefinierten Daten.

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

[**\_DEV \_ BROADCAST \_ USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

