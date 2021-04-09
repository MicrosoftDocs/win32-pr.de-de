---
title: WM_CTLCOLORSCROLLBAR Meldung (Winuser. h)
description: Die WM- \_ ctlcolorscrollbar-Meldung wird an das übergeordnete Fenster eines ScrollBar-Steuer Elements gesendet, wenn das Steuerelement gezeichnet wird.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Windows-Steuerelemente für WM_CTLCOLORSCROLLBAR Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949814"
---
# <a name="wm_ctlcolorscrollbar-message"></a>WM \_ ctlcolorscrollbar-Meldung

Die **WM- \_ ctlcolorscrollbar** -Meldung wird an das übergeordnete Fenster eines ScrollBar-Steuer Elements gesendet, wenn das Steuerelement gezeichnet wird. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den Kontext Zieh Punkt der Anzeige verwenden, um die Hintergrundfarbe des ScrollBar-Steuer Elements festzulegen.

Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für den Gerätekontext für das ScrollBar-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die Bild Lauf Leiste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie das Handle an einen Pinsel zurückgeben. Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des ScrollBar-Steuer Elements.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben. Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.

Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das ScrollBar-Steuerelement aus.

Die " **WM \_ ctlcolorscrollbar** "-Nachricht wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben. Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt. Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.

Die " **WM \_ ctlcolorscrollbar** "-Meldung wird nur von untergeordneten ScrollBar-Steuerelementen verwendet. Bild Lauf leisten, die an ein Fenster angefügt sind (WS \_ Scroll und WS \_ VScroll), generieren diese Meldung nicht. Verwenden Sie zum Anpassen der Darstellung von Bild Lauf leisten, die an ein Fenster angefügt sind, die Funktionen der flatscrollleiste.

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

[**WM \_ ctlcolorbtn**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ ctlcoloredit**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ ctlcolorlistbox**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ ctlcolorstatic**](wm-ctlcolorstatic.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**WM \_ ctlcolordlg**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

