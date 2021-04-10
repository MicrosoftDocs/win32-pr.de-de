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
# <a name="how-to-scroll-text"></a><span data-ttu-id="83e9a-103">Vorgehensweise beim Scrollen von Text</span><span class="sxs-lookup"><span data-stu-id="83e9a-103">How to Scroll Text</span></span>

<span data-ttu-id="83e9a-104">In diesem Abschnitt werden die Änderungen beschrieben, die Sie an der Hauptfenster Prozedur einer Anwendung vornehmen können, damit ein Benutzer einen Bildlauf durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="83e9a-104">This section describes the changes you can make to an application's main window procedure to enable a user to scroll text.</span></span> <span data-ttu-id="83e9a-105">Im Beispiel in diesem Abschnitt wird ein Array von Text Zeichenfolgen erstellt und angezeigt. Außerdem werden die Bild Lauf leisten Meldungen [**WM \_ HScroll**](wm-hscroll.md) und [**WM \_ VScroll**](wm-vscroll.md) verarbeitet, sodass der Benutzer sowohl vertikal als auch horizontal einen Bildlauf durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="83e9a-105">The example in this section creates and displays an array of text strings, and processes [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) scroll bar messages so that the user can scroll text both vertically and horizontally.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="83e9a-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="83e9a-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="83e9a-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="83e9a-107">Technologies</span></span>

-   [<span data-ttu-id="83e9a-108">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="83e9a-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="83e9a-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="83e9a-109">Prerequisites</span></span>

-   <span data-ttu-id="83e9a-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="83e9a-110">C/C++</span></span>
-   <span data-ttu-id="83e9a-111">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="83e9a-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="83e9a-112">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="83e9a-112">Instructions</span></span>

### <a name="processing-the-wm_create-message"></a><span data-ttu-id="83e9a-113">Verarbeiten der WM \_ Create-Nachricht</span><span class="sxs-lookup"><span data-stu-id="83e9a-113">Processing the WM\_CREATE Message</span></span>

<span data-ttu-id="83e9a-114">Scrolleinheiten werden in der Regel beim Verarbeiten der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="83e9a-114">Scrolling units are typically set while processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="83e9a-115">Es ist praktisch, die scrolleinheiten auf den Dimensionen der Schriftart zu basieren, die dem Gerätekontext (DC) des Fensters zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83e9a-115">It is convenient to base the scrolling units on the dimensions of the font associated with the window's device context (DC).</span></span> <span data-ttu-id="83e9a-116">Verwenden Sie die [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) -Funktion, um die Schriftart Dimensionen für einen bestimmten Domänen Controller abzurufen.</span><span class="sxs-lookup"><span data-stu-id="83e9a-116">To retrieve the font dimensions for a specific DC, use the [**GetTextMetrics**](/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics) function.</span></span>

<span data-ttu-id="83e9a-117">Im Beispiel in diesem Abschnitt ist eine vertikale scrolleinheit mit der Höhe einer Zeichen Zelle Plus externer führenden identisch.</span><span class="sxs-lookup"><span data-stu-id="83e9a-117">In the example in this section, one vertical scrolling unit is equivalent to the height of a character cell, plus external leading.</span></span> <span data-ttu-id="83e9a-118">Eine horizontale scrolleinheit entspricht der durchschnittlichen Breite einer Zeichen Zelle.</span><span class="sxs-lookup"><span data-stu-id="83e9a-118">One horizontal scrolling unit is equivalent to the average width of a character cell.</span></span> <span data-ttu-id="83e9a-119">Die horizontalen scrollpositionen entsprechen daher nicht den tatsächlichen Zeichen, es sei denn, die Bildschirm Schriftart ist mit fester Breite versehen.</span><span class="sxs-lookup"><span data-stu-id="83e9a-119">The horizontal scrolling positions, therefore, do not correspond to actual characters, unless the screen font is fixed-width.</span></span>

### <a name="processing-the-wm_size-message"></a><span data-ttu-id="83e9a-120">Verarbeiten der WM- \_ Größen Meldung</span><span class="sxs-lookup"><span data-stu-id="83e9a-120">Processing the WM\_SIZE Message</span></span>

<span data-ttu-id="83e9a-121">Bei der Verarbeitung der [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht ist es praktisch, den scrollbereich und die Bild Lauf Position entsprechend der Abmessungen des Client Bereichs und der Anzahl der angezeigten Textzeilen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="83e9a-121">When processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, it is convenient to adjust the scrolling range and scrolling position to reflect the dimensions of the client area as well as the number of lines of text that will be displayed.</span></span>

<span data-ttu-id="83e9a-122">Die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion legt die minimalen und maximalen Positionswerte, die Seitengröße und die Scrollposition für eine Schiebe Leiste fest.</span><span class="sxs-lookup"><span data-stu-id="83e9a-122">The [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function sets the minimum and maximum position values, the page size, and the scrolling position for a scroll bar.</span></span>

### <a name="processing-the-wm_hscroll-and-wm_vscroll-messages"></a><span data-ttu-id="83e9a-123">Verarbeiten der \_ Nachrichten "WM HScroll" und "WM \_ VScroll"</span><span class="sxs-lookup"><span data-stu-id="83e9a-123">Processing the WM\_HSCROLL and WM\_VSCROLL Messages</span></span>

<span data-ttu-id="83e9a-124">Die Bild Lauf Leiste sendet [**WM \_ HScroll**](wm-hscroll.md) -und [**WM- \_ VScroll**](wm-vscroll.md) -Nachrichten an die Fenster Prozedur, wenn der Benutzer auf die Bild Lauf Leiste klickt oder das Bild Lauf Feld zieht.</span><span class="sxs-lookup"><span data-stu-id="83e9a-124">The scroll bar sends [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to the window procedure whenever the user clicks the scroll bar or drags the scroll box.</span></span> <span data-ttu-id="83e9a-125">Die nieder wertigen Wörter von **WM \_ VScroll** und **WM \_ HScroll** enthalten einen Anforderungs Code, der die Richtung und die Größe der scrollaktion angibt.</span><span class="sxs-lookup"><span data-stu-id="83e9a-125">The low-order words of **WM\_VSCROLL** and **WM\_HSCROLL** each contain a request code that indicates the direction and magnitude of the scrolling action.</span></span>

<span data-ttu-id="83e9a-126">Wenn die " [**WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Nachrichten verarbeitet werden, wird der Anforderungs Code der Scrollleiste überprüft, und das scrollinkrement wird berechnet.</span><span class="sxs-lookup"><span data-stu-id="83e9a-126">When the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages are processed, the scroll bar request code is examined and the scrolling increment is calculated.</span></span> <span data-ttu-id="83e9a-127">Nachdem das Inkrement auf die aktuelle Scrollposition angewendet wurde, wird das Fenster mithilfe der [**scrollwindowex**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) -Funktion an die neue Position gescrollt, und die Position des Bild Lauf Felds wird mithilfe der [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion angepasst.</span><span class="sxs-lookup"><span data-stu-id="83e9a-127">After the increment is applied to the current scrolling position, the window is scrolled to the new position by using the [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) function, and the position of the scroll box is adjusted by using the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span>

<span data-ttu-id="83e9a-128">Nachdem ein Fenster einen Rollup ausgeführt hat, wird ein Teil des Client Bereichs als ungültig festgestellt.</span><span class="sxs-lookup"><span data-stu-id="83e9a-128">After a window is scrolled, part of its client area is made invalid.</span></span> <span data-ttu-id="83e9a-129">Um sicherzustellen, dass die ungültige Region aktualisiert wird, wird die [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) -Funktion verwendet, um eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="83e9a-129">To ensure that the invalid region is updated, the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function is used to generate a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

### <a name="processing-the-wm_paint-message"></a><span data-ttu-id="83e9a-130">Die WM-Zeichnungs Nachricht wird verarbeitet. \_</span><span class="sxs-lookup"><span data-stu-id="83e9a-130">Processing the WM\_PAINT Message</span></span>

<span data-ttu-id="83e9a-131">Beim Verarbeiten der [**WM \_**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht ist es praktisch, die Textzeilen zu zeichnen, die im ungültigen Teil des Fensters angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83e9a-131">When processing the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, it is convenient to draw the lines of text that you want to appear in the invalid portion of the window.</span></span> <span data-ttu-id="83e9a-132">Im folgenden Beispiel wird die aktuelle Scrollposition und die Dimensionen des ungültigen Bereichs verwendet, um den Bereich der Zeilen innerhalb des ungültigen Bereichs zu bestimmen, um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83e9a-132">The following example uses the current scrolling position and the dimensions of the invalid region to determine the range of lines within the invalid region in order to display them.</span></span>

## <a name="example-of-scrolling-text"></a><span data-ttu-id="83e9a-133">Beispiel für Scrolltext</span><span class="sxs-lookup"><span data-stu-id="83e9a-133">Example of Scrolling Text</span></span>

<span data-ttu-id="83e9a-134">Das folgende Beispiel zeigt eine Fenster Prozedur für ein Fenster, in dem Text im Client Bereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83e9a-134">The following example is a window procedure for a window that displays text in its client area.</span></span> <span data-ttu-id="83e9a-135">Im Beispiel wird veranschaulicht, wie der Text als Reaktion auf Eingaben von den horizontalen und vertikalen Schiebe leisten durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="83e9a-135">The example demonstrates how to scroll the text in response to input from the horizontal and vertical scroll bars.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="83e9a-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83e9a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83e9a-137">Verwenden von Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="83e9a-137">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="83e9a-138">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="83e9a-138">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 