---
title: Antworten auf Mausklicks
description: Antworten auf Mausklicks
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101619"
---
# <a name="responding-to-mouse-clicks"></a><span data-ttu-id="44aac-103">Antworten auf Mausklicks</span><span class="sxs-lookup"><span data-stu-id="44aac-103">Responding to Mouse Clicks</span></span>

<span data-ttu-id="44aac-104">Wenn der Benutzer auf eine Maustaste klickt, während sich der Cursor über dem Client Bereich eines Fensters befindet, empfängt das Fenster eine der folgenden Meldungen.</span><span class="sxs-lookup"><span data-stu-id="44aac-104">If the user clicks a mouse button while the cursor is over the client area of a window, the window receives one of the following messages.</span></span>



| <span data-ttu-id="44aac-105">Nachricht</span><span class="sxs-lookup"><span data-stu-id="44aac-105">Message</span></span>                                        | <span data-ttu-id="44aac-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="44aac-106">Meaning</span></span>                   |
|------------------------------------------------|---------------------------|
| [<span data-ttu-id="44aac-107">**WM \_ lbuttondown**</span><span class="sxs-lookup"><span data-stu-id="44aac-107">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown) | <span data-ttu-id="44aac-108">Linke Schaltfläche nach unten</span><span class="sxs-lookup"><span data-stu-id="44aac-108">Left button down</span></span>          |
| [<span data-ttu-id="44aac-109">**WM- \_ lbuttonup**</span><span class="sxs-lookup"><span data-stu-id="44aac-109">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)     | <span data-ttu-id="44aac-110">Linke Schaltfläche nach oben</span><span class="sxs-lookup"><span data-stu-id="44aac-110">Left button up</span></span>            |
| [<span data-ttu-id="44aac-111">**WM- \_ mbuttondown**</span><span class="sxs-lookup"><span data-stu-id="44aac-111">**WM\_MBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-mbuttondown) | <span data-ttu-id="44aac-112">Mittlere Schaltfläche nach unten</span><span class="sxs-lookup"><span data-stu-id="44aac-112">Middle button down</span></span>        |
| [<span data-ttu-id="44aac-113">**WM- \_ mbuttonup**</span><span class="sxs-lookup"><span data-stu-id="44aac-113">**WM\_MBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-mbuttonup)     | <span data-ttu-id="44aac-114">Mittlere Schaltfläche nach oben</span><span class="sxs-lookup"><span data-stu-id="44aac-114">Middle button up</span></span>          |
| [<span data-ttu-id="44aac-115">**WM- \_ rbuttondown**</span><span class="sxs-lookup"><span data-stu-id="44aac-115">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown) | <span data-ttu-id="44aac-116">Nach-rechts-Taste</span><span class="sxs-lookup"><span data-stu-id="44aac-116">Right button down</span></span>         |
| [<span data-ttu-id="44aac-117">**WM- \_ rbuttonup**</span><span class="sxs-lookup"><span data-stu-id="44aac-117">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)     | <span data-ttu-id="44aac-118">Rechter Schaltfläche nach oben</span><span class="sxs-lookup"><span data-stu-id="44aac-118">Right button up</span></span>           |
| [<span data-ttu-id="44aac-119">**WM- \_ xbuttondown**</span><span class="sxs-lookup"><span data-stu-id="44aac-119">**WM\_XBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-xbuttondown) | <span data-ttu-id="44aac-120">XButton1 oder XButton2 Down</span><span class="sxs-lookup"><span data-stu-id="44aac-120">XBUTTON1 or XBUTTON2 down</span></span> |
| [<span data-ttu-id="44aac-121">**WM- \_ xbuttonup**</span><span class="sxs-lookup"><span data-stu-id="44aac-121">**WM\_XBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-xbuttonup)     | <span data-ttu-id="44aac-122">XButton1 oder XButton2 up</span><span class="sxs-lookup"><span data-stu-id="44aac-122">XBUTTON1 or XBUTTON2 up</span></span>   |



 

<span data-ttu-id="44aac-123">Beachten Sie, dass der Client Bereich der Teil des Fensters ist, in dem der Frame ausgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="44aac-123">Recall that the client area is the portion of the window that excludes the frame.</span></span> <span data-ttu-id="44aac-124">Weitere Informationen zu Client Bereichen finden Sie unter [Was ist ein Fenster?](what-is-a-window-.md)</span><span class="sxs-lookup"><span data-stu-id="44aac-124">For more information about client areas, see [What Is a Window?](what-is-a-window-.md)</span></span>

### <a name="mouse-coordinates"></a><span data-ttu-id="44aac-125">Maus Koordinaten</span><span class="sxs-lookup"><span data-stu-id="44aac-125">Mouse Coordinates</span></span>

<span data-ttu-id="44aac-126">In allen diesen Nachrichten enthält der *LPARAM* -Parameter die x-und y-Koordinaten des Mauszeigers.</span><span class="sxs-lookup"><span data-stu-id="44aac-126">In all of these messages, the *lParam* parameter contains the x- and y-coordinates of the mouse pointer.</span></span> <span data-ttu-id="44aac-127">Die niedrigsten 16 Bits von *LPARAM* enthalten die x-Koordinate, und die nächsten 16 Bits enthalten die y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="44aac-127">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="44aac-128">Verwenden Sie die lParam-Makros [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) , um die Koordinaten aus *LPARAM* zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="44aac-128">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="44aac-129">Diese Makros sind in der Header Datei WINDOWSX. h definiert.</span><span class="sxs-lookup"><span data-stu-id="44aac-129">These macros are defined in the header file WindowsX.h.</span></span>

<span data-ttu-id="44aac-130">Bei 64-Bit-Fenstern ist *LPARAM* 64-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="44aac-130">On 64-bit Windows, *lParam* is 64-bit value.</span></span> <span data-ttu-id="44aac-131">Die oberen 32 Bits von *LPARAM* werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44aac-131">The upper 32 bits of *lParam* are not used.</span></span> <span data-ttu-id="44aac-132">In der MSDN-Dokumentation werden das "nieder wertige Wort" und "High-Order Word" von *LPARAM* erwähnt.</span><span class="sxs-lookup"><span data-stu-id="44aac-132">The MSDN documentation mentions the "low-order word" and "high-order word" of *lParam*.</span></span> <span data-ttu-id="44aac-133">Im 64-Bit-Fall bedeutet dies, dass das niedrige und das hochwertige Wort der unteren 32 Bits ist.</span><span class="sxs-lookup"><span data-stu-id="44aac-133">In the 64-bit case, this means the low- and high-order words of the lower 32 bits.</span></span> <span data-ttu-id="44aac-134">Die Makros extrahieren die richtigen Werte, sodass Sie sicher sind, wenn Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="44aac-134">The macros extract the right values, so if you use them, you will be safe.</span></span>

<span data-ttu-id="44aac-135">Maus Koordinaten werden in Pixel angegeben, nicht in geräteunabhängigen Pixeln (Dips) und werden relativ zum Client Bereich des Fensters gemessen.</span><span class="sxs-lookup"><span data-stu-id="44aac-135">Mouse coordinates are given in pixels, not device-independent pixels (DIPs), and are measured relative to the client area of the window.</span></span> <span data-ttu-id="44aac-136">Koordinaten sind signierte Werte.</span><span class="sxs-lookup"><span data-stu-id="44aac-136">Coordinates are signed values.</span></span> <span data-ttu-id="44aac-137">Positionen oberhalb und Links vom Client Bereich haben negative Koordinaten, was wichtig ist, wenn Sie die Mausposition außerhalb des Fensters verfolgen.</span><span class="sxs-lookup"><span data-stu-id="44aac-137">Positions above and to the left of the client area have negative coordinates, which is important if you track the mouse position outside the window.</span></span> <span data-ttu-id="44aac-138">Dies wird in einem späteren Thema erläutert, wobei [die Mausbewegung außerhalb des Fensters erfasst](mouse-movement.md)wird.</span><span class="sxs-lookup"><span data-stu-id="44aac-138">We will see how to do that in a later topic, [Capturing Mouse Movement Outside the Window](mouse-movement.md).</span></span>

### <a name="additional-flags"></a><span data-ttu-id="44aac-139">Zusätzliche Flags</span><span class="sxs-lookup"><span data-stu-id="44aac-139">Additional Flags</span></span>

<span data-ttu-id="44aac-140">Der *wParam* -Parameter enthält ein bitweises **or** von-Flags, das den Zustand der anderen Maustasten sowie die UMSCHALTTASTE und die STRG-Taste angibt.</span><span class="sxs-lookup"><span data-stu-id="44aac-140">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span>



| <span data-ttu-id="44aac-141">Flag</span><span class="sxs-lookup"><span data-stu-id="44aac-141">Flag</span></span>             | <span data-ttu-id="44aac-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="44aac-142">Meaning</span></span>                          |
|------------------|----------------------------------|
| <span data-ttu-id="44aac-143">**MK- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="44aac-143">**MK\_CONTROL**</span></span>  | <span data-ttu-id="44aac-144">Die STRG-Taste ist nicht gedrückt.</span><span class="sxs-lookup"><span data-stu-id="44aac-144">The CTRL key is down.</span></span>            |
| <span data-ttu-id="44aac-145">**MK \_ lbutton**</span><span class="sxs-lookup"><span data-stu-id="44aac-145">**MK\_LBUTTON**</span></span>  | <span data-ttu-id="44aac-146">Die linke Maustaste ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="44aac-146">The left mouse button is down.</span></span>   |
| <span data-ttu-id="44aac-147">**MK- \_ MButton**</span><span class="sxs-lookup"><span data-stu-id="44aac-147">**MK\_MBUTTON**</span></span>  | <span data-ttu-id="44aac-148">Die mittlere Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44aac-148">The middle mouse button is down.</span></span> |
| <span data-ttu-id="44aac-149">**MK \_ rbutton**</span><span class="sxs-lookup"><span data-stu-id="44aac-149">**MK\_RBUTTON**</span></span>  | <span data-ttu-id="44aac-150">Die Rechte Maustaste ist nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44aac-150">The right mouse button is down.</span></span>  |
| <span data-ttu-id="44aac-151">**MK \_ UMSCHALT**</span><span class="sxs-lookup"><span data-stu-id="44aac-151">**MK\_SHIFT**</span></span>    | <span data-ttu-id="44aac-152">Die UMSCHALTTASTE ist nicht mehr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44aac-152">The SHIFT key is down.</span></span>           |
| <span data-ttu-id="44aac-153">**MK \_ XButton1**</span><span class="sxs-lookup"><span data-stu-id="44aac-153">**MK\_XBUTTON1**</span></span> | <span data-ttu-id="44aac-154">Die Schaltfläche XButton1 ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44aac-154">The XBUTTON1 button is down.</span></span>     |
| <span data-ttu-id="44aac-155">**MK \_ XButton2**</span><span class="sxs-lookup"><span data-stu-id="44aac-155">**MK\_XBUTTON2**</span></span> | <span data-ttu-id="44aac-156">Die Schaltfläche XButton2 ist nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44aac-156">The XBUTTON2 button is down.</span></span>     |



 

<span data-ttu-id="44aac-157">Das Fehlen eines Flags bedeutet, dass die entsprechende Schaltfläche oder der entsprechende Schlüssel nicht gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="44aac-157">The absence of a flag means the corresponding button or key was not pressed.</span></span> <span data-ttu-id="44aac-158">So können Sie beispielsweise testen, ob die STRG-Taste gedrückt ist:</span><span class="sxs-lookup"><span data-stu-id="44aac-158">For example, to test whether the CTRL key is down:</span></span>


```C++
if (wParam & MK_CONTROL) { ...
```



<span data-ttu-id="44aac-159">Wenn Sie neben STRG und UMSCHALT den Zustand anderer Schlüssel ermitteln müssen, verwenden Sie die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Funktion, die in [Tastatureingaben](keyboard-input.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="44aac-159">If you need to find the state of other keys besides CTRL and SHIFT, use the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function, which is described in [Keyboard Input](keyboard-input.md).</span></span>

<span data-ttu-id="44aac-160">Die Nachrichten " [**WM \_ xbuttondown**](/windows/desktop/inputdev/wm-xbuttondown) " und " [**WM \_ xbuttonup" werden**](/windows/desktop/inputdev/wm-xbuttonup) sowohl auf XButton1 als auch auf XButton2 angewendet.</span><span class="sxs-lookup"><span data-stu-id="44aac-160">The [**WM\_XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) and [**WM\_XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) window messages apply to both XBUTTON1 and XBUTTON2.</span></span> <span data-ttu-id="44aac-161">Der *wParam* -Parameter gibt an, auf welche Schaltfläche geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="44aac-161">The *wParam* parameter indicates which button was clicked.</span></span>


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a><span data-ttu-id="44aac-162">Doppelte Klicks</span><span class="sxs-lookup"><span data-stu-id="44aac-162">Double Clicks</span></span>

<span data-ttu-id="44aac-163">Ein Fenster erhält standardmäßig keine Doppelklick-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="44aac-163">A window does not receive double-click notifications by default.</span></span> <span data-ttu-id="44aac-164">Um doppelte Klicks zu erhalten, legen Sie das **CS \_ dblclert** -Flag in der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur fest, wenn Sie die Fenster Klasse registrieren.</span><span class="sxs-lookup"><span data-stu-id="44aac-164">To receive double clicks, set the **CS\_DBLCLKS** flag in the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when you register the window class.</span></span>


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



<span data-ttu-id="44aac-165">Wenn Sie das Flag **CS \_ dblclcs** wie gezeigt festlegen, empfängt das Fenster Doppelklick-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="44aac-165">If you set the **CS\_DBLCLKS** flag as shown, the window will receive double-click notifications.</span></span> <span data-ttu-id="44aac-166">Ein Doppelklick wird durch eine Fenster Meldung mit dem Namen "dblclk" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44aac-166">A double click is indicated by a window message with "DBLCLK" in the name.</span></span> <span data-ttu-id="44aac-167">Ein Doppelklick mit der linken Maustaste erzeugt beispielsweise die folgende Sequenz von Meldungen:</span><span class="sxs-lookup"><span data-stu-id="44aac-167">For example, a double click on the left mouse button produces the following sequence of messages:</span></span>

<dl>

[<span data-ttu-id="44aac-168">**WM \_ lbuttondown**</span><span class="sxs-lookup"><span data-stu-id="44aac-168">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)  
[<span data-ttu-id="44aac-169">**WM- \_ lbuttonup**</span><span class="sxs-lookup"><span data-stu-id="44aac-169">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
[<span data-ttu-id="44aac-170">**WM \_ lbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="44aac-170">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)  
[<span data-ttu-id="44aac-171">**WM- \_ lbuttonup**</span><span class="sxs-lookup"><span data-stu-id="44aac-171">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

<span data-ttu-id="44aac-172">Tatsächlich wird die zweite [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldung, die normalerweise generiert wird, zu einer [**WM \_ lbuttondblclk**](/windows/desktop/inputdev/wm-lbuttondblclk) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="44aac-172">In effect, the second [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message that would normally be generated becomes a [**WM\_LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) message.</span></span> <span data-ttu-id="44aac-173">Äquivalente Nachrichten werden für die Schaltflächen right, Middle und XButton definiert.</span><span class="sxs-lookup"><span data-stu-id="44aac-173">Equivalent messages are defined for right, middle, and XBUTTON buttons.</span></span>

<span data-ttu-id="44aac-174">Bis Sie die Doppelklick Nachricht erhalten haben, gibt es keine Möglichkeit, zu erkennen, dass der erste Mausklick den Anfang eines Doppelklicks enthält.</span><span class="sxs-lookup"><span data-stu-id="44aac-174">Until you get the double-click message, there is no way to tell that the first mouse click is the start of a double click.</span></span> <span data-ttu-id="44aac-175">Aus diesem Grund sollte eine Doppelklick Aktion eine Aktion fortsetzen, die mit dem ersten Mausklick beginnt.</span><span class="sxs-lookup"><span data-stu-id="44aac-175">Therefore, a double-click action should continue an action that begins with the first mouse click.</span></span> <span data-ttu-id="44aac-176">Beispielsweise wird in der Windows-Shell mit einem einzigen Klick ein Ordner ausgewählt, während mit einem Doppelklick der Ordner geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="44aac-176">For example, in the Windows Shell, a single click selects a folder, while a double click opens the folder.</span></span>

## <a name="non-client-mouse-messages"></a><span data-ttu-id="44aac-177">Nicht-Client-Maus Meldungen</span><span class="sxs-lookup"><span data-stu-id="44aac-177">Non-client Mouse Messages</span></span>

<span data-ttu-id="44aac-178">Für Mausereignisse, die im nicht-Client Bereich des Fensters auftreten, wird ein separater Satz von Meldungen definiert.</span><span class="sxs-lookup"><span data-stu-id="44aac-178">A separate set of messages are defined for mouse events that occur within the non-client area of the window.</span></span> <span data-ttu-id="44aac-179">Diese Nachrichten enthalten den Buchstaben "NC" im Namen.</span><span class="sxs-lookup"><span data-stu-id="44aac-179">These messages have the letters "NC" in the name.</span></span> <span data-ttu-id="44aac-180">Beispielsweise ist [**WM \_ nclbuttondown**](/windows/desktop/inputdev/wm-nclbuttondown) die nicht-Client-Entsprechung von [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="44aac-180">For example, [**WM\_NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) is the non-client equivalent of [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="44aac-181">Diese Nachrichten werden von einer typischen Anwendung nicht abgefangen, da diese Nachrichten von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ordnungsgemäß verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="44aac-181">A typical application will not intercept these messages, because the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function handles these messages correctly.</span></span> <span data-ttu-id="44aac-182">Allerdings können Sie für bestimmte erweiterte Funktionen nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="44aac-182">However, they can be useful for certain advanced functions.</span></span> <span data-ttu-id="44aac-183">Beispielsweise können Sie diese Nachrichten verwenden, um ein benutzerdefiniertes Verhalten in der Titelleiste zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="44aac-183">For example, you could use these messages to implement custom behavior in the title bar.</span></span> <span data-ttu-id="44aac-184">Wenn Sie diese Nachrichten verarbeiten, sollten Sie Sie in der Regel an **defwindowproc** weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="44aac-184">If you do handle these messages, you should generally pass them to **DefWindowProc** afterward.</span></span> <span data-ttu-id="44aac-185">Andernfalls werden von der Anwendung Standardfunktionen wie z. b. ziehen oder Minimieren des Fensters unterbricht.</span><span class="sxs-lookup"><span data-stu-id="44aac-185">Otherwise, your application will break standard functionality such as dragging or minimizing the window.</span></span>

## <a name="next"></a><span data-ttu-id="44aac-186">Nächste</span><span class="sxs-lookup"><span data-stu-id="44aac-186">Next</span></span>

[<span data-ttu-id="44aac-187">Mausbewegung</span><span class="sxs-lookup"><span data-stu-id="44aac-187">Mouse Movement</span></span>](mouse-movement.md)

 

 