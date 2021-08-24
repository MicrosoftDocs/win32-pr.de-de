---
title: Benutzerdefinierter Fensterrahmen mit DWM
description: In diesem Thema wird veranschaulicht, wie Sie die DWM-APIs (Desktopfenster-Manager) verwenden, um benutzerdefinierte Fensterrahmen für Ihre Anwendung zu erstellen.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Desktopfenster-Manager (DWM), benutzerdefinierte Fensterrahmen
- DWM (Desktopfenster-Manager), benutzerdefinierte Fensterrahmen
- Benutzerdefinierte Fensterrahmen
- Entfernen von Standardframes
- Erweitern von Clientframes
- Desktopfenster-Manager (DWM),Erweitern von Clientframes
- DWM (Desktopfenster-Manager),Erweitern von Clientframes
- Desktopfenster-Manager (DWM), Entfernen von Standardframes
- DWM (Desktopfenster-Manager),Entfernen von Standardframes
- Desktopfenster-Manager (DWM), Zeichnen in erweiterten Frames
- DWM (Desktopfenster-Manager),Zeichnen in erweiterten Frames
- Zeichnen in erweiterten Frames
- Treffertests
- Desktopfenster-Manager (DWM), Treffertests
- DWM (Desktopfenster-Manager),Treffertests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b440f475dfacc610354ce151ab0be42dbbe3069390b1efa211195252f7a3914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741454"
---
# <a name="custom-window-frame-using-dwm"></a>Benutzerdefinierter Fensterrahmen mit DWM

In diesem Thema wird veranschaulicht, wie Sie die DWM-APIs (Desktopfenster-Manager) verwenden, um benutzerdefinierte Fensterrahmen für Ihre Anwendung zu erstellen.

-   [Introduction (Einführung)](#introduction)
-   [Erweitern des Clientframes](#extending-the-client-frame)
-   [Entfernen des Standardframes](#removing-the-standard-frame)
-   [Zeichnen im erweiterten Rahmenfenster](#drawing-in-the-extended-frame-window)
-   [Aktivieren von Treffertests für den benutzerdefinierten Frame](#enabling-hit-testing-for-the-custom-frame)
-   [Anhang A: Beispielfensterprozedur](#appendix-a-sample-window-procedure)
-   [Anhang B: Zeichnen des Titels der Beschriftung](#appendix-b-painting-the-caption-title)
-   [Anhang C: HitTestNCA-Funktion](#appendix-c-hittestnca-function)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

In Windows Vista und höher wird die Darstellung der Nicht-Clientbereiche von Anwendungsfenstern (Titelleiste, Symbol, Fensterrahmen und Beschriftungsschaltflächen) vom DWM gesteuert. Mithilfe der DWM-APIs können Sie die Art und Weise ändern, in der dwm den Rahmen eines Fensters rendert.

Ein Feature der DWM-APIs ist die Möglichkeit, den Anwendungsrahmen auf den Clientbereich zu erweitern. Auf diese Weise können Sie ein Benutzeroberflächenelement des Clients , z. B. eine Symbolleiste, in den Rahmen integrieren, sodass die Steuerelemente der Benutzeroberfläche in der Benutzeroberfläche der Anwendung einen besseren Platz erhalten. Beispielsweise integriert Windows Internet Explorer 7 auf Windows Vista die Navigationsleiste in den Fensterrahmen, indem der obere Rand des Frames erweitert wird, wie im folgenden Screenshot gezeigt.

![in den Fensterrahmen integrierte Navigationsleiste.](images/ie7-extendedborder-boxed.png)

Die Möglichkeit, den Fensterrahmen zu erweitern, ermöglicht es Ihnen auch, benutzerdefinierte Frames zu erstellen und gleichzeitig das Aussehen und Haptik des Fensters beizubehalten. Beispielsweise zeichnet Microsoft Office Word 2007 die Schaltfläche "Office" und die Symbolleiste "Schnellzugriff" innerhalb des benutzerdefinierten Frames und stellt die Standardschaltflächen "Minimieren", "Maximieren" und "Schließen" für Untertitel bereit, wie im folgenden Screenshot gezeigt.

![Office-Schaltfläche und Symbolleiste für den Schnellzugriff in Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a>Erweitern des Clientframes

Die Funktionalität zum Erweitern des Frames in den Clientbereich wird von der [**DwmExtendFrameIntoClientArea-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) verfügbar gemacht. Um den Frame zu erweitern, übergeben Sie das Handle des Zielfensters zusammen mit den randinset-Werten an **DwmExtendFrameIntoClientArea.** Die Randinsetwerte bestimmen, wie weit der Rahmen auf den vier Seiten des Fensters erweitert werden soll.

Der folgende Code veranschaulicht die Verwendung von [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) zum Erweitern des Frames.


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



Beachten Sie, dass die Frameerweiterung nicht in der [**WM \_ CREATE-Nachricht,**](/windows/desktop/winmsg/wm-create) sondern in der [**WM \_ ACTIVATE-Nachricht**](/windows/desktop/inputdev/wm-activate) erfolgt. Dadurch wird sichergestellt, dass die Frameerweiterung ordnungsgemäß verarbeitet wird, wenn das Fenster seine Standardgröße hat und maximiert wird.

Die folgende Abbildung zeigt einen Standardfensterrahmen (links) und den gleichen erweiterten Fensterrahmen (auf der rechten Seite). Der Frame wird mithilfe des vorherigen Codebeispiels erweitert, und die Standardeinstellung Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX-Hintergrund**](/windows/win32/api/winuser/ns-winuser-wndclassexa) (COLOR \_ WINDOW +1).

![Screenshot eines Standardframes (links) und eines erweiterten Frames (rechts) mit weißem Hintergrund](images/white-sidebyside.png)

Der visuelle Unterschied zwischen diesen beiden Fenstern ist sehr dezent. Der einzige Unterschied zwischen den beiden besteht darin, dass der schlanke schwarze Linienrahmen des Clientbereichs im Fenster auf der linken Seite im Fenster auf der rechten Seite fehlt. Der Grund für diesen fehlenden Rahmen ist, dass er in den erweiterten Frame integriert ist, der Rest des Clientbereichs jedoch nicht. Damit die erweiterten Frames sichtbar sind, müssen die Bereiche, die den Seiten des erweiterten Frames zugrunde liegen, Pixeldaten mit einem Alphawert von 0 aufweisen. Der schwarze Rahmen um den Clientbereich enthält Pixeldaten, in denen alle Farbwerte (rot, grün, blau und alpha) auf 0 festgelegt sind. Im restlichen Hintergrund ist der Alphawert nicht auf 0 festgelegt, sodass der Rest des erweiterten Frames nicht sichtbar ist.

Die einfachste Möglichkeit, sicherzustellen, dass die erweiterten Frames sichtbar sind, besteht darin, den gesamten Clientbereich schwarz zu zeichnen. Um dies zu erreichen, initialisieren Sie den *hbrBackground-Member* Ihrer [**WNDCLASS-**](/windows/win32/api/winuser/ns-winuser-wndclassa) oder [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) mit dem Handle des \_ black-Pinsels auf Lager. Die folgende Abbildung zeigt den gleichen Standardframe (links) und den erweiterten Frame (rechts), der zuvor gezeigt wurde. Dieses Mal wird *hbrBackground* jedoch auf das BLACK BRUSH-Handle festgelegt, \_ das von der [**GetStockObject-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) abgerufen wurde.

![Screenshot eines Standardframes (links) und eines erweiterten Frames (rechts) mit schwarzem Hintergrund](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a>Entfernen des Standardframes

Nachdem Sie den Rahmen Ihrer Anwendung erweitert und sichtbar gemacht haben, können Sie den Standardframe entfernen. Wenn Sie den Standardrahmen entfernen, können Sie die Breite der einzelnen Seiten des Rahmens steuern, anstatt einfach den Standardrahmen zu erweitern.

Um den Standardfensterrahmen zu entfernen, müssen Sie die [**WM \_ NCCALCSIZE-Meldung**](/windows/desktop/winmsg/wm-nccalcsize) behandeln, insbesondere wenn der *wParam-Wert* **TRUE** und der Rückgabewert 0 ist. Auf diese Weise verwendet Ihre Anwendung den gesamten Fensterbereich als Clientbereich, sodass der Standardframe entfernt wird.

Die Ergebnisse der Verarbeitung der [**WM \_ NCCALCSIZE-Nachricht**](/windows/desktop/winmsg/wm-nccalcsize) sind erst sichtbar, wenn die Größe der Clientregion geändert werden muss. Bis zu diesem Zeitpunkt wird die anfängliche Ansicht des Fensters mit dem Standardrahmen und erweiterten Rahmen angezeigt. Um dies zu umgehen, müssen Sie entweder die Größe Ihres Fensters ändern oder eine Aktion ausführen, die zum Zeitpunkt der Fenstererstellung eine **WM \_ NCCALCSIZE-Nachricht** initiiert. Dies kann erreicht werden, indem Sie die [**SetWindowPos-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) verwenden, um Ihr Fenster zu verschieben und seine Größe zu ändern. Der folgende Code veranschaulicht einen Aufruf von **SetWindowPos,** der erzwingt, dass eine **WM \_ NCCALCSIZE-Nachricht** mit den aktuellen Fensterrechteckattributen und dem SWP \_ FRAMECHANGED-Flag gesendet wird.


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



Die folgende Abbildung zeigt den Standardframe (links) und den neu erweiterten Frame ohne den Standardframe (rechts).

![Screenshot eines Standardframes (links) und eines benutzerdefinierten Frames (rechts)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a>Zeichnen im erweiterten Rahmenfenster

Wenn Sie den Standardrahmen entfernen, verlieren Sie das automatische Zeichnen des Anwendungssymbols und des Titels. Um diese wieder zu Ihrer Anwendung hinzuzufügen, müssen Sie sie selbst zeichnen. Sehen Sie sich hierzu zunächst die Änderung an Ihrem Clientbereich an.

Mit dem Entfernen des Standardframes besteht Ihr Clientbereich jetzt aus dem gesamten Fenster, einschließlich des erweiterten Rahmens. Dies schließt den Bereich ein, in dem die Beschriftungsschaltflächen gezeichnet werden. Im folgenden parallelen Vergleich wird der Clientbereich für den Standardframe und den benutzerdefinierten erweiterten Frame rot hervorgehoben. Der Clientbereich für das Standardrahmenfenster (links) ist der schwarze Bereich. Im erweiterten Rahmenfenster (rechts) ist der Clientbereich das gesamte Fenster.

![Screenshot eines rot hervorgehobenen Clientbereichs im standard- und benutzerdefinierten Frame](images/clientarea-sidebyside.png)

Da das gesamte Fenster Ihr Clientbereich ist, können Sie einfach die gewünschten Daten im erweiterten Frame zeichnen. Um Ihrer Anwendung einen Titel hinzuzufügen, zeichnen Sie einfach Text in der entsprechenden Region. Die folgende Abbildung zeigt themenspezifischen Text, der auf dem benutzerdefinierten Beschriftungsrahmen gezeichnet wird. Der Titel wird mithilfe der [**DrawThemeTextEx-Funktion**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) gezeichnet. Informationen zum Anzeigen des Codes, der den Titel zeichnet, finden Sie unter [Anhang B: Zeichnen des Titels der Beschriftung](#appendix-b-painting-the-caption-title).

![Screenshot eines benutzerdefinierten Frames mit Titel](images/custom-caption-title.png)

> [!Note]  
> Achten Sie beim Zeichnen im benutzerdefinierten Frame beim Platzieren von Ui-Steuerelementen auf Vorsicht. Da das gesamte Fenster Ihre Clientregion ist, müssen Sie die Platzierung des Benutzeroberflächensteuerelements für jede Framebreite anpassen, wenn sie nicht auf oder im erweiterten Frame angezeigt werden soll.

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a>Aktivieren von Treffertests für den benutzerdefinierten Frame

Ein Nebeneffekt des Entfernens des Standardframes ist der Verlust des standardmäßigen Größenänderungs- und Verlagerungsverhaltens. Damit Ihre Anwendung das Standardfensterverhalten ordnungsgemäß emuliert, müssen Sie Logik implementieren, um Treffertests für Beschriftungsschaltflächen zu verarbeiten und die Größe des Frames zu ändern bzw. zu verschieben.

Für Treffertests der Beschriftungsschaltfläche stellt DWM die [**DwmDefWindowProc-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) bereit. Um die Beschriftungsschaltflächen in benutzerdefinierten Frameszenarien ordnungsgemäß zu testen, sollten Nachrichten zuerst zur Verarbeitung an **DwmDefWindowProc** übergeben werden. **DwmDefWindowProc** gibt **TRUE** zurück, wenn eine Nachricht verarbeitet wird, **andernfalls FALSE.** Wenn die Nachricht nicht von **DwmDefWindowProc** verarbeitet wird, sollte Ihre Anwendung die Nachricht selbst verarbeiten oder die Nachricht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.

Zum Ändern und Verschieben der Frame-Größe muss Ihre Anwendung die Treffertestlogik bereitstellen und Frametreffertestmeldungen verarbeiten. Frametreffertestmeldungen werden über die [**WM \_ NCHITTEST-Nachricht**](/windows/desktop/inputdev/wm-nchittest) an Sie gesendet, auch wenn Ihre Anwendung einen benutzerdefinierten Frame ohne den Standardframe erstellt. Der folgende Code veranschaulicht die Verarbeitung der **WM \_ NCHITTEST-Nachricht,** wenn [**dwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) sie nicht verarbeitet. Den Code der aufgerufenen `HitTestNCA` Funktion finden Sie unter Anhang [C: HitTestNCA-Funktion.](#appendix-c-hittestnca-function)


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



## <a name="appendix-a-sample-window-procedure"></a>Anhang A: Beispielfensterprozedur

Im folgenden Codebeispiel werden eine Fensterprozedur und die unterstützenden Workerfunktionen veranschaulicht, die zum Erstellen einer benutzerdefinierten Frameanwendung verwendet werden.


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



## <a name="appendix-b-painting-the-caption-title"></a>Anhang B: Malen des Titels der Beschriftung

Der folgende Code veranschaulicht das Zeichnen eines Titels einer Beschriftung auf dem erweiterten Frame. Diese Funktion muss innerhalb der [**BeginPaint-**](/windows/desktop/api/winuser/nf-winuser-beginpaint) und [**EndPaint-Aufrufe aufgerufen**](/windows/desktop/api/winuser/nf-winuser-endpaint) werden.


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



## <a name="appendix-c-hittestnca-function"></a>Anhang C: HitTestNCA-Funktion

Der folgende Code zeigt die `HitTestNCA` Funktion, die in [Aktivieren von Treffertests für den benutzerdefinierten Frame verwendet wird.](#enabling-hit-testing-for-the-custom-frame) Diese Funktion verarbeitet die Treffertestlogik für [**WM \_ NCHITTEST,**](/windows/desktop/inputdev/wm-nchittest) [**wenn DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) die Nachricht nicht verarbeitet.


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

 

 