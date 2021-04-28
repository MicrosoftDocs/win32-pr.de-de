---
title: Modul 1. Ihr erstes Windows-Programm
description: Modul 1. Ihr erstes Windows-Programm
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6515b012f968707379ebf24023c3d282c50d6fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110948"
---
# <a name="module-1-your-first-windows-program"></a>Modul 1. Ihr erstes Windows-Programm

In diesem Modul schreiben wir ein minimales Windows-Desktopprogramm. Es wird nur ein leeres Fenster erstellt und angezeigt. Dieses erste Programm enthält ungefähr 50 Codezeilen, ohne leere Zeilen und Kommentare zu zählen. Es wird unser Ausgangspunkt sein. Später fügen wir Grafiken, Text, Benutzereingaben und andere Features hinzu.

Weitere Informationen zum Erstellen einer herkömmlichen Windows-Desktopanwendung in Visual Studio finden Sie unter [Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktopanwendung (C++).](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)

![Screenshot des Beispielprogramms](images/window01.png)

Hier ist der vollständige Code für das Programm:


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





Sie können das vollständige Visual Studio-Projekt aus [Windows Hello World Sample](windows-hello-world-sample.md)herunterladen.

Es kann hilfreich sein, einen kurzen Überblick über die Aufgabe dieses Codes zu geben. In späteren Themen wird der Code ausführlich untersucht.

1.  **wWinMain** ist der Einstiegspunkt für das Programm. Wenn das Programm gestartet wird, werden einige Informationen zum Verhalten des Anwendungsfensters registriert. Eines der wichtigsten Elemente ist die Adresse einer Funktion, die in diesem Beispiel benannt `WindowProc` wird. Diese Funktion definiert das Verhalten des Fensters – seine Darstellung, die Interaktion mit dem Benutzer usw.
2.  Als Nächstes erstellt das Programm das Fenster und empfängt ein Handle, das das Fenster eindeutig identifiziert.
3.  Wenn das Fenster erfolgreich erstellt wurde, geht das Programm in eine **while-Schleife** über. Das Programm verbleibt in dieser Schleife, bis der Benutzer das Fenster schließt und die Anwendung beendet.

Beachten Sie, dass das Programm die Funktion nicht explizit aufruft, obwohl wir gesagt haben, dass hier der Großteil `WindowProc` der Anwendungslogik definiert ist. Windows kommuniziert mit Ihrem Programm, indem eine Reihe von Nachrichten übergeben *wird.* Der Code in der **while-Schleife** steuert diesen Prozess. Jedes Mal, wenn das Programm die [**DispatchMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) aufruft, führt es indirekt dazu, dass Windows die WindowProc-Funktion einmal für jede Nachricht aufruft.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Erstellen eines Fensters](creating-a-window.md)
-   [Fenstermeldungen](window-messages.md)
-   [Schreiben der Fensterprozedur](writing-the-window-procedure.md)
-   [Malen des Fensters](painting-the-window.md)
-   [Schließen des Fensters](closing-the-window.md)
-   [Managing Application State (Verwalten eines Anwendungszustands)](managing-application-state-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Programmieren für Windows in C++](learn-to-program-for-windows.md)
</dt> <dt>

[Windows Hello World Sample](windows-hello-world-sample.md)
</dt> </dl>

 

 
