---
description: Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge im Ergebnis eines Aufrufes der Funktion SetWindowPos oder einer anderen Fenster Verwaltungsfunktion geändert wird.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: WM_WINDOWPOSCHANGING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758461"
---
# <a name="wm_windowposchanging-message"></a>WM- \_ windowposchanging-Meldung

Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge im Ergebnis eines Aufrufes der Funktion [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) oder einer anderen Fenster Verwaltungsfunktion geändert wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) -Struktur, die Informationen über die neue Größe und Position des Fensters enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Bei einem Fenster mit dem [**\_ über**](window-styles.md) Lapp enden oder dem **WS- \_ dicken Frame** -Stil sendet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die [**WM \_ getminmaxinfo**](wm-getminmaxinfo.md) -Meldung an das Fenster. Dies geschieht, um die neue Größe und Position des Fensters zu überprüfen und die Client Stile [CS \_ bytealignclient](about-window-classes.md) und CS \_ bytealignwindow zu erzwingen. Wenn die WM- **\_ windowposchanging** -Nachricht nicht an die **defwindowproc** -Funktion übergeben wird, kann eine Anwendung diese Standardeinstellungen überschreiben.

Während diese Nachricht verarbeitet wird, wirkt sich das Ändern aller Werte in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) auf die neue Größe, Position oder Position des Fensters in der Z-Reihenfolge aus. Eine Anwendung kann Änderungen am Fenster verhindern, indem die entsprechenden Bits im **Flags** -Member von **Windows POS** festgelegt oder gelöscht werden.

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

[**Enddeferwindowpos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ getminmaxinfo**](wm-getminmaxinfo.md)
</dt> <dt>

[**WM \_ verschieben**](wm-move.md)
</dt> <dt>

[**WM- \_ Größe**](wm-size.md)
</dt> <dt>

[**WM-Windows-Server \_**](wm-windowposchanged.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
