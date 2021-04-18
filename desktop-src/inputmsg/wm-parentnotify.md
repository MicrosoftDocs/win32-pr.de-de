---
title: WM_PARENTNOTIFY Meldung
description: Wird an ein Fenster gesendet, wenn eine bedeutende Aktion in einem Nachfolger Fenster auftritt.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_PARENTNOTIFY Nachricht
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518320"
---
# <a name="wm_parentnotify-message"></a>WM_PARENTNOTIFY Meldung

Wird an ein Fenster gesendet, wenn eine bedeutende Aktion in einem Nachfolger Fenster auftritt. Diese Meldung ist nun so erweitert, dass Sie das [**WM_POINTERDOWN**](wm-pointerdown.md) -Ereignis einschließt. Wenn das untergeordnete Fenster erstellt wird, sendet das System [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) direkt vor der Funktion "" [**, die das**](/windows/win32/api/winuser/nf-winuser-createwindowa) Fenster erstellt hat [**, und gibt**](/windows/win32/api/winuser/nf-winuser-createwindowexa) es zurück. Wenn das untergeordnete Fenster zerstört wird, sendet das System die Nachricht, bevor eine Verarbeitung zum Zerstören des Fensters erfolgt.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

> \[! Wichtig\]  
> Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort von *wParam* gibt das Ereignis an, für das das übergeordnete Element benachrichtigt wird. Der Wert des höherwertigen Worts hängt vom Wert des nieder wertigen Worts ab. Dieser Parameter kann einen der folgenden Werte annehmen.



| LoWord (*wParam*)                                                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | Das untergeordnete Fenster wird erstellt.<br/> HIWORD (*wParam*) ist der Bezeichner des untergeordneten Fensters.<br/> *LPARAM* ist ein Handle für das untergeordnete Fenster.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | Das untergeordnete Fenster wird zerstört.<br/> HIWORD (*wParam*) ist der Bezeichner des untergeordneten Fensters.<br/> *LPARAM* ist ein Handle für das untergeordnete Fenster.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat mit der linken Maustaste geklickt.<br/> HIWORD (*wParam*) ist nicht definiert.<br/> *LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat auf die mittlere Maustaste geklickt.<br/> HIWORD (*wParam*) ist nicht definiert.<br/> *LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat mit der rechten Maustaste geklickt.<br/> HIWORD (*wParam*) ist nicht definiert.<br/> *LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020b</dt> </dl> | Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat auf die erste oder zweite X-Schaltfläche geklickt.<br/> HIWORD (*wParam*) gibt an, welche Schaltfläche gedrückt wurde. Dieser Parameter kann einen der folgenden Werte aufweisen: XButton1 oder XButton2.<br/> *LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Ein Zeiger hat eine Verbindung mit dem untergeordneten Fenster hergestellt.<br/> HIWORD (*wParam*) enthält den Bezeichner des Zeigers, der das [**WM_POINTERDOWN**](wm-pointerdown.md) Ereignis generiert hat.<br/>                                                                                                                                                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist. Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.

 

Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anwendung diese Nachricht verarbeitet, gibt Sie 0 (null) zurück.

Wenn die Anwendung diese Nachricht nicht verarbeitet, ruft Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)auf.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird auch an alle übergeordneten Fenster des untergeordneten Fensters gesendet, einschließlich des Fensters der obersten Ebene.

Alle untergeordneten Fenster, mit Ausnahme derjenigen, die den **WS_EX_NOPARENTNOTIFY** erweiterten Fenster Stil aufweisen, senden diese Nachricht an die übergeordneten Fenster. Standardmäßig haben untergeordnete Fenster in einem Dialogfeld den **WS_EX_NOPARENTNOTIFY** Stil, es sei denn, die Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " wird aufgerufen, um das untergeordnete Fenster ohne diesen Stil zu erstellen.

Diese Benachrichtigung bietet den Vorgänger Fenstern des untergeordneten Fensters die Möglichkeit, die Zeiger Informationen zu untersuchen und ggf. den Zeiger mithilfe der Zeiger Erfassungs Funktionen zu erfassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM_CREATE**](../winmsg/wm-create.md)
</dt> <dt>

[**WM_DESTROY**](../winmsg/wm-destroy.md)
</dt> <dt>

[**WM_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[**WM_MBUTTONDOWN**](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[**WM_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[**WM_XBUTTONDOWN**](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

