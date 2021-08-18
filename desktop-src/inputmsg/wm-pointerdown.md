---
title: WM_POINTERDOWN Meldung
description: Wird gesendet, wenn ein Zeiger den Kontakt über den Clientbereich eines Fensters annimmt.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN Nachrichteneingabenachrichten und -benachrichtigungen
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: fd2c5900cba4a66b4f7cf94f1df362ddc0f29f3d258b972b77ad63f3fd45a5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481981"
---
# <a name="wm_pointerdown-message"></a>WM_POINTERDOWN Meldung

Wird gesendet, wenn ein Zeiger den Kontakt über den Clientbereich eines Fensters annimmt. Diese Eingabenachricht ist auf das Fenster ausgerichtet, über das der Zeiger Kontakt aufnimmt, und der Zeiger wird implizit auf das Fenster aufgezeichnet, sodass das Fenster weiterhin Eingaben für den Zeiger empfängt, bis er den Kontakt unterbricht.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält Informationen über den Zeiger. Verwenden Sie die folgenden Makros, um Informationen aus dem wParam-Parameter abzurufen.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): der Zeigerbezeichner.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht die erste Eingabe darstellt, die von einem neuen Zeiger generiert wurde.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht während der Lebensdauer von einem Zeiger generiert wurde. Dieses Flag ist nicht für Meldungen festgelegt, die darauf hinweisen, dass der Zeiger über den linken Erkennungsbereich verfügt.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht von einem Zeiger generiert wurde, der mit der Fensteroberfläche in Kontakt steht. Dieses Flag ist nicht für Nachrichten festgelegt, die auf einen Zeigenzeiger hinweisen.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): gibt an, dass dieser Zeiger als primär festgelegt wurde.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob eine primäre Aktion vorhanden ist.
    -   Dies entspricht einer linken Maustaste nach unten.
    -   Für einen Touchzeiger wird dieser festgelegt, wenn er mit der Digitizeroberfläche in Kontakt steht.
    -   Für einen Stiftzeiger wird diese Einstellung festgelegt, wenn sie ohne Gedrückte Schaltflächen mit der Digitizeroberfläche in Kontakt steht.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob eine sekundäre Aktion vorhanden ist.
    -   Dies entspricht einer Nach-unten-Taste mit der rechten Maustaste.
    -   Für einen Stiftzeiger wird dieser festgelegt, wenn er mit der Digitizeroberfläche in Kontakt steht und die Stiftschaltfläche gedrückt wird.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine oder mehrere tertiäre Aktionen basierend auf dem Zeigertyp vorhanden sind. -Anwendungen, die auf bildungsbezogene Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, auf welche tertiären Schaltflächen gedrückt werden. Beispielsweise kann eine Anwendung die Schaltflächenzustände eines Stifts bestimmen, indem [**Sie GetPointerPenInfo**](/previous-versions/windows/desktop/api) aufrufen und die Flags untersuchen, die Schaltflächenzustände angeben.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob der angegebene Zeiger die vierte Aktion ausgeführt hat. Anwendungen, die auf vierte Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die erste erweiterte Mausschaltfläche (XButton1) gedrückt wird.
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein [**Flag,**](pointer-flags-contants.md) das angibt, ob der angegebene Zeiger die fünfte Aktion ausgeführt hat. Anwendungen, die auf fünfte Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die zweite erweiterte Maustaste (XButton2) gedrückt wird.

    Weitere Informationen finden Sie unter [**Zeigerflags.**](pointer-flags-contants.md)

    > [!Note]  
    > Für einen zeigenden Zeiger ist keines der Schaltflächenflags festgelegt. Dies entspricht einer Mauszeigerbewegung ohne Nach-unten-Maustasten. Eine Anwendung kann die Schaltflächenzustände eines Stifts mit dem Mauszeiger bestimmen, indem sie beispielsweise [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) aufruft und die Flags untersucht, die Schaltflächenzustände angeben.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich herstellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein. Wenn möglich, sollte eine Anwendung anstelle der Punktposition die vollständigen Zeigerbereichsinformationen verwenden.

 

Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): die x-Koordinate (horizontaler Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): die y-Koordinate (vertikaler Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte sie [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufrufen.

## <a name="remarks"></a>Hinweise

> \[! Wichtig\]  
> Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, empfängt es in der Regel keine weiteren Benachrichtigungen. Aus diesem Grund ist es wichtig, dass Sie keine Annahmen basierend auf gleichmäßig gekoppelten **WM_POINTERDOWN** / [**WM_POINTERUP**](wm-pointerup.md) oder [**WM_POINTERENTER**](wm-pointerenter.md) / [**WM_POINTERLEAVE-Benachrichtigungen**](wm-pointerleave.md) treffen.

 

Jeder Zeiger verfügt während seiner Lebensdauer über einen eindeutigen Zeigerbezeichner. Die Lebensdauer eines Zeigers beginnt, wenn er zum ersten Mal erkannt wird.

Eine [**WM_POINTERENTER**](wm-pointerenter.md) Meldung wird generiert, wenn ein Zeiger mit dem Mauszeiger erkannt wird. Eine **WM_POINTERDOWN** Nachricht gefolgt von einer **WM_POINTERENTER** Nachricht wird generiert, wenn ein Zeiger erkannt wird, der nicht mit dem Mauszeiger zeigt.

Während seiner Lebensdauer kann ein Zeiger eine Reihe von [**WM_POINTERUPDATE**](wm-pointerupdate.md) Nachrichten generieren, während er mit dem Mauszeiger oder im Kontakt ist.

Die Lebensdauer eines Zeigers endet, wenn er nicht mehr erkannt wird. Dadurch wird eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Meldung generiert.

Wenn ein Zeiger abgebrochen wird, wird [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) festgelegt.

Eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Nachricht kann auch generiert werden, wenn sich ein nicht erfasster Zeiger außerhalb der Grenzen eines Fensters bewegt.

Um die horizontale und vertikale Position eines Zeigers abzurufen, verwenden Sie Folgendes:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Verwenden Sie das [**MAKEPOINTS-Makro,**](/windows/win32/api/wingdi/nf-wingdi-makepoints) um den lParam-Parameter in eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) zu konvertieren.

Verwenden Sie die [**GetPointerInfo-Funktion,**](/previous-versions/windows/desktop/api) um weitere Der Nachricht zugeordnete Informationen abzurufen.

Verwenden Sie die [**GetKeyState-Funktion,**](/windows/win32/api/winuser/nf-winuser-getkeystate) um die dieser Meldung zugeordneten Tastenzustände des Tastaturmodifizierer zu bestimmen. Um beispielsweise zu erkennen, dass die ALT-Taste gedrückt wurde, überprüfen Sie, ob GetKeyState(VK_MENU) &lt; 0 lautet.

Beachten Sie Folgendes: Wenn die Anwendung diese Nachricht nicht verarbeitet, generiert [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) möglicherweise eine oder mehrere [**WM_GESTURE**](../wintouch/wm-gesture.md) Nachrichten, wenn die Sequenz der Eingabe von dieser und möglicherweise anderen Zeigern als Geste erkannt wird. Wenn eine Geste nicht erkannt wird, generiert **DefWindowProc** möglicherweise Mauseingaben.

Wenn eine Anwendung selektiv Zeigereingaben nutzt und den Rest an [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergibt, ist das resultierende Verhalten nicht definiert.

Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, empfängt es in der Regel keine weiteren Benachrichtigungen. Daher ist es wichtig, dass ein Fenster keine Annahmen über seinen Zeigerstatus trifft, unabhängig davon, ob es gleichmäßig gekoppelte DOWN-/UP- oder ENTER/LEAVE-Benachrichtigungen empfängt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie [**sie IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)und [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)verwenden, um die relevanten Informationen abzurufen, die der **WM_POINTERDOWN** Nachricht zugeordnet sind.


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



Im folgenden Codebeispiel wird veranschaulicht, wie [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) verwendet wird, um die Zeiger-ID aus der **WM_POINTERDOWN-Nachricht** abzurufen.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



Das folgende Codebeispiel zeigt, wie verschiedene Zeigertypen wie Toucheingaben, Stifte oder Standardzeigergeräte behandelt werden.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

**Referenz**
</dt> <dt>

[**Zeigerflags**](pointer-flags-contants.md)
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>
