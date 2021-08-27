---
description: In diesem Thema wird gezeigt, wie Timer erstellt und zerstört werden und wie ein Timer verwendet wird, um Mauseingaben in bestimmten Intervallen abzufangen.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Verwenden von Timern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7922be60012ae81ce1971afe6f2300f54689f7a6cc8d7f088df2fb126e834ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028308"
---
# <a name="using-timers"></a>Verwenden von Timern

In diesem Thema wird gezeigt, wie Timer erstellt und zerstört werden und wie ein Timer verwendet wird, um Mauseingaben in bestimmten Intervallen abzufangen.

Dieses Thema enthält folgende Abschnitte:

-   [Erstellen eines Timers](#creating-a-timer)
-   [Zerstören eines Timers](#destroying-a-timer)
-   [Verwenden von Timerfunktionen zum Abfangen von Mauseingaben](#using-timer-functions-to-trap-mouse-input)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-timer"></a>Erstellen eines Timers

Im folgenden Beispiel wird die [**SetTimer-Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) verwendet, um zwei Timer zu erstellen. Der erste Timer wird alle 10 Sekunden festgelegt, der zweite für alle fünf Minuten.


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



Um die von diesen Timern generierten [**WM \_ TIMER-Nachrichten**](wm-timer.md) zu verarbeiten, fügen Sie der Fensterprozedur für den *hwnd-Parameter* eine **WM \_ TIMER-Case-Anweisung** hinzu.


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



Eine Anwendung kann auch einen Timer erstellen, dessen [**WM \_ TIMER-Nachrichten**](wm-timer.md) nicht durch die Hauptfensterprozedur, sondern durch eine anwendungsdefinierte Rückruffunktion verarbeitet werden, wie im folgenden Codebeispiel, das einen Timer erstellt und die Rückruffunktion **MyTimerProc** verwendet, um die **WM \_ TIMER-Nachrichten** des Timers zu verarbeiten.


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



Die Aufrufkonvention für **MyTimerProc** muss auf der [*TimerProc-Rückruffunktion*](/windows/win32/api/winuser/nc-winuser-timerproc) basieren.

Wenn Ihre Anwendung einen Timer erstellt, ohne ein Fensterhandle anzugeben, muss Ihre Anwendung die Nachrichtenwarteschlange auf [**WM \_ TIMER-Nachrichten**](wm-timer.md) überwachen und an das entsprechende Fenster senden.


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

Anwendungen sollten die [**KillTimer-Funktion**](/windows/win32/api/winuser/nf-winuser-killtimer) verwenden, um Timer zu zerstören, die nicht mehr benötigt werden. Im folgenden Beispiel werden die durch die Konstanten IDT \_ TIMER1, IDT \_ TIMER2 und IDT TIMER3 identifizierten \_ Timer gelöscht.


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Verwenden von Timerfunktionen zum Abfangen von Mauseingaben

Manchmal ist es notwendig, mehr Eingaben zu verhindern, während Sie einen Mauszeiger auf dem Bildschirm haben. Eine Möglichkeit, dies zu erreichen, besteht darin, eine spezielle Routine zu erstellen, die Mauseingaben abfängt, bis ein bestimmtes Ereignis eintritt. Viele Entwickler bezeichnen diese Routine als "Erstellen einer Maustrap".

Im folgenden Beispiel werden die [**Funktionen SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) und [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) verwendet, um Mauseingaben abzufangen. **SetTimer** erstellt einen Timer, der alle 10 Sekunden eine [**WM \_ TIMER-Nachricht**](wm-timer.md) sendet. Jedes Mal, wenn die Anwendung eine **WM \_ TIMER-Nachricht** empfängt, zeichnet sie die Position des Mauszeigers auf. Wenn die aktuelle Position mit der vorherigen Position identisch ist und das Hauptfenster der Anwendung minimiert ist, verschiebt die Anwendung den Mauszeiger auf das Symbol. Wenn die Anwendung geschlossen wird, beendet **KillTimer** den Timer.


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



Obwohl im folgenden Beispiel auch gezeigt wird, wie Mauseingaben abfangen werden, wird die [**WM \_ TIMER-Nachricht**](wm-timer.md) über die anwendungsdefinierte Rückruffunktion **MyTimerProc** und nicht über die Nachrichtenwarteschlange der Anwendung verarbeitet.


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

 

 
