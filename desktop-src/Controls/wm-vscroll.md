---
title: WM_VSCROLL Meldung (Winuser. h)
description: Die WM \_ -VScroll-Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der vertikalen Standard Scrollleiste des Fensters auftritt.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- Windows-Steuerelemente für WM_VSCROLL Meldung
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
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106154"
---
# <a name="wm_vscroll-message"></a>WM- \_ VScroll-Nachricht

Die **WM- \_ VScroll** -Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der vertikalen Standard Scrollleiste des Fensters auftritt. Diese Meldung wird auch an den Besitzer eines vertikalen Schiebe leisten-Steuer Elements gesendet, wenn im-Steuerelement ein scrollereignis auftritt.

Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Bild Lauf Felds an, wenn das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) SB- \_ Fingerposition oder SB-Finger \_ Abdruck ist; andernfalls wird dieses Wort nicht verwendet.

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt einen Scrollleisten-Wert an, der die scrollanforderung des Benutzers angibt. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ unten**</dt> </dl>                      | Führt einen Bildlauf nach unten rechts aus.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB- \_ endscroll**</dt> </dl>             | Beendet den Bildlauf.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB- \_ LineDown**</dt> </dl>                | Führt einen Bildlauf nach unten durch.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ -Auflistung**</dt> </dl>                      | Führt einen Bildlauf nach oben durch.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB- \_ PageDown**</dt> </dl>                | Führt einen Bildlauf nach unten durch.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB- \_ PageUp**</dt> </dl>                      | Führt einen Bildlauf nach oben durch.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB-Finger \_ Position**</dt> </dl> | Der Benutzer hat das Bild Lauf Feld (Thumb) gezogen und die Maustaste losgelassen. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) zeigt die Position des Bild Lauf Felds am Ende des Zieh Vorgangs an.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB-Finger \_ Abdruck**</dt> </dl>          | Der Benutzer zieht die Bildlaufbox. Diese Meldung wird wiederholt gesendet, bis der Benutzer die Maustaste loslässt. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Position an, zu der das Bild Lauf Feld gezogen wurde.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB- \_ Top**</dt> </dl>                               | Führt einen Bildlauf nach oben links durch.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn die Nachricht von einem Schiebe leisten-Steuerelement gesendet wird, ist dieser Parameter das Handle für das ScrollBar-Steuerelement. Wenn die Nachricht von einer Standard Scrollleiste gesendet wird, ist dieser Parameter **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Der SB- \_ ThumbTrack-Anforderungs Code wird in der Regel von Anwendungen verwendet, die Feedback geben, wenn der Benutzer das Bild Lauf Feld zieht.

Wenn eine Anwendung im Inhalt des Fensters einen Bildlauf durchführt, muss Sie auch die Position des Bild Lauf Felds mithilfe der [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) -Funktion Zurücksetzen.

Beachten Sie, dass die **WM \_ VScroll** -Nachricht nur 16 Bits an Positionsdaten der Scrollbox enthält. Daher haben Anwendungen, die sich ausschließlich auf **WM \_ VScroll** (und [**WM \_ HScroll**](wm-hscroll.md)) für Bild Lauf Positionsdaten verlassen, einen praktischen maximalen Positionswert von 65.535.

Da die Funktionen [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)und [**getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) jedoch 32-Bit-ScrollBar-Positionsdaten unterstützen, gibt es eine Möglichkeit, die 16-Bit-Barriere der [**WM \_ HScroll**](wm-hscroll.md) -und **WM \_ VScroll** -Nachrichten zu umgehen. Eine Beschreibung der Technik finden Sie unter **getscrollinfo** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**Getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**Getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**Setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**Setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**WM- \_ HScroll**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VScroll (TrackBar)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

