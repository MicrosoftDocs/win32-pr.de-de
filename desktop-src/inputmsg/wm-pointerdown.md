---
title: WM_POINTERDOWN Meldung
description: Wird gepostet, wenn ein Zeiger über den Client Bereich eines Fensters kontaktiert wird.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERDOWN Nachricht
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
ms.openlocfilehash: 051e7f0aa08305e4c38d7eefec94483fd11f3bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104858"
---
# <a name="wm_pointerdown-message"></a>WM_POINTERDOWN Meldung

Wird gepostet, wenn ein Zeiger über den Client Bereich eines Fensters kontaktiert wird. Diese Eingabe Nachricht bezieht sich auf das Fenster, über das der Zeiger Kontakt herstellt, und der Zeiger wird implizit im Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger empfängt, bis der Kontakt unterbrochen wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

> \[! Wichtig\]  
> Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält Informationen über den-Zeiger. Verwenden Sie die folgenden Makros zum Abrufen von Informationen aus dem wParam-Parameter.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): der Zeiger Bezeichner.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob diese Meldung die erste Eingabe darstellt, die von einem neuen Zeiger generiert wird.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob diese Meldung während ihrer Lebensdauer von einem Zeiger generiert wurde. Dieses Flag ist für Meldungen, die darauf hinweisen, dass der Zeiger den linken Erkennungsbereich aufweist, nicht festgelegt.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob diese Meldung von einem Zeiger generiert wurde, der sich in Verbindung mit der Fenster Oberfläche befindet. Dieses Flag ist nicht für Meldungen festgelegt, die einen Mauszeiger angeben.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): gibt an, dass dieser Zeiger als primär festgelegt wurde.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine primäre Aktion vorliegt.
    -   Dies ist analog zu einer mouseleft-Schaltfläche nach unten.
    -   Ein Fingerabdruck wird festgelegt, wenn er sich mit der digitalisiereroberfläche in Verbindung setzt.
    -   Bei einem Stift Zeiger wird dieser Satz festgelegt, wenn er sich auf der digitalisiereroberfläche befindet und keine Schaltflächen gedrückt sind.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine sekundäre Aktion vorliegt.
    -   Dies ist analog zu einer Maustaste nach unten.
    -   Bei einem Stift Zeiger wird dieser Satz festgelegt, wenn er sich im Kontakt mit der Digitalisierungs Oberfläche befindet, auf die die Stift Taste gedrückt wird.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine oder mehrere tertiäre Aktionen auf Grundlage des Zeiger Typs vorhanden sind. Anwendungen, die auf tertiäre Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, welche tertiären Schaltflächen gedrückt werden. Eine Anwendung kann z. b. die Schaltflächen Zustände eines Stifts ermitteln, indem [**getpointerpeninfo**](/previous-versions/windows/desktop/api) aufgerufen und die Flags untersucht werden, die Schaltflächen Zustände angeben.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob der angegebene Zeiger die vierte Aktion gedauert hat. Anwendungen, die auf vierte Aktionen antworten möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die erste erweiterte Maus Taste (XButton1) gedrückt ist.
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein [**Flag**](pointer-flags-contants.md) , das angibt, ob der angegebene Zeiger eine fünfte Aktion gedauert hat. Anwendungen, die auf fünfte Aktionen antworten möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die zweite Schaltfläche mit der erweiterten Maus (XButton2) gedrückt ist.

    Weitere Informationen finden Sie unter [**Zeiger-Flags**](pointer-flags-contants.md) .

    > [!Note]  
    > Für einen Mauszeiger ist keines der schaltflächenflags festgelegt. Dies ist analog zu einer Mausbewegung ohne die Maustasten. Eine Anwendung kann die Schaltflächen Zustände eines Maus zeigenden Stifts ermitteln, z. b. durch Aufrufen von [**getpointerpeninfo**](/previous-versions/windows/desktop/api) und untersuchen der Flags, die Schaltflächen Zustände angeben.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist. Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.

 

Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.

## <a name="remarks"></a>Bemerkungen

> \[! Wichtig\]  
> Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, werden normalerweise keine weiteren Benachrichtigungen empfangen. Aus diesem Grund ist es wichtig, dass Sie keine Annahmen auf der Grundlage von gleichmäßig gekoppelten **WM_POINTERDOWN** / [**WM_POINTERUP**](wm-pointerup.md) oder [**WM_POINTERENTER**](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) Benachrichtigungen treffen.

 

Jeder Zeiger hat während seiner Lebensdauer einen eindeutigen Zeiger Bezeichner. Die Lebensdauer eines Zeigers beginnt, wenn er erstmals erkannt wird.

Eine [**WM_POINTERENTER**](wm-pointerenter.md) Meldung wird generiert, wenn ein Mauszeiger erkannt wird. Eine **WM_POINTERDOWN** Meldung, auf die eine **WM_POINTERENTER** Meldung folgt, wird generiert, wenn ein nicht Mauszeiger erkannt wird.

Während der Lebensdauer kann ein Zeiger eine Reihe von [**WM_POINTERUPDATE**](wm-pointerupdate.md) Meldungen generieren, während er darauf zeigt oder in Kontakt steht.

Die Lebensdauer eines Zeigers endet, wenn er nicht mehr erkannt wird. Dadurch wird eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Nachricht generiert.

Wenn ein Zeiger abgebrochen wird, wird [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) festgelegt.

Eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Meldung kann auch generiert werden, wenn ein nicht erfasster Zeiger außerhalb der Begrenzungen eines Fensters bewegt wird.

Um die horizontale und vertikale Position eines Zeigers zu erhalten, verwenden Sie Folgendes:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Verwenden Sie das [**makepoints**](/windows/win32/api/wingdi/nf-wingdi-makepoints) -Makro, um den lParam-Parameter in eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur zu konvertieren.

Verwenden Sie die [**getpointerinfo**](/previous-versions/windows/desktop/api) -Funktion, um weitere Informationen abzurufen, die der Nachricht zugeordnet sind.

Verwenden Sie die [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) -Funktion, um die mit dieser Meldung verknüpften Tastatur modifiziererschlüsselzustände zu ermitteln. Um beispielsweise zu erkennen, dass die Alt-Taste gedrückt wurde, überprüfen Sie, ob GetKeyState (VK_MENU) &lt; 0 ist.

Beachten Sie Folgendes: Wenn die Anwendung diese Nachricht nicht verarbeitet, generiert [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) möglicherweise mindestens eine [**WM_GESTURE**](../wintouch/wm-gesture.md) Nachricht, wenn die Sequenz der Eingabe aus diesem und möglicherweise anderen Zeigern als Geste erkannt wird. Wenn eine Geste nicht erkannt wird, generiert **defwindowproc** möglicherweise Maus Eingaben.

Wenn eine Anwendung selektiv eine Zeiger Eingabe verwendet und den Rest an [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergibt, ist das resultierende Verhalten nicht definiert.

Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, werden normalerweise keine weiteren Benachrichtigungen empfangen. Daher ist es wichtig, dass ein Fenster keine Annahmen über den Zeiger Status trifft, unabhängig davon, ob es gleichmäßig gekoppelte nach-oben-oder-nach-oben-Benachrichtigungen empfängt.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)und [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)verwendet werden, um die relevanten Informationen abzurufen, die mit der **WM_POINTERDOWN** Nachricht verknüpft sind.


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



Im folgenden Codebeispiel wird gezeigt, wie [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) verwendet wird, um die Zeiger-ID aus der **WM_POINTERDOWN** Nachricht abzurufen.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



Im folgenden Codebeispiel wird gezeigt, wie unterschiedliche Zeiger Typen wie Finger Eingaben, Pen oder Standard Zeiger behandelt werden.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &amp;pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &amp;touchInfo))
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
    if (!GetPointerPenInfo(pointerId, &amp;penInfo))
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
    if (!GetPointerInfo(pointerId, &amp;pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&amp;pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

**Verweis**
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

 

