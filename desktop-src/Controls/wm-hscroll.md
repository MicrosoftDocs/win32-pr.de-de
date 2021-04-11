---
title: WM_HSCROLL Meldung (Winuser. h)
description: Die WM \_ -HScroll-Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der horizontalen Standard Scrollleiste des Fensters auftritt.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- Windows-Steuerelemente für WM_HSCROLL Meldung
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104421"
---
# <a name="wm_hscroll-message"></a>WM- \_ hscrollnachricht

Die **WM- \_ HScroll** -Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der horizontalen Standard Scrollleiste des Fensters auftritt. Diese Meldung wird auch an den Besitzer eines horizontalen Schiebe leisten-Steuer Elements gesendet, wenn im-Steuerelement ein scrollereignis auftritt.

Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Bild Lauf Felds an, wenn das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) SB- \_ Fingerposition oder SB-Finger \_ Abdruck ist; andernfalls wird dieses Wort nicht verwendet.

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt einen Scrollleisten-Wert an, der die scrollanforderung des Benutzers angibt. Bei diesem Wort kann es sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB- \_ endscroll**</dt> </dl>             | Beendet den Bildlauf.<br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ Links**</dt> </dl>                            | Führt einen Bildlauf nach oben links durch.<br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ right**</dt> </dl>                         | Führt einen Bildlauf nach unten rechts aus.<br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB- \_ LineLeft**</dt> </dl>                | Scrollt nach links um eine Einheit.<br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB- \_ LineRight**</dt> </dl>             | Scrollt nach rechts um eine Einheit.<br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB- \_ PageLeft**</dt> </dl>                | Führt einen Bildlauf nach links um die Breite des Fensters aus.<br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB- \_ PageRight**</dt> </dl>             | Führt einen Bildlauf nach rechts um die Breite des Fensters aus.<br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB-Finger \_ Position**</dt> </dl> | Der Benutzer hat das Bild Lauf Feld (Thumb) gezogen und die Maustaste losgelassen. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) zeigt die Position des Bild Lauf Felds am Ende des Zieh Vorgangs an.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB-Finger \_ Abdruck**</dt> </dl>          | Der Benutzer zieht die Bildlaufbox. Diese Meldung wird wiederholt gesendet, bis der Benutzer die Maustaste loslässt. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Position an, zu der das Bild Lauf Feld gezogen wurde.<br/> |



 

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

Beachten Sie, dass die **WM- \_ HScroll** -Nachricht nur 16 Bits an Positionsdaten der Scrollbox enthält. Daher haben Anwendungen, die ausschließlich von **WM \_ HScroll** (und [**WM \_ VScroll**](wm-vscroll.md)) für Bild Lauf Positionsdaten abhängen, einen praktischen maximalen Positionswert von 65.535.

Da die Funktionen [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)und [**getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) jedoch 32-Bit-ScrollBar-Positionsdaten unterstützen, gibt es eine Möglichkeit, die 16-Bit-Barriere der **WM \_ HScroll** -und [**WM \_ VScroll**](wm-vscroll.md) -Nachrichten zu umgehen. Eine Beschreibung der Technik finden Sie unter **getscrollinfo** .

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

[**WM \_ HScroll (TrackBar)**](wm-hscroll--trackbar-.md)
</dt> <dt>

[**WM- \_ VScroll**](wm-vscroll.md)
</dt> </dl>

 

