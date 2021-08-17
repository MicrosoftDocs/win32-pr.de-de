---
description: Sie können in Zeitintervallen zeichnen, indem Sie einen Timer mit der SetTimer-Funktion erstellen.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Zeichnen in zeitierten Intervallen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d82d385dce232c84be0dfeb8fd0f825891563ec64daa6c6cd41b82db81c6f67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887108"
---
# <a name="drawing-at-timed-intervals"></a>Zeichnen in zeitierten Intervallen

Sie können in Zeitintervallen zeichnen, indem Sie einen Timer mit der [**SetTimer-Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) erstellen. Durch die Verwendung eines Timers zum Senden von [**WM \_ TIMER-Nachrichten**](../winmsg/wm-timer.md) an die Fensterprozedur in regelmäßigen Abständen kann eine Anwendung einfache Animationen im Clientbereich ausführen, während andere Anwendungen weiterhin ausgeführt werden.

Im folgenden Beispiel springt die Anwendung einen Stern im Clientbereich von Seite zu Seite. Jedes Mal, wenn die Fensterprozedur eine [**WM \_ TIMER-Nachricht**](../winmsg/wm-timer.md) empfängt, löscht die Prozedur den Stern an der aktuellen Position, berechnet eine neue Position und zeichnet den Stern innerhalb der neuen Position. Die Prozedur startet den Timer durch Aufrufen [**von SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) während der Verarbeitung der [**WM \_ CREATE-Nachricht.**](../winmsg/wm-create.md)


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



Diese Anwendung verwendet einen privaten Gerätekontext, um die Zeit zu minimieren, die zum Vorbereiten des Gerätekontexts für das Zeichnen erforderlich ist. Die Fensterprozedur ruft beim Verarbeiten der [**WM \_ CREATE-Nachricht**](../winmsg/wm-create.md) den privaten Gerätekontext ab und initialisiert ihn. Dabei wird der Binärraster-Betriebsmodus so festgelegt, dass der Stern gelöscht und mit dem gleichen Aufruf der [**Polyline-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) gezeichnet werden kann. Die Fensterprozedur legt auch den Viewport-Ursprung fest, damit der Stern mit dem gleichen Satz von Punkten gezeichnet werden kann, unabhängig von der Sternposition im Clientbereich.

Die Anwendung verwendet die [**WM \_ PAINT-Nachricht,**](wm-paint.md) um den Stern zu zeichnen, wenn das Fenster aktualisiert werden muss. Die Fensterprozedur zeichnet den Stern nur, wenn er nicht sichtbar ist. das heißt, nur, wenn es durch die [**WM \_ ERASEBKGND-Nachricht gelöscht**](../winmsg/wm-erasebkgnd.md) wurde. Die Fensterprozedur fängt die **WM \_ ERASEBKGND-Nachricht** ab, um die *fVisible-Variable* zu festlegen, übergibt die Nachricht jedoch an [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) damit das System den Fensterhintergrund zeichnen kann.

Die Anwendung verwendet die [**WM \_ SIZE-Meldung,**](../winmsg/wm-size.md) um den Timer zu beenden, wenn das Fenster minimiert ist, und um den Timer neu zu starten, wenn das minimierte Fenster wiederhergestellt wird. Die Fensterprozedur verwendet auch die Meldung, um die aktuelle Position des Sterns zu aktualisieren, wenn die Größe des Fensters reduziert wurde, sodass sich der Stern nicht mehr im Clientbereich befindet. Die Anwendung verfolgt die aktuelle Position des Sterns mithilfe der durch rcCurrent angegebenen Struktur nach, die das umgebundene Rechteck für den Stern definiert. Wenn Sie alle Ecken des Rechtecks im Clientbereich behalten, bleibt der Stern im Bereich. Die Fensterprozedur centert den Stern zunächst im Clientbereich, wenn die [**WM \_ CREATE-Nachricht verarbeitet**](../winmsg/wm-create.md) wird.

 

 
