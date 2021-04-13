---
description: In diesem Thema wird gezeigt, wie Timer erstellt und zerstört werden und wie ein Timer verwendet wird, um Maus Eingaben in angegebenen Intervallen abzufangen.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Verwenden von Timern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c6479aca9d5394c2ad9ade87dd77b1474f31f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348179"
---
# <a name="using-timers"></a>Verwenden von Timern

In diesem Thema wird gezeigt, wie Timer erstellt und zerstört werden und wie ein Timer verwendet wird, um Maus Eingaben in angegebenen Intervallen abzufangen.

Dieses Thema enthält folgende Abschnitte:

-   [Erstellen eines Timers](#creating-a-timer)
-   [Zerstören eines Timers](#destroying-a-timer)
-   [Verwenden von Timer-Funktionen zum Abfangen von Maus Eingaben](#using-timer-functions-to-trap-mouse-input)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-timer"></a>Erstellen eines Timers

Im folgenden Beispiel wird die [**Funktion "**](/windows/win32/api/winuser/nf-winuser-settimer) -Funktion" verwendet, um zwei Timer zu erstellen. Der erste Timer wird für alle 10 Sekunden festgelegt, die zweite für alle fünf Minuten.


```
// Set two timers. 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER1,            // timer identifier 
    10000,                 // 10-second interval 
    (TIMERPROC) NULL);     // no timer callback 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER2,            // timer identifier 
    300000,                // five-minute interval 
    (TIMERPROC) NULL);     // no timer callback 
```



Um die von diesen Zeit Gebern generierten WM-Zeit Geber Meldungen zu verarbeiten, fügen Sie der Fenster Prozedur für den *HWND* -Parameter eine " **WM- \_ Timer** Case"-Anweisung hinzu. [**\_**](wm-timer.md)


```
case WM_TIMER: 
 
    switch (wParam) 
    { 
        case IDT_TIMER1: 
            // process the 10-second timer 
 
             return 0; 
 
        case IDT_TIMER2: 
            // process the five-minute timer 

            return 0; 
    } 
```



Eine Anwendung kann auch einen Timer erstellen, dessen WM-Zeit Geber Nachrichten nicht von der Hauptfenster Prozedur, sondern von einer Anwendungs definierten Rückruffunktion verarbeitet werden, wie im folgenden Codebeispiel, das einen Timer erstellt und die Rückruffunktion **mytimerproc** verwendet, um die **WM \_** -Zeit Geber Meldungen des Timers zu verarbeiten. [**\_**](wm-timer.md)


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



Die Aufruf Konvention für **mytimerproc** muss auf der [*timerproc*](/windows/win32/api/winuser/nc-winuser-timerproc) -Rückruffunktion basieren.

Wenn Ihre Anwendung einen Timer ohne Angabe eines Fenster Handles erstellt, muss Ihre Anwendung die Nachrichten Warteschlange auf die Zeit Geber Nachrichten der [**WM \_**](wm-timer.md) überwachen und Sie an das entsprechende Fenster verteilen.


```
HWND hwndTimer;   // handle to window for timer messages 
MSG msg;          // message structure 
 
    while (GetMessage(&msg, // message structure 
            NULL,           // handle to window to receive the message 
               0,           // lowest message to examine 
               0))          // highest message to examine 
    { 
 
        // Post WM_TIMER messages to the hwndTimer procedure. 
 
        if (msg.message == WM_TIMER) 
        { 
            msg.hwnd = hwndTimer; 
        } 
 
        TranslateMessage(&msg); // translates virtual-key codes 
        DispatchMessage(&msg);  // dispatches message to window 
    } 
```



## <a name="destroying-a-timer"></a>Zerstören eines Timers

Anwendungen sollten die [**killtimer**](/windows/win32/api/winuser/nf-winuser-killtimer) -Funktion verwenden, um Timer zu zerstören, die nicht mehr benötigt werden. Im folgenden Beispiel werden die von den konstanten IDT \_ Timer1, IDT \_ TIMER2 und IDT TIMER3 identifizierten Timer zerstört \_ .


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Verwenden von Timer-Funktionen zum Abfangen von Maus Eingaben

Manchmal ist es erforderlich, mehr Eingaben zu verhindern, während ein Mauszeiger auf dem Bildschirm angezeigt wird. Eine Möglichkeit, dies zu erreichen, besteht darin, eine spezielle Routine zu erstellen, die Maus Eingaben abfängt, bis ein bestimmtes Ereignis eintritt. Viele Entwickler verweisen auf diese Routine als "aufbauen eines moustraps".

Im folgenden Beispiel werden die Funktionen " [**SETTIMER**](/windows/win32/api/winuser/nf-winuser-settimer) " und " [**killtimer**](/windows/win32/api/winuser/nf-winuser-killtimer) " zum Abfangen der Maus Eingaben verwendet.  "" Ist ein Timer, der alle 10 Sekunden eine Zeit Geber Meldung vom [**WM \_**](wm-timer.md) sendet. Jedes Mal, wenn die Anwendung **eine \_ WM** -Zeit Geber Nachricht empfängt, wird die Position des Mauszeigers aufgezeichnet. Wenn der aktuelle Speicherort mit dem vorherigen Speicherort identisch ist und das Hauptfenster der Anwendung minimiert ist, verschiebt die Anwendung den Mauszeiger auf das Symbol. Wenn die Anwendung geschlossen wird, beendet **killtimer** den Timer.


```
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
UINT uResult;               // SetTimer's return value 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the initial cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,             // handle to main window 
    IDT_MOUSETRAP,                   // timer identifier 
    10000,                           // 10-second interval 
    (TIMERPROC) NULL);               // no timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM  lParam)     // additional information 
{ 
 
    HDC hdc;        // handle to device context 
    POINT pt;       // current cursor location 
    RECT rc;        // location of minimized window 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
 
        case WM_TIMER: 
        // If the window is minimized, compare the current 
        // cursor position with the one from 10 seconds 
        // earlier. If the cursor position has not changed, 
        // move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left, rc.top); 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_DESTROY: 
 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
```



Obwohl das folgende Beispiel zeigt, wie Maus Eingaben abgefangen werden, wird die WM- [**Zeit \_**](wm-timer.md) Geber Nachricht durch die Anwendungs definierte Rückruffunktion **mytimerproc** und nicht durch die Meldungs Warteschlange der Anwendung verarbeitet.


```
UINT uResult;               // SetTimer's return value 
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the current cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,      // handle to main window 
    IDT_MOUSETRAP,            // timer identifier 
    10000,                    // 10-second interval 
    (TIMERPROC) MyTimerProc); // timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM   lParam)    // additional information 
{ 
 
    HDC hdc;            // handle to device context 
 
    switch (message) 
    { 
    // 
    // Process other messages. 
    // 
 
        case WM_DESTROY: 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
 
// MyTimerProc is an application-defined callback function that 
// processes WM_TIMER messages. 
 
VOID CALLBACK MyTimerProc( 
    HWND hwnd,        // handle to window for timer messages 
    UINT message,     // WM_TIMER message 
    UINT idTimer,     // timer identifier 
    DWORD dwTime)     // current system time 
{ 
 
    RECT rc; 
    POINT pt; 
 
    // If the window is minimized, compare the current 
    // cursor position with the one from 10 seconds earlier. 
    // If the cursor position has not changed, move the 
    // cursor to the icon. 
 
    if (IsIconic(hwnd)) 
    { 
        GetCursorPos(&pt); 
 
        if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
        { 
            GetWindowRect(hwnd, &rc); 
            SetCursorPos(rc.left, rc.top); 
        } 
        else 
        { 
            ptOld.x = pt.x; 
            ptOld.y = pt.y; 
        } 
    } 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Timern](about-timers.md)
</dt> </dl>

 

 
