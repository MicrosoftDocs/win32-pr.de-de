---
title: WM_LBUTTONDOWN Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die linke Maustaste drückt, während sich der Cursor im Client Bereich eines Fensters befindet.
ms.assetid: 2e43720a-98e6-407a-9430-34c288c3da51
keywords:
- Tastatur-und Maus Eingaben für WM_LBUTTONDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_LBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: c8ac54e813d622f47462b73b763534977ba0932f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367704"
---
# <a name="wm_lbuttondown-message"></a><span data-ttu-id="770df-104">WM- \_ lbuttondown-Meldung</span><span class="sxs-lookup"><span data-stu-id="770df-104">WM\_LBUTTONDOWN message</span></span>

<span data-ttu-id="770df-105">Wird gesendet, wenn der Benutzer die linke Maustaste drückt, während sich der Cursor im Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="770df-105">Posted when the user presses the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="770df-106">Wenn die Maus nicht erfasst wird, wird die Nachricht im Fenster unterhalb des Cursors gepostet.</span><span class="sxs-lookup"><span data-stu-id="770df-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="770df-107">Andernfalls wird die Nachricht an das Fenster gesendet, das die Maus erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="770df-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="770df-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="770df-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDOWN                  0x0201
```



## <a name="parameters"></a><span data-ttu-id="770df-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="770df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="770df-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="770df-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="770df-111">Gibt an, ob verschiedene virtuelle Schlüssel nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="770df-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="770df-112">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="770df-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="770df-113">Wert</span><span class="sxs-lookup"><span data-stu-id="770df-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="770df-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="770df-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="770df-115"><dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="770df-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="770df-116">Die STRG-Taste ist nicht gedrückt.</span><span class="sxs-lookup"><span data-stu-id="770df-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="770df-117"><dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="770df-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="770df-118">Die linke Maustaste ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="770df-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="770df-119"><dt>**MK \_ MButton**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="770df-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="770df-120">Die mittlere Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="770df-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="770df-121"><dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="770df-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="770df-122">Die Rechte Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="770df-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="770df-123"><dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="770df-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="770df-124">Die UMSCHALTTASTE ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="770df-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="770df-125"><dt>**MK \_ XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="770df-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="770df-126">Die erste X-Schaltfläche ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="770df-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="770df-127"><dt>**MK \_ XButton2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="770df-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="770df-128">Die zweite X-Schaltfläche ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="770df-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="770df-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="770df-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="770df-130">Das nieder wertige Wort gibt die x-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="770df-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="770df-131">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="770df-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="770df-132">Das höchst wertige Wort gibt die y-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="770df-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="770df-133">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="770df-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="770df-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="770df-134">Return value</span></span>

<span data-ttu-id="770df-135">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="770df-135">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="770df-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="770df-136">Example</span></span>


```cpp
LRESULT CALLBACK WndProc(_In_ HWND hWnd, _In_ UINT msg, _In_ WPARAM wParam, _In_ LPARAM lParam)
{
    POINT pt;

    switch (msg)
    {

    case WM_LBUTTONDOWN:
            {
                pt.x = GET_X_LPARAM(lParam);
                pt.y = GET_Y_LPARAM(lParam);
            }
        }
        break;

    default:
        return DefWindowProc(hWnd, msg, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="770df-137">Weitere Beispiele finden Sie unter [klassische Windows-Beispiele](https://github.com/microsoft/Windows-classic-samples) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="770df-137">For more examples see [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="770df-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="770df-138">Remarks</span></span>

<span data-ttu-id="770df-139">Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können).</span><span class="sxs-lookup"><span data-stu-id="770df-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="770df-140">Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen.</span><span class="sxs-lookup"><span data-stu-id="770df-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="770df-141">Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="770df-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="770df-142">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="770df-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="770df-143">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="770df-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="770df-144">Um zu erkennen, dass die Alt-Taste gedrückt wurde, überprüfen Sie, ob [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) mit dem **VK- \_ Menü** < 0</span><span class="sxs-lookup"><span data-stu-id="770df-144">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="770df-145">Beachten Sie, dass dies nicht [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate)sein darf.</span><span class="sxs-lookup"><span data-stu-id="770df-145">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="770df-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="770df-146">Requirements</span></span>



| <span data-ttu-id="770df-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="770df-147">Requirement</span></span> | <span data-ttu-id="770df-148">Wert</span><span class="sxs-lookup"><span data-stu-id="770df-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="770df-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="770df-149">Minimum supported client</span></span><br/> | <span data-ttu-id="770df-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="770df-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="770df-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="770df-151">Minimum supported server</span></span><br/> | <span data-ttu-id="770df-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="770df-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="770df-153">Header</span><span class="sxs-lookup"><span data-stu-id="770df-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="770df-154"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="770df-154"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="770df-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="770df-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="770df-156">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="770df-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="770df-157">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="770df-157">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="770df-158">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="770df-158">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="770df-159">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="770df-159">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="770df-160">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="770df-160">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="770df-161">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="770df-161">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="770df-162">**WM \_ lbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="770df-162">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="770df-163">**WM- \_ lbuttonup**</span><span class="sxs-lookup"><span data-stu-id="770df-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="770df-164">**Licher**</span><span class="sxs-lookup"><span data-stu-id="770df-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="770df-165">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="770df-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="770df-166">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="770df-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="770df-167">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="770df-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="770df-168">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="770df-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

