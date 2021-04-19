---
description: Bedingungs Variablen sind Synchronisierungs primitive, mit denen Threads warten können, bis eine bestimmte Bedingung eintritt. Bedingungs Variablen sind Benutzermodus-Objekte, die nicht Prozess übergreifend freigegeben werden können.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Bedingungs Variablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368892"
---
# <a name="condition-variables"></a><span data-ttu-id="3d140-104">Bedingungs Variablen</span><span class="sxs-lookup"><span data-stu-id="3d140-104">Condition Variables</span></span>

<span data-ttu-id="3d140-105">Bedingungs Variablen sind Synchronisierungs primitive, mit denen Threads warten können, bis eine bestimmte Bedingung eintritt.</span><span class="sxs-lookup"><span data-stu-id="3d140-105">Condition variables are synchronization primitives that enable threads to wait until a particular condition occurs.</span></span> <span data-ttu-id="3d140-106">Bedingungs Variablen sind Benutzermodus-Objekte, die nicht Prozess übergreifend freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3d140-106">Condition variables are user-mode objects that cannot be shared across processes.</span></span>

<span data-ttu-id="3d140-107">Mit Bedingungs Variablen können Threads eine Sperre atomisch freigeben und in den Ruhezustand wechseln.</span><span class="sxs-lookup"><span data-stu-id="3d140-107">Condition variables enable threads to atomically release a lock and enter the sleeping state.</span></span> <span data-ttu-id="3d140-108">Sie können mit kritischen Abschnitten oder SRW-Sperren (Slim Reader/Writer) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d140-108">They can be used with critical sections or slim reader/writer (SRW) locks.</span></span> <span data-ttu-id="3d140-109">Bedingungs Variablen unterstützen Vorgänge, die wartende Threads "reaktivieren" oder "alle reaktivieren".</span><span class="sxs-lookup"><span data-stu-id="3d140-109">Condition variables support operations that "wake one" or "wake all" waiting threads.</span></span> <span data-ttu-id="3d140-110">Nachdem ein Thread aktiviert wurde, erhält er die Sperre erneut, die er freigegeben hat, als der Thread in den Ruhezustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="3d140-110">After a thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.</span></span>

<span data-ttu-id="3d140-111">Beachten Sie, dass der Aufrufer eine Bedingungs **\_ Variablen** Struktur zuordnen und diese initialisieren muss, indem [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) aufgerufen wird (um die Struktur dynamisch zu initialisieren), oder die Konstante Bedingungs **\_ Variable \_ Init** der Struktur Variablen zuzuweisen (um die Struktur statisch zu initialisieren).</span><span class="sxs-lookup"><span data-stu-id="3d140-111">Note that the caller must allocate a **CONDITION\_VARIABLE** structure and initialize it by either calling [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (to initialize the structure dynamically) or assign the constant **CONDITION\_VARIABLE\_INIT** to the structure variable (to initialize the structure statically).</span></span>

<span data-ttu-id="3d140-112">**Windows Server 2003 und Windows XP:** Bedingungs Variablen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d140-112">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>

<span data-ttu-id="3d140-113">Es folgen die Bedingungs Variablen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3d140-113">The following are the condition variable functions.</span></span>



| <span data-ttu-id="3d140-114">Bedingungs Variablen Funktion</span><span class="sxs-lookup"><span data-stu-id="3d140-114">Condition variable function</span></span>                                        | <span data-ttu-id="3d140-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d140-115">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d140-116">**InitializeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="3d140-116">**InitializeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | <span data-ttu-id="3d140-117">Initialisiert eine Bedingungs Variable.</span><span class="sxs-lookup"><span data-stu-id="3d140-117">Initializes a condition variable.</span></span>                                                                              |
| [<span data-ttu-id="3d140-118">**SleepConditionVariableCS**</span><span class="sxs-lookup"><span data-stu-id="3d140-118">**SleepConditionVariableCS**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | <span data-ttu-id="3d140-119">Gibt für die angegebene Bedingungs Variable aus und gibt den angegebenen kritischen Abschnitt als atomarischen Vorgang frei.</span><span class="sxs-lookup"><span data-stu-id="3d140-119">Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.</span></span> |
| [<span data-ttu-id="3d140-120">**SleepConditionVariableSRW**</span><span class="sxs-lookup"><span data-stu-id="3d140-120">**SleepConditionVariableSRW**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | <span data-ttu-id="3d140-121">Gibt für die angegebene Bedingungs Variable aus und gibt die angegebene SRW-Sperre als atomarischen Vorgang frei.</span><span class="sxs-lookup"><span data-stu-id="3d140-121">Sleeps on the specified condition variable and releases the specified SRW lock as an atomic operation.</span></span>         |
| [<span data-ttu-id="3d140-122">**WakeAllConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="3d140-122">**WakeAllConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | <span data-ttu-id="3d140-123">Aktiviert alle Threads, die auf die angegebene Bedingungs Variable warten.</span><span class="sxs-lookup"><span data-stu-id="3d140-123">Wakes all threads waiting on the specified condition variable.</span></span>                                                 |
| [<span data-ttu-id="3d140-124">**WakeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="3d140-124">**WakeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | <span data-ttu-id="3d140-125">Aktiviert einen einzelnen Thread, der auf die angegebene Bedingungs Variable wartet.</span><span class="sxs-lookup"><span data-stu-id="3d140-125">Wakes a single thread waiting on the specified condition variable.</span></span>                                             |



 

<span data-ttu-id="3d140-126">Der folgende Pseudo Code veranschaulicht das typische Verwendungs Muster von Bedingungs Variablen.</span><span class="sxs-lookup"><span data-stu-id="3d140-126">The following pseudocode demonstrates the typical usage pattern of condition variables.</span></span>

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

<span data-ttu-id="3d140-127">Beispielsweise würde die Funktion in einer Implementierung einer Reader-/Schreibsperre `TestPredicate` überprüfen, ob die aktuelle Sperranforderung mit den vorhandenen Besitzern kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="3d140-127">For example, in an implementation of a reader/writer lock, the `TestPredicate` function would verify that the current lock request is compatible with the existing owners.</span></span> <span data-ttu-id="3d140-128">Wenn dies der Fall ist, erhalten Sie die Sperre. andernfalls der Standbymodus.</span><span class="sxs-lookup"><span data-stu-id="3d140-128">If it is, acquire the lock; otherwise, sleep.</span></span> <span data-ttu-id="3d140-129">Ein ausführlicheres Beispiel finden Sie unter [verwenden](using-condition-variables.md)von Bedingungs Variablen.</span><span class="sxs-lookup"><span data-stu-id="3d140-129">For a more detailed example, see [Using Condition Variables](using-condition-variables.md).</span></span>

<span data-ttu-id="3d140-130">Bedingungs Variablen unterliegen falschen aufwecken (die nicht mit einem expliziten Aktivierungs Modus verknüpft sind) und gestohlenen aufwecken (ein anderer Thread wird vor dem aufwachten Thread verwaltet).</span><span class="sxs-lookup"><span data-stu-id="3d140-130">Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread).</span></span> <span data-ttu-id="3d140-131">Daher sollten Sie ein Prädikat (in der Regel in einer **while** -Schleife) nach dem zurückkehren eines Ruhe Zustands erneut überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3d140-131">Therefore, you should recheck a predicate (typically in a **while** loop) after a sleep operation returns.</span></span>

<span data-ttu-id="3d140-132">Sie können andere Threads mithilfe von [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) oder [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) entweder innerhalb oder außerhalb der der Bedingungs Variablen zugeordneten Sperre aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3d140-132">You can wake other threads using [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) or [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) either inside or outside the lock associated with the condition variable.</span></span> <span data-ttu-id="3d140-133">Es ist in der Regel besser, die Sperre freizugeben, bevor andere Threads aktiviert werden, um die Anzahl von Kontext Schaltern zu verringern.</span><span class="sxs-lookup"><span data-stu-id="3d140-133">It is usually better to release the lock before waking other threads to reduce the number of context switches.</span></span>

<span data-ttu-id="3d140-134">Häufig ist es praktisch, mehr als eine Bedingungs Variable mit derselben Sperre zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d140-134">It is often convenient to use more than one condition variable with the same lock.</span></span> <span data-ttu-id="3d140-135">Beispielsweise kann eine Implementierung einer Reader-/Writer-Sperre einen einzelnen kritischen Abschnitt verwenden, aber separate Bedingungs Variablen für Reader und Writer.</span><span class="sxs-lookup"><span data-stu-id="3d140-135">For example, an implementation of a reader/writer lock might use a single critical section but separate condition variables for readers and writers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d140-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d140-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d140-137">Verwenden von Bedingungs Variablen</span><span class="sxs-lookup"><span data-stu-id="3d140-137">Using Condition Variables</span></span>](using-condition-variables.md)
</dt> </dl>

 

 
