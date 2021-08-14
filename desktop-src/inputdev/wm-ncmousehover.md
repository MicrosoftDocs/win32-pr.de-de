---
title: WM_NCMOUSEHOVER (Winuser.h)
description: Wird in ein Fenster geschrieben, wenn der Cursor für den Zeitraum, der in einem vorherigen Aufruf von TrackMouseEvent angegeben wurde, über den Nicht-Clientbereich des Fensters bewegt wird.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- WM_NCMOUSEHOVER der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323464d32a2529475823003e51d5bbf0b15c616e32edb0622efe5be7f94dfb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611460"
---
# <a name="wm_ncmousehover-message"></a>WM \_ NCMOUSEHOVER-Meldung

Wird in einem Fenster angezeigt, wenn der Cursor für den Zeitraum, der in einem vorherigen Aufruf von [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegeben wurde, über den Nicht-Clientbereich des Fensters bewegt wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Treffertestwert, der von der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) als Ergebnis der Verarbeitung der [**WM \_ NCHITTEST-Nachricht zurückgegeben**](wm-nchittest.md) wird. Eine Liste der Treffertestwerte finden Sie unter **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [](/previous-versions//dd162808(v=vs.85)) POINTS-Struktur, die die x- und y-Koordinaten des Cursors enthält. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Die Nachverfolgung des Hovers wird beendet, wenn diese Meldung generiert wird. Die Anwendung muss [**TrackMouseEvent erneut aufrufen,**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) wenn eine weitere Nachverfolgung des Mauszeigerbewegungsverhaltens erforderlich ist.

Sie können auch die [**GET \_ X \_ LPARAM-**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**GET \_ \_ Y-LPARAM-Makros**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der x- und y-Koordinaten aus *lParam zu extrahieren.*


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten haben, **und LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (einschließlich Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ MOUSEHOVER**](wm-mousehover.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkte**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

