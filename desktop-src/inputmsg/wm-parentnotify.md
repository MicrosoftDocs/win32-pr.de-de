---
title: WM_PARENTNOTIFY Meldung
description: Wird an ein Fenster gesendet, wenn eine bedeutende Aktion in einem Nachfolger Fenster auftritt.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_PARENTNOTIFY Nachricht
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518320"
---
# <a name="wm_parentnotify-message"></a><span data-ttu-id="712ce-104">WM_PARENTNOTIFY Meldung</span><span class="sxs-lookup"><span data-stu-id="712ce-104">WM_PARENTNOTIFY message</span></span>

<span data-ttu-id="712ce-105">Wird an ein Fenster gesendet, wenn eine bedeutende Aktion in einem Nachfolger Fenster auftritt.</span><span class="sxs-lookup"><span data-stu-id="712ce-105">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="712ce-106">Diese Meldung ist nun so erweitert, dass Sie das [**WM_POINTERDOWN**](wm-pointerdown.md) -Ereignis einschließt.</span><span class="sxs-lookup"><span data-stu-id="712ce-106">This message is now extended to include the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span> <span data-ttu-id="712ce-107">Wenn das untergeordnete Fenster erstellt wird, sendet das System [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) direkt vor der Funktion "" [**, die das**](/windows/win32/api/winuser/nf-winuser-createwindowa) Fenster erstellt hat [**, und gibt**](/windows/win32/api/winuser/nf-winuser-createwindowexa) es zurück.</span><span class="sxs-lookup"><span data-stu-id="712ce-107">When the child window is being created, the system sends [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="712ce-108">Wenn das untergeordnete Fenster zerstört wird, sendet das System die Nachricht, bevor eine Verarbeitung zum Zerstören des Fensters erfolgt.</span><span class="sxs-lookup"><span data-stu-id="712ce-108">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span>

<span data-ttu-id="712ce-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="712ce-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="712ce-110">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="712ce-110">\[!Important\]</span></span>  
> <span data-ttu-id="712ce-111">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="712ce-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="712ce-112">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="712ce-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="712ce-113">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="712ce-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="712ce-114">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="712ce-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a><span data-ttu-id="712ce-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="712ce-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="712ce-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="712ce-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="712ce-117">Das nieder wertige Wort von *wParam* gibt das Ereignis an, für das das übergeordnete Element benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="712ce-117">The low-order word of *wParam* specifies the event for which the parent is being notified.</span></span> <span data-ttu-id="712ce-118">Der Wert des höherwertigen Worts hängt vom Wert des nieder wertigen Worts ab.</span><span class="sxs-lookup"><span data-stu-id="712ce-118">The value of the high-order word depends on the value of the low-order word.</span></span> <span data-ttu-id="712ce-119">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="712ce-119">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="712ce-120">LoWord (*wParam*)</span><span class="sxs-lookup"><span data-stu-id="712ce-120">LOWORD(*wParam*)</span></span>                                                                                                                                                                                                             | <span data-ttu-id="712ce-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="712ce-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <span data-ttu-id="712ce-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span></span> </dl>                | <span data-ttu-id="712ce-123">Das untergeordnete Fenster wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="712ce-123">The child window is being created.</span></span><br/> <span data-ttu-id="712ce-124">HIWORD (*wParam*) ist der Bezeichner des untergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="712ce-124">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="712ce-125">*LPARAM* ist ein Handle für das untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="712ce-125">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <span data-ttu-id="712ce-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span></span> </dl>             | <span data-ttu-id="712ce-127">Das untergeordnete Fenster wird zerstört.</span><span class="sxs-lookup"><span data-stu-id="712ce-127">The child window is being destroyed.</span></span><br/> <span data-ttu-id="712ce-128">HIWORD (*wParam*) ist der Bezeichner des untergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="712ce-128">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="712ce-129">*LPARAM* ist ein Handle für das untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="712ce-129">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <span data-ttu-id="712ce-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span></span> </dl> | <span data-ttu-id="712ce-131">Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat mit der linken Maustaste geklickt.</span><span class="sxs-lookup"><span data-stu-id="712ce-131">The user has placed the cursor over the child window and has clicked the left mouse button.</span></span><br/> <span data-ttu-id="712ce-132">HIWORD (*wParam*) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="712ce-132">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="712ce-133">*LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.</span><span class="sxs-lookup"><span data-stu-id="712ce-133">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <span data-ttu-id="712ce-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span></span> </dl> | <span data-ttu-id="712ce-135">Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat auf die mittlere Maustaste geklickt.</span><span class="sxs-lookup"><span data-stu-id="712ce-135">The user has placed the cursor over the child window and has clicked the middle mouse button.</span></span><br/> <span data-ttu-id="712ce-136">HIWORD (*wParam*) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="712ce-136">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="712ce-137">*LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.</span><span class="sxs-lookup"><span data-stu-id="712ce-137">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <span data-ttu-id="712ce-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span></span> </dl> | <span data-ttu-id="712ce-139">Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat mit der rechten Maustaste geklickt.</span><span class="sxs-lookup"><span data-stu-id="712ce-139">The user has placed the cursor over the child window and has clicked the right mouse button.</span></span><br/> <span data-ttu-id="712ce-140">HIWORD (*wParam*) ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="712ce-140">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="712ce-141">*LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.</span><span class="sxs-lookup"><span data-stu-id="712ce-141">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <span data-ttu-id="712ce-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020b</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span></span> </dl> | <span data-ttu-id="712ce-143">Der Benutzer hat den Cursor über das untergeordnete Fenster platziert und hat auf die erste oder zweite X-Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="712ce-143">The user has placed the cursor over the child window and has clicked the first or second X button.</span></span><br/> <span data-ttu-id="712ce-144">HIWORD (*wParam*) gibt an, welche Schaltfläche gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="712ce-144">HIWORD(*wParam*) indicates which button was pressed.</span></span> <span data-ttu-id="712ce-145">Dieser Parameter kann einen der folgenden Werte aufweisen: XButton1 oder XButton2.</span><span class="sxs-lookup"><span data-stu-id="712ce-145">This parameter can be one of the following values: XBUTTON1 or XBUTTON2.</span></span><br/> <span data-ttu-id="712ce-146">*LPARAM* ist die x-Koordinate des Cursors ist das nieder wertige Wort, und die y-Koordinate des Cursors ist das hochwertige Wort.</span><span class="sxs-lookup"><span data-stu-id="712ce-146">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <span data-ttu-id="712ce-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span></span> </dl> | <span data-ttu-id="712ce-148">Ein Zeiger hat eine Verbindung mit dem untergeordneten Fenster hergestellt.</span><span class="sxs-lookup"><span data-stu-id="712ce-148">A pointer has made contact with the child window.</span></span><br/> <span data-ttu-id="712ce-149">HIWORD (*wParam*) enthält den Bezeichner des Zeigers, der das [**WM_POINTERDOWN**](wm-pointerdown.md) Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="712ce-149">HIWORD(*wParam*) contains the identifier of the pointer that generated the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span><br/>                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="712ce-150">*lParam*</span><span class="sxs-lookup"><span data-stu-id="712ce-150">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="712ce-151">Enthält die Punktposition des Zeigers.</span><span class="sxs-lookup"><span data-stu-id="712ce-151">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="712ce-152">Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="712ce-152">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="712ce-153">Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="712ce-153">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="712ce-154">Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.</span><span class="sxs-lookup"><span data-stu-id="712ce-154">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="712ce-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).</span><span class="sxs-lookup"><span data-stu-id="712ce-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="712ce-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).</span><span class="sxs-lookup"><span data-stu-id="712ce-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="712ce-157">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="712ce-157">Return value</span></span>

<span data-ttu-id="712ce-158">Wenn die Anwendung diese Nachricht verarbeitet, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="712ce-158">If the application processes this message, it returns zero.</span></span>

<span data-ttu-id="712ce-159">Wenn die Anwendung diese Nachricht nicht verarbeitet, ruft Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)auf.</span><span class="sxs-lookup"><span data-stu-id="712ce-159">If the application does not process this message, it calls [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="712ce-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="712ce-160">Remarks</span></span>

<span data-ttu-id="712ce-161">Diese Meldung wird auch an alle übergeordneten Fenster des untergeordneten Fensters gesendet, einschließlich des Fensters der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="712ce-161">This message is also sent to all ancestor windows of the child window, including the top-level window.</span></span>

<span data-ttu-id="712ce-162">Alle untergeordneten Fenster, mit Ausnahme derjenigen, die den **WS_EX_NOPARENTNOTIFY** erweiterten Fenster Stil aufweisen, senden diese Nachricht an die übergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="712ce-162">All child windows, except those that have the **WS_EX_NOPARENTNOTIFY** extended window style, send this message to their parent windows.</span></span> <span data-ttu-id="712ce-163">Standardmäßig haben untergeordnete Fenster in einem Dialogfeld den **WS_EX_NOPARENTNOTIFY** Stil, es sei denn, die Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " wird aufgerufen, um das untergeordnete Fenster ohne diesen Stil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="712ce-163">By default, child windows in a dialog box have the **WS_EX_NOPARENTNOTIFY** style, unless the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function is called to create the child window without this style.</span></span>

<span data-ttu-id="712ce-164">Diese Benachrichtigung bietet den Vorgänger Fenstern des untergeordneten Fensters die Möglichkeit, die Zeiger Informationen zu untersuchen und ggf. den Zeiger mithilfe der Zeiger Erfassungs Funktionen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="712ce-164">This notification provides the child window's ancestor windows an opportunity to examine the pointer information and, if required, capture the pointer using the pointer capture functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="712ce-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="712ce-165">Requirements</span></span>



| <span data-ttu-id="712ce-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="712ce-166">Requirement</span></span> | <span data-ttu-id="712ce-167">Wert</span><span class="sxs-lookup"><span data-stu-id="712ce-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="712ce-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="712ce-168">Minimum supported client</span></span><br/> | <span data-ttu-id="712ce-169">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="712ce-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="712ce-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="712ce-170">Minimum supported server</span></span><br/> | <span data-ttu-id="712ce-171">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="712ce-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="712ce-172">Header</span><span class="sxs-lookup"><span data-stu-id="712ce-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="712ce-173"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="712ce-173"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712ce-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="712ce-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712ce-175">Meldungen</span><span class="sxs-lookup"><span data-stu-id="712ce-175">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="712ce-176">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="712ce-176">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="712ce-177">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="712ce-177">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

<span data-ttu-id="712ce-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="712ce-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="712ce-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="712ce-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="712ce-180">**WM_CREATE**</span><span class="sxs-lookup"><span data-stu-id="712ce-180">**WM_CREATE**</span></span>](../winmsg/wm-create.md)
</dt> <dt>

[<span data-ttu-id="712ce-181">**WM_DESTROY**</span><span class="sxs-lookup"><span data-stu-id="712ce-181">**WM_DESTROY**</span></span>](../winmsg/wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="712ce-182">**WM_LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="712ce-182">**WM_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="712ce-183">**WM_MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="712ce-183">**WM_MBUTTONDOWN**</span></span>](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="712ce-184">**WM_RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="712ce-184">**WM_RBUTTONDOWN**</span></span>](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="712ce-185">**WM_XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="712ce-185">**WM_XBUTTONDOWN**</span></span>](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

