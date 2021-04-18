---
description: Der Scheduler verwaltet eine Warteschlange mit ausführbaren Threads für jede Prioritätsstufe.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Kontextwechsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216019"
---
# <a name="context-switches"></a><span data-ttu-id="21ee5-103">Kontextwechsel</span><span class="sxs-lookup"><span data-stu-id="21ee5-103">Context Switches</span></span>

<span data-ttu-id="21ee5-104">Der Scheduler verwaltet eine Warteschlange mit ausführbaren Threads für jede Prioritätsstufe.</span><span class="sxs-lookup"><span data-stu-id="21ee5-104">The scheduler maintains a queue of executable threads for each priority level.</span></span> <span data-ttu-id="21ee5-105">Diese werden als *bereite Threads* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="21ee5-105">These are known as *ready threads*.</span></span> <span data-ttu-id="21ee5-106">Wenn ein Prozessor verfügbar wird, führt das System einen *Kontextwechsel* aus.</span><span class="sxs-lookup"><span data-stu-id="21ee5-106">When a processor becomes available, the system performs a *context switch*.</span></span> <span data-ttu-id="21ee5-107">Die Schritte in einem Kontextwechsel lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="21ee5-107">The steps in a context switch are:</span></span>

1.  <span data-ttu-id="21ee5-108">Speichern Sie den Kontext des Threads, der gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21ee5-108">Save the context of the thread that just finished executing.</span></span>
2.  <span data-ttu-id="21ee5-109">Platzieren Sie den soeben ausgeführten Thread am Ende der Warteschlange für seine Priorität.</span><span class="sxs-lookup"><span data-stu-id="21ee5-109">Place the thread that just finished executing at the end of the queue for its priority.</span></span>
3.  <span data-ttu-id="21ee5-110">Suchen Sie die Warteschlange mit der höchsten Priorität, die bereite Threads enthält.</span><span class="sxs-lookup"><span data-stu-id="21ee5-110">Find the highest priority queue that contains ready threads.</span></span>
4.  <span data-ttu-id="21ee5-111">Entfernen Sie den Thread am Anfang der Warteschlange, laden Sie seinen Kontext, und führen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="21ee5-111">Remove the thread at the head of the queue, load its context, and execute it.</span></span>

<span data-ttu-id="21ee5-112">Bei den folgenden Thread Klassen handelt es sich nicht um bereite Threads.</span><span class="sxs-lookup"><span data-stu-id="21ee5-112">The following classes of threads are not ready threads.</span></span>

-   <span data-ttu-id="21ee5-113">Mit dem Flag zum Erstellen von angehaltenen Threads erstellte Threads \_</span><span class="sxs-lookup"><span data-stu-id="21ee5-113">Threads created with the CREATE\_SUSPENDED flag</span></span>
-   <span data-ttu-id="21ee5-114">Threads, die während der Ausführung mit der [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) -oder [**SwitchTo Thread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) -Funktion angehalten wurden</span><span class="sxs-lookup"><span data-stu-id="21ee5-114">Threads halted during execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function</span></span>
-   <span data-ttu-id="21ee5-115">Threads, die auf ein Synchronisierungs Objekt oder eine Eingabe warten.</span><span class="sxs-lookup"><span data-stu-id="21ee5-115">Threads waiting for a synchronization object or input.</span></span>

<span data-ttu-id="21ee5-116">Bis die Threads, die angehalten oder blockiert werden, ausgeführt werden können, weist der Planer unabhängig von ihrer Priorität keine Prozessorzeit zu.</span><span class="sxs-lookup"><span data-stu-id="21ee5-116">Until threads that are suspended or blocked become ready to run, the scheduler does not allocate any processor time to them, regardless of their priority.</span></span>

<span data-ttu-id="21ee5-117">Die häufigsten Gründe für einen Kontextwechsel sind:</span><span class="sxs-lookup"><span data-stu-id="21ee5-117">The most common reasons for a context switch are:</span></span>

-   <span data-ttu-id="21ee5-118">Der Zeit Slice ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="21ee5-118">The time slice has elapsed.</span></span>
-   <span data-ttu-id="21ee5-119">Ein Thread mit einer höheren Priorität ist für die Durchführung bereit.</span><span class="sxs-lookup"><span data-stu-id="21ee5-119">A thread with a higher priority has become ready to run.</span></span>
-   <span data-ttu-id="21ee5-120">Ein laufender Thread muss warten.</span><span class="sxs-lookup"><span data-stu-id="21ee5-120">A running thread needs to wait.</span></span>

<span data-ttu-id="21ee5-121">Wenn ein laufender Thread warten muss, wird der restliche Zeit Slice aufgegeben.</span><span class="sxs-lookup"><span data-stu-id="21ee5-121">When a running thread needs to wait, it relinquishes the remainder of its time slice.</span></span>

 

 
