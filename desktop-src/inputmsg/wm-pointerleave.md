---
title: WM_POINTERLEAVE Meldung
description: Wird an ein Fenster gesendet, wenn ein Zeiger den Erkennungsbereich über dem Fenster verlässt (Hover) oder wenn ein Zeiger außerhalb der Fenstergrenzen bewegt wird.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERLEAVE Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2ee58fd74f266d067f6211e156d984a3b3d1c477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340352"
---
# <a name="wm_pointerleave-message"></a>WM_POINTERLEAVE Meldung

Wird an ein Fenster gesendet, wenn ein Zeiger den Erkennungsbereich über dem Fenster verlässt (Hover) oder wenn ein Zeiger außerhalb der Fenstergrenzen bewegt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

> \[! Wichtig\]  
> Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeiger Bezeichner und zusätzliche Informationen. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): der Zeiger Bezeichner.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): gibt an, ob diese Nachricht von einem Zeiger generiert wurde, der nicht den Erkennungsbereich verlassen hat. Dieses Flag wird nicht festgelegt, wenn der Zeiger den Erkennungsbereich des Fensters verlässt.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob diese Nachricht von einem Zeiger generiert wurde, der sich im Kontakt befindet. Dieses Flag ist für einen Zeiger im Erkennungsbereich (Hover) nicht festgelegt.

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

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.

## <a name="remarks"></a>Bemerkungen

Die **WM_POINTERLEAVE** Benachrichtigung kann von einem Fenster verwendet werden, um den Modus zu ändern oder Feedback an den Benutzer zu senden, während sich der Mauszeiger über der Fenster Oberfläche befindet.

Diese Benachrichtigung wird nur an das Fenster gesendet, das Eingaben für den Zeiger empfängt. In der folgenden Tabelle sind einige Situationen aufgeführt, in denen diese Benachrichtigung gesendet wird.



| Aktion                                        | Flags festgelegt                                                         | Gesendete Benachrichtigungen an                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| Ein Mauszeiger überschreitet Fenstergrenzen. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | Fenster außerhalb von, dessen Grenze der Zeiger verschoben wurde.  |
| Ein Zeiger geht aus dem Erkennungsbereich.        | –                                                               | Das Fenster, für das der Zeiger den Erkennungsbereich verlässt. |



 

> \[! Wichtig\]  
> Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, werden normalerweise keine weiteren Benachrichtigungen empfangen. Aus diesem Grund ist es wichtig, dass Sie keine Annahmen auf der Grundlage von gleichmäßig gekoppelten [**WM_POINTERDOWN**](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md) oder [**WM_POINTERENTER**](wm-pointerenter.md) / **WM_POINTERLEAVE** Benachrichtigungen treffen.

 

Wenn Contact mit dem eingabedigitalisierer verwaltet wird und der Zeiger außerhalb des Fensters bewegt wird, wird **WM_POINTERLEAVE** nicht generiert. **WM_POINTERLEAVE** wird nur generiert, wenn ein Mauszeiger den Fenstergrenzen überschreitet oder der Kontakt beendet wird.

**WM_POINTERLEAVE** wird in der Nachrichten Warteschlange gepostet, wenn die Eingabe von einem Mausgerät stammt.

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

**Verweis**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

