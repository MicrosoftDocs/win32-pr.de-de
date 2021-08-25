---
title: WM_POINTERUPDATE-Nachricht
description: Veröffentlicht, um ein Update für einen Zeiger zur Verfügung zu stellen, der den Kontakt über den Clientbereich eines Fensters hergestellt hat, oder auf einen nicht gekapselten Zeiger, der auf den Clientbereich eines Fensters zeigt.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac222
keywords:
- 'WM_POINTERUPDATE-Nachricht: Eingabemeldungen und Benachrichtigungen'
topic_type:
- apiref
api_name:
- WM_POINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 40c1decbf3c209a381356c58c901c4cab992fadd28eb9566e55e46b1cf87e3d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829510"
---
# <a name="wm_pointerupdate-message"></a>WM_POINTERUPDATE-Nachricht

Veröffentlicht, um ein Update für einen Zeiger zur Verfügung zu stellen, der den Kontakt über den Clientbereich eines Fensters hergestellt hat, oder auf einen nicht gekapselten Zeiger, der auf den Clientbereich eines Fensters zeigt. Während der Zeiger darauf zeigt, richtet sich die Nachricht an das Fenster, über dem sich der Zeiger befindet. Während der Zeiger mit der Oberfläche in Kontakt ist, wird der Zeiger implizit auf das Fenster erfasst, über das der Zeiger kontaktiert wurde, und dieses Fenster erhält weiterhin Eingaben für den Zeiger, bis er den Kontakt unterbricht.

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERUPDATE              0x0245
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält Informationen zum Zeiger. Verwenden Sie die folgenden Makros, um Informationen aus dem wParam-Parameter abzurufen.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Der Zeigerbezeichner.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Meldung die erste Eingabe darstellt, die von einem neuen Zeiger generiert wurde.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Meldung während ihrer Lebensdauer von einem Zeiger generiert wurde. Dieses Flag ist nicht für Meldungen festgelegt, die angeben, dass der Zeiger über einen linken Erkennungsbereich verfügt.
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht von einem Zeiger generiert wurde, der mit der Fensteroberfläche in Kontakt steht. Dieses Flag ist nicht für Meldungen festgelegt, die auf einen Zeigenzeiger zeigen.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Gibt an, dass dieser Zeiger als primär festgelegt wurde.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob es eine primäre Aktion gibt.
    -   Dies entspricht einer linken Maustaste nach unten.
    -   Ein Berührungszeiger hat diese Menge, wenn er mit der Digitizeroberfläche in Kontakt ist.
    -   Ein Stiftzeiger hat diese Menge, wenn er mit der Digitizeroberfläche in Kontakt ist, ohne dass Schaltflächen gedrückt sind.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob es eine sekundäre Aktion gibt.
    -   Dies entspricht einer nach unten gedrückten Maustaste.
    -   Ein Stiftzeiger hat diese Menge, wenn er mit der Digitizeroberfläche in Kontakt ist, während die Stifttaste gedrückt ist.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine oder mehrere tertiäre Aktionen basierend auf dem Zeigertyp durchgeführt werden. -Anwendungen, die auf tertiäre Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, welche Schaltflächen gedrückt werden. Beispielsweise kann eine Anwendung die Schaltflächenzustände eines Stifts bestimmen, indem [**getPointerPenInfo**](/previous-versions/windows/desktop/api) aufruft und die Flags untersucht werden, die Schaltflächenzustände angeben.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob der angegebene Zeiger die vierte Aktion verwendet hat. Anwendungen, die auf vierte Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die erste erweiterte Mausschaltfläche (XButton1) gedrückt wird.
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein [**Flag,**](pointer-flags-contants.md) das angibt, ob der angegebene Zeiger die fünfte Aktion verwendet hat. Anwendungen, die auf fünfte Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die zweite erweiterte Mausschaltfläche (XButton2) gedrückt wird.

    Weitere [**Informationen finden Sie unter Zeigerflags.**](pointer-flags-contants.md)

    > [!Note]  
    > Für einen zeigenden Zeiger ist keines der Schaltflächenflags festgelegt. Dies entspricht einer Mausbewegung, bei der keine Maustaste nach unten bewegt wird. Eine Anwendung kann die Schaltflächenzustände eines Hoverstifts bestimmen, z. B. durch Aufrufen von [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) und Untersuchen der Flags, die Schaltflächenzustände angeben.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich stellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein. Wenn möglich, sollte eine Anwendung die vollständigen Zeigerbereichsinformationen anstelle der Punktposition verwenden.

 

Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): Die x-Koordinate (horizontaler Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): Die y-Koordinate (vertikaler Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Meldung nicht verarbeiten kann, sollte sie [**DefWindowProc aufrufen.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Hinweise

Jeder Zeiger verfügt während seiner Lebensdauer über einen eindeutigen Zeigerbezeichner. Die Lebensdauer eines Zeigers beginnt, wenn er zum ersten Mal erkannt wird.

Eine [**WM_POINTERENTER**](wm-pointerenter.md) wird generiert, wenn ein Zeigenzeiger erkannt wird. Eine [**WM_POINTERDOWN**](wm-pointerdown.md) meldung gefolgt von **einer** WM_POINTERENTER wird generiert, wenn ein zeigerfreier Zeiger erkannt wird.

Während seiner Lebensdauer kann ein Zeiger  eine Reihe von Nachrichten generieren WM_POINTERUPDATE während er darauf oder in Kontakt ist.

Die Lebensdauer eines Zeigers endet, wenn er nicht mehr erkannt wird. Dadurch wird eine [**WM_POINTERLEAVE**](wm-pointerleave.md) generiert.

Wenn ein Zeiger abgebrochen wird, wird [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) festgelegt.

Eine [**WM_POINTERLEAVE**](wm-pointerleave.md) meldung kann auch generiert werden, wenn ein nicht erfasster Zeiger außerhalb der Grenzen eines Fensters bewegt wird.

Um die horizontale und vertikale Position eines Zeigers zu erhalten, verwenden Sie Folgendes:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Das [**MAKEPOINTS-Makro**](/windows/win32/api/wingdi/nf-wingdi-makepoints) kann auch verwendet werden, um den lParam-Parameter in eine [**POINTS-Struktur zu**](/previous-versions//dd162808(v=vs.85)) konvertieren.

Die [**GetKeyState-Funktion**](/windows/win32/api/winuser/nf-winuser-getkeystate) kann verwendet werden, um die Tastenzustände des Tastaturmodifizierers zu bestimmen, die dieser Meldung zugeordnet sind. Um beispielsweise zu erkennen, dass die ALT-TASTE gedrückt wurde, überprüfen Sie, ob **GetKeyState** (VK_MENU) &lt; 0 ist.

Wenn die Anwendung diese Nachricht nicht verarbeiten kann, generiert [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) möglicherweise eine oder mehrere [**WM_GESTURE-Nachrichten,**](../wintouch/wm-gesture.md) wenn die Eingabesequenz von dieser und ggf. andere Zeiger als Geste erkannt wird. Wenn eine Geste nicht erkannt wird, generiert **DefWindowProc möglicherweise** Mauseingaben.

Wenn eine Anwendung selektiv Zeigereingaben verwendet und den Rest an [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergibt, ist das resultierende Verhalten nicht definiert.

Verwenden Sie die [**GetPointerInfo-Funktion,**](/previous-versions/windows/desktop/api) um weitere Informationen zu dieser Nachricht abzurufen.

Wenn die Anwendung diese Nachrichten nicht so schnell wie generiert verarbeiten, können einige Verschiebebewegungen zusammenfingen. Der Verlauf der Eingaben, die in dieser Nachricht zusammengeknaust wurden, kann mit der [**GetPointerInfoHistory-Funktion abgerufen**](/previous-versions/windows/desktop/api) werden.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie Sie GET_X_LPARAM [**,**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)und IS_POINTER_SECONDBUTTON_WPARAM verwenden, um relevante Informationen [**aus**](/previous-versions/windows/desktop/api) den wParam- und lParam-Parametern der WM_POINTERUPDATE **abzurufen.**


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer move while down, similar to mouse move with right button down
}
```



Das folgende Codebeispiel zeigt, wie sie GET_POINTERID_WPARAM, um die [**Zeiger-ID**](/previous-versions/windows/desktop/api) aus dem wParam-Parameter der WM_POINTERUPDATE **abzurufen.**


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



Das folgende Codebeispiel zeigt, wie verschiedene Zeigertypen behandelt werden.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_INPUT_TYPE pointerType = PT_POINTER;

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
        fHandled = HandleGenericPointerInfo(&pointerInfo);
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



## <a name="see-also"></a>Siehe auch

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

 

