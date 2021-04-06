---
title: WM_XBUTTONDBLCLK Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf die erste oder zweite X-Schaltfläche doppelklickt, während sich der Cursor im Client Bereich eines Fensters befindet.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- Tastatur-und Maus Eingaben für WM_XBUTTONDBLCLK Nachricht
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed0612c2850f784901f01313935145fc9d3d7910
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742344"
---
# <a name="wm_xbuttondblclk-message"></a><span data-ttu-id="c95a5-104">WM- \_ xbuttondblclk-Meldung</span><span class="sxs-lookup"><span data-stu-id="c95a5-104">WM\_XBUTTONDBLCLK message</span></span>

<span data-ttu-id="c95a5-105">Wird gesendet, wenn der Benutzer auf die erste oder zweite X-Schaltfläche doppelklickt, während sich der Cursor im Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="c95a5-105">Posted when the user double-clicks the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="c95a5-106">Wenn die Maus nicht erfasst wird, wird die Nachricht im Fenster unterhalb des Cursors gepostet.</span><span class="sxs-lookup"><span data-stu-id="c95a5-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="c95a5-107">Andernfalls wird die Nachricht an das Fenster gesendet, das die Maus erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="c95a5-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="c95a5-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c95a5-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a><span data-ttu-id="c95a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c95a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c95a5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c95a5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c95a5-111">Das nieder wertige Wort gibt an, ob verschiedene virtuelle Schlüssel ausfallen.</span><span class="sxs-lookup"><span data-stu-id="c95a5-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="c95a5-112">Es kann sich um einen oder mehrere der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="c95a5-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="c95a5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c95a5-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="c95a5-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c95a5-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="c95a5-115"><dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="c95a5-116">Die STRG-Taste ist nicht gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="c95a5-117"><dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="c95a5-118">Die linke Maustaste ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c95a5-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="c95a5-119"><dt>**MK \_ MButton**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="c95a5-120">Die mittlere Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="c95a5-121"><dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="c95a5-122">Die Rechte Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="c95a5-123"><dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="c95a5-124">Die UMSCHALTTASTE ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="c95a5-125"><dt>**MK \_ XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="c95a5-126">Die erste X-Schaltfläche ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="c95a5-127"><dt>**MK \_ XButton2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="c95a5-128">Die zweite X-Schaltfläche ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="c95a5-129">Das höchst wertige Wort gibt an, auf welche Schaltfläche Doppel geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="c95a5-129">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="c95a5-130">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c95a5-130">It can be one of the following values.</span></span>



| <span data-ttu-id="c95a5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c95a5-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="c95a5-132">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c95a5-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="c95a5-133"><dt>**XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="c95a5-134">Es wurde auf die erste X-Schaltfläche Doppel geklickt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-134">The first X button was double-clicked.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="c95a5-135"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="c95a5-136">Auf die zweite X-Schaltfläche wurde Doppel geklickt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-136">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c95a5-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c95a5-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c95a5-138">Das nieder wertige Wort gibt die x-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="c95a5-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="c95a5-139">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c95a5-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="c95a5-140">Das höchst wertige Wort gibt die y-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="c95a5-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="c95a5-141">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c95a5-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c95a5-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c95a5-142">Return value</span></span>

<span data-ttu-id="c95a5-143">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c95a5-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="c95a5-144">Weitere Informationen zum Verarbeiten des Rückgabewerts finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="c95a5-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="c95a5-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c95a5-145">Remarks</span></span>

<span data-ttu-id="c95a5-146">Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c95a5-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="c95a5-147">Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:</span><span class="sxs-lookup"><span data-stu-id="c95a5-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="c95a5-148">Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können).</span><span class="sxs-lookup"><span data-stu-id="c95a5-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="c95a5-149">Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen.</span><span class="sxs-lookup"><span data-stu-id="c95a5-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="c95a5-150">Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c95a5-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c95a5-151">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c95a5-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="c95a5-152">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="c95a5-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="c95a5-153">Nur Fenster, die den **CS \_ dblclks** -Stil aufweisen, können **WM- \_ xbuttondblclk** -Nachrichten empfangen, die das System generiert, wenn der Benutzer eine X-Schaltfläche im Doppelklick-Zeit Limit des Systems drückt, loslässt und erneut drückt.</span><span class="sxs-lookup"><span data-stu-id="c95a5-153">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_XBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="c95a5-154">Durch Doppelklicken auf eine dieser Schaltflächen werden tatsächlich vier Meldungen generiert: " [**WM \_ xbuttondown**](wm-xbuttondown.md)", " [**WM \_ xbuttonup**](wm-xbuttonup.md)", " **WM \_ xbuttondblclk**" und " **WM \_ xbuttonup** ".</span><span class="sxs-lookup"><span data-stu-id="c95a5-154">Double-clicking one of these buttons actually generates four messages: [**WM\_XBUTTONDOWN**](wm-xbuttondown.md), [**WM\_XBUTTONUP**](wm-xbuttonup.md), **WM\_XBUTTONDBLCLK**, and **WM\_XBUTTONUP** again.</span></span>

<span data-ttu-id="c95a5-155">Im Gegensatz zu den Nachrichten [**WM \_ lbuttondblclk**](wm-lbuttondblclk.md), [**WM \_ mbuttondblclk**](wm-mbuttondblclk.md)und [**WM \_ rbuttondblclk**](wm-rbuttondblclk.md) sollte eine Anwendung bei der Verarbeitung von dieser Nachricht **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c95a5-155">Unlike the [**WM\_LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM\_MBUTTONDBLCLK**](wm-mbuttondblclk.md), and [**WM\_RBUTTONDBLCLK**](wm-rbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="c95a5-156">Auf diese Weise kann Software, die diese Meldung auf Windows-Systemen vor Windows 2000 simuliert, ermitteln, ob die Fenster Prozedur die Nachricht verarbeitet hat oder [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c95a5-156">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c95a5-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c95a5-157">Requirements</span></span>



| <span data-ttu-id="c95a5-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c95a5-158">Requirement</span></span> | <span data-ttu-id="c95a5-159">Wert</span><span class="sxs-lookup"><span data-stu-id="c95a5-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c95a5-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c95a5-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c95a5-161">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c95a5-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c95a5-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c95a5-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c95a5-163">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c95a5-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c95a5-164">Header</span><span class="sxs-lookup"><span data-stu-id="c95a5-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="c95a5-165"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c95a5-165"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c95a5-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c95a5-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="c95a5-167">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c95a5-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c95a5-168">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c95a5-168">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c95a5-169">**\_KeyState- \_ wParam-Element**</span><span class="sxs-lookup"><span data-stu-id="c95a5-169">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="c95a5-170">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c95a5-170">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="c95a5-171">**\_XButton- \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="c95a5-171">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="c95a5-172">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c95a5-172">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="c95a5-173">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="c95a5-173">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="c95a5-174">**Getdoubleclicktime**</span><span class="sxs-lookup"><span data-stu-id="c95a5-174">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="c95a5-175">**Setdoubleclicktime**</span><span class="sxs-lookup"><span data-stu-id="c95a5-175">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="c95a5-176">**WM- \_ xbuttondown**</span><span class="sxs-lookup"><span data-stu-id="c95a5-176">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

[<span data-ttu-id="c95a5-177">**WM- \_ xbuttonup**</span><span class="sxs-lookup"><span data-stu-id="c95a5-177">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)
</dt> <dt>

<span data-ttu-id="c95a5-178">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c95a5-178">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c95a5-179">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="c95a5-179">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="c95a5-180">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c95a5-180">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c95a5-181">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="c95a5-181">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="c95a5-182">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c95a5-182">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

