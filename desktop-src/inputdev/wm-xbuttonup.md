---
title: WM_XBUTTONUP (Winuser.h)
description: Wird veröffentlicht, wenn der Benutzer die erste oder zweite X-Schaltfläche loslässt, während sich der Cursor im Clientbereich eines Fensters befindet.
ms.assetid: ad726859-368a-4603-bffa-4e639bc69a6a
keywords:
- WM_XBUTTONUP der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_XBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 08/23/2019
ms.openlocfilehash: 55b26ae92889261e7a5fea3e57281d6407fc39fb03aad0124d00aa135f9ed438
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757111"
---
# <a name="wm_xbuttonup-message"></a>WM \_ XBUTTONUP-Nachricht

Wird veröffentlicht, wenn der Benutzer die erste oder zweite X-Schaltfläche loslässt, während sich der Cursor im Clientbereich eines Fensters befindet. Wenn die Maus nicht erfasst wird, wird die Nachricht an das Fenster unter dem Cursor gesendet. Andernfalls wird die Nachricht an das Fenster gesendet, in dem die Maus erfasst wurde.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_XBUTTONUP                    0x020C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt an, ob verschiedene virtuelle Schlüssel nicht mehr verwendet werden können. Dies kann einer oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                               | Bedeutung                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROL**</dt> <dt>0x0008</dt> </dl>    | Die STRG-TASTE ist gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON-0x0001**</dt> <dt></dt> </dl>    | Die linke Maustaste ist nach unten.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON-0x0010**</dt> <dt></dt> </dl>    | Die mittlere Maustaste ist nach unten.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON-0x0002**</dt> <dt></dt> </dl>    | Die rechte Maustaste ist nach unten.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT 0X0004**</dt> <dt></dt> </dl>          | Die UMSCHALTTASTE ist heruntergefahren.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1-0x0020**</dt> <dt></dt> </dl> | Die erste X-Schaltfläche ist nicht mehr zu sehen.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2-0x0040**</dt> <dt></dt> </dl> | Die zweite X-Schaltfläche ist nicht mehr zu sehen.<br/>     |



 

Das obere Wort gibt an, welche Schaltfläche freigegeben wurde. Es kann sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                                                     | Bedeutung                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1-0x0001**</dt> <dt></dt> </dl> | Die erste X-Schaltfläche wurde freigegeben.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2-0x0002**</dt> <dt></dt> </dl> | Die zweite X-Schaltfläche wurde freigegeben.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das niedrige Wort gibt die x-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.

Das obere Wort gibt die y-Koordinate des Cursors an. Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE zurückgeben.** Weitere Informationen zur Verarbeitung des Rückgabewerts finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Hinweise

Verwenden Sie den folgenden Code, um die Informationen im *wParam-Parameter* zu erhalten:


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



Verwenden Sie den folgenden Code, um die horizontale und vertikale Position zu erhalten:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wie bereits erwähnt, liegt die x-Koordinate in der niedrigen Reihenfolge **unter dem** Rückgabewert. Die y-Koordinate befindet sich in  der hohen Kurzen **(beide** stellen signierte Werte dar, da sie negative Werte auf Systemen mit mehreren Monitoren übernehmen können). Wenn der Rückgabewert einer Variablen zugewiesen wird, können Sie das [**MAKEPOINTS-Makro**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) verwenden, um eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) aus dem Rückgabewert zu erhalten. Sie können auch das [**GET \_ X \_ LPARAM-**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) oder [**GET \_ \_ Y-LPARAM-Makro**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die x- oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten haben, **und LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

Im Gegensatz [**zu den \_ WM-Meldungen LBUTTONUP,**](wm-lbuttonup.md) [**WM \_ MBUTTONUP**](wm-mbuttonup.md)und [**WM \_ RBUTTONUP**](wm-rbuttonup.md) sollte eine Anwendung **true** aus dieser Meldung zurückgeben, wenn sie sie verarbeitet. Auf diese Weise kann Software, die diese Nachricht auf Windows-Systemen vor Windows 2000 simuliert, bestimmen, ob die Fensterprozedur die Nachricht verarbeitet oder [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um sie zu verarbeiten.

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

[**GET \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ XBUTTON \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
</dt> <dt>

[**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
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

 

