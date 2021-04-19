---
title: WM_MOUSEWHEEL Meldung (Winuser. h)
description: Wird an das Fokus Fenster gesendet, wenn das Mausrad gedreht wird.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSEWHEEL Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338724"
---
# <a name="wm_mousewheel-message"></a><span data-ttu-id="22781-104">WM- \_ mouswheel-Meldung</span><span class="sxs-lookup"><span data-stu-id="22781-104">WM\_MOUSEWHEEL message</span></span>

<span data-ttu-id="22781-105">Wird an das Fokus Fenster gesendet, wenn das Mausrad gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="22781-105">Sent to the focus window when the mouse wheel is rotated.</span></span> <span data-ttu-id="22781-106">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt die Nachricht an das übergeordnete Fenster des Fensters weiter.</span><span class="sxs-lookup"><span data-stu-id="22781-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="22781-107">Es sollte keine interne Weiterleitung der Nachricht vorhanden sein, da **defwindowproc** Sie in der übergeordneten Kette weitergibt, bis ein Fenster gefunden wird, in dem Sie verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="22781-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="22781-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="22781-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a><span data-ttu-id="22781-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="22781-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22781-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22781-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22781-111">Das höchst wertige Wort gibt die Entfernung an, um die das Rad gedreht wird, ausgedrückt in Vielfachen oder Abteilungen des **\_ raddeltas**, das 120 ist.</span><span class="sxs-lookup"><span data-stu-id="22781-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or divisions of **WHEEL\_DELTA**, which is 120.</span></span> <span data-ttu-id="22781-112">Ein positiver Wert gibt an, dass das Rad vom Benutzer entfernt wurde. ein negativer Wert gibt an, dass das Rad in Richtung des Benutzers rückwärts gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="22781-112">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span>

<span data-ttu-id="22781-113">Das nieder wertige Wort gibt an, ob verschiedene virtuelle Schlüssel ausfallen.</span><span class="sxs-lookup"><span data-stu-id="22781-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="22781-114">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="22781-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="22781-115">Wert</span><span class="sxs-lookup"><span data-stu-id="22781-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="22781-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="22781-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="22781-117"><dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="22781-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="22781-118">Die STRG-Taste ist nicht gedrückt.</span><span class="sxs-lookup"><span data-stu-id="22781-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="22781-119"><dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="22781-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="22781-120">Die linke Maustaste ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="22781-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="22781-121"><dt>**MK \_ MButton**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="22781-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="22781-122">Die mittlere Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22781-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="22781-123"><dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="22781-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="22781-124">Die Rechte Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22781-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="22781-125"><dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="22781-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="22781-126">Die UMSCHALTTASTE ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22781-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="22781-127"><dt>**MK \_ XButton1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="22781-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="22781-128">Die erste X-Schaltfläche ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22781-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="22781-129"><dt>**MK \_ XButton2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="22781-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="22781-130">Die zweite X-Schaltfläche ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22781-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="22781-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22781-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22781-132">Das nieder wertige Wort gibt die x-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="22781-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="22781-133">Das höchst wertige Wort gibt die y-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="22781-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22781-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22781-134">Return value</span></span>

<span data-ttu-id="22781-135">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22781-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="22781-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22781-136">Remarks</span></span>

<span data-ttu-id="22781-137">Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="22781-137">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="22781-138">Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:</span><span class="sxs-lookup"><span data-stu-id="22781-138">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="22781-139">Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können).</span><span class="sxs-lookup"><span data-stu-id="22781-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="22781-140">Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen.</span><span class="sxs-lookup"><span data-stu-id="22781-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="22781-141">Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="22781-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22781-142">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22781-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="22781-143">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="22781-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="22781-144">Die Raddrehung ist ein Vielfaches von **\_ raddelta**, das bei 120 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="22781-144">The wheel rotation will be a multiple of **WHEEL\_DELTA**, which is set at 120.</span></span> <span data-ttu-id="22781-145">Dies ist der Schwellenwert für die auszuführende Aktion, und eine Aktion (z. b. durch Scrollen eines Inkrements) sollte für jedes Delta stattfinden.</span><span class="sxs-lookup"><span data-stu-id="22781-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="22781-146">Das Delta wurde auf 120 festgelegt, um es Microsoft oder anderen Anbietern zu ermöglichen, feinere Auflösungs Räder (ein rotiertes Rad ohne Notches) zu erstellen, um mehr Nachrichten pro Drehung zu senden, aber mit einem geringeren Wert in jeder Nachricht.</span><span class="sxs-lookup"><span data-stu-id="22781-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="22781-147">Um dieses Feature verwenden zu können, können Sie die eingehenden Delta Werte hinzufügen, bis das **\_ raddelta** erreicht ist (sodass Sie für eine Delta Drehung dieselbe Antwort erhalten), oder indem Sie Teil Zeilen als Reaktion auf häufigere Nachrichten scrollen.</span><span class="sxs-lookup"><span data-stu-id="22781-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages.</span></span> <span data-ttu-id="22781-148">Sie können auch die Bildlauf-Granularität auswählen und die Delta-Optionen ansammeln, bis Sie erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="22781-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

<span data-ttu-id="22781-149">Beachten Sie, dass es keine *Schlüssel* für das **msh- \_ mouswheel** gibt.</span><span class="sxs-lookup"><span data-stu-id="22781-149">Note, there is no *fwKeys* for **MSH\_MOUSEWHEEL**.</span></span> <span data-ttu-id="22781-150">Andernfalls sind die Parameter genau identisch mit denen für **WM \_ mouswheel**.</span><span class="sxs-lookup"><span data-stu-id="22781-150">Otherwise, the parameters are exactly the same as for **WM\_MOUSEWHEEL**.</span></span>

<span data-ttu-id="22781-151">Die Anwendung kann **msh \_ MouseWheel** an alle eingebetteten Objekte oder Steuerelemente weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="22781-151">It is up to the application to forward **MSH\_MOUSEWHEEL** to any embedded objects or controls.</span></span> <span data-ttu-id="22781-152">Die Anwendung ist erforderlich, um die Nachricht an eine aktive eingebettete OLE-Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="22781-152">The application is required to send the message to an active embedded OLE application.</span></span> <span data-ttu-id="22781-153">Es ist optional, dass die Anwendung diese an ein Rad aktiviertes Steuerelement mit dem Fokus sendet.</span><span class="sxs-lookup"><span data-stu-id="22781-153">It is optional that the application sends it to a wheel-enabled control with focus.</span></span> <span data-ttu-id="22781-154">Wenn die Anwendung die Nachricht an ein Steuerelement sendet, kann Sie den Rückgabewert überprüfen, um festzustellen, ob die Nachricht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="22781-154">If the application does send the message to a control, it can check the return value to see if the message was processed.</span></span> <span data-ttu-id="22781-155">Steuerelemente müssen den Wert " **true** " zurückgeben, wenn Sie die Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="22781-155">Controls are required to return a value of **TRUE** if they process the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="22781-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22781-156">Requirements</span></span>



| <span data-ttu-id="22781-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22781-157">Requirement</span></span> | <span data-ttu-id="22781-158">Wert</span><span class="sxs-lookup"><span data-stu-id="22781-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22781-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22781-159">Minimum supported client</span></span><br/> | <span data-ttu-id="22781-160">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22781-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="22781-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22781-161">Minimum supported server</span></span><br/> | <span data-ttu-id="22781-162">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22781-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="22781-163">Header</span><span class="sxs-lookup"><span data-stu-id="22781-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="22781-164"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22781-164"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22781-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22781-165">See also</span></span>

<dl> <dt>

<span data-ttu-id="22781-166">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="22781-166">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22781-167">**\_KeyState- \_ wParam-Element**</span><span class="sxs-lookup"><span data-stu-id="22781-167">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="22781-168">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="22781-168">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="22781-169">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="22781-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="22781-170">**\_ \_ rasterdelta- \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="22781-170">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="22781-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22781-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="22781-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22781-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22781-173">**Maus \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="22781-173">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="22781-174">**Licher**</span><span class="sxs-lookup"><span data-stu-id="22781-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22781-175">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="22781-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="22781-176">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="22781-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="22781-177">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="22781-177">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="22781-178">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="22781-178">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="22781-179">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22781-179">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22781-180">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="22781-180">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

