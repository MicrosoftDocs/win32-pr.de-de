---
title: WM_MOUSEHWHEEL Meldung (Winuser. h)
description: Wird an das aktive Fenster gesendet, wenn das horizontale Mausrad der Maus gekippt oder gedreht wird.
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSEHWHEEL Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1f3b1690ad39919e2a62b50ba6eacec8348e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338138"
---
# <a name="wm_mousehwheel-message"></a><span data-ttu-id="cacbd-104">WM- \_ mousehwheel-Meldung</span><span class="sxs-lookup"><span data-stu-id="cacbd-104">WM\_MOUSEHWHEEL message</span></span>

<span data-ttu-id="cacbd-105">Wird an das aktive Fenster gesendet, wenn das horizontale Mausrad der Maus gekippt oder gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="cacbd-105">Sent to the active window when the mouse's horizontal scroll wheel is tilted or rotated.</span></span> <span data-ttu-id="cacbd-106">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt die Nachricht an das übergeordnete Fenster des Fensters weiter.</span><span class="sxs-lookup"><span data-stu-id="cacbd-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="cacbd-107">Es sollte keine interne Weiterleitung der Nachricht vorhanden sein, da **defwindowproc** Sie in der übergeordneten Kette weitergibt, bis ein Fenster gefunden wird, in dem Sie verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cacbd-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="cacbd-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cacbd-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a><span data-ttu-id="cacbd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cacbd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cacbd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cacbd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cacbd-111">Das höchst wertige Wort gibt die Entfernung an, um die das Rad gedreht wird, ausgedrückt in Vielfachen oder Faktoren des **\_ raddeltas**, das auf 120 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cacbd-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or factors of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="cacbd-112">Ein positiver Wert gibt an, dass das Mausrad nach rechts gedreht wurde. ein negativer Wert gibt an, dass das Rad nach links gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="cacbd-112">A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left.</span></span>

<span data-ttu-id="cacbd-113">Das nieder wertige Wort gibt an, ob verschiedene virtuelle Schlüssel ausfallen.</span><span class="sxs-lookup"><span data-stu-id="cacbd-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="cacbd-114">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cacbd-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cacbd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cacbd-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="cacbd-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cacbd-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="cacbd-117"><dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="cacbd-118">Die STRG-Taste ist nicht gedrückt.</span><span class="sxs-lookup"><span data-stu-id="cacbd-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="cacbd-119"><dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="cacbd-120">Die linke Maustaste ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cacbd-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="cacbd-121"><dt>**MK \_ MButton**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="cacbd-122">Die mittlere Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cacbd-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="cacbd-123"><dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="cacbd-124">Die Rechte Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cacbd-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="cacbd-125"><dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="cacbd-126">Die UMSCHALTTASTE ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cacbd-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="cacbd-127"><dt>**MK \_ XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="cacbd-128">Die erste X-Schaltfläche ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cacbd-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="cacbd-129"><dt>**MK \_ XButton2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="cacbd-130">Die zweite X-Schaltfläche ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cacbd-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="cacbd-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cacbd-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cacbd-132">Das nieder wertige Wort gibt die x-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="cacbd-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="cacbd-133">Das höchst wertige Wort gibt die y-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="cacbd-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cacbd-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cacbd-134">Return value</span></span>

<span data-ttu-id="cacbd-135">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cacbd-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cacbd-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cacbd-136">Remarks</span></span>

<span data-ttu-id="cacbd-137">Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cacbd-137">Use the following code to obtain the information in the *wParam* parameter.</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="cacbd-138">Verwenden Sie den folgenden Code, um die horizontale und vertikale Position abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cacbd-138">Use the following code to obtain the horizontal and vertical position.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="cacbd-139">Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können).</span><span class="sxs-lookup"><span data-stu-id="cacbd-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="cacbd-140">Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen.</span><span class="sxs-lookup"><span data-stu-id="cacbd-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="cacbd-141">Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="cacbd-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cacbd-142">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cacbd-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="cacbd-143">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="cacbd-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="cacbd-144">Die Raddrehung ist ein Vielfaches von **\_ raddelta**, das auf 120 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cacbd-144">The wheel rotation is a multiple of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="cacbd-145">Dies ist der Schwellenwert für die auszuführende Aktion, und eine Aktion (z. b. durch Scrollen eines Inkrements) sollte für jedes Delta stattfinden.</span><span class="sxs-lookup"><span data-stu-id="cacbd-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="cacbd-146">Das Delta wurde auf 120 festgelegt, um es Microsoft oder anderen Anbietern zu ermöglichen, feinere Auflösungs Räder (z. b. ein rotiertes Rad ohne Notches) zu erstellen, um mehr Nachrichten pro Drehung zu senden, aber mit einem geringeren Wert in jeder Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cacbd-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (for example, a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="cacbd-147">Um dieses Feature verwenden zu können, können Sie die eingehenden Delta Werte hinzufügen, bis das **\_ raddelta** erreicht ist (also bei einer Delta Drehung dieselbe Antwort), oder wenn Sie Teil Zeilen als Reaktion auf häufigere Nachrichten scrollen.</span><span class="sxs-lookup"><span data-stu-id="cacbd-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to more frequent messages.</span></span> <span data-ttu-id="cacbd-148">Sie können auch die Bildlauf-Granularität auswählen und die Delta-Optionen ansammeln, bis Sie erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="cacbd-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="cacbd-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cacbd-149">Requirements</span></span>



| <span data-ttu-id="cacbd-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cacbd-150">Requirement</span></span> | <span data-ttu-id="cacbd-151">Wert</span><span class="sxs-lookup"><span data-stu-id="cacbd-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cacbd-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cacbd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="cacbd-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cacbd-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="cacbd-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cacbd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="cacbd-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cacbd-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cacbd-156">Header</span><span class="sxs-lookup"><span data-stu-id="cacbd-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="cacbd-157"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cacbd-157"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cacbd-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cacbd-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="cacbd-159">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cacbd-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cacbd-160">**\_KeyState- \_ wParam-Element**</span><span class="sxs-lookup"><span data-stu-id="cacbd-160">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="cacbd-161">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="cacbd-161">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="cacbd-162">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="cacbd-162">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="cacbd-163">**\_ \_ rasterdelta- \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="cacbd-163">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="cacbd-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cacbd-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="cacbd-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cacbd-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cacbd-166">**Maus \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="cacbd-166">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="cacbd-167">**Licher**</span><span class="sxs-lookup"><span data-stu-id="cacbd-167">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cacbd-168">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="cacbd-168">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="cacbd-169">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="cacbd-169">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cacbd-170">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="cacbd-170">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="cacbd-171">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="cacbd-171">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="cacbd-172">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cacbd-172">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cacbd-173">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="cacbd-173">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

