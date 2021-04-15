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
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="2e33e-104">Modul 1.</span><span class="sxs-lookup"><span data-stu-id="2e33e-104">Module 1.</span></span> <span data-ttu-id="2e33e-105">Ihr erstes Windows-Programm</span><span class="sxs-lookup"><span data-stu-id="2e33e-105">Your First Windows Program</span></span>

<span data-ttu-id="2e33e-106">In diesem Modul wird ein minimales Windows-Desktop Programm geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2e33e-106">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="2e33e-107">Es wird lediglich ein leeres Fenster erstellt und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e33e-107">All it does is create and show a blank window.</span></span> <span data-ttu-id="2e33e-108">Dieses erste Programm enthält ungefähr 50 Codezeilen, wobei keine leeren Zeilen und Kommentare gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="2e33e-108">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="2e33e-109">Das ist unser Ausgangspunkt. Später fügen wir Grafiken, Text, Benutzereingaben und andere Features hinzu.</span><span class="sxs-lookup"><span data-stu-id="2e33e-109">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="2e33e-110">Weitere Informationen zum Erstellen einer herkömmlichen Windows-Desktop Anwendung in Visual Studio finden Sie unter Exemplarische Vorgehensweise  [: Erstellen einer herkömmlichen Windows-Desktop Anwendung (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="2e33e-110">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![Screenshot des Beispiel Programms](images/window01.png)

<span data-ttu-id="2e33e-112">Im folgenden finden Sie den gesamten Code für das Programm:</span><span class="sxs-lookup"><span data-stu-id="2e33e-112">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="2e33e-113">Sie können das komplette Visual Studio-Projekt aus dem [Windows Hallo Welt-Beispiel](windows-hello-world-sample.md)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2e33e-113">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="2e33e-114">Es kann sinnvoll sein, einen kurzen Überblick über die Funktionsweise dieses Codes zu geben.</span><span class="sxs-lookup"><span data-stu-id="2e33e-114">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="2e33e-115">In späteren Themen wird der Code ausführlich untersucht.</span><span class="sxs-lookup"><span data-stu-id="2e33e-115">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="2e33e-116">**wWinMain** ist der Programm Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="2e33e-116">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="2e33e-117">Wenn das Programm gestartet wird, werden einige Informationen über das Verhalten des Anwendungsfensters registriert.</span><span class="sxs-lookup"><span data-stu-id="2e33e-117">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="2e33e-118">Eines der wichtigsten Elemente ist die Adresse einer Funktion, die `WindowProc` in diesem Beispiel benannt wird.</span><span class="sxs-lookup"><span data-stu-id="2e33e-118">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="2e33e-119">Diese Funktion definiert das Verhalten des Fensters – seine Darstellung, die Interaktion mit dem Benutzer und so weiter.</span><span class="sxs-lookup"><span data-stu-id="2e33e-119">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="2e33e-120">Als Nächstes erstellt das Programm das Fenster und empfängt ein Handle, das das Fenster eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2e33e-120">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="2e33e-121">Wenn das Fenster erfolgreich erstellt wurde, gibt das Programm eine **while** -Schleife ein.</span><span class="sxs-lookup"><span data-stu-id="2e33e-121">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="2e33e-122">Das Programm verbleibt in dieser Schleife, bis der Benutzer das Fenster schließt und die Anwendung beendet.</span><span class="sxs-lookup"><span data-stu-id="2e33e-122">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="2e33e-123">Beachten Sie, dass das Programm die-Funktion nicht explizit aufruft `WindowProc` , obwohl wir sagten, dass dies der größte Teil der Anwendungslogik ist.</span><span class="sxs-lookup"><span data-stu-id="2e33e-123">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="2e33e-124">Windows kommuniziert mit Ihrem Programm, indem es eine Reihe von *Nachrichten* übergibt.</span><span class="sxs-lookup"><span data-stu-id="2e33e-124">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="2e33e-125">Der Code in der **while** -Schleife steuert diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="2e33e-125">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="2e33e-126">Jedes Mal, wenn das Programm die [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) -Funktion aufruft, bewirkt dies indirekt, dass Windows die WindowProc-Funktion aufruft, einmal für jede Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2e33e-126">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e33e-127">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2e33e-127">In this section</span></span>

-   [<span data-ttu-id="2e33e-128">Erstellen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="2e33e-128">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="2e33e-129">Fenster Meldungen</span><span class="sxs-lookup"><span data-stu-id="2e33e-129">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="2e33e-130">Schreiben der Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="2e33e-130">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="2e33e-131">Zeichnen des Fensters</span><span class="sxs-lookup"><span data-stu-id="2e33e-131">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="2e33e-132">Schließen des Fensters</span><span class="sxs-lookup"><span data-stu-id="2e33e-132">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="2e33e-133">Managing Application State (Verwalten eines Anwendungszustands)</span><span class="sxs-lookup"><span data-stu-id="2e33e-133">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="2e33e-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e33e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e33e-135">Erlernen Sie das Program mieren für Windows in C++</span><span class="sxs-lookup"><span data-stu-id="2e33e-135">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="2e33e-136">Windows Hallo Welt-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e33e-136">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
