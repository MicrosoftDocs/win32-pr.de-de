---
description: Windows umfasst die folgenden neuen Programmier Elemente für die Synchronisierung.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Neuerungen bei der Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216187"
---
# <a name="whats-new-in-synchronization"></a><span data-ttu-id="c6877-103">Neuerungen bei der Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="c6877-103">What's New in Synchronization</span></span>

<span data-ttu-id="c6877-104">Windows umfasst die folgenden neuen Programmier Elemente für die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="c6877-104">Windows includes the following new programming elements for synchronization.</span></span>

## <a name="windows-8"></a><span data-ttu-id="c6877-105">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c6877-105">Windows 8</span></span>

### <a name="new-functions"></a><span data-ttu-id="c6877-106">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="c6877-106">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="c6877-107">**Delta-ynchronizationbarrier**</span><span class="sxs-lookup"><span data-stu-id="c6877-107">**DeleteSynchronizationBarrier**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="c6877-108">Löscht eine Synchronisierungs Barriere.</span><span class="sxs-lookup"><span data-stu-id="c6877-108">Deletes a synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-109">**Entersynchronizationbarrier**</span><span class="sxs-lookup"><span data-stu-id="c6877-109">**EnterSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="c6877-110">Bewirkt, dass der aufrufende Thread auf eine Synchronisierungs Barriere wartet, bis die maximale Anzahl von Threads in die Barriere eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c6877-110">Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-111">**Gejeverlappedresultex**</span><span class="sxs-lookup"><span data-stu-id="c6877-111">**GetOverlappedResultEx**</span></span>](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

<span data-ttu-id="c6877-112">Ruft die Ergebnisse eines überlappenden Vorgangs für die angegebene Datei, Named Pipe oder das Kommunikationsgerät innerhalb des angegebenen Timeout Intervalls ab.</span><span class="sxs-lookup"><span data-stu-id="c6877-112">Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval.</span></span> <span data-ttu-id="c6877-113">Der aufrufende Thread kann einen Warn Tabellen-warte Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6877-113">The calling thread can perform an alertable wait.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-114">**Initializesynchronizationbarrier**</span><span class="sxs-lookup"><span data-stu-id="c6877-114">**InitializeSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="c6877-115">Gibt die maximale Anzahl von Threads und die Drehungs Anzahl für eine neue Synchronisierungs Barriere an.</span><span class="sxs-lookup"><span data-stu-id="c6877-115">Specifies the maximum number of threads and spin count for a new synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-116">**Waitonaddress**</span><span class="sxs-lookup"><span data-stu-id="c6877-116">**WaitOnAddress**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

<span data-ttu-id="c6877-117">Wartet, bis der Wert an der angegebenen Adresse geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c6877-117">Waits for the value at the specified address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-118">**Wakebyaddressall**</span><span class="sxs-lookup"><span data-stu-id="c6877-118">**WakeByAddressAll**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

<span data-ttu-id="c6877-119">Aktiviert alle Threads, die darauf warten, dass sich der Wert einer Adresse ändert.</span><span class="sxs-lookup"><span data-stu-id="c6877-119">Wakes all threads that are waiting for the value of an address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-120">**Wakebyaddresssingle**</span><span class="sxs-lookup"><span data-stu-id="c6877-120">**WakeByAddressSingle**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

<span data-ttu-id="c6877-121">Aktiviert einen Thread, der darauf wartet, dass sich der Wert einer Adresse ändert.</span><span class="sxs-lookup"><span data-stu-id="c6877-121">Wakes one thread that is waiting for the value of an address to change.</span></span>

</dd> </dl>

### <a name="new-interlocked-functions"></a><span data-ttu-id="c6877-122">Neue Interlocked-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c6877-122">New Interlocked Functions</span></span>

<dl> <dt>

<span data-ttu-id="c6877-123">[**Interlockedaddnofence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-124">Führt eine atomarische Additions Operation für die angegebenen **langen** Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-124">Performs an atomic addition operation on the specified **LONG** values.</span></span> <span data-ttu-id="c6877-125">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-125">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-127">Führt eine atomarische Additions Operation für die angegebenen **Longlong** -Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-127">Performs an atomic addition operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="c6877-128">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-128">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-129">[**Interlockedandnofence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-130">Führt eine atomarische and-Operation für die angegebenen **langen** Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-130">Performs an atomic AND operation on the specified **LONG** values.</span></span> <span data-ttu-id="c6877-131">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-131">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-133">Führt eine atomarische and-Operation für die angegebenen **char** -Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-133">Performs an atomic AND operation on the specified **char** values.</span></span> <span data-ttu-id="c6877-134">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-134">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-136">Führt eine atomarische and-Operation für die angegebenen **kurzwerte** aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-136">Performs an atomic AND operation on the specified **SHORT** values.</span></span> <span data-ttu-id="c6877-137">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-137">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-139">Führt eine atomarische and-Operation für die angegebenen **Longlong** -Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-139">Performs an atomic AND operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="c6877-140">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-140">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-142">Testet das angegebene Bit des angegebenen **LONG64** -Werts und ergänzt dieses.</span><span class="sxs-lookup"><span data-stu-id="c6877-142">Tests the specified bit of the specified **LONG64** value and complements it.</span></span> <span data-ttu-id="c6877-143">Der Vorgang ist atomarisch.</span><span class="sxs-lookup"><span data-stu-id="c6877-143">The operation is atomic.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-144">[**Interlockedbittestandresettings**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-145">Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-145">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="c6877-146">Der Vorgang ist atomarisch und wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-146">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-147">[**Interlockedbittestandreanlelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-148">Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-148">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="c6877-149">Der Vorgang ist atomarisch und wird mithilfe der Speicherfreigabe Semantik ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-149">The operation is atomic, and it is performed using memory release semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-150">[**Interlockedbittestandabtacquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-151">Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-151">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="c6877-152">Der Vorgang ist atomarisch und wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-152">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-153">[**Interlockedbittestandletrelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-154">Testet das angegebene Bit des angegebenen **Long** -Werts und legt es auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-154">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="c6877-155">Der Vorgang ist atomarisch und wird mit der Versions Semantik für releasearbeitsspeicher ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-155">The operation is atomic, and it is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-156">[**Interlockedcompareexchangenofence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-157">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-157">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-158">Die-Funktion vergleicht zwei angegebene 32-Bit-Werte und tauscht sich mit einem anderen 32-Bit-Wert aus, der auf dem Ergebnis des Vergleichs basiert.</span><span class="sxs-lookup"><span data-stu-id="c6877-158">The function compares two specified 32-bit values and exchanges with another 32-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="c6877-159">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-159">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-160">**InterlockedCompareExchange16**</span><span class="sxs-lookup"><span data-stu-id="c6877-160">**InterlockedCompareExchange16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

<span data-ttu-id="c6877-161">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-161">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-162">Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-162">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-164">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-164">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-165">Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-165">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="c6877-166">Der Vorgang wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-166">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-168">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-168">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-169">Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-169">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="c6877-170">Der Austausch erfolgt mit der Auftrags Semantik für releasearbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c6877-170">The exchange is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-172">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-172">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-173">Die-Funktion vergleicht zwei angegebene 16-Bit-Werte und tauscht auf der Grundlage des Ergebnisses des Vergleichs einen anderen 16-Bit-Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-173">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="c6877-174">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-174">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-176">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-176">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-177">Die-Funktion vergleicht zwei angegebene 64-Bit-Werte und tauscht sich mit einem anderen 64-Bit-Wert aus, der auf dem Ergebnis des Vergleichs basiert.</span><span class="sxs-lookup"><span data-stu-id="c6877-177">The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="c6877-178">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-178">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-179">**InterlockedCompareExchange128**</span><span class="sxs-lookup"><span data-stu-id="c6877-179">**InterlockedCompareExchange128**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

<span data-ttu-id="c6877-180">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-180">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-181">Die-Funktion vergleicht zwei angegebene 128-Bit-Werte und tauscht sich mit einem anderen 128-Bit-Wert aus, der auf dem Ergebnis des Vergleichs basiert.</span><span class="sxs-lookup"><span data-stu-id="c6877-181">The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-182">[**Interlockedcompareexchangepointernofence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-183">Führt einen atomaren Vergleichs-und Austausch Vorgang für die angegebenen Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-183">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="c6877-184">Die-Funktion vergleicht zwei angegebene Zeiger Werte und tauscht mit einem anderen Zeiger Wert auf der Grundlage des Ergebnisses des Vergleichs aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-184">The function compares two specified pointer values and exchanges with another pointer value based on the outcome of the comparison.</span></span> <span data-ttu-id="c6877-185">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-185">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-186">[**Interlockeddecrementnofence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-187">Verringert den Wert der angegebenen 32-Bit-Variablen als atomarischen Vorgang (verringert um 1).</span><span class="sxs-lookup"><span data-stu-id="c6877-187">Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-188">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-188">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-189">**InterlockedDecrement16**</span><span class="sxs-lookup"><span data-stu-id="c6877-189">**InterlockedDecrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

<span data-ttu-id="c6877-190">Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1).</span><span class="sxs-lookup"><span data-stu-id="c6877-190">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-192">Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1).</span><span class="sxs-lookup"><span data-stu-id="c6877-192">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-193">Der Vorgang wird mit der Semantik für die Speicher Reihenfolge abrufen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-193">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-195">Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1).</span><span class="sxs-lookup"><span data-stu-id="c6877-195">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-196">Der Vorgang wird mit der Versions Semantik für releasearbeitsspeicher ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-196">The operation is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-198">Verringert den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (verringert um 1).</span><span class="sxs-lookup"><span data-stu-id="c6877-198">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-199">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-199">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-201">Verringert den Wert der angegebenen 64-Bit-Variablen als atomarischen Vorgang (verringert um 1).</span><span class="sxs-lookup"><span data-stu-id="c6877-201">Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-202">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-202">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-203">[**Interlockedexchangenofence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-204">Legt eine 64-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-204">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="c6877-205">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-205">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-206">**InterlockedExchange8**</span><span class="sxs-lookup"><span data-stu-id="c6877-206">**InterlockedExchange8**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

<span data-ttu-id="c6877-207">Legt eine 8-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-207">Sets an 8-bit variable to the specified value as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-209">Legt eine 16-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-209">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="c6877-210">Der Vorgang wird mithilfe der Semantik zum Abrufen der Speicher Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-210">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-212">Legt eine 16-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-212">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="c6877-213">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-213">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-215">Legt eine 64-Bit-Variable als atomarischen Vorgang auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c6877-215">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="c6877-216">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-216">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-217">[**Interlockedexchangepointernofence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-218">Tauscht atomisch ein Adress Paar aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-218">Atomically exchanges a pair of addresses.</span></span> <span data-ttu-id="c6877-219">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-219">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-220">[**Interlockedexchangeaddnofence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-221">Führt eine atomarische Addition von 2 32-Bit-Werten aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-221">Performs an atomic addition of two 32-bit values.</span></span> <span data-ttu-id="c6877-222">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-222">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-224">Führt eine atomarische Addition von 2 64-Bit-Werten aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-224">Performs an atomic addition of two 64-bit values.</span></span> <span data-ttu-id="c6877-225">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-225">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-226">[**Interlockedinkrementnofence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-227">Erhöht den Wert der angegebenen 32-Bit-Variablen als atomarischen Vorgang (um 1 erhöht).</span><span class="sxs-lookup"><span data-stu-id="c6877-227">Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-228">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-228">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-229">**InterlockedIncrement16**</span><span class="sxs-lookup"><span data-stu-id="c6877-229">**InterlockedIncrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

<span data-ttu-id="c6877-230">Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht).</span><span class="sxs-lookup"><span data-stu-id="c6877-230">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-232">Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht).</span><span class="sxs-lookup"><span data-stu-id="c6877-232">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-233">Der Vorgang wird mithilfe der Semantik zum Abrufen der Speicher Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-233">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-235">Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht).</span><span class="sxs-lookup"><span data-stu-id="c6877-235">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-236">Der Vorgang wird mithilfe der Semantik der releasespeicherreihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6877-236">The operation is performed using release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-238">Erhöht den Wert der angegebenen 16-Bit-Variablen als atomarischen Vorgang (um 1 erhöht).</span><span class="sxs-lookup"><span data-stu-id="c6877-238">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-239">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-239">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-241">Erhöht den Wert der angegebenen 64-Bit-Variablen als atomarischen Vorgang (um 1 erhöht).</span><span class="sxs-lookup"><span data-stu-id="c6877-241">Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="c6877-242">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-242">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-243">[**Interlockedornofence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-244">Führt eine atomarische OR-Operation für die angegebenen **langen** Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-244">Performs an atomic OR operation on the specified **LONG** values.</span></span> <span data-ttu-id="c6877-245">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-245">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-247">Führt eine atomarische OR-Operation für die angegebenen **char** -Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-247">Performs an atomic OR operation on the specified **char** values.</span></span> <span data-ttu-id="c6877-248">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-248">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-250">Führt eine atomarische OR-Operation für die angegebenen **kurzwerte** aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-250">Performs an atomic OR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="c6877-251">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-251">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-253">Führt eine atomarische OR-Operation für die angegebenen **Longlong** -Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-253">Performs an atomic OR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="c6877-254">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-254">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-255">**Interlockedpushlistslistex**</span><span class="sxs-lookup"><span data-stu-id="c6877-255">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

<span data-ttu-id="c6877-256">Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein.</span><span class="sxs-lookup"><span data-stu-id="c6877-256">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="c6877-257">Der Zugriff auf die Listen wird auf einem Multiprozessorsystem synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c6877-257">Access to the lists is synchronized on a multiprocessor system.</span></span> <span data-ttu-id="c6877-258">Diese Version der-Methode verwendet nicht die [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) -Aufruf Konvention.</span><span class="sxs-lookup"><span data-stu-id="c6877-258">This version of the method does not use the [\_\_fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) calling convention.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-259">[**Interlockedxornofence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-260">Führt eine atomarische XOR-Operation für die angegebenen **langen** Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-260">Performs an atomic XOR operation on the specified **LONG** values.</span></span> <span data-ttu-id="c6877-261">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-261">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-263">Führt eine atomarische XOR-Operation für die angegebenen **char** -Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-263">Performs an atomic XOR operation on the specified **char** values.</span></span> <span data-ttu-id="c6877-264">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-264">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-266">Führt eine atomarische XOR-Operation für die angegebenen **kurzwerte** aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-266">Performs an atomic XOR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="c6877-267">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-267">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="c6877-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6877-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="c6877-269">Führt eine atomarische XOR-Operation für die angegebenen **Longlong** -Werte aus.</span><span class="sxs-lookup"><span data-stu-id="c6877-269">Performs an atomic XOR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="c6877-270">Der Vorgang wird atomarisch ausgeführt, ohne dass Speicherbarrieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6877-270">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> </dl>

## <a name="windows-7"></a><span data-ttu-id="c6877-271">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6877-271">Windows 7</span></span>

### <a name="new-functions"></a><span data-ttu-id="c6877-272">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="c6877-272">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="c6877-273">**Setwaitabletimerex**</span><span class="sxs-lookup"><span data-stu-id="c6877-273">**SetWaitableTimerEx**</span></span>](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

<span data-ttu-id="c6877-274">Aktiviert den angegebenen ausnutzbaren Timer und stellt Kontextinformationen für den Timer bereit.</span><span class="sxs-lookup"><span data-stu-id="c6877-274">Activates the specified waitable timer and provides context information for the timer.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-275">**Tryacquiresrwlockexclusive**</span><span class="sxs-lookup"><span data-stu-id="c6877-275">**TryAcquireSRWLockExclusive**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

<span data-ttu-id="c6877-276">Versucht, eine SRW-Sperre (Slim Reader/Writer) im exklusiven Modus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6877-276">Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode.</span></span> <span data-ttu-id="c6877-277">Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre.</span><span class="sxs-lookup"><span data-stu-id="c6877-277">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> <dt>

[<span data-ttu-id="c6877-278">**Tryacquiresrwlockshared**</span><span class="sxs-lookup"><span data-stu-id="c6877-278">**TryAcquireSRWLockShared**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

<span data-ttu-id="c6877-279">Versucht, eine SRW-Sperre (Slim Reader/Writer) im freigegebenen Modus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6877-279">Attempts to acquire a slim reader/writer (SRW) lock in shared mode.</span></span> <span data-ttu-id="c6877-280">Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre.</span><span class="sxs-lookup"><span data-stu-id="c6877-280">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> </dl>

### <a name="new-structures"></a><span data-ttu-id="c6877-281">Neue Strukturen</span><span class="sxs-lookup"><span data-stu-id="c6877-281">New Structures</span></span>

<dl> <dt>

[<span data-ttu-id="c6877-282">**Grund \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="c6877-282">**REASON\_CONTEXT**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

<span data-ttu-id="c6877-283">Enthält Kontextinformationen für einen mit [**setwaitabletimerex**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)aktivierten Timer.</span><span class="sxs-lookup"><span data-stu-id="c6877-283">Contains context information for a timer activated with [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span></span>

</dd> </dl>

 

 
