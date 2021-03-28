---
Description: Die WM- \_ Paint-Meldung wird gesendet, wenn das System oder eine andere Anwendung eine Anforderung zum Zeichnen eines Teils des Fensters einer Anwendung sendet.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: WM_PAINT Meldung (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982956"
---
# <a name="wm_paint-message"></a><span data-ttu-id="64102-103">WM \_ Paint-Meldung</span><span class="sxs-lookup"><span data-stu-id="64102-103">WM\_PAINT message</span></span>

<span data-ttu-id="64102-104">Die **WM- \_ Paint** -Meldung wird gesendet, wenn das System oder eine andere Anwendung eine Anforderung zum Zeichnen eines Teils des Fensters einer Anwendung sendet.</span><span class="sxs-lookup"><span data-stu-id="64102-104">The **WM\_PAINT** message is sent when the system or another application makes a request to paint a portion of an application's window.</span></span> <span data-ttu-id="64102-105">Die Nachricht wird gesendet, wenn die Funktion [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) oder [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) aufgerufen wird, oder durch [**die DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) -Funktion, wenn die Anwendung eine WM-Zeichnungs Nachricht mithilfe der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer-Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion erhält. **\_**</span><span class="sxs-lookup"><span data-stu-id="64102-105">The message is sent when the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) or [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) function is called, or by the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function when the application obtains a **WM\_PAINT** message by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>

<span data-ttu-id="64102-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="64102-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="64102-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="64102-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64102-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64102-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64102-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="64102-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="64102-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64102-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64102-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="64102-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64102-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64102-112">Return value</span></span>

<span data-ttu-id="64102-113">Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="64102-113">An application returns zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="64102-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="64102-114">Example</span></span>

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

<span data-ttu-id="64102-115">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="64102-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="64102-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64102-116">Remarks</span></span>

<span data-ttu-id="64102-117">Die **WM- \_ Paint** -Meldung wird vom System generiert und sollte nicht von einer Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="64102-117">The **WM\_PAINT** message is generated by the system and should not be sent by an application.</span></span> <span data-ttu-id="64102-118">Um zu erzwingen, dass ein Fenster in einen bestimmten Gerätekontext gezeichnet wird, verwenden Sie die Meldung [**WM \_ Print**](wm-print.md) oder [**WM \_ printclient**](wm-printclient.md) .</span><span class="sxs-lookup"><span data-stu-id="64102-118">To force a window to draw into a specific device context, use the [**WM\_PRINT**](wm-print.md) or [**WM\_PRINTCLIENT**](wm-printclient.md) message.</span></span> <span data-ttu-id="64102-119">Beachten Sie, dass das Zielfenster die WM- **\_ printclient** -Nachricht unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="64102-119">Note that this requires the target window to support the **WM\_PRINTCLIENT** message.</span></span> <span data-ttu-id="64102-120">Die meisten gängigen Steuerelemente unterstützen die **WM- \_ printclient** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="64102-120">Most common controls support the **WM\_PRINTCLIENT** message.</span></span>

<span data-ttu-id="64102-121">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion überprüft den Update Bereich.</span><span class="sxs-lookup"><span data-stu-id="64102-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function validates the update region.</span></span> <span data-ttu-id="64102-122">Die Funktion kann die [**WM \_ ncpaint**](wm-ncpaint.md) -Nachricht auch an die Fenster Prozedur senden, wenn der Fensterrahmen gezeichnet werden muss, und die [**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Nachricht senden, wenn der Fenster Hintergrund gelöscht werden muss.</span><span class="sxs-lookup"><span data-stu-id="64102-122">The function may also send the [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

<span data-ttu-id="64102-123">Das System sendet diese Nachricht, wenn in der Nachrichten Warteschlange der Anwendung keine weiteren Meldungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="64102-123">The system sends this message when there are no other messages in the application's message queue.</span></span> <span data-ttu-id="64102-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) legt fest, wohin die Nachricht gesendet werden soll. [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) bestimmt, welche Nachricht versendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64102-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determines where to send the message; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determines which message to dispatch.</span></span> <span data-ttu-id="64102-125">**GetMessage** gibt die **WM \_** -Zeichnungs Nachricht zurück, wenn keine weiteren Meldungen in der Nachrichten Warteschlange der Anwendung vorhanden sind, und **DispatchMessage** sendet die Nachricht an die entsprechende Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="64102-125">**GetMessage** returns the **WM\_PAINT** message when there are no other messages in the application's message queue, and **DispatchMessage** sends the message to the appropriate window procedure.</span></span>

<span data-ttu-id="64102-126">Ein Fenster empfängt möglicherweise interne Paint-Meldungen als Ergebnis des Aufruf von [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) mit dem \_ festgelegten RDW internalpaint-Flag.</span><span class="sxs-lookup"><span data-stu-id="64102-126">A window may receive internal paint messages as a result of calling [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span> <span data-ttu-id="64102-127">In diesem Fall verfügt das Fenster möglicherweise nicht über einen Update Bereich.</span><span class="sxs-lookup"><span data-stu-id="64102-127">In this case, the window may not have an update region.</span></span> <span data-ttu-id="64102-128">Eine Anwendung kann die [**getupdatererfunktion**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) aufrufen, um zu bestimmen, ob das Fenster über einen Update Bereich verfügt.</span><span class="sxs-lookup"><span data-stu-id="64102-128">An application may call the [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) function to determine whether the window has an update region.</span></span> <span data-ttu-id="64102-129">Wenn **getupdatdent** NULL zurückgibt, muss die Anwendung die [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -und [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -Funktionen nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64102-129">If **GetUpdateRect** returns zero, the application need not call the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions.</span></span>

<span data-ttu-id="64102-130">Eine Anwendung muss überprüfen, ob Sie über die internen Datenstrukturen für jede WM-Zeichnungs Nachricht verfügen, da eine **WM- \_** Zeichnungs Nachricht sowohl von einem Update Bereich ungleich NULL als auch von einem Rückruf von [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) mit dem festgelegten RDW **\_** \_ internalpaint-Flag ausgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="64102-130">An application must check for any necessary internal painting by looking at its internal data structures for each **WM\_PAINT** message, because a **WM\_PAINT** message may have been caused by both a non-NULL update region and a call to [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="64102-131">Das System sendet eine interne **WM \_** -Zeichnungs Nachricht nur einmal.</span><span class="sxs-lookup"><span data-stu-id="64102-131">The system sends an internal **WM\_PAINT** message only once.</span></span> <span data-ttu-id="64102-132">Nachdem eine interne **WM \_** -Zeichnungs Meldung von [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) zurückgegeben oder an ein Fenster durch [**Update Window**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)gesendet wurde, sendet oder sendet das System keine weiteren **WM \_ Paint** -Meldungen, bis das Fenster ungültig gemacht wird, oder bis [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) erneut aufgerufen wird, wenn das RDW \_ internalpaint-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64102-132">After an internal **WM\_PAINT** message is returned from [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) or is sent to a window by [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), the system does not post or send further **WM\_PAINT** messages until the window is invalidated or until [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) is called again with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="64102-133">Bei einigen allgemeinen Steuerelementen überprüft die standardmäßige **WM \_ Paint** -Nachrichtenverarbeitung den *wParam* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="64102-133">For some common controls, the default **WM\_PAINT** message processing checks the *wParam* parameter.</span></span> <span data-ttu-id="64102-134">Wenn *wParam* ungleich NULL ist, geht das Steuerelement davon aus, dass es sich bei dem Wert um einen HDC handelt und zeichnet sich mit diesem Gerätekontext aus.</span><span class="sxs-lookup"><span data-stu-id="64102-134">If *wParam* is non-NULL, the control assumes that the value is an HDC and paints using that device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="64102-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="64102-135">Requirements</span></span>



| <span data-ttu-id="64102-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64102-136">Requirement</span></span> | <span data-ttu-id="64102-137">Wert</span><span class="sxs-lookup"><span data-stu-id="64102-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64102-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64102-138">Minimum supported client</span></span><br/> | <span data-ttu-id="64102-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64102-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="64102-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64102-140">Minimum supported server</span></span><br/> | <span data-ttu-id="64102-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64102-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64102-142">Header</span><span class="sxs-lookup"><span data-stu-id="64102-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="64102-143"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="64102-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64102-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="64102-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64102-145">Übersicht über das Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="64102-145">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="64102-146">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="64102-146">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="64102-147">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="64102-147">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="64102-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="64102-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="64102-149">**DispatchMessage gesendet**</span><span class="sxs-lookup"><span data-stu-id="64102-149">**DispatchMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[<span data-ttu-id="64102-150">**Endpaint auf**</span><span class="sxs-lookup"><span data-stu-id="64102-150">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="64102-151">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="64102-151">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="64102-152">**Getupdaterierten**</span><span class="sxs-lookup"><span data-stu-id="64102-152">**GetUpdateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[<span data-ttu-id="64102-153">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="64102-153">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="64102-154">**Redrawwindow**</span><span class="sxs-lookup"><span data-stu-id="64102-154">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[<span data-ttu-id="64102-155">**Update Window**</span><span class="sxs-lookup"><span data-stu-id="64102-155">**UpdateWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[<span data-ttu-id="64102-156">**WM- \_ erasebkgnd**</span><span class="sxs-lookup"><span data-stu-id="64102-156">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="64102-157">**WM- \_ ncpaint**</span><span class="sxs-lookup"><span data-stu-id="64102-157">**WM\_NCPAINT**</span></span>](wm-ncpaint.md)
</dt> <dt>

[<span data-ttu-id="64102-158">**WM- \_ Druck**</span><span class="sxs-lookup"><span data-stu-id="64102-158">**WM\_PRINT**</span></span>](wm-print.md)
</dt> <dt>

[<span data-ttu-id="64102-159">**WM- \_ printclient**</span><span class="sxs-lookup"><span data-stu-id="64102-159">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
