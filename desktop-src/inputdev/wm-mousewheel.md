---
title: WM_MOUSEWHEEL Nachricht (Winuser.h)
description: Wird an das Fokusfenster gesendet, wenn das Mausrad gedreht wird.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- WM_MOUSEWHEEL Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae3e750a8544c050e735671b7fd2df6980d53b1200e2f67493b46ad7a2e0b017
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888730"
---
# <a name="wm_mousewheel-message"></a>WM \_ MOUSEWHEEL-Meldung

Wird an das Fokusfenster gesendet, wenn das Mausrad gedreht wird. Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt die Nachricht an das übergeordnete Element des Fensters weiter. Es sollte keine interne Weiterleitung der Nachricht erfolgen, da **DefWindowProc** sie in der übergeordneten Kette weiterleitet, bis sie ein Fenster findet, in dem sie verarbeitet wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort in hoher Reihenfolge gibt den Abstand an, in dem das Rad gedreht wird, ausgedrückt in Vielfachen oder Divisionen von **WHEEL \_ DELTA**( 120). Ein positiver Wert gibt an, dass das Rad vom Benutzer weg nach vorn gedreht wurde. ein negativer Wert gibt an, dass das Rad rückwärts in Richtung des Benutzers gedreht wurde.

Das Wort mit niedriger Reihenfolge gibt an, ob verschiedene virtuelle Schlüssel ausgeschaltet sind. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                               | Bedeutung                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROL**</dt> <dt>0x0008</dt> </dl>    | Die STRG-TASTE ist gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Die linke Maustaste ist nach unten geschaltet.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Die mittlere Maustaste ist gedrückt.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Die rechte Maustaste ist nach unten geschaltet.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT**</dt> <dt>0X0004</dt> </dl>          | Die UMSCHALTTASTE ist nicht mehr gedrückt.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1-0x0020**</dt> <dt></dt> </dl> | Die erste X-Schaltfläche ist ausgeschaltet.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Die zweite X-Schaltfläche ist nicht mehr angezeigt.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort mit niedriger Ordnung gibt die x-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.

Das Wort in hoher Reihenfolge gibt die y-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie den folgenden Code, um die Informationen im *wParam-Parameter* abzurufen:


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Verwenden Sie den folgenden Code, um die horizontale und vertikale Position abzurufen:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wie oben erwähnt, befindet sich die x-Koordinate in der unteren Reihenfolge **unter** dem Rückgabewert. Die y-Koordinate befindet sich in der hohen **Kurzreihenfolge** (beide stellen *signierte* Werte dar, da sie negative Werte auf Systemen mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen wird, können Sie das [**MAKEPOINTS-Makro**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) verwenden, um eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) aus dem Rückgabewert abzurufen. Sie können auch das [**MAKRO GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) oder [**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die x- oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten aufweisen, und **LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

Die Raddrehung ist ein Vielfaches von **WHEEL \_ DELTA**, das auf 120 festgelegt ist. Dies ist der Schwellenwert für die durchzuführende Aktion, und eine solche Aktion (z. B. scrollen in einem Schritt) sollte für jedes Delta erfolgen.

Das Delta wurde auf 120 festgelegt, damit Microsoft oder andere Anbieter feiner aufgelöste Laufräder erstellen können (ein frei rotierendes Rad ohne Notches), um mehr Nachrichten pro Drehung zu senden, jedoch mit einem kleineren Wert in jeder Nachricht. Um dieses Feature zu verwenden, können Sie entweder die eingehenden Deltawerte hinzufügen, bis **WHEEL \_ DELTA** erreicht ist (für eine Deltarotation erhalten Sie also die gleiche Antwort), oder als Reaktion auf die häufigeren Nachrichten teilzeilen scrollen. Sie können auch Ihre Scrollgranularität auswählen und Deltas sammeln, bis sie erreicht ist.

Beachten Sie, dass es keine *fwKeys* für **MSH \_ MOUSEWHEEL** gibt. Andernfalls sind die Parameter genau mit denen für **WM \_ MOUSEWHEEL** identisch.

Es liegt an der Anwendung, **MSH \_ MOUSEWHEEL** an eingebettete Objekte oder Steuerelemente weiterzuleiten. Die Anwendung ist erforderlich, um die Nachricht an eine aktive eingebettete OLE-Anwendung zu senden. Es ist optional, dass die Anwendung sie an ein steuerfähiges Steuerelement mit Fokus sendet. Wenn die Anwendung die Nachricht an ein Steuerelement sendet, kann sie den Rückgabewert überprüfen, um festzustellen, ob die Nachricht verarbeitet wurde. Steuerelemente sind erforderlich, um den Wert **TRUE** zurückzugeben, wenn sie die Nachricht verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (windowsx.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**GET \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GET \_ WHEEL \_ DELTA \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_Mausereignis**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Getsystemmetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkte**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**Systemparametersinfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

