---
title: WM_RBUTTONDBLCLK Meldung (Winuser.h)
description: Wird gesendet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im Clientbereich eines Fensters befindet.
ms.assetid: 2db9a947-f052-4738-9fae-6ecaba3de9b9
keywords:
- WM_RBUTTONDBLCLK Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_RBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4b2ee4722825f0404d590d593a2c7f72c815f8cfd2ad4991b0a604c188bfbfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829870"
---
# <a name="wm_rbuttondblclk-message"></a>WM \_ RBUTTONDBLCLK-Nachricht

Wird gesendet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im Clientbereich eines Fensters befindet. Wenn die Maus nicht erfasst wird, wird die Meldung an das Fenster unterhalb des Cursors gesendet. Andernfalls wird die Nachricht an das Fenster gesendet, in dem die Maus erfasst wurde.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_RBUTTONDBLCLK                0x0206
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob verschiedene virtuelle Schlüssel ausgeschaltet sind. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



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

Das Wort mit niedriger Reihenfolge gibt die x-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.

Das Wort in hoher Reihenfolge gibt die y-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Nur Fenster im **CS \_ DBLCLKS-Stil** können **WM \_ RBUTTONDBLCLK-Nachrichten** empfangen, die das System generiert, wenn der Benutzer die rechte Maustaste innerhalb des Doppelklick-Zeitlimits des Systems drückt, loslässt und erneut drückt. Wenn Sie mit der rechten Maustaste doppelklicken, werden vier Meldungen generiert: [**WM \_ RBUTTONDOWN,**](wm-rbuttondown.md) [**WM \_ RBUTTONUP,**](wm-rbuttonup.md) **WM \_ RBUTTONDBLCLK** und **WM \_ RBUTTONUP.**

Verwenden Sie den folgenden Code, um die horizontale und vertikale Position abzurufen:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wie oben erwähnt, befindet sich die x-Koordinate in der unteren Reihenfolge **unter** dem Rückgabewert. Die y-Koordinate befindet sich in der hohen **Kurzreihenfolge** (beide stellen *signierte* Werte dar, da sie negative Werte auf Systemen mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen wird, können Sie das [**MAKEPOINTS-Makro**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) verwenden, um eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) aus dem Rückgabewert abzurufen. Sie können auch das [**MAKRO GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) oder [**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die x- oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten aufweisen, und **LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (windowsx.h einschließen)</dt> </dl> |



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

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)
</dt> <dt>

[**WM \_ RBUTTONUP**](wm-rbuttonup.md)
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

 

