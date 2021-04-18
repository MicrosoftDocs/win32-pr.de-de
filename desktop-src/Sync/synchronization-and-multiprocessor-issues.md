---
description: Bei Anwendungen können Probleme auftreten, wenn Sie auf Multiprozessorsystemen ausgeführt werden. Dies trifft auf Annahmen zu, die nur für Systeme mit nur einem Prozessor gültig sind.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Synchronisierungs- und Multiprozessorprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106361094"
---
# <a name="synchronization-and-multiprocessor-issues"></a><span data-ttu-id="826f8-103">Synchronisierungs- und Multiprozessorprobleme</span><span class="sxs-lookup"><span data-stu-id="826f8-103">Synchronization and Multiprocessor Issues</span></span>

<span data-ttu-id="826f8-104">Bei Anwendungen können Probleme auftreten, wenn Sie auf Multiprozessorsystemen ausgeführt werden. Dies trifft auf Annahmen zu, die nur für Systeme mit nur einem Prozessor gültig sind.</span><span class="sxs-lookup"><span data-stu-id="826f8-104">Applications may encounter problems when run on multiprocessor systems due to assumptions they make which are valid only on single-processor systems.</span></span>

## <a name="thread-priorities"></a><span data-ttu-id="826f8-105">Threadprioritäten</span><span class="sxs-lookup"><span data-stu-id="826f8-105">Thread Priorities</span></span>

<span data-ttu-id="826f8-106">Stellen Sie sich ein Programm mit zwei Threads vor, eine mit einer höheren Priorität als die andere.</span><span class="sxs-lookup"><span data-stu-id="826f8-106">Consider a program with two threads, one with a higher priority than the other.</span></span> <span data-ttu-id="826f8-107">Bei einem System mit einem einzelnen Prozessor übergibt der Thread mit höherer Priorität die Steuerung nicht an den Thread mit niedrigerer Priorität, da der Scheduler die Threads mit höherer Priorität bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="826f8-107">On a single-processor system, the higher priority thread will not relinquish control to the lower priority thread because the scheduler gives preference to higher priority threads.</span></span> <span data-ttu-id="826f8-108">Auf einem Multiprozessorsystem können beide Threads gleichzeitig ausgeführt werden, jeweils auf dem eigenen Prozessor.</span><span class="sxs-lookup"><span data-stu-id="826f8-108">On a multiprocessor system, both threads can run simultaneously, each on its own processor.</span></span>

<span data-ttu-id="826f8-109">Anwendungen sollten den Zugriff auf Datenstrukturen synchronisieren, um Racebedingungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="826f8-109">Applications should synchronize access to data structures to avoid race conditions.</span></span> <span data-ttu-id="826f8-110">Code, der davon ausgeht, dass Threads mit höherer Priorität ohne Störungen von Threads mit niedrigerer Priorität ausgeführt werden, schlagen auf Multiprozessorsystemen fehl</span><span class="sxs-lookup"><span data-stu-id="826f8-110">Code that assumes that higher priority threads run without interference from lower priority threads will fail on multiprocessor systems.</span></span>

## <a name="memory-ordering"></a><span data-ttu-id="826f8-111">Speicher Anordnung</span><span class="sxs-lookup"><span data-stu-id="826f8-111">Memory Ordering</span></span>

<span data-ttu-id="826f8-112">Wenn ein Prozessor in einen Speicherort schreibt, wird der Wert zwischengespeichert, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="826f8-112">When a processor writes to a memory location, the value is cached to improve performance.</span></span> <span data-ttu-id="826f8-113">Ebenso versucht der Prozessor, Lese Anforderungen aus dem Cache zu erfüllen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="826f8-113">Similarly, the processor attempts to satisfy read requests from the cache to improve performance.</span></span> <span data-ttu-id="826f8-114">Außerdem beginnen Prozessoren mit dem Abrufen von Werten aus dem Arbeitsspeicher, bevor Sie von der Anwendung angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="826f8-114">Furthermore, processors begin to fetch values from memory before they are requested by the application.</span></span> <span data-ttu-id="826f8-115">Dies kann als Teil der spekulativen Ausführung oder aufgrund von Cache Zeilen Problemen auftreten.</span><span class="sxs-lookup"><span data-stu-id="826f8-115">This can happen as part of speculative execution or due to cache line issues.</span></span>

<span data-ttu-id="826f8-116">CPU-Caches können in Banken partitioniert werden, auf die gleichzeitig zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="826f8-116">CPU caches can be partitioned into banks that can be accessed in parallel.</span></span> <span data-ttu-id="826f8-117">Dies bedeutet, dass Speichervorgänge außerhalb der Reihenfolge abgeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="826f8-117">This means that memory operations can be completed out of order.</span></span> <span data-ttu-id="826f8-118">Um sicherzustellen, dass Speichervorgänge in der richtigen Reihenfolge abgeschlossen werden, stellen die meisten Prozessoren Speicher Absperr Anweisungen bereit.</span><span class="sxs-lookup"><span data-stu-id="826f8-118">To ensure that memory operations are completed in order, most processors provide memory-barrier instructions.</span></span> <span data-ttu-id="826f8-119">Eine *vollständige Speicherbarriere* stellt sicher, dass Arbeitsspeicher Lese-und-Schreibvorgänge, die vor der Speicher Abbild Anweisung angezeigt werden, vor Lese-und Schreibvorgängen im Arbeitsspeicher, die nach der Speicher Abbild Anweisung angezeigt werden,</span><span class="sxs-lookup"><span data-stu-id="826f8-119">A *full memory barrier* ensures that memory read and write operations that appear before the memory barrier instruction are committed to memory before any memory read and write operations that appear after the memory barrier instruction.</span></span> <span data-ttu-id="826f8-120">Eine *Lese Speicherbarriere* ordnet nur die Speicher Lesevorgänge zu, und eine *Schreib Speicherbarriere* ordnet nur die Speicher Schreibvorgänge an.</span><span class="sxs-lookup"><span data-stu-id="826f8-120">A *read memory barrier* orders only the memory read operations and a *write memory barrier* orders only the memory write operations.</span></span> <span data-ttu-id="826f8-121">Diese Anweisungen stellen außerdem sicher, dass der Compiler alle Optimierungen deaktiviert, die Arbeitsspeicher Vorgänge über die Barrieren hinweg neu anordnen können.</span><span class="sxs-lookup"><span data-stu-id="826f8-121">These instructions also ensure that the compiler disables any optimizations that could reorder memory operations across the barriers.</span></span>

<span data-ttu-id="826f8-122">Prozessoren können Anweisungen für Speicherbarrieren mit Abruf-, Release-und Fence Semantik unterstützen.</span><span class="sxs-lookup"><span data-stu-id="826f8-122">Processors can support instructions for memory barriers with acquire, release, and fence semantics.</span></span> <span data-ttu-id="826f8-123">Diese Semantik beschreibt die Reihenfolge, in der die Ergebnisse eines Vorgangs verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="826f8-123">These semantics describe the order in which results of an operation become available.</span></span> <span data-ttu-id="826f8-124">Bei der Semantik zum Abrufen sind die Ergebnisse des Vorgangs vor den Ergebnissen eines beliebigen Vorgangs verfügbar, der im Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="826f8-124">With acquire semantics, the results of the operation are available before the results of any operation that appears after it in code.</span></span> <span data-ttu-id="826f8-125">Bei der releasesemantik sind die Ergebnisse des Vorgangs nach den Ergebnissen eines beliebigen Vorgangs verfügbar, der im Code vor ihm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="826f8-125">With release semantics, the results of the operation are available after the results of any operation that appears before it in code.</span></span> <span data-ttu-id="826f8-126">Die Fence-Semantik kombiniert die Semantik zum Abrufen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="826f8-126">Fence semantics combine acquire and release semantics.</span></span> <span data-ttu-id="826f8-127">Die Ergebnisse eines Vorgangs mit der Fence-Semantik sind vor den Vorgängen eines beliebigen Vorgangs verfügbar, der im Code nach dem Vorgang angezeigt wird, und nach dem eines beliebigen Vorgangs, der vor ihm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="826f8-127">The results of an operation with fence semantics are available before those of any operation that appears after it in code and after those of any operation that appears before it.</span></span>

<span data-ttu-id="826f8-128">Auf x86-und x64-Prozessoren, die SSE2 unterstützen, sind die Anweisungen **mfence** (arbeitsspeicherfence), **lfence** (Load Fence) und **sfence** (Store Fence).</span><span class="sxs-lookup"><span data-stu-id="826f8-128">On x86 and x64 processors that support SSE2, the instructions are **mfence** (memory fence), **lfence** (load fence), and **sfence** (store fence).</span></span> <span data-ttu-id="826f8-129">Bei ARM-Prozessoren sind die instrumentierten **DMB** und **DSB**.</span><span class="sxs-lookup"><span data-stu-id="826f8-129">On ARM processors, the instrutions are **dmb** and **dsb**.</span></span> <span data-ttu-id="826f8-130">Weitere Informationen finden Sie in der Dokumentation für den Prozessor.</span><span class="sxs-lookup"><span data-stu-id="826f8-130">For more information, see the documentation for the processor.</span></span>

<span data-ttu-id="826f8-131">Die folgenden Synchronisierungs Funktionen verwenden die entsprechenden Barrieren, um die Arbeitsspeicher Anordnung sicherzustellen:</span><span class="sxs-lookup"><span data-stu-id="826f8-131">The following synchronization functions use the appropriate barriers to ensure memory ordering:</span></span>

-   <span data-ttu-id="826f8-132">Funktionen, die kritische Abschnitte eingeben oder verlassen</span><span class="sxs-lookup"><span data-stu-id="826f8-132">Functions that enter or leave critical sections</span></span>
-   <span data-ttu-id="826f8-133">Funktionen, die SRW-Sperren abrufen oder freigeben</span><span class="sxs-lookup"><span data-stu-id="826f8-133">Functions that acquire or release SRW locks</span></span>
-   <span data-ttu-id="826f8-134">Einmalige Initialisierung beginnt und Fertigstellung</span><span class="sxs-lookup"><span data-stu-id="826f8-134">One-time initialization begin and completion</span></span>
-   <span data-ttu-id="826f8-135">**Entersynchronizationbarrier** -Funktion</span><span class="sxs-lookup"><span data-stu-id="826f8-135">**EnterSynchronizationBarrier** function</span></span>
-   <span data-ttu-id="826f8-136">Funktionen, die Synchronisierungs Objekten signalisieren</span><span class="sxs-lookup"><span data-stu-id="826f8-136">Functions that signal synchronization objects</span></span>
-   <span data-ttu-id="826f8-137">Wait-Funktionen</span><span class="sxs-lookup"><span data-stu-id="826f8-137">Wait functions</span></span>
-   <span data-ttu-id="826f8-138">Interlocked-Funktionen (außer Funktionen mit einem _nofence_ -Suffix oder intrinsie mit dem _\_ NF_ -Suffix)</span><span class="sxs-lookup"><span data-stu-id="826f8-138">Interlocked functions (except functions with _NoFence_ suffix, or intrinsics with _\_nf_ suffix)</span></span>

## <a name="fixing-a-race-condition"></a><span data-ttu-id="826f8-139">Reparieren einer Racebedingung</span><span class="sxs-lookup"><span data-stu-id="826f8-139">Fixing a Race Condition</span></span>

<span data-ttu-id="826f8-140">Der folgende Code hat eine Racebedingung auf einem Multiprozessorsystem, da der Prozessor, `CacheComputedValue` der zum ersten Mal ausgeführt wird, in den Hauptspeicher schreiben kann, `fValueHasBeenComputed` bevor er `iValue` in den Hauptspeicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="826f8-140">The following code has a race condition on a multiprocessor systems because the processor that executes `CacheComputedValue` the first time may write `fValueHasBeenComputed` to main memory before writing `iValue` to main memory.</span></span> <span data-ttu-id="826f8-141">Folglich liest ein zweiter Prozessor, der `FetchComputedValue` gleichzeitig ausgeführt wird `fValueHasBeenComputed` , **true**, aber der neue Wert von `iValue` befindet sich noch im Cache des ersten Prozessors und wurde nicht in den Arbeitsspeicher geschrieben.</span><span class="sxs-lookup"><span data-stu-id="826f8-141">Consequently, a second processor executing `FetchComputedValue` at the same time reads `fValueHasBeenComputed` as **TRUE**, but the new value of `iValue` is still in the first processor's cache and has not been written to memory.</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="826f8-142">Diese Racebedingung oben kann mithilfe des **volatile** -Schlüssel Worts oder der [**interlockedexchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) -Funktion repariert werden, um sicherzustellen, dass der Wert von `iValue` für alle Prozessoren aktualisiert wird, bevor der Wert von `fValueHasBeenComputed` auf **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="826f8-142">This race condition above can be repaired by using the **volatile** keyword or the [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) function to ensure that the value of `iValue` is updated for all processors before the value of `fValueHasBeenComputed` is set to **TRUE**.</span></span>

<span data-ttu-id="826f8-143">Beim Starten von Visual Studio 2005 verwendet der Compiler bei der Kompilierung im **/volatile: ms** -Modus die erfassten Semantik für Lesevorgänge für **flüchtige** Variablen und releasesemantik für Schreibvorgänge für **flüchtige** Variablen (sofern von der CPU unterstützt).</span><span class="sxs-lookup"><span data-stu-id="826f8-143">Starting Visual Studio 2005, if compiled in **/volatile:ms** mode, the compiler uses acquire semantics for read operations on **volatile** variables and release semantics for write operations on **volatile** variables (when supported by the CPU).</span></span> <span data-ttu-id="826f8-144">Aus diesem Grund können Sie das Beispiel wie folgt korrigieren:</span><span class="sxs-lookup"><span data-stu-id="826f8-144">Therefore, you can correct the example as follows:</span></span>

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="826f8-145">Mit Visual Studio 2003 werden **flüchtige** und **flüchtige** Verweise angeordnet. der Compiler wird den Zugriff auf **flüchtige** Variablen nicht neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="826f8-145">With Visual Studio 2003, **volatile** to **volatile** references are ordered; the compiler will not re-order **volatile** variable access.</span></span> <span data-ttu-id="826f8-146">Diese Vorgänge können jedoch vom Prozessor neu angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="826f8-146">However, these operations could be re-ordered by the processor.</span></span> <span data-ttu-id="826f8-147">Aus diesem Grund können Sie das Beispiel wie folgt korrigieren:</span><span class="sxs-lookup"><span data-stu-id="826f8-147">Therefore, you can correct the example as follows:</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a><span data-ttu-id="826f8-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="826f8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="826f8-149">Kritische Abschnitts Objekte</span><span class="sxs-lookup"><span data-stu-id="826f8-149">Critical Section Objects</span></span>](critical-section-objects.md)
</dt> <dt>

[<span data-ttu-id="826f8-150">Interlocked-Variablen Zugriff</span><span class="sxs-lookup"><span data-stu-id="826f8-150">Interlocked Variable Access</span></span>](interlocked-variable-access.md)
</dt> <dt>

[<span data-ttu-id="826f8-151">Wait-Funktionen</span><span class="sxs-lookup"><span data-stu-id="826f8-151">Wait Functions</span></span>](wait-functions.md)
</dt> </dl>

 

 



