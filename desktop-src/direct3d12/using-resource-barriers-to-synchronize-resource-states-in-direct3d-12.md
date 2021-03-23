---
title: Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12
description: Um die CPU-Gesamtauslastung zu reduzieren und das Multithreading und die Vorverarbeitung von Treibern zu ermöglichen, verschiebt Direct3D 12 die Verantwortung für die Ressourcen übergreifende Zustands Verwaltung vom Grafiktreiber zur Anwendung.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104548741"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="03851-103">Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="03851-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="03851-104">Um die CPU-Gesamtauslastung zu reduzieren und das Multithreading und die Vorverarbeitung von Treibern zu ermöglichen, verschiebt Direct3D 12 die Verantwortung für die Ressourcen übergreifende Zustands Verwaltung vom Grafiktreiber zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="03851-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="03851-105">Ein Beispiel für den ressourcenbezogenen Status ist, ob auf eine Textur Ressource zurzeit als über einen Shader Ressourcenansicht oder als renderzielansicht zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="03851-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="03851-106">In Direct3D 11 waren Treiber erforderlich, um diesen Zustand im Hintergrund zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="03851-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="03851-107">Dies ist aus der CPU-Sicht aufwendig und erschwert jede Art von Multithreaded-Design erheblich.</span><span class="sxs-lookup"><span data-stu-id="03851-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="03851-108">In Microsoft Direct3D 12 werden die meisten Ressourcen pro Ressourcen von der Anwendung mit einer einzigen API, [**ID3D12GraphicsCommandList:: resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier), verwaltet.</span><span class="sxs-lookup"><span data-stu-id="03851-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="03851-109">Verwenden der resourcebarrier-API zum Verwalten des ressourcenbezogenen Zustands</span><span class="sxs-lookup"><span data-stu-id="03851-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="03851-110">Ressourcen Zustände</span><span class="sxs-lookup"><span data-stu-id="03851-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="03851-111">Anfängliche Zustände für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03851-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="03851-112">Ressourcen Zustands Einschränkungen für Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="03851-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="03851-113">Ressourcen Zustände für das darstellen von backpuffern</span><span class="sxs-lookup"><span data-stu-id="03851-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="03851-114">Verwerfen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03851-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="03851-115">Implizite Zustandsübergänge</span><span class="sxs-lookup"><span data-stu-id="03851-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="03851-116">Allgemeine Zustands herauf Stufung</span><span class="sxs-lookup"><span data-stu-id="03851-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="03851-117">Status Verfall in "Allgemein"</span><span class="sxs-lookup"><span data-stu-id="03851-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="03851-118">Folgen für die Leistung</span><span class="sxs-lookup"><span data-stu-id="03851-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="03851-119">Grenzen aufteilen</span><span class="sxs-lookup"><span data-stu-id="03851-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="03851-120">Beispielszenario für Ressourcen Barriere</span><span class="sxs-lookup"><span data-stu-id="03851-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="03851-121">Beispiel für allgemeine Zustands herauf Stufung und-Verfall</span><span class="sxs-lookup"><span data-stu-id="03851-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="03851-122">Beispiel für geteilte Barrieren</span><span class="sxs-lookup"><span data-stu-id="03851-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="03851-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="03851-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="03851-124">Verwenden der resourcebarrier-API zum Verwalten des ressourcenbezogenen Zustands</span><span class="sxs-lookup"><span data-stu-id="03851-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="03851-125">[**Resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) benachrichtigt den Grafiktreiber über Situationen, in denen der Treiber möglicherweise mehrere Zugriffe auf den Speicher synchronisieren muss, in dem eine Ressource gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="03851-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="03851-126">Die-Methode wird mit mindestens einer Ressourcen Barriere-Beschreibungs Struktur aufgerufen, die den Typ der zu deklarierten Ressourcen Barriere angibt.</span><span class="sxs-lookup"><span data-stu-id="03851-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="03851-127">Es gibt drei Arten von Ressourcen Barrieren:</span><span class="sxs-lookup"><span data-stu-id="03851-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="03851-128">**Übergangs Barriere** : eine Übergangs Barriere gibt an, dass ein Satz von untergeordneten Quellen zwischen unterschiedlichen Verwendungen übergeht.</span><span class="sxs-lookup"><span data-stu-id="03851-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="03851-129">Eine [**D3D12- \_ Ressourcen \_ Übergangs \_ Barriere**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) -Struktur wird verwendet, um die unter Berichts Quelle sowie den Zustand *vor* und *nach* der untergeordneten Quelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03851-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="03851-130">Das System überprüft, ob die Übergängen von untergeordneten Quellen in einer Befehlsliste mit vorherigen Übergängen in derselben Befehlsliste konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="03851-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="03851-131">Die debugschicht verfolgt den Status der untergeordneten Quelle weiter, um andere Fehler zu finden. diese Überprüfung ist jedoch konservativ und nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="03851-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="03851-132">Beachten Sie, dass Sie das Flag "D3D12 \_ Resource \_ Barrier \_ all unter Ressourcen" verwenden können, \_ um anzugeben, dass alle unter Ressourcen innerhalb einer Ressource übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="03851-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="03851-133">**Aliasing-Barriere** : eine Aliasing-Barriere gibt einen Übergang zwischen der Verwendung von zwei verschiedenen Ressourcen an, die überlappende Zuordnungen in denselben Heap haben.</span><span class="sxs-lookup"><span data-stu-id="03851-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="03851-134">Dies gilt für reservierte und Angestellte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="03851-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="03851-135">Eine [**D3D12 \_ \_ ressourcenaliasing- \_ Barriere**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) wird verwendet, um die *vorher* -Ressource und die *after* -Ressource anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03851-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="03851-136">Beachten Sie, dass eine oder beide Ressourcen NULL sein können, was bedeutet, dass jede gekachelte Ressource Aliasing verursachen könnte.</span><span class="sxs-lookup"><span data-stu-id="03851-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="03851-137">Weitere Informationen zum Verwenden von gekachelten Ressourcen finden Sie unter [gekachelte](../direct3d11/tiled-resources.md) Ressourcen und [Volumen Kachel Ressourcen](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="03851-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="03851-138">**Ungeordnete Zugriffsansicht (UAV) Barriere** -eine UAV-Barriere gibt an, dass alle UAV-Zugriffe, sowohl Lese-als auch Schreibzugriff auf eine bestimmte Ressource, zwischen allen zukünftigen UAV-Zugriffen, sowohl Lese-als auch Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="03851-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="03851-139">Es ist nicht erforderlich, dass eine APP eine UAV-Barriere zwischen zwei Draw-oder Dispatch-aufrufen platziert, die nur aus einer UAV gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="03851-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="03851-140">Außerdem ist es nicht erforderlich, eine UAV-Barriere zwischen zwei Draw-oder Dispatch-aufrufen zu platzieren, die in dieselbe UAV schreiben, wenn die Anwendung weiß, dass es sicher ist, dass der UAV-Zugriff in beliebiger Reihenfolge ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="03851-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="03851-141">Eine [**D3D12 \_ Resource \_ UAV- \_ Sperrungs**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) Struktur wird verwendet, um die UAV-Ressource anzugeben, für die die Barriere gilt.</span><span class="sxs-lookup"><span data-stu-id="03851-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="03851-142">Die Anwendung kann für die UAV der Barriere NULL angeben. Dies bedeutet, dass jeder UAV-Zugriff die Barriere erfordern könnte.</span><span class="sxs-lookup"><span data-stu-id="03851-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="03851-143">Wenn [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) mit einem Array von Ressourcen Sperr Beschreibungen aufgerufen wird, verhält sich die API so, als ob Sie einmal für jedes Element in der Reihenfolge aufgerufen wurde, in der Sie bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="03851-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="03851-144">Ein unter Bericht befindet sich zu einem beliebigen Zeitpunkt in genau einem Zustand, der durch den Satz von [**D3D12- \_ ressourcenstatusflags \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) festgelegt wird, die für [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="03851-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="03851-145">Die Anwendung muss sicherstellen, dass der Zustand *vor* und *nach* aufeinander folgender Aufrufe von **resourcebarrier** zustimmt.</span><span class="sxs-lookup"><span data-stu-id="03851-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="03851-146">Anwendungen sollten nach Möglichkeit mehrere Übergänge in einen API-Befehl stapeln.</span><span class="sxs-lookup"><span data-stu-id="03851-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="03851-147">Ressourcen Zustände</span><span class="sxs-lookup"><span data-stu-id="03851-147">Resource states</span></span>

<span data-ttu-id="03851-148">Eine umfassende Liste mit Ressourcen Zuständen, zwischen denen eine Ressource wechseln kann, finden Sie im Referenz Thema für die [**D3D12 \_ Resource \_ States**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="03851-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="03851-149">Informationen zu Teilen von Ressourcen Barrieren finden Sie auch unter [**D3D12 \_ \_ ressourcensperrenflags \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="03851-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="03851-150">Anfängliche Zustände für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03851-150">Initial states for resources</span></span>

<span data-ttu-id="03851-151">Ressourcen können mit einem beliebigen benutzerdefinierten Anfangszustand (gültig für die Ressourcen Beschreibung) mit den folgenden Ausnahmen erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="03851-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="03851-152">Das Hochladen von Heaps muss im Zustand "State D3D12 \_ Resource \_ State Generic Read" beginnen. \_ \_ Dies ist eine bitweise OR-Kombination aus:</span><span class="sxs-lookup"><span data-stu-id="03851-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="03851-153">D3D12 \_ Resource \_ State \_ -Scheitelpunkt \_ und \_ \_ Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="03851-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="03851-154">D3D12 \_ Resource \_ State \_ Index- \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="03851-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="03851-155">D3D12 \_ ressourcenstatuskopie- \_ \_ \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="03851-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="03851-156">D3D12 \_ Resource \_ State- \_ nicht-Pixel- \_ \_ Shader- \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="03851-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="03851-157">D3D12 \_ Resource \_ State- \_ Pixel- \_ Shader- \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="03851-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="03851-158">D3D12 \_ \_ \_ indirektes Argument des Ressourcen Zustands \_</span><span class="sxs-lookup"><span data-stu-id="03851-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="03851-159">Das Lesen von Heaps muss mit dem Status "D3D12 \_ Resource \_ State \_ Copy \_ dest" beginnen.</span><span class="sxs-lookup"><span data-stu-id="03851-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="03851-160">Austausch Ketten-Back-Puffer beginnen automatisch mit dem \_ allgemeinen Status des D3D12-Ressourcen \_ Zustands \_ .</span><span class="sxs-lookup"><span data-stu-id="03851-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="03851-161">Bevor ein Heap das Ziel eines GPU-Kopiervorgangs sein kann, muss der Heap normalerweise zuerst in den Zustand "D3D12 \_ Resource \_ State \_ Copy \_ dest" übergeht.</span><span class="sxs-lookup"><span data-stu-id="03851-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="03851-162">Beim Hochladen von Heaps erstellte Ressourcen müssen jedoch in gestartet werden und können sich nicht vom generischen \_ Lese Zustand ändern, da nur die CPU Schreibvorgänge durchführt.</span><span class="sxs-lookup"><span data-stu-id="03851-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="03851-163">Umgekehrt müssen in den Rückmeldungen erstellte Ressourcen mit zugesichertem Commit in gestartet werden und können sich nicht im Zustand "Kopie dest" ändern \_ .</span><span class="sxs-lookup"><span data-stu-id="03851-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="03851-164">Ressourcen Zustands Einschränkungen für Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="03851-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="03851-165">Die Verwendungs Bits des Ressourcen Zustands, die zur Beschreibung eines Ressourcen Status verwendet werden, sind in schreibgeschützte und Lese-/schreibzustände unterteilt.</span><span class="sxs-lookup"><span data-stu-id="03851-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="03851-166">Das Referenz Thema für den [**D3D12 \_ - \_ Ressourcen**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) Status gibt die Lese-/Schreib-Zugriffsebene für jedes Bit in der-Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="03851-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="03851-167">Höchstens ein Lese-/schreibbit kann für jede Ressource festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="03851-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="03851-168">Wenn ein Schreib Bit festgelegt ist, kann für diese Ressource kein Schreib geschütztes Bit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="03851-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="03851-169">Wenn kein Schreib Bit festgelegt ist, kann eine beliebige Anzahl von gelesenen Bits festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="03851-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="03851-170">Ressourcen Zustände für das darstellen von backpuffern</span><span class="sxs-lookup"><span data-stu-id="03851-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="03851-171">Bevor ein Hintergrund Puffer angezeigt wird, muss er sich im Status "D3D12 \_ Resource \_ State Common" befinden \_ .</span><span class="sxs-lookup"><span data-stu-id="03851-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="03851-172">Beachten Sie, dass der Ressourcen Status D3D12 der \_ Ressourcen Status \_ \_ ist ein Synonym für den \_ allgemeinen D3D12 \_ -Ressourcen Status \_ und beide den Wert 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="03851-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="03851-173">Wenn [**idxgiswapchain::P Resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (oder [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) für eine Ressource aufgerufen wird, die sich zurzeit nicht in diesem Zustand befindet, wird eine debugebenenwarnung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="03851-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="03851-174">Verwerfen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03851-174">Discarding resources</span></span>

<span data-ttu-id="03851-175">Alle unter Ressourcen in einer Ressource müssen den \_ renderzielstatus oder den tiefen \_ Schreib Zustand für Renderziele/tiefen Schablone-Ressourcen aufweisen, wenn [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="03851-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="03851-176">Implizite Zustandsübergänge</span><span class="sxs-lookup"><span data-stu-id="03851-176">Implicit State Transitions</span></span>

<span data-ttu-id="03851-177">Ressourcen können nur "höher gestuft" aus dem allgemeinen D3D12- \_ Ressourcen \_ Status werden \_ .</span><span class="sxs-lookup"><span data-stu-id="03851-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="03851-178">Ebenso werden Ressourcen nur für den gemeinsamen D3D12- \_ Ressourcen \_ Status verwendet \_ .</span><span class="sxs-lookup"><span data-stu-id="03851-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="03851-179">Allgemeine Zustands herauf Stufung</span><span class="sxs-lookup"><span data-stu-id="03851-179">Common state promotion</span></span>

<span data-ttu-id="03851-180">Alle Puffer Ressourcen und Texturen mit dem D3D12- \_ \_ ressourcenflag \_ Allow \_ gleichzeitige \_ Zugriffs Kennzeichen werden implizit von dem D3D12- \_ Ressourcen Status herauf gestuft \_ \_ , der für den ersten GPU-Zugriff auf den entsprechenden Status festgelegt ist, einschließlich des generischen Lese Zugriffs, \_ um alle Lese Szenarien abzudecken.</span><span class="sxs-lookup"><span data-stu-id="03851-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="03851-181">Auf jede Ressource im gemeinsamen Zustand kann zugegriffen werden, während Sie sich in einem einzelnen Zustand mit</span><span class="sxs-lookup"><span data-stu-id="03851-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="03851-182">1 Schreibflag oder</span><span class="sxs-lookup"><span data-stu-id="03851-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="03851-183">mindestens 1 leseflags</span><span class="sxs-lookup"><span data-stu-id="03851-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="03851-184">Ressourcen können basierend auf der folgenden Tabelle aus dem allgemeinen Status herauf gestuft werden:</span><span class="sxs-lookup"><span data-stu-id="03851-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="03851-185">Statusflag</span><span class="sxs-lookup"><span data-stu-id="03851-185">State flag</span></span>                    | <span data-ttu-id="03851-186">Erweiterbarer Zustand</span><span class="sxs-lookup"><span data-stu-id="03851-186">Promotable State</span></span>                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | <span data-ttu-id="03851-187">**Puffer-und Simultaneous-Access Texturen**</span><span class="sxs-lookup"><span data-stu-id="03851-187">**Buffers and Simultaneous-Access Textures**</span></span> | <span data-ttu-id="03851-188">**Nicht gleichzeitige Zugriffs Texturen**</span><span class="sxs-lookup"><span data-stu-id="03851-188">**Non-Simultaneous-Access Textures**</span></span> |
| <span data-ttu-id="03851-189">Vertex \_ und \_ konstanter \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="03851-189">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="03851-190">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-190">Yes</span></span>                                          | <span data-ttu-id="03851-191">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-191">No</span></span>                                   |
| <span data-ttu-id="03851-192">Index \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="03851-192">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="03851-193">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-193">Yes</span></span>                                          | <span data-ttu-id="03851-194">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-194">No</span></span>                                   |
| <span data-ttu-id="03851-195">\_Renderziel</span><span class="sxs-lookup"><span data-stu-id="03851-195">RENDER\_TARGET</span></span>                | <span data-ttu-id="03851-196">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-196">Yes</span></span>                                          | <span data-ttu-id="03851-197">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-197">No</span></span>                                   |
| <span data-ttu-id="03851-198">unsortierter \_ Zugriff</span><span class="sxs-lookup"><span data-stu-id="03851-198">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="03851-199">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-199">Yes</span></span>                                          | <span data-ttu-id="03851-200">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-200">No</span></span>                                   |
| <span data-ttu-id="03851-201">Ausführlichere \_ Schreibvorgänge</span><span class="sxs-lookup"><span data-stu-id="03851-201">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="03851-202">Nein<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="03851-202">No<sup>\*</sup></span></span>                              | <span data-ttu-id="03851-203">No</span><span class="sxs-lookup"><span data-stu-id="03851-203">No</span></span>                                   |
| <span data-ttu-id="03851-204">\_Lesetiefe</span><span class="sxs-lookup"><span data-stu-id="03851-204">DEPTH\_READ</span></span>                   | <span data-ttu-id="03851-205">Nein<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="03851-205">No<sup>\*</sup></span></span>                              | <span data-ttu-id="03851-206">No</span><span class="sxs-lookup"><span data-stu-id="03851-206">No</span></span>                                   |
| <span data-ttu-id="03851-207">nicht \_ Pixel- \_ Shader- \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="03851-207">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="03851-208">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-208">Yes</span></span>                                          | <span data-ttu-id="03851-209">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-209">Yes</span></span>                                  |
| <span data-ttu-id="03851-210">Pixel- \_ Shader- \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="03851-210">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="03851-211">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-211">Yes</span></span>                                          | <span data-ttu-id="03851-212">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-212">Yes</span></span>                                  |
| <span data-ttu-id="03851-213">Stream \_ ausgehend</span><span class="sxs-lookup"><span data-stu-id="03851-213">STREAM\_OUT</span></span>                   | <span data-ttu-id="03851-214">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-214">Yes</span></span>                                          | <span data-ttu-id="03851-215">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-215">No</span></span>                                   |
| <span data-ttu-id="03851-216">indirektes \_ Argument</span><span class="sxs-lookup"><span data-stu-id="03851-216">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="03851-217">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-217">Yes</span></span>                                          | <span data-ttu-id="03851-218">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-218">No</span></span>                                   |
| <span data-ttu-id="03851-219">Kopie \_ dest</span><span class="sxs-lookup"><span data-stu-id="03851-219">COPY\_DEST</span></span>                    | <span data-ttu-id="03851-220">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-220">Yes</span></span>                                          | <span data-ttu-id="03851-221">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-221">Yes</span></span>                                  |
| <span data-ttu-id="03851-222">\_Quelle kopieren</span><span class="sxs-lookup"><span data-stu-id="03851-222">COPY\_SOURCE</span></span>                  | <span data-ttu-id="03851-223">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-223">Yes</span></span>                                          | <span data-ttu-id="03851-224">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-224">Yes</span></span>                                  |
| <span data-ttu-id="03851-225">\_dest auflösen</span><span class="sxs-lookup"><span data-stu-id="03851-225">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="03851-226">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-226">Yes</span></span>                                          | <span data-ttu-id="03851-227">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-227">No</span></span>                                   |
| <span data-ttu-id="03851-228">\_Quelle auflösen</span><span class="sxs-lookup"><span data-stu-id="03851-228">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="03851-229">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-229">Yes</span></span>                                          | <span data-ttu-id="03851-230">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-230">No</span></span>                                   |
| <span data-ttu-id="03851-231">Prädikation übersprungen</span><span class="sxs-lookup"><span data-stu-id="03851-231">PREDICATION</span></span>                   | <span data-ttu-id="03851-232">Ja</span><span class="sxs-lookup"><span data-stu-id="03851-232">Yes</span></span>                                          | <span data-ttu-id="03851-233">Nein</span><span class="sxs-lookup"><span data-stu-id="03851-233">No</span></span>                                   |



 

<span data-ttu-id="03851-234"><sup>\*</sup>Tiefen Schablonen Ressourcen müssen nicht gleichzeitig auf Texturen zugreifen und können daher nie implizit herauf gestuft werden.</span><span class="sxs-lookup"><span data-stu-id="03851-234"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="03851-235">Wenn dieser Zugriff auftritt, verhält sich die herauf Stufung wie eine implizite Ressourcen Barriere.</span><span class="sxs-lookup"><span data-stu-id="03851-235">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="03851-236">Bei nachfolgenden Zugriffen werden Ressourcen Sperren benötigt, um den Ressourcen Status bei Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="03851-236">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="03851-237">Beachten Sie, dass die herauf Stufung von einem höher gestuften Lese Zustand in den Zustand "mehrere Lesevorgänge" gültig ist, dies jedoch nicht für Schreib Zustände gilt.</span><span class="sxs-lookup"><span data-stu-id="03851-237">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="03851-238">Wenn z. b. eine Ressource im gemeinsamen Zustand in einem zeichnen-Befehl zu einer Pixel-Shader-Ressource herauf gestuft wird \_ \_ , kann Sie weiterhin zu NON_PIXEL \_ Shader- \_ Ressource herauf gestuft werden. Pixel- \_ Shader- \_ Ressource in einem anderen Draw-Befehl.</span><span class="sxs-lookup"><span data-stu-id="03851-238">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="03851-239">Wenn Sie jedoch in einem Schreibvorgang, z. b. einem Kopier Ziel, verwendet wird, wird eine Ressourcen Zustands Übergangs Barriere von den kombinierten höher gestuften Lese Zuständen hier NON_PIXEL \_ Shader- \_ Ressource | Die Pixel- \_ Shader- \_ Ressource zum Kopieren der dest-Ressource \_ ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="03851-239">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="03851-240">Ebenso muss bei herauf Stufung von Common zum Kopieren \_ dest noch eine Barriere von der Kopie \_ dest zum Renderziel gewechselt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="03851-240">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="03851-241">Beachten Sie, dass die gemeinsame Zustands herauf Stufung "kostenlos" ist, da die GPU keine Synchronisierungs Wartezeiten ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="03851-241">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="03851-242">Die herauf Stufung stellt die Tatsache dar, dass Ressourcen im gemeinsamen Zustand keine zusätzliche GPU-Arbeit oder Treiber Nachverfolgung benötigen, um bestimmte Zugriffe zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="03851-242">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="03851-243">Status Verfall in "Allgemein"</span><span class="sxs-lookup"><span data-stu-id="03851-243">State decay to common</span></span>

<span data-ttu-id="03851-244">Die Kehrseite der allgemeinen herauf Stufung des Zustands wird wieder in den allgemeinen D3D12- \_ Ressourcen Status zurückversetzt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="03851-244">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="03851-245">Ressourcen, die bestimmte Anforderungen erfüllen, werden als zustandslos angesehen und werden effektiv in den gemeinsamen Zustand zurückversetzt, wenn die GPU die Ausführung eines [**executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) -Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="03851-245">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="03851-246">Der Zerfall tritt nicht zwischen Befehlslisten auf, die gemeinsam im selben **executecommandlists** -Befehl ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="03851-246">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="03851-247">Die folgenden Ressourcen verfallen, wenn ein [**executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) -Vorgang auf der GPU abgeschlossen ist:</span><span class="sxs-lookup"><span data-stu-id="03851-247">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="03851-248">Ressourcen, auf die in einer Kopier Warteschlange zugegriffen wird, *oder*</span><span class="sxs-lookup"><span data-stu-id="03851-248">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="03851-249">Puffer Ressourcen für beliebige Warteschlangen Typen *oder*</span><span class="sxs-lookup"><span data-stu-id="03851-249">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="03851-250">Textur Ressourcen für beliebige Warteschlangen Typen, für die das D3D12- \_ \_ ressourcenflag das \_ \_ gleichzeitige \_ Zugriffsflag zulässt, *oder*</span><span class="sxs-lookup"><span data-stu-id="03851-250">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="03851-251">Alle Ressourcen, die implizit in einen schreibgeschützten Zustand herauf gestuft wurden.</span><span class="sxs-lookup"><span data-stu-id="03851-251">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="03851-252">Wie bei der allgemeinen herauf Stufung ist der Verfall in kostenlos, da keine zusätzliche Synchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="03851-252">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="03851-253">Durch die Kombination von Common State Promotion und Decay können viele unnötige [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Übergänge vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="03851-253">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="03851-254">In einigen Fällen kann dies erhebliche Leistungsverbesserungen bieten.</span><span class="sxs-lookup"><span data-stu-id="03851-254">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="03851-255">Puffer und Simultaneous-Access Ressourcen werden in den gemeinsamen Zustand übergehen, unabhängig davon, ob Sie explizit mithilfe von Ressourcen Barrieren oder implizit höher gestuft wurden.</span><span class="sxs-lookup"><span data-stu-id="03851-255">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="03851-256">Folgen für die Leistung</span><span class="sxs-lookup"><span data-stu-id="03851-256">Performance implications</span></span>

<span data-ttu-id="03851-257">Beim Aufzeichnen expliziter [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Übergänge für Ressourcen im gemeinsamen Zustand ist es richtig, entweder "D3D12 \_ Resource \_ State \_ Common" oder einen beliebigen heraufstufbaren Zustand als " *beforestate* "-Wert in der D3D12- \_ Ressourcen \_ Übergangs \_ Barriere-Struktur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="03851-257">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="03851-258">Dies ermöglicht eine herkömmliche Zustands Verwaltung, bei der der automatische Zerfall von Puffern und Texturen mit gleichzeitigem Zugriff ignoriert wird</span><span class="sxs-lookup"><span data-stu-id="03851-258">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="03851-259">Dies ist jedoch möglicherweise nicht wünschenswert, da der Übergang von **resourcebarrier** -aufrufen mit Ressourcen, die bekanntermaßen den gemeinsamen Zustand aufweisen, die Leistung erheblich verbessern kann.</span><span class="sxs-lookup"><span data-stu-id="03851-259">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="03851-260">Ressourcen Barrieren können teuer sein.</span><span class="sxs-lookup"><span data-stu-id="03851-260">Resource barriers can be expensive.</span></span> <span data-ttu-id="03851-261">Sie sind darauf ausgelegt, Cache Leerungen, Änderungen am Arbeitsspeicher Layout und andere Synchronisierungen zu erzwingen, die für Ressourcen, die sich bereits im gemeinsamen Zustand befinden, nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="03851-261">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="03851-262">Eine Befehlsliste, in der eine Ressourcen Barriere von einem nicht gemeinsamen Zustand zu einem anderen nicht allgemeinen Zustand für eine Ressource verwendet wird, die sich derzeit im gemeinsamen Status befindet, kann zu einem viel unbenötigten Aufwand führen.</span><span class="sxs-lookup"><span data-stu-id="03851-262">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="03851-263">Vermeiden Sie außerdem explizite [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Übergänge in \_ den D3D12-Ressourcen \_ Status, \_ sofern dies nicht unbedingt erforderlich ist (z. b. der nächste Zugriff auf eine Kopier Befehls Warteschlange, die erfordert, dass Ressourcen mit einem gemeinsamen Zustand beginnen).</span><span class="sxs-lookup"><span data-stu-id="03851-263">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="03851-264">Übermäßige Übergänge in den gemeinsamen Status können die GPU-Leistung erheblich verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="03851-264">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="03851-265">Versuchen Sie sich zusammenfassend, sich auf allgemeine Zustands herauf Stufung und-Verfall zu verlassen, wenn die Semantik Ihnen ermöglicht, keine [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Aufrufe auszugeben.</span><span class="sxs-lookup"><span data-stu-id="03851-265">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="03851-266">Grenzen aufteilen</span><span class="sxs-lookup"><span data-stu-id="03851-266">Split Barriers</span></span>

<span data-ttu-id="03851-267">Eine Ressourcen Übergangs Barriere mit dem Flag "D3D12 \_ Resource \_ Barrier \_ Flag \_ Begin \_ only" beginnt eine geteilte Barriere, und die Übergangs Barriere wird als ausstehend bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="03851-267">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="03851-268">Während der Barriere steht, kann die (Sub)-Ressource nicht von der GPU gelesen oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="03851-268">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="03851-269">Die einzige zulässige Übergangs Barriere, die auf eine (Sub)-Ressource mit einer ausstehenden Barriere angewendet werden kann, ist eine, die *vor* und *nach* den Zuständen gleich ist, und das \_ Flag D3D12 Resource \_ Barrier \_ Flag \_ End \_ only, das die Grenze für den ausstehenden Übergang abschließt.</span><span class="sxs-lookup"><span data-stu-id="03851-269">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="03851-270">Geteilte Barrieren stellen Hinweise für die GPU bereit, dass eine Ressource in Bundesland *a* später später in Bundesland *B* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03851-270">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="03851-271">Dadurch kann die GPU die Übergangs Arbeitsauslastung optimieren und Ausführungs Staus möglicherweise verringern oder eliminieren.</span><span class="sxs-lookup"><span data-stu-id="03851-271">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="03851-272">Das Ausstellen der reinen Sperre gewährleistet, dass alle GPU-Übergangs Aufgaben abgeschlossen sind, bevor Sie mit dem nächsten Befehl fortfahren.</span><span class="sxs-lookup"><span data-stu-id="03851-272">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="03851-273">Die Verwendung von Teilungs Barrieren kann zur Verbesserung der Leistung beitragen, insbesondere in Szenarios mit mehreren Engines oder bei der Umstellung von Ressourcen mit Lese-/Schreibzugriff in einer oder mehreren Befehlslisten.</span><span class="sxs-lookup"><span data-stu-id="03851-273">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="03851-274">Beispielszenario für Ressourcen Barriere</span><span class="sxs-lookup"><span data-stu-id="03851-274">Resource barrier example scenario</span></span>

<span data-ttu-id="03851-275">Die folgenden Code Ausschnitte zeigen die Verwendung der [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Methode in einem Multithreading-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="03851-275">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="03851-276">Erstellen der Ansicht "tiefen Schablone", die in einen beschreibbaren Zustand übergeht.</span><span class="sxs-lookup"><span data-stu-id="03851-276">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



<span data-ttu-id="03851-277">Erstellen der vertexpufferansicht, ändern Sie Sie zuerst von einem gemeinsamen Zustand in ein Ziel und dann von einem Ziel in einen generischen lesbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="03851-277">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



<span data-ttu-id="03851-278">Erstellen der Index Puffer Ansicht, ändern Sie Sie zuerst von einem gemeinsamen Zustand in ein Ziel und dann von einem Ziel in einen allgemeinen lesbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="03851-278">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



<span data-ttu-id="03851-279">Erstellen von Texturen und Shader-Ressourcen Ansichten.</span><span class="sxs-lookup"><span data-stu-id="03851-279">Creating textures and shader resource views.</span></span> <span data-ttu-id="03851-280">Die Textur wird von einem gemeinsamen Zustand in ein Ziel und dann von einem Ziel zu einer Pixel-Shader-Ressource geändert.</span><span class="sxs-lookup"><span data-stu-id="03851-280">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



<span data-ttu-id="03851-281">Beginnen eines Frames Dadurch wird nicht nur [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) verwendet, um anzugeben, dass der Swapkette als Renderziel verwendet werden soll, sondern auch die Frame-Ressource initialisiert (die **resourcebarrier** für den tiefen Schablone-Puffer aufruft).</span><span class="sxs-lookup"><span data-stu-id="03851-281">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



<span data-ttu-id="03851-282">Das Beenden eines Frames, der angibt, dass der Hintergrund Puffer jetzt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03851-282">Ending a frame, indicating the back buffer is now used to present.</span></span>


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



<span data-ttu-id="03851-283">Beim Initialisieren einer Frame Ressource, die beim Starten eines Frames aufgerufen wird, wird der tiefen Schablone-Puffer in einen beschreibbaren Puffer übergegangen.</span><span class="sxs-lookup"><span data-stu-id="03851-283">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



<span data-ttu-id="03851-284">Barrieren werden Mid-Frame ausgetauscht, wobei die Schatten Zuordnung vom beschreibbaren in lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="03851-284">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="03851-285">"Finish" wird aufgerufen, wenn ein Frame beendet wird, wobei die Schatten Zuordnung in einen gemeinsamen Zustand übergeht.</span><span class="sxs-lookup"><span data-stu-id="03851-285">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="03851-286">Beispiel für allgemeine Zustands herauf Stufung und-Verfall</span><span class="sxs-lookup"><span data-stu-id="03851-286">Common state promotion and decay sample</span></span>

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a><span data-ttu-id="03851-287">Beispiel für geteilte Barrieren</span><span class="sxs-lookup"><span data-stu-id="03851-287">Example of split barriers</span></span>

<span data-ttu-id="03851-288">Im folgenden Beispiel wird gezeigt, wie Sie eine geteilte Barriere zum Reduzieren von Pipeline Ständen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="03851-288">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="03851-289">Der folgende Code verwendet keine Splitter Barrieren:</span><span class="sxs-lookup"><span data-stu-id="03851-289">The code that follows does not use split barriers:</span></span>

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

<span data-ttu-id="03851-290">Der folgende Code verwendet geteilte Barrieren:</span><span class="sxs-lookup"><span data-stu-id="03851-290">The following code uses split barriers:</span></span>

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a><span data-ttu-id="03851-291">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="03851-291">Related topics</span></span>

[<span data-ttu-id="03851-292">Video-Tutorials zu DirectX Advanced Learning: Ressourcen Barrieren und Zustandsüberwachung</span><span class="sxs-lookup"><span data-stu-id="03851-292">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="03851-293">Multi-Engine-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="03851-293">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="03851-294">Arbeits Übermittlung in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="03851-294">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="03851-295">Ein Einblick in D3D12 Ressourcen Zustands Barrieren</span><span class="sxs-lookup"><span data-stu-id="03851-295">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

