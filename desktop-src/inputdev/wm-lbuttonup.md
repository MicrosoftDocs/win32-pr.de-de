---
title: WM_LBUTTONUP Meldung (Winuser.h)
description: Wird gesendet, wenn der Benutzer die linke Maustaste freigibt, während sich der Cursor im Clientbereich eines Fensters befindet.
ms.assetid: 6efa298f-85f7-40ab-a64b-16b5071f2437
keywords:
- WM_LBUTTONUP Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_LBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe921ffe68359efe15aa0782c5c8543fd0870fa
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335394"
---
# <a name="wm_lbuttonup-message"></a><span data-ttu-id="1e13b-104">\_WM-LBUTTONUP-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1e13b-104">WM\_LBUTTONUP message</span></span>

<span data-ttu-id="1e13b-105">Wird gesendet, wenn der Benutzer die linke Maustaste freigibt, während sich der Cursor im Clientbereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="1e13b-105">Posted when the user releases the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="1e13b-106">Wenn die Maus nicht erfasst wird, wird die Meldung an das Fenster unterhalb des Cursors gesendet.</span><span class="sxs-lookup"><span data-stu-id="1e13b-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="1e13b-107">Andernfalls wird die Nachricht an das Fenster gesendet, in dem die Maus erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="1e13b-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="1e13b-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e13b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONUP                    0x0202
```



## <a name="parameters"></a><span data-ttu-id="1e13b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e13b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e13b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e13b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e13b-111">Gibt an, ob verschiedene virtuelle Schlüssel ausgeschaltet sind.</span><span class="sxs-lookup"><span data-stu-id="1e13b-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="1e13b-112">Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="1e13b-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1e13b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1e13b-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="1e13b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e13b-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="1e13b-115"><dt>**MK \_ CONTROL**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="1e13b-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="1e13b-116">Die STRG-TASTE ist gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e13b-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="1e13b-117"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="1e13b-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="1e13b-118">Die mittlere Maustaste ist gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e13b-118">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="1e13b-119"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="1e13b-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="1e13b-120">Die rechte Maustaste ist nach unten geschaltet.</span><span class="sxs-lookup"><span data-stu-id="1e13b-120">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="1e13b-121"><dt>**MK \_ UMSCHALT**</dt> <dt>0X0004</dt></span><span class="sxs-lookup"><span data-stu-id="1e13b-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="1e13b-122">Die UMSCHALTTASTE ist nicht mehr gedrückt.</span><span class="sxs-lookup"><span data-stu-id="1e13b-122">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="1e13b-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="1e13b-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="1e13b-124">Die erste X-Schaltfläche ist ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="1e13b-124">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="1e13b-125"><dt>**MK \_ XBUTTON2-0x0040**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e13b-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="1e13b-126">Die zweite X-Schaltfläche ist nicht mehr zu sehen.</span><span class="sxs-lookup"><span data-stu-id="1e13b-126">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="1e13b-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e13b-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e13b-128">Das niedrige Wort gibt die x-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="1e13b-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="1e13b-129">Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.</span><span class="sxs-lookup"><span data-stu-id="1e13b-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="1e13b-130">Das obere Wort gibt die y-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="1e13b-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="1e13b-131">Die Koordinate ist relativ zur oberen linken Ecke des Clientbereichs.</span><span class="sxs-lookup"><span data-stu-id="1e13b-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e13b-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e13b-132">Return value</span></span>

<span data-ttu-id="1e13b-133">Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e13b-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e13b-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e13b-134">Remarks</span></span>

<span data-ttu-id="1e13b-135">Verwenden Sie den folgenden Code, um die horizontale und vertikale Position zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="1e13b-135">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="1e13b-136">Wie bereits erwähnt, liegt die x-Koordinate in der niedrigen Reihenfolge **unter** dem lParam-Wert. Die y-Koordinate befindet sich in  der hohen Kurzen **(beide** stellen werte mit Vorsignieren dar, da sie negative Werte auf Systemen mit mehreren Monitoren verwenden können).</span><span class="sxs-lookup"><span data-stu-id="1e13b-136">As noted above, the x-coordinate is in the low-order **short** of the lParam value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="1e13b-137">Wenn der Rückgabewert einer Variablen zugewiesen wird, können Sie das [**MAKEPOINTS-Makro**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) verwenden, um eine [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) aus dem Rückgabewert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e13b-137">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="1e13b-138">Sie können auch das [**GET \_ X \_ LPARAM-**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) oder [**GET \_ \_ Y-LPARAM-Makro**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die x- oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="1e13b-138">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e13b-139">Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e13b-139">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="1e13b-140">Systeme mit mehreren Monitoren können negative x- und y-Koordinaten haben, **und LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="1e13b-140">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e13b-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e13b-141">Requirements</span></span>



| <span data-ttu-id="1e13b-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e13b-142">Requirement</span></span> | <span data-ttu-id="1e13b-143">Wert</span><span class="sxs-lookup"><span data-stu-id="1e13b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e13b-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e13b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1e13b-145">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e13b-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e13b-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e13b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1e13b-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e13b-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e13b-148">Header</span><span class="sxs-lookup"><span data-stu-id="1e13b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e13b-149"><dt>Winuser.h (einschließlich Windowsx.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e13b-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e13b-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1e13b-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e13b-151">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="1e13b-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e13b-152">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="1e13b-152">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="1e13b-153">**GET \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="1e13b-153">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="1e13b-154">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="1e13b-154">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="1e13b-155">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="1e13b-155">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="1e13b-156">**WM \_ LBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="1e13b-156">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="1e13b-157">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="1e13b-157">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

<span data-ttu-id="1e13b-158">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="1e13b-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e13b-159">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="1e13b-159">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="1e13b-160">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="1e13b-160">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1e13b-161">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="1e13b-161">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="1e13b-162">[**Punkte**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e13b-162">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

