---
title: WM_MOUSEHOVER (Winuser.h)
description: Wird in einem Fenster angezeigt, wenn der Cursor für den zeitraum, der in einem vorherigen Aufruf von TrackMouseEvent angegeben wurde, über den Clientbereich des Fensters bewegt wird.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- WM_MOUSEHOVER der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a8fb4aef4d363b87b0093316d264dddb212aa11d42e10b6ae97a4a93ee46a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451500"
---
# <a name="wm_mousehover-message"></a>WM \_ MOUSEHOVER-Meldung

Wird in einem Fenster angezeigt, wenn der Cursor für den in einem vorherigen Aufruf von [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegebenen Zeitraum über den Clientbereich des Fensters bewegt wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob verschiedene virtuelle Schlüssel nicht mehr verwendet werden können. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                               | Bedeutung                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROL**</dt> <dt>0x0008</dt> </dl>    | Die STRG-TASTE wird gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON-0x0001**</dt> <dt></dt> </dl>    | Die linke Maustaste ist geschwenkt.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON-0x0010**</dt> <dt></dt> </dl>    | Die mittlere Maustaste wird geschwenkt.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON-0x0002**</dt> <dt></dt> </dl>    | Die rechte Maustaste ist geschwenkt.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT 0X0004**</dt> <dt></dt> </dl>          | Die UMSCHALTTASTE wird gedrückt.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1-0x0020**</dt> <dt></dt> </dl> | Die erste X-Schaltfläche ist nicht mehr zu sehen.<br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2-0x0040**</dt> <dt></dt> </dl> | Die zweite X-Schaltfläche ist nicht mehr zu sehen.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das niedrige Wort gibt die x-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.

Das obere Wort gibt die y-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Die Nachverfolgung des Mauszeigers wird beendet, wenn **WM \_ MOUSEHOVER** generiert wird. Die Anwendung muss [**TrackMouseEvent erneut aufrufen,**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) wenn eine weitere Nachverfolgung des Mauszeigerbewegungsverhaltens erforderlich ist.

Verwenden Sie den folgenden Code, um die horizontale und vertikale Position zu erhalten:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wie bereits erwähnt, liegt die x-Koordinate in der niedrigen Reihenfolge **unter dem** Rückgabewert. Die y-Koordinate befindet sich in  der hohen Kurzen **(beide** stellen werte mit Vorsignieren dar, da sie negative Werte auf Systemen mit mehreren Monitoren verwenden können). Wenn der Rückgabewert einer Variablen zugewiesen wird, können Sie das [**MAKEPOINTS-Makro**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) verwenden, um eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) aus dem Rückgabewert zu erhalten. Sie können auch das [**GET \_ X \_ LPARAM-**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) oder [**GET \_ \_ Y-LPARAM-Makro**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die x- oder y-Koordinate zu extrahieren.

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

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
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

 

