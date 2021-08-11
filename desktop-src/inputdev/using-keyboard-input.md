---
title: Verwenden der Tastatureingabe
description: In diesem Abschnitt werden Aufgaben behandelt, die tastatureingaben zugeordnet sind.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- Benutzereingabe, Tastatureingabe
- Erfassen von Benutzereingaben, Tastatureingaben
- Tastatureingabe
- Tastatureingabenachrichten
- Zeichenmeldungen
- Carets, Tastatureingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1be8753ec6a5f920f09f6e5376b7988a88de0f9a49551492408e84908bb0c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248272"
---
# <a name="using-keyboard-input"></a>Verwenden der Tastatureingabe

Ein Fenster empfängt Tastatureingaben in Form von Tastatureingabenachrichten und Zeichenmeldungen. Die an das Fenster angefügte Nachrichtenschleife muss Code enthalten, um Tastatureingabenachrichten in die entsprechenden Zeichenmeldungen zu übersetzen. Wenn im Fenster Tastatureingaben im Clientbereich angezeigt werden, sollte ein Caretzeichen erstellt und angezeigt werden, um die Position anzugeben, an der das nächste Zeichen eingegeben wird. In den folgenden Abschnitten wird der Code beschrieben, der am Empfangen, Verarbeiten und Anzeigen von Tastatureingaben beteiligt ist:

-   [Verarbeiten von Tastatureingabenachrichten](#processing-keystroke-messages)
-   [Übersetzen von Zeichennachrichten](#translating-character-messages)
-   [Verarbeiten von Zeichenmeldungen](#processing-character-messages)
-   [Verwenden von Caret](#using-the-caret)
-   [Anzeigen von Tastatureingaben](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a>Verarbeiten von Tastatureingabenachrichten

Die Fensterprozedur des Fensters mit dem Tastaturfokus empfängt Tastatureingabemeldungen, wenn der Benutzer die Tastatur eingibt. Die Tastatureingabenachrichten sind [**WM \_ KEYDOWN,**](wm-keydown.md) [**WM \_ KEYUP,**](wm-keyup.md) [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)und [**WM \_ SYSKEYUP.**](wm-syskeyup.md) Eine typische Fensterprozedur ignoriert alle Tastatureingabemeldungen außer **WM \_ KEYDOWN**. Das System sendet die **WM \_ KEYDOWN-Nachricht,** wenn der Benutzer eine Taste drückt.

Wenn die Fensterprozedur die [**WM \_ KEYDOWN-Nachricht**](wm-keydown.md) empfängt, sollte sie den Code des virtuellen Schlüssels untersuchen, der die Nachricht begleitet, um zu bestimmen, wie die Tastatureingabe verarbeitet werden soll. Der Code des virtuellen Schlüssels befindet sich im *wParam-Parameter* der Nachricht. In der Regel verarbeitet eine Anwendung nur Tastatureingaben, die von Nichtzeichenschlüsseln generiert werden, einschließlich der Funktionsschlüssel, der Cursorbewegungsschlüssel und der speziellen Schlüssel wie INS, DEL, HOME und END.

Das folgende Beispiel zeigt das Fensterprozedurframework, das eine typische Anwendung verwendet, um Tastatureingabenachrichten zu empfangen und zu verarbeiten.


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



## <a name="translating-character-messages"></a>Übersetzen von Zeichennachrichten

Jeder Thread, der Zeicheneingaben vom Benutzer empfängt, muss die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) in seine Nachrichtenschleife einschließen. Diese Funktion untersucht den Virtuellen Schlüsselcode einer Tastatureingabenachricht und platziert, wenn der Code einem Zeichen entspricht, eine Zeichennachricht in die Nachrichtenwarteschlange. Die Zeichennachricht wird entfernt und bei der nächsten Iteration der Nachrichtenschleife gesendet. Der *wParam-Parameter* der Nachricht enthält den Zeichencode.

Im Allgemeinen sollte die Nachrichtenschleife eines Threads die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) verwenden, um jede Nachricht zu übersetzen, nicht nur Nachrichten mit virtuellen Schlüsseln. **TranslateMessage** hat zwar keine Auswirkungen auf andere Nachrichtentypen, garantiert jedoch, dass tastatureingaben ordnungsgemäß übersetzt werden. Das folgende Beispiel zeigt, wie die **TranslateMessage-Funktion** in eine typische Threadnachrichtenschleife eingeschlossen wird.


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



## <a name="processing-character-messages"></a>Verarbeiten von Zeichenmeldungen

Eine Fensterprozedur empfängt eine Zeichenmeldung, wenn die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) einen virtuellen Schlüsselcode übersetzt, der einem Zeichenschlüssel entspricht. Die Zeichenmeldungen sind [**WM \_ CHAR,**](wm-char.md) [**WM \_ DEADCHAR,**](wm-deadchar.md) [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)und [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md). Eine typische Fensterprozedur ignoriert alle Zeichenmeldungen außer **WM \_ CHAR**. Die **TranslateMessage-Funktion** generiert eine **WM \_ CHAR-Nachricht,** wenn der Benutzer einen der folgenden Tasten drückt:

-   Beliebiger Zeichenschlüssel
-   RÜCKTASTE
-   EINGABETASTE (Wagenrücklauf)
-   ESC
-   UMSCHALT+EINGABETASTE (Zeilenumbruch)
-   TAB

Wenn eine Fensterprozedur die [**WM \_ CHAR-Nachricht**](wm-char.md) empfängt, sollte sie den Zeichencode untersuchen, der die Nachricht begleitet, um zu bestimmen, wie das Zeichen verarbeitet werden soll. Der Zeichencode befindet sich im *wParam-Parameter* der Nachricht.

Das folgende Beispiel zeigt das Fensterprozedurframework, das eine typische Anwendung verwendet, um Zeichenmeldungen zu empfangen und zu verarbeiten.


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



## <a name="using-the-caret"></a>Verwenden von Caret

Ein Fenster, das Tastatureingaben empfängt, zeigt in der Regel die Zeichen an, die der Benutzer im Clientbereich des Fensters eingibt. Ein Fenster sollte ein Caretzeichen verwenden, um die Position im Clientbereich anzugeben, an der das nächste Zeichen angezeigt wird. Das Fenster sollte auch das Caretfeld erstellen und anzeigen, wenn es den Tastaturfokus erhält, und das Caretfeld ausblenden und zerstören, wenn es den Fokus verliert. Ein Fenster kann diese Vorgänge bei der Verarbeitung der [**WM \_ SETFOCUS-**](wm-setfocus.md) und [**WM \_ KILLFOCUS-Meldungen**](wm-killfocus.md) ausführen. Weitere Informationen zu Carets finden Sie unter [Carets](/windows/desktop/menurc/carets).

## <a name="displaying-keyboard-input"></a>Anzeigen von Tastatureingaben

Das Beispiel in diesem Abschnitt zeigt, wie eine Anwendung Zeichen von der Tastatur empfangen, im Clientbereich eines Fensters anzeigen und die Position des Caretzeichens mit jedem eingegebenen Zeichen aktualisieren kann. Außerdem wird veranschaulicht, wie das Caretzeichen als Reaktion auf die TastenkombinationEN NACH-LINKS-PFEIL, NACH-RECHTS-TASTE, HOME und END verschoben wird. Außerdem wird gezeigt, wie ausgewählter Text als Reaktion auf die Tastenkombination UMSCHALT+NACH-RECHTS-TASTE hervorgehoben wird.

Während der Verarbeitung der [**WM \_ CREATE-Nachricht**](/windows/desktop/winmsg/wm-create) ordnet die im Beispiel gezeigte Fensterprozedur einen 64K-Puffer zum Speichern von Tastatureingaben zu. Außerdem werden die Metriken der aktuell geladenen Schriftart abgerufen, wodurch die Höhe und die durchschnittliche Breite der Zeichen in der Schriftart gespeichert werden. Die Höhe und Breite werden bei der Verarbeitung der [**WM \_ SIZE-Nachricht**](/windows/desktop/winmsg/wm-size) verwendet, um die Zeilenlänge und die maximale Anzahl von Zeilen basierend auf der Größe des Clientbereichs zu berechnen.

Die Fensterprozedur erstellt das Caretzeichen und zeigt es an, wenn die [**WM \_ SETFOCUS-Meldung**](wm-setfocus.md) verarbeitet wird. Das Caretzeichen wird ausgeblendet und gelöscht, wenn die [**WM \_ KILLFOCUS-Nachricht**](wm-killfocus.md) verarbeitet wird.

Beim Verarbeiten der [**WM \_ CHAR-Nachricht**](wm-char.md) zeigt die Fensterprozedur Zeichen an, speichert sie im Eingabepuffer und aktualisiert die Position des Caretzeichens. Die Fensterprozedur konvertiert tabellarische Zeichen auch in vier aufeinanderfolgende Leerzeichen. Rücktasten-, Zeilenfeed- und Escapezeichen generieren einen Signalton, werden aber nicht anderweitig verarbeitet.

Die Fensterprozedur führt beim Verarbeiten der [**WM \_ KEYDOWN-Nachricht**](wm-keydown.md) die Bewegungen links, rechts, end und home caret aus. Beim Verarbeiten der Aktion der NACH-RECHTS-TASTE überprüft die Fensterprozedur den Zustand der UMSCHALTTASTE und wählt das Zeichen rechts neben dem Caretzeichen aus, wenn das Caretzeichen verschoben wird.

Beachten Sie, dass der folgende Code so geschrieben ist, dass er entweder als Unicode oder als ANSI kompiliert werden kann. Wenn der Quellcode UNICODE definiert, werden Zeichenfolgen als Unicode-Zeichen behandelt. andernfalls werden sie als ANSI-Zeichen behandelt.


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



 

 