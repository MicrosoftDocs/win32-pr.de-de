---
title: WM_POINTERUPDATE Meldung
description: Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den Client Bereich eines Fensters hergestellt hat, oder auf einem nicht aufgezeichneten Zeiger, der auf den Client Bereich eines Fensters zeigt.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac222
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERUPDATE Nachricht
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
ms.openlocfilehash: 215874f4dc1b3438ae3d69b22758ced09a050f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106311"
---
# <a name="wm_pointerupdate-message"></a><span data-ttu-id="97aa4-104">WM_POINTERUPDATE Meldung</span><span class="sxs-lookup"><span data-stu-id="97aa4-104">WM_POINTERUPDATE message</span></span>

<span data-ttu-id="97aa4-105">Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den Client Bereich eines Fensters hergestellt hat, oder auf einem nicht aufgezeichneten Zeiger, der auf den Client Bereich eines Fensters zeigt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-105">Posted to provide an update on a pointer that made contact over the client area of a window or on a hovering uncaptured pointer over the client area of a window.</span></span> <span data-ttu-id="97aa4-106">Während der Mauszeiger bewegt wird, wird die Nachricht auf das Fenster ausgerichtet, über das sich der Zeiger befindet.</span><span class="sxs-lookup"><span data-stu-id="97aa4-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="97aa4-107">Während sich der Mauszeiger auf der-Oberfläche befindet, wird der Zeiger implizit in dem Fenster erfasst, über das der Zeiger den Kontakt hergestellt hat, und dieses Fenster empfängt weiterhin Eingaben für den Zeiger, bis der Kontakt unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

> <span data-ttu-id="97aa4-108">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="97aa4-108">\[!Important\]</span></span>  
> <span data-ttu-id="97aa4-109">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="97aa4-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="97aa4-110">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="97aa4-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="97aa4-111">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="97aa4-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="97aa4-112">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="97aa4-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERUPDATE              0x0245
```



## <a name="parameters"></a><span data-ttu-id="97aa4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="97aa4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97aa4-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97aa4-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97aa4-115">Enthält Informationen über den-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="97aa4-115">Contains information about the pointer.</span></span> <span data-ttu-id="97aa4-116">Verwenden Sie die folgenden Makros zum Abrufen von Informationen aus dem wParam-Parameter.</span><span class="sxs-lookup"><span data-stu-id="97aa4-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="97aa4-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): der Zeiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="97aa4-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="97aa4-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob diese Meldung die erste Eingabe darstellt, die von einem neuen Zeiger generiert wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="97aa4-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob diese Meldung während ihrer Lebensdauer von einem Zeiger generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="97aa4-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="97aa4-120">Dieses Flag ist für Meldungen, die darauf hinweisen, dass der Zeiger den linken Erkennungsbereich aufweist, nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="97aa4-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob diese Meldung von einem Zeiger generiert wurde, der sich in Verbindung mit der Fenster Oberfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="97aa4-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="97aa4-122">Dieses Flag ist nicht für Meldungen festgelegt, die einen Mauszeiger angeben.</span><span class="sxs-lookup"><span data-stu-id="97aa4-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="97aa4-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): gibt an, dass dieser Zeiger als primär festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="97aa4-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="97aa4-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine primäre Aktion vorliegt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="97aa4-125">Dies ist analog zu einer mouseleft-Schaltfläche nach unten.</span><span class="sxs-lookup"><span data-stu-id="97aa4-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="97aa4-126">Ein Fingerabdruck wird festgelegt, wenn er sich mit der digitalisiereroberfläche in Verbindung setzt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="97aa4-127">Bei einem Stift Zeiger wird dieser Satz festgelegt, wenn er sich auf der digitalisiereroberfläche befindet und keine Schaltflächen gedrückt sind.</span><span class="sxs-lookup"><span data-stu-id="97aa4-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="97aa4-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine sekundäre Aktion vorliegt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="97aa4-129">Dies ist analog zu einer Maustaste nach unten.</span><span class="sxs-lookup"><span data-stu-id="97aa4-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="97aa4-130">Bei einem Stift Zeiger wird dieser Satz festgelegt, wenn er sich im Kontakt mit der Digitalisierungs Oberfläche befindet, auf die die Stift Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="97aa4-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob eine oder mehrere tertiäre Aktionen auf Grundlage des Zeiger Typs vorhanden sind. Anwendungen, die auf tertiäre Aktionen reagieren möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, welche tertiären Schaltflächen gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="97aa4-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="97aa4-132">Eine Anwendung kann z. b. die Schaltflächen Zustände eines Stifts ermitteln, indem [**getpointerpeninfo**](/previous-versions/windows/desktop/api) aufgerufen und die Flags untersucht werden, die Schaltflächen Zustände angeben.</span><span class="sxs-lookup"><span data-stu-id="97aa4-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="97aa4-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein Flag, das angibt, ob der angegebene Zeiger die vierte Aktion gedauert hat.</span><span class="sxs-lookup"><span data-stu-id="97aa4-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="97aa4-134">Anwendungen, die auf vierte Aktionen antworten möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die erste erweiterte Maus Taste (XButton1) gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="97aa4-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="97aa4-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): ein [**Flag**](pointer-flags-contants.md) , das angibt, ob der angegebene Zeiger eine fünfte Aktion gedauert hat.</span><span class="sxs-lookup"><span data-stu-id="97aa4-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="97aa4-136">Anwendungen, die auf fünfte Aktionen antworten möchten, müssen spezifische Informationen für den Zeigertyp abrufen, um zu bestimmen, ob die zweite Schaltfläche mit der erweiterten Maus (XButton2) gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="97aa4-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="97aa4-137">Weitere Informationen finden Sie unter [**Zeiger-Flags**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="97aa4-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="97aa4-138">Für einen Mauszeiger ist keines der schaltflächenflags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="97aa4-139">Dies ist analog zu einer Mausbewegung ohne die Maustasten.</span><span class="sxs-lookup"><span data-stu-id="97aa4-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="97aa4-140">Eine Anwendung kann die Schaltflächen Zustände eines Maus zeigenden Stifts ermitteln, z. b. durch Aufrufen von [**getpointerpeninfo**](/previous-versions/windows/desktop/api) und untersuchen der Flags, die Schaltflächen Zustände angeben.</span><span class="sxs-lookup"><span data-stu-id="97aa4-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="97aa4-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97aa4-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97aa4-142">Enthält die Punktposition des Zeigers.</span><span class="sxs-lookup"><span data-stu-id="97aa4-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="97aa4-143">Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="97aa4-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="97aa4-144">Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="97aa4-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="97aa4-145">Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.</span><span class="sxs-lookup"><span data-stu-id="97aa4-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="97aa4-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).</span><span class="sxs-lookup"><span data-stu-id="97aa4-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="97aa4-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).</span><span class="sxs-lookup"><span data-stu-id="97aa4-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97aa4-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97aa4-148">Return value</span></span>

<span data-ttu-id="97aa4-149">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="97aa4-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="97aa4-150">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="97aa4-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="97aa4-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97aa4-151">Remarks</span></span>

<span data-ttu-id="97aa4-152">Jeder Zeiger hat während seiner Lebensdauer einen eindeutigen Zeiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="97aa4-152">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="97aa4-153">Die Lebensdauer eines Zeigers beginnt, wenn er erstmals erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-153">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="97aa4-154">Eine [**WM_POINTERENTER**](wm-pointerenter.md) Meldung wird generiert, wenn ein Mauszeiger erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-154">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="97aa4-155">Eine [**WM_POINTERDOWN**](wm-pointerdown.md) Meldung, auf die eine **WM_POINTERENTER** Meldung folgt, wird generiert, wenn ein nicht Mauszeiger erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-155">A [**WM_POINTERDOWN**](wm-pointerdown.md) message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="97aa4-156">Während der Lebensdauer kann ein Zeiger eine Reihe von **WM_POINTERUPDATE** Meldungen generieren, während er darauf zeigt oder in Kontakt steht.</span><span class="sxs-lookup"><span data-stu-id="97aa4-156">During its lifetime, a pointer may generate a series of **WM_POINTERUPDATE** messages while it is hovering or in contact.</span></span>

<span data-ttu-id="97aa4-157">Die Lebensdauer eines Zeigers endet, wenn er nicht mehr erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-157">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="97aa4-158">Dadurch wird eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Nachricht generiert.</span><span class="sxs-lookup"><span data-stu-id="97aa4-158">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="97aa4-159">Wenn ein Zeiger abgebrochen wird, wird [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-159">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="97aa4-160">Eine [**WM_POINTERLEAVE**](wm-pointerleave.md) Meldung kann auch generiert werden, wenn ein nicht erfasster Zeiger außerhalb der Begrenzungen eines Fensters bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-160">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="97aa4-161">Um die horizontale und vertikale Position eines Zeigers zu erhalten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97aa4-161">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="97aa4-162">Das [**makepoints**](/windows/win32/api/wingdi/nf-wingdi-makepoints) -Makro kann auch verwendet werden, um den lParam-Parameter in eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="97aa4-162">The [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro can also be used to convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="97aa4-163">Die [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) -Funktion kann verwendet werden, um die mit dieser Meldung verknüpften Tastatur-modifiziererschlüsselzustände zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="97aa4-163">The [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function can be used to determine the keyboard modifier key states associated with this message.</span></span> <span data-ttu-id="97aa4-164">Um beispielsweise zu erkennen, dass die Alt-Taste gedrückt wurde, überprüfen Sie, ob **GetKeyState** (VK_MENU) &lt; 0 ist.</span><span class="sxs-lookup"><span data-stu-id="97aa4-164">For example, to detect that the ALT key was pressed, check whether **GetKeyState** (VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="97aa4-165">Wenn die Anwendung diese Nachricht nicht verarbeitet, generiert [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) möglicherweise eine oder mehrere [**WM_GESTURE**](../wintouch/wm-gesture.md) Meldungen, wenn die Sequenz der Eingaben aus diesem und möglicherweise anderen Zeigern als Geste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="97aa4-165">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="97aa4-166">Wenn eine Geste nicht erkannt wird, generiert **defwindowproc** möglicherweise Maus Eingaben.</span><span class="sxs-lookup"><span data-stu-id="97aa4-166">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="97aa4-167">Wenn eine Anwendung selektiv eine Zeiger Eingabe verwendet und den Rest an [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergibt, ist das resultierende Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="97aa4-167">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="97aa4-168">Verwenden Sie die [**getpointerinfo**](/previous-versions/windows/desktop/api) -Funktion, um weitere Informationen zu dieser Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="97aa4-168">Use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function to retrieve further information related to this message.</span></span>

<span data-ttu-id="97aa4-169">Wenn die Anwendung diese Nachrichten nicht so schnell verarbeitet, wie Sie generiert werden, werden möglicherweise einige Verschiebungen zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="97aa4-169">If the application does not process these messages as fast as they are generated, some moves may be coalesced.</span></span> <span data-ttu-id="97aa4-170">Der Verlauf von Eingaben, die in diese Nachricht zusammengerufen wurden, kann mit der [**getpointerinfohistory**](/previous-versions/windows/desktop/api) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="97aa4-170">The history of inputs that were coalesced into this message can be retrieved using the [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) function.</span></span>

## <a name="examples"></a><span data-ttu-id="97aa4-171">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97aa4-171">Examples</span></span>

<span data-ttu-id="97aa4-172">Im folgenden Codebeispiel wird gezeigt, wie [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)und [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) verwendet werden, um relevante Informationen aus den wParam-und lParam-Parametern der **WM_POINTERUPDATE** Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="97aa4-172">The following code example shows how to use [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) to retrieve relevant information from the wParam and lParam parameters of the **WM_POINTERUPDATE** message.</span></span>


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



<span data-ttu-id="97aa4-173">Im folgenden Codebeispiel wird gezeigt, wie [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) verwendet wird, um die Zeiger-ID aus dem wParam-Parameter der **WM_POINTERUPDATE** Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="97aa4-173">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the wParam parameter of the **WM_POINTERUPDATE** message.</span></span>


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



<span data-ttu-id="97aa4-174">Im folgenden Codebeispiel wird gezeigt, wie unterschiedliche Zeiger Typen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="97aa4-174">The following code example shows how to handle different pointer types.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="97aa4-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97aa4-175">Requirements</span></span>



| <span data-ttu-id="97aa4-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97aa4-176">Requirement</span></span> | <span data-ttu-id="97aa4-177">Wert</span><span class="sxs-lookup"><span data-stu-id="97aa4-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97aa4-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97aa4-178">Minimum supported client</span></span><br/> | <span data-ttu-id="97aa4-179">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97aa4-179">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="97aa4-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97aa4-180">Minimum supported server</span></span><br/> | <span data-ttu-id="97aa4-181">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97aa4-181">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97aa4-182">Header</span><span class="sxs-lookup"><span data-stu-id="97aa4-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="97aa4-183"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="97aa4-183"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97aa4-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97aa4-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97aa4-185">Meldungen</span><span class="sxs-lookup"><span data-stu-id="97aa4-185">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="97aa4-186">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="97aa4-186">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97aa4-187">**Zeigerflags**</span><span class="sxs-lookup"><span data-stu-id="97aa4-187">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="97aa4-188">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-188">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-189">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-189">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-190">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-190">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-191">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-191">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-192">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-192">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-193">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-193">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-194">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-194">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-195">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-195">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-196">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-196">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="97aa4-197">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="97aa4-197">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

