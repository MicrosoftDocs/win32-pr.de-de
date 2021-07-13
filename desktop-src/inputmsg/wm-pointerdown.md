---
title: WM_POINTERDOWN Meldung
description: Wird gesendet, wenn ein Zeiger den Kontakt über den Clientbereich eines Fensters annimmt.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN Der Nachrichteneingabenachrichten und -benachrichtigungen
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
ms.openlocfilehash: 9f94bf4474e208d0b1d29df7a5e2939d7826ca77
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689203"
---
# <a name="wm_pointerdown-message"></a><span data-ttu-id="bde54-104">WM_POINTERDOWN Meldung</span><span class="sxs-lookup"><span data-stu-id="bde54-104">WM_POINTERDOWN message</span></span>

<span data-ttu-id="bde54-105">Wird gesendet, wenn ein Zeiger den Kontakt über den Clientbereich eines Fensters annimmt.</span><span class="sxs-lookup"><span data-stu-id="bde54-105">Posted when a pointer makes contact over the client area of a window.</span></span> <span data-ttu-id="bde54-106">Diese Eingabenachricht ist auf das Fenster ausgerichtet, über das der Zeiger Kontakt aufnimmt, und der Zeiger wird implizit auf das Fenster aufgezeichnet, sodass das Fenster weiterhin Eingaben für den Zeiger empfängt, bis er den Kontakt unterbricht.</span><span class="sxs-lookup"><span data-stu-id="bde54-106">This input message targets the window over which the pointer makes contact, and the pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="bde54-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bde54-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="bde54-108">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="bde54-108">\[!Important\]</span></span>  
> <span data-ttu-id="bde54-109">Desktop-Apps sollten DPI-fähige Apps sein.</span><span class="sxs-lookup"><span data-stu-id="bde54-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="bde54-110">Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="bde54-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="bde54-111">Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-fähige Anwendungen sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="bde54-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="bde54-112">Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bde54-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a><span data-ttu-id="bde54-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bde54-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bde54-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bde54-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bde54-115">Enthält Informationen über den Zeiger.</span><span class="sxs-lookup"><span data-stu-id="bde54-115">Contains information about the pointer.</span></span> <span data-ttu-id="bde54-116">Verwenden Sie die folgenden Makros, um Informationen aus dem wParam-Parameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bde54-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="bde54-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): der Zeigerbezeichner.</span><span class="sxs-lookup"><span data-stu-id="bde54-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="bde54-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht die erste Eingabe darstellt, die von einem neuen Zeiger generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bde54-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="bde54-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht während der Lebensdauer von einem Zeiger generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bde54-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="bde54-120">Dieses Flag ist nicht für Meldungen festgelegt, die darauf hinweisen, dass der Zeiger über den linken Erkennungsbereich verfügt.</span><span class="sxs-lookup"><span data-stu-id="bde54-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="bde54-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob diese Nachricht von einem Zeiger generiert wurde, der mit der Fensteroberfläche in Kontakt steht.</span><span class="sxs-lookup"><span data-stu-id="bde54-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="bde54-122">Dieses Flag ist nicht für Nachrichten festgelegt, die auf einen Zeigenzeiger hinweisen.</span><span class="sxs-lookup"><span data-stu-id="bde54-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="bde54-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): gibt an, dass dieser Zeiger als primär festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="bde54-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="bde54-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob eine primäre Aktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bde54-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="bde54-125">Dies entspricht einer linken Maustaste nach unten.</span><span class="sxs-lookup"><span data-stu-id="bde54-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="bde54-126">Für einen Touchzeiger wird dieser festgelegt, wenn er mit der Digitizeroberfläche in Kontakt steht.</span><span class="sxs-lookup"><span data-stu-id="bde54-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="bde54-127">Für einen Stiftzeiger wird diese Einstellung festgelegt, wenn sie ohne Gedrückte Schaltflächen mit der Digitizeroberfläche in Kontakt steht.</span><span class="sxs-lookup"><span data-stu-id="bde54-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="bde54-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob eine sekundäre Aktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bde54-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="bde54-129">Dies entspricht einer Nach-unten-Taste mit der rechten Maustaste.</span><span class="sxs-lookup"><span data-stu-id="bde54-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="bde54-130">Für einen Stiftzeiger wird dieser festgelegt, wenn er mit der Digitizeroberfläche in Kontakt steht und die Stiftschaltfläche gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="bde54-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="bde54-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine oder mehrere tertiäre Aktionen basierend auf dem Zeigertyp vorhanden sind; -Anwendungen, die auf bildungsbezogene Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, auf welche tertiären Schaltflächen gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="bde54-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="bde54-132">Beispielsweise kann eine Anwendung die Schaltflächenzustände eines Stifts bestimmen, indem [**Sie GetPointerPenInfo**](/previous-versions/windows/desktop/api) aufrufen und die Flags untersuchen, die Schaltflächenzustände angeben.</span><span class="sxs-lookup"><span data-stu-id="bde54-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="bde54-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein Flag, das angibt, ob der angegebene Zeiger die vierte Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="bde54-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="bde54-134">Anwendungen, die auf vierte Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die erste erweiterte Mausschaltfläche (XButton1) gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="bde54-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="bde54-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Ein [**Flag,**](pointer-flags-contants.md) das angibt, ob der angegebene Zeiger die fünfte Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="bde54-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="bde54-136">Anwendungen, die auf fünfte Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die zweite erweiterte Maustaste (XButton2) gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="bde54-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="bde54-137">Weitere Informationen finden Sie unter [**Zeigerflags.**](pointer-flags-contants.md)</span><span class="sxs-lookup"><span data-stu-id="bde54-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="bde54-138">Für einen zeigenden Zeiger ist keines der Schaltflächenflags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bde54-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="bde54-139">Dies entspricht einer Mauszeigerbewegung ohne Nach-unten-Maustasten.</span><span class="sxs-lookup"><span data-stu-id="bde54-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="bde54-140">Eine Anwendung kann die Schaltflächenzustände eines Mauszeigers bestimmen, z. B. durch Aufrufen von [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) und Untersuchen der Flags, die Schaltflächenzustände angeben.</span><span class="sxs-lookup"><span data-stu-id="bde54-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="bde54-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bde54-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bde54-142">Enthält die Punktposition des Zeigers.</span><span class="sxs-lookup"><span data-stu-id="bde54-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="bde54-143">Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich herstellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein.</span><span class="sxs-lookup"><span data-stu-id="bde54-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="bde54-144">Wenn möglich, sollte eine Anwendung anstelle der Punktposition die vollständigen Zeigerbereichsinformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bde54-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="bde54-145">Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bde54-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="bde54-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): die x-Koordinate (horizontaler Punkt).</span><span class="sxs-lookup"><span data-stu-id="bde54-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="bde54-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): die y-Koordinate (vertikaler Punkt).</span><span class="sxs-lookup"><span data-stu-id="bde54-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bde54-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bde54-148">Return value</span></span>

<span data-ttu-id="bde54-149">Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bde54-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="bde54-150">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte [**sie DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bde54-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="bde54-151">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bde54-151">Remarks</span></span>

> <span data-ttu-id="bde54-152">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="bde54-152">\[!Important\]</span></span>  
> <span data-ttu-id="bde54-153">Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, empfängt es in der Regel keine weiteren Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="bde54-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="bde54-154">Aus diesem Grund ist es wichtig, dass Sie keine Annahmen basierend auf gleichmäßig gekoppelten **WM_POINTERDOWN** / [**WM_POINTERUP**](wm-pointerup.md) oder [**WM_POINTERENTER**](wm-pointerenter.md) / [**WM_POINTERLEAVE-Benachrichtigungen**](wm-pointerleave.md) treffen.</span><span class="sxs-lookup"><span data-stu-id="bde54-154">For this reason, it is important that you not make any assumptions based on evenly paired **WM_POINTERDOWN**/[**WM_POINTERUP**](wm-pointerup.md) or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="bde54-155">Jeder Zeiger verfügt während seiner Lebensdauer über einen eindeutigen Zeigerbezeichner.</span><span class="sxs-lookup"><span data-stu-id="bde54-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="bde54-156">Die Lebensdauer eines Zeigers beginnt, wenn er zum ersten Mal erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="bde54-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="bde54-157">Eine [**WM_POINTERENTER**](wm-pointerenter.md) Meldung wird generiert, wenn ein Zeiger mit dem Mauszeiger erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="bde54-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="bde54-158">Eine **WM_POINTERDOWN** Nachricht gefolgt von einer **WM_POINTERENTER** Meldung wird generiert, wenn ein Zeiger erkannt wird, der nicht mit dem Mauszeiger zeigt.</span><span class="sxs-lookup"><span data-stu-id="bde54-158">A **WM_POINTERDOWN** message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="bde54-159">Während seiner Lebensdauer kann ein Zeiger eine Reihe von [**WM_POINTERUPDATE**](wm-pointerupdate.md) Nachrichten generieren, während er mit dem Mauszeiger oder im Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="bde54-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="bde54-160">Die Lebensdauer eines Zeigers endet, wenn er nicht mehr erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="bde54-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="bde54-161">Dadurch wird eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Meldung generiert.</span><span class="sxs-lookup"><span data-stu-id="bde54-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="bde54-162">Wenn ein Zeiger abgebrochen wird, wird [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bde54-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="bde54-163">Eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Nachricht kann auch generiert werden, wenn sich ein nicht erfasster Zeiger außerhalb der Grenzen eines Fensters bewegt.</span><span class="sxs-lookup"><span data-stu-id="bde54-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="bde54-164">Um die horizontale und vertikale Position eines Zeigers abzurufen, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bde54-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="bde54-165">Verwenden Sie das [**MAKEPOINTS-Makro,**](/windows/win32/api/wingdi/nf-wingdi-makepoints) um den lParam-Parameter in eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="bde54-165">To convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure, use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro.</span></span>

<span data-ttu-id="bde54-166">Verwenden Sie die [**GetPointerInfo-Funktion,**](/previous-versions/windows/desktop/api) um weitere Der Nachricht zugeordnete Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bde54-166">To retrieve further information associated with the message, use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span>

<span data-ttu-id="bde54-167">Verwenden Sie die [**GetKeyState-Funktion,**](/windows/win32/api/winuser/nf-winuser-getkeystate) um die dieser Meldung zugeordneten Tastenzustände des Tastaturmodifizierer zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bde54-167">To determine the keyboard modifier key states associated with this message, use the [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function.</span></span> <span data-ttu-id="bde54-168">Um beispielsweise zu erkennen, dass die ALT-Taste gedrückt wurde, überprüfen Sie, ob GetKeyState(VK_MENU) &lt; 0 lautet.</span><span class="sxs-lookup"><span data-stu-id="bde54-168">For example, to detect that the ALT key was pressed, check whether GetKeyState(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="bde54-169">Beachten Sie Folgendes: Wenn die Anwendung diese Nachricht nicht verarbeitet, generiert [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) möglicherweise eine oder mehrere [**WM_GESTURE**](../wintouch/wm-gesture.md) Nachrichten, wenn die Sequenz der Eingabe von diesem und möglicherweise anderen Zeigern als Geste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="bde54-169">Note that if the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="bde54-170">Wenn eine Geste nicht erkannt wird, generiert **DefWindowProc** möglicherweise Mauseingaben.</span><span class="sxs-lookup"><span data-stu-id="bde54-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="bde54-171">Wenn eine Anwendung selektiv Zeigereingaben nutzt und den Rest an [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergibt, ist das resultierende Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="bde54-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="bde54-172">Wenn ein Fenster die Erfassung eines Zeigers verliert und die [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Benachrichtigung empfängt, empfängt es in der Regel keine weiteren Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="bde54-172">When a window loses capture of a pointer and receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it will typically not receive any further notifications.</span></span> <span data-ttu-id="bde54-173">Daher ist es wichtig, dass ein Fenster keine Annahmen über seinen Zeigerstatus trifft, unabhängig davon, ob es gleichmäßig gekoppelte DOWN-/UP- oder ENTER/LEAVE-Benachrichtigungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="bde54-173">Therefore, it is important that a window does not make any assumptions of its pointer status, regardless of whether it receives evenly paired DOWN / UP or ENTER / LEAVE notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="bde54-174">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bde54-174">Examples</span></span>

<span data-ttu-id="bde54-175">Das folgende Codebeispiel zeigt, wie [**sie IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)und [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)verwenden, um die relevanten Informationen abzurufen, die der **WM_POINTERDOWN** Nachricht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bde54-175">The following code example shows how to use [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)to retrieve the relevant information associated with the **WM_POINTERDOWN** message.</span></span>


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



<span data-ttu-id="bde54-176">Das folgende Codebeispiel zeigt, wie [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) verwendet wird, um die Zeiger-ID aus der **WM_POINTERDOWN-Nachricht** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bde54-176">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the **WM_POINTERDOWN** message.</span></span>


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



<span data-ttu-id="bde54-177">Das folgende Codebeispiel zeigt, wie verschiedene Zeigertypen wie Toucheingaben, Stifte oder Standardzeigergeräte behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="bde54-177">The following code example shows how to handle different pointer type such as touch, pen, or default pointing devices.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bde54-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bde54-178">Requirements</span></span>



| <span data-ttu-id="bde54-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bde54-179">Requirement</span></span> | <span data-ttu-id="bde54-180">Wert</span><span class="sxs-lookup"><span data-stu-id="bde54-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde54-181">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bde54-181">Minimum supported client</span></span><br/> | <span data-ttu-id="bde54-182">\[Windows 8 Nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bde54-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="bde54-183">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bde54-183">Minimum supported server</span></span><br/> | <span data-ttu-id="bde54-184">\[Windows Server 2012 Nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bde54-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bde54-185">Header</span><span class="sxs-lookup"><span data-stu-id="bde54-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde54-186"><dt>Winuser.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="bde54-186"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde54-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bde54-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde54-188">Meldungen</span><span class="sxs-lookup"><span data-stu-id="bde54-188">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="bde54-189">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="bde54-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bde54-190">**Zeigerflags**</span><span class="sxs-lookup"><span data-stu-id="bde54-190">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="bde54-191">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-191">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-192">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-192">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-193">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-193">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-194">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-194">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-195">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-195">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="bde54-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="bde54-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>
