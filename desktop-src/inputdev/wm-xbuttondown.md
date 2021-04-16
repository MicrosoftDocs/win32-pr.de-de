---
title: WM_XBUTTONDOWN Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die erste oder zweite X-Schaltfläche drückt, während sich der Cursor im Client Bereich eines Fensters befindet.
ms.assetid: 4d972841-1513-4925-9d59-2557233561a2
keywords:
- Tastatur-und Maus Eingaben für WM_XBUTTONDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_XBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976a5f3d7282853b5267b0b1640a7a95120efbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477952"
---
# <a name="wm_xbuttondown-message"></a>WM- \_ xbuttondown-Meldung

Wird gesendet, wenn der Benutzer die erste oder zweite X-Schaltfläche drückt, während sich der Cursor im Client Bereich eines Fensters befindet. Wenn die Maus nicht erfasst wird, wird die Nachricht im Fenster unterhalb des Cursors gepostet. Andernfalls wird die Nachricht an das Fenster gesendet, das die Maus erfasst hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_XBUTTONDOWN                  0x020B
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt an, ob verschiedene virtuelle Schlüssel ausfallen. Es kann sich um einen oder mehrere der folgenden Werte handeln:



| Wert                                                                                                                                                                                                               | Bedeutung                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt> </dl>    | Die STRG-Taste ist nicht gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt> </dl>    | Die linke Maustaste ist nicht mehr vorhanden.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MButton**</dt> <dt>0x0010</dt> </dl>    | Die mittlere Maustaste ist nicht mehr angezeigt.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt> </dl>    | Die Rechte Maustaste ist nicht mehr angezeigt.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt> </dl>          | Die UMSCHALTTASTE ist nicht mehr festgelegt.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XButton1**</dt> <dt>0x0020</dt> </dl> | Die erste X-Schaltfläche ist nicht angezeigt.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XButton2**</dt> <dt>0x0040</dt> </dl> | Die zweite X-Schaltfläche ist nicht mehr festgelegt.<br/>     |



 

Das höchst wertige Wort gibt an, auf welche Schaltfläche geklickt wurde. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                     | Bedeutung                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XButton1**</dt> <dt>0x0001</dt> </dl> | Es wurde auf die erste X-Schaltfläche geklickt.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XButton2**</dt> <dt>0x0002</dt> </dl> | Es wurde auf die zweite X-Schaltfläche geklickt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt die x-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.

Das höchst wertige Wort gibt die y-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben. Weitere Informationen zum Verarbeiten des Rückgabewerts finden Sie im Abschnitt "Hinweise".

## <a name="remarks"></a>Bemerkungen

Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten:


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam);
```



Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen. Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.

 

Anders als die Nachrichten [**WM \_ lbuttondown**](wm-lbuttondown.md), [**WM \_ mbuttondown**](wm-mbuttondown.md)und [**WM \_ rbuttondown**](wm-rbuttondown.md) , sollte eine Anwendung bei der Verarbeitung von dieser Nachricht **true** zurückgeben. Auf diese Weise kann Software, die diese Meldung auf Windows-Systemen vor Windows 2000 simuliert, feststellen, ob die Fenster Prozedur die Nachricht verarbeitet oder [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um Sie zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser. h (Include WINDOWSX. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**\_KeyState- \_ wParam-Element**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**\_XButton- \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**\_Y- \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**WM- \_ xbuttondblclk**](wm-xbuttondblclk.md)
</dt> <dt>

[**WM- \_ xbuttonup**](wm-xbuttonup.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkt**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

