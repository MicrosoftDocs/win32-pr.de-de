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
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="af903-105">Modul 1.</span><span class="sxs-lookup"><span data-stu-id="af903-105">Module 1.</span></span> <span data-ttu-id="af903-106">Ihr erstes Windows-Programm</span><span class="sxs-lookup"><span data-stu-id="af903-106">Your First Windows Program</span></span>

<span data-ttu-id="af903-107">In diesem Modul schreiben wir ein minimales Windows-Desktopprogramm.</span><span class="sxs-lookup"><span data-stu-id="af903-107">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="af903-108">Es wird nur ein leeres Fenster erstellt und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af903-108">All it does is create and show a blank window.</span></span> <span data-ttu-id="af903-109">Dieses erste Programm enthält ungefähr 50 Codezeilen, ohne leere Zeilen und Kommentare zu zählen.</span><span class="sxs-lookup"><span data-stu-id="af903-109">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="af903-110">Es wird unser Ausgangspunkt sein. Später fügen wir Grafiken, Text, Benutzereingaben und andere Features hinzu.</span><span class="sxs-lookup"><span data-stu-id="af903-110">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="af903-111">Weitere Informationen zum Erstellen einer herkömmlichen Windows-Desktopanwendung in Visual Studio finden Sie unter [Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows-Desktopanwendung (C++).](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)</span><span class="sxs-lookup"><span data-stu-id="af903-111">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![Screenshot des Beispielprogramms](images/window01.png)

<span data-ttu-id="af903-113">Hier ist der vollständige Code für das Programm:</span><span class="sxs-lookup"><span data-stu-id="af903-113">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="af903-114">Sie können das vollständige Visual Studio-Projekt aus [Windows Hello World Sample](windows-hello-world-sample.md)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="af903-114">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="af903-115">Es kann hilfreich sein, einen kurzen Überblick über die Aufgabe dieses Codes zu geben.</span><span class="sxs-lookup"><span data-stu-id="af903-115">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="af903-116">In späteren Themen wird der Code ausführlich untersucht.</span><span class="sxs-lookup"><span data-stu-id="af903-116">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="af903-117">**wWinMain** ist der Einstiegspunkt für das Programm.</span><span class="sxs-lookup"><span data-stu-id="af903-117">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="af903-118">Wenn das Programm gestartet wird, werden einige Informationen zum Verhalten des Anwendungsfensters registriert.</span><span class="sxs-lookup"><span data-stu-id="af903-118">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="af903-119">Eines der wichtigsten Elemente ist die Adresse einer Funktion, die in diesem Beispiel benannt `WindowProc` wird.</span><span class="sxs-lookup"><span data-stu-id="af903-119">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="af903-120">Diese Funktion definiert das Verhalten des Fensters – seine Darstellung, die Interaktion mit dem Benutzer usw.</span><span class="sxs-lookup"><span data-stu-id="af903-120">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="af903-121">Als Nächstes erstellt das Programm das Fenster und empfängt ein Handle, das das Fenster eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="af903-121">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="af903-122">Wenn das Fenster erfolgreich erstellt wurde, geht das Programm in eine **while-Schleife** über.</span><span class="sxs-lookup"><span data-stu-id="af903-122">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="af903-123">Das Programm verbleibt in dieser Schleife, bis der Benutzer das Fenster schließt und die Anwendung beendet.</span><span class="sxs-lookup"><span data-stu-id="af903-123">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="af903-124">Beachten Sie, dass das Programm die Funktion nicht explizit aufruft, obwohl wir gesagt haben, dass hier der Großteil `WindowProc` der Anwendungslogik definiert ist.</span><span class="sxs-lookup"><span data-stu-id="af903-124">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="af903-125">Windows kommuniziert mit Ihrem Programm, indem eine Reihe von Nachrichten übergeben *wird.*</span><span class="sxs-lookup"><span data-stu-id="af903-125">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="af903-126">Der Code in der **while-Schleife** steuert diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="af903-126">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="af903-127">Jedes Mal, wenn das Programm die [**DispatchMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) aufruft, führt es indirekt dazu, dass Windows die WindowProc-Funktion einmal für jede Nachricht aufruft.</span><span class="sxs-lookup"><span data-stu-id="af903-127">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af903-128">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="af903-128">In this section</span></span>

-   [<span data-ttu-id="af903-129">Erstellen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="af903-129">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="af903-130">Fenstermeldungen</span><span class="sxs-lookup"><span data-stu-id="af903-130">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="af903-131">Schreiben der Fensterprozedur</span><span class="sxs-lookup"><span data-stu-id="af903-131">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="af903-132">Malen des Fensters</span><span class="sxs-lookup"><span data-stu-id="af903-132">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="af903-133">Schließen des Fensters</span><span class="sxs-lookup"><span data-stu-id="af903-133">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="af903-134">Managing Application State (Verwalten eines Anwendungszustands)</span><span class="sxs-lookup"><span data-stu-id="af903-134">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="af903-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af903-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af903-136">Informationen zum Programmieren für Windows in C++</span><span class="sxs-lookup"><span data-stu-id="af903-136">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="af903-137">Windows Hello World Sample</span><span class="sxs-lookup"><span data-stu-id="af903-137">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
