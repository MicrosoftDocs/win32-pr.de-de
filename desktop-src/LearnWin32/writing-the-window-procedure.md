---
title: Schreiben der Fenster Prozedur
description: .
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f11b22ba5dd0653905ca4e2bdb546d106183fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339480"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="2f3b5-103">Schreiben der Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="2f3b5-103">Writing the Window Procedure</span></span>

<span data-ttu-id="2f3b5-104">Die [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) -Funktion Ruft die Fenster Prozedur des Fensters auf, das das Ziel der Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="2f3b5-105">Die Fenster Prozedur weist die folgende Signatur auf.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="2f3b5-106">Es gibt vier Parameter:</span><span class="sxs-lookup"><span data-stu-id="2f3b5-106">There are four parameters:</span></span>

- <span data-ttu-id="2f3b5-107">*HWND* ist ein Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="2f3b5-108">die *Umschlag* Sequenz ist der Nachrichten Code. Beispielsweise gibt die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Meldung an, dass die Größe des Fensters angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="2f3b5-109">*wParam* und *LPARAM* enthalten zusätzliche Daten, die sich auf die Nachricht beziehen.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="2f3b5-110">Die genaue Bedeutung hängt vom Nachrichten Code ab.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="2f3b5-111">**LRESULT** ist ein ganzzahliger Wert, den das Programm an Windows zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="2f3b5-112">Sie enthält die Antwort des Programms auf eine bestimmte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="2f3b5-113">Die Bedeutung dieses Werts hängt vom Nachrichten Code ab.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="2f3b5-114">**Callback** ist die Aufruf Konvention für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="2f3b5-115">Eine typische Fenster Prozedur ist einfach eine große Switch-Anweisung, die den Nachrichten Code schaltet.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="2f3b5-116">Fügen Sie für jede zu behandelnde Nachricht Fälle hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="2f3b5-117">Zusätzliche Daten für die Nachricht sind in den *LPARAM* -und *wParam* -Parametern enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="2f3b5-118">Beide Parameter sind ganzzahlige Werte die Größe einer Zeiger Breite (32 Bits oder 64 Bits).</span><span class="sxs-lookup"><span data-stu-id="2f3b5-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="2f3b5-119">Die Bedeutung der einzelnen hängt vom Nachrichten Code (*Umschlag*) ab.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="2f3b5-120">Für jede Nachricht müssen Sie den Nachrichten Code auf MSDN suchen und die Parameter in den richtigen Datentyp umwandeln.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="2f3b5-121">Normalerweise handelt es sich bei den Daten entweder um einen numerischen Wert oder um einen Zeiger auf eine-Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="2f3b5-122">Einige Nachrichten enthalten keine Daten.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-122">Some messages do not have any data.</span></span>

<span data-ttu-id="2f3b5-123">In der Dokumentation für die WM- [**\_ Größe**](/windows/desktop/winmsg/wm-size) wird beispielsweise Folgendes angezeigt:</span><span class="sxs-lookup"><span data-stu-id="2f3b5-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="2f3b5-124">*wParam* ist ein Flag, das angibt, ob das Fenster minimiert, maximiert oder verkleinert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="2f3b5-125">*LPARAM* enthält die neue Breite und Höhe des Fensters als 16-Bit-Werte, die in 1 32-oder 64-Bit-Zahlen verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="2f3b5-126">Sie müssen einige Bitverschiebungen durchführen, um diese Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="2f3b5-127">Glücklicherweise enthält die Header Datei WINDEF. h Hilfsmakros, die dies tun.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="2f3b5-128">Eine typische Fenster Prozedur verarbeitet Dutzende von Nachrichten, sodass Sie sehr lange anwachsen kann.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="2f3b5-129">Eine Möglichkeit, Ihren Code modularerer zu gestalten, besteht darin, die Logik für die Verarbeitung der einzelnen Nachrichten in einer separaten Funktion zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="2f3b5-130">Wandeln Sie in der Fenster Prozedur die *wParam* -und *LPARAM* -Parameter in den richtigen Datentyp um, und übergeben Sie diese Werte an die-Funktion.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="2f3b5-131">Um z. b. die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Meldung zu verarbeiten, würde die Fenster Prozedur wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="2f3b5-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

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

<span data-ttu-id="2f3b5-132">Die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -und [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros erhalten die 16-Bit-Werte für Breite und Höhe von *LPARAM*.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="2f3b5-133">(In der MSDN-Dokumentation finden Sie Informationen zu den einzelnen Nachrichten Codes.) Die Fenster Prozedur extrahiert die Breite und Höhe und übergibt diese Werte dann an die `OnSize` Funktion.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="2f3b5-134">Standardmäßige Nachrichten Behandlung</span><span class="sxs-lookup"><span data-stu-id="2f3b5-134">Default Message Handling</span></span>

<span data-ttu-id="2f3b5-135">Wenn Sie eine bestimmte Nachricht in der Fenster Prozedur nicht verarbeiten, übergeben Sie die Nachrichten Parameter direkt an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="2f3b5-136">Diese Funktion führt die Standardaktion für die Nachricht aus, die je nach Nachrichtentyp variiert.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="2f3b5-137">Vermeiden von Engpässen in der Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="2f3b5-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="2f3b5-138">Während die Fenster Prozedur ausgeführt wird, werden alle anderen Nachrichten für Windows, die im gleichen Thread erstellt wurden, blockiert.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="2f3b5-139">Vermeiden Sie daher eine lange Verarbeitung in der Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="2f3b5-140">Angenommen, das Programm öffnet eine TCP-Verbindung und wartet unbegrenzt, bis der Server antwortet.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="2f3b5-141">Wenn Sie dies innerhalb der Fenster Prozedur tun, antwortet die Benutzeroberfläche erst, wenn die Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="2f3b5-142">Während dieser Zeit kann das Fenster keine Maus-oder Tastatureingaben verarbeiten, sich selbst neu zeichnen oder sogar schließen.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="2f3b5-143">Stattdessen sollten Sie die Arbeit in einen anderen Thread verschieben. verwenden Sie dazu eine der in Windows integrierten Multitasking-Funktionen:</span><span class="sxs-lookup"><span data-stu-id="2f3b5-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="2f3b5-144">Erstellen Sie einen neuen Thread.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-144">Create a new thread.</span></span>
- <span data-ttu-id="2f3b5-145">Verwenden von Threadpools.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-145">Use a thread pool.</span></span>
- <span data-ttu-id="2f3b5-146">Verwenden Sie asynchrone e/a-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="2f3b5-147">Verwenden Sie asynchrone Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="2f3b5-148">Nächste</span><span class="sxs-lookup"><span data-stu-id="2f3b5-148">Next</span></span>

[<span data-ttu-id="2f3b5-149">Zeichnen des Fensters</span><span class="sxs-lookup"><span data-stu-id="2f3b5-149">Painting the Window</span></span>](painting-the-window.md)