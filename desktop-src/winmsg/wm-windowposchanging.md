---
description: Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge sich als Ergebnis eines Aufrufs der SetWindowPos-Funktion oder einer anderen Fensterverwaltungsfunktion ändern wird.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: WM_WINDOWPOSCHANGING (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f10abcb0692374209c2070a465df7c4a5f18672eebf376378d6fb16cbca537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771940"
---
# <a name="wm_windowposchanging-message"></a>WM \_ WINDOWPOSCHANGING-Meldung

Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge sich als Ergebnis eines Aufrufs der [**SetWindowPos-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowpos) oder einer anderen Fensterverwaltungsfunktion ändern wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Ein Zeiger auf eine [**WINDOWPOS-Struktur,**](/windows/win32/api/winuser/ns-winuser-windowpos) die Informationen über die neue Größe und Position des Fensters enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Für ein Fenster mit [**dem Format WS \_ OVERLAPPED**](window-styles.md) oder **WS \_ THICKFRAME** sendet die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die [**WM \_ GETMINMAXINFO-Nachricht**](wm-getminmaxinfo.md) an das Fenster. Dies erfolgt, um die neue Größe und Position des Fensters zu überprüfen und die [Clientstile CS \_ BYTEALIGNCLIENT](about-window-classes.md) und CS \_ BYTEALIGNWINDOW zu erzwingen. Wenn die **WM \_ WINDOWPOSCHANGING-Nachricht** nicht an die **DefWindowProc-Funktion** übergeben wird, kann eine Anwendung diese Standardwerte überschreiben.

Während diese Nachricht verarbeitet wird, wirkt sich das Ändern eines der Werte in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) auf die neue Größe, Position oder Position des Fensters in der Z-Reihenfolge aus. Eine Anwendung kann Änderungen am Fenster verhindern, indem sie die entsprechenden Bits im **Flags-Member** von **WINDOWPOS festlegen oder löschen.**

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md)
</dt> <dt>

[**WM \_ MOVE**](wm-move.md)
</dt> <dt>

[**WM \_ SIZE**](wm-size.md)
</dt> <dt>

[**\_WM-FENSTERPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
