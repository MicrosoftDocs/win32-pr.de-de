---
description: Die Ausführung von Threads wird basierend auf Ihrer Planungs Priorität geplant.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Planen von Prioritäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356156"
---
# <a name="scheduling-priorities"></a><span data-ttu-id="43832-103">Planen von Prioritäten</span><span class="sxs-lookup"><span data-stu-id="43832-103">Scheduling Priorities</span></span>

<span data-ttu-id="43832-104">Die Ausführung von Threads wird basierend auf Ihrer *Planungs Priorität* geplant.</span><span class="sxs-lookup"><span data-stu-id="43832-104">Threads are scheduled to run based on their *scheduling priority*.</span></span> <span data-ttu-id="43832-105">Jedem Thread wird eine Planungs Priorität zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="43832-105">Each thread is assigned a scheduling priority.</span></span> <span data-ttu-id="43832-106">Die Prioritätsstufen liegen zwischen NULL (niedrigste Priorität) und 31 (höchste Priorität).</span><span class="sxs-lookup"><span data-stu-id="43832-106">The priority levels range from zero (lowest priority) to 31 (highest priority).</span></span> <span data-ttu-id="43832-107">Nur der Zero-page-Thread kann eine Priorität von 0 (null) haben.</span><span class="sxs-lookup"><span data-stu-id="43832-107">Only the zero-page thread can have a priority of zero.</span></span> <span data-ttu-id="43832-108">(Der Zero-page-Thread ist ein System Thread, der für das Nullen von freien Seiten zuständig ist, wenn keine anderen Threads ausgeführt werden müssen.)</span><span class="sxs-lookup"><span data-stu-id="43832-108">(The zero-page thread is a system thread responsible for zeroing any free pages when there are no other threads that need to run.)</span></span>

<span data-ttu-id="43832-109">Das System behandelt alle Threads mit der gleichen Priorität als gleich.</span><span class="sxs-lookup"><span data-stu-id="43832-109">The system treats all threads with the same priority as equal.</span></span> <span data-ttu-id="43832-110">Das System weist Zeit Scheiben in einer Roundrobin-Methode allen Threads mit der höchsten Priorität zu.</span><span class="sxs-lookup"><span data-stu-id="43832-110">The system assigns time slices in a round-robin fashion to all threads with the highest priority.</span></span> <span data-ttu-id="43832-111">Wenn keiner dieser Threads zur Laufzeit bereit ist, weist das Systemzeit Scheiben in einer Roundrobin-Methode allen Threads mit der nächsthöheren Priorität zu.</span><span class="sxs-lookup"><span data-stu-id="43832-111">If none of these threads are ready to run, the system assigns time slices in a round-robin fashion to all threads with the next highest priority.</span></span> <span data-ttu-id="43832-112">Wenn ein Thread mit höherer Priorität für die Ausführung verfügbar ist, beendet das System die Ausführung des Threads mit niedrigerer Priorität (ohne die Beendigung seines Zeitabschnitts zuzulassen) und weist dem Thread mit höherer Priorität einen vollen Zeit Slice zu.</span><span class="sxs-lookup"><span data-stu-id="43832-112">If a higher-priority thread becomes available to run, the system ceases to execute the lower-priority thread (without allowing it to finish using its time slice) and assigns a full time slice to the higher-priority thread.</span></span> <span data-ttu-id="43832-113">Weitere Informationen finden Sie unter [Kontext](context-switches.md)Wechsel.</span><span class="sxs-lookup"><span data-stu-id="43832-113">For more information, see [Context Switches](context-switches.md).</span></span>

<span data-ttu-id="43832-114">Die Priorität der einzelnen Threads wird durch die folgenden Kriterien bestimmt:</span><span class="sxs-lookup"><span data-stu-id="43832-114">The priority of each thread is determined by the following criteria:</span></span>

-   <span data-ttu-id="43832-115">Die Prioritäts Klasse des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="43832-115">The priority class of its process</span></span>
-   <span data-ttu-id="43832-116">Die Prioritäts Ebene des Threads innerhalb der Prioritäts Klasse des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="43832-116">The priority level of the thread within the priority class of its process</span></span>

<span data-ttu-id="43832-117">Die Prioritäts Klasse und die Prioritätsstufe werden kombiniert, um die *Basis Priorität* eines Threads zu bilden.</span><span class="sxs-lookup"><span data-stu-id="43832-117">The priority class and priority level are combined to form the *base priority* of a thread.</span></span> <span data-ttu-id="43832-118">Informationen zur dynamischen Priorität eines Threads finden Sie unter [Prioritäts Steigerungen](priority-boosts.md).</span><span class="sxs-lookup"><span data-stu-id="43832-118">For information on the dynamic priority of a thread, see [Priority Boosts](priority-boosts.md).</span></span>

## <a name="priority-class"></a><span data-ttu-id="43832-119">Prioritäts Klasse</span><span class="sxs-lookup"><span data-stu-id="43832-119">Priority Class</span></span>

<span data-ttu-id="43832-120">Jeder Prozess gehört zu einer der folgenden Prioritäts Klassen:</span><span class="sxs-lookup"><span data-stu-id="43832-120">Each process belongs to one of the following priority classes:</span></span><dl> <span data-ttu-id="43832-121">inaktive \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="43832-121">IDLE\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="43832-122">unterhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="43832-122">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="43832-123">Klasse der normalen \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="43832-123">NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="43832-124">oberhalb der \_ normalen \_ Prioritäts \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="43832-124">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="43832-125">Klasse mit hoher \_ Priorität \_</span><span class="sxs-lookup"><span data-stu-id="43832-125">HIGH\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="43832-126">Realtime \_ priority- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="43832-126">REALTIME\_PRIORITY\_CLASS</span></span>  
</dl>

<span data-ttu-id="43832-127">Standardmäßig ist die Prioritäts Klasse eines Prozesses normale \_ Prioritäts \_ Klasse.</span><span class="sxs-lookup"><span data-stu-id="43832-127">By default, the priority class of a process is NORMAL\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="43832-128">Verwenden Sie die Funktion "up- [**Process**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ", um die Prioritäts Klasse eines untergeordneten Prozesses anzugeben, wenn Sie Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="43832-128">Use the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function to specify the priority class of a child process when you create it.</span></span> <span data-ttu-id="43832-129">Wenn der aufrufende Prozess die \_ Prioritäts Klasse im Leerlauf \_ oder unter der \_ normalen \_ Prioritäts \_ Klasse ist, erbt der neue Prozess diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="43832-129">If the calling process is IDLE\_PRIORITY\_CLASS or BELOW\_NORMAL\_PRIORITY\_CLASS, the new process will inherit this class.</span></span> <span data-ttu-id="43832-130">Verwenden Sie die [**getpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) -Funktion, um die aktuelle Prioritäts Klasse eines Prozesses zu bestimmen, und die [**setpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) -Funktion, um die Prioritäts Klasse eines Prozesses zu ändern.</span><span class="sxs-lookup"><span data-stu-id="43832-130">Use the [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) function to determine the current priority class of a process and the [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) function to change the priority class of a process.</span></span>

<span data-ttu-id="43832-131">Prozesse, die das System überwachen, z. b. Bildschirmschoner oder Anwendungen, die in regelmäßigen Abständen eine Anzeige aktualisieren, sollten die Klasse mit der \_ Priorität " \_</span><span class="sxs-lookup"><span data-stu-id="43832-131">Processes that monitor the system, such as screen savers or applications that periodically update a display, should use IDLE\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="43832-132">Dadurch wird verhindert, dass die Threads dieses Prozesses, die keine hohe Priorität haben, von Threads mit höherer Priorität gestört werden.</span><span class="sxs-lookup"><span data-stu-id="43832-132">This prevents the threads of this process, which do not have high priority, from interfering with higher priority threads.</span></span>

<span data-ttu-id="43832-133">Verwenden Sie \_ die \_ Klasse mit hoher Priorität mit Bedacht.</span><span class="sxs-lookup"><span data-stu-id="43832-133">Use HIGH\_PRIORITY\_CLASS with care.</span></span> <span data-ttu-id="43832-134">Wenn ein Thread für erweiterte Zeiträume mit der höchsten Prioritätsstufe ausgeführt wird, erhalten andere Threads im System keine Prozessorzeit.</span><span class="sxs-lookup"><span data-stu-id="43832-134">If a thread runs at the highest priority level for extended periods, other threads in the system will not get processor time.</span></span> <span data-ttu-id="43832-135">Wenn mehrere Threads gleichzeitig mit hoher Priorität festgelegt werden, verlieren die Threads ihre Wirksamkeit.</span><span class="sxs-lookup"><span data-stu-id="43832-135">If several threads are set at high priority at the same time, the threads lose their effectiveness.</span></span> <span data-ttu-id="43832-136">Die Klasse mit hoher Priorität sollte für Threads reserviert werden, die auf zeitkritische Ereignisse reagieren müssen.</span><span class="sxs-lookup"><span data-stu-id="43832-136">The high-priority class should be reserved for threads that must respond to time-critical events.</span></span> <span data-ttu-id="43832-137">Wenn Ihre Anwendung eine Aufgabe ausführt, die die Klasse mit hoher Priorität erfordert, während die restlichen Aufgaben eine normale Priorität haben, verwenden Sie [**setpriorityclass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) , um die Prioritäts Klasse der Anwendung vorübergehend zu erhöhen. verringern Sie Sie anschließend, nachdem die zeitkritische Aufgabe abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="43832-137">If your application performs one task that requires the high-priority class while the rest of its tasks are normal priority, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) to raise the priority class of the application temporarily; then reduce it after the time-critical task has been completed.</span></span> <span data-ttu-id="43832-138">Eine andere Strategie besteht darin, einen Prozess mit hoher Priorität zu erstellen, bei dem alle Threads in den meisten Fällen blockiert werden, sodass Threads nur dann wiedererweckt werden, wenn wichtige Aufgaben benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="43832-138">Another strategy is to create a high-priority process that has all of its threads blocked most of the time, awakening threads only when critical tasks are needed.</span></span> <span data-ttu-id="43832-139">Der wichtigste Punkt ist, dass ein Thread mit hoher Priorität für einen kurzen Zeitraum ausgeführt werden sollte und nur wenn er zeitkritische Aufgaben ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="43832-139">The important point is that a high-priority thread should execute for a brief time, and only when it has time-critical work to perform.</span></span>

<span data-ttu-id="43832-140">Sie sollten fast nie die Echtzeit- \_ Prioritäts \_ Klasse verwenden, da dadurch Systemthreads unterbrochen werden, die Maus Eingaben, Tastatureingaben und das Leeren von Hintergrund Datenträger verwalten.</span><span class="sxs-lookup"><span data-stu-id="43832-140">You should almost never use REALTIME\_PRIORITY\_CLASS, because this interrupts system threads that manage mouse input, keyboard input, and background disk flushing.</span></span> <span data-ttu-id="43832-141">Diese Klasse eignet sich für Anwendungen, die direkt mit der Hardware kommunizieren oder kurze Aufgaben ausführen, die begrenzte Unterbrechungen aufweisen sollten.</span><span class="sxs-lookup"><span data-stu-id="43832-141">This class can be appropriate for applications that "talk" directly to hardware or that perform brief tasks that should have limited interruptions.</span></span>

## <a name="priority-level"></a><span data-ttu-id="43832-142">Prioritätsstufe</span><span class="sxs-lookup"><span data-stu-id="43832-142">Priority Level</span></span>

<span data-ttu-id="43832-143">Die folgenden Prioritätsstufen sind in jeder Prioritäts Klasse aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="43832-143">The following are priority levels within each priority class:</span></span><dl> <span data-ttu-id="43832-144">Thread \_ Priorität im \_ Leerlauf</span><span class="sxs-lookup"><span data-stu-id="43832-144">THREAD\_PRIORITY\_IDLE</span></span>  
<span data-ttu-id="43832-145">Thread \_ Priorität \_ niedrigste</span><span class="sxs-lookup"><span data-stu-id="43832-145">THREAD\_PRIORITY\_LOWEST</span></span>  
<span data-ttu-id="43832-146">Thread \_ Priorität \_ unterhalb von \_ Normal</span><span class="sxs-lookup"><span data-stu-id="43832-146">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  
<span data-ttu-id="43832-147">Thread \_ Priorität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="43832-147">THREAD\_PRIORITY\_NORMAL</span></span>  
<span data-ttu-id="43832-148">Thread \_ Priorität \_ oberhalb des \_ normalen</span><span class="sxs-lookup"><span data-stu-id="43832-148">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  
<span data-ttu-id="43832-149">Thread \_ Priorität \_ höchste</span><span class="sxs-lookup"><span data-stu-id="43832-149">THREAD\_PRIORITY\_HIGHEST</span></span>  
<span data-ttu-id="43832-150">Thread \_ Prioritäts \_ Zeit \_ kritisch</span><span class="sxs-lookup"><span data-stu-id="43832-150">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span>  
</dl>

<span data-ttu-id="43832-151">Alle Threads werden mithilfe der Thread \_ Priorität \_ Normal erstellt.</span><span class="sxs-lookup"><span data-stu-id="43832-151">All threads are created using THREAD\_PRIORITY\_NORMAL.</span></span> <span data-ttu-id="43832-152">Dies bedeutet, dass die Thread Priorität mit der Prozess Prioritäts Klasse identisch ist.</span><span class="sxs-lookup"><span data-stu-id="43832-152">This means that the thread priority is the same as the process priority class.</span></span> <span data-ttu-id="43832-153">Nachdem Sie einen Thread erstellt haben, verwenden Sie die [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) -Funktion, um die Priorität relativ zu anderen Threads im Prozess anzupassen.</span><span class="sxs-lookup"><span data-stu-id="43832-153">After you create a thread, use the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function to adjust its priority relative to other threads in the process.</span></span>

<span data-ttu-id="43832-154">Eine typische Strategie besteht darin, die Thread \_ Priorität \_ oberhalb \_ der normalen oder Thread \_ Priorität \_ für den Eingabe Thread des Prozesses zu verwenden, um sicherzustellen, dass die Anwendung auf den Benutzer reagiert.</span><span class="sxs-lookup"><span data-stu-id="43832-154">A typical strategy is to use THREAD\_PRIORITY\_ABOVE\_NORMAL or THREAD\_PRIORITY\_HIGHEST for the process's input thread, to ensure that the application is responsive to the user.</span></span> <span data-ttu-id="43832-155">Hintergrundthreads, insbesondere prozessorintensive, können auf die Thread \_ Priorität \_ unterhalb \_ der normalen oder Thread Priorität niedrigste festgelegt werden \_ \_ , um sicherzustellen, dass Sie bei Bedarf vorzeitig entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="43832-155">Background threads, particularly those that are processor intensive, can be set to THREAD\_PRIORITY\_BELOW\_NORMAL or THREAD\_PRIORITY\_LOWEST, to ensure that they can be preempted when necessary.</span></span> <span data-ttu-id="43832-156">Wenn Sie jedoch einen Thread haben, der darauf wartet, dass ein anderer Thread mit niedrigerer Priorität einen Task abschließt, müssen Sie die Ausführung des wartenden Threads mit hoher Priorität blockieren.</span><span class="sxs-lookup"><span data-stu-id="43832-156">However, if you have a thread waiting for another thread with a lower priority to complete some task, be sure to block the execution of the waiting high-priority thread.</span></span> <span data-ttu-id="43832-157">Verwenden Sie hierzu eine Wait- [Funktion](../sync/wait-functions.md), einen [kritischen Abschnitt](../sync/critical-section-objects.md) [**oder die Funktion**](/windows/win32/api/synchapi/nf-synchapi-sleep) "Standby", " [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex)" oder " [**SwitchTo Thread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) ".</span><span class="sxs-lookup"><span data-stu-id="43832-157">To do this, use a [wait function](../sync/wait-functions.md), [critical section](../sync/critical-section-objects.md), or the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function, [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function.</span></span> <span data-ttu-id="43832-158">Dies ist vorzuziehen, wenn der Thread eine Schleife ausführt.</span><span class="sxs-lookup"><span data-stu-id="43832-158">This is preferable to having the thread execute a loop.</span></span> <span data-ttu-id="43832-159">Andernfalls kann der Prozess blockiert werden, da der Thread mit niedrigerer Priorität nie geplant wird.</span><span class="sxs-lookup"><span data-stu-id="43832-159">Otherwise, the process may become deadlocked, because the thread with lower priority is never scheduled.</span></span>

<span data-ttu-id="43832-160">Verwenden Sie die [**getthreadpriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) -Funktion, um die aktuelle Prioritätsstufe eines Threads zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="43832-160">To determine the current priority level of a thread, use the [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) function.</span></span>

## <a name="base-priority"></a><span data-ttu-id="43832-161">Basispriorität</span><span class="sxs-lookup"><span data-stu-id="43832-161">Base Priority</span></span>

<span data-ttu-id="43832-162">Die Prozess Prioritäts Klasse und die Thread Prioritätsstufe werden kombiniert, um die Basis Priorität der einzelnen Threads zu bilden.</span><span class="sxs-lookup"><span data-stu-id="43832-162">The process priority class and thread priority level are combined to form the base priority of each thread.</span></span>

<span data-ttu-id="43832-163">In der folgenden Tabelle wird die Basis Priorität für Kombinationen aus der Prozess Prioritäts Klasse und dem Thread Prioritätswert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="43832-163">The following table shows the base priority for combinations of process priority class and thread priority value.</span></span>


<table>
<tr>
<th colspan="2"><span data-ttu-id="43832-164">Prozess Prioritäts Klasse</span><span class="sxs-lookup"><span data-stu-id="43832-164">Process priority class</span></span></th>
<th><span data-ttu-id="43832-165">Thread Prioritätsstufe</span><span class="sxs-lookup"><span data-stu-id="43832-165">Thread priority level</span></span></th>
<th><span data-ttu-id="43832-166">Basis Priorität</span><span class="sxs-lookup"><span data-stu-id="43832-166">Base priority</span></span></th>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="43832-167">IDLE_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="43832-167">IDLE_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="43832-168">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="43832-168">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="43832-169">1</span><span class="sxs-lookup"><span data-stu-id="43832-169">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-170">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="43832-170">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="43832-171">2</span><span class="sxs-lookup"><span data-stu-id="43832-171">2</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-172">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-172">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="43832-173">3</span><span class="sxs-lookup"><span data-stu-id="43832-173">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-174">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-174">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="43832-175">4</span><span class="sxs-lookup"><span data-stu-id="43832-175">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-176">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-176">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="43832-177">5</span><span class="sxs-lookup"><span data-stu-id="43832-177">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-178">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="43832-178">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="43832-179">6</span><span class="sxs-lookup"><span data-stu-id="43832-179">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-180">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="43832-180">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="43832-181">15</span><span class="sxs-lookup"><span data-stu-id="43832-181">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="43832-182">BELOW_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="43832-182">BELOW_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="43832-183">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="43832-183">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="43832-184">1</span><span class="sxs-lookup"><span data-stu-id="43832-184">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-185">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="43832-185">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="43832-186">4</span><span class="sxs-lookup"><span data-stu-id="43832-186">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-187">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-187">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="43832-188">5</span><span class="sxs-lookup"><span data-stu-id="43832-188">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-189">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-189">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="43832-190">6</span><span class="sxs-lookup"><span data-stu-id="43832-190">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-191">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-191">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="43832-192">7</span><span class="sxs-lookup"><span data-stu-id="43832-192">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-193">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="43832-193">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="43832-194">8</span><span class="sxs-lookup"><span data-stu-id="43832-194">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-195">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="43832-195">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="43832-196">15</span><span class="sxs-lookup"><span data-stu-id="43832-196">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="43832-197">NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="43832-197">NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="43832-198">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="43832-198">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="43832-199">1</span><span class="sxs-lookup"><span data-stu-id="43832-199">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-200">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="43832-200">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="43832-201">6</span><span class="sxs-lookup"><span data-stu-id="43832-201">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-202">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-202">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="43832-203">7</span><span class="sxs-lookup"><span data-stu-id="43832-203">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-204">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-204">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="43832-205">8</span><span class="sxs-lookup"><span data-stu-id="43832-205">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-206">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-206">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="43832-207">9</span><span class="sxs-lookup"><span data-stu-id="43832-207">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-208">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="43832-208">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="43832-209">10</span><span class="sxs-lookup"><span data-stu-id="43832-209">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-210">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="43832-210">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="43832-211">15</span><span class="sxs-lookup"><span data-stu-id="43832-211">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="43832-212">ABOVE_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="43832-212">ABOVE_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="43832-213">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="43832-213">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="43832-214">1</span><span class="sxs-lookup"><span data-stu-id="43832-214">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-215">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="43832-215">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="43832-216">8</span><span class="sxs-lookup"><span data-stu-id="43832-216">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-217">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-217">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="43832-218">9</span><span class="sxs-lookup"><span data-stu-id="43832-218">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-219">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-219">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="43832-220">10</span><span class="sxs-lookup"><span data-stu-id="43832-220">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-221">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-221">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="43832-222">11</span><span class="sxs-lookup"><span data-stu-id="43832-222">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-223">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="43832-223">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="43832-224">12</span><span class="sxs-lookup"><span data-stu-id="43832-224">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-225">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="43832-225">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="43832-226">15</span><span class="sxs-lookup"><span data-stu-id="43832-226">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="43832-227">HIGH_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="43832-227">HIGH_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="43832-228">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="43832-228">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="43832-229">1</span><span class="sxs-lookup"><span data-stu-id="43832-229">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-230">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="43832-230">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="43832-231">11</span><span class="sxs-lookup"><span data-stu-id="43832-231">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-232">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-232">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="43832-233">12</span><span class="sxs-lookup"><span data-stu-id="43832-233">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-234">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-234">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="43832-235">13</span><span class="sxs-lookup"><span data-stu-id="43832-235">13</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-236">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-236">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="43832-237">14</span><span class="sxs-lookup"><span data-stu-id="43832-237">14</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-238">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="43832-238">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="43832-239">15</span><span class="sxs-lookup"><span data-stu-id="43832-239">15</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-240">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="43832-240">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="43832-241">15</span><span class="sxs-lookup"><span data-stu-id="43832-241">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="43832-242">REALTIME_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="43832-242">REALTIME_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="43832-243">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="43832-243">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="43832-244">16</span><span class="sxs-lookup"><span data-stu-id="43832-244">16</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-245">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="43832-245">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="43832-246">22</span><span class="sxs-lookup"><span data-stu-id="43832-246">22</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-247">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-247">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="43832-248">23</span><span class="sxs-lookup"><span data-stu-id="43832-248">23</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-249">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-249">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="43832-250">24</span><span class="sxs-lookup"><span data-stu-id="43832-250">24</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-251">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="43832-251">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="43832-252">25</span><span class="sxs-lookup"><span data-stu-id="43832-252">25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-253">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="43832-253">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="43832-254">26</span><span class="sxs-lookup"><span data-stu-id="43832-254">26</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="43832-255">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="43832-255">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="43832-256">31</span><span class="sxs-lookup"><span data-stu-id="43832-256">31</span></span></td>
</tr>
</table>

 

 

 
