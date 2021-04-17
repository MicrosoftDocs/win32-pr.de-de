---
description: Die Funktion "kreatethread" erstellt einen neuen Thread für einen Prozess.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Thread Funktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523672"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="ae9fb-103">Thread Funktionen für das Debuggen</span><span class="sxs-lookup"><span data-stu-id="ae9fb-103">Thread Functions for Debugging</span></span>

<span data-ttu-id="ae9fb-104">Die Funktion " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " erstellt einen neuen Thread für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="ae9fb-105">Debuggger müssen in der Regel den Inhalt der Register eines Threads überprüfen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-105">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="ae9fb-106">Um dies zu erreichen, muss ein Debugger ein Handle für den Thread abrufen, indem er die [**duplialisiehandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion verwendet und den entsprechenden Zugriff auf den Thread (Thread Abruf \_ \_ Kontext, Thread \_ Satz \_ Kontext oder beides) angibt.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-106">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="ae9fb-107">Die [**openthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) -Funktion ermöglicht einem Debugger das Abrufen des Bezeichners eines vorhandenen Threads.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-107">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="ae9fb-108">Ein Prozess mit geeigneendem Zugriff auf einen Thread kann die Register des Threads mithilfe der [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) -Funktion untersuchen und den Inhalt der Register des Threads mithilfe der [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) -Funktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-108">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="ae9fb-109">Ein Prozess kann auch den Thread \_ Suspend \_ anhaltezugriff auf einen Thread erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-109">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="ae9fb-110">Diese Art von Zugriff ermöglicht einem Debugger, die Ausführung eines Threads mit den Funktionen " [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) " und " [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) " zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-110">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="ae9fb-111">Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="ae9fb-111">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
