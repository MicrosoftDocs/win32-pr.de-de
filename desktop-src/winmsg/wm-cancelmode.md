---
description: Wird gesendet, um bestimmte Modi abzubrechen, z. b. die Maus Aufzeichnung
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: WM_CANCELMODE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359163"
---
# <a name="wm_cancelmode-message"></a>WM \_ cancelmode-Meldung

Wird gesendet, um bestimmte Modi abzubrechen, z. b. die Maus Aufzeichnung Das System sendet diese Meldung z. b. an das aktive Fenster, wenn ein Dialogfeld oder ein Meldungs Feld angezeigt wird. Bestimmte Funktionen senden diese Nachricht auch explizit an das angegebene Fenster, unabhängig davon, ob es sich um das aktive Fenster handelt. Die [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) -Funktion sendet diese Meldung z. b., wenn das angegebene Fenster deaktiviert wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn die **WM \_ cancelmode** -Meldung gesendet wird, bricht die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die interne Verarbeitung der Standardbild Lauf leisten Eingabe ab, bricht die interne Menü Verarbeitung ab und gibt die Maus Aufzeichnung frei.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**Releasecapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
