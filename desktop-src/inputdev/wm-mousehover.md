---
title: WM_MOUSEHOVER Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, wenn der Cursor für den Zeitraum, der in einem vorherigen Aufruf von TrackMouseEvent angegeben ist, auf den Client Bereich des Fensters zeigt.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSEHOVER Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65747ade6bd2ec9456281ac02711de18675a411e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476146"
---
# <a name="wm_mousehover-message"></a><span data-ttu-id="720cf-104">WM- \_ moupagehover-Meldung</span><span class="sxs-lookup"><span data-stu-id="720cf-104">WM\_MOUSEHOVER message</span></span>

<span data-ttu-id="720cf-105">Wird an ein Fenster gesendet, wenn der Cursor für den Zeitraum, der in einem vorherigen Aufruf von [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegeben ist, auf den Client Bereich des Fensters zeigt.</span><span class="sxs-lookup"><span data-stu-id="720cf-105">Posted to a window when the cursor hovers over the client area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="720cf-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="720cf-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a><span data-ttu-id="720cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="720cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720cf-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="720cf-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="720cf-109">Gibt an, ob verschiedene virtuelle Schlüssel nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="720cf-109">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="720cf-110">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="720cf-110">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="720cf-111">Wert</span><span class="sxs-lookup"><span data-stu-id="720cf-111">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="720cf-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="720cf-112">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="720cf-113"><dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-113"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="720cf-114">Die STRG-Taste ist gedrückt.</span><span class="sxs-lookup"><span data-stu-id="720cf-114">The CTRL key is depressed.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="720cf-115"><dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-115"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="720cf-116">Die linke Maustaste ist gedrückt.</span><span class="sxs-lookup"><span data-stu-id="720cf-116">The left mouse button is depressed.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="720cf-117"><dt>**MK \_ MButton**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="720cf-118">Die mittlere Maustaste ist gedrückt.</span><span class="sxs-lookup"><span data-stu-id="720cf-118">The middle mouse button is depressed.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="720cf-119"><dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="720cf-120">Die Rechte Maustaste ist gedrückt.</span><span class="sxs-lookup"><span data-stu-id="720cf-120">The right mouse button is depressed.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="720cf-121"><dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="720cf-122">Die UMSCHALTTASTE ist gedrückt.</span><span class="sxs-lookup"><span data-stu-id="720cf-122">The SHIFT key is depressed.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="720cf-123"><dt>**MK \_ XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="720cf-124">Die erste X-Schaltfläche ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="720cf-124">The first X button is down.</span></span><br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="720cf-125"><dt>**MK \_ XButton2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="720cf-126">Die zweite X-Schaltfläche ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="720cf-126">The second X button is down.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="720cf-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="720cf-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="720cf-128">Das nieder wertige Wort gibt die x-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="720cf-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="720cf-129">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="720cf-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="720cf-130">Das höchst wertige Wort gibt die y-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="720cf-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="720cf-131">Die Koordinate ist relativ zur oberen linken Ecke des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="720cf-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720cf-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="720cf-132">Return value</span></span>

<span data-ttu-id="720cf-133">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="720cf-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="720cf-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="720cf-134">Remarks</span></span>

<span data-ttu-id="720cf-135">Die Hover-Nachverfolgung wird beendet, wenn **WM- \_ moupagehover** generiert wird</span><span class="sxs-lookup"><span data-stu-id="720cf-135">Hover tracking stops when **WM\_MOUSEHOVER** is generated.</span></span> <span data-ttu-id="720cf-136">Die Anwendung muss [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) erneut aufrufen, wenn Sie eine weitere Nachverfolgung des Mauszeiger Verhaltens erfordert.</span><span class="sxs-lookup"><span data-stu-id="720cf-136">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="720cf-137">Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:</span><span class="sxs-lookup"><span data-stu-id="720cf-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="720cf-138">Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können).</span><span class="sxs-lookup"><span data-stu-id="720cf-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="720cf-139">Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen.</span><span class="sxs-lookup"><span data-stu-id="720cf-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="720cf-140">Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="720cf-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="720cf-141">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="720cf-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="720cf-142">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="720cf-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="720cf-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="720cf-143">Requirements</span></span>



| <span data-ttu-id="720cf-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="720cf-144">Requirement</span></span> | <span data-ttu-id="720cf-145">Wert</span><span class="sxs-lookup"><span data-stu-id="720cf-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="720cf-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="720cf-146">Minimum supported client</span></span><br/> | <span data-ttu-id="720cf-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="720cf-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="720cf-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="720cf-148">Minimum supported server</span></span><br/> | <span data-ttu-id="720cf-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="720cf-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="720cf-150">Header</span><span class="sxs-lookup"><span data-stu-id="720cf-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="720cf-151"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="720cf-151"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="720cf-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="720cf-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="720cf-153">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="720cf-153">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="720cf-154">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="720cf-154">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="720cf-155">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="720cf-155">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="720cf-156">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="720cf-156">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="720cf-157">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="720cf-157">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="720cf-158">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="720cf-158">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="720cf-159">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="720cf-159">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

<span data-ttu-id="720cf-160">**Licher**</span><span class="sxs-lookup"><span data-stu-id="720cf-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="720cf-161">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="720cf-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="720cf-162">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="720cf-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="720cf-163">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="720cf-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="720cf-164">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="720cf-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

