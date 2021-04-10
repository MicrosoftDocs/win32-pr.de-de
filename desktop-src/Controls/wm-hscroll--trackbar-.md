---
title: WM_HSCROLL (TrackBar)-Benachrichtigungs Code (Winuser. h)
description: Die WM- \_ HScroll-Nachricht wird an den Besitzer eines horizontalen TrackBar-Steuer Elements gesendet, wenn die Position des Schiebereglers geändert wird. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- WM_HSCROLL (TrackBar)-Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: 10727b745900520e8af31561236c8e93eeeb3a81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040538"
---
# <a name="wm_hscroll-trackbar-notification-code"></a>WM- \_ HScroll-Benachrichtigungs Code (TrackBar)

Die **WM- \_ HScroll** -Nachricht wird an den Besitzer eines horizontalen TrackBar-Steuer Elements gesendet, wenn die Position des Schiebereglers geändert wird.

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

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Schiebereglers an, wenn das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) eine TB- \_ Fingerposition oder TB-Finger \_ Abdruck aufweist. Für alle anderen Benachrichtigungs Codes ist das höchst wertige Wort 0 (null). sendet die [**TBM- \_ GetPos**](tbm-getpos.md) -Nachricht, um die Position des Schiebereglers zu ermitteln

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt einen Benachrichtigungs Code an, der die Interaktion des Benutzers mit der TrackBar angibt. Bei diesem Wort kann es sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB \_ unten**</dt> </dl>                      | Der Benutzer hat die endtaste gedrückt ([**VK- \_ Ende**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB- \_ EndTrack**</dt> </dl>                | Die TrackBar erhielt eine [**WM- \_ KeyUp**](/windows/desktop/inputdev/wm-keyup), was bedeutet, dass der Benutzer einen Schlüssel freigegeben hat, der einen relevanten Code für den virtuellen Schlüssel gesendet hat <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TB \_ nach unten**</dt> </dl>                | Der Benutzer hat den Pfeil nach rechts ([**VK \_ Rechts**](/windows/desktop/inputdev/virtual-key-codes)) oder die nach-unten-Taste ([**VK- \_ ab**](/windows/desktop/inputdev/virtual-key-codes)) gedrückt.<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**TB \_ -Auflistung**</dt> </dl>                      | Der Benutzer hat den Pfeil nach links ([**VK \_ Links**](/windows/desktop/inputdev/virtual-key-codes)) oder nach oben (nach [**oben) gedrückt \_**](/windows/desktop/inputdev/virtual-key-codes).<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB- \_ PageDown**</dt> </dl>                | Der Benutzer hat auf den Kanal unten oder rechts neben dem Schieberegler geklickt ("[**VK \_ Next**](/windows/desktop/inputdev/virtual-key-codes)").<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB- \_ PageUp**</dt> </dl>                      | Der Benutzer hat auf den Kanal oberhalb oder links neben dem Schieberegler geklickt ([**VK \_ vor**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB-Finger \_ Position**</dt> </dl> | Die TrackBar erhielt [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) nach einem Finger \_ Abdruck-Benachrichtigungs Code von TB.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB-Finger \_ Abdruck**</dt> </dl>          | Der Benutzer hat den Schieberegler gezogen.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB ( \_ oben)**</dt> </dl>                               | Der Benutzer hat die Start Taste gedrückt ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das Handle für das TrackBar-Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Der TB-Finger \_ Abdruck Code wird in der Regel von Anwendungen verwendet, die Feedback geben, wenn der Benutzer das Bild Lauf Feld zieht.

Beachten Sie, dass die **WM- \_ HScroll** -Nachricht nur 16 Bits an Positionsdaten enthält. Daher haben Anwendungen, die ausschließlich von **WM \_ HScroll** (und [**WM \_ VScroll**](wm-vscroll--trackbar-.md)) für Schieberegler-Positionsdaten abhängen, einen praktischen maximalen Positionswert von 65.535.

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

[**WM- \_ VScroll**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

