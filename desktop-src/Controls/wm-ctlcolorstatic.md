---
title: WM_CTLCOLORSTATIC Meldung (Winuser. h)
description: Ein statisches Steuerelement oder ein Schreib geschütztes oder deaktiviertes Bearbeitungs Steuerelement sendet die WM \_ ctlcolorstatic-Meldung an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- Windows-Steuerelemente für WM_CTLCOLORSTATIC Meldung
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
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741368"
---
# <a name="wm_ctlcolorstatic-message"></a>WM \_ ctlcolorstatic-Meldung

Ein statisches Steuerelement oder ein Schreib geschütztes oder deaktiviertes Bearbeitungs Steuerelement sendet die **WM \_ ctlcolorstatic** -Meldung an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den angegebenen Gerätekontext Handle verwenden, um die Text Vordergrund-und Hintergrundfarben des statischen Steuer Elements festzulegen.

Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für den Gerätekontext für das statische Steuerelement Fenster.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das statische Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, ist der Rückgabewert ein Handle für einen Pinsel, den das System zum Zeichnen des Hintergrunds des statischen Steuer Elements verwendet.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben. Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.

Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das statische Steuerelement aus.

Sie können die Text Hintergrundfarbe eines deaktivierten Bearbeitungs Steuer Elements festlegen, aber Sie können die textvorder Grundfarbe nicht festlegen. Das System verwendet immer Color \_ GrayText.

Wenn Sie Steuerelemente bearbeiten, die nicht schreibgeschützt oder deaktiviert sind, wird die " **WM \_ ctlcolorstatic** "-Nachricht nicht gesendet; stattdessen wird die [**WM- \_ ctlcoloredit**](wm-ctlcoloredit.md) -Nachricht gesendet.

Die " **WM \_ ctlcolorstatic** "-Meldung wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben. Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt. Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.

## <a name="examples"></a>Beispiele

Im folgenden C++-Beispiel wird gezeigt, wie die Text Vordergrund-und Hintergrundfarben eines statischen-Steuer Elements als Reaktion auf die **WM \_ ctlcolorstatic** -Nachricht festgelegt werden. Die `hbrBkgnd` Variable ist eine statische **hBrush** -Variable, die mit NULL initialisiert wird, und speichert den Hintergrund Pinsel zwischen den Aufrufen von **WM \_ ctlcolorstatic**. Der Pinsel muss durch einen Aufrufen der [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) -Funktion zerstört werden, wenn er nicht mehr benötigt wird, in der Regel, wenn das zugehörige Dialogfeld zerstört wird.


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

[**WM \_ ctlcolorscrollbar**](wm-ctlcolorscrollbar.md)
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

 

