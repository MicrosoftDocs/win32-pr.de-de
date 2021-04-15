---
title: Modul 1. Ihr erstes Windows-Programm
description: .
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27749cddabaefb4fd83b836887fbb2dac017d238
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "104570285"
---
# <a name="module-1-your-first-windows-program"></a>Modul 1. Ihr erstes Windows-Programm

In diesem Modul wird ein minimales Windows-Desktop Programm geschrieben. Es wird lediglich ein leeres Fenster erstellt und angezeigt. Dieses erste Programm enthält ungefähr 50 Codezeilen, wobei keine leeren Zeilen und Kommentare gezählt werden. Das ist unser Ausgangspunkt. Später fügen wir Grafiken, Text, Benutzereingaben und andere Features hinzu.

Weitere Informationen zum Erstellen einer herkömmlichen Windows-Desktop Anwendung in Visual Studio finden Sie unter Exemplarische Vorgehensweise  [: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).

![Screenshot des Beispiel Programms](images/window01.png)

Im folgenden finden Sie den gesamten Code für das Programm:


```C++
#ifndef UNICODE
#define UNICODE
#endif 

#include <windows.h>

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow)
{
    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    // Create the window.

    HWND hwnd = CreateWindowEx(
        0,                              // Optional window styles.
        CLASS_NAME,                     // Window class
        L"Learn to Program Windows",    // Window text
        WS_OVERLAPPEDWINDOW,            // Window style

        // Size and position
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

        NULL,       // Parent window    
        NULL,       // Menu
        hInstance,  // Instance handle
        NULL        // Additional application data
        );

    if (hwnd == NULL)
    {
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);



            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

            EndPaint(hwnd, &ps);
        }
        return 0;

    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}
```





Sie können das komplette Visual Studio-Projekt aus dem [Windows Hallo Welt-Beispiel](windows-hello-world-sample.md)herunterladen.

Es kann sinnvoll sein, einen kurzen Überblick über die Funktionsweise dieses Codes zu geben. In späteren Themen wird der Code ausführlich untersucht.

1.  **wWinMain** ist der Programm Einstiegspunkt. Wenn das Programm gestartet wird, werden einige Informationen über das Verhalten des Anwendungsfensters registriert. Eines der wichtigsten Elemente ist die Adresse einer Funktion, die `WindowProc` in diesem Beispiel benannt wird. Diese Funktion definiert das Verhalten des Fensters – seine Darstellung, die Interaktion mit dem Benutzer und so weiter.
2.  Als Nächstes erstellt das Programm das Fenster und empfängt ein Handle, das das Fenster eindeutig identifiziert.
3.  Wenn das Fenster erfolgreich erstellt wurde, gibt das Programm eine **while** -Schleife ein. Das Programm verbleibt in dieser Schleife, bis der Benutzer das Fenster schließt und die Anwendung beendet.

Beachten Sie, dass das Programm die-Funktion nicht explizit aufruft `WindowProc` , obwohl wir sagten, dass dies der größte Teil der Anwendungslogik ist. Windows kommuniziert mit Ihrem Programm, indem es eine Reihe von *Nachrichten* übergibt. Der Code in der **while** -Schleife steuert diesen Prozess. Jedes Mal, wenn das Programm die [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) -Funktion aufruft, bewirkt dies indirekt, dass Windows die WindowProc-Funktion aufruft, einmal für jede Nachricht.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Erstellen eines Fensters](creating-a-window.md)
-   [Fenster Meldungen](window-messages.md)
-   [Schreiben der Fenster Prozedur](writing-the-window-procedure.md)
-   [Zeichnen des Fensters](painting-the-window.md)
-   [Schließen des Fensters](closing-the-window.md)
-   [Managing Application State (Verwalten eines Anwendungszustands)](managing-application-state-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erlernen Sie das Program mieren für Windows in C++](learn-to-program-for-windows.md)
</dt> <dt>

[Windows Hallo Welt-Beispiel](windows-hello-world-sample.md)
</dt> </dl>

 

 
