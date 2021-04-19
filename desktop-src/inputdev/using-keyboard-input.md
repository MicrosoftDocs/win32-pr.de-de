---
title: Verwenden von Tastatureingaben
description: In diesem Abschnitt werden Aufgaben behandelt, die mit Tastatureingaben verknüpft sind.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- Benutzereingabe, Tastatureingabe
- Erfassen von Benutzereingaben, Tastatureingaben
- Tastatureingabe
- Tastatureingaben
- Zeichen Nachrichten
- Caretzeichen, Tastatureingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76b3f90a626506430b91e7539069c6ecdf634c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341933"
---
# <a name="using-keyboard-input"></a>Verwenden von Tastatureingaben

Ein Fenster empfängt Tastatureingaben in Form von Tastatureingaben und Zeichen Nachrichten. Die an das Fenster angefügte Nachrichten Schleife muss Code enthalten, um Tastatureingabe-Nachrichten in die entsprechenden Zeichen Nachrichten zu übersetzen. Wenn im Fenster der Client Bereich Tastatureingaben angezeigt werden, sollte ein Caretzeichen erstellt und angezeigt werden, um die Position anzugeben, an der das nächste Zeichen eingegeben wird. In den folgenden Abschnitten wird der Code beschrieben, der beim empfangen, verarbeiten und Anzeigen von Tastatureingaben beteiligt ist:

-   [Verarbeiten von Tastatureingaben](#processing-keystroke-messages)
-   [Übersetzen von Zeichen Meldungen](#translating-character-messages)
-   [Verarbeiten von Zeichen Meldungen](#processing-character-messages)
-   [Verwenden der Einfügemarke](#using-the-caret)
-   [Anzeigen von Tastatureingaben](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>Verarbeiten von Tastatureingaben

Die Fenster Prozedur des Fensters, das über den Tastaturfokus verfügt, empfängt Tastatureingaben, wenn der Benutzer die Tastatur eingibt. Die Tastatureingabe Nachrichten sind [**WM \_ KeyDown**](wm-keydown.md), [**WM \_ KeyUp**](wm-keyup.md), [**WM \_ syskeydown**](wm-syskeydown.md)und [**WM \_ syskeyup**](wm-syskeyup.md). Eine typische Fenster Prozedur ignoriert alle Tastatureingabe-Meldungen außer **WM \_ KeyDown**. Das System sendet die **WM- \_ KeyDown** -Nachricht, wenn der Benutzer eine Taste drückt.

Wenn die Fenster Prozedur die [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht empfängt, sollte Sie den Code der virtuellen Taste untersuchen, der die Nachricht begleitet, um zu bestimmen, wie die Tastatureingabe verarbeitet wird. Der Code des virtuellen Schlüssels befindet sich im *wParam* -Parameter der Nachricht. In der Regel verarbeitet eine Anwendung nur Tastatureingaben, die von nicht-Zeichen Schlüsseln generiert werden, z. b. die Funktionstasten, die Cursor Verschiebungs Tasten und die speziellen Schlüssel, wie z. b. ins, del, Home und End.

Das folgende Beispiel zeigt das Fenster Prozedur Framework, das eine typische Anwendung verwendet, um Tastatureingaben zu empfangen und zu verarbeiten.


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a>Übersetzen von Zeichen Meldungen

Jeder Thread, der Zeichen Eingaben vom Benutzer empfängt, muss die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion in der Nachrichten Schleife enthalten. Diese Funktion untersucht den Code für den virtuellen Schlüssel einer Tastatureingabe-Nachricht und stellt eine Zeichen Nachricht in die Meldungs Warteschlange, wenn der Code einem Zeichen entspricht. Die Zeichen Nachricht wird entfernt und bei der nächsten Iterationen der Nachrichten Schleife gesendet. der *wParam* -Parameter der Nachricht enthält den Zeichencode.

Im Allgemeinen sollte die Nachrichten Schleife eines Threads die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion verwenden, um jede Nachricht und nicht nur die Nachrichten mit einem virtuellen Schlüssel zu übersetzen. Obwohl **translatemess** keine Auswirkung auf andere Nachrichten Typen hat, wird sichergestellt, dass Tastatureingaben ordnungsgemäß übersetzt werden. Im folgenden Beispiel wird gezeigt, wie die **translatemess** -Funktion in eine typische Thread Nachrichten Schleife eingeschlossen wird.


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a>Verarbeiten von Zeichen Meldungen

Eine Fenster Prozedur empfängt eine Zeichen Nachricht, wenn die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion einen virtuellen Schlüsselcode übersetzt, der einem Zeichen Schlüssel entspricht. Die Zeichen Nachrichten lauten [**WM \_ char**](wm-char.md), [**WM \_ deadchar**](wm-deadchar.md), [**WM \_ Sychar**](/windows/desktop/menurc/wm-syschar)und [**WM \_ sysdeadchar**](wm-sysdeadchar.md). Eine typische Fenster Prozedur ignoriert alle Zeichen Meldungen außer **WM \_ char**. Die **translatemess** -Funktion generiert eine **WM- \_ char** -Nachricht, wenn der Benutzer einen der folgenden Schlüssel drückt:

-   Beliebige Zeichen Taste
-   RÜCKTASTE
-   EINGABETASTE (Wagen Rücklauf)
-   ESC
-   UMSCHALT + Eingabe (Zeilenvorschub)
-   TAB

Wenn eine Fenster Prozedur die Meldung " [**WM \_ char**](wm-char.md) " empfängt, sollte Sie den Zeichencode untersuchen, der die Nachricht begleitet, um zu bestimmen, wie das Zeichen verarbeitet werden soll. Der Zeichencode befindet sich im *wParam* -Parameter der Nachricht.

Das folgende Beispiel zeigt das Fenster Prozedur Framework, das eine typische Anwendung verwendet, um Zeichen Nachrichten zu empfangen und zu verarbeiten.


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a>Verwenden der Einfügemarke

Ein Fenster, das Tastatureingaben empfängt, zeigt in der Regel die Zeichen an, die der Benutzer im Client Bereich des Fensters eingibt. Ein Fenster sollte eine Einfügemarke verwenden, um die Position im Client Bereich anzugeben, an der das nächste Zeichen angezeigt wird. Das Fenster sollte auch die Einfügemarke beim Empfang des Tastaturfokus erstellen und anzeigen und die Einfügemarke ausblenden und zerstören, wenn Sie den Fokus verliert. Diese Vorgänge können von einem Fenster bei der Verarbeitung der Nachrichten " [**WM \_ SetFocus**](wm-setfocus.md) " und " [**WM \_ killfocus**](wm-killfocus.md) " durchgeführt werden. Weitere Informationen zu Carets finden Sie unter [Caretzeichen](/windows/desktop/menurc/carets).

## <a name="displaying-keyboard-input"></a>Anzeigen von Tastatureingaben

Das Beispiel in diesem Abschnitt zeigt, wie eine Anwendung Zeichen von der Tastatur empfangen, Sie im Client Bereich eines Fensters anzeigen und die Position der Einfügemarke mit jedem typisierten Zeichen aktualisieren kann. Außerdem wird veranschaulicht, wie die Einfügemarke in Reaktion auf den nach-links-Pfeil, den Pfeil nach rechts, den Pfeil nach rechts und den Ende Tastatureingaben verschoben wird, und zeigt, wie ausgewählter Text als Reaktion auf die Tastenkombination UMSCHALT + nach-rechts hervorgehoben wird

Während der Verarbeitung der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung wird durch die im Beispiel gezeigte Fenster Prozedur ein 64K-Puffer zum Speichern von Tastatureingaben zugeordnet. Außerdem werden die Metriken der aktuell geladenen Schriftart abgerufen, und die Höhe und die durchschnittliche Breite der Zeichen in der Schriftart werden gespeichert. Die Höhe und Breite werden bei der Verarbeitung der [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verwendet, um die Zeilenlänge und die maximale Zeilen Anzahl basierend auf der Größe des Client Bereichs zu berechnen.

Die Fenster Prozedur erstellt die Einfügemarke und zeigt diese an, wenn die [**WM \_ SetFocus**](wm-setfocus.md) -Nachricht verarbeitet wird. Beim Verarbeiten der [**WM- \_ killfocus**](wm-killfocus.md) -Nachricht wird die Einfügemarke ausgeblendet und gelöscht.

Bei der Verarbeitung der " [**WM \_ char**](wm-char.md) "-Nachricht zeigt die Fenster Prozedur Zeichen an, speichert Sie im Eingabepuffer und aktualisiert die Position der Einfügemarke. Die Fenster Prozedur konvertiert auch Tabstopp Zeichen in vier aufeinander folgende Leerzeichen. Rücktaste, linefeed und Escapezeichen generieren ein Signal, werden jedoch nicht anderweitig verarbeitet.

Die Fenster Prozedur führt bei der Verarbeitung der [**WM- \_ keydownnachricht**](wm-keydown.md) die Bewegungen Links, rechts, Ende und Home Caretzeichen aus. Bei der Verarbeitung der Aktion der nach-rechts-Taste wird der Zustand der Umschalttaste von der Fenster Prozedur überprüft. wenn der Wert nicht ist, wird das Zeichen rechts neben der Einfügemarke ausgewählt, wenn die Einfügemarke verschoben wird.

Beachten Sie, dass der folgende Code so geschrieben ist, dass er entweder als Unicode oder als ANSI kompiliert werden kann. Wenn der Quellcode Unicode definiert, werden Zeichen folgen als Unicode-Zeichen behandelt. Andernfalls werden Sie als ANSI-Zeichen behandelt.


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 