---
description: Die folgenden Codebeispiele veranschaulichen, wie die folgenden Aufgaben ausgeführt werden, die Windows-Meldungen und Nachrichten Warteschlangen zugeordnet sind.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Verwenden von Meldungen und Nachrichten Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373057"
---
# <a name="using-messages-and-message-queues"></a><span data-ttu-id="ca6d5-103">Verwenden von Meldungen und Nachrichten Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="ca6d5-103">Using Messages and Message Queues</span></span>

<span data-ttu-id="ca6d5-104">Die folgenden Codebeispiele veranschaulichen, wie die folgenden Aufgaben ausgeführt werden, die Windows-Meldungen und Nachrichten Warteschlangen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-104">The following code examples demonstrate how to perform the following tasks associated with Windows messages and message queues.</span></span>

-   [<span data-ttu-id="ca6d5-105">Erstellen einer Nachrichten Schleife</span><span class="sxs-lookup"><span data-stu-id="ca6d5-105">Creating a Message Loop</span></span>](#creating-a-message-loop)
-   [<span data-ttu-id="ca6d5-106">Überprüfen einer Nachrichten Warteschlange</span><span class="sxs-lookup"><span data-stu-id="ca6d5-106">Examining a Message Queue</span></span>](#examining-a-message-queue)
-   [<span data-ttu-id="ca6d5-107">Veröffentlichen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="ca6d5-107">Posting a Message</span></span>](#posting-a-message)
-   [<span data-ttu-id="ca6d5-108">Senden einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="ca6d5-108">Sending a Message</span></span>](#sending-a-message)

## <a name="creating-a-message-loop"></a><span data-ttu-id="ca6d5-109">Erstellen einer Nachrichten Schleife</span><span class="sxs-lookup"><span data-stu-id="ca6d5-109">Creating a Message Loop</span></span>

<span data-ttu-id="ca6d5-110">Das System erstellt nicht automatisch eine Nachrichten Warteschlange für jeden Thread.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-110">The system does not automatically create a message queue for each thread.</span></span> <span data-ttu-id="ca6d5-111">Stattdessen erstellt das System eine Nachrichten Warteschlange nur für Threads, die Vorgänge ausführen, für die eine Nachrichten Warteschlange erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-111">Instead, the system creates a message queue only for threads that perform operations which require a message queue.</span></span> <span data-ttu-id="ca6d5-112">Wenn der Thread ein oder mehrere Fenster erstellt, muss eine Nachrichten Schleife bereitgestellt werden. Diese Nachrichten Schleife ruft Nachrichten aus der Nachrichten Warteschlange des Threads ab und sendet Sie an die entsprechenden Fenster Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-112">If the thread creates one or more windows, a message loop must be provided; this message loop retrieves messages from the thread's message queue and dispatches them to the appropriate window procedures.</span></span>

<span data-ttu-id="ca6d5-113">Da das System Nachrichten an einzelne Fenster in einer Anwendung weiterleitet, muss ein Thread vor dem Starten der Nachrichten Schleife mindestens ein Fenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-113">Because the system directs messages to individual windows in an application, a thread must create at least one window before starting its message loop.</span></span> <span data-ttu-id="ca6d5-114">Die meisten Anwendungen enthalten einen einzelnen Thread, der Windows erstellt.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-114">Most applications contain a single thread that creates windows.</span></span> <span data-ttu-id="ca6d5-115">Eine typische Anwendung registriert die Fenster Klasse für das Hauptfenster, erstellt und zeigt das Hauptfenster an und startet dann die Nachrichten Schleife – alles in der [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-115">A typical application registers the window class for its main window, creates and shows the main window, and then starts its message loop — all in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span>

<span data-ttu-id="ca6d5-116">Sie erstellen eine Nachrichten Schleife mithilfe der Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="ca6d5-116">You create a message loop by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span> <span data-ttu-id="ca6d5-117">Wenn die Anwendung Zeichen Eingaben vom Benutzer abrufen muss, schließen Sie die [**translatemess**](/windows/win32/api/winuser/nf-winuser-translatemessage) -Funktion in die-Schleife ein.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-117">If your application must obtain character input from the user, include the [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) function in the loop.</span></span> <span data-ttu-id="ca6d5-118">**Translatemess** übersetzt die Nachrichten von virtuellen Schlüsseln in Zeichen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-118">**TranslateMessage** translates virtual-key messages into character messages.</span></span> <span data-ttu-id="ca6d5-119">Das folgende Beispiel zeigt die Nachrichten Schleife in der [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion einer einfachen Windows-basierten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-119">The following example shows the message loop in the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of a simple Windows-based application.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



<span data-ttu-id="ca6d5-120">Das folgende Beispiel zeigt eine Meldungs Schleife für einen Thread, der Accelerators verwendet und ein nicht modalem Dialogfeld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-120">The following example shows a message loop for a thread that uses accelerators and displays a modeless dialog box.</span></span> <span data-ttu-id="ca6d5-121">Wenn [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) oder [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) **true** zurückgibt (gibt an, dass die Nachricht verarbeitet wurde), werden [**translatemmeage**](/windows/win32/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-121">When [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) or [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) returns **TRUE** (indicating that the message has been processed), [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) are not called.</span></span> <span data-ttu-id="ca6d5-122">Der Grund hierfür ist, dass **TranslateAccelerator** und **IsDialogMessage** alle notwendigen Übersetzungen und die Weiterleitung von Nachrichten durchführen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-122">The reason for this is that **TranslateAccelerator** and **IsDialogMessage** perform all necessary translating and dispatching of messages.</span></span>


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a><span data-ttu-id="ca6d5-123">Überprüfen einer Nachrichten Warteschlange</span><span class="sxs-lookup"><span data-stu-id="ca6d5-123">Examining a Message Queue</span></span>

<span data-ttu-id="ca6d5-124">Gelegentlich muss eine Anwendung den Inhalt der Nachrichten Warteschlange eines Threads von außerhalb der Nachrichten Schleife des Threads untersuchen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-124">Occasionally, an application needs to examine the contents of a thread's message queue from outside the thread's message loop.</span></span> <span data-ttu-id="ca6d5-125">Wenn z. b. die Fenster Prozedur einer Anwendung einen langwierigen Zeichnungs Vorgang ausführt, kann es sein, dass der Benutzer in der Lage sein soll, den Vorgang zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-125">For example, if an application's window procedure performs a lengthy drawing operation, you may want the user to be able to interrupt the operation.</span></span> <span data-ttu-id="ca6d5-126">Wenn die Anwendung die Nachrichten Warteschlange während des Vorgangs für Maus-und Tastatur Meldungen nicht regelmäßig überprüft, antwortet sie erst nach Abschluss des Vorgangs auf Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-126">Unless your application periodically examines the message queue during the operation for mouse and keyboard messages, it will not respond to user input until after the operation has completed.</span></span> <span data-ttu-id="ca6d5-127">Der Grund hierfür ist, dass die [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) -Funktion in der Nachrichten Schleife des Threads erst dann zurückgegeben wird, wenn die Verarbeitung einer Nachricht durch die Fenster Prozedur abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-127">The reason for this is that the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function in the thread's message loop does not return until the window procedure finishes processing a message.</span></span>

<span data-ttu-id="ca6d5-128">Sie können die Funktion " [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) " verwenden, um eine Nachrichten Warteschlange während eines langen Vorgangs zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-128">You can use the [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function to examine a message queue during a lengthy operation.</span></span> <span data-ttu-id="ca6d5-129">" **Peer Message** " ähnelt der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion. Beide überprüfen eine Meldungs Warteschlange auf eine Nachricht, die den Filterkriterien entspricht, und kopieren dann die Nachricht in eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-129">**PeekMessage** is similar to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function; both check a message queue for a message that matches the filter criteria and then copy the message to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="ca6d5-130">Der Hauptunterschied zwischen den beiden Funktionen besteht darin, dass **GetMessage** nicht **zurückgibt,** bis eine Nachricht, die mit den Filterkriterien übereinstimmt, in der Warteschlange platziert wird.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-130">The main difference between the two functions is that **GetMessage** does not return until a message matching the filter criteria is placed in the queue, whereas **PeekMessage** returns immediately regardless of whether a message is in the queue.</span></span>

<span data-ttu-id="ca6d5-131">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von " [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) " eine Meldungs Warteschlange für Mausklicks und Tastatureingaben während eines langen Vorgangs untersuchen können.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-131">The following example shows how to use [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) to examine a message queue for mouse clicks and keyboard input during a lengthy operation.</span></span>


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



<span data-ttu-id="ca6d5-132">Andere Funktionen, einschließlich [**getqueuestatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) und [**getinputstate**](/windows/win32/api/winuser/nf-winuser-getinputstate), ermöglichen es Ihnen außerdem, den Inhalt der Nachrichten Warteschlange eines Threads zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-132">Other functions, including [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) and [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate), also allow you to examine the contents of a thread's message queue.</span></span> <span data-ttu-id="ca6d5-133">**Getqueuestatus** gibt ein Array von Flags zurück, das die Nachrichten Typen in der Warteschlange angibt. die Verwendung ist die schnellste Möglichkeit, um zu ermitteln, ob die Warteschlange Nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-133">**GetQueueStatus** returns an array of flags that indicates the types of messages in the queue; using it is the fastest way to discover whether the queue contains any messages.</span></span> <span data-ttu-id="ca6d5-134">**Getinputstate** gibt **true** zurück, wenn die Warteschlange Maus-oder Tastatur Meldungen enthält.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-134">**GetInputState** returns **TRUE** if the queue contains mouse or keyboard messages.</span></span> <span data-ttu-id="ca6d5-135">Beide Funktionen können verwendet werden, um zu bestimmen, ob die Warteschlange Nachrichten enthält, die verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-135">Both of these functions can be used to determine whether the queue contains messages that need to be processed.</span></span>

## <a name="posting-a-message"></a><span data-ttu-id="ca6d5-136">Veröffentlichen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="ca6d5-136">Posting a Message</span></span>

<span data-ttu-id="ca6d5-137">Mithilfe der [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion können Sie eine Nachricht in einer Nachrichten Warteschlange veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-137">You can post a message to a message queue by using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function.</span></span> <span data-ttu-id="ca6d5-138">Nach **richten** platziert eine Nachricht am Ende der Nachrichten Warteschlange eines Threads und gibt sofort zurück, ohne darauf zu warten, dass der Thread die Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-138">**PostMessage** places a message at the end of a thread's message queue and returns immediately, without waiting for the thread to process the message.</span></span> <span data-ttu-id="ca6d5-139">Die Parameter der Funktion enthalten ein Fenster Handle, eine Nachrichten-ID und zwei Nachrichten Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-139">The function's parameters include a window handle, a message identifier, and two message parameters.</span></span> <span data-ttu-id="ca6d5-140">Das System kopiert diese Parameter in eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, füllt die **Zeit** -und **PT** -Member der Struktur aus und platziert die Struktur in der Nachrichten Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-140">The system copies these parameters to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure, fills the **time** and **pt** members of the structure, and places the structure in the message queue.</span></span>

<span data-ttu-id="ca6d5-141">Das System verwendet das mit der [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion über gegebene Fenster Handle, um zu bestimmen, welche Thread Nachrichten Warteschlange die Nachricht empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-141">The system uses the window handle passed with the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to determine which thread message queue should receive the message.</span></span> <span data-ttu-id="ca6d5-142">Wenn das Handle das **\_ oberste HWND** ist, stellt das System die Nachricht an die Thread Nachrichten Warteschlangen aller Fenster der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-142">If the handle is **HWND\_TOPMOST**, the system posts the message to the thread message queues of all top-level windows.</span></span>

<span data-ttu-id="ca6d5-143">Sie können die [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) -Funktion verwenden, um eine Nachricht an eine bestimmte Thread Nachrichten Warteschlange zu senden.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-143">You can use the [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) function to post a message to a specific thread message queue.</span></span> <span data-ttu-id="ca6d5-144">**PostThreadMessage** ist " [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)" ähnlich, außer der erste Parameter ist ein Thread Bezeichner und kein Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-144">**PostThreadMessage** is similar to [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea), except the first parameter is a thread identifier rather than a window handle.</span></span> <span data-ttu-id="ca6d5-145">Sie können den Thread Bezeichner abrufen, indem Sie die [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-145">You can retrieve the thread identifier by calling the [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) function.</span></span>

<span data-ttu-id="ca6d5-146">Verwenden Sie die [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion, um eine Nachrichten Schleife zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-146">Use the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to exit a message loop.</span></span> <span data-ttu-id="ca6d5-147">**PostQuitMessage sendet** die [**WM \_**](wm-quit.md) -beendenden Nachricht an den derzeit ausgeführten Thread.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-147">**PostQuitMessage** posts the [**WM\_QUIT**](wm-quit.md) message to the currently executing thread.</span></span> <span data-ttu-id="ca6d5-148">Die Nachrichten Schleife des Threads wird beendet, und die Steuerung wird an das System zurückgegeben, wenn die **WM- \_** Beendungs Meldung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-148">The thread's message loop terminates and returns control to the system when it encounters the **WM\_QUIT** message.</span></span> <span data-ttu-id="ca6d5-149">Eine Anwendung ruft in der Regel **PostQuitMessage** als Antwort auf die WM-Lösch Meldung auf, wie im folgenden Beispiel gezeigt. [**\_**](wm-destroy.md)</span><span class="sxs-lookup"><span data-stu-id="ca6d5-149">An application usually calls **PostQuitMessage** in response to the [**WM\_DESTROY**](wm-destroy.md) message, as shown in the following example.</span></span>


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a><span data-ttu-id="ca6d5-150">Senden einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="ca6d5-150">Sending a Message</span></span>

<span data-ttu-id="ca6d5-151">Die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion wird verwendet, um eine Nachricht direkt an eine Fenster Prozedur zu senden.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-151">The [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function is used to send a message directly to a window procedure.</span></span> <span data-ttu-id="ca6d5-152">**SendMessage** Ruft eine Fenster Prozedur auf und wartet darauf, dass diese Prozedur die Nachricht verarbeitet und ein Ergebnis zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-152">**SendMessage** calls a window procedure and waits for that procedure to process the message and return a result.</span></span>

<span data-ttu-id="ca6d5-153">Eine Nachricht kann an jedes Fenster im System gesendet werden. alles, was erforderlich ist, ist ein Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-153">A message can be sent to any window in the system; all that is required is a window handle.</span></span> <span data-ttu-id="ca6d5-154">Das System verwendet das Handle, um zu bestimmen, welche Fenster Prozedur die Nachricht empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-154">The system uses the handle to determine which window procedure should receive the message.</span></span>

<span data-ttu-id="ca6d5-155">Vor dem Verarbeiten einer Nachricht, die möglicherweise von einem anderen Thread gesendet wurde, sollte eine Fenster Prozedur zuerst die [**insendmessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-155">Before processing a message that may have been sent from another thread, a window procedure should first call the [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) function.</span></span> <span data-ttu-id="ca6d5-156">Wenn diese Funktion " **true**" zurückgibt, sollte die Fenster Prozedur " [**replymess Age**](/windows/win32/api/winuser/nf-winuser-replymessage) " vor jeder Funktion aufgerufen werden, die bewirkt, dass der Thread die Steuerung übernimmt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-156">If this function returns **TRUE**, the window procedure should call [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) before any function that causes the thread to yield control, as shown in the following example.</span></span>


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



<span data-ttu-id="ca6d5-157">An Steuerelemente in einem Dialogfeld können eine Reihe von Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-157">A number of messages can be sent to controls in a dialog box.</span></span> <span data-ttu-id="ca6d5-158">Diese Steuerungs Meldungen legen die Darstellung, das Verhalten und den Inhalt von Steuerelementen fest oder rufen Informationen zu Steuerelementen ab.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-158">These control messages set the appearance, behavior, and content of controls or retrieve information about controls.</span></span> <span data-ttu-id="ca6d5-159">Beispielsweise kann die [**CB \_ AddString**](../controls/cb-addstring.md) -Nachricht eine Zeichenfolge zu einem Kombinations Feld hinzufügen, und die [**BM- \_ setcheck**](../controls/bm-setcheck.md) -Nachricht kann den Prüf Zustand eines Kontrollkästchens oder Options Felds festlegen.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-159">For example, the [**CB\_ADDSTRING**](../controls/cb-addstring.md) message can add a string to a combo box, and the [**BM\_SETCHECK**](../controls/bm-setcheck.md) message can set the check state of a check box or radio button.</span></span>

<span data-ttu-id="ca6d5-160">Verwenden Sie die [**SendDlgItemMess**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) -Funktion, um eine Nachricht an ein Steuerelement zu senden, und geben Sie dabei den Bezeichner des Steuer Elements und das Handle des Dialogfeld Fensters an, das das Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-160">Use the [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) function to send a message to a control, specifying the identifier of the control and the handle of the dialog box window that contains the control.</span></span> <span data-ttu-id="ca6d5-161">Im folgenden Beispiel, das aus einer Dialogfeld Prozedur stammt, wird eine Zeichenfolge aus dem Bearbeitungs Steuerelement eines Kombinations Felds in das Listenfeld kopiert.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-161">The following example, taken from a dialog box procedure, copies a string from a combo box's edit control into its list box.</span></span> <span data-ttu-id="ca6d5-162">Das Beispiel verwendet **SendDlgItemMess** , um eine [**CB \_ AddString**](../controls/cb-addstring.md) -Nachricht an das Kombinations Feld zu senden.</span><span class="sxs-lookup"><span data-stu-id="ca6d5-162">The example uses **SendDlgItemMessage** to send a [**CB\_ADDSTRING**](../controls/cb-addstring.md) message to the combo box.</span></span>


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
