---
description: Warn Bare e/a ist die Methode, mit der Anwendungsthreads asynchrone e/a-Anforderungen verarbeiten, wenn Sie sich in einem wartungstabellenzustand befinden.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: Warn Bare e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347026"
---
# <a name="alertable-io"></a><span data-ttu-id="5fe19-103">Warn Bare e/a</span><span class="sxs-lookup"><span data-stu-id="5fe19-103">Alertable I/O</span></span>

<span data-ttu-id="5fe19-104">Warn Bare e/a ist die Methode, mit der Anwendungsthreads asynchrone e/a-Anforderungen verarbeiten, wenn Sie sich in einem wartungstabellenzustand befinden.</span><span class="sxs-lookup"><span data-stu-id="5fe19-104">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span>

<span data-ttu-id="5fe19-105">Um zu verstehen, wenn sich ein Thread in einem Warn baren Zustand befindet, sollten Sie das folgende Szenario in Erwägung ziehen:</span><span class="sxs-lookup"><span data-stu-id="5fe19-105">To understand when a thread is in an alertable state, consider the following scenario:</span></span>

1.  <span data-ttu-id="5fe19-106">Ein Thread initiiert eine asynchrone Lese Anforderung durch Aufrufen von " [**lesefileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " mit einem Zeiger auf eine Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="5fe19-106">A thread initiates an asynchronous read request by calling [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) with a pointer to a callback function.</span></span>
2.  <span data-ttu-id="5fe19-107">Der Thread initiiert eine asynchrone Schreib Anforderung, indem er "Write [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) " mit einem Zeiger auf eine Rückruffunktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="5fe19-107">The thread initiates an asynchronous write request by calling [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) with a pointer to a callback function.</span></span>
3.  <span data-ttu-id="5fe19-108">Der Thread ruft eine Funktion auf, die eine Zeile mit Daten von einem Remote-Datenbankserver abruft.</span><span class="sxs-lookup"><span data-stu-id="5fe19-108">The thread calls a function that fetches a row of data from a remote database server.</span></span>

<span data-ttu-id="5fe19-109">In diesem Szenario werden die Aufrufe von "read [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " und " [**schreitefileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) " wahrscheinlich vor dem Funktionsaufruf in Schritt 3 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5fe19-109">In this scenario, the calls to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) will most likely return before the function call in step 3.</span></span> <span data-ttu-id="5fe19-110">Wenn dies der Fall ist, platziert der Kernel die Zeiger auf die Rückruf Funktionen in der asynchronen Prozedur aufrufswarteschlange (APC) des Threads.</span><span class="sxs-lookup"><span data-stu-id="5fe19-110">When they do, the kernel places the pointers to the callback functions on the thread's Asynchronous Procedure Call (APC) queue.</span></span> <span data-ttu-id="5fe19-111">Der Kernel verwaltet diese Warteschlange speziell zum Speichern zurückgegebener e/a-Anforderungs Daten, bis Sie vom entsprechenden Thread verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fe19-111">The kernel maintains this queue specifically to hold returned I/O request data until it can be processed by the corresponding thread.</span></span>

<span data-ttu-id="5fe19-112">Wenn das Abrufen der Zeile beendet ist und der Thread von der Funktion zurückgegeben wird, besteht die höchste Priorität darin, die zurückgegebenen e/a-Anforderungen in der Warteschlange zu verarbeiten, indem die Rückruf Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5fe19-112">When the row fetch is complete and the thread returns from the function, its highest priority is to process the returned I/O requests on the queue by calling the callback functions.</span></span> <span data-ttu-id="5fe19-113">Zu diesem Zweck muss ein Warn Tabellen Status eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5fe19-113">To do this, it must enter an alertable state.</span></span> <span data-ttu-id="5fe19-114">Ein Thread kann dies nur durch Aufrufen einer der folgenden Funktionen mit den entsprechenden Flags erreichen:</span><span class="sxs-lookup"><span data-stu-id="5fe19-114">A thread can only do this by calling one of the following functions with the appropriate flags:</span></span>

-   [<span data-ttu-id="5fe19-115">**SleepEx**</span><span class="sxs-lookup"><span data-stu-id="5fe19-115">**SleepEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [<span data-ttu-id="5fe19-116">**WaitForSingleObjectEx**</span><span class="sxs-lookup"><span data-stu-id="5fe19-116">**WaitForSingleObjectEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [<span data-ttu-id="5fe19-117">**WaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="5fe19-117">**WaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [<span data-ttu-id="5fe19-118">**Signalobjectandwait**</span><span class="sxs-lookup"><span data-stu-id="5fe19-118">**SignalObjectAndWait**</span></span>](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [<span data-ttu-id="5fe19-119">**MsgWaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="5fe19-119">**MsgWaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

<span data-ttu-id="5fe19-120">Wenn der Thread in einen Warn baren Status wechselt, treten die folgenden Ereignisse auf:</span><span class="sxs-lookup"><span data-stu-id="5fe19-120">When the thread enters an alertable state, the following events occur:</span></span>

1.  <span data-ttu-id="5fe19-121">Der Kernel überprüft die APC-Warteschlange des Threads.</span><span class="sxs-lookup"><span data-stu-id="5fe19-121">The kernel checks the thread's APC queue.</span></span> <span data-ttu-id="5fe19-122">Wenn die Warteschlange Rückruf Funktionszeiger enthält, entfernt der Kernel den Zeiger aus der Warteschlange und sendet ihn an den Thread.</span><span class="sxs-lookup"><span data-stu-id="5fe19-122">If the queue contains callback function pointers, the kernel removes the pointer from the queue and sends it to the thread.</span></span>
2.  <span data-ttu-id="5fe19-123">Der Thread führt die Rückruffunktion aus.</span><span class="sxs-lookup"><span data-stu-id="5fe19-123">The thread executes the callback function.</span></span>
3.  <span data-ttu-id="5fe19-124">Die Schritte 1 und 2 werden für jeden Zeiger wiederholt, der in der Warteschlange verbleiben.</span><span class="sxs-lookup"><span data-stu-id="5fe19-124">Steps 1 and 2 are repeated for each pointer remaining in the queue.</span></span>
4.  <span data-ttu-id="5fe19-125">Wenn die Warteschlange leer ist, gibt der Thread von der Funktion zurück, die ihn in einen Warn baren Zustand versetzt hat.</span><span class="sxs-lookup"><span data-stu-id="5fe19-125">When the queue is empty, the thread returns from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="5fe19-126">Wenn der Thread in diesem Szenario in einen wartungstabellenzustand wechselt, ruft er die an " [**getfileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " und " [**Write fileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)" gesendeten Rückruf Funktionen auf und gibt dann von der Funktion zurück, die ihn in einen Warn baren Zustand versetzt hat.</span><span class="sxs-lookup"><span data-stu-id="5fe19-126">In this scenario, once the thread enters an alertable state it will call the callback functions sent to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), then return from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="5fe19-127">Wenn ein Thread in einen Warn baren Zustand wechselt, während die zugehörige APC-Warteschlange leer ist, wird die Ausführung des Threads vom Kernel angehalten, bis eine der folgenden Aktionen auftritt:</span><span class="sxs-lookup"><span data-stu-id="5fe19-127">If a thread enters an alertable state while its APC queue is empty, the thread's execution will be suspended by the kernel until one of the following occurs:</span></span>

-   <span data-ttu-id="5fe19-128">Das Kernel Objekt, auf das gewartet wird, wird signalisiert.</span><span class="sxs-lookup"><span data-stu-id="5fe19-128">The kernel object that is being waited on becomes signaled.</span></span>
-   <span data-ttu-id="5fe19-129">Ein Rückruf Funktionszeiger wird in die APC-Warteschlange eingefügt.</span><span class="sxs-lookup"><span data-stu-id="5fe19-129">A callback function pointer is placed in the APC queue.</span></span>

<span data-ttu-id="5fe19-130">Ein Thread, der Warn Bare e/a-Vorgänge verwendet, verarbeitet asynchrone e/a-Anforderungen effizienter als bei der einfachen Wartezeit auf das ereignisflag in der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur, und der Warnbare e/a-Mechanismus ist weniger kompliziert als die zu verwendenden e/a-Abschlussports. [](i-o-completion-ports.md)</span><span class="sxs-lookup"><span data-stu-id="5fe19-130">A thread that uses alertable I/O processes asynchronous I/O requests more efficiently than when they simply wait on the event flag in the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to be set, and the alertable I/O mechanism is less complicated than [I/O completion ports](i-o-completion-ports.md) to use.</span></span> <span data-ttu-id="5fe19-131">Allerdings wird das Ergebnis der e/a-Anforderung nur an den Thread zurückgegeben, der die e/a-Anforderung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="5fe19-131">However, alertable I/O returns the result of the I/O request only to the thread that initiated it.</span></span> <span data-ttu-id="5fe19-132">Für e/a-Abschlussports gilt diese Einschränkung nicht.</span><span class="sxs-lookup"><span data-stu-id="5fe19-132">I/O completion ports do not have this limitation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fe19-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fe19-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fe19-134">Asynchrone Prozedur Aufrufe</span><span class="sxs-lookup"><span data-stu-id="5fe19-134">Asynchronous Procedure Calls</span></span>](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
