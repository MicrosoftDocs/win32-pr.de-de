---
title: Benutzerdefinierter Fensterrahmen mithilfe von DWM
description: In diesem Thema wird veranschaulicht, wie Sie die Desktopfenster-Manager (DWM)-APIs verwenden, um benutzerdefinierte Fensterrahmen für Ihre Anwendung zu erstellen.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Desktopfenster-Manager (DWM), benutzerdefinierte Fensterrahmen
- Dwm (Desktopfenster-Manager), benutzerdefinierte Fensterrahmen
- benutzerdefinierte Fensterrahmen
- Entfernen von Standard Frames
- Erweitern von Client Frames
- Desktopfenster-Manager (DWM), Erweitern von Client Frames
- Dwm (Desktopfenster-Manager), Erweitern von Client Frames
- Desktopfenster-Manager (DWM), Standardrahmen entfernen
- Dwm (Desktopfenster-Manager), Standardrahmen werden entfernt
- Desktopfenster-Manager (DWM), zeichnen in erweiterten Frames
- Dwm (Desktopfenster-Manager), zeichnen in erweiterten Frames
- Zeichnen in erweiterten Frames
- Treffertests
- Desktopfenster-Manager (DWM), Treffer Test
- Dwm (Desktopfenster-Manager), Treffer Test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039575"
---
# <a name="custom-window-frame-using-dwm"></a><span data-ttu-id="e1ba3-118">Benutzerdefinierter Fensterrahmen mithilfe von DWM</span><span class="sxs-lookup"><span data-stu-id="e1ba3-118">Custom Window Frame Using DWM</span></span>

<span data-ttu-id="e1ba3-119">In diesem Thema wird veranschaulicht, wie Sie die Desktopfenster-Manager (DWM)-APIs verwenden, um benutzerdefinierte Fensterrahmen für Ihre Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-119">This topic demonstrates how to use the Desktop Window Manager (DWM) APIs to create custom window frames for your application.</span></span>

-   [<span data-ttu-id="e1ba3-120">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="e1ba3-120">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="e1ba3-121">Erweitern des Client Frames</span><span class="sxs-lookup"><span data-stu-id="e1ba3-121">Extending the Client Frame</span></span>](#extending-the-client-frame)
-   [<span data-ttu-id="e1ba3-122">Entfernen des Standard Rahmens</span><span class="sxs-lookup"><span data-stu-id="e1ba3-122">Removing the Standard Frame</span></span>](#removing-the-standard-frame)
-   [<span data-ttu-id="e1ba3-123">Zeichnen im erweiterten Rahmen Fenster</span><span class="sxs-lookup"><span data-stu-id="e1ba3-123">Drawing in the Extended Frame Window</span></span>](#drawing-in-the-extended-frame-window)
-   [<span data-ttu-id="e1ba3-124">Aktivieren von Treffer Tests für den benutzerdefinierten Frame</span><span class="sxs-lookup"><span data-stu-id="e1ba3-124">Enabling Hit Testing for the Custom Frame</span></span>](#enabling-hit-testing-for-the-custom-frame)
-   [<span data-ttu-id="e1ba3-125">Anhang A: Beispiel Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="e1ba3-125">Appendix A: Sample Window Procedure</span></span>](#appendix-a-sample-window-procedure)
-   [<span data-ttu-id="e1ba3-126">Anhang B: Zeichnen des Beschriftungs Titels</span><span class="sxs-lookup"><span data-stu-id="e1ba3-126">Appendix B: Painting the Caption Title</span></span>](#appendix-b-painting-the-caption-title)
-   [<span data-ttu-id="e1ba3-127">Anhang C: hittestnca-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1ba3-127">Appendix C: HitTestNCA Function</span></span>](#appendix-c-hittestnca-function)
-   [<span data-ttu-id="e1ba3-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1ba3-128">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="e1ba3-129">Einführung</span><span class="sxs-lookup"><span data-stu-id="e1ba3-129">Introduction</span></span>

<span data-ttu-id="e1ba3-130">In Windows Vista und höher wird die Darstellung der nicht-Client Bereiche von Anwendungs Fenstern (Titelleiste, Symbol, Fensterrahmen und Beschriftungs Schaltflächen) durch die DWM gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-130">In Windows Vista and later, the appearance of the non-client areas of application windows (the title bar, icon, window border, and caption buttons) is controlled by the DWM.</span></span> <span data-ttu-id="e1ba3-131">Mithilfe der DWM-APIs können Sie die Art und Weise ändern, in der die DWM den Rahmen eines Fensters rendert.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-131">Using the DWM APIs, you can change the way the DWM renders a window's frame.</span></span>

<span data-ttu-id="e1ba3-132">Ein Feature der DWM-APIs ist die Möglichkeit, den Anwendungs Frame in den Client Bereich zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-132">One feature of the DWM APIs is the ability to extend the application frame into the client area.</span></span> <span data-ttu-id="e1ba3-133">Dies ermöglicht es Ihnen, ein Client Benutzeroberflächen Element – z. b. eine Symbolleiste – in den Frame zu integrieren, sodass die UI-Steuerelemente in der Benutzeroberfläche der Anwendung wichtiger werden.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-133">This enables you to integrate a client UI element—such as a toolbar—into the frame, giving the UI controls a more prominent place in the application UI.</span></span> <span data-ttu-id="e1ba3-134">Windows Internet Explorer 7 unter Windows Vista integriert z. b. die Navigationsleiste in den Fensterrahmen, indem die obere Seite des Frames erweitert wird, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-134">For example, Windows Internet Explorer 7 on Windows Vista integrates the navigation bar into the window frame by extending the top of the frame as shown in the following screen shot.</span></span>

![Navigationsleiste, die in den Fensterrahmen integriert ist.](images/ie7-extendedborder-boxed.png)

<span data-ttu-id="e1ba3-136">Durch die Möglichkeit, den Fensterrahmen zu erweitern, können Sie auch benutzerdefinierte Frames erstellen und gleichzeitig das Aussehen und das Erscheinungsbild des Fensters beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-136">The ability to extend the window frame also enables you to create custom frames while maintaining the window's look and feel.</span></span> <span data-ttu-id="e1ba3-137">Microsoft Office Word 2007 zeichnet z. b. die Office-Schaltfläche und die Symbolleiste für den schnell Zugriff im benutzerdefinierten Frame und stellt dabei die Standard Schaltflächen Minimieren, maximieren und schließen bereit, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-137">For example, Microsoft Office Word 2007 draws the Office button and the Quick Access toolbar inside the custom frame while providing the standard Minimize, Maximize, and Close caption buttons, as shown in the following screen shot.</span></span>

![Office-Schaltfläche und Symbolleiste für den schnell Zugriff in Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a><span data-ttu-id="e1ba3-139">Erweitern des Client Frames</span><span class="sxs-lookup"><span data-stu-id="e1ba3-139">Extending the Client Frame</span></span>

<span data-ttu-id="e1ba3-140">Die Funktionalität zum Erweitern des Frames in den Client Bereich wird von der Funktion " [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) " verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-140">The functionality to extend the frame into the client area is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span> <span data-ttu-id="e1ba3-141">Um den Frame zu erweitern, übergeben Sie das Handle des Zielfensters mit den Margin-einfügen-Werten an **DwmExtendFrameIntoClientArea**.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-141">To extend the frame, pass the handle of the target window together with the margin inset values to **DwmExtendFrameIntoClientArea**.</span></span> <span data-ttu-id="e1ba3-142">Die Werte für den Margin-Wert legen fest, wie weit der Frame auf den vier Seiten des Fensters erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-142">The margin inset values determine how far to extend the frame on the four sides of the window.</span></span>

<span data-ttu-id="e1ba3-143">Der folgende Code veranschaulicht die Verwendung von [**dwmextendframeinumclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) zum Erweitern des Frames.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-143">The following code demonstrates the use of [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to extend the frame.</span></span>


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="e1ba3-144">Beachten Sie, dass die Frame Erweiterung innerhalb der [**WM- \_ Aktivierungs**](/windows/desktop/inputdev/wm-activate) Nachricht statt in der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-144">Note that the frame extension is done within the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message rather than the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="e1ba3-145">Dadurch wird sichergestellt, dass die Frame Erweiterung ordnungsgemäß verarbeitet wird, wenn das Fenster seine Standardgröße hat und wenn es maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-145">This ensures that frame extension is handled properly when the window is at its default size and when it is maximized.</span></span>

<span data-ttu-id="e1ba3-146">In der folgenden Abbildung wird ein Standardfenster Rahmen (auf der linken Seite) und der erweiterte Fensterrahmen (auf der rechten Seite) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-146">The following image shows a standard window frame (on the left) and the same window frame extended (on the right).</span></span> <span data-ttu-id="e1ba3-147">Der Frame wird mit dem vorherigen Codebeispiel und dem Standard Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Hintergrund (Farb \_ Fenster + 1) erweitert.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-147">The frame is extended using the previous code example and the default Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)/[**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (COLOR\_WINDOW +1).</span></span>

![Screenshot eines standardmäßigen (linken) und erweiterten Rahmens (rechts) mit weißem Hintergrund](images/white-sidebyside.png)

<span data-ttu-id="e1ba3-149">Der visuelle Unterschied zwischen diesen beiden Fenstern ist sehr gering.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-149">The visual difference between these two windows is very subtle.</span></span> <span data-ttu-id="e1ba3-150">Der einzige Unterschied zwischen den beiden besteht darin, dass der schlanke schwarze Linien Rand des Client Bereichs im Fenster links im Fenster auf der rechten Seite fehlt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-150">The only difference between the two is that the thin black line border of the client region in the window on the left is missing from the window on the right.</span></span> <span data-ttu-id="e1ba3-151">Der Grund für diese fehlende Grenze ist, dass Sie in den erweiterten Frame integriert ist, aber der Rest des Client Bereichs ist nicht.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-151">The reason for this missing border is that it is incorporated into the extended frame, but the rest of the client area is not.</span></span> <span data-ttu-id="e1ba3-152">Damit die erweiterten Frames sichtbar sind, müssen die Regionen, die den einzelnen Seiten des erweiterten Frames zugrunde liegen, Pixeldaten mit einem Alphawert von 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-152">For the extended frames to be visible, the regions underlying each of the extended frame's sides must have pixel data with an alpha value of 0.</span></span> <span data-ttu-id="e1ba3-153">Der schwarze Rahmen um den Client Bereich verfügt über Pixeldaten, in denen alle Farbwerte (rot, grün, blau und Alpha) auf 0 festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-153">The black border around the client region has pixel data in which all color values (red, green, blue, and alpha) are set to 0.</span></span> <span data-ttu-id="e1ba3-154">Im restlichen Hintergrund ist der Alpha-Wert nicht auf 0 festgelegt, sodass der restliche Rahmen nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-154">The rest of the background does not have the alpha value set to 0, so the rest of the extended frame is not visible.</span></span>

<span data-ttu-id="e1ba3-155">Die einfachste Möglichkeit, um sicherzustellen, dass die erweiterten Frames sichtbar sind, besteht darin, den gesamten Client Bereich schwarz zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-155">The easiest way to ensure that the extended frames are visible is to paint the entire client region black.</span></span> <span data-ttu-id="e1ba3-156">Um dies zu erreichen, initialisieren Sie den *hbrbackground* -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -oder [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur mit dem Handle des Stock Black- \_ Pinsels.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-156">To accomplish this, initialize the *hbrBackground* member of your [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure to the handle of the stock BLACK\_BRUSH.</span></span> <span data-ttu-id="e1ba3-157">Die folgende Abbildung zeigt den gleichen Standard Frame (links) und den erweiterten Frame (rechts), der zuvor gezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-157">The following image shows the same standard frame (left) and extended frame (right) shown previously.</span></span> <span data-ttu-id="e1ba3-158">Dieses Mal wird jedoch *hbrbackground* auf das schwarze Pinsel handle festgelegt, das \_ von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-158">This time, however, *hbrBackground* is set to the BLACK\_BRUSH handle obtained from the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) function.</span></span>

![Screenshot eines standardmäßigen (linken) und erweiterten Rahmens (rechts) mit schwarzem Hintergrund](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a><span data-ttu-id="e1ba3-160">Entfernen des Standard Rahmens</span><span class="sxs-lookup"><span data-stu-id="e1ba3-160">Removing the Standard Frame</span></span>

<span data-ttu-id="e1ba3-161">Nachdem Sie den Frame der Anwendung erweitert und sichtbar gemacht haben, können Sie den Standard Frame entfernen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-161">After you have extended the frame of your application and made it visible, you can remove the standard frame.</span></span> <span data-ttu-id="e1ba3-162">Wenn Sie den Standardrahmen entfernen, können Sie die Breite jeder Seite des Frames steuern, anstatt einfach den Standardrahmen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-162">Removing the standard frame enables you to control the width of each side of the frame rather than simply extending the standard frame.</span></span>

<span data-ttu-id="e1ba3-163">Um den Standardfenster Rahmen zu entfernen, müssen Sie die [**WM- \_ nccalcsize**](/windows/desktop/winmsg/wm-nccalcsize) -Nachricht behandeln, insbesondere wenn der *wParam* -Wert " **true** " und der Rückgabewert "0" ist.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-163">To remove the standard window frame, you must handle the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message, specifically when its *wParam* value is **TRUE** and the return value is 0.</span></span> <span data-ttu-id="e1ba3-164">Dadurch wird die gesamte Fenster Region als Client Bereich verwendet, wobei der Standardrahmen entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-164">By doing so, your application uses the entire window region as the client area, removing the standard frame.</span></span>

<span data-ttu-id="e1ba3-165">Die Ergebnisse der Verarbeitung der [**WM- \_ nccalcsize**](/windows/desktop/winmsg/wm-nccalcsize) -Nachricht sind erst sichtbar, wenn die Größe des Client Bereichs geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-165">The results of handling the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message are not visible until the client region needs to be resized.</span></span> <span data-ttu-id="e1ba3-166">Bis zu diesem Zeitpunkt wird die anfängliche Ansicht des Fensters mit dem Standardrahmen und den erweiterten Rahmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-166">Until that time, the initial view of the window appears with the standard frame and extended borders.</span></span> <span data-ttu-id="e1ba3-167">Um dies zu umgehen, müssen Sie entweder die Größe des Fensters ändern oder eine Aktion ausführen, die zum Zeitpunkt der Fenster Erstellung eine **WM- \_ nccalcsize** -Nachricht auslöst.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-167">To overcome this, you must either resize your window or perform an action that initiates a **WM\_NCCALCSIZE** message at the time of window creation.</span></span> <span data-ttu-id="e1ba3-168">Dies kann mithilfe der [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion erreicht werden, um das Fenster zu verschieben und seine Größe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-168">This can be accomplished by using the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move your window and resize it.</span></span> <span data-ttu-id="e1ba3-169">Der folgende Code veranschaulicht einen Aufrufen von **SetWindowPos** , der erzwingt, dass eine **WM- \_ nccalcsize** -Nachricht mithilfe der aktuellen Fenster Rechteck Attribute und des das- \_ Flag "framechanout" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-169">The following code demonstrates a call to **SetWindowPos** that forces a **WM\_NCCALCSIZE** message to be sent using the current window rectangle attributes and the SWP\_FRAMECHANGED flag.</span></span>


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="e1ba3-170">In der folgenden Abbildung wird der Standardrahmen (links) und der neu erweiterte Rahmen ohne den Standardrahmen (right) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-170">The following image shows the standard frame (left) and the newly extended frame without the standard frame (right).</span></span>

![Screenshot eines Standardrahmens (links) und benutzerdefiniertem Frame (rechts)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a><span data-ttu-id="e1ba3-172">Zeichnen im erweiterten Rahmen Fenster</span><span class="sxs-lookup"><span data-stu-id="e1ba3-172">Drawing in the Extended Frame Window</span></span>

<span data-ttu-id="e1ba3-173">Wenn Sie den Standardrahmen entfernen, verlieren Sie das automatische Zeichnen des Anwendungs Symbols und des Titels.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-173">By removing the standard frame, you lose the automatic drawing of the application icon and title.</span></span> <span data-ttu-id="e1ba3-174">Wenn Sie diese wieder der Anwendung hinzufügen möchten, müssen Sie Sie selbst zeichnen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-174">To add these back to your application, you must draw them yourself.</span></span> <span data-ttu-id="e1ba3-175">Betrachten Sie hierzu zunächst die Änderung, die in Ihrem Client Bereich aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-175">To do this, first look at the change that has occurred to your client area.</span></span>

<span data-ttu-id="e1ba3-176">Wenn Sie den Standard Frame entfernen, besteht der Client Bereich nun aus dem gesamten Fenster, einschließlich des erweiterten Frames.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-176">With the removal of the standard frame, your client area now consists of the entire window, including the extended frame.</span></span> <span data-ttu-id="e1ba3-177">Dies umfasst die Region, in der die Beschriftungs Schaltflächen gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-177">This includes the region where the caption buttons are drawn.</span></span> <span data-ttu-id="e1ba3-178">In der folgenden Seite-an-Seite-Vergleich wird der Client Bereich für den Standard Frame und den benutzerdefinierten erweiterten Frame rot hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-178">In the following side-by-side comparison, the client area for both the standard frame and the custom extended frame is highlighted in red.</span></span> <span data-ttu-id="e1ba3-179">Der Client Bereich für das Standardrahmen Fenster (links) ist der schwarze Bereich.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-179">The client area for the standard frame window (left) is the black region.</span></span> <span data-ttu-id="e1ba3-180">Im erweiterten Rahmen Fenster (rechts) ist der Client Bereich das gesamte Fenster.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-180">On the extended frame window (right), the client area is the entire window.</span></span>

![Screenshot eines rot markierten Client Bereichs in Standard-und benutzerdefiniertem Frame](images/clientarea-sidebyside.png)

<span data-ttu-id="e1ba3-182">Da es sich bei dem gesamten Fenster um Ihren Client Bereich handelt, können Sie einfach die gewünschten Elemente im erweiterten Frame zeichnen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-182">Because the entire window is your client area, you can simply draw what you want in the extended frame.</span></span> <span data-ttu-id="e1ba3-183">Um der Anwendung einen Titel hinzuzufügen, zeichnen Sie einfach Text in der entsprechenden Region.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-183">To add a title to your application, just draw text in the appropriate region.</span></span> <span data-ttu-id="e1ba3-184">Die folgende Abbildung zeigt den Text für den Text, der im benutzerdefinierten Beschriftungs Rahmen gezeichnet wurde</span><span class="sxs-lookup"><span data-stu-id="e1ba3-184">The following image shows themed text drawn on the custom caption frame.</span></span> <span data-ttu-id="e1ba3-185">Der Titel wird mithilfe der [**drawdermetextex**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) -Funktion gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-185">The title is drawn using the [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="e1ba3-186">Informationen zum Anzeigen des Codes, der den Titel zeichnet, finden Sie unter [Anhang B: Zeichnen des Beschriftungs Titels](#appendix-b-painting-the-caption-title).</span><span class="sxs-lookup"><span data-stu-id="e1ba3-186">To view the code that paints the title, see [Appendix B: Painting the Caption Title](#appendix-b-painting-the-caption-title).</span></span>

![Screenshot eines benutzerdefinierten Frames mit dem Titel](images/custom-caption-title.png)

> [!Note]  
> <span data-ttu-id="e1ba3-188">Wenn Sie in Ihren benutzerdefinierten Frame zeichnen, gehen Sie beim Platzieren von UI-Steuerelementen vorsichtig vor</span><span class="sxs-lookup"><span data-stu-id="e1ba3-188">When drawing in your custom frame, be careful when placing UI controls.</span></span> <span data-ttu-id="e1ba3-189">Da es sich bei dem gesamten Fenster um die Client Region handelt, müssen Sie die Platzierung des UI-Steuer Elements für jede Frame Breite anpassen, wenn Sie nicht im erweiterten Frame angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-189">Because the entire window is your client region, you must adjust your UI control placement for each frame width if you do not want them to appear on or in the extended frame.</span></span>

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a><span data-ttu-id="e1ba3-190">Aktivieren von Treffer Tests für den benutzerdefinierten Frame</span><span class="sxs-lookup"><span data-stu-id="e1ba3-190">Enabling Hit Testing for the Custom Frame</span></span>

<span data-ttu-id="e1ba3-191">Ein Nebeneffekt beim Entfernen des Standardrahmens ist der Verlust der standardmäßigen Änderung der Größe und des Verschiebungs Verhaltens.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-191">A side effect of removing the standard frame is the loss of the default resizing and moving behavior.</span></span> <span data-ttu-id="e1ba3-192">Damit Ihre Anwendung das Standardverhalten des Fensters ordnungsgemäß emulieren kann, müssen Sie eine Logik implementieren, um Treffer Tests für Beschriftungs Schaltflächen und die Größe der Frame Größe/Verschiebung zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="e1ba3-192">For your application to properly emulate standard window behavior, you will need to implement logic to handle caption button hit testing and frame resizing/moving.</span></span>

<span data-ttu-id="e1ba3-193">Für die Treffer Tests der Beschriftungs Schaltfläche stellt DWM die [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) -Funktion bereit.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-193">For caption button hit testing, DWM provides the [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="e1ba3-194">Um die Beschriftungs Schaltflächen in benutzerdefinierten Frame Szenarios ordnungsgemäß zu erreichen, sollten Nachrichten zur Behandlung an **DwmDefWindowProc** übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-194">To properly hit test the caption buttons in custom frame scenarios, messages should first be passed to **DwmDefWindowProc** for handling.</span></span> <span data-ttu-id="e1ba3-195">**DwmDefWindowProc** gibt **true** zurück, wenn eine Nachricht behandelt wird, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e1ba3-195">**DwmDefWindowProc** returns **TRUE** if a message is handled and **FALSE** if it is not.</span></span> <span data-ttu-id="e1ba3-196">Wenn die Nachricht nicht von **DwmDefWindowProc** behandelt wird, sollte die Anwendung die Nachricht selbst verarbeiten oder die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-196">If the message is not handled by **DwmDefWindowProc**, your application should handle the message itself or pass the message onto [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="e1ba3-197">Wenn Sie die Größe der Frame Größe ändern und verschieben, muss Ihre Anwendung die Treffer Test Logik bereitstellen und Frame-Treffer Testnachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-197">For frame resizing and moving, your application must provide the hit testing logic and handle frame hit test messages.</span></span> <span data-ttu-id="e1ba3-198">Frame Treffer Test-Meldungen werden über die WM- [**\_ nchittest**](/windows/desktop/inputdev/wm-nchittest) -Nachricht gesendet, auch wenn Ihre Anwendung einen benutzerdefinierten Frame ohne den Standardrahmen erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-198">Frame hit test messages are sent to you through the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message, even if your application creates a custom frame without the standard frame.</span></span> <span data-ttu-id="e1ba3-199">Der folgende Code veranschaulicht die Verarbeitung der **WM- \_ nchittest** -Nachricht, wenn Sie von [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) nicht behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-199">The following code demonstrates handling the **WM\_NCHITTEST** message when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle it.</span></span> <span data-ttu-id="e1ba3-200">Den Code der aufgerufenen Funktion finden Sie unter `HitTestNCA` [Anhang C: hittestnca-Funktion](#appendix-c-hittestnca-function).</span><span class="sxs-lookup"><span data-stu-id="e1ba3-200">To see the code of the called `HitTestNCA` function, see [Appendix C: HitTestNCA Function](#appendix-c-hittestnca-function).</span></span>


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a><span data-ttu-id="e1ba3-201">Anhang A: Beispiel Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="e1ba3-201">Appendix A: Sample Window Procedure</span></span>

<span data-ttu-id="e1ba3-202">Im folgenden Codebeispiel wird eine Fenster Prozedur und die unterstützenden workerfunktionen veranschaulicht, die zum Erstellen einer benutzerdefinierten Frame Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-202">The following code sample demonstrates a window procedure and its supporting worker functions used to create a custom frame application.</span></span>


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a><span data-ttu-id="e1ba3-203">Anhang B: Zeichnen des Beschriftungs Titels</span><span class="sxs-lookup"><span data-stu-id="e1ba3-203">Appendix B: Painting the Caption Title</span></span>

<span data-ttu-id="e1ba3-204">Der folgende Code veranschaulicht, wie Sie einen Beschriftungs Titel für den erweiterten Frame zeichnen.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-204">The following code demonstrates how to paint a caption title on the extended frame.</span></span> <span data-ttu-id="e1ba3-205">Diese Funktion muss in den [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) -und [**endpaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) -aufrufen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-205">This function must be called from within the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) calls.</span></span>


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a><span data-ttu-id="e1ba3-206">Anhang C: hittestnca-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1ba3-206">Appendix C: HitTestNCA Function</span></span>

<span data-ttu-id="e1ba3-207">Der folgende Code zeigt die-Funktion, die zum `HitTestNCA` [Aktivieren von Treffer Tests für den benutzerdefinierten Frame](#enabling-hit-testing-for-the-custom-frame)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-207">The following code shows the `HitTestNCA` function used in [Enabling Hit Testing for the Custom Frame](#enabling-hit-testing-for-the-custom-frame).</span></span> <span data-ttu-id="e1ba3-208">Diese Funktion verarbeitet die Treffer Test Logik für den [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) , wenn [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) die Nachricht nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e1ba3-208">This function handles the hit testing logic for the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle the message.</span></span>


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a><span data-ttu-id="e1ba3-209">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1ba3-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1ba3-210">Übersicht über Desktop Window Manager</span><span class="sxs-lookup"><span data-stu-id="e1ba3-210">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> </dl>

 

 