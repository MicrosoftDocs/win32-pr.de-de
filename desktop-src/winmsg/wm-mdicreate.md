---
description: Eine Anwendung sendet die WM \_ MDICREATE-Nachricht an ein MDI-Clientfenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu erstellen.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: WM_MDICREATE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69a894ebd2e55bb74486e26cd118366b1e533a490cc50feb5f77aad64c6be3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056010"
---
# <a name="wm_mdicreate-message"></a>WM \_ MDICREATE-Nachricht

Eine Anwendung sendet die **WM \_ MDICREATE-Nachricht** an ein MDI-Clientfenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu erstellen.


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**MDICREATESTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) mit Informationen, die das System zum Erstellen des untergeordneten MDI-Fensters verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HWND**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert das Handle für das neue untergeordnete Fenster.

Wenn die Meldung fehlschlägt, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Das untergeordnete MDI-Fenster [](window-styles.md) wird mit den Fensterformatbits **WS \_ CHILD,** **WS \_ CLIPSIBLINGS,** **WS \_ CLIPCHILDREN,** **WS \_ SYSMENU,** **WS \_ CAPTION**, **WS \_ THICKFRAME,** **WS \_ MINIMIZEBOX** und **WS \_ MAXIMIZEBOX** sowie zusätzlichen Stilbits erstellt, die in der [**MDICREATESTRUCT-Struktur angegeben**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) sind. Das System fügt dem Fenstermenü des Rahmenfensters den Titel des neuen untergeordneten Fensters hinzu. Eine Anwendung sollte diese Meldung verwenden, um alle untergeordneten Fenster des Clientfensters zu erstellen.

Wenn ein MDI-Clientfenster eine Meldung empfängt, die die Aktivierung seiner untergeordneten Fenster ändert, während das aktive untergeordnete Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder auf und maximiert das neu aktivierte untergeordnete Fenster.

Wenn ein untergeordnetes MDI-Fenster erstellt wird, sendet das System die [**WM \_ CREATE-Nachricht**](wm-create.md) an das Fenster. Der *lParam-Parameter* der **WM \_ CREATE-Nachricht** enthält einen Zeiger auf eine [**CREATESTRUCT-Struktur.**](/windows/win32/api/winuser/ns-winuser-createstructa) Das *lpCreateParams-Member* dieser -Struktur enthält einen Zeiger auf die [**MDICREATESTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) die mit der **WM \_ MDICREATE-Nachricht** übergeben wurde, die das untergeordnete MDI-Fenster erstellt hat.

Eine Anwendung sollte keine zweite **\_ WM MDICREATE-Nachricht** senden, während eine **WM \_ MDICREATE-Nachricht** noch verarbeitet wird. Beispielsweise sollte keine WM **\_ MDICREATE-Nachricht** gesendet werden, während ein untergeordnetes MDI-Fenster seine **WM \_ MDICREATE-Nachricht** verarbeitet.

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

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**WM \_ CREATE**](wm-create.md)
</dt> <dt>

[**WM \_ MDIDESTROY**](wm-mdidestroy.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mehrere Dokumentschnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 
