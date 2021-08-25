---
title: Verwenden der Mauseingabe
description: In diesem Abschnitt werden Aufgaben behandelt, die der Mauseingabe zugeordnet sind.
ms.assetid: b96d0046-a507-4733-bcf3-fcf757beec7f
keywords:
- Benutzereingabe, Mauseingabe
- Erfassen von Benutzereingaben, Mauseingabe
- Mauseingabe
- Cursor, Mauseingabe
- Mauszeiger
- Doppelklicken auf die Nachrichtenverarbeitung
- Mausrad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38105da1fbbe3bee1be9ca280f1f5573dbb41ba4b7b6aa2013d9c600b8ad00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829970"
---
# <a name="using-mouse-input"></a>Verwenden der Mauseingabe

In diesem Abschnitt werden Aufgaben behandelt, die der Mauseingabe zugeordnet sind.

-   [Nachverfolgen des Mauszeigers](#tracking-the-mouse-cursor)
-   [Zeichnen von Linien mit der Maus](#drawing-lines-with-the-mouse)
-   [Verarbeiten einer Doppelklicknachricht](#processing-a-double-click-message)
-   [Auswählen einer Textzeile](#selecting-a-line-of-text)
-   [Verwenden eines Mausrads in einem Dokument mit eingebetteten Objekten](#using-a-mouse-wheel-in-a-document-with-embedded-objects)
-   [Abrufen der Anzahl der Mausrad-Bildlauflinien](#retrieving-the-number-of-mouse-wheel-scroll-lines)

## <a name="tracking-the-mouse-cursor"></a>Nachverfolgen des Mauszeigers

Anwendungen führen häufig Aufgaben aus, bei denen die Position des Mauscursors nachverfolgt wird. Die meisten Zeichnungsanwendungen verfolgen beispielsweise die Position des Mauscursors während Zeichnungsvorgängen nach, sodass der Benutzer durch Ziehen der Maus in den Clientbereich eines Fensters zeichnen kann. Textverarbeitungsanwendungen verfolgen auch den Cursor nach, sodass der Benutzer ein Wort oder einen Textblock durch Klicken und Ziehen der Maus auswählen kann.

Die Nachverfolgung des Cursors umfasst in der Regel die Verarbeitung der [**\_ WM-Meldungen LBUTTONDOWN,**](wm-lbuttondown.md) [**WM \_ MOUSEMOVE**](wm-mousemove.md)und [**WM \_ LBUTTONUP.**](wm-lbuttonup.md) Ein Fenster bestimmt, wann mit der Nachverfolgung des Cursors begonnen werden soll, indem die Cursorposition überprüft wird, die im *lParam-Parameter* der **\_ WM-LBUTTONDOWN-Meldung angegeben** ist. Eine Textverarbeitungsanwendung würde z. B. nur dann mit der Nachverfolgung des Cursors beginnen, wenn die **\_ WM-LBUTTONDOWN-Meldung** aufgetreten ist, während sich der Cursor in einer Textzeile befindet, aber nicht, wenn er sich über das Ende des Dokuments hinaus befindet.

Ein Fenster verfolgt die Position des Cursors, indem der Stream von [**WM \_ MOUSEMOVE-Nachrichten**](wm-mousemove.md) verarbeitet wird, die während der Mausbewegung im Fenster angezeigt werden. Die Verarbeitung **der WM \_ MOUSEMOVE-Nachricht** umfasst in der Regel einen sich wiederholenden Zeichnungs- oder Zeichnungsvorgang im Clientbereich. Beispielsweise könnte eine Zeichnungsanwendung eine Linie wiederholt neu zeichnen, wenn sich die Maus bewegt. Ein Fenster verwendet die [**\_ WM-LBUTTONUP-Nachricht**](wm-lbuttonup.md) als Signal, um die Nachverfolgung des Cursors zu beenden.

Darüber hinaus kann eine Anwendung die [**TrackMouseEvent-Funktion**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) aufrufen, damit das System andere Nachrichten sendet, die für die Nachverfolgung des Cursors nützlich sind. Das System übermittelt die [**WM \_ MOUSEHOVER-Nachricht,**](wm-mousehover.md) wenn der Cursor für einen bestimmten Zeitraum über den Clientbereich bewegt wird. Es wird die [**WM \_ MOUSELEAVE-Nachricht**](wm-mouseleave.md) gesendet, wenn der Cursor den Clientbereich verlässt. Die [**WM \_ NCMOUSEHOVER-**](wm-ncmousehover.md) und [**WM \_ NCMOUSELEAVE-Nachrichten**](wm-ncmouseleave.md) sind die entsprechenden Nachrichten für die Nicht-Clientbereiche.

## <a name="drawing-lines-with-the-mouse"></a>Zeichnen von Linien mit der Maus

Im Beispiel in diesem Abschnitt wird veranschaulicht, wie der Mauszeiger nachverfolgt wird. Sie enthält Teile einer Fensterprozedur, mit denen der Benutzer Linien im Clientbereich eines Fensters zeichnen kann, indem er die Maus zieht.

Wenn die Fensterprozedur eine [**\_ WM-LBUTTONDOWN-Nachricht**](wm-lbuttondown.md) empfängt, erfasst sie die Maus und speichert die Koordinaten des Cursors unter Verwendung der Koordinaten als Ausgangspunkt der Linie. Außerdem wird die [**ClipCursor-Funktion**](/windows/desktop/api/winuser/nf-winuser-clipcursor) verwendet, um den Cursor während des Strichzeichnungsvorgang auf den Clientbereich zu beschränken.

Während der ersten [**WM \_ MOUSEMOVE-Meldung**](wm-mousemove.md) zeichnet die Fensterprozedur eine Linie vom Startpunkt bis zur aktuellen Position des Cursors. Bei **nachfolgenden WM \_ MOUSEMOVE-Meldungen** löscht die Fensterprozedur die vorherige Zeile, indem sie mit einer umgekehrten Stiftfarbe darüber gezeichnunget wird. Anschließend wird eine neue Zeile vom Anfangspunkt bis zur neuen Position des Cursors ge zeichnet.

Die [**\_ WM-LBUTTONUP-Meldung**](wm-lbuttonup.md) signalisiert das Ende des Zeichnungsvorgang. Die Fensterprozedur gibt die Mauserfassung und die Maus aus dem Clientbereich frei.


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



## <a name="processing-a-double-click-message"></a>Verarbeiten einer Doppelklicknachricht

Um Doppelklicknachrichten zu empfangen, muss ein Fenster zu einer Fensterklasse gehören, die den [**CS \_ DBLCLKS-Klassenstil**](/windows/desktop/winmsg/about-window-classes) hat. Sie legen diesen Stil beim Registrieren der Fensterklasse fest, wie im folgenden Beispiel gezeigt.


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



Einer Doppelklickmeldung wird immer eine Schaltflächen-nach-unten-Meldung vorangehende. Aus diesem Grund verwenden Anwendungen in der Regel eine Doppelklickmeldung, um eine Aufgabe zu erweitern, die während einer Schaltflächenabschaltfläche begonnen wurde.

## <a name="selecting-a-line-of-text"></a>Auswählen einer Textzeile

Das Beispiel in diesem Abschnitt ist eine einfache Anwendung zur Verarbeitung von Wörtern. Sie enthält Code, mit dem der Benutzer die Position des Caretstrichs festlegen kann, indem er auf eine beliebige Stelle in einer Textzeile klickt und eine Textzeile durch Doppelklicken an eine beliebige Stelle in der Zeile auswählt (hervorhebt).


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



## <a name="using-a-mouse-wheel-in-a-document-with-embedded-objects"></a>Verwenden eines Mausrads in einem Dokument mit eingebetteten Objekten

In diesem Beispiel wird von einem Microsoft Word mit verschiedenen eingebetteten Objekten ausgegangen:

-   Ein Microsoft Excel Arbeitsblatt
-   Ein eingebettetes Listenfeld-Steuerelement, das als Reaktion auf das Rad scrollt
-   Ein eingebettetes Textfeld-Steuerelement, das nicht auf das Rad reagiert

Die [MSH \_ MOUSEWHEEL-Meldung](about-mouse-input.md) wird immer an das Hauptfenster in der Microsoft Word. Dies gilt auch, wenn das eingebettete Arbeitsblatt aktiv ist. In der folgenden Tabelle wird erläutert, wie die MSH \_ MOUSEWHEEL-Nachricht entsprechend dem Fokus behandelt wird.



| Fokus liegt auf                | Die Behandlung ist wie folgt:                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Word-Dokument              | Word führt einen Bildlauf im Dokumentfenster durch.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Eingebettete Excel Tabelle | Word veröffentlicht die Nachricht an Excel. Sie müssen entscheiden, ob die eingebettete Anwendung auf die Nachricht reagieren soll oder nicht.                                                                                                                                                                                                                                                                                                                                                            |
| Eingebettetes Steuerelement           | Es liegt in der Hand der Anwendung, die Nachricht an ein eingebettetes Steuerelement zu senden, das den Fokus besitzt, und den Rückgabecode zu überprüfen, um zu überprüfen, ob es vom Steuerelement behandelt wurde. Wenn das Steuerelement dies nicht verarbeitet hat, sollte die Anwendung im Dokumentfenster scrollen. Wenn der Benutzer beispielsweise auf ein Listenfeld klickt und dann das Rad rollt, würde dieses Steuerelement als Reaktion auf eine Radrotation scrollen. Wenn der Benutzer auf ein Textfeld klickt und dann das Rad drehen würde, würde das gesamte Dokument scrollen. |



 

Das folgende Beispiel zeigt, wie eine Anwendung die zwei Radmeldungen behandeln kann.


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



## <a name="retrieving-the-number-of-mouse-wheel-scroll-lines"></a>Abrufen der Anzahl der Mausrad-Bildlauflinien

Mit dem folgenden Code kann eine Anwendung die Anzahl von Bildlauflinien mithilfe der [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) abrufen.


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



 

 