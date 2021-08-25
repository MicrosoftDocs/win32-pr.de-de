---
title: WM_PARENTNOTIFY Nachricht
description: Wird an ein Fenster gesendet, wenn eine wichtige Aktion in einem Nachfolgerfenster auftritt.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- 'WM_PARENTNOTIFY-Nachricht: Eingabemeldungen und Benachrichtigungen'
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
ms.openlocfilehash: 5de0845f906e72a42fa8d9a290c6cd8ac16cc0e96cae21ac25b3e9d7810309e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829570"
---
# <a name="wm_parentnotify-message"></a>WM_PARENTNOTIFY Nachricht

Wird an ein Fenster gesendet, wenn eine wichtige Aktion in einem Nachfolgerfenster auftritt. Diese Meldung wurde nun erweitert, um das [**WM_POINTERDOWN**](wm-pointerdown.md) ein. Wenn das untergeordnete Fenster erstellt wird, sendet das System WM_PARENTNOTIFY direkt vor der [**Funktion CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) die das Fenster erstellt. Wenn das untergeordnete Fenster zerstört wird, sendet das System die Nachricht, bevor eine Verarbeitung zum Zerstören des Fensters stattfindet.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das niedrige Wort *von wParam* gibt das Ereignis an, für das das übergeordnete Element benachrichtigt wird. Der Wert des hohen Worts hängt vom Wert des niedrigen Worts ab. Dieser Parameter kann einen der folgenden Werte annehmen.



| LOWORD(*wParam*)                                                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | Das untergeordnete Fenster wird erstellt.<br/> HIWORD(*wParam*) ist der Bezeichner des untergeordneten Fensters.<br/> *lParam* ist ein Handle für das untergeordnete Fenster.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | Das untergeordnete Fenster wird zerstört.<br/> HIWORD(*wParam*) ist der Bezeichner des untergeordneten Fensters.<br/> *lParam* ist ein Handle für das untergeordnete Fenster.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | Der Benutzer hat den Cursor über dem untergeordneten Fenster platziert und auf die linke Maustaste geklickt.<br/> HIWORD(*wParam*) ist nicht definiert.<br/> *lParam* ist die x-Koordinate des Cursors ist das Wort in niedriger Reihenfolge, und die y-Koordinate des Cursors ist das hochgeordnete Wort.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | Der Benutzer hat den Cursor über dem untergeordneten Fenster platziert und auf die mittlere Maustaste geklickt.<br/> HIWORD(*wParam*) ist nicht definiert.<br/> *lParam* ist die x-Koordinate des Cursors ist das Wort in niedriger Reihenfolge, und die y-Koordinate des Cursors ist das hochgeordnete Wort.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | Der Benutzer hat den Cursor über dem untergeordneten Fenster platziert und mit der rechten Maustaste geklickt.<br/> HIWORD(*wParam*) ist nicht definiert.<br/> *lParam* ist die x-Koordinate des Cursors ist das Wort in niedriger Reihenfolge, und die y-Koordinate des Cursors ist das hochgeordnete Wort.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | Der Benutzer hat den Cursor über dem untergeordneten Fenster platziert und auf die erste oder zweite X-Schaltfläche geklickt.<br/> HIWORD(*wParam*) gibt an, welche Schaltfläche gedrückt wurde. Dieser Parameter kann einer der folgenden Werte sein: XBUTTON1 oder XBUTTON2.<br/> *lParam* ist die x-Koordinate des Cursors ist das Wort in niedriger Reihenfolge, und die y-Koordinate des Cursors ist das hochgeordnete Wort.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Ein Zeiger hat kontakt mit dem untergeordneten Fenster hergestellt.<br/> HIWORD(*wParam*) enthält den Bezeichner des Zeigers, der das WM_POINTERDOWN [**generiert**](wm-pointerdown.md) hat.<br/>                                                                                                                                                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich stellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein. Wenn möglich, sollte eine Anwendung die vollständigen Zeigerbereichsinformationen anstelle der Punktposition verwenden.

 

Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): Die x-Koordinate (horizontaler Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): die y-Koordinate (vertikaler Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anwendung diese Nachricht verarbeitet, gibt sie 0 (null) zurück.

Wenn die Anwendung diese Nachricht nicht verarbeiten kann, ruft sie [**DefWindowProc auf.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Hinweise

Diese Meldung wird auch an alle Vorgängerfenster des untergeordneten Fensters gesendet, einschließlich des Fensters der obersten Ebene.

Alle untergeordneten Fenster, mit  Ausnahme derer, die über WS_EX_NOPARENTNOTIFY erweiterten Fensterstil verfügen, senden diese Meldung an die übergeordneten Fenster. Standardmäßig haben untergeordnete Fenster in einem  Dialogfeld das formatierte WS_EX_NOPARENTNOTIFY, es sei denn, die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) wird aufgerufen, um das untergeordnete Fenster ohne diesen Stil zu erstellen.

Diese Benachrichtigung bietet den Vorgängerfenstern des untergeordneten Fensters die Möglichkeit, die Zeigerinformationen zu untersuchen und den Zeiger bei Bedarf mithilfe der Zeigererfassungsfunktionen zu erfassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Createwindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Wm_create**](../winmsg/wm-create.md)
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

 

