---
title: Vorgehensweise beim Scrollen von Text
description: In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfenster Prozedur einer Anwendung vornehmen können, damit ein Benutzer einen Bildlauf durchführen kann.
ms.assetid: ACB4FF34-38EF-4F3D-9395-D48D58A72C0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ef9a2eea9490beac7b6ff5048b70de61eb635f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858481"
---
# <a name="how-to-scroll-text"></a>Vorgehensweise beim Scrollen von Text

In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfenster Prozedur einer Anwendung vornehmen können, damit ein Benutzer einen Bildlauf durchführen kann. Im Beispiel in diesem Abschnitt wird ein Array von Text Zeichenfolgen erstellt und angezeigt. Außerdem werden die Bild Lauf leisten Meldungen [**WM \_ HScroll**](wm-hscroll.md) und [**WM \_ VScroll**](wm-vscroll.md) verarbeitet, sodass der Benutzer sowohl vertikal als auch horizontal einen Bildlauf durchführen kann.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="processing-the-wm_create-message"></a>Verarbeiten der WM \_ Create-Nachricht

Scrolleinheiten werden in der Regel beim Verarbeiten der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht festgelegt. Es ist praktisch, die scrolleinheiten auf den Dimensionen der Schriftart zu basieren, die dem Gerätekontext (DC) des Fensters zugeordnet ist. Verwenden Sie die [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) -Funktion, um die Schriftart Dimensionen für einen bestimmten Domänen Controller abzurufen.

Im Beispiel in diesem Abschnitt ist eine vertikale scrolleinheit mit der Höhe einer Zeichen Zelle Plus externer führenden identisch. Eine horizontale scrolleinheit entspricht der durchschnittlichen Breite einer Zeichen Zelle. Die horizontalen scrollpositionen entsprechen daher nicht den tatsächlichen Zeichen, es sei denn, die Bildschirm Schriftart ist mit fester Breite versehen.

### <a name="processing-the-wm_size-message"></a>Verarbeiten der WM- \_ Größen Meldung

Bei der Verarbeitung der [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht ist es praktisch, den scrollbereich und die Bild Lauf Position entsprechend der Abmessungen des Client Bereichs und der Anzahl der angezeigten Textzeilen anzupassen.

Die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion legt die minimalen und maximalen Positionswerte, die Seitengröße und die Scrollposition für eine Schiebe Leiste fest.

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a>Verarbeiten der \_ Nachrichten "WM HScroll" und "WM \_ VScroll"

Die Bild Lauf Leiste sendet [**WM \_ HScroll**](wm-hscroll.md) -und [**WM- \_ VScroll**](wm-vscroll.md) -Nachrichten an die Fenster Prozedur, wenn der Benutzer auf die Bild Lauf Leiste klickt oder das Bild Lauf Feld zieht. Die nieder wertigen Wörter von **WM \_ VScroll** und **WM \_ HScroll** enthalten einen Anforderungs Code, der die Richtung und die Größe der scrollaktion angibt.

Wenn die " [**WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Nachrichten verarbeitet werden, wird der Anforderungs Code der Scrollleiste überprüft, und das scrollinkrement wird berechnet. Nachdem das Inkrement auf die aktuelle Scrollposition angewendet wurde, wird das Fenster mithilfe der [**scrollwindowex**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) -Funktion an die neue Position gescrollt, und die Position des Bild Lauf Felds wird mithilfe der [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion angepasst.

Nachdem ein Fenster einen Rollup ausgeführt hat, wird ein Teil des Client Bereichs als ungültig festgestellt. Um sicherzustellen, dass die ungültige Region aktualisiert wird, wird die [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) -Funktion verwendet, um eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung zu generieren.

### <a name="processing-the-wm_paint-message"></a>Die WM-Zeichnungs Nachricht wird verarbeitet. \_

Beim Verarbeiten der [**WM \_**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht ist es praktisch, die Textzeilen zu zeichnen, die im ungültigen Teil des Fensters angezeigt werden sollen. Im folgenden Beispiel wird die aktuelle Scrollposition und die Dimensionen des ungültigen Bereichs verwendet, um den Bereich der Zeilen innerhalb des ungültigen Bereichs zu bestimmen, um Sie anzuzeigen.

## <a name="example-of-scrolling-text"></a>Beispiel für Scrolltext

Das folgende Beispiel zeigt eine Fenster Prozedur für ein Fenster, in dem Text im Client Bereich angezeigt wird. Im Beispiel wird veranschaulicht, wie der Text als Reaktion auf Eingaben von den horizontalen und vertikalen Schiebe leisten durchlaufen wird.


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

[Verwenden von Scrollleisten](using-scroll-bars.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 