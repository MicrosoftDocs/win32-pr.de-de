---
title: Scrollen von Text
description: In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfensterprozedur einer Anwendung vornehmen können, um einem Benutzer das Scrollen von Text zu ermöglichen.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2139ac1bff3d197d63011e6a6e76c861b984c5e20b5c54ceab8871678d31a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914220"
---
# <a name="how-to-scroll-text"></a>Scrollen von Text

In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfensterprozedur einer Anwendung vornehmen können, um einem Benutzer das Scrollen von Text zu ermöglichen. Im Beispiel in diesem Abschnitt wird ein Array von Textzeichenfolgen erstellt und angezeigt, und WM [**\_ HSCROLL-**](wm-hscroll.md) und [**WM \_ VSCROLL-Scrollleistenmeldungen**](wm-vscroll.md) werden verarbeitet, sodass der Benutzer text vertikal und horizontal scrollen kann.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="processing-the-wm_create-message"></a>Verarbeiten der WM \_ CREATE-Nachricht

Bildlaufeinheiten werden in der Regel während der Verarbeitung der [**WM \_ CREATE-Nachricht**](/windows/desktop/winmsg/wm-create) festgelegt. Es ist praktisch, die Bildlaufeinheiten auf den Abmessungen der Schriftart zu basieren, die dem Gerätekontext (DC) des Fensters zugeordnet ist. Verwenden Sie die [**GetTextMetrics-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) um die Schriftdimensionen für einen bestimmten Domänencontroller abzurufen.

Im Beispiel in diesem Abschnitt entspricht eine vertikale Bildlaufeinheit der Höhe einer Zeichenzelle plus externer führendem Zeichen. Eine horizontale Bildlaufeinheit entspricht der durchschnittlichen Breite einer Zeichenzelle. Die horizontalen Bildlaufpositionen entsprechen daher nicht den tatsächlichen Zeichen, es sei denn, die Bildschirmschriftart hat eine feste Breite.

### <a name="processing-the-wm_size-message"></a>Verarbeiten der WM \_ SIZE-Nachricht

Bei der Verarbeitung der [**WM \_ SIZE-Nachricht**](/windows/desktop/winmsg/wm-size) ist es praktisch, den Bildlaufbereich und die Bildlaufposition so anzupassen, dass die Abmessungen des Clientbereichs sowie die Anzahl der angezeigten Textzeilen widergespiegelt werden.

Die [**SetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) legt die Minimal- und Höchstpositionswerte, die Seitengröße und die Bildlaufposition für eine Bildlaufleiste fest.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Verarbeiten der WM \_ HSCROLL- und WM \_ VSCROLL-Nachrichten

Die Scrollleiste sendet [**WM \_ HSCROLL-**](wm-hscroll.md) und [**WM \_ VSCROLL-Meldungen**](wm-vscroll.md) an die Fensterprozedur, wenn der Benutzer auf die Scrollleiste klickt oder das Scrollfeld zieht. Die Wörter in niedriger Reihenfolge von **WM \_ VSCROLL** und **WM \_ HSCROLL** enthalten jeweils einen Anforderungscode, der die Richtung und Größe der Scrollaktion angibt.

Wenn die [**WM \_ HSCROLL-**](wm-hscroll.md) und [**WM \_ VSCROLL-Nachrichten**](wm-vscroll.md) verarbeitet werden, wird der Anforderungscode der Scrollleiste untersucht und das Scrollinkrement berechnet. Nachdem das Inkrement auf die aktuelle Bildlaufposition angewendet wurde, wird das Fenster mithilfe der [**ScrollWindowEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) zur neuen Position gescrollt, und die Position des Bildlauffelds wird mithilfe der [**SetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) angepasst.

Nachdem ein Fenster gescrollt wurde, wird ein Teil des Clientbereichs ungültig. Um sicherzustellen, dass die ungültige Region aktualisiert wird, wird die [**UpdateWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-updatewindow) verwendet, um eine [**WM \_ PAINT-Meldung**](/windows/desktop/gdi/wm-paint) zu generieren.

### <a name="processing-the-wm_paint-message"></a>Verarbeiten der \_ WM-PAINT-Nachricht

Bei der Verarbeitung der [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) ist es praktisch, die Textzeilen zu zeichnen, die im ungültigen Teil des Fensters angezeigt werden sollen. Im folgenden Beispiel werden die aktuelle Bildlaufposition und die Abmessungen des ungültigen Bereichs verwendet, um den Zeilenbereich innerhalb des ungültigen Bereichs zu bestimmen, um sie anzuzeigen.

## <a name="example-of-scrolling-text"></a>Beispiel für das Scrollen von Text

Das folgende Beispiel ist eine Fensterprozedur für ein Fenster, das Text im Clientbereich anzeigt. Im Beispiel wird veranschaulicht, wie der Text als Reaktion auf Eingaben von den horizontalen und vertikalen Bildlaufleisten gescrollt wird.


```C++
#include "strsafe.h"

LRESULT CALLBACK MyTextWindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
HDC hdc; 
PAINTSTRUCT ps; 
TEXTMETRIC tm; 
SCROLLINFO si; 
 
// These variables are required to display text. 
static int xClient;     // width of client area 
static int yClient;     // height of client area 
static int xClientMax;  // maximum width of client area 
 
static int xChar;       // horizontal scrolling unit 
static int yChar;       // vertical scrolling unit 
static int xUpper;      // average width of uppercase letters 
 
static int xPos;        // current horizontal scrolling position 
static int yPos;        // current vertical scrolling position 
 
int i;                  // loop counter 
int x, y;               // horizontal and vertical coordinates
 
int FirstLine;          // first line in the invalidated area 
int LastLine;           // last line in the invalidated area 
HRESULT hr;
size_t abcLength;        // length of an abc[] item 

// Create an array of lines to display. 
#define LINES 28 
static TCHAR *abc[] = { 
       TEXT("anteater"),  TEXT("bear"),      TEXT("cougar"), 
       TEXT("dingo"),     TEXT("elephant"),  TEXT("falcon"), 
       TEXT("gazelle"),   TEXT("hyena"),     TEXT("iguana"), 
       TEXT("jackal"),    TEXT("kangaroo"),  TEXT("llama"), 
       TEXT("moose"),     TEXT("newt"),      TEXT("octopus"), 
       TEXT("penguin"),   TEXT("quail"),     TEXT("rat"), 
       TEXT("squid"),     TEXT("tortoise"),  TEXT("urus"), 
       TEXT("vole"),      TEXT("walrus"),    TEXT("xylophone"), 
       TEXT("yak"),       TEXT("zebra"),
       TEXT("This line contains words, but no character. Go figure."),
       TEXT("")
     }; 
 
switch (uMsg) 
{ 
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hwnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hwnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0; 
 
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hwnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hwnd, SB_HORZ, &si, TRUE); 
 
        return 0; 
    case WM_HSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;

        // Save the position for comparison later on.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;
        switch (LOWORD (wParam))
        {
        // User clicked the left arrow.
        case SB_LINELEFT: 
            si.nPos -= 1;
            break;
              
        // User clicked the right arrow.
        case SB_LINERIGHT: 
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft left of the scroll box.
        case SB_PAGELEFT:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft right of the scroll box.
        case SB_PAGERIGHT:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK: 
            si.nPos = si.nTrackPos;
            break;
              
        default :
            break;
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_HORZ, &si, TRUE);
        GetScrollInfo (hwnd, SB_HORZ, &si);
         
        // If the position has changed, scroll the window.
        if (si.nPos != xPos)
        {
            ScrollWindow(hwnd, xChar * (xPos - si.nPos), 0, NULL, NULL);
        }

        return 0;
         
    case WM_VSCROLL:
        // Get all the vertial scroll bar information.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hwnd, SB_VERT, &si);

        // Save the position for comparison later on.
        yPos = si.nPos;
        switch (LOWORD (wParam))
        {

        // User clicked the HOME keyboard key.
        case SB_TOP:
            si.nPos = si.nMin;
            break;
              
        // User clicked the END keyboard key.
        case SB_BOTTOM:
            si.nPos = si.nMax;
            break;
              
        // User clicked the top arrow.
        case SB_LINEUP:
            si.nPos -= 1;
            break;
              
        // User clicked the bottom arrow.
        case SB_LINEDOWN:
            si.nPos += 1;
            break;
              
        // User clicked the scroll bar shaft above the scroll box.
        case SB_PAGEUP:
            si.nPos -= si.nPage;
            break;
              
        // User clicked the scroll bar shaft below the scroll box.
        case SB_PAGEDOWN:
            si.nPos += si.nPage;
            break;
              
        // User dragged the scroll box.
        case SB_THUMBTRACK:
            si.nPos = si.nTrackPos;
            break;
              
        default:
            break; 
        }

        // Set the position and then retrieve it.  Due to adjustments
        // by Windows it may not be the same as the value set.
        si.fMask = SIF_POS;
        SetScrollInfo (hwnd, SB_VERT, &si, TRUE);
        GetScrollInfo (hwnd, SB_VERT, &si);

        // If the position has changed, scroll window and update it.
        if (si.nPos != yPos)
        {                    
            ScrollWindow(hwnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
            UpdateWindow (hwnd);
        }

        return 0;
         
    case WM_PAINT :
        // Prepare the window for painting.
        hdc = BeginPaint (hwnd, &ps);

        // Get vertical scroll bar position.
        si.cbSize = sizeof (si);
        si.fMask  = SIF_POS;
        GetScrollInfo (hwnd, SB_VERT, &si);
        yPos = si.nPos;

        // Get horizontal scroll bar position.
        GetScrollInfo (hwnd, SB_HORZ, &si);
        xPos = si.nPos;

        // Find painting limits.
        FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
        LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
        for (i = FirstLine; i <= LastLine; i++)
        {
            x = xChar * (1 - xPos);
            y = yChar * (i - yPos);
              
            // Note that "55" in the following depends on the 
            // maximum size of an abc[] item. Also, you must include
            // strsafe.h to use the StringCchLength function.
            hr = StringCchLength(abc[i], 55, &abcLength);
            if ((FAILED(hr))|(abcLength == NULL))
            {
                //
                // TODO: write error handler
                //
            }

            // Write a line of text to the client area.
            TextOut(hdc, x, y, abc[i], abcLength); 
        }

        // Indicate that painting is finished.
        EndPaint (hwnd, &ps);
        return 0;
         
    case WM_DESTROY :
        PostQuitMessage (0);
        return 0;
    }

    return DefWindowProc (hwnd, uMsg, wParam, lParam);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Bildlaufleisten](using-scroll-bars.md)
</dt> <dt>

[Demo Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 