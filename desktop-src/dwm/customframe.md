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
# <a name="custom-window-frame-using-dwm"></a>Benutzerdefinierter Fensterrahmen mithilfe von DWM

In diesem Thema wird veranschaulicht, wie Sie die Desktopfenster-Manager (DWM)-APIs verwenden, um benutzerdefinierte Fensterrahmen für Ihre Anwendung zu erstellen.

-   [Introduction (Einführung)](#introduction)
-   [Erweitern des Client Frames](#extending-the-client-frame)
-   [Entfernen des Standard Rahmens](#removing-the-standard-frame)
-   [Zeichnen im erweiterten Rahmen Fenster](#drawing-in-the-extended-frame-window)
-   [Aktivieren von Treffer Tests für den benutzerdefinierten Frame](#enabling-hit-testing-for-the-custom-frame)
-   [Anhang A: Beispiel Fenster Prozedur](#appendix-a-sample-window-procedure)
-   [Anhang B: Zeichnen des Beschriftungs Titels](#appendix-b-painting-the-caption-title)
-   [Anhang C: hittestnca-Funktion](#appendix-c-hittestnca-function)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

In Windows Vista und höher wird die Darstellung der nicht-Client Bereiche von Anwendungs Fenstern (Titelleiste, Symbol, Fensterrahmen und Beschriftungs Schaltflächen) durch die DWM gesteuert. Mithilfe der DWM-APIs können Sie die Art und Weise ändern, in der die DWM den Rahmen eines Fensters rendert.

Ein Feature der DWM-APIs ist die Möglichkeit, den Anwendungs Frame in den Client Bereich zu erweitern. Dies ermöglicht es Ihnen, ein Client Benutzeroberflächen Element – z. b. eine Symbolleiste – in den Frame zu integrieren, sodass die UI-Steuerelemente in der Benutzeroberfläche der Anwendung wichtiger werden. Windows Internet Explorer 7 unter Windows Vista integriert z. b. die Navigationsleiste in den Fensterrahmen, indem die obere Seite des Frames erweitert wird, wie im folgenden Screenshot gezeigt.

![Navigationsleiste, die in den Fensterrahmen integriert ist.](images/ie7-extendedborder-boxed.png)

Durch die Möglichkeit, den Fensterrahmen zu erweitern, können Sie auch benutzerdefinierte Frames erstellen und gleichzeitig das Aussehen und das Erscheinungsbild des Fensters beibehalten. Microsoft Office Word 2007 zeichnet z. b. die Office-Schaltfläche und die Symbolleiste für den schnell Zugriff im benutzerdefinierten Frame und stellt dabei die Standard Schaltflächen Minimieren, maximieren und schließen bereit, wie im folgenden Screenshot gezeigt.

![Office-Schaltfläche und Symbolleiste für den schnell Zugriff in Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Erweitern des Client Frames

Die Funktionalität zum Erweitern des Frames in den Client Bereich wird von der Funktion " [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) " verfügbar gemacht. Um den Frame zu erweitern, übergeben Sie das Handle des Zielfensters mit den Margin-einfügen-Werten an **DwmExtendFrameIntoClientArea**. Die Werte für den Margin-Wert legen fest, wie weit der Frame auf den vier Seiten des Fensters erweitert werden soll.

Der folgende Code veranschaulicht die Verwendung von [**dwmextendframeinumclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) zum Erweitern des Frames.


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



Beachten Sie, dass die Frame Erweiterung innerhalb der [**WM- \_ Aktivierungs**](/windows/desktop/inputdev/wm-activate) Nachricht statt in der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung erfolgt. Dadurch wird sichergestellt, dass die Frame Erweiterung ordnungsgemäß verarbeitet wird, wenn das Fenster seine Standardgröße hat und wenn es maximiert ist.

In der folgenden Abbildung wird ein Standardfenster Rahmen (auf der linken Seite) und der erweiterte Fensterrahmen (auf der rechten Seite) angezeigt. Der Frame wird mit dem vorherigen Codebeispiel und dem Standard Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Hintergrund (Farb \_ Fenster + 1) erweitert.

![Screenshot eines standardmäßigen (linken) und erweiterten Rahmens (rechts) mit weißem Hintergrund](images/white-sidebyside.png)

Der visuelle Unterschied zwischen diesen beiden Fenstern ist sehr gering. Der einzige Unterschied zwischen den beiden besteht darin, dass der schlanke schwarze Linien Rand des Client Bereichs im Fenster links im Fenster auf der rechten Seite fehlt. Der Grund für diese fehlende Grenze ist, dass Sie in den erweiterten Frame integriert ist, aber der Rest des Client Bereichs ist nicht. Damit die erweiterten Frames sichtbar sind, müssen die Regionen, die den einzelnen Seiten des erweiterten Frames zugrunde liegen, Pixeldaten mit einem Alphawert von 0 aufweisen. Der schwarze Rahmen um den Client Bereich verfügt über Pixeldaten, in denen alle Farbwerte (rot, grün, blau und Alpha) auf 0 festgelegt sind. Im restlichen Hintergrund ist der Alpha-Wert nicht auf 0 festgelegt, sodass der restliche Rahmen nicht sichtbar ist.

Die einfachste Möglichkeit, um sicherzustellen, dass die erweiterten Frames sichtbar sind, besteht darin, den gesamten Client Bereich schwarz zu zeichnen. Um dies zu erreichen, initialisieren Sie den *hbrbackground* -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -oder [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur mit dem Handle des Stock Black- \_ Pinsels. Die folgende Abbildung zeigt den gleichen Standard Frame (links) und den erweiterten Frame (rechts), der zuvor gezeigt wurde. Dieses Mal wird jedoch *hbrbackground* auf das schwarze Pinsel handle festgelegt, das \_ von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion abgerufen wird.

![Screenshot eines standardmäßigen (linken) und erweiterten Rahmens (rechts) mit schwarzem Hintergrund](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Entfernen des Standard Rahmens

Nachdem Sie den Frame der Anwendung erweitert und sichtbar gemacht haben, können Sie den Standard Frame entfernen. Wenn Sie den Standardrahmen entfernen, können Sie die Breite jeder Seite des Frames steuern, anstatt einfach den Standardrahmen zu erweitern.

Um den Standardfenster Rahmen zu entfernen, müssen Sie die [**WM- \_ nccalcsize**](/windows/desktop/winmsg/wm-nccalcsize) -Nachricht behandeln, insbesondere wenn der *wParam* -Wert " **true** " und der Rückgabewert "0" ist. Dadurch wird die gesamte Fenster Region als Client Bereich verwendet, wobei der Standardrahmen entfernt wird.

Die Ergebnisse der Verarbeitung der [**WM- \_ nccalcsize**](/windows/desktop/winmsg/wm-nccalcsize) -Nachricht sind erst sichtbar, wenn die Größe des Client Bereichs geändert werden muss. Bis zu diesem Zeitpunkt wird die anfängliche Ansicht des Fensters mit dem Standardrahmen und den erweiterten Rahmen angezeigt. Um dies zu umgehen, müssen Sie entweder die Größe des Fensters ändern oder eine Aktion ausführen, die zum Zeitpunkt der Fenster Erstellung eine **WM- \_ nccalcsize** -Nachricht auslöst. Dies kann mithilfe der [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion erreicht werden, um das Fenster zu verschieben und seine Größe zu ändern. Der folgende Code veranschaulicht einen Aufrufen von **SetWindowPos** , der erzwingt, dass eine **WM- \_ nccalcsize** -Nachricht mithilfe der aktuellen Fenster Rechteck Attribute und des das- \_ Flag "framechanout" gesendet wird.


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



In der folgenden Abbildung wird der Standardrahmen (links) und der neu erweiterte Rahmen ohne den Standardrahmen (right) angezeigt.

![Screenshot eines Standardrahmens (links) und benutzerdefiniertem Frame (rechts)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Zeichnen im erweiterten Rahmen Fenster

Wenn Sie den Standardrahmen entfernen, verlieren Sie das automatische Zeichnen des Anwendungs Symbols und des Titels. Wenn Sie diese wieder der Anwendung hinzufügen möchten, müssen Sie Sie selbst zeichnen. Betrachten Sie hierzu zunächst die Änderung, die in Ihrem Client Bereich aufgetreten ist.

Wenn Sie den Standard Frame entfernen, besteht der Client Bereich nun aus dem gesamten Fenster, einschließlich des erweiterten Frames. Dies umfasst die Region, in der die Beschriftungs Schaltflächen gezeichnet werden. In der folgenden Seite-an-Seite-Vergleich wird der Client Bereich für den Standard Frame und den benutzerdefinierten erweiterten Frame rot hervorgehoben. Der Client Bereich für das Standardrahmen Fenster (links) ist der schwarze Bereich. Im erweiterten Rahmen Fenster (rechts) ist der Client Bereich das gesamte Fenster.

![Screenshot eines rot markierten Client Bereichs in Standard-und benutzerdefiniertem Frame](images/clientarea-sidebyside.png)

Da es sich bei dem gesamten Fenster um Ihren Client Bereich handelt, können Sie einfach die gewünschten Elemente im erweiterten Frame zeichnen. Um der Anwendung einen Titel hinzuzufügen, zeichnen Sie einfach Text in der entsprechenden Region. Die folgende Abbildung zeigt den Text für den Text, der im benutzerdefinierten Beschriftungs Rahmen gezeichnet wurde Der Titel wird mithilfe der [**drawdermetextex**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) -Funktion gezeichnet. Informationen zum Anzeigen des Codes, der den Titel zeichnet, finden Sie unter [Anhang B: Zeichnen des Beschriftungs Titels](#appendix-b-painting-the-caption-title).

![Screenshot eines benutzerdefinierten Frames mit dem Titel](images/custom-caption-title.png)

> [!Note]  
> Wenn Sie in Ihren benutzerdefinierten Frame zeichnen, gehen Sie beim Platzieren von UI-Steuerelementen vorsichtig vor Da es sich bei dem gesamten Fenster um die Client Region handelt, müssen Sie die Platzierung des UI-Steuer Elements für jede Frame Breite anpassen, wenn Sie nicht im erweiterten Frame angezeigt werden sollen.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Aktivieren von Treffer Tests für den benutzerdefinierten Frame

Ein Nebeneffekt beim Entfernen des Standardrahmens ist der Verlust der standardmäßigen Änderung der Größe und des Verschiebungs Verhaltens. Damit Ihre Anwendung das Standardverhalten des Fensters ordnungsgemäß emulieren kann, müssen Sie eine Logik implementieren, um Treffer Tests für Beschriftungs Schaltflächen und die Größe der Frame Größe/Verschiebung zu verarbeiten

Für die Treffer Tests der Beschriftungs Schaltfläche stellt DWM die [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) -Funktion bereit. Um die Beschriftungs Schaltflächen in benutzerdefinierten Frame Szenarios ordnungsgemäß zu erreichen, sollten Nachrichten zur Behandlung an **DwmDefWindowProc** übermittelt werden. **DwmDefWindowProc** gibt **true** zurück, wenn eine Nachricht behandelt wird, andernfalls **false** . Wenn die Nachricht nicht von **DwmDefWindowProc** behandelt wird, sollte die Anwendung die Nachricht selbst verarbeiten oder die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.

Wenn Sie die Größe der Frame Größe ändern und verschieben, muss Ihre Anwendung die Treffer Test Logik bereitstellen und Frame-Treffer Testnachrichten verarbeiten. Frame Treffer Test-Meldungen werden über die WM- [**\_ nchittest**](/windows/desktop/inputdev/wm-nchittest) -Nachricht gesendet, auch wenn Ihre Anwendung einen benutzerdefinierten Frame ohne den Standardrahmen erstellt. Der folgende Code veranschaulicht die Verarbeitung der **WM- \_ nchittest** -Nachricht, wenn Sie von [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) nicht behandelt wird. Den Code der aufgerufenen Funktion finden Sie unter `HitTestNCA` [Anhang C: hittestnca-Funktion](#appendix-c-hittestnca-function).


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



## <a name="appendix-a-sample-window-procedure"></a>Anhang A: Beispiel Fenster Prozedur

Im folgenden Codebeispiel wird eine Fenster Prozedur und die unterstützenden workerfunktionen veranschaulicht, die zum Erstellen einer benutzerdefinierten Frame Anwendung verwendet werden.


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



## <a name="appendix-b-painting-the-caption-title"></a>Anhang B: Zeichnen des Beschriftungs Titels

Der folgende Code veranschaulicht, wie Sie einen Beschriftungs Titel für den erweiterten Frame zeichnen. Diese Funktion muss in den [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) -und [**endpaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) -aufrufen aufgerufen werden.


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



## <a name="appendix-c-hittestnca-function"></a>Anhang C: hittestnca-Funktion

Der folgende Code zeigt die-Funktion, die zum `HitTestNCA` [Aktivieren von Treffer Tests für den benutzerdefinierten Frame](#enabling-hit-testing-for-the-custom-frame)verwendet wird. Diese Funktion verarbeitet die Treffer Test Logik für den [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) , wenn [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) die Nachricht nicht verarbeitet.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Desktop Window Manager](dwm-overview.md)
</dt> </dl>

 

 