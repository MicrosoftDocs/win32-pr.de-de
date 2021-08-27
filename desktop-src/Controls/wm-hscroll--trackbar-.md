---
title: WM_HSCROLL -Benachrichtigungscode (Trackbar) (Winuser.h)
description: Die WM HSCROLL-Meldung wird an den Besitzer eines horizontalen \_ Trackbar-Steuerelements gesendet, wenn der Schieberegler die Position ändert. Ein Fenster empfängt diese Nachricht über seine WindowProc-Funktion.
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- WM_HSCROLL -Benachrichtigungscode (Trackbar) Windows Steuerelementen
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
ms.openlocfilehash: 5a21000f9eeeb3ff83d4fb65456b21447aa3fd604412f3b4d6d3b94fda58606b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059310"
---
# <a name="wm_hscroll-trackbar-notification-code"></a>WM \_ HSCROLL-Benachrichtigungscode (Trackbar)

Die **WM \_ HSCROLL-Meldung** wird an den Besitzer eines horizontalen Trackbar-Steuerelements gesendet, wenn der Schieberegler die Position ändert.

Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die aktuelle Position des Schiebereglers an, wenn [**das LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) TB \_ THUMBPOSITION oder TB \_ THUMBTRACK ist. Für alle anderen Benachrichtigungscodes ist das obere Wort 0 (null). Senden Sie die [**TBM \_ GETPOS-Nachricht,**](tbm-getpos.md) um die Position des Schiebereglers zu bestimmen.

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) einen Benachrichtigungscode an, der die Interaktion des Benutzers mit der Trackleiste angibt. Dieses Wort kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TB \_ BOTTOM**</dt> </dl>                      | Der Benutzer hat die END-TASTE [**(VK \_ END ) gedrückt.**](/windows/desktop/inputdev/virtual-key-codes)<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TB \_ ENDTRACK**</dt> </dl>                | Die Trackleiste hat [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)empfangen. Dies bedeutet, dass der Benutzer einen Schlüssel freigegeben hat, der einen relevanten virtuellen Schlüsselcode gesendet hat. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**\_TB-LINEDOWN**</dt> </dl>                | Der Benutzer hat die NACH-RECHTS-TASTE [**(VK \_ NACH-RECHTS)**](/windows/desktop/inputdev/virtual-key-codes)oder DIE NACH-UNTEN-TASTE [**(VK \_ NACH-UNTEN)**](/windows/desktop/inputdev/virtual-key-codes)gedrückt.<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**TB \_ LINEUP**</dt> </dl>                      | Der Benutzer hat die NACH-LINKS-TASTE [**(VK \_ LEFT)**](/windows/desktop/inputdev/virtual-key-codes)oder DIE NACH-OBEN-TASTE [**(VK \_ NACH OBEN)**](/windows/desktop/inputdev/virtual-key-codes)gedrückt.<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TB \_ PAGEDOWN**</dt> </dl>                | Der Benutzer hat auf den Kanal unten oder rechts neben dem Schieberegler [**(VK \_ NEXT ) geklickt.**](/windows/desktop/inputdev/virtual-key-codes)<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TB \_ PAGEUP**</dt> </dl>                      | Der Benutzer hat auf den Kanal oben oder links vom Schieberegler geklickt [**(VK \_ PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TB \_ THUMBPOSITION**</dt> </dl> | Die Trackleiste hat [**WM \_ LBUTTONUP nach**](/windows/desktop/inputdev/wm-lbuttonup) einem TB \_ THUMBTRACK-Benachrichtigungscode empfangen.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TB \_ THUMBTRACK**</dt> </dl>          | Der Benutzer hat den Schieberegler gezogen.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TB \_ TOP**</dt> </dl>                               | Der Benutzer hat die HOME-TASTE gedrückt ([**VK \_ HOME**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das Handle für das Trackbar-Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Der TB THUMBTRACK-Code wird in der Regel von Anwendungen verwendet, die Feedback geben, wenn der \_ Benutzer das Bildlauffeld zieht.

Beachten Sie, dass **die WM \_ HSCROLL-Nachricht** nur 16 Bits von Positionsdaten enthält. Daher haben Anwendungen, die ausschließlich **WM \_ HSCROLL** (und [**WM \_ VSCROLL)**](wm-vscroll--trackbar-.md)für Schiebereglerpositionsdaten verwenden, einen praktischen maximalen Positionswert von 65.535.

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

[**WM \_ VSCROLL**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

