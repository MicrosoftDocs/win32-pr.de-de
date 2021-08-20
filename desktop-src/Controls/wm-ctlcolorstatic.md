---
title: WM_CTLCOLORSTATIC (Winuser.h)
description: Ein statisches Steuerelement oder ein Bearbeitungssteuer steuerelement, das schreibgeschützt oder deaktiviert ist, sendet die WM CTLCOLORSTATIC-Nachricht an das übergeordnete Fenster, wenn das Steuerelement \_ gezeichnet werden soll.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2df23b86539d07c9e1551d64f59e60e54df24ae2d48b316996542fb80c92ae8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539930"
---
# <a name="wm_ctlcolorstatic-message"></a>WM \_ CTLCOLORSTATIC-Meldung

Ein statisches Steuerelement oder ein Edit-Steuerelement, das schreibgeschützt oder deaktiviert ist, sendet die **WM \_ CTLCOLORSTATIC-Nachricht** an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll. Wenn auf diese Meldung reagiert wird, kann das übergeordnete Fenster das angegebene Gerätekontexthand handle verwenden, um die Text- und Hintergrundfarben des statischen Steuerelements festzulegen.

Ein Fenster empfängt diese Nachricht über seine [*WindowProc-Funktion.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für den Gerätekontext für das statische Steuerfenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das statische Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, ist der Rückgabewert ein Handle für einen Pinsel, mit dem das System den Hintergrund des statischen Steuerelements zeichnet.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung einen von ihr erstellten Pinsel zurückgibt (z. B. mithilfe der [**CreateSolidBrush-**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) oder [**CreateBrushIndirect-Funktion),**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) muss die Anwendung den Pinsel frei geben. Wenn die Anwendung einen Systempinsel zurückgibt (z. B. einen, der von der [**GetStockObject-**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) oder [**GetSysColorBrush-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) abgerufen wurde), muss die Anwendung den Pinsel nicht freigibt.

Standardmäßig wählt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardsystemfarben für das statische Steuerelement aus.

Sie können die Texthintergrundfarbe eines deaktivierten Bearbeitungssteuerfelds festlegen, aber Sie können die Textgrundfarbe nicht festlegen. Das System verwendet immer COLOR \_ GRAYTEXT.

Bearbeitungssteuerelemente, die nicht schreibgeschützt oder deaktiviert sind, senden die **WM \_ CTLCOLORSTATIC-Nachricht** nicht. Stattdessen senden sie die [**\_ WM-CTLCOLOREDIT-Nachricht.**](wm-ctlcoloredit.md)

Die **WM \_ CTLCOLORSTATIC-Nachricht** wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert **in eine INT \_ PTR-Datei** casten und den Wert direkt zurückgeben. Wenn die Dialogfeldprozedur **FALSE zurückgibt,** wird die Standardnachrichtenbehandlung ausgeführt. Der von der \_ [**SetWindowLong-Funktion festgelegte**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) MSGRESULT-DWL-Wert wird ignoriert.

## <a name="examples"></a>Beispiele

Das folgende C++-Beispiel zeigt, wie die Text- und Hintergrundfarben eines statischen Steuerelements als Reaktion auf die **\_ WM-CTLCOLORSTATIC-Meldung festgelegt** werden. Die `hbrBkgnd` Variable ist eine statische **HBRUSH-Variable,** die mit NULL initialisiert wird und den Hintergrundpinsel zwischen Aufrufen von **WM \_ CTLCOLORSTATIC speichert.** Der Pinsel muss durch einen Aufruf der [**DeleteObject-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) zerstört werden, wenn er nicht mehr benötigt wird, in der Regel, wenn das zugeordnete Dialogfeld zerstört wird.


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



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

[**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md)
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

 

