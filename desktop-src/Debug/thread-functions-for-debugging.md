---
description: Erfahren Sie, wie Sie die CreateThread-Funktion verwenden, um einen neuen Thread für einen Prozess zu erstellen. Debugger müssen in der Regel den Inhalt der Register eines Threads untersuchen oder ändern.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Threadfunktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403983"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="2d95d-104">Threadfunktionen für das Debuggen</span><span class="sxs-lookup"><span data-stu-id="2d95d-104">Thread Functions for Debugging</span></span>

<span data-ttu-id="2d95d-105">Die [**CreateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) erstellt einen neuen Thread für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="2d95d-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="2d95d-106">Debugger müssen in der Regel den Inhalt der Register eines Threads untersuchen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="2d95d-106">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="2d95d-107">Dazu muss ein Debugger ein Handle für den Thread abrufen, indem er die [**DuplicateHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) verwendet und den entsprechenden Zugriff auf den Thread (THREAD \_ GET \_ CONTEXT, THREAD \_ SET CONTEXT \_ oder beides) angibt.</span><span class="sxs-lookup"><span data-stu-id="2d95d-107">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="2d95d-108">Mit der [**OpenThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) kann ein Debugger den Bezeichner eines vorhandenen Threads abrufen.</span><span class="sxs-lookup"><span data-stu-id="2d95d-108">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="2d95d-109">Ein Prozess mit entsprechendem Zugriff auf einen Thread kann die Register des Threads mithilfe der [**GetThreadContext-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) untersuchen und den Inhalt der Register des Threads mithilfe der [**SetThreadContext-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d95d-109">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="2d95d-110">Ein Prozess kann auch THREAD \_ SUSPEND \_ RESUME-Zugriff auf einen Thread erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d95d-110">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="2d95d-111">Dieser Zugriffstyp ermöglicht es einem Debugger, die Ausführung eines Threads mit den Funktionen [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) und [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2d95d-111">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="2d95d-112">Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads.](../procthread/processes-and-threads.md)</span><span class="sxs-lookup"><span data-stu-id="2d95d-112">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
