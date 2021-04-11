---
title: Verwenden von Maus Eingaben
description: In diesem Abschnitt werden die mit der Maus Eingaben verknüpften Aufgaben behandelt.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- Benutzereingabe, Mauseingabe
- Erfassen von Benutzereingaben, Maus Eingaben
- Mauseingabe
- Cursor, Maus Eingaben
- Mauszeiger
- Doppelklicken Sie auf Nachrichtenverarbeitung.
- Mausrad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b34f180aad6aec6120bf4e3ffa997eba13e760
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314943"
---
# <a name="using-mouse-input"></a>Verwenden von Maus Eingaben

In diesem Abschnitt werden die mit der Maus Eingaben verknüpften Aufgaben behandelt.

-   [Nachverfolgen des Maus Cursors](#tracking-the-mouse-cursor)
-   [Zeichnen von Linien mit der Maus](#drawing-lines-with-the-mouse)
-   [Verarbeiten einer Doppelklick Nachricht](#processing-a-double-click-message)
-   [Auswählen einer Textzeile](#selecting-a-line-of-text)
-   [Verwenden eines Mausrades in einem Dokument mit eingebetteten Objekten](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [Abrufen der Anzahl von Mausrad-scrolllinien](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a>Nachverfolgen des Maus Cursors

Anwendungen führen häufig Aufgaben aus, die die Position des Mauszeigers überwachen. Die meisten Zeichnungs Anwendungen können z. b. die Position des Mauszeigers während Zeichnungs Vorgängen verfolgen, sodass der Benutzer den Client Bereich eines Fensters durchziehen der Maus zeichnen kann. Textverarbeitungsanwendungen verfolgen den Cursor auch nach, um dem Benutzer zu ermöglichen, ein Wort oder einen Textblock auszuwählen, indem Sie darauf klicken und die Maus ziehen.

Die Nachverfolgung des Cursors umfasst in der Regel die Verarbeitung der Nachrichten [**WM \_ lbuttondown**](wm-lbuttondown.md), [**WM \_ mousetmove**](wm-mousemove.md)und [**WM \_ lbuttonup**](wm-lbuttonup.md) . Ein Fenster bestimmt, wann mit der Nachverfolgung des Cursors begonnen werden soll, indem die Cursorposition im *LPARAM* -Parameter der **WM- \_ lbuttondown** -Meldung überprüft wird. Beispielsweise beginnt eine Textverarbeitungsanwendung nur dann mit der Nachverfolgung des Cursors, wenn die **WM- \_ lbuttondown** -Nachricht aufgetreten ist, während sich der Cursor in einer Textzeile befand, aber nicht, wenn Sie sich hinter dem Ende des Dokuments befand.

Ein Fenster verfolgt die Position des Cursors, indem der Stream von [**WM- \_ MouseMove**](wm-mousemove.md) -Meldungen verarbeitet wird, die beim Bewegen der Maus an das Fenster gesendet werden. Die Verarbeitung der **WM- \_ mouseemove** -Nachricht umfasst in der Regel einen sich wiederholenden Zeichnungs-oder Zeichnungs Vorgang im Client Bereich. Beispielsweise kann eine Zeichnungsanwendung eine Zeile wiederholt neu zeichnen, wenn die Maus bewegt wird. Ein Fenster verwendet die [**WM- \_ lbuttonup**](wm-lbuttonup.md) -Meldung als Signal, um die Nachverfolgung des Cursors zu verhindern.

Außerdem kann eine Anwendung die [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) -Funktion aufrufen, damit das System andere Meldungen sendet, die für die Nachverfolgung des Cursors nützlich sind. Das System sendet die [**WM- \_ MouseHover**](wm-mousehover.md) -Nachricht, wenn der Cursor für einen bestimmten Zeitraum über den Client Bereich bewegt wird. Sie sendet die [**WM- \_ MouseLeave**](wm-mouseleave.md) -Nachricht, wenn der Cursor den Client Bereich verlässt. Die Nachrichten " [**WM \_ ncmouanhover**](wm-ncmousehover.md) " und " [**WM \_ ncmouseleave**](wm-ncmouseleave.md) " sind die entsprechenden Nachrichten für die nicht-Client Bereiche.

## <a name="drawing-lines-with-the-mouse"></a>Zeichnen von Linien mit der Maus

Das Beispiel in diesem Abschnitt veranschaulicht, wie der Mauszeiger nachverfolgt wird. Sie enthält Teile einer Fenster Prozedur, mit der der Benutzer durchziehen der Maus Zeilen im Client Bereich eines Fensters zeichnen kann.

Wenn die Fenster Prozedur eine [**WM \_ lbuttondown**](wm-lbuttondown.md) -Nachricht empfängt, wird die Maus erfasst und die Koordinaten des Cursors gespeichert, wobei die Koordinaten als Ausgangspunkt der Linie verwendet werden. Außerdem wird die [**clipcursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) -Funktion verwendet, um den Cursor während des Zeilen Zeichnungs Vorgangs auf den Client Bereich einzuschränken.

Während der ersten [**WM- \_ mousetmove**](wm-mousemove.md) -Nachricht zeichnet die Fenster Prozedur eine Linie vom Startpunkt bis zur aktuellen Cursorposition. Während der nachfolgenden **WM- \_ MouseMove** -Nachrichten löscht die Fenster Prozedur die vorherige Zeile, indem Sie mit einer umgekehrten Stift Farbe gezeichnet wird. Anschließend wird eine neue Zeile vom Ausgangspunkt zur neuen Position des Cursors gezeichnet.

Die [**WM- \_ lbuttonup**](wm-lbuttonup.md) -Meldung signalisiert das Ende der Zeichnungs Operation. Die Fenster Prozedur gibt die Maus Aufzeichnung frei und gibt die Maus aus dem Client Bereich frei.


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                       // handle to device context 
    RECT rcClient;                 // client area rectangle 
    POINT ptClientUL;              // client upper left corner 
    POINT ptClientLR;              // client lower right corner 
    static POINTS ptsBegin;        // beginning point 
    static POINTS ptsEnd;          // new endpoint 
    static POINTS ptsPrevEnd;      // previous endpoint 
    static BOOL fPrevLine = FALSE; // previous line flag 
 
    switch (uMsg) 
    { 
       case WM_LBUTTONDOWN: 
 
            // Capture mouse input. 
 
            SetCapture(hwndMain); 
 
            // Retrieve the screen coordinates of the client area, 
            // and convert them into client coordinates. 
 
            GetClientRect(hwndMain, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
 
            // Add one to the right and bottom sides, because the 
            // coordinates retrieved by GetClientRect do not 
            // include the far left and lowermost pixels. 
 
            ptClientLR.x = rcClient.right + 1; 
            ptClientLR.y = rcClient.bottom + 1; 
            ClientToScreen(hwndMain, &ptClientUL); 
            ClientToScreen(hwndMain, &ptClientLR); 
 
            // Copy the client coordinates of the client area 
            // to the rcClient structure. Confine the mouse cursor 
            // to the client area by passing the rcClient structure 
            // to the ClipCursor function. 
 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            ClipCursor(&rcClient); 
 
            // Convert the cursor coordinates into a POINTS 
            // structure, which defines the beginning point of the 
            // line drawn during a WM_MOUSEMOVE message. 
 
            ptsBegin = MAKEPOINTS(lParam); 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // When moving the mouse, the user must hold down 
            // the left mouse button to draw lines. 
 
            if (wParam & MK_LBUTTON) 
            { 
 
                // Retrieve a device context (DC) for the client area. 
 
                hdc = GetDC(hwndMain); 
 
                // The following function ensures that pixels of 
                // the previously drawn line are set to white and 
                // those of the new line are set to black. 
 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a line was drawn during an earlier WM_MOUSEMOVE 
                // message, draw over it. This erases the line by 
                // setting the color of its pixels to white. 
 
                if (fPrevLine) 
                { 
                    MoveToEx(hdc, ptsBegin.x, ptsBegin.y, 
                        (LPPOINT) NULL); 
                    LineTo(hdc, ptsPrevEnd.x, ptsPrevEnd.y); 
                } 
 
                // Convert the current cursor coordinates to a 
                // POINTS structure, and then draw a new line. 
 
                ptsEnd = MAKEPOINTS(lParam); 
                MoveToEx(hdc, ptsBegin.x, ptsBegin.y, (LPPOINT) NULL); 
                LineTo(hdc, ptsEnd.x, ptsEnd.y); 
 
                // Set the previous line flag, save the ending 
                // point of the new line, and then release the DC. 
 
                fPrevLine = TRUE; 
                ptsPrevEnd = ptsEnd; 
                ReleaseDC(hwndMain, hdc); 
            } 
            break; 
 
        case WM_LBUTTONUP: 
 
            // The user has finished drawing the line. Reset the 
            // previous line flag, release the mouse cursor, and 
            // release the mouse capture. 
 
            fPrevLine = FALSE; 
            ClipCursor(NULL); 
            ReleaseCapture(); 
            return 0; 
 
        case WM_DESTROY: 
            PostQuitMessage(0); 
            break; 
 
        // Process other messages. 
        
```



## <a name="processing-a-double-click-message"></a>Verarbeiten einer Doppelklick Nachricht

Um Doppelklick Nachrichten zu empfangen, muss ein Fenster zu einer Fenster Klasse gehören, die über den Klassen Stil [**CS \_ dblclert**](/windows/desktop/winmsg/about-window-classes) verfügt. Sie legen diesen Stil fest, wenn Sie die Fenster Klasse registrieren, wie im folgenden Beispiel gezeigt.


```
BOOL InitApplication(HINSTANCE hInstance) 
{ 
    WNDCLASS wc; 
 
    wc.style = CS_DBLCLKS | CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hInstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_IBEAM); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName = "MainMenu"; 
    wc.lpszClassName = "MainWClass"; 
 
    return RegisterClass(&wc); 
} 
```



Einer Doppelklick Nachricht wird immer eine Schaltflächen-nach-unten-Meldung vorangestellt. Aus diesem Grund verwenden Anwendungen in der Regel eine Doppelklick Nachricht, um eine Aufgabe zu erweitern, die während einer Schaltflächen-nach-unten-Nachricht gestartet wurde.

## <a name="selecting-a-line-of-text"></a>Auswählen einer Textzeile

Das Beispiel in diesem Abschnitt stammt aus einer einfachen Textverarbeitungsanwendung. Sie enthält Code, mit dem der Benutzer die Position der Einfügemarke festlegen kann, indem er auf eine Textzeile klickt und eine Textzeile durch Doppelklicken auf eine beliebige Stelle in der Zeile auswählen (markieren).


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                     // handle to device context 
    TEXTMETRIC tm;               // font size data 
    int i, j;                    // loop counters 
    int cCR = 0;                 // count of carriage returns 
    char ch;                     // character from input buffer 
    static int nBegLine;         // beginning of selected line 
    static int nCurrentLine = 0; // currently selected line 
    static int nLastLine = 0;    // last text line 
    static int nCaretPosX = 0;   // x-coordinate of caret 
    static int cch = 0;          // number of characters entered 
    static int nCharWidth = 0;   // exact width of a character 
    static char szHilite[128];   // text string to highlight 
    static DWORD dwCharX;        // average width of characters 
    static DWORD dwLineHeight;   // line height 
    static POINTS ptsCursor;     // coordinates of mouse cursor 
    static COLORREF crPrevText;  // previous text color 
    static COLORREF crPrevBk;    // previous background color 
    static PTCHAR pchInputBuf;   // pointer to input buffer 
    static BOOL fTextSelected = FALSE; // text-selection flag 
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
            dwLineHeight = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
 
            return 0; 
 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep( (UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return, and position the 
                    // caret at the beginning of the new line. 
 
                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCurrentLine += 1; 
                    break; 
 
                default:    / displayable character 
 
                    ch = (char) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width, and display the 
                    // character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, 
                        nCurrentLine * dwLineHeight, &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer. 
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the new position exceeds the maximum, 
                    // insert a carriage return and reposition the 
                    // caret at the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwMaxCharX) 
                    { 
                        nCaretPosX = 0; 
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCurrentLine; 
                    } 
 
                    ShowCaret(hwndMain); 
 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            nLastLine = max(nLastLine, nCurrentLine); 
            break; 
 
        // Process other messages. 
 
        case WM_LBUTTONDOWN: 
 
            // If a line of text is currently highlighted, redraw 
            // the text to remove the highlighting. 
 
            if (fTextSelected) 
            { 
                hdc = GetDC(hwndMain); 
                SetTextColor(hdc, crPrevText); 
                SetBkColor(hdc, crPrevBk);
                hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
                if (FAILED(hResult))
                {
                // TODO: write error handler
                } 
                TextOut(hdc, 0, nCurrentLine * dwLineHeight, 
                    szHilite, *pcch); 
                ReleaseDC(hwndMain, hdc); 
                ShowCaret(hwndMain); 
                fTextSelected = FALSE; 
            } 
 
            // Save the current mouse-cursor coordinates. 
 
            ptsCursor = MAKEPOINTS(lParam); 
 
            // Determine which line the cursor is on, and save 
            // the line number. Do not allow line numbers greater 
            // than the number of the last line of text. The 
            // line number is later multiplied by the average height 
            // of the current font. The result is used to set the 
            // y-coordinate of the caret. 
 
            nCurrentLine = min((int)(ptsCursor.y / dwLineHeight), 
                nLastLine); 
 
            // Parse the text input buffer to find the first 
            // character in the selected line of text. Each 
            // line ends with a carriage return, so it is possible 
            // to count the carriage returns to find the selected 
            // line. 
 
            cCR = 0; 
            nBegLine = 0; 
            if (nCurrentLine != 0) 
            { 
                for (i = 0; (i < cch) && 
                        (cCR < nCurrentLine); i++) 
                { 
                    if (pchInputBuf[i] == 0x0D) 
                        ++cCR; 
                } 
                nBegLine = i; 
            } 
 
            // Starting at the beginning of the selected line, 
            // measure  the width of each character, summing the 
            // width with each character measured. Stop when the 
            // sum is greater than the x-coordinate of the cursor. 
            // The sum is used to set the x-coordinate of the caret. 
 
            hdc = GetDC(hwndMain); 
            nCaretPosX = 0; 
            for (i = nBegLine; 
                (pchInputBuf[i] != 0x0D) && (i < cch); i++) 
            { 
                ch = pchInputBuf[i]; 
                GetCharWidth32(hdc, (int) ch, (int) ch, &nCharWidth); 
                if ((nCaretPosX + nCharWidth) > ptsCursor.x) break; 
                else nCaretPosX += nCharWidth; 
            } 
            ReleaseDC(hwndMain, hdc); 
 
            // Set the caret to the user-selected position. 
 
            SetCaretPos(nCaretPosX, nCurrentLine * dwLineHeight); 
            break; 
 
        case WM_LBUTTONDBLCLK: 
 
            // Copy the selected line of text to a buffer. 
 
            for (i = nBegLine, j = 0; (pchInputBuf[i] != 0x0D) && 
                    (i < cch); i++) 
            {
                szHilite[j++] = pchInputBuf[i]; 
            }
            szHilite[j] = '\0'; 
 
            // Hide the caret, invert the background and foreground 
            // colors, and then redraw the selected line. 
 
            HideCaret(hwndMain); 
            hdc = GetDC(hwndMain); 
            crPrevText = SetTextColor(hdc, RGB(255, 255, 255)); 
            crPrevBk = SetBkColor(hdc, RGB(0, 0, 0));
            hResult = StringCchLength(szHilite, 128/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 0, nCurrentLine * dwLineHeight, szHilite, *pcch); 
            SetTextColor(hdc, crPrevText); 
            SetBkColor(hdc, crPrevBk); 
            ReleaseDC(hwndMain, hdc); 
 
            fTextSelected = TRUE; 
            break; 

            // Process other messages. 

        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a>Verwenden eines Mausrades in einem Dokument mit eingebetteten Objekten

In diesem Beispiel wird ein Microsoft Word-Dokument mit verschiedenen eingebetteten Objekten angenommen:

-   Eine Microsoft Excel-Tabelle
-   Ein eingebettetes Listenfeld-Steuerelement, das als Reaktion auf das Rad scrollt
-   Ein eingebettetes Textfeld-Steuerelement, das nicht auf das Rad reagiert.

Die [msh \_ mouswheel](about-mouse-input.md) -Meldung wird immer an das Hauptfenster in Microsoft Word gesendet. Dies gilt auch, wenn die eingebettete Kalkulations Tabelle aktiv ist. In der folgenden Tabelle wird erläutert, wie die msh \_ mouelwheel-Nachricht entsprechend dem Fokus verarbeitet wird.



| Fokus ist on                | Die Verarbeitung erfolgt wie folgt:                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Word-Dokument              | Word scrollt das Dokument Fenster.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Eingebettete Excel-Tabelle | Word sendet die Nachricht an Excel. Sie müssen entscheiden, ob die eingebettete Anwendung auf die Nachricht reagieren soll oder nicht.                                                                                                                                                                                                                                                                                                                                                            |
| Eingebettetes Steuerelement           | Die Anwendung kann die Nachricht an ein eingebettetes Steuerelement senden, das den Fokus besitzt, und den Rückgabecode überprüfen, um festzustellen, ob das Steuerelement es behandelt hat. Wenn das Steuerelement es nicht behandelt hat, sollte die Anwendung im Dokument Fenster einen Bildlauf durchführen. Wenn der Benutzer z. b. auf ein Listenfeld geklickt hat und dann das Mausrad aufführt, würde dieses Steuerelement als Reaktion auf eine Rad Drehung scrollen. Wenn der Benutzer auf ein Textfeld geklickt und dann das Rad gedreht hat, würde das gesamte Dokument einen Bildlauf durchführen. |



 

Im folgenden Beispiel wird gezeigt, wie eine Anwendung die zwei radnachrichten verarbeiten kann.


```
/************************************************
* this code deals with MSH_MOUSEWHEEL
*************************************************/
#include "zmouse.h"

//
// Mouse Wheel rotation stuff, only define if we are
// on a version of the OS that does not support
// WM_MOUSEWHEEL messages.
//
#ifndef WM_MOUSEWHEEL
#define WM_MOUSEWHEEL WM_MOUSELAST+1 
    // Message ID for IntelliMouse wheel
#endif

UINT uMSH_MOUSEWHEEL = 0;   // Value returned from
                            // RegisterWindowMessage()

/**************************************************

INT WINAPI WinMain(
         HINSTANCE hInst, 
         HINSTANCE hPrevInst, 
         LPSTR lpCmdLine, 
         INT nCmdShow)
{
    MSG msg;
    BOOL bRet;

    if (!InitInstance(hInst, nCmdShow))
        return FALSE;

    //
    // The new IntelliMouse uses a Registered message to transmit
    // wheel rotation info. So register for it!
 
    uMSH_MOUSEWHEEL =
     RegisterWindowMessage(MSH_MOUSEWHEEL); 
    if ( !uMSH_MOUSEWHEEL )
    {
        MessageBox(NULL,"
                   RegisterWindowMessag Failed!",
                   "Error",MB_OK);
        return msg.wParam;
    }
    
    while (( bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            if (!TranslateAccelerator(ghwndApp,
                                      ghaccelTable,
                                      &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }

    return msg.wParam;
}

/************************************************
* this code deals with WM_MOUSEWHEEL
*************************************************/
LONG APIENTRY MainWndProc(
    HWND hwnd,
    UINT msg,
    WPARAM wParam,
    LPARAM lParam)
{
    static int nZoom = 0;
    

    switch (msg)
    {
        //
        // Handle Mouse Wheel messages generated
        // by the operating systems that have built-in
        // support for the WM_MOUSEWHEEL message.
        //

        case WM_MOUSEWHEEL:
            ((short) HIWORD(wParam)< 0) ? nZoom-- : nZoom++;

            //
            // Do other wheel stuff...
            //

            break;

        default:
            //
            // uMSH_MOUSEWHEEL is a message registered by
            // the mswheel dll on versions of Windows that
            // do not support the new message in the OS.

            if( msg == uMSH_MOUSEWHEEL )
            {
               ((int)wParam < 0) ? nZoom-- : nZoom++;

                //
                // Do other wheel stuff...
                //
                break;
            }

            return DefWindowProc(hwnd,
                                 msg,
                                 wParam,
                                 lParam);
    }

    return 0L;
}
```



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a>Abrufen der Anzahl von Mausrad-scrolllinien

Der folgende Code ermöglicht es einer Anwendung, die Anzahl der scrollzeilen mithilfe der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion abzurufen.


```
#ifndef SPI_GETWHEELSCROLLLINES
#define SPI_GETWHEELSCROLLLINES   104
#endif

#include "zmouse.h"

/*********************************************************
* FUNCTION: GetNumScrollLines
* Purpose : An OS independent method to retrieve the 
*           number of wheel scroll lines
* Params  : none
* Returns : UINT:  Number of scroll lines where WHEEL_PAGESCROLL 
*           indicates to scroll a page at a time.
*********************************************************/
UINT GetNumScrollLines(void)
{
   HWND hdlMsWheel;
   UINT ucNumLines=3;  // 3 is the default
   OSVERSIONINFO osversion;
   UINT uiMsh_MsgScrollLines;
   

   memset(&osversion, 0, sizeof(osversion));
   osversion.dwOSVersionInfoSize =sizeof(osversion);
   GetVersionEx(&osversion);

   if ((osversion.dwPlatformId == VER_PLATFORM_WIN32_WINDOWS) ||
       ( (osversion.dwPlatformId == VER_PLATFORM_WIN32_NT) && 
         (osversion.dwMajorVersion < 4) )   )
   {
        hdlMsWheel = FindWindow(MSH_WHEELMODULE_CLASS, 
                                MSH_WHEELMODULE_TITLE);
        if (hdlMsWheel)
        {
           uiMsh_MsgScrollLines = RegisterWindowMessage
                                     (MSH_SCROLL_LINES);
           if (uiMsh_MsgScrollLines)
                ucNumLines = (int)SendMessage(hdlMsWheel,
                                    uiMsh_MsgScrollLines, 
                                                       0, 
                                                       0);
        }
   }
   else if ( (osversion.dwPlatformId ==
                         VER_PLATFORM_WIN32_NT) &&
             (osversion.dwMajorVersion >= 4) )
   {
      SystemParametersInfo(SPI_GETWHEELSCROLLLINES,
                                          0,
                                    &ucNumLines, 0);
   }
   return(ucNumLines);
}
```



 

 