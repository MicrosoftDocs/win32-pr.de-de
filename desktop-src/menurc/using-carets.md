---
title: Verwenden von Carets
description: Dieser Abschnitt enthält Codebeispiele, in denen gezeigt wird, wie Aufgaben im Zusammenhang mit Carets durchgeführt werden.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- resources,carets
- Carets,creating
- Carets, anzeigend
- Carets,destroying
- Caret-/Ausblenden
- Caret-, Blinkzeiten
- blinkende Linien
- blinkende Blöcke
- blinkende Bitmaps
- Erstellen von Carets
- Anzeigen von Caret-Texten
- Ausblenden von Carets
- Zerstören von Carets
- Blinkzeiten
- Benutzereingabe,Tastatureingabe
- Erfassen von Benutzereingaben, Tastatureingabe
- Tastatureingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c930931df8ce401fbed8cc9af16db3cb52de08ebe9cf539109b426497318d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472646"
---
# <a name="using-carets"></a>Verwenden von Carets

Dieser Abschnitt enthält Codebeispiele für die folgenden Aufgaben:

-   [Erstellen und Anzeigen eines Caret-Text](#creating-and-displaying-a-caret)
-   [Ausblenden eines Caret-](#hiding-a-caret)
-   [Zerstören eines Caret-](#destroying-a-caret)
-   [Anpassen der Blinkzeit](#adjusting-the-blink-time)
-   [Verarbeiten der Tastatureingabe](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Erstellen und Anzeigen eines Caret-Text

Wenn der Tastaturfokus angezeigt wird, sollte das Fenster das Caret-Caret-Fenster erstellen und anzeigen. Verwenden Sie [**die CreateCaret-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-createcaret) um ein Caret-Caret-Paar im angegebenen Fenster zu erstellen. Anschließend können Sie [**SetCaretPos aufrufen,**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) um die aktuelle Position des Caret-Caret-Zeichens und [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) so festlegen, dass das Caret-Zeichen sichtbar wird.

Das System sendet die [**WM \_ SETFOCUS-Nachricht**](/windows/desktop/inputdev/wm-setfocus) an das Fenster, das den Tastaturfokus empfängt. Daher sollte eine Anwendung das Caret-Caret-Format erstellen und anzeigen, während diese Nachricht verarbeitet wird.


```
HWND hwnd,       // window handle 
int x;           // horizontal coordinate of cursor 
int y;           // vertical coordinate of cursor 
int nWidth;      // width of cursor 
int nHeight;     // height of cursor 
char *lpszChar;  // pointer to character 
 
    case WM_SETFOCUS: 
 
    // Create a solid black caret. 
        CreateCaret(hwnd, (HBITMAP) NULL, nWidth, nHeight); 
 
    // Adjust the caret position, in client coordinates. 
        SetCaretPos(x, y); 
 
    // Display the caret. 
        ShowCaret(hwnd); 
 
        break; 
```



Um ein Caret-Zeichen basierend auf einer Bitmap zu erstellen, müssen Sie bei Verwendung von [**CreateCaret ein Bitmaphand handle angeben.**](/windows/desktop/api/Winuser/nf-winuser-createcaret) Sie können eine Grafikanwendung verwenden, um die Bitmap zu erstellen, und einen Ressourcencompiler, um die Bitmap den Ressourcen Ihrer Anwendung hinzuzufügen. Ihre Anwendung kann dann die [**LoadBitmap-Funktion verwenden,**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) um das Bitmaphand handle zu laden. Beispielsweise könnten Sie die **CreateCaret-Zeile** im vorherigen Beispiel durch die folgenden Zeilen ersetzen, um ein Bitmap-Caretstrich zu erstellen.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



Alternativ können Sie die Funktion [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) oder [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) verwenden, um das Handle der Caretbitmap abzurufen. Weitere Informationen zu Bitmaps finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

Wenn Ihre Anwendung ein Bitmaphand handle angibt, ignoriert [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) die Breiten- und Höhenparameter. Die Bitmap definiert die Größe des Caret-Zeichens.

## <a name="hiding-a-caret"></a>Ausblenden eines Caret-

Jedes Mal, wenn Ihre Anwendung einen Bildschirm neu zeichnet, während eine andere Nachricht als [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)verarbeitet wird, muss sie das Caretstrich mithilfe der [**HideCaret-Funktion unsichtbar**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) machen. Wenn die Anwendung mit dem Zeichnen fertig ist, zeigen Sie das Caret-Zeichen erneut an, indem Sie die [**ShowCaret-Funktion**](/windows/desktop/api/Winuser/nf-winuser-showcaret) verwenden. Wenn Ihre Anwendung die **WM \_ PAINT-Nachricht** verarbeitet, ist es nicht erforderlich, das Caretstrich auszublenden und erneut einblenden, da diese Funktion dies automatisch tut.

Das folgende Codebeispiel zeigt, wie Ihre Anwendung das Caretzeichen beim Zeichnen eines Zeichens auf dem Bildschirm und beim Verarbeiten der [**WM \_ CHAR-Nachricht ausblenden**](/windows/desktop/inputdev/wm-char) kann.


```
HWND hwnd,   // window handle 
HDC hdc;     // device context 
 
    case WM_CHAR: 
        switch (wParam) 
        { 
            case 0x08: 
             
             // Process a backspace. 
             
                break; 
 
            case 0x09: 
             
             // Process a tab.  
             
                break; 
 
            case 0x0D: 
             
             // Process a carriage return. 
             
                break; 
 
            case 0x1B: 
             
             // Process an escape. 
             
                break; 
 
            case 0x0A: 
             
             // Process a linefeed. 
             
                break; 
 
            default: 
                // Hide the caret. 
                HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                hdc = GetDC(hwnd); 
                SelectObject(hdc, 
                    GetStockObject(SYSTEM_FIXED_FONT)); 
 
                TextOut(hdc, x, y, lpszChar, 1); 
 
                ReleaseDC(hwnd, hdc); 
 
                // Display the caret. 
 
                ShowCaret(hwnd); 
 
        } 
```



Wenn Ihre Anwendung die [**HideCaret-Funktion**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) mehrmals aufruft, ohne [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)auf aufruft, wird das Caretzeichen erst angezeigt, wenn die Anwendung **ShowCaret** genauso oft aufruft.

## <a name="destroying-a-caret"></a>Zerstören eines Caret-

Wenn ein Fenster den Tastaturfokus verliert, sendet das System die [**WM \_ KILLFOCUS-Nachricht**](/windows/desktop/inputdev/wm-killfocus) an das Fenster. Ihre Anwendung sollte das Caret-Caret-Gerät während der Verarbeitung dieser Nachricht mithilfe der [**DestroyCaret-Funktion**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) zerstören. Der folgende Code zeigt, wie Ein caret in einem Fenster zerstört wird, das nicht mehr über den Tastaturfokus verfügt.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Anpassen der Blinkzeit

In 16-Bit-Windows könnte eine Windows-basierte Anwendung die [**GetCaretBlinkTime-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) aufrufen, um die aktuelle Blinkzeit zu speichern, und dann die [**SetCaretBlinkTime-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) aufrufen, um die Blinkzeit während der Verarbeitung der [**WM \_ SETFOCUS-Nachricht**](/windows/desktop/inputdev/wm-setfocus) anzupassen. Die Anwendung würde die gespeicherte Blinkzeit für die Verwendung anderer Anwendungen wiederherstellen, indem **sie SetCaretBlinkTime** während der Verarbeitung der [**WM \_ KILLFOCUS-Nachricht**](/windows/desktop/inputdev/wm-killfocus) aufruft. Diese Technik funktioniert jedoch nicht in Multithreadumgebungen. Insbesondere wird die Deaktivierung einer Anwendung nicht mit der Aktivierung einer anderen Anwendung synchronisiert, sodass eine andere Anwendung weiterhin aktiviert werden kann, wenn eine Anwendung nicht mehr aktiv ist.

Anwendungen sollten die vom Benutzer gewählte Blinkzeit achten. Die [**SetCaretBlinkTime-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) sollte nur von einer Anwendung aufgerufen werden, die dem Benutzer das Festlegen der Blinkzeit ermöglicht.

## <a name="processing-keyboard-input"></a>Verarbeiten der Tastatureingabe

Im folgenden Beispiel wird veranschaulicht, wie ein Caret-Text in einem einfachen Text-Editor verwendet wird. Im Beispiel wird die Position des Caretzeichens aktualisiert, wenn der Benutzer druckbare Zeichen ein gibt und verschiedene Tasten verwendet, um den Clientbereich zu wechseln.


```
#define TEXTMATRIX(x, y) *(pTextMatrix + (y * nWindowCharsX) + x) 
// Global variables.
HINSTANCE hinst;                  // current instance 
HBITMAP hCaret;                   // caret bitmap 
HDC hdc;                          // device context  
PAINTSTRUCT ps;                   // client area paint info 
static char *pTextMatrix = NULL;  // points to text matrix 
static int  nCharX,               // width of char. in logical units 
            nCharY,               // height of char. in logical units 
            nWindowX,             // width of client area 
            nWindowY,             // height of client area 
            nWindowCharsX,        // width of client area 
            nWindowCharsY,        // height of client area 
            nCaretPosX,           // x-position of caret 
            nCaretPosY;           // y-position of caret 
static UINT uOldBlink;            // previous blink rate 
int x, y;                         // coordinates for text matrix 
TEXTMETRIC tm;                    // font information 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,            // window handle 
    UINT message,         // type of message 
    UINT wParam,          // additional information 
    LONG lParam)          // additional information 
{ 
 
    switch (message) 
    { 
        case WM_CREATE: 
        // Select a fixed-width system font, and get its text metrics.
 
            hdc = GetDC(hwnd); 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwnd, hdc); 
 
        // Save the avg. width and height of characters. 
 
            nCharX = tm.tmAveCharWidth; 
            nCharY = tm.tmHeight; 
 
            return 0; 
 
        case WM_SIZE: 
        // Determine the width of the client area, in pixels 
        // and in number of characters. 
 
            nWindowX = LOWORD(lParam); 
            nWindowCharsX = max(1, nWindowX/nCharX); 
 
            // Determine the height of the client area, in 
            // pixels and in number of characters. 
 
            nWindowY = HIWORD(lParam); 
            nWindowCharsY = max(1, nWindowY/nCharY); 
 
            // Clear the buffer that holds the text input. 
 
            if (pTextMatrix != NULL) 
                free(pTextMatrix); 
 
            // If there is enough memory, allocate space for the 
            // text input buffer. 
 
            pTextMatrix = malloc(nWindowCharsX * nWindowCharsY); 
 
            if (pTextMatrix == NULL) 
                ErrorHandler("Not enough memory."); 
            else 
                for (y = 0; y < nWindowCharsY; y++) 
                    for (x = 0; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, y) = ' '; 
 
            // Move the caret to the origin. 
 
            SetCaretPos(0, 0); 
 
            return 0; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_HOME:       // Home 
                    nCaretPosX = 0; 
                    break; 
 
                case VK_END:        // End 
                    nCaretPosX = nWindowCharsX - 1; 
                    break; 
 
                case VK_PRIOR:      // Page Up 
                    nCaretPosY = 0; 
                    break; 
 
                case VK_NEXT:       // Page Down 
                    nCaretPosY = nWindowCharsY -1; 
                    break; 
 
                case VK_LEFT:       // Left arrow 
                    nCaretPosX = max(nCaretPosX - 1, 0); 
                    break; 
 
                case VK_RIGHT:      // Right arrow 
                    nCaretPosX = min(nCaretPosX + 1, 
                        nWindowCharsX - 1); 
                    break; 
 
                case VK_UP:         // Up arrow 
                    nCaretPosY = max(nCaretPosY - 1, 0); 
                    break; 
 
                case VK_DOWN:       // Down arrow 
                    nCaretPosY = min(nCaretPosY + 1, 
                        nWindowCharsY - 1); 
                    break; 
 
                case VK_DELETE:     // Delete 
 
                // Move all the characters that followed the 
                // deleted character (on the same line) one 
                // space back (to the left) in the matrix. 
 
                    for (x = nCaretPosX; x < nWindowCharsX; x++) 
                        TEXTMATRIX(x, nCaretPosY) = 
                            TEXTMATRIX(x + 1, nCaretPosY); 
 
                    // Replace the last character on the 
                    // line with a space. 
 
                    TEXTMATRIX(nWindowCharsX - 1, 
                        nCaretPosY) = ' '; 
 
                    // The application will draw outside the 
                    // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                    // Redraw the line, adjusted for the 
                    // deleted character. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 
                        nWindowCharsX - nCaretPosX); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // virtual-key processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:          // Backspace 
                // Move the caret back one space, and then 
                // process this like the DEL key. 
 
                    if (nCaretPosX > 0) 
                    { 
                        nCaretPosX--; 
                        SendMessage(hwnd, WM_KEYDOWN, 
                            VK_DELETE, 1L); 
                    } 
                    break; 
 
                case 0x09:          // Tab 
                // Tab stops exist every four spaces, so add 
                // spaces until the user hits the next tab. 
 
                    do 
                    { 
                        SendMessage(hwnd, WM_CHAR, ' ', 1L); 
                    } while (nCaretPosX % 4 != 0); 
                    break; 
 
                case 0x0D:          // Carriage return 
                // Go to the beginning of the next line. 
                // The bottom line wraps around to the top. 
 
                    nCaretPosX = 0; 
 
                    if (++nCaretPosY == nWindowCharsY) 
                        nCaretPosY = 0; 
                    break; 
 
                case 0x1B:        // Escape 
                case 0x0A:        // Linefeed 
                    MessageBeep((UINT) -1); 
                    break; 
 
                default: 
                // Add the character to the text buffer. 
 
                    TEXTMATRIX(nCaretPosX, nCaretPosY) = 
                        (char) wParam; 
 
                // The application will draw outside the 
                // WM_PAINT message processing, so hide the caret. 
 
                    HideCaret(hwnd); 
 
                // Draw the character on the screen. 
 
                    hdc = GetDC(hwnd); 
                    SelectObject(hdc, 
                        GetStockObject(SYSTEM_FIXED_FONT)); 
 
                    TextOut(hdc, nCaretPosX * nCharX, 
                        nCaretPosY * nCharY, 
                        &TEXTMATRIX(nCaretPosX, nCaretPosY), 1); 
 
                    ReleaseDC(hwnd, hdc); 
 
                    // Display the caret. 
 
                    ShowCaret(hwnd); 
 
                    // Prepare to wrap around if you reached the 
                    // end of the line. 
 
                    if (++nCaretPosX == nWindowCharsX) 
                    { 
                        nCaretPosX = 0; 
                        if (++nCaretPosY == nWindowCharsY) 
                            nCaretPosY = 0; 
                    } 
                    break; 
            } 
 
            // Adjust the caret position based on the 
            // character processing. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            return 0; 
 
        case WM_PAINT: 
        // Draw all the characters in the buffer, line by line. 
 
            hdc = BeginPaint(hwnd, &ps); 
 
            SelectObject(hdc, 
                GetStockObject(SYSTEM_FIXED_FONT)); 
 
            for (y = 0; y < nWindowCharsY; y++) 
                TextOut(hdc, 0, y * nCharY, &TEXTMATRIX(0, y), 
                    nWindowCharsX); 
 
            EndPaint(hwnd, &ps); 
 
        case WM_SETFOCUS: 
        // The window has the input focus. Load the 
        // application-defined caret resource. 
 
            hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
            // Create the caret. 
 
            CreateCaret(hwnd, hCaret, 0, 0); 
 
            // Adjust the caret position. 
 
            SetCaretPos(nCaretPosX * nCharX, 
                nCaretPosY * nCharY); 
 
            // Display the caret. 
 
            ShowCaret(hwnd); 
 
            break; 
 
        case WM_KILLFOCUS: 
        // The window is losing the input focus, 
        // so destroy the caret. 
 
            DestroyCaret(); 
 
            break; 
 
        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
    } 
 
    return NULL; 
} 
```



 

 