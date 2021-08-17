---
title: WM_MOUSEHWHEEL-Nachricht (Winuser.h)
description: Wird an das aktive Fenster gesendet, wenn das horizontale Scrollrad der Maus geneigt oder gedreht wird.
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- WM_MOUSEHWHEEL Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de63d214d087cb804c3973fbba6a90c46955506ebddf5da57a7578d224edb803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451490"
---
# <a name="wm_mousehwheel-message"></a>WM \_ MOUSEHWHEEL-Nachricht

Wird an das aktive Fenster gesendet, wenn das horizontale Scrollrad der Maus geneigt oder gedreht wird. Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt die Nachricht an das übergeordnete Element des Fensters weiter. Es sollte keine interne Weiterleitung der Nachricht erfolgen, da **DefWindowProc** sie in der übergeordneten Kette weiterleitet, bis sie ein Fenster findet, in dem sie verarbeitet wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort in hoher Reihenfolge gibt den Abstand an, in dem das Rad gedreht wird, ausgedrückt in Vielfachen oder Faktoren von **WHEEL \_ DELTA**, die auf 120 festgelegt ist. Ein positiver Wert gibt an, dass das Rad nach rechts gedreht wurde. ein negativer Wert gibt an, dass das Rad nach links gedreht wurde.

Das Wort mit niedriger Reihenfolge gibt an, ob verschiedene virtuelle Schlüssel ausgeschaltet sind. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                               | Bedeutung                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROL**</dt> <dt>0x0008</dt> </dl>    | Die STRG-TASTE ist gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Die linke Maustaste ist nach unten geschaltet.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Die mittlere Maustaste ist gedrückt.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Die rechte Maustaste ist nach unten geschaltet.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT**</dt> <dt>0X0004</dt> </dl>          | Die UMSCHALTTASTE ist nicht mehr gedrückt.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Die erste X-Schaltfläche ist ausgeschaltet.<br/>      |
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

Verwenden Sie den folgenden Code, um die Informationen im *wParam-Parameter* abzurufen.


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Verwenden Sie den folgenden Code, um die horizontale und vertikale Position abzurufen.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Wie oben erwähnt, befindet sich die x-Koordinate in der unteren Reihenfolge **unter** dem Rückgabewert. Die y-Koordinate befindet sich in der hohen **Kurzreihenfolge** (beide stellen *signierte* Werte dar, da sie negative Werte auf Systemen mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen wird, können Sie das [**MAKEPOINTS-Makro**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) verwenden, um eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) aus dem Rückgabewert abzurufen. Sie können auch das [**MAKRO GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) oder [**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die x- oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten aufweisen, und **LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

Die Raddrehung ist ein Vielfaches von **WHEEL \_ DELTA**, das auf 120 festgelegt ist. Dies ist der Schwellenwert für die durchzuführende Aktion, und eine solche Aktion (z. B. scrollen in einem Schritt) sollte für jedes Delta erfolgen.

Das Delta wurde auf 120 festgelegt, damit Microsoft oder andere Anbieter präzisere Radauflösungen erstellen können (z. B. ein frei drehendes Rad ohne Notches), um mehr Nachrichten pro Drehung zu senden, jedoch mit einem kleineren Wert in jeder Nachricht. Um dieses Feature zu verwenden, können Sie entweder die eingehenden Deltawerte hinzufügen, bis **WHEEL \_ DELTA** erreicht ist (für eine Deltarotation erhalten Sie die gleiche Antwort), oder als Reaktion auf häufigere Nachrichten teilzeilen scrollen. Sie können auch Ihre Scrollgranularität auswählen und Deltas sammeln, bis sie erreicht ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (windowsx.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

 

