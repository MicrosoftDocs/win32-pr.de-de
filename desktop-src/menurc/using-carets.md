---
title: Verwenden von Caretzeichen
description: Dieser Abschnitt enthält Codebeispiele, die das Ausführen von Aufgaben im Zusammenhang mit Caretzeichen veranschaulichen.
ms.assetid: 82b0a84c-49a9-4d9d-b4c8-7c4511d863eb
keywords:
- Ressourcen, Caretzeichen
- Caretzeichen, erstellen
- Caretzeichen, anzeigen
- Caretzeichen, zerstören
- Caretzeichen, ausblenden
- Caretzeichen, blinkende Zeiten
- blinkende Linien
- blinkende Blöcke
- blinken von Bitmaps
- Erstellen von Caretzeichen
- Anzeigen von Caretzeichen
- Ausblenden von Caretzeichen
- zerstören von Caretzeichen
- blinkende Zeiten
- Benutzereingabe, Tastatureingabe
- Erfassen von Benutzereingaben, Tastatureingaben
- Tastatureingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6450a3169588b3072d1fee271f4890a7cdeafd2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038882"
---
# <a name="using-carets"></a>Verwenden von Caretzeichen

Dieser Abschnitt enthält Codebeispiele für die folgenden Aufgaben:

-   [Erstellen und Anzeigen einer Einfügemarke](#creating-and-displaying-a-caret)
-   [Ausblenden einer Einfügemarke](#hiding-a-caret)
-   [Zerstören eines Caretzeichen](#destroying-a-caret)
-   [Anpassen der Blink Zeit](#adjusting-the-blink-time)
-   [Verarbeiten von Tastatureingaben](#processing-keyboard-input)

## <a name="creating-and-displaying-a-caret"></a>Erstellen und Anzeigen einer Einfügemarke

Wenn Sie den Tastaturfokus erhalten, sollte das Fenster die Einfügemarke erstellen und anzeigen. Verwenden Sie die Funktion " [**kreatecaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) ", um eine Einfügemarke im angegebenen Fenster zu erstellen. Sie können dann [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) aufrufen, um die aktuelle Position der Einfügemarke und des [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) festzulegen, um die Einfügemarke sichtbar zu machen.

Das System sendet die [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht an das Fenster, das den Tastaturfokus erhält. Daher sollte eine Anwendung die Einfügemarke bei der Verarbeitung dieser Nachricht erstellen und anzeigen.


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



Wenn Sie eine Einfügemarke auf der Grundlage einer Bitmap erstellen möchten, müssen Sie bei der Verwendung von " [**anatecaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)" ein Bitmaphandle angeben. Sie können eine Grafikanwendung verwenden, um die Bitmap und einen Ressourcen Compiler zu erstellen, um die Bitmap den Ressourcen Ihrer Anwendung hinzuzufügen. Die Anwendung kann dann die [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion verwenden, um das Bitmap-Handle zu laden. Beispielsweise können Sie die Zeile " **anatecaret** " im vorherigen Beispiel durch die folgenden Zeilen ersetzen, um eine Bitmap-Einfügemarke zu erstellen.


```
// Load the application-defined caret resource. 
 
    hCaret = LoadBitmap(hinst, MAKEINTRESOURCE(120)); 
 
// Create a bitmap caret. 
 
    CreateCaret(hwnd, hCaret, 0, 0); 
```



Alternativ dazu können [**Sie die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) "up" oder " [**reatedibitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) " verwenden, um das Handle der Bitmap für die Einfügemarke abzurufen. Weitere Informationen zu Bitmaps finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

Wenn Ihre Anwendung ein Bitmap-Handle angibt, ignoriert " [**kreatecaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) " die Parameter "width" und "Height". Die Bitmap definiert die Größe der Einfügemarke.

## <a name="hiding-a-caret"></a>Ausblenden einer Einfügemarke

Wenn Ihre Anwendung während der Verarbeitung einer anderen Nachricht als [**WM \_ Paint**](/windows/desktop/gdi/wm-paint)einen Bildschirm neu zeichnet, muss die Einfügemarke mithilfe der [**hideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) -Funktion unsichtbar werden. Wenn die Anwendung abgeschlossen ist, zeigen Sie die Einfügemarke mithilfe der [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) -Funktion erneut an. Wenn die Anwendung die **WM- \_** Zeichnungs Nachricht verarbeitet, ist es nicht notwendig, die Einfügemarke auszublenden und erneut anzuzeigen, da diese Funktion dies automatisch erledigt.

Im folgenden Codebeispiel wird veranschaulicht, wie die Anwendung die Einfügemarke ausblenden kann, während ein Zeichen auf dem Bildschirm gezeichnet und die [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht verarbeitet wird.


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



Wenn die Anwendung die [**hideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) -Funktion mehrmals aufruft, ohne [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)aufzurufen, wird die Einfügemarke erst angezeigt, wenn die Anwendung **ShowCaret** gleich oft aufruft.

## <a name="destroying-a-caret"></a>Zerstören eines Caretzeichen

Wenn ein Fenster den Tastaturfokus verliert, sendet das System die [**WM- \_ killfocus**](/windows/desktop/inputdev/wm-killfocus) -Meldung an das Fenster. Die Anwendung sollte die Einfügemarke bei der Verarbeitung dieser Nachricht mithilfe der [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) -Funktion zerstören. Der folgende Code zeigt, wie Sie eine Einfügemarke in einem Fenster, das nicht mehr über den Tastaturfokus verfügt, zerstören.


```
case WM_KILLFOCUS: 
 
// The window is losing the keyboard focus, so destroy the caret. 
 
    DestroyCaret(); 
 
    break; 
```



## <a name="adjusting-the-blink-time"></a>Anpassen der Blink Zeit

In 16-Bit-Fenstern könnte eine Windows-basierte Anwendung die [**getcaretblinktime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) -Funktion aufrufen, um die aktuelle Blink Zeit zu speichern, und dann die [**setcaretblinktime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) -Funktion aufrufen, um die Blink Zeit während der Verarbeitung der [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht anzupassen. Die Anwendung würde die gespeicherte Blink Zeit für die Verwendung anderer Anwendungen wiederherstellen, indem **setcaretblinktime** während der Verarbeitung der [**WM- \_ killfocus**](/windows/desktop/inputdev/wm-killfocus) -Nachricht aufgerufen wird. Diese Methode funktioniert jedoch nicht in Multithread-Umgebungen. Insbesondere die Aktivierung einer Anwendung wird nicht mit der Aktivierung einer anderen Anwendung synchronisiert, sodass eine andere Anwendung auch dann aktiviert werden kann, wenn eine Anwendung nicht mehr reagiert.

Anwendungen sollten die vom Benutzer gewählte Blink Zeit berücksichtigen. Die [**setcaretblinktime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) -Funktion sollte nur von einer Anwendung aufgerufen werden, die es dem Benutzer ermöglicht, die Blink Zeit festzulegen.

## <a name="processing-keyboard-input"></a>Verarbeiten von Tastatureingaben

Im folgenden Beispiel wird veranschaulicht, wie eine Einfügemarke in einem einfachen Text-Editor verwendet wird. Im Beispiel wird die Position der Einfügemarke aktualisiert, wenn der Benutzer druckbare Zeichen eingibt und verschiedene Schlüssel verwendet, um durch den Client Bereich zu navigieren.


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



 

 