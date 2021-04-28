---
title: Schreiben der Fensterprozedur
description: Schreiben der Fensterprozedur
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105718"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="fa8ec-103">Schreiben der Fensterprozedur</span><span class="sxs-lookup"><span data-stu-id="fa8ec-103">Writing the Window Procedure</span></span>

<span data-ttu-id="fa8ec-104">Die [**DispatchMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) ruft die Fensterprozedur des Fensters auf, das das Ziel der Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="fa8ec-105">Die Fensterprozedur weist die folgende Signatur auf.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="fa8ec-106">Es gibt vier Parameter:</span><span class="sxs-lookup"><span data-stu-id="fa8ec-106">There are four parameters:</span></span>

- <span data-ttu-id="fa8ec-107">*hwnd* ist ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="fa8ec-108">*uMsg* ist der Nachrichtencode. Beispielsweise gibt die [**WM \_ SIZE-Meldung**](/windows/desktop/winmsg/wm-size) an, dass die Größe des Fensters geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="fa8ec-109">*wParam* und *lParam* enthalten zusätzliche Daten, die sich auf die Nachricht beziehen.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="fa8ec-110">Die genaue Bedeutung hängt vom Nachrichtencode ab.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="fa8ec-111">**LRESULT** ist ein ganzzahliger Wert, den Ihr Programm an Windows zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="fa8ec-112">Sie enthält die Antwort Ihres Programms auf eine bestimmte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="fa8ec-113">Die Bedeutung dieses Werts hängt vom Nachrichtencode ab.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="fa8ec-114">**CALLBACK** ist die Aufrufkonvention für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="fa8ec-115">Eine typische Fensterprozedur ist einfach eine große switch-Anweisung, die den Nachrichtencode einschaltet.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="fa8ec-116">Fügen Sie Fälle für jede Nachricht hinzu, die Sie behandeln möchten.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="fa8ec-117">Zusätzliche Daten für die Nachricht sind in den *Parametern lParam* und *wParam* enthalten.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="fa8ec-118">Beide Parameter sind ganzzahlige Werte der Größe einer Zeigerbreite (32 Bits oder 64 Bits).</span><span class="sxs-lookup"><span data-stu-id="fa8ec-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="fa8ec-119">Die Bedeutung der einzelnen Hängt vom Nachrichtencode *(uMsg*) ab.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="fa8ec-120">Für jede Nachricht müssen Sie den Nachrichtencode auf MSDN suchen und die Parameter in den richtigen Datentyp umschreiben.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="fa8ec-121">In der Regel sind die Daten entweder ein numerischer Wert oder ein Zeiger auf eine Struktur.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="fa8ec-122">Einige Nachrichten enthalten keine Daten.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-122">Some messages do not have any data.</span></span>

<span data-ttu-id="fa8ec-123">In der Dokumentation für die [**WM \_ SIZE-Meldung**](/windows/desktop/winmsg/wm-size) wird beispielsweise Folgendes angezeigt:</span><span class="sxs-lookup"><span data-stu-id="fa8ec-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="fa8ec-124">*wParam ist* ein Flag, das angibt, ob das Fenster minimiert, maximiert oder die Größe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="fa8ec-125">*lParam* enthält die neue Breite und Höhe des Fensters als 16-Bit-Werte, die in eine 32- oder 64-Bit-Zahl gepackt sind.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="fa8ec-126">Sie müssen einige Bitverschiebungen durchführen, um diese Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="fa8ec-127">Glücklicherweise enthält die Headerdatei WinDef.h Hilfsmakros, die dies tun.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="fa8ec-128">Eine typische Fensterprozedur verarbeitet Dutzende von Nachrichten, sodass sie sehr lang werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="fa8ec-129">Eine Möglichkeit, Ihren Code modularer zu machen, besteht in der Logik für die Behandlung jeder Nachricht in einer separaten Funktion.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="fa8ec-130">Geben Sie in der Fensterprozedur die *Parameter wParam* und *lParam* in den richtigen Datentyp um, und übergeben Sie diese Werte an die Funktion.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="fa8ec-131">Um beispielsweise die WM [**\_ SIZE-Meldung zu**](/windows/desktop/winmsg/wm-size) verarbeiten, sieht die Fensterprozedur wie die folgende aus:</span><span class="sxs-lookup"><span data-stu-id="fa8ec-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

<span data-ttu-id="fa8ec-132">Die [**MAKROs LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) erhalten die Werte für Breite und Höhe von 16 Bit aus *lParam.*</span><span class="sxs-lookup"><span data-stu-id="fa8ec-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="fa8ec-133">(Sie können diese Art von Details in der MSDN-Dokumentation für jeden Meldungscode nachschauen.) Die Fensterprozedur extrahiert die Breite und Höhe und übergibt diese Werte dann an die `OnSize` Funktion.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="fa8ec-134">Standardnachrichtenbehandlung</span><span class="sxs-lookup"><span data-stu-id="fa8ec-134">Default Message Handling</span></span>

<span data-ttu-id="fa8ec-135">Wenn Sie eine bestimmte Nachricht in Ihrer Fensterprozedur nicht verarbeiten, übergeben Sie die Nachrichtenparameter direkt an die [**DefWindowProc-Funktion.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)</span><span class="sxs-lookup"><span data-stu-id="fa8ec-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="fa8ec-136">Diese Funktion führt die Standardaktion für die Nachricht aus, die je nach Nachrichtentyp variiert.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="fa8ec-137">Vermeiden von Engpässen in der Fensterprozedur</span><span class="sxs-lookup"><span data-stu-id="fa8ec-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="fa8ec-138">Während die Fensterprozedur ausgeführt wird, werden alle anderen Meldungen für Fenster blockiert, die im selben Thread erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="fa8ec-139">Vermeiden Sie daher eine lange Verarbeitung innerhalb der Fensterprozedur.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="fa8ec-140">Angenommen, Ihr Programm öffnet eine TCP-Verbindung und wartet unbegrenzt, bis der Server antwortet.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="fa8ec-141">Wenn Sie dies innerhalb der Fensterprozedur tun, antwortet Die Benutzeroberfläche erst, wenn die Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="fa8ec-142">Während dieser Zeit kann das Fenster keine Maus- oder Tastatureingaben verarbeiten, sich selbst neu malen oder sogar schließen.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="fa8ec-143">Stattdessen sollten Sie die Arbeit in einen anderen Thread verschieben, indem Sie eine der in Windows integrierten Multitasking-Einrichtungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="fa8ec-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="fa8ec-144">Erstellen Sie einen neuen Thread.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-144">Create a new thread.</span></span>
- <span data-ttu-id="fa8ec-145">Verwenden von Threadpools.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-145">Use a thread pool.</span></span>
- <span data-ttu-id="fa8ec-146">Verwenden Sie asynchrone E/A-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="fa8ec-147">Verwenden Sie asynchrone Prozeduraufrufe.</span><span class="sxs-lookup"><span data-stu-id="fa8ec-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="fa8ec-148">Nächste</span><span class="sxs-lookup"><span data-stu-id="fa8ec-148">Next</span></span>

[<span data-ttu-id="fa8ec-149">Zeichnen des Fensters</span><span class="sxs-lookup"><span data-stu-id="fa8ec-149">Painting the Window</span></span>](painting-the-window.md)
