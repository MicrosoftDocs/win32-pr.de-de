---
title: Verschiedene Maus Vorgänge
description: In den vorherigen Abschnitten wurden Mausklicks und Mausbewegung erläutert. Im folgenden finden Sie einige andere Vorgänge, die mit der Maus ausgeführt werden können.
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315068"
---
# <a name="miscellaneous-mouse-operations"></a><span data-ttu-id="491db-104">Verschiedene Maus Vorgänge</span><span class="sxs-lookup"><span data-stu-id="491db-104">Miscellaneous Mouse Operations</span></span>

<span data-ttu-id="491db-105">In den vorherigen Abschnitten wurden Mausklicks und Mausbewegung erläutert.</span><span class="sxs-lookup"><span data-stu-id="491db-105">The previous sections have discussed mouse clicks and mouse movement.</span></span> <span data-ttu-id="491db-106">Im folgenden finden Sie einige andere Vorgänge, die mit der Maus ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="491db-106">Here are some other operations that can be performed with the mouse.</span></span>

## <a name="dragging-ui-elements"></a><span data-ttu-id="491db-107">Ziehen von UI-Elementen</span><span class="sxs-lookup"><span data-stu-id="491db-107">Dragging UI Elements</span></span>

<span data-ttu-id="491db-108">Wenn Ihre Benutzeroberfläche das Ziehen von UI-Elementen unterstützt, gibt es eine andere Funktion, die Sie in Ihrem MouseDown-Meldungs Handler aufzurufen: [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span><span class="sxs-lookup"><span data-stu-id="491db-108">If your UI supports dragging of UI elements, there is one other function that you should call in your mouse-down message handler: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span></span> <span data-ttu-id="491db-109">Die **dragdetect** -Funktion gibt **true** zurück, wenn der Benutzer eine Mausbewegung initiiert, die als Drag & amp; Drop interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="491db-109">The **DragDetect** function returns **TRUE** if the user initiates a mouse gesture that should be interpreted as dragging.</span></span> <span data-ttu-id="491db-110">Der folgende Code zeigt, wie Sie diese Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="491db-110">The following code shows how to use this function.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



<span data-ttu-id="491db-111">Hier ist die Idee: Wenn ein Programm Drag & Drop unterstützt, möchten Sie nicht, dass alle Mausklicks als Drag & amp; Drop interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="491db-111">Here's the idea: When a program supports drag and drop, you don't want every mouse click to be interpreted as a drag.</span></span> <span data-ttu-id="491db-112">Andernfalls kann der Benutzer versehentlich etwas ziehen, wenn er einfach darauf klickt (z. b. um ihn auszuwählen).</span><span class="sxs-lookup"><span data-stu-id="491db-112">Otherwise, the user might accidentally drag something when he or she simply meant to click on it (for example, to select it).</span></span> <span data-ttu-id="491db-113">Wenn eine Maus jedoch besonders empfindlich ist, kann es schwierig sein, die Maus beim Klicken immer noch perfekt zu halten.</span><span class="sxs-lookup"><span data-stu-id="491db-113">But if a mouse is particularly sensitive, it can be hard to keep the mouse perfectly still while clicking.</span></span> <span data-ttu-id="491db-114">Daher definiert Windows einen Zieh Schwellenwert von einigen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="491db-114">Therefore, Windows defines a drag threshold of a few pixels.</span></span> <span data-ttu-id="491db-115">Wenn der Benutzer die Maustaste drückt, wird er nicht als Drag-Vorgang betrachtet, es sei denn, der Mauszeiger überschreitet diesen Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="491db-115">When the user presses the mouse button, it is not considered a drag unless the mouse crosses this threshold.</span></span> <span data-ttu-id="491db-116">Die [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) -Funktion testet, ob dieser Schwellenwert erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="491db-116">The [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function tests whether this threshold is reached.</span></span> <span data-ttu-id="491db-117">Wenn die Funktion **true** zurückgibt, können Sie den Mauszeiger als Drag & amp; Drop interpretieren.</span><span class="sxs-lookup"><span data-stu-id="491db-117">If the function returns **TRUE**, you can interpret the mouse click as a drag.</span></span> <span data-ttu-id="491db-118">Andernfalls ist dies nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="491db-118">Otherwise, do not.</span></span>

> [!Note]  
> <span data-ttu-id="491db-119">Wenn [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) **false** zurückgibt, unterdrückt Windows die [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung, wenn der Benutzer die Maustaste loslässt.</span><span class="sxs-lookup"><span data-stu-id="491db-119">If [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) returns **FALSE**, Windows suppresses the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message when the user releases the mouse button.</span></span> <span data-ttu-id="491db-120">Verwenden Sie daher nicht **dragdetect** , es sei denn, Ihr Programm befindet sich derzeit in einem Modus, der das Ziehen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="491db-120">Therefore, do not call **DragDetect** unless your program is currently in a mode that supports dragging.</span></span> <span data-ttu-id="491db-121">(Z. b. Wenn ein Draggable-Element bereits ausgewählt ist.) Am Ende dieses Moduls wird ein längeres Codebeispiel angezeigt, in dem die **dragdetect** -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="491db-121">(For example, if a draggable UI element is already selected.) At the end of this module, we will see a longer code example that uses the **DragDetect** function.</span></span>

 

## <a name="confining-the-cursor"></a><span data-ttu-id="491db-122">Einschränken des Cursors</span><span class="sxs-lookup"><span data-stu-id="491db-122">Confining the Cursor</span></span>

<span data-ttu-id="491db-123">Manchmal möchten Sie möglicherweise den Cursor auf den Client Bereich oder einen Teil des Client Bereichs einschränken.</span><span class="sxs-lookup"><span data-stu-id="491db-123">Sometimes you might want to restrict the cursor to the client area or a portion of the client area.</span></span> <span data-ttu-id="491db-124">Die [**clipcursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) -Funktion schränkt die Bewegung des Cursors auf ein angegebenes Rechteck ein.</span><span class="sxs-lookup"><span data-stu-id="491db-124">The [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function restricts the movement of the cursor to a specified rectangle.</span></span> <span data-ttu-id="491db-125">Dieses Rechteck wird anstelle von Client Koordinaten in Bildschirm Koordinaten angegeben, sodass der Punkt (0,0) die obere linke Ecke des Bildschirms bedeutet.</span><span class="sxs-lookup"><span data-stu-id="491db-125">This rectangle is given in screen coordinates, rather than client coordinates, so the point (0, 0) means the upper left corner of the screen.</span></span> <span data-ttu-id="491db-126">Wenn Sie Client Koordinaten in Bildschirm Koordinaten übersetzen möchten, müssen Sie die Funktion [**clientumscreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="491db-126">To translate client coordinates into screen coordinates, call the function [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span></span>

<span data-ttu-id="491db-127">Der folgende Code schränkt den Cursor auf den Client Bereich des Fensters ein.</span><span class="sxs-lookup"><span data-stu-id="491db-127">The following code confines the cursor to the client area of the window.</span></span>


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



<span data-ttu-id="491db-128">[**Clipcursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) nimmt eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, aber [**clientchanscreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) übernimmt eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur.</span><span class="sxs-lookup"><span data-stu-id="491db-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) takes a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure, but [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) takes a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="491db-129">Ein Rechteck wird durch seine oberen linken und unteren rechten Punkte definiert.</span><span class="sxs-lookup"><span data-stu-id="491db-129">A rectangle is defined by its top-left and bottom-right points.</span></span> <span data-ttu-id="491db-130">Sie können den Cursor auf einen beliebigen rechteckigen Bereich beschränken, einschließlich Bereiche außerhalb des Fensters, aber das Einschränken des Cursors auf den Client Bereich ist eine typische Methode zur Verwendung der Funktion.</span><span class="sxs-lookup"><span data-stu-id="491db-130">You can confine the cursor to any rectangular area, including areas outside the window, but confining the cursor to the client area is a typical way to use the function.</span></span> <span data-ttu-id="491db-131">Die Beschränkung des Cursors auf eine Region außerhalb des Fensters wäre ungewöhnlich, und Benutzer würden Sie wahrscheinlich als Fehler betrachten.</span><span class="sxs-lookup"><span data-stu-id="491db-131">Confining the cursor to a region entirely outside your window would be unusual, and users would probably perceive it as a bug.</span></span>

<span data-ttu-id="491db-132">Um die Einschränkung zu entfernen, wenden Sie [**clipcursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) mit dem Wert **null** an.</span><span class="sxs-lookup"><span data-stu-id="491db-132">To remove the restriction, call [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) with the value **NULL**.</span></span>


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a><span data-ttu-id="491db-133">Maus Verfolgungs Ereignisse: hover und Leave</span><span class="sxs-lookup"><span data-stu-id="491db-133">Mouse Tracking Events: Hover and Leave</span></span>

<span data-ttu-id="491db-134">Zwei andere Maus Meldungen sind standardmäßig deaktiviert, können aber für einige Anwendungen nützlich sein:</span><span class="sxs-lookup"><span data-stu-id="491db-134">Two other mouse messages are disabled by default, but may be useful for some applications:</span></span>

-   <span data-ttu-id="491db-135">[**WM \_ MouseHover**](/windows/desktop/inputdev/wm-mousehover): der Cursor befindet sich für einen bestimmten Zeitraum über den Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="491db-135">[**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): The cursor has hovered over the client area for a fixed period of time.</span></span>
-   <span data-ttu-id="491db-136">[**WM \_ MouseLeave**](/windows/desktop/inputdev/wm-mouseleave): der Cursor hat den Client Bereich verlassen.</span><span class="sxs-lookup"><span data-stu-id="491db-136">[**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): The cursor has left the client area.</span></span>

<span data-ttu-id="491db-137">Um diese Nachrichten zu aktivieren, müssen Sie die [**trackmousevent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="491db-137">To enable these messages, call the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function.</span></span>


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



<span data-ttu-id="491db-138">Die [**trackmousevent**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) -Struktur enthält die Parameter für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="491db-138">The [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) structure contains the parameters for the function.</span></span> <span data-ttu-id="491db-139">Der **dwFlags** -Member der-Struktur enthält Bitflags, die angeben, an welchen nach Verfolgungs Meldungen Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="491db-139">The **dwFlags** member of the structure contains bit flags that specify which tracking messages you are interested in.</span></span> <span data-ttu-id="491db-140">Sie können sowohl [**WM \_ moust Hover**](/windows/desktop/inputdev/wm-mousehover) als auch [**WM \_ MouseLeave**](/windows/desktop/inputdev/wm-mouseleave)erhalten, wie hier gezeigt, oder nur eine der beiden Optionen.</span><span class="sxs-lookup"><span data-stu-id="491db-140">You can choose to get both [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) and [**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), as shown here, or just one of the two.</span></span> <span data-ttu-id="491db-141">Der **dwhovertime** -Member gibt an, wie lange der Mauszeiger bewegen muss, bevor das System eine Hover-Nachricht generiert.</span><span class="sxs-lookup"><span data-stu-id="491db-141">The **dwHoverTime** member specifies how long the mouse needs to hover before the system generates a hover message.</span></span> <span data-ttu-id="491db-142">Dieser Wert wird in Millisekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="491db-142">This value is given in milliseconds.</span></span> <span data-ttu-id="491db-143">Der **\_ Standard** Wert der Konstanten Hover bedeutet, dass die Standardeinstellung des Systems verwendet wird</span><span class="sxs-lookup"><span data-stu-id="491db-143">The constant **HOVER\_DEFAULT** means to use the system default.</span></span>

<span data-ttu-id="491db-144">Nachdem Sie eine der angeforderten Nachrichten erhalten haben, setzt die [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="491db-144">After you get one of the messages that you requested, the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function resets.</span></span> <span data-ttu-id="491db-145">Sie müssen ihn erneut abrufen, um eine weitere nach Verfolgungs Meldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="491db-145">You must call it again to get another tracking message.</span></span> <span data-ttu-id="491db-146">Sie sollten jedoch bis zur nächsten Mausbewegung warten, bevor Sie **TrackMouseEvent** erneut aufrufen.</span><span class="sxs-lookup"><span data-stu-id="491db-146">However, you should wait until the next mouse-move message before calling **TrackMouseEvent** again.</span></span> <span data-ttu-id="491db-147">Andernfalls wird das Fenster möglicherweise mit nach Verfolgungs Meldungen überflutet.</span><span class="sxs-lookup"><span data-stu-id="491db-147">Otherwise, your window might be flooded with tracking messages.</span></span> <span data-ttu-id="491db-148">Wenn der Mauszeiger z. b. mit der Maus bewegt wird, generiert das System weiterhin einen Stream von [**WM- \_ MouseHover**](/windows/desktop/inputdev/wm-mousehover) -Nachrichten, während die Maus stationär ist.</span><span class="sxs-lookup"><span data-stu-id="491db-148">For example, if the mouse is hovering, the system would continue to generate a stream of [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) messages while the mouse is stationary.</span></span> <span data-ttu-id="491db-149">Sie möchten keine weitere **WM- \_ MouseHover** -Nachricht, bis der Mauszeiger an eine andere Stelle bewegt wird, und dann erneut darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="491db-149">You don't actually want another **WM\_MOUSEHOVER** message until the mouse moves to another spot and hovers again.</span></span>

<span data-ttu-id="491db-150">Hier ist eine kleine Hilfsklasse, die Sie zum Verwalten von Maus Verfolgungs Ereignissen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="491db-150">Here is a small helper class that you can use to manage mouse-tracking events.</span></span>


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



<span data-ttu-id="491db-151">Im nächsten Beispiel wird gezeigt, wie Sie diese Klasse in der Fenster Prozedur verwenden.</span><span class="sxs-lookup"><span data-stu-id="491db-151">The next example shows how to use this class in your window procedure.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="491db-152">Maus Verfolgungs Ereignisse erfordern eine zusätzliche Verarbeitung durch das System, sodass Sie deaktiviert bleiben, wenn Sie Sie nicht benötigen.</span><span class="sxs-lookup"><span data-stu-id="491db-152">Mouse tracking events require additional processing by the system, so leave them disabled if you do not need them.</span></span>

<span data-ttu-id="491db-153">Aus Gründen der Vollständigkeit ist hier eine Funktion, die das System auf das standardmäßige Hover-Timeout abfragt.</span><span class="sxs-lookup"><span data-stu-id="491db-153">For completeness, here is a function that queries the system for the default hover timeout.</span></span>


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a><span data-ttu-id="491db-154">Mausrad</span><span class="sxs-lookup"><span data-stu-id="491db-154">Mouse Wheel</span></span>

<span data-ttu-id="491db-155">Die folgende Funktion überprüft, ob ein Mausrad vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="491db-155">The following function checks if a mouse wheel is present.</span></span>


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



<span data-ttu-id="491db-156">Wenn der Benutzer das Mausrad dreht, empfängt das Fenster mit dem Fokus eine [**WM- \_ MouseWheel**](/windows/desktop/inputdev/wm-mousewheel) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="491db-156">If the user rotates the mouse wheel, the window with focus receives a [**WM\_MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) message.</span></span> <span data-ttu-id="491db-157">Der *wParam* -Parameter dieser Nachricht enthält einen ganzzahligen Wert, der als *Delta* bezeichnet wird und misst, wie weit das Rad gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="491db-157">The *wParam* parameter of this message contains an integer value called the *delta* that measures how far the wheel was rotated.</span></span> <span data-ttu-id="491db-158">Das Delta verwendet beliebige Einheiten, wobei 120 Einheiten als Drehung definiert werden, die zum Ausführen einer Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="491db-158">The delta uses arbitrary units, where 120 units is defined as the rotation needed to perform one "action."</span></span> <span data-ttu-id="491db-159">Die Definition einer Aktion hängt natürlich von Ihrem Programm ab.</span><span class="sxs-lookup"><span data-stu-id="491db-159">Of course, the definition of an action depends on your program.</span></span> <span data-ttu-id="491db-160">Wenn das Mausrad z. b. zum Scrollen von Text verwendet wird, werden die einzelnen 120 Einheiten der Drehung in einer Textzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="491db-160">For example, if the mouse wheel is used to scroll text, each 120 units of rotation would scroll one line of text.</span></span>

<span data-ttu-id="491db-161">Das Vorzeichen des Deltas gibt die Richtung der Drehung an:</span><span class="sxs-lookup"><span data-stu-id="491db-161">The sign of the delta indicates the direction of rotation:</span></span>

-   <span data-ttu-id="491db-162">Positiv: Drehen Sie vorwärts, vom Benutzer entfernt.</span><span class="sxs-lookup"><span data-stu-id="491db-162">Positive: Rotate forward, away from the user.</span></span>
-   <span data-ttu-id="491db-163">Negativ: Drehen Sie rückwärts zu dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="491db-163">Negative: Rotate backward, toward the user.</span></span>

<span data-ttu-id="491db-164">Der Wert des Deltas wird zusammen mit einigen zusätzlichen Flags in *wParam* platziert.</span><span class="sxs-lookup"><span data-stu-id="491db-164">The value of the delta is placed in *wParam* along with some additional flags.</span></span> <span data-ttu-id="491db-165">Verwenden Sie das [**get \_ Wheel \_ Delta \_ wParam**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) -Makro, um den Wert des Deltas zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="491db-165">Use the [**GET\_WHEEL\_DELTA\_WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) macro to get the value of the delta.</span></span>


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="491db-166">Wenn das Mausrad eine hohe Auflösung aufweist, kann der absolute Wert des Deltas kleiner als 120 sein.</span><span class="sxs-lookup"><span data-stu-id="491db-166">If the mouse wheel has a high resolution, the absolute value of the delta might be less than 120.</span></span> <span data-ttu-id="491db-167">Wenn es in diesem Fall sinnvoll ist, die Aktion in kleineren Schritten durchzuführen, können Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="491db-167">In that case, if it makes sense for the action to occur in smaller increments, you can do so.</span></span> <span data-ttu-id="491db-168">Beispielsweise kann Text durch Inkremente von weniger als einer Zeile scrollen.</span><span class="sxs-lookup"><span data-stu-id="491db-168">For example, text could scroll by increments of less than one line.</span></span> <span data-ttu-id="491db-169">Akkumulieren Sie andernfalls das gesamte Delta, bis das Rad genug dreht, um die Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="491db-169">Otherwise, accumulate the total delta until the wheel rotates enough to perform the action.</span></span> <span data-ttu-id="491db-170">Speichern Sie das nicht verwendete Delta in einer Variablen, und führen Sie die Aktion aus, wenn 120 Einheiten akkumuliert werden (entweder positiv oder negativ).</span><span class="sxs-lookup"><span data-stu-id="491db-170">Store the unused delta in a variable, and when 120 units accumulate (either positive or negative), perform the action.</span></span>

## <a name="next"></a><span data-ttu-id="491db-171">Nächste</span><span class="sxs-lookup"><span data-stu-id="491db-171">Next</span></span>

[<span data-ttu-id="491db-172">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="491db-172">Keyboard Input</span></span>](keyboard-input.md)

 

 