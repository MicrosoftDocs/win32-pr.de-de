---
title: WM_POINTERLEAVE Meldung
description: Wird an ein Fenster gesendet, wenn ein Zeiger den Erkennungsbereich über dem Fenster verlässt (Zeigen) oder wenn ein Zeiger außerhalb der Grenzen des Fensters bewegt wird.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- WM_POINTERLEAVE Der Nachrichteneingabenachrichten und -benachrichtigungen
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
ms.openlocfilehash: 519e354aa43cf31d0a2477aec2f50a1405b7c4a254f2641497229c14f55d4679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964230"
---
# <a name="wm_pointerleave-message"></a>WM_POINTERLEAVE Meldung

Wird an ein Fenster gesendet, wenn ein Zeiger den Erkennungsbereich über dem Fenster verlässt (Zeigen) oder wenn ein Zeiger außerhalb der Grenzen des Fensters bewegt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeigerbezeichner und zusätzliche Informationen. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): der Zeigerbezeichner.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Gibt an, ob diese Nachricht von einem Zeiger generiert wurde, der den Erkennungsbereich nicht verlassen hat. Dieses Flag wird nicht festgelegt, wenn der Zeiger den Erkennungsbereich des Fensters verlässt.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht von einem Zeiger generiert wurde, der kontaktiert. Dieses Flag ist nicht für einen Zeiger im Erkennungsbereich festgelegt (zeigen Sie darauf).

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich herstellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein. Wenn möglich, sollte eine Anwendung anstelle der Punktposition die vollständigen Zeigerbereichsinformationen verwenden.

 

Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): die x-Koordinate (horizontaler Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): die y-Koordinate (vertikaler Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte sie [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufrufen.

## <a name="remarks"></a>Hinweise

Die **WM_POINTERLEAVE** Benachrichtigung kann von einem Fenster verwendet werden, um den Modus zu ändern oder Feedback an den Benutzer zu beenden, während sich der Zeiger über der Fensteroberfläche befindet.

Diese Benachrichtigung wird nur an das Fenster gesendet, das Eingaben für den Zeiger empfängt. In der folgenden Tabelle sind einige Situationen aufgeführt, in denen diese Benachrichtigung gesendet wird.



| Aktion                                        | Festlegen von Flags                                                         | An gesendete Benachrichtigungen                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| Ein zeigender Zeiger überschreitet Fenstergrenzen. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | Fenster außerhalb des Fensters, dessen Begrenzung der Zeiger verschoben hat.  |
| Ein Zeiger liegt außerhalb des Erkennungsbereichs.        | Nicht zutreffend                                                               | Fenster, für das der Zeiger den Erkennungsbereich verlässt. |



 

> \[! Wichtig\]  
> Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, empfängt es in der Regel keine weiteren Benachrichtigungen. Aus diesem Grund ist es wichtig, dass Sie keine Annahmen basierend auf gleichmäßig gekoppelten [**WM_POINTERDOWN**](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md) oder [**WM_POINTERENTER**](wm-pointerenter.md) / **WM_POINTERLEAVE-Benachrichtigungen** treffen.

 

Wenn der Kontakt mit dem Eingabedigitalisierer beibehalten wird und sich der Zeiger außerhalb des Fensters bewegt, **wird WM_POINTERLEAVE** nicht generiert. **WM_POINTERLEAVE** wird nur generiert, wenn ein zeigerender Zeiger Fenstergrenzen überschreitet oder der Kontakt beendet wird.

**WM_POINTERLEAVE** wird an die Warteschlange für gesendete Nachrichten gesendet, wenn die Eingabe von einem Mausgerät stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

**Referenz**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

