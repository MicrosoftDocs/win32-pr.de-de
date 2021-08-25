---
description: Eine Anwendung sendet die WM \_ MDIDESTROY-Nachricht an ein MDI-Clientfenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu schließen.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: WM_MDIDESTROY (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232514831defe3c65cdce66a5e1c7348ad4f80508eb01615572b7aa5b7d8e9c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772060"
---
# <a name="wm_mdidestroy-message"></a>WM \_ MDIDESTROY-Nachricht

Eine Anwendung sendet die **WM \_ MDIDESTROY-Nachricht** an ein MDI-Clientfenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu schließen.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das zu schließende untergeordnete MDI-Fenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **0 (null)**

Diese Meldung gibt immer 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung entfernt den Titel des untergeordneten MDI-Fensters aus dem MDI-Rahmenfenster und deaktiviert das untergeordnete Fenster. Eine Anwendung sollte diese Meldung verwenden, um alle untergeordneten MDI-Fenster zu schließen.

Wenn ein MDI-Clientfenster eine Meldung empfängt, die die Aktivierung seiner untergeordneten Fenster ändert und das aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder auf und maximiert das neu aktivierte untergeordnete Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ MDICREATE**](wm-mdicreate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mehrere Dokumentschnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




