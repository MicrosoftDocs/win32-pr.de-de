---
description: Implementieren Sie Multitasking, planen Sie Prioritäten, und arbeiten Sie mit Prozessen, Threads, Thread Pools, Auftrags Objekten und Fibers. Planen Sie Threads mithilfe der benutzermodusplanung.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Prozesse und Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367934"
---
# <a name="processes-and-threads"></a><span data-ttu-id="769ee-104">Prozesse und Threads</span><span class="sxs-lookup"><span data-stu-id="769ee-104">Processes and Threads</span></span>

<span data-ttu-id="769ee-105">Eine Anwendung besteht aus einem oder mehreren Prozessen.</span><span class="sxs-lookup"><span data-stu-id="769ee-105">An application consists of one or more processes.</span></span> <span data-ttu-id="769ee-106">Ein *Prozess* ist in den einfachsten Begriffen ein ausführendes Programm.</span><span class="sxs-lookup"><span data-stu-id="769ee-106">A *process*, in the simplest terms, is an executing program.</span></span> <span data-ttu-id="769ee-107">Mindestens ein Thread wird im Kontext des Prozesses ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="769ee-107">One or more threads run in the context of the process.</span></span> <span data-ttu-id="769ee-108">Ein *Thread* ist die Basiseinheit, der die Prozessorzeit vom Betriebssystem zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="769ee-108">A *thread* is the basic unit to which the operating system allocates processor time.</span></span> <span data-ttu-id="769ee-109">Ein Thread kann einen beliebigen Teil des Prozess Codes ausführen, einschließlich der Teile, die gerade von einem anderen Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="769ee-109">A thread can execute any part of the process code, including parts currently being executed by another thread.</span></span>

<span data-ttu-id="769ee-110">Ein *Auftrags Objekt* ermöglicht das Verwalten von Gruppen von Prozessen als Einheit.</span><span class="sxs-lookup"><span data-stu-id="769ee-110">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="769ee-111">Auftrags Objekte sind namable-, Securable-und freigegeben-Objekte, die Attribute der zugeordneten Prozesse steuern.</span><span class="sxs-lookup"><span data-stu-id="769ee-111">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="769ee-112">Die für das Auftrags Objekt ausgeführten Vorgänge wirken sich auf alle Prozesse aus, die dem Auftrags Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="769ee-112">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="769ee-113">Ein *Thread Pool* ist eine Sammlung von Arbeitsthreads, die im Auftrag der Anwendung asynchrone Rückrufe effizient ausführen.</span><span class="sxs-lookup"><span data-stu-id="769ee-113">A *thread pool* is a collection of worker threads that efficiently execute asynchronous callbacks on behalf of the application.</span></span> <span data-ttu-id="769ee-114">Der Thread Pool wird hauptsächlich verwendet, um die Anzahl der Anwendungsthreads zu verringern und die Verwaltung der Arbeitsthreads zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="769ee-114">The thread pool is primarily used to reduce the number of application threads and provide management of the worker threads.</span></span>

<span data-ttu-id="769ee-115">Eine *Fiber* ist eine Ausführungs Einheit, die manuell von der Anwendung geplant werden muss.</span><span class="sxs-lookup"><span data-stu-id="769ee-115">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="769ee-116">Fibers werden im Kontext der Threads ausgeführt, die Sie planen.</span><span class="sxs-lookup"><span data-stu-id="769ee-116">Fibers run in the context of the threads that schedule them.</span></span>

<span data-ttu-id="769ee-117">Die *benutzermodusplanung* (ums) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können.</span><span class="sxs-lookup"><span data-stu-id="769ee-117">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="769ee-118">UMS-Threads unterscheiden sich von [Fibers](fibers.md) darin, dass jeder ums-Thread über einen eigenen Thread Kontext verfügt, anstatt den Thread Kontext eines einzelnen Threads gemeinsam zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="769ee-118">UMS threads differ from [fibers](fibers.md) in that each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span>

-   [<span data-ttu-id="769ee-119">Neues bei Prozessen und Threads</span><span class="sxs-lookup"><span data-stu-id="769ee-119">What's New in Processes and Threads</span></span>](what-s-new-in-processes-and-threads.md)
-   [<span data-ttu-id="769ee-120">About Processes and Threads (Informationen zu Prozessen und Threads)</span><span class="sxs-lookup"><span data-stu-id="769ee-120">About Processes and Threads</span></span>](about-processes-and-threads.md)
-   [<span data-ttu-id="769ee-121">Verwenden von Prozessen und Threads</span><span class="sxs-lookup"><span data-stu-id="769ee-121">Using Processes and Threads</span></span>](using-processes-and-threads.md)
-   [<span data-ttu-id="769ee-122">Prozess-und Thread Verweis</span><span class="sxs-lookup"><span data-stu-id="769ee-122">Process and Thread Reference</span></span>](process-and-thread-reference.md)

 

 



