---
title: WM_CTLCOLORSCROLLBAR (Winuser.h)
description: Die WM CTLCOLORSCROLLBAR-Meldung wird an das übergeordnete Fenster eines Bildlaufleisten-Steuerelements gesendet, wenn das Steuerelement \_ gezeichnet werden soll.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR von Windows Steuerelementen
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
ms.openlocfilehash: 35dba3394c3d8fd99fef88d6fa1869ea1129d95ae8a82cc33f2935e5688871a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018558"
---
# <a name="wm_ctlcolorscrollbar-message"></a>WM \_ CTLCOLORSCROLLBAR-Meldung

Die **WM \_ CTLCOLORSCROLLBAR-Meldung** wird an das übergeordnete Fenster eines Bildlaufleisten-Steuerelements gesendet, wenn das Steuerelement gezeichnet werden soll. Wenn auf diese Meldung reagiert wird, kann das übergeordnete Fenster das Anzeigekontexthand handle verwenden, um die Hintergrundfarbe des Bildlaufleisten-Steuerelements fest zu legen.

Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für den Gerätekontext für das Bildlaufleisten-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die Bildlaufleiste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss sie das Handle an einen Pinsel zurückgeben. Das System verwendet den Pinsel, um den Hintergrund des Bildlaufleisten-Steuerelements zu zeichnen.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung einen von ihr erstellten Pinsel zurückgibt (z. B. mithilfe der [**CreateSolidBrush-**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) oder [**CreateBrushIndirect-Funktion),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) muss die Anwendung den Pinsel frei geben. Wenn die Anwendung einen Systempinsel zurückgibt (z. B. einen, der von der [**GetStockObject-**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) oder [**GetSysColorBrush-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) abgerufen wurde), muss die Anwendung den Pinsel nicht freigibt.

Standardmäßig wählt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardsystemfarben für das Bildlaufleisten-Steuerelement aus.

Die **WM \_ CTLCOLORSCROLLBAR-Nachricht** wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert **in eine INT \_ PTR-Datei** casten und den Wert direkt zurückgeben. Wenn die Dialogfeldprozedur **FALSE zurückgibt,** wird die Standardnachrichtenbehandlung ausgeführt. Der von der \_ [**SetWindowLong-Funktion festgelegte**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) MSGRESULT-DWL-Wert wird ignoriert.

Die **WM \_ CTLCOLORSCROLLBAR-Meldung** wird nur von untergeordneten Scrollleisten-Steuerelementen verwendet. Scrollleisten, die an ein Fenster angefügt sind (WS \_ SCROLL und WS \_ VSCROLL), generieren diese Meldung nicht. Verwenden Sie zum Anpassen der Darstellung von Scrollleisten, die an ein Fenster angefügt sind, die Funktionen für flache Scrollleisten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**Wählen SiePalette aus.**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**WM \_ CTLCOLORDLG**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

