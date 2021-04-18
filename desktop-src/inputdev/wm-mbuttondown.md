---
title: WM_MBUTTONDOWN Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die mittlere Maustaste drückt, während sich der Cursor im Client Bereich eines Fensters befindet.
ms.assetid: 5181a425-2577-4806-8926-1075a1a756ee
keywords:
- Tastatur-und Maus Eingaben für WM_MBUTTONDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_MBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0f7ce257dd50ad16eda3c13feef73890fbbfd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340994"
---
# <a name="wm_mbuttondown-message"></a><span data-ttu-id="4a228-104">WM- \_ mbuttondown-Meldung</span><span class="sxs-lookup"><span data-stu-id="4a228-104">WM\_MBUTTONDOWN message</span></span>

<span data-ttu-id="4a228-105">Wird gesendet, wenn der Benutzer die mittlere Maustaste drückt, während sich der Cursor im Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="4a228-105">Posted when the user presses the middle mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="4a228-106">Wenn die Maus nicht erfasst wird, wird die Nachricht im Fenster unterhalb des Cursors gepostet.</span><span class="sxs-lookup"><span data-stu-id="4a228-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="4a228-107">Andernfalls wird die Nachricht an das Fenster gesendet, das die Maus erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="4a228-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="4a228-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4a228-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MBUTTONDOWN                  0x0207
```



## <a name="parameters"></a><span data-ttu-id="4a228-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a228-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a228-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a228-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a228-111">Gibt an, ob verschiedene virtuelle Schlüssel nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a228-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="4a228-112">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4a228-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="4a228-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4a228-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="4a228-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4a228-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="4a228-115"><dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="4a228-116">Die STRG-Taste ist nicht gedrückt.</span><span class="sxs-lookup"><span data-stu-id="4a228-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="4a228-117"><dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="4a228-118">Die linke Maustaste ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4a228-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="4a228-119"><dt>**MK \_ MButton**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="4a228-120">Die mittlere Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a228-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="4a228-121"><dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="4a228-122">Die Rechte Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a228-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="4a228-123"><dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="4a228-124">Die UMSCHALTTASTE ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a228-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="4a228-125"><dt>**MK \_ XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="4a228-126">Die erste X-Schaltfläche ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a228-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="4a228-127"><dt>**MK \_ XButton2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="4a228-128">Die zweite X-Schaltfläche ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a228-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="4a228-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a228-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a228-130">Das nieder wertige Wort gibt die x-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="4a228-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="4a228-131">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="4a228-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="4a228-132">Das höchst wertige Wort gibt die y-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="4a228-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="4a228-133">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="4a228-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a228-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a228-134">Return value</span></span>

<span data-ttu-id="4a228-135">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4a228-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a228-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a228-136">Remarks</span></span>

<span data-ttu-id="4a228-137">Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:</span><span class="sxs-lookup"><span data-stu-id="4a228-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="4a228-138">Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können).</span><span class="sxs-lookup"><span data-stu-id="4a228-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="4a228-139">Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen.</span><span class="sxs-lookup"><span data-stu-id="4a228-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="4a228-140">Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="4a228-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a228-141">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4a228-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="4a228-142">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="4a228-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="4a228-143">Um zu erkennen, dass die Alt-Taste gedrückt wurde, überprüfen Sie, ob [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) mit dem **VK- \_ Menü** < 0</span><span class="sxs-lookup"><span data-stu-id="4a228-143">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="4a228-144">Beachten Sie, dass dies nicht [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate)sein darf.</span><span class="sxs-lookup"><span data-stu-id="4a228-144">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a228-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a228-145">Requirements</span></span>



| <span data-ttu-id="4a228-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a228-146">Requirement</span></span> | <span data-ttu-id="4a228-147">Wert</span><span class="sxs-lookup"><span data-stu-id="4a228-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a228-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a228-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4a228-149">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a228-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4a228-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a228-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4a228-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a228-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4a228-152">Header</span><span class="sxs-lookup"><span data-stu-id="4a228-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a228-153"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a228-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a228-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a228-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a228-155">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="4a228-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a228-156">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="4a228-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="4a228-157">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="4a228-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="4a228-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="4a228-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="4a228-159">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="4a228-159">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="4a228-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="4a228-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="4a228-161">**WM- \_ mbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="4a228-161">**WM\_MBUTTONDBLCLK**</span></span>](wm-mbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="4a228-162">**WM- \_ mbuttonup**</span><span class="sxs-lookup"><span data-stu-id="4a228-162">**WM\_MBUTTONUP**</span></span>](wm-mbuttonup.md)
</dt> <dt>

<span data-ttu-id="4a228-163">**Licher**</span><span class="sxs-lookup"><span data-stu-id="4a228-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4a228-164">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="4a228-164">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="4a228-165">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="4a228-165">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4a228-166">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="4a228-166">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="4a228-167">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a228-167">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

