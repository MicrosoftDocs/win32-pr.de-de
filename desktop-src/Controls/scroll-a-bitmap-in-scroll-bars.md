---
title: Vorgehensweise beim Scrollen einer Bitmap
description: In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfenster Prozedur einer Anwendung vornehmen können, damit der Benutzer einen Bildlauf in einer Bitmap ausführen kann.
ms.assetid: FA6FEA49-25EB-4C18-AD07-74BD77501906
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01a93fbb005b75d7cd860bc8545c4e77a80767
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474389"
---
# <a name="how-to-scroll-a-bitmap"></a>Vorgehensweise beim Scrollen einer Bitmap

In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfenster Prozedur einer Anwendung vornehmen können, damit der Benutzer einen Bildlauf in einer Bitmap ausführen kann.

Das Beispiel enthält ein Menü Element, mit dem der Bildschirminhalt in eine Bitmap kopiert und die Bitmap im Client Bereich angezeigt wird. Im Beispiel werden auch die von den Schiebe leisten generierten " [**WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Meldungen verarbeitet, sodass der Benutzer die Bitmap horizontal und vertikal scrollen kann. Im Gegensatz zum Beispiel für Text mit Text wird mit dem Bitmap-Beispiel die [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion verwendet, um den ungültigen Teil des Client Bereichs zu zeichnen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="processing-the-wm_create-message"></a>Verarbeiten der WM \_ Create-Nachricht

Wenn die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht verarbeitet wird, werden die für den Bildlauf erforderlichen Variablen initialisiert. Verwenden Sie die Funktion [**"Funktion"**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) , um einen kompatiblen Gerätekontext (DC), die Funktion "Anordnen" zum Erstellen einer Bitmap und [**die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) " [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) " zum Auswählen der Bitmap für den Domänen Controller zu erstellen. Beachten Sie, dass ein kompatibler DC auch als Speicher-DC bezeichnet wird.

Die gerätespezifischen Informationen zum Anzeigegerät werden abgerufen. Wenn für den Bildschirm ein kompatibler DC erstellt wird, wie im Beispiel, verwenden Sie die [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) -Funktion, um diese Informationen zu erhalten. Die Informationen enthalten die Anzahl der angrenzenden Farbbits pro Pixel, die Anzahl von Farbebenen und die Höhe und Breite des DC.

### <a name="processing-the-wm_size-message"></a>Verarbeiten der WM- \_ Größen Meldung

Die Verarbeitung der [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht erfordert, dass der scrollbereich und die Position angepasst werden, damit Sie die Dimensionen des Client Bereichs und der anzuzeigenden Bitmap widerspiegeln.

Die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion legt die minimalen und maximalen Positionswerte, die Seitengröße und die Scrollposition für eine Schiebe Leiste fest.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Verarbeiten der \_ Nachrichten "WM HScroll" und "WM \_ VScroll"

Wenn die " [**WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Nachrichten verarbeitet werden, wird der Anforderungs Code der Scrollleiste überprüft und die Scrollposition auf einen neuen Wert festgelegt, der die scrollaktion des Benutzers widerspiegelt. Wenn die Scrollposition innerhalb des scrollbereichs liegt, wird das Fenster mithilfe der [**scrollwindow**](/windows/desktop/api/Winuser/nf-winuser-scrollwindow) -Funktion an die neue Position gescrollt. Die Position des Bild Lauf Felds wird dann mithilfe der [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion angepasst.

Nachdem ein Fenster einen Rollup ausgeführt hat, wird ein Teil des Client Bereichs als ungültig festgestellt. Um sicherzustellen, dass die ungültige Region aktualisiert wird, verwenden Sie die [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) -Funktion, um eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung zu generieren. Bei der Verarbeitung **der \_ WM** -Zeichnungs Nachricht muss eine Anwendung den ungültigen Bereich unten im Client Bereich neu zeichnen. Beim Scrollen oder Ändern der Größe des Client Bereichs wird im Beispiel die [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion verwendet, um den entsprechenden Teil der Bitmap in den ungültigen Teil des Client Bereichs zu kopieren.

## <a name="example-of-scrolling-a-bitmap"></a>Beispiel für das Scrollen einer Bitmap

Im folgenden Beispiel wird der Benutzer in die Lage versetzt, den Bildschirminhalt in einer Bitmap aufzuzeichnen und im Client Bereich einen Bildlauf durch die Bitmap durchführen. Der Bildschirminhalt wird aufgezeichnet, wenn der Benutzer mit der rechten Maustaste auf den Client Bereich klickt.


```C++
LRESULT CALLBACK MyBitmapWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    HDC hdc; 
    PAINTSTRUCT ps; 
    SCROLLINFO si; 
 
    // These variables are required by BitBlt. 
    static HDC hdcWin;           // window DC 
    static HDC hdcScreen;        // DC for entire screen 
    static HDC hdcScreenCompat;  // memory DC for screen 
    static HBITMAP hbmpCompat;   // bitmap handle to old DC 
    static BITMAP bmp;           // bitmap data structure 
    static BOOL fBlt;            // TRUE if BitBlt occurred 
    static BOOL fScroll;         // TRUE if scrolling occurred 
    static BOOL fSize;           // TRUE if fBlt & WM_SIZE 
 
    // These variables are required for horizontal scrolling. 
    static int xMinScroll;       // minimum horizontal scroll value 
    static int xCurrentScroll;   // current horizontal scroll value 
    static int xMaxScroll;       // maximum horizontal scroll value 
 
    // These variables are required for vertical scrolling. 
    static int yMinScroll;       // minimum vertical scroll value 
    static int yCurrentScroll;   // current vertical scroll value 
    static int yMaxScroll;       // maximum vertical scroll value 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create a normal DC and a memory DC for the entire 
            // screen. The normal DC provides a snapshot of the 
            // screen contents. The memory DC keeps a copy of this 
            // snapshot in the associated bitmap. 
            hdcScreen = CreateDC(L"DISPLAY", (PCTSTR) NULL, 
                (PCTSTR) NULL, (CONST DEVMODE *) NULL); 
            hdcScreenCompat = CreateCompatibleDC(hdcScreen); 
 
            // Retrieve the metrics for the bitmap associated with the 
            // regular device context. 
            bmp.bmBitsPixel = 
                (BYTE) GetDeviceCaps(hdcScreen, BITSPIXEL); 
            bmp.bmPlanes = (BYTE) GetDeviceCaps(hdcScreen, PLANES); 
            bmp.bmWidth = GetDeviceCaps(hdcScreen, HORZRES); 
            bmp.bmHeight = GetDeviceCaps(hdcScreen, VERTRES); 
 
            // The width must be byte-aligned. 
            bmp.bmWidthBytes = ((bmp.bmWidth + 15) &~15)/8; 
 
            // Create a bitmap for the compatible DC. 
            hbmpCompat = CreateBitmap(bmp.bmWidth, bmp.bmHeight, 
                bmp.bmPlanes, bmp.bmBitsPixel, (CONST VOID *) NULL); 
 
            // Select the bitmap for the compatible DC. 
            SelectObject(hdcScreenCompat, hbmpCompat); 
 
            // Initialize the flags. 
            fBlt = FALSE; 
            fScroll = FALSE; 
            fSize = FALSE; 
 
            // Initialize the horizontal scrolling variables. 
            xMinScroll = 0; 
            xCurrentScroll = 0; 
            xMaxScroll = 0; 
 
            // Initialize the vertical scrolling variables. 
            yMinScroll = 0; 
            yCurrentScroll = 0; 
            yMaxScroll = 0; 
 
            break; 
 
        case WM_SIZE: 
        { 
            int xNewSize; 
            int yNewSize; 
 
            xNewSize = LOWORD(lParam); 
            yNewSize = HIWORD(lParam); 
 
            if (fBlt) 
                fSize = TRUE; 
     
            // The horizontal scrolling range is defined by 
            // (bitmap_width) - (client_width). The current horizontal 
            // scroll value remains within the horizontal scrolling range. 
            xMaxScroll = max(bmp.bmWidth-xNewSize, 0); 
            xCurrentScroll = min(xCurrentScroll, xMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = xMinScroll; 
            si.nMax   = bmp.bmWidth; 
            si.nPage  = xNewSize; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            // The vertical scrolling range is defined by 
            // (bitmap_height) - (client_height). The current vertical 
            // scroll value remains within the vertical scrolling range. 
            yMaxScroll = max(bmp.bmHeight - yNewSize, 0); 
            yCurrentScroll = min(yCurrentScroll, yMaxScroll); 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_RANGE | SIF_PAGE | SIF_POS; 
            si.nMin   = yMinScroll; 
            si.nMax   = bmp.bmHeight; 
            si.nPage  = yNewSize; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 
 
        case WM_PAINT: 
        { 
            PRECT prect; 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            // If the window has been resized and the user has 
            // captured the screen, use the following call to 
            // BitBlt to paint the window's client area. 
            if (fSize) 
            { 
                BitBlt(ps.hdc, 
                    0, 0, 
                    bmp.bmWidth, bmp.bmHeight, 
                    hdcScreenCompat, 
                    xCurrentScroll, yCurrentScroll, 
                    SRCCOPY); 
 
                fSize = FALSE; 
            } 
 
            // If scrolling has occurred, use the following call to 
            // BitBlt to paint the invalid rectangle. 
            // 
            // The coordinates of this rectangle are specified in the 
            // RECT structure to which prect points. 
            // 
            // Note that it is necessary to increment the seventh 
            // argument (prect->left) by xCurrentScroll and the 
            // eighth argument (prect->top) by yCurrentScroll in 
            // order to map the correct pixels from the source bitmap. 
             if (fScroll) 
            { 
                prect = &ps.rcPaint; 
 
                BitBlt(ps.hdc, 
                    prect->left, prect->top, 
                    (prect->right - prect->left), 
                    (prect->bottom - prect->top), 
                    hdcScreenCompat, 
                    prect->left + xCurrentScroll, 
                    prect->top + yCurrentScroll, 
                    SRCCOPY); 
 
                fScroll = FALSE; 
            } 
 
            EndPaint(hwnd, &ps); 

            break; 
        } 

        case WM_HSCROLL: 
        { 
            int xDelta;     // xDelta = new_pos - current_pos  
            int xNewPos;    // new position 
            int yDelta = 0; 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft left of the scroll box. 
                case SB_PAGEUP: 
                    xNewPos = xCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft right of the scroll box. 
                case SB_PAGEDOWN: 
                    xNewPos = xCurrentScroll + 50; 
                    break; 
 
                // User clicked the left arrow. 
                case SB_LINEUP: 
                    xNewPos = xCurrentScroll - 5; 
                    break; 
 
                // User clicked the right arrow. 
                case SB_LINEDOWN: 
                    xNewPos = xCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    xNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    xNewPos = xCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen width. 
            xNewPos = max(0, xNewPos); 
            xNewPos = min(xMaxScroll, xNewPos); 
 
            // If the current position does not change, do not scroll.
            if (xNewPos == xCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            xDelta = xNewPos - xCurrentScroll; 
 
            // Reset the current scroll position. 
            xCurrentScroll = xNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = xCurrentScroll; 
            SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
            break; 
        } 
        
        case WM_VSCROLL: 
        { 
            int xDelta = 0; 
            int yDelta;     // yDelta = new_pos - current_pos 
            int yNewPos;    // new position 
 
            switch (LOWORD(wParam)) 
            { 
                // User clicked the scroll bar shaft above the scroll box. 
                case SB_PAGEUP: 
                    yNewPos = yCurrentScroll - 50; 
                    break; 
 
                // User clicked the scroll bar shaft below the scroll box. 
                case SB_PAGEDOWN: 
                    yNewPos = yCurrentScroll + 50; 
                    break; 
 
                // User clicked the top arrow. 
                case SB_LINEUP: 
                    yNewPos = yCurrentScroll - 5; 
                    break; 
 
                // User clicked the bottom arrow. 
                case SB_LINEDOWN: 
                    yNewPos = yCurrentScroll + 5; 
                    break; 
 
                // User dragged the scroll box. 
                case SB_THUMBPOSITION: 
                    yNewPos = HIWORD(wParam); 
                    break; 
 
                default: 
                    yNewPos = yCurrentScroll; 
            } 
 
            // New position must be between 0 and the screen height. 
            yNewPos = max(0, yNewPos); 
            yNewPos = min(yMaxScroll, yNewPos); 
 
            // If the current position does not change, do not scroll.
            if (yNewPos == yCurrentScroll) 
                break; 
 
            // Set the scroll flag to TRUE. 
            fScroll = TRUE; 
 
            // Determine the amount scrolled (in pixels). 
            yDelta = yNewPos - yCurrentScroll; 
 
            // Reset the current scroll position. 
            yCurrentScroll = yNewPos; 
 
            // Scroll the window. (The system repaints most of the 
            // client area when ScrollWindowEx is called; however, it is 
            // necessary to call UpdateWindow in order to repaint the 
            // rectangle of pixels that were invalidated.) 
            ScrollWindowEx(hwnd, -xDelta, -yDelta, (CONST RECT *) NULL, 
                (CONST RECT *) NULL, (HRGN) NULL, (PRECT) NULL, 
                SW_INVALIDATE); 
            UpdateWindow(hwnd); 
 
            // Reset the scroll bar. 
            si.cbSize = sizeof(si); 
            si.fMask  = SIF_POS; 
            si.nPos   = yCurrentScroll; 
            SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 

            break; 
        } 

        case WM_RBUTTONDOWN:
        {
            // Get the compatible DC of the client area. 
            hdcWin = GetDC(hwnd); 

            // Fill the client area to remove any existing contents. 
            RECT rect;
            GetClientRect(hwnd, &rect);
            FillRect(hdcWin, &rect, (HBRUSH)(COLOR_WINDOW+1));
 
            // Copy the contents of the current screen 
            // into the compatible DC. 
            BitBlt(hdcScreenCompat, 0, 0, bmp.bmWidth, 
                bmp.bmHeight, hdcScreen, 0, 0, SRCCOPY); 
 
            // Copy the compatible DC to the client area.
            BitBlt(hdcWin, 0, 0, bmp.bmWidth, bmp.bmHeight, 
                hdcScreenCompat, 0, 0, SRCCOPY); 
 
            ReleaseDC(hwnd, hdcWin); 
            fBlt = TRUE; 
            break; 
        }

        case WM_DESTROY :
            PostQuitMessage (0);
            return 0;
    }
    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Scrollleisten](using-scroll-bars.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 