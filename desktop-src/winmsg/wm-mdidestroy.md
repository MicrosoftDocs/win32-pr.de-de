---
description: Eine Anwendung sendet die WM- \_ mdidestroy-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu schließen.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: WM_MDIDESTROY Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751209"
---
# <a name="wm_mdidestroy-message"></a>WM- \_ mdidestroy-Meldung

Eine Anwendung sendet die **WM- \_ mdidestroy** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu schließen.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das geschlossen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **null**

Diese Meldung gibt immer 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung entfernt den Titel des untergeordneten MDI-Fensters aus dem MDI-Rahmen Fenster und deaktiviert das untergeordnete Fenster. Eine Anwendung sollte diese Nachricht verwenden, um alle untergeordneten MDI-Fenster zu schließen.

Wenn ein MDI-Client Fenster eine Meldung empfängt, mit der die Aktivierung der untergeordneten Fenster geändert wird, und das aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.

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

[**WM- \_ mdicreate**](wm-mdicreate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




