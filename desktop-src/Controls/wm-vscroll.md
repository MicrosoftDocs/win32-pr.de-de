---
title: WM_VSCROLL (Winuser.h)
description: Die WM VSCROLL-Meldung wird an ein Fenster gesendet, wenn ein Bildlaufereignis in der standardmäßigen vertikalen Scrollleiste des \_ Fensters auftritt.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbb87f63cb0f4801787be1f2cb23b321470b1053a58b13d0f3eea34112b1341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636710"
---
# <a name="wm_vscroll-message"></a>WM \_ VSCROLL-Meldung

Die **WM \_ VSCROLL-Meldung** wird an ein Fenster gesendet, wenn ein Bildlaufereignis in der standardmäßigen vertikalen Scrollleiste des Fensters auftritt. Diese Meldung wird auch an den Besitzer eines vertikalen Bildlaufleisten-Steuerelements gesendet, wenn ein Bildlaufereignis im Steuerelement auftritt.

Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die aktuelle Position des Bildlauffelds an, wenn [**DAS LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) SB THUMBPOSITION oder \_ SB \_ THUMBTRACK ist. Andernfalls wird dieses Wort nicht verwendet.

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) einen Bildlaufleistenwert an, der die Scrollanforderung des Benutzers angibt. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ BOTTOM**</dt> </dl>                      | Führt einen Bildlauf nach unten rechts durch.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> </dl>             | Beendet den Bildlauf.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl>                | Führt einen Bildlauf um eine Zeile nach unten aus.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> </dl>                      | Führt einen Bildlauf um eine Zeile nach oben aus.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> </dl>                | Führt einen Bildlauf um eine Seite nach unten aus.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> </dl>                      | Führt einen Bildlauf um eine Seite nach oben aus.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> </dl> | Der Benutzer hat das Bildlauffeld (Ziehfinger) gezogen und die Maustaste losgelassen. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die Position des Bildlauffelds am Ende des Ziehvorgang an.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ THUMBTRACK**</dt> </dl>          | Der Benutzer zieht die Bildlaufbox. Diese Meldung wird wiederholt gesendet, bis der Benutzer die Maustaste loslässt. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die Position an, an die das Bildlauffeld gezogen wurde.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> </dl>                               | Scrollt nach oben links.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn die Nachricht von einem Bildlaufleisten-Steuerelement gesendet wird, ist dieser Parameter das Handle für das Bildlaufleisten-Steuerelement. Wenn die Nachricht von einer Standardscrollleiste gesendet wird, ist dieser Parameter **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Der SB THUMBTRACK-Anforderungscode wird in der Regel von Anwendungen verwendet, die Feedback geben, wenn der \_ Benutzer das Bildlauffeld zieht.

Wenn eine Anwendung durch den Inhalt des Fensters scrollt, muss sie auch die Position des Bildlauffelds mithilfe der [**SetScrollPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) zurücksetzen.

Beachten Sie, dass **die WM \_ VSCROLL-Nachricht** nur 16 Bits bildlauffeldpositionsdaten enthält. Daher haben Anwendungen, die ausschließlich **WM \_ VSCROLL** (und [**WM \_ HSCROLL)**](wm-hscroll.md)für Bildlaufpositionsdaten verwenden, einen praktischen maximalen Positionswert von 65.535.

Da die Funktionen [**SetScrollInfo,**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) [**SetScrollPos,**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) [**SetScrollRange,**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) [**GetScrollInfo,**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)und [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) jedoch 32-Bit-Bildlaufleisten-Positionsdaten unterstützen, gibt es eine Möglichkeit, die 16-Bit-Barriere der [**WM \_ HSCROLL-**](wm-hscroll.md) und **WM \_ VSCROLL-Meldungen** zu umgehen. Eine Beschreibung der Technik finden Sie unter **GetScrollInfo.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**WM \_ HSCROLL**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (Trackbar)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

