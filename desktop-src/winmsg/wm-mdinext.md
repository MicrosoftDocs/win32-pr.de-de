---
description: Eine Anwendung sendet die WM- \_ mdinext-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das nächste oder vorherige untergeordnete Fenster zu aktivieren.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: WM_MDINEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751208"
---
# <a name="wm_mdinext-message"></a>WM- \_ mdinext-Nachricht

Eine Anwendung sendet die **WM- \_ mdinext** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das nächste oder vorherige untergeordnete Fenster zu aktivieren.


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster. Das System aktiviert das untergeordnete Fenster direkt vor oder nach dem angegebenen untergeordneten Fenster, abhängig vom Wert des *LPARAM* -Parameters. Wenn der *wParam* -Parameter **null** ist, aktiviert das System das untergeordnete Fenster, das unmittelbar vor oder nach dem momentan aktiven untergeordneten Fenster liegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn dieser Parameter NULL ist, aktiviert das System das nächste untergeordnete MDI-Fenster und platziert das untergeordnete Fenster, das durch den *wParam* -Parameter identifiziert wird, hinter allen anderen untergeordneten Fenstern. Wenn dieser Parameter ungleich NULL ist, aktiviert das System das vorherige untergeordnete Fenster und platziert es vor dem durch *wParam* identifizierten untergeordneten Fenster.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **null**

Der Rückgabewert ist immer 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn ein MDI-Client Fenster eine Nachricht empfängt, die die Aktivierung der untergeordneten Fenster ändert, während das aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM- \_ mdiaktivierung**](wm-mdiactivate.md)
</dt> <dt>

[**WM- \_ mdigetactive**](wm-mdigetactive.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




