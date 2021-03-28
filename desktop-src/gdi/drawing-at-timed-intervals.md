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
# <a name="drawing-at-timed-intervals"></a>Zeichnen in zeitgesteuerten Intervallen

Sie können in zeitgesteuerten Intervallen zeichnen, indem Sie einen Timer [**mit der Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) "-Funktion" erstellen. Durch die Verwendung eines Timers zum Senden von WM-Zeit Geber Nachrichten an die Fenster Prozedur in regelmäßigen Abständen kann eine Anwendung im Client Bereich eine einfache Animation ausführen, während andere Anwendungen weiterhin ausgeführt werden. [**\_**](../winmsg/wm-timer.md)

Im folgenden Beispiel springt die Anwendung einen Stern von der Seite zu Seite im Client Bereich. Jedes Mal, wenn die Fenster Prozedur [**eine \_ WM**](../winmsg/wm-timer.md) -Zeit Geber Nachricht empfängt, löscht die Prozedur den Stern an der aktuellen Position, berechnet eine neue Position und zeichnet den Stern innerhalb der neuen Position. Die Prozedur startet den Zeitgeber, indem er bei der Verarbeitung der [**WM \_**](../winmsg/wm-create.md) -Erstellungs Nachricht [**den Aufruf von**](/windows/win32/api/winuser/nf-winuser-settimer) "*


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



Diese Anwendung verwendet einen privaten Gerätekontext, um den Zeitaufwand für die Vorbereitung des Geräte Kontexts für das Zeichnen zu minimieren. Die Fenster Prozedur ruft den privaten Gerätekontext bei der Verarbeitung der [**WM \_ Create**](../winmsg/wm-create.md) -Nachricht ab und initialisiert diesen, wobei der Modus für binäre Raster Vorgänge festgelegt wird, um zuzulassen, dass der Stern mithilfe desselben Aufrufens der [**polylinienfunktion**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) gelöscht und gezeichnet werden kann. Die Fenster Prozedur legt auch den Ansichts Port fest, um zuzulassen, dass der Stern mit demselben Satz von Punkten gezeichnet wird, unabhängig von der Position des Sterns im Client Bereich.

Die Anwendung verwendet die [**WM \_**](wm-paint.md) -Zeichnungs Nachricht, um den Stern zu zeichnen, wenn das Fenster aktualisiert werden muss. Die Fenster Prozedur zeichnet den Stern nur, wenn er nicht sichtbar ist. Dies ist nur der Fall, wenn er von der [**WM- \_ Lösch**](../winmsg/wm-erasebkgnd.md) Nachricht gelöscht wurde. Die Fenster Prozedur fängt die **WM- \_ erasebkgnd** -Meldung ab, um die *fVisible* -Variable festzulegen, übergibt die Nachricht jedoch an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , damit das System den Hintergrund des Fensters zeichnen kann.

Die Anwendung verwendet die [**WM- \_ Größen**](../winmsg/wm-size.md) Nachricht, um den Timer zu beenden, wenn das Fenster minimiert wird, und den Timer neu zu starten, wenn das minimierte Fenster wieder hergestellt wird. Die Fenster Prozedur verwendet auch die-Meldung, um die aktuelle Position des Sterns zu aktualisieren, wenn die Größe des Fensters reduziert wurde, sodass sich der Stern nicht mehr im Client Bereich befindet. Die Anwendung verfolgt die aktuelle Position des Sterns mithilfe der von rccurrent angegebenen Struktur, die das umgebende Rechteck für den Stern definiert. Wenn alle Ecken des Rechtecks im Client Bereich aufbewahrt werden, bleibt der Stern im Bereich. Bei der Verarbeitung der [**WM \_ Create**](../winmsg/wm-create.md) -Nachricht zentriert die Fenster Prozedur zunächst den Stern im Client Bereich.

 

 
