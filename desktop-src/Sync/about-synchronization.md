---
description: Verwenden Sie zum Synchronisieren des Zugriffs auf eine Ressource eines der Synchronisierungs Objekte in einer der Warte Funktionen.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Informationen zur Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352206"
---
# <a name="about-synchronization"></a><span data-ttu-id="78ab2-103">Informationen zur Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="78ab2-103">About Synchronization</span></span>

<span data-ttu-id="78ab2-104">Verwenden Sie zum Synchronisieren des Zugriffs auf eine Ressource eines der [Synchronisierungs Objekte](synchronization-objects.md) in einer der [warte Funktionen](wait-functions.md).</span><span class="sxs-lookup"><span data-stu-id="78ab2-104">To synchronize access to a resource, use one of the [synchronization objects](synchronization-objects.md) in one of the [wait functions](wait-functions.md).</span></span> <span data-ttu-id="78ab2-105">Der Status eines Synchronisierungs Objekts wird entweder *signalisiert* oder *nicht signalisiert*.</span><span class="sxs-lookup"><span data-stu-id="78ab2-105">The state of a synchronization object is either *signaled* or *nonsignaled*.</span></span> <span data-ttu-id="78ab2-106">Mit den Wait-Funktionen kann ein Thread seine eigene Ausführung blockieren, bis ein angegebenes nicht signalisiertes Objekt auf den signalisierten Zustand festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="78ab2-106">The wait functions allow a thread to block its own execution until a specified nonsignaled object is set to the signaled state.</span></span> <span data-ttu-id="78ab2-107">Weitere Informationen finden Sie unter [prozessübergreifende Synchronisierung](interprocess-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="78ab2-107">For more information, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

<span data-ttu-id="78ab2-108">Im folgenden werden andere Synchronisierungs Mechanismen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="78ab2-108">The following are other synchronization mechanisms:</span></span>

-   [<span data-ttu-id="78ab2-109">überlappende Eingabe und Ausgabe</span><span class="sxs-lookup"><span data-stu-id="78ab2-109">overlapped input and output</span></span>](synchronization-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="78ab2-110">asynchrone Prozedur Aufrufe</span><span class="sxs-lookup"><span data-stu-id="78ab2-110">asynchronous procedure calls</span></span>](asynchronous-procedure-calls.md)
-   [<span data-ttu-id="78ab2-111">kritische Abschnitts Objekte</span><span class="sxs-lookup"><span data-stu-id="78ab2-111">critical section objects</span></span>](critical-section-objects.md)
-   [<span data-ttu-id="78ab2-112">Bedingungsvariablen</span><span class="sxs-lookup"><span data-stu-id="78ab2-112">condition variables</span></span>](condition-variables.md)
-   [<span data-ttu-id="78ab2-113">schlanke Lese-/Schreibsperren</span><span class="sxs-lookup"><span data-stu-id="78ab2-113">slim reader/writer locks</span></span>](slim-reader-writer--srw--locks.md)
-   [<span data-ttu-id="78ab2-114">einmalige Initialisierung</span><span class="sxs-lookup"><span data-stu-id="78ab2-114">one-time initialization</span></span>](one-time-initialization.md)
-   [<span data-ttu-id="78ab2-115">Interlocked-Variablen Zugriff</span><span class="sxs-lookup"><span data-stu-id="78ab2-115">interlocked variable access</span></span>](interlocked-variable-access.md)
-   [<span data-ttu-id="78ab2-116">miteinander verknüpfte, einzeln verknüpfte Listen</span><span class="sxs-lookup"><span data-stu-id="78ab2-116">interlocked singly linked lists</span></span>](interlocked-singly-linked-lists.md)
-   [<span data-ttu-id="78ab2-117">Timer-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="78ab2-117">timer queues</span></span>](timer-queues.md)
-   <span data-ttu-id="78ab2-118">Das [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) -Makro</span><span class="sxs-lookup"><span data-stu-id="78ab2-118">the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) macro</span></span>

<span data-ttu-id="78ab2-119">Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisierung und Multiprozessorprobleme](synchronization-and-multiprocessor-issues.md).</span><span class="sxs-lookup"><span data-stu-id="78ab2-119">For additional information on synchronization, see [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).</span></span>

 

 
