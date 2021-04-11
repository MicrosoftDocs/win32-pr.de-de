---
description: Das Ereignis des benutzerdefinierten DBT- \_ Geräts identifiziert ein benutzerdefiniertes Ereignis.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: DBT_USERDEFINED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041431"
---
# <a name="dbt_userdefined-event"></a>DBT \_ UserDefined-Ereignis

Das Ereignis des benutzerdefinierten DBT- \_ Geräts identifiziert ein benutzerdefiniertes Ereignis.

Um dieses Geräte Ereignis zu übertragen, müssen Sie die Funktion [**broadcastsystemmessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) mit der [**WM \_ devicechange**](wm-devicechange.md) -Nachricht abrufen. Legen Sie *wParam* auf DBT \_ UserDefined fest, und legen Sie *LPARAM* wie im folgenden beschrieben fest.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
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

Legen Sie auf DBT \_ UserDefined fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**\_ \_ \_ benutzerdefinierte dev Broadcast**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) -Struktur, die die in Bearbeitung befindliche benutzerdefinierte Übertragung beschreibt. Der Member **dbud \_ szName** enthält den Namen der benutzerdefinierten Meldung, gefolgt von benutzerdefinierten Daten.

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

[**\_\_ \_ benutzerdefinierter Entwickler-Broadcast**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**WM- \_ devicechange**](wm-devicechange.md)
</dt> <dt>

[**Broadcastsystemmessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

