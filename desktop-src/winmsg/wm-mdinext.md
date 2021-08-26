---
description: Eine Anwendung sendet die WM \_ MDINEXT-Nachricht an ein MDI-Clientfenster (Multiple Document Interface), um das nächste oder vorherige untergeordnete Fenster zu aktivieren.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: WM_MDINEXT (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa2b88e5368db2a6b700e0b4d469d1ba680d3caa4d2c1e1c208c5143660396f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931240"
---
# <a name="wm_mdinext-message"></a>WM \_ MDINEXT-Nachricht

Eine Anwendung sendet die **WM \_ MDINEXT-Nachricht** an ein MDI-Clientfenster (Multiple Document Interface), um das nächste oder vorherige untergeordnete Fenster zu aktivieren.


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster. Das System aktiviert das untergeordnete Fenster, das sich direkt vor oder nach dem angegebenen untergeordneten Fenster befindet, abhängig vom Wert des *lParam-Parameters.* Wenn der *wParam-Parameter* **NULL ist,** aktiviert das System das untergeordnete Fenster unmittelbar vor oder nach dem derzeit aktiven untergeordneten Fenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn dieser Parameter 0 (null) ist, aktiviert das System das nächste untergeordnete MDI-Fenster und platziert das untergeordnete Fenster, das durch den *wParam-Parameter* identifiziert wird, hinter allen anderen untergeordneten Fenstern. Wenn dieser Parameter ungleich 0 (null) ist, aktiviert das System das vorherige untergeordnete Fenster und platziert es vor dem untergeordneten Fenster, das von *wParam identifiziert wird.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **0 (null)**

Der Rückgabewert ist immer 0 (null).

## <a name="remarks"></a>Hinweise

Wenn ein MDI-Clientfenster eine Meldung empfängt, die die Aktivierung seiner untergeordneten Fenster ändert, während das aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder auf und maximiert das neu aktivierte untergeordnete Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ MDIACTIVATE**](wm-mdiactivate.md)
</dt> <dt>

[**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mehrere Dokumentschnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




