---
description: Sie können in zeitgesteuerten Intervallen zeichnen, indem Sie einen Timer mit der Funktion "-Funktion" erstellen.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Zeichnen in zeitgesteuerten Intervallen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757aca4e6be8f169aea378c52038420519ee879
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528358"
---
# <a name="drawing-at-timed-intervals"></a><span data-ttu-id="67656-103">Zeichnen in zeitgesteuerten Intervallen</span><span class="sxs-lookup"><span data-stu-id="67656-103">Drawing at Timed Intervals</span></span>

<span data-ttu-id="67656-104">Sie können in zeitgesteuerten Intervallen zeichnen, indem Sie einen Timer [**mit der Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) "-Funktion" erstellen.</span><span class="sxs-lookup"><span data-stu-id="67656-104">You can draw at timed intervals by creating a timer with the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function.</span></span> <span data-ttu-id="67656-105">Durch die Verwendung eines Timers zum Senden von WM-Zeit Geber Nachrichten an die Fenster Prozedur in regelmäßigen Abständen kann eine Anwendung im Client Bereich eine einfache Animation ausführen, während andere Anwendungen weiterhin ausgeführt werden. [**\_**](../winmsg/wm-timer.md)</span><span class="sxs-lookup"><span data-stu-id="67656-105">By using a timer to send [**WM\_TIMER**](../winmsg/wm-timer.md) messages to the window procedure at regular intervals, an application can carry out simple animation in the client area while other applications continue running.</span></span>

<span data-ttu-id="67656-106">Im folgenden Beispiel springt die Anwendung einen Stern von der Seite zu Seite im Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="67656-106">In the following example, the application bounces a star from side to side in the client area.</span></span> <span data-ttu-id="67656-107">Jedes Mal, wenn die Fenster Prozedur [**eine \_ WM**](../winmsg/wm-timer.md) -Zeit Geber Nachricht empfängt, löscht die Prozedur den Stern an der aktuellen Position, berechnet eine neue Position und zeichnet den Stern innerhalb der neuen Position.</span><span class="sxs-lookup"><span data-stu-id="67656-107">Each time the window procedure receives a [**WM\_TIMER**](../winmsg/wm-timer.md) message, the procedure erases the star at the current position, calculates a new position, and draws the star within the new position.</span></span> <span data-ttu-id="67656-108">Die Prozedur startet den Zeitgeber, indem er bei der Verarbeitung der [**WM \_**](../winmsg/wm-create.md) -Erstellungs Nachricht [**den Aufruf von**](/windows/win32/api/winuser/nf-winuser-settimer) "\*</span><span class="sxs-lookup"><span data-stu-id="67656-108">The procedure starts the timer by calling [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) while processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>


```C++
RECT rcCurrent = {0,0,20,20}; 
POINT aptStar[6] = {10,1, 1,19, 19,6, 1,6, 19,19, 10,1}; 
int X = 2, Y = -1, idTimer = -1; 
BOOL fVisible = FALSE; 
HDC hdc; 
 
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    RECT rc; 
 
    switch (message) 
    { 
        case WM_CREATE: 
 
            // Calculate the starting point.  
 
            GetClientRect(hwnd, &rc); 
            OffsetRect(&rcCurrent, rc.right / 2, rc.bottom / 2); 
 
            // Initialize the private DC.  
 
            hdc = GetDC(hwnd); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            SetROP2(hdc, R2_NOT); 
 
            // Start the timer.  
 
            SetTimer(hwnd, idTimer = 1, 10, NULL); 
            return 0L; 
 
        case WM_DESTROY: 
            KillTimer(hwnd, 1); 
            PostQuitMessage(0); 
            return 0L; 
 
        case WM_SIZE: 
            switch (wParam) 
            { 
                case SIZE_MINIMIZED: 
 
                    // Stop the timer if the window is minimized. 
 
                    KillTimer(hwnd, 1); 
                    idTimer = -1; 
                    break; 
 
                case SIZE_RESTORED: 
 
                    // Move the star back into the client area  
                    // if necessary.  
 
                    if (rcCurrent.right > (int) LOWORD(lParam)) 
                    {
                        rcCurrent.left = 
                            (rcCurrent.right = 
                                (int) LOWORD(lParam)) - 20; 
                    }
                    if (rcCurrent.bottom > (int) HIWORD(lParam)) 
                    {
                        rcCurrent.top = 
                            (rcCurrent.bottom = 
                                (int) HIWORD(lParam)) - 20; 
                    }
 
                    // Fall through to the next case.  
 
                case SIZE_MAXIMIZED: 
 
                    // Start the timer if it had been stopped.  
 
                    if (idTimer == -1) 
                        SetTimer(hwnd, idTimer = 1, 10, NULL); 
                    break; 
            } 
            return 0L; 
 
        case WM_TIMER: 
 
            // Hide the star if it is visible.  
 
            if (fVisible) 
                Polyline(hdc, aptStar, 6); 
 
            // Bounce the star off a side if necessary.  
 
            GetClientRect(hwnd, &rc); 
            if (rcCurrent.left + X < rc.left || 
                rcCurrent.right + X > rc.right) 
                X = -X; 
            if (rcCurrent.top + Y < rc.top || 
                rcCurrent.bottom + Y > rc.bottom) 
                Y = -Y; 
 
            // Show the star in its new position.  
 
            OffsetRect(&rcCurrent, X, Y); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            fVisible = Polyline(hdc, aptStar, 6); 
 
            return 0L; 
 
        case WM_ERASEBKGND: 
 
            // Erase the star.  
 
            fVisible = FALSE; 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
        case WM_PAINT: 
 
            // Show the star if it is not visible. Use BeginPaint  
            // to clear the update region.  
 
            BeginPaint(hwnd, &ps); 
            if (!fVisible) 
                fVisible = Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
    } 
    return DefWindowProc(hwnd, message, wParam, lParam); 
} 
```



<span data-ttu-id="67656-109">Diese Anwendung verwendet einen privaten Gerätekontext, um den Zeitaufwand für die Vorbereitung des Geräte Kontexts für das Zeichnen zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="67656-109">This application uses a private device context to minimize the time required to prepare the device context for drawing.</span></span> <span data-ttu-id="67656-110">Die Fenster Prozedur ruft den privaten Gerätekontext bei der Verarbeitung der [**WM \_ Create**](../winmsg/wm-create.md) -Nachricht ab und initialisiert diesen, wobei der Modus für binäre Raster Vorgänge festgelegt wird, um zuzulassen, dass der Stern mithilfe desselben Aufrufens der [**polylinienfunktion**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) gelöscht und gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="67656-110">The window procedure retrieves and initializes the private device context when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message, setting the binary raster operation mode to allow the star to be erased and drawn using the same call to the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function.</span></span> <span data-ttu-id="67656-111">Die Fenster Prozedur legt auch den Ansichts Port fest, um zuzulassen, dass der Stern mit demselben Satz von Punkten gezeichnet wird, unabhängig von der Position des Sterns im Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="67656-111">The window procedure also sets the viewport origin to allow the star to be drawn using the same set of points regardless of the star's position in the client area.</span></span>

<span data-ttu-id="67656-112">Die Anwendung verwendet die [**WM \_**](wm-paint.md) -Zeichnungs Nachricht, um den Stern zu zeichnen, wenn das Fenster aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="67656-112">The application uses the [**WM\_PAINT**](wm-paint.md) message to draw the star whenever the window must be updated.</span></span> <span data-ttu-id="67656-113">Die Fenster Prozedur zeichnet den Stern nur, wenn er nicht sichtbar ist. Dies ist nur der Fall, wenn er von der [**WM- \_ Lösch**](../winmsg/wm-erasebkgnd.md) Nachricht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="67656-113">The window procedure draws the star only if it is not visible; that is, only if it has been erased by the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message.</span></span> <span data-ttu-id="67656-114">Die Fenster Prozedur fängt die **WM- \_ erasebkgnd** -Meldung ab, um die *fVisible* -Variable festzulegen, übergibt die Nachricht jedoch an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , damit das System den Hintergrund des Fensters zeichnen kann.</span><span class="sxs-lookup"><span data-stu-id="67656-114">The window procedure intercepts the **WM\_ERASEBKGND** message to set the *fVisible* variable, but passes the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so that the system can draw the window background.</span></span>

<span data-ttu-id="67656-115">Die Anwendung verwendet die [**WM- \_ Größen**](../winmsg/wm-size.md) Nachricht, um den Timer zu beenden, wenn das Fenster minimiert wird, und den Timer neu zu starten, wenn das minimierte Fenster wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="67656-115">The application uses the [**WM\_SIZE**](../winmsg/wm-size.md) message to stop the timer when the window is minimized and to restart the timer when the minimized window is restored.</span></span> <span data-ttu-id="67656-116">Die Fenster Prozedur verwendet auch die-Meldung, um die aktuelle Position des Sterns zu aktualisieren, wenn die Größe des Fensters reduziert wurde, sodass sich der Stern nicht mehr im Client Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="67656-116">The window procedure also uses the message to update the current position of the star if the size of the window has been reduced so that the star is no longer in the client area.</span></span> <span data-ttu-id="67656-117">Die Anwendung verfolgt die aktuelle Position des Sterns mithilfe der von rccurrent angegebenen Struktur, die das umgebende Rechteck für den Stern definiert.</span><span class="sxs-lookup"><span data-stu-id="67656-117">The application keeps track of the star's current position by using the structure specified by rcCurrent, which defines the bounding rectangle for the star.</span></span> <span data-ttu-id="67656-118">Wenn alle Ecken des Rechtecks im Client Bereich aufbewahrt werden, bleibt der Stern im Bereich.</span><span class="sxs-lookup"><span data-stu-id="67656-118">Keeping all corners of the rectangle in the client area keeps the star in the area.</span></span> <span data-ttu-id="67656-119">Bei der Verarbeitung der [**WM \_ Create**](../winmsg/wm-create.md) -Nachricht zentriert die Fenster Prozedur zunächst den Stern im Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="67656-119">The window procedure initially centers the star in the client area when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>

 

 
