---
title: Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen in Direct3D 12
description: Um die CPU-Gesamtauslastung zu reduzieren und Multithreading und Vorverarbeitung von Treibern zu ermöglichen, überträgt Direct3D 12 die Verantwortung für die ressourcenspezifische Zustandsverwaltung vom Grafiktreiber in die Anwendung.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343475"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="7a371-103">Verwenden von Ressourcenbarrieren zum Synchronisieren von Ressourcenzuständen in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7a371-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="7a371-104">Um die CPU-Gesamtauslastung zu reduzieren und Multithreading und Vorverarbeitung von Treibern zu ermöglichen, überträgt Direct3D 12 die Verantwortung für die ressourcenspezifische Zustandsverwaltung vom Grafiktreiber in die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7a371-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="7a371-105">Ein Beispiel für den ressourcenspezifischen Zustand ist, ob auf eine Texturressource derzeit als über einen Shader-Ressourcenansicht oder als Renderzielansicht zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7a371-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="7a371-106">In Direct3D 11 mussten Treiber diesen Zustand im Hintergrund nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="7a371-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="7a371-107">Dies ist aus CPU-Sicht teuer und erschwert jede Art von Multithreadentwurf erheblich.</span><span class="sxs-lookup"><span data-stu-id="7a371-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="7a371-108">In Microsoft Direct3D 12 wird der meiste Zustand pro Ressource von der Anwendung mit einer einzigen API verwaltet: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="7a371-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="7a371-109">Verwenden der ResourceBarrier-API zum Verwalten des Zustands pro Ressource</span><span class="sxs-lookup"><span data-stu-id="7a371-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="7a371-110">Ressourcenzustände</span><span class="sxs-lookup"><span data-stu-id="7a371-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="7a371-111">Anfangszustände für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a371-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="7a371-112">Einschränkungen für den Lese-/Schreibzustand der Ressource</span><span class="sxs-lookup"><span data-stu-id="7a371-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="7a371-113">Ressourcenzustände für die Präsentation von Puffern</span><span class="sxs-lookup"><span data-stu-id="7a371-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="7a371-114">Verwerfen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a371-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="7a371-115">Implizite Zustandsübergänge</span><span class="sxs-lookup"><span data-stu-id="7a371-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="7a371-116">Allgemeine Statusaufstufung</span><span class="sxs-lookup"><span data-stu-id="7a371-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="7a371-117">Zustandsverfall zu gemeinsamer</span><span class="sxs-lookup"><span data-stu-id="7a371-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="7a371-118">Folgen für die Leistung</span><span class="sxs-lookup"><span data-stu-id="7a371-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="7a371-119">Teilungsbarrieren</span><span class="sxs-lookup"><span data-stu-id="7a371-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="7a371-120">Beispielszenario für Ressourcenbarrieren</span><span class="sxs-lookup"><span data-stu-id="7a371-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="7a371-121">Beispiel für allgemeine Zustandsaufstufung und -zerfall</span><span class="sxs-lookup"><span data-stu-id="7a371-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="7a371-122">Beispiel für Teilungsbarrieren</span><span class="sxs-lookup"><span data-stu-id="7a371-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="7a371-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7a371-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="7a371-124">Verwenden der ResourceBarrier-API zum Verwalten des Ressourcenzustands pro Ressource</span><span class="sxs-lookup"><span data-stu-id="7a371-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="7a371-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) benachrichtigt den Grafiktreiber über Situationen, in denen der Treiber möglicherweise mehrere Zugriffe auf den Arbeitsspeicher synchronisieren muss, in dem eine Ressource gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7a371-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="7a371-126">Die -Methode wird mit einer oder mehreren Beschreibungsstrukturen der Ressourcenbarriere aufgerufen, die den Typ der deklarierten Ressourcenbarriere angeben.</span><span class="sxs-lookup"><span data-stu-id="7a371-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="7a371-127">Es gibt drei Arten von Ressourcenbarrieren:</span><span class="sxs-lookup"><span data-stu-id="7a371-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="7a371-128">**Übergangsbarriere:** Eine Übergangsbarriere gibt an, dass ein Satz von Unterressourcen zwischen verschiedenen Verwendungen übergehen soll.</span><span class="sxs-lookup"><span data-stu-id="7a371-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="7a371-129">Eine [**D3D12 \_ RESOURCE TRANSITION \_ \_ BARRIER-Struktur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) wird verwendet, um die Unterressource anzugeben, die den Übergang ausführt, sowie den *Vorher-* und *Nachher-Status* der Unterressource.</span><span class="sxs-lookup"><span data-stu-id="7a371-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="7a371-130">Das System überprüft, ob unterresource-Übergänge in einer Befehlsliste mit vorherigen Übergängen in derselben Befehlsliste konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="7a371-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="7a371-131">Die Debugebene verfolgt den Zustand der Unterressource weiter, um andere Fehler zu finden. Diese Überprüfung ist jedoch konservativer und nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="7a371-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="7a371-132">Beachten Sie, dass Sie das Flag D3D12 \_ RESOURCE \_ BARRIER ALL \_ \_ SUBRESOURCES verwenden können, um anzugeben, dass alle Unterressourcen innerhalb einer Ressource umgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="7a371-133">**Aliasing-Barriere:** Eine Aliasingbarriere gibt einen Übergang zwischen der Verwendung von zwei verschiedenen Ressourcen an, die überlappende Zuordnungen zum gleichen Heap aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a371-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="7a371-134">Dies gilt sowohl für reservierte als auch für platzierte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7a371-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="7a371-135">Eine [**D3D12 \_ RESOURCE \_ ALIASING \_ BARRIER-Struktur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) wird verwendet, um sowohl die *before-Ressource* als auch die *after-Ressource* anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7a371-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="7a371-136">Beachten Sie, dass eine oder beide Ressourcen NULL sein können, was darauf hinweist, dass jede gekachelte Ressource aliasing verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="7a371-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="7a371-137">Weitere Informationen zur Verwendung von gekachelten Ressourcen finden Sie unter [Kachelressourcen](../direct3d11/tiled-resources.md) und [Volumenkachelressourcen.](volume-tiled-resources.md)</span><span class="sxs-lookup"><span data-stu-id="7a371-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="7a371-138">**Unordered access view (UAV)-Barriere :** Eine UAV-Barriere gibt an, dass alle UAV-Zugriffe , sowohl Lese- als auch Schreibzugriffe, auf eine bestimmte Ressource zwischen allen zukünftigen UAV-Zugriffen (Sowohl Lese- als auch Schreibzugriff) abgeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7a371-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="7a371-139">Es ist nicht erforderlich, dass eine App eine UAV-Barriere zwischen zwei Draw- oder Dispatch-Aufrufen setzt, die nur aus einem UAV lesen.</span><span class="sxs-lookup"><span data-stu-id="7a371-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="7a371-140">Außerdem ist es nicht notwendig, eine UAV-Barriere zwischen zwei Draw- oder Dispatch-Aufrufen zu setzen, die in dieselbe UAV schreiben, wenn die Anwendung weiß, dass es sicher ist, den UAV-Zugriff in beliebiger Reihenfolge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7a371-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="7a371-141">Eine [**\_ \_ UAV \_ BARRIER-Struktur der D3D12-RESSOURCE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) wird verwendet, um die UAV-Ressource anzugeben, für die die Barriere gilt.</span><span class="sxs-lookup"><span data-stu-id="7a371-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="7a371-142">Die Anwendung kann NULL für die UAV der Barriere angeben, was darauf hinweist, dass jeder UAV-Zugriff die Barriere erfordern könnte.</span><span class="sxs-lookup"><span data-stu-id="7a371-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="7a371-143">Wenn [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) mit einem Array von Ressourcenbarrierenbeschreibungen aufgerufen wird, verhält sich die API so, als ob sie einmal für jedes Element in der Reihenfolge aufgerufen würde, in der sie bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7a371-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="7a371-144">Zu jedem Zeitpunkt befindet sich eine Unterressource in genau einem Zustand, der durch den Satz von [**D3D12 \_ RESOURCE \_ STATES-Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) bestimmt wird, die [**resourceBarrier bereitgestellt werden.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="7a371-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="7a371-145">Die Anwendung muss sicherstellen, dass *die Zustände vor* und *nach* aufeinander folgenden Aufrufen von **ResourceBarrier** zustimmen.</span><span class="sxs-lookup"><span data-stu-id="7a371-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="7a371-146">Anwendungen sollten nach Möglichkeit mehrere Übergänge in einen API-Aufruf batchen.</span><span class="sxs-lookup"><span data-stu-id="7a371-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="7a371-147">Ressourcenzustände</span><span class="sxs-lookup"><span data-stu-id="7a371-147">Resource states</span></span>

<span data-ttu-id="7a371-148">Die vollständige Liste der Ressourcenzustände, zwischen denen eine Ressource umstiegen kann, finden Sie im Referenzthema für die [**\_ RESOURCE \_ STATES-Enumeration D3D12.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="7a371-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="7a371-149">Informationen zu Split Resource Barriers finden Sie auch unter [**D3D12 \_ RESOURCE \_ BARRIER \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="7a371-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="7a371-150">Anfangszustände für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a371-150">Initial states for resources</span></span>

<span data-ttu-id="7a371-151">Ressourcen können mit einem beliebigen vom Benutzer angegebenen Anfangszustand erstellt werden (gültig für die Ressourcenbeschreibung), mit den folgenden Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="7a371-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="7a371-152">Upload heaps must start out in the state D3D12 RESOURCE STATE GENERIC READ (Hochladen von Heaps muss im Zustand D3D12 RESOURCE STATE GENERIC READ beginnen. Dabei handelt es sich \_ \_ um eine \_ \_ bitweise OR-Kombination aus:</span><span class="sxs-lookup"><span data-stu-id="7a371-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="7a371-153">D3D12 \_ RESOURCE \_ STATE \_ VERTEX \_ AND \_ CONSTANT \_ BUFFER</span><span class="sxs-lookup"><span data-stu-id="7a371-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="7a371-154">D3D12 \_ RESOURCE \_ STATE \_ INDEX \_ BUFFER</span><span class="sxs-lookup"><span data-stu-id="7a371-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="7a371-155">D3D12 \_ RESOURCE \_ STATE \_ COPY \_ SOURCE</span><span class="sxs-lookup"><span data-stu-id="7a371-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="7a371-156">RESSOURCE "D3D12 \_ RESOURCE STATE NON PIXEL \_ \_ \_ \_ \_ SHADER"</span><span class="sxs-lookup"><span data-stu-id="7a371-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="7a371-157">D3D12 \_ RESOURCE STATE PIXEL \_ \_ \_ \_ SHADER-RESSOURCE</span><span class="sxs-lookup"><span data-stu-id="7a371-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="7a371-158">D3D12 \_ RESOURCE \_ STATE \_ INDIRECT \_ ARGUMENT</span><span class="sxs-lookup"><span data-stu-id="7a371-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="7a371-159">Rückleseheaps müssen im Zustand D3D12 RESOURCE STATE COPY DEST gestartet \_ \_ \_ \_ werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="7a371-160">Swap chain back buffers automatically start out in the D3D12 \_ RESOURCE STATE COMMON state \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7a371-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="7a371-161">Bevor ein Heap das Ziel eines GPU-Kopiervorgangs sein kann, muss der Heap normalerweise zuerst in den Zustand D3D12 \_ RESOURCE STATE COPY DEST \_ übergehen. \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a371-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="7a371-162">Ressourcen, die auf UPLOADheaps erstellt werden, müssen jedoch in beginnen und können sich nicht vom \_ GENERISCHEN READ-Zustand ändern, da nur die CPU schreibe.</span><span class="sxs-lookup"><span data-stu-id="7a371-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="7a371-163">Umgekehrt müssen in READBACK-Heaps erstellte Ressourcen, für die ein Commit ausgeführt wurde, in beginnen und können sich nicht vom \_ COPY DEST-Zustand ändern.</span><span class="sxs-lookup"><span data-stu-id="7a371-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="7a371-164">Ressourcenzustandseinschränkungen für Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="7a371-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="7a371-165">Die Ressourcenzustandsnutzungsbits, die zum Beschreiben eines Ressourcenzustands verwendet werden, werden in schreibgeschützte und Lese-/Schreibzustände unterteilt.</span><span class="sxs-lookup"><span data-stu-id="7a371-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="7a371-166">Das Referenzthema für [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) gibt die Lese-/Schreibzugriffsebene für jedes Bit in der Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="7a371-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="7a371-167">Für jede Ressource kann höchstens ein Lese-/Schreibbit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="7a371-168">Wenn ein Schreibbit festgelegt ist, kann kein schreibgeschütztes Bit für diese Ressource festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="7a371-169">Wenn kein Schreibbit festgelegt ist, kann eine beliebige Anzahl von Lesebits festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="7a371-170">Ressourcenzustände für die Darstellung von Puffern</span><span class="sxs-lookup"><span data-stu-id="7a371-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="7a371-171">Bevor ein Hintergrundpuffer angezeigt wird, muss er sich im Zustand D3D12 \_ RESOURCE \_ STATE COMMON \_ befinden.</span><span class="sxs-lookup"><span data-stu-id="7a371-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="7a371-172">Beachten Sie, dass der Ressourcenzustand D3D12 \_ RESOURCE STATE PRESENT ein Synonym für \_ \_ D3D12 RESOURCE STATE COMMON ist \_ und beide den Wert \_ \_ 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a371-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="7a371-173">Wenn [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (oder [**IDXGISwapChain1::P resent1)**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)für eine Ressource aufgerufen wird, die sich derzeit nicht in diesem Zustand befindet, wird eine Warnung der Debugebene ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a371-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="7a371-174">Verwerfen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a371-174">Discarding resources</span></span>

<span data-ttu-id="7a371-175">Alle Unterressourcen in einer Ressource müssen den Zustand RENDER TARGET oder DEPTH WRITE für Renderziele bzw. Tiefen-Schablonenressourcen haben, wenn \_ \_ [**ID3D12GraphicsCommandList::D iscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7a371-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="7a371-176">Implizite Zustandsübergänge</span><span class="sxs-lookup"><span data-stu-id="7a371-176">Implicit State Transitions</span></span>

<span data-ttu-id="7a371-177">Ressourcen können nur aus D3D12 \_ RESOURCE STATE COMMON "promoted" \_ \_ werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="7a371-178">Ebenso werden Ressourcen nur in D3D12 \_ RESOURCE STATE COMMON "verfällt". \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a371-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="7a371-179">Allgemeine Statusaufstufung</span><span class="sxs-lookup"><span data-stu-id="7a371-179">Common state promotion</span></span>

<span data-ttu-id="7a371-180">Alle Pufferressourcen sowie Texturen mit dem D3D12 RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS-Flag werden implizit von \_ \_ \_ \_ \_ D3D12 RESOURCE STATE \_ COMMON \_ \_ \_ auf den relevanten Zustand beim ersten GPU-Zugriff hoch 2012, einschließlich GENERISCHER LESEzugriff, um alle Leseszenarios abdecken zu können.</span><span class="sxs-lookup"><span data-stu-id="7a371-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="7a371-181">Auf jede Ressource im Common-Zustand kann so zugegriffen werden, als ob sie sich in einem einzigen Zustand mit</span><span class="sxs-lookup"><span data-stu-id="7a371-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="7a371-182">1 WRITE-Flag oder</span><span class="sxs-lookup"><span data-stu-id="7a371-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="7a371-183">1 oder mehr READ-Flags</span><span class="sxs-lookup"><span data-stu-id="7a371-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="7a371-184">Ressourcen können basierend auf der folgenden Tabelle aus dem COMMON-Status promotet werden:</span><span class="sxs-lookup"><span data-stu-id="7a371-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="7a371-185">Statusflag</span><span class="sxs-lookup"><span data-stu-id="7a371-185">State flag</span></span>                    | <span data-ttu-id="7a371-186">Puffer und Simultaneous-Access Texturen</span><span class="sxs-lookup"><span data-stu-id="7a371-186">Buffers and Simultaneous-Access Textures</span></span>                             | <span data-ttu-id="7a371-187">Texturen ohne gleichzeitigen Zugriff</span><span class="sxs-lookup"><span data-stu-id="7a371-187">Non-Simultaneous-Access Textures</span></span>                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| <span data-ttu-id="7a371-188">\_SCHEITELPUNKT UND \_ KONSTANTER \_ PUFFER</span><span class="sxs-lookup"><span data-stu-id="7a371-188">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="7a371-189">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-189">Yes</span></span>                                          | <span data-ttu-id="7a371-190">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-190">No</span></span>                                   |
| <span data-ttu-id="7a371-191">INDEX \_ BUFFER</span><span class="sxs-lookup"><span data-stu-id="7a371-191">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="7a371-192">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-192">Yes</span></span>                                          | <span data-ttu-id="7a371-193">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-193">No</span></span>                                   |
| <span data-ttu-id="7a371-194">\_RENDERZIEL</span><span class="sxs-lookup"><span data-stu-id="7a371-194">RENDER\_TARGET</span></span>                | <span data-ttu-id="7a371-195">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-195">Yes</span></span>                                          | <span data-ttu-id="7a371-196">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-196">No</span></span>                                   |
| <span data-ttu-id="7a371-197">UNGEORDNETER \_ ZUGRIFF</span><span class="sxs-lookup"><span data-stu-id="7a371-197">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="7a371-198">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-198">Yes</span></span>                                          | <span data-ttu-id="7a371-199">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-199">No</span></span>                                   |
| <span data-ttu-id="7a371-200">\_TIEFENSCHREIBEN</span><span class="sxs-lookup"><span data-stu-id="7a371-200">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="7a371-201">Nein<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7a371-201">No<sup>\*</sup></span></span>                              | <span data-ttu-id="7a371-202">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-202">No</span></span>                                   |
| <span data-ttu-id="7a371-203">\_TIEFENLESE</span><span class="sxs-lookup"><span data-stu-id="7a371-203">DEPTH\_READ</span></span>                   | <span data-ttu-id="7a371-204">Nein<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7a371-204">No<sup>\*</sup></span></span>                              | <span data-ttu-id="7a371-205">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-205">No</span></span>                                   |
| <span data-ttu-id="7a371-206">NICHT \_ \_ PIXEL-SHADERRESSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="7a371-206">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="7a371-207">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-207">Yes</span></span>                                          | <span data-ttu-id="7a371-208">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-208">Yes</span></span>                                  |
| <span data-ttu-id="7a371-209">\_ \_ PIXEL-SHADERRESSOURCE</span><span class="sxs-lookup"><span data-stu-id="7a371-209">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="7a371-210">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-210">Yes</span></span>                                          | <span data-ttu-id="7a371-211">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-211">Yes</span></span>                                  |
| <span data-ttu-id="7a371-212">STREAM \_ OUT</span><span class="sxs-lookup"><span data-stu-id="7a371-212">STREAM\_OUT</span></span>                   | <span data-ttu-id="7a371-213">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-213">Yes</span></span>                                          | <span data-ttu-id="7a371-214">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-214">No</span></span>                                   |
| <span data-ttu-id="7a371-215">INDIREKTES \_ ARGUMENT</span><span class="sxs-lookup"><span data-stu-id="7a371-215">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="7a371-216">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-216">Yes</span></span>                                          | <span data-ttu-id="7a371-217">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-217">No</span></span>                                   |
| <span data-ttu-id="7a371-218">COPY \_ DEST</span><span class="sxs-lookup"><span data-stu-id="7a371-218">COPY\_DEST</span></span>                    | <span data-ttu-id="7a371-219">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-219">Yes</span></span>                                          | <span data-ttu-id="7a371-220">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-220">Yes</span></span>                                  |
| <span data-ttu-id="7a371-221">QUELLE \_ KOPIEREN</span><span class="sxs-lookup"><span data-stu-id="7a371-221">COPY\_SOURCE</span></span>                  | <span data-ttu-id="7a371-222">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-222">Yes</span></span>                                          | <span data-ttu-id="7a371-223">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-223">Yes</span></span>                                  |
| <span data-ttu-id="7a371-224">RESOLVE \_ DEST</span><span class="sxs-lookup"><span data-stu-id="7a371-224">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="7a371-225">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-225">Yes</span></span>                                          | <span data-ttu-id="7a371-226">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-226">No</span></span>                                   |
| <span data-ttu-id="7a371-227">RESOLVE \_ SOURCE</span><span class="sxs-lookup"><span data-stu-id="7a371-227">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="7a371-228">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-228">Yes</span></span>                                          | <span data-ttu-id="7a371-229">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-229">No</span></span>                                   |
| <span data-ttu-id="7a371-230">PRÄDIKATION</span><span class="sxs-lookup"><span data-stu-id="7a371-230">PREDICATION</span></span>                   | <span data-ttu-id="7a371-231">Ja</span><span class="sxs-lookup"><span data-stu-id="7a371-231">Yes</span></span>                                          | <span data-ttu-id="7a371-232">Nein</span><span class="sxs-lookup"><span data-stu-id="7a371-232">No</span></span>                                   |



 

<span data-ttu-id="7a371-233"><sup>\*</sup>Tiefenschablonenressourcen müssen nicht gleichzeitige Zugriffstexturen sein und können daher nie implizit heraufgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-233"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="7a371-234">Wenn dieser Zugriff erfolgt, verhält sich die Heraufstufung wie eine implizite Ressourcenbarriere.</span><span class="sxs-lookup"><span data-stu-id="7a371-234">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="7a371-235">Bei nachfolgenden Zugriffen sind Ressourcenbarrieren erforderlich, um den Ressourcenzustand bei Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7a371-235">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="7a371-236">Beachten Sie, dass die Heraufstufung von einem heraufgestuften Lesezustand in mehrere Lesezustände gültig ist, aber dies ist bei Schreibzuständen nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="7a371-236">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="7a371-237">Wenn z. B. eine Ressource im allgemeinen Zustand in einem Draw-Aufruf zu PIXEL SHADER RESOURCE (PIXEL \_ SHADER-RESSOURCE) gestuft \_ wird, kann sie trotzdem zu NON_PIXEL \_ \_ SHADER-RESSOURCE | \_PIXEL-SHADER-RESSOURCE \_ in einem anderen Draw-Aufruf.</span><span class="sxs-lookup"><span data-stu-id="7a371-237">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="7a371-238">Wenn sie jedoch in einem Schreibvorgang wie einem Kopierziel verwendet wird, ist hier NON_PIXEL \_ SHADER RESOURCE | eine Barriere für den Übergang des Ressourcenzustands von den kombinierten hergestuften Lesezuständen. \_ DIE \_ \_ PIXELSHADR-RESSOURCE zum KOPIEREN \_ DEST ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a371-238">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="7a371-239">Ebenso ist beim Heraufstufen von COMMON auf COPY \_ DEST eine Barriere für den Übergang von COPY \_ DEST zu RENDER \_ TARGET erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a371-239">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="7a371-240">Beachten Sie, dass die allgemeine Zustandsaufstufung "kostenlos" ist, da die GPU keine Synchronisierungswartevorgänge ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="7a371-240">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="7a371-241">Die Heraufstufung stellt die Tatsache dar, dass Ressourcen im Status COMMON keine zusätzliche GPU-Arbeit oder Treibernachverfolgung erfordern sollten, um bestimmte Zugriffe zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7a371-241">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="7a371-242">Zustandsverfall auf "Allgemein"</span><span class="sxs-lookup"><span data-stu-id="7a371-242">State decay to common</span></span>

<span data-ttu-id="7a371-243">Die Kehrseite der Allgemeinen Zustandsaufstufung ist der Rückfall zurück zu D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="7a371-243">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="7a371-244">Ressourcen, die bestimmte Anforderungen erfüllen, gelten als zustandslos und kehren effektiv in den allgemeinen Zustand zurück, wenn die GPU die Ausführung eines [**ExecuteCommandLists-Vorgangs**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) beendet.</span><span class="sxs-lookup"><span data-stu-id="7a371-244">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="7a371-245">Der Unterfall tritt nicht zwischen Befehlslisten auf, die zusammen im gleichen **ExecuteCommandLists-Aufruf ausgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-245">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="7a371-246">Die folgenden Ressourcen verfällt, wenn ein [**ExecuteCommandLists-Vorgang**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) auf der GPU abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="7a371-246">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="7a371-247">Ressourcen, auf die in einer Kopierwarteschlange zugegriffen wird, *oder*</span><span class="sxs-lookup"><span data-stu-id="7a371-247">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="7a371-248">Puffern von Ressourcen für einen beliebigen Warteschlangentyp *oder*</span><span class="sxs-lookup"><span data-stu-id="7a371-248">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="7a371-249">Texturressourcen für jeden Warteschlangentyp, für den das \_ D3D12-RESSOURCENFlag ALLOW SIMULTANEOUS ACCESS \_ festgelegt \_ \_ \_ ist, *oder*</span><span class="sxs-lookup"><span data-stu-id="7a371-249">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="7a371-250">Jede Ressource, die implizit in einen schreibgeschützten Zustand hoch 2.</span><span class="sxs-lookup"><span data-stu-id="7a371-250">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="7a371-251">Wie bei der Heraufstufung des allgemeinen Zustands ist der Verfall frei, da keine zusätzliche Synchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7a371-251">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="7a371-252">Die Kombination von common state promotion und decay kann dazu beitragen, viele unnötige [**ResourceBarrier-Übergänge**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7a371-252">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="7a371-253">In einigen Fällen kann dies zu erheblichen Leistungsverbesserungen führen.</span><span class="sxs-lookup"><span data-stu-id="7a371-253">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="7a371-254">Puffer und Simultaneous-Access werden in den allgemeinen Zustand verfällt, unabhängig davon, ob sie explizit mithilfe von Ressourcenbarrieren oder implizit promotet wurden.</span><span class="sxs-lookup"><span data-stu-id="7a371-254">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="7a371-255">Folgen für die Leistung</span><span class="sxs-lookup"><span data-stu-id="7a371-255">Performance implications</span></span>

<span data-ttu-id="7a371-256">Wenn Sie [**explizite ResourceBarrier-Übergänge**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) für Ressourcen im allgemeinen Zustand aufzeichnen, ist es richtig, entweder D3D12 RESOURCE STATE COMMON oder einen beliebigen aufstlegbaren Zustand als BeforeState-Wert in der \_ \_ \_ D3D12 RESOURCE TRANSITION  BARRIER-Struktur zu \_ \_ \_ verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a371-256">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="7a371-257">Dies ermöglicht eine herkömmliche Zustandsverwaltung, bei der der automatische Verfall von Puffern und Texturen mit gleichzeitigem Zugriff ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="7a371-257">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="7a371-258">Dies ist jedoch möglicherweise nicht wünschenswert, da das Vermeiden von **ResourceBarrier-Übergangsaufrufen** mit Ressourcen, die bekannterfalls den allgemeinen Zustand haben, die Leistung erheblich verbessern kann.</span><span class="sxs-lookup"><span data-stu-id="7a371-258">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="7a371-259">Ressourcenbarrieren können teuer sein.</span><span class="sxs-lookup"><span data-stu-id="7a371-259">Resource barriers can be expensive.</span></span> <span data-ttu-id="7a371-260">Sie sind dafür konzipiert, Cachelöschungen, Änderungen am Speicherlayout und andere Synchronisierungen zu erzwingen, die für Ressourcen, die sich bereits im allgemeinen Zustand befinden, möglicherweise nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7a371-260">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="7a371-261">Eine Befehlsliste, die eine Ressourcenbarriere von einem nicht allgemeinen Zustand zu einem anderen nicht allgemeinen Zustand für eine Ressource verwendet, die sich derzeit im allgemeinen Zustand befindet, kann zu viel nicht benötigtem Mehraufwand führen.</span><span class="sxs-lookup"><span data-stu-id="7a371-261">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="7a371-262">Vermeiden Sie außerdem explizite [**ResourceBarrier-Übergänge**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) zu D3D12 \_ RESOURCE STATE \_ \_ COMMON, sofern dies nicht unbedingt erforderlich ist (z. B. befindet sich der nächste Zugriff in einer COPY-Befehlswarteschlange, die erfordert, dass ressourcen im allgemeinen Zustand beginnen).</span><span class="sxs-lookup"><span data-stu-id="7a371-262">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="7a371-263">Übermäßige Übergänge in den allgemeinen Zustand können die GPU-Leistung erheblich verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="7a371-263">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="7a371-264">Versuchen Sie zusammenfassend, sich auf allgemeine Zustandsverschiebungen und -verfallen zu verlassen, wenn ihre Semantik Ihnen den Weg freigibt, ohne [**ResourceBarrier-Aufrufe**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) auszugeben.</span><span class="sxs-lookup"><span data-stu-id="7a371-264">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="7a371-265">Split Barriers</span><span class="sxs-lookup"><span data-stu-id="7a371-265">Split Barriers</span></span>

<span data-ttu-id="7a371-266">Eine Ressourcenübergangsbarriere mit dem FLAG D3D12 \_ RESOURCE BARRIER FLAG BEGIN ONLY beginnt mit einer \_ \_ \_ \_ Aufteilungsbarriere, und die Übergangsbarriere wird als ausstehend bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7a371-266">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="7a371-267">Während die Barriere aussteht, kann die (untergeordnete) Ressource nicht von der GPU gelesen oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-267">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="7a371-268">Die einzige gesetzliche Übergangsbarriere, die auf eine (untergeordnete) Ressource mit einer ausstehenden Barriere angewendet werden kann, ist eine mit denselben *Zuständen vor* und *nach* und dem Flag D3D12 \_ RESOURCE BARRIER FLAG END \_ \_ \_ \_ ONLY, das den ausstehenden Übergang abschließt.</span><span class="sxs-lookup"><span data-stu-id="7a371-268">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="7a371-269">Split-Barrieren geben der GPU Hinweise darauf, dass eine Ressource im Zustand *A* zu einem späteren Zeitpunkt im Zustand *B* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a371-269">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="7a371-270">Dadurch erhält die GPU die Möglichkeit, die Übergangsworkload zu optimieren, wodurch ausführungsverhindernde Auslastungen möglicherweise reduziert oder beseitigt werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-270">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="7a371-271">Das Ausstellen der end-only-Barriere garantiert, dass alle GPU-Übergangsarbeiten abgeschlossen sind, bevor sie mit dem nächsten Befehl fortfahren.</span><span class="sxs-lookup"><span data-stu-id="7a371-271">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="7a371-272">Die Verwendung von Split Barriers kann zur Verbesserung der Leistung beitragen, insbesondere in Szenarios mit mehreren Engines oder wenn Ressourcen in einer oder mehreren Befehlslisten nur selten gelesen/geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7a371-272">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="7a371-273">Beispielszenario für Ressourcenbarrieren</span><span class="sxs-lookup"><span data-stu-id="7a371-273">Resource barrier example scenario</span></span>

<span data-ttu-id="7a371-274">Die folgenden Codeausschnitte zeigen die Verwendung der [**ResourceBarrier-Methode**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) in einem Multithreadingbeispiel.</span><span class="sxs-lookup"><span data-stu-id="7a371-274">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="7a371-275">Erstellen der Tiefen-Schablonenansicht und Übergang in einen schreibbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="7a371-275">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


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



<span data-ttu-id="7a371-276">Erstellen der Scheitelpunktpufferansicht, zuerst ändern Sie sie von einem allgemeinen Zustand in ein Ziel und dann von einem Ziel in einen generischen lesbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="7a371-276">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="7a371-277">Erstellen der Indexpufferansicht, zuerst ändern Sie sie von einem allgemeinen Zustand in ein Ziel und dann von einem Ziel in einen generischen lesbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="7a371-277">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="7a371-278">Erstellen von Texturen und Shader-Ressourcenansichten.</span><span class="sxs-lookup"><span data-stu-id="7a371-278">Creating textures and shader resource views.</span></span> <span data-ttu-id="7a371-279">Die Textur wird von einem allgemeinen Zustand in ein Ziel und dann von einem Ziel in eine Pixel-Shaderressource geändert.</span><span class="sxs-lookup"><span data-stu-id="7a371-279">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


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



<span data-ttu-id="7a371-280">Beginnen eines Frames; dabei wird nicht nur [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) verwendet, um anzugeben, dass der Backbuffer als Renderziel verwendet werden soll, sondern auch die Frameressource (die **ResourceBarrier** im Tiefen-Schablonenpuffer aufruft).</span><span class="sxs-lookup"><span data-stu-id="7a371-280">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


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



<span data-ttu-id="7a371-281">Beenden eines Frames, der angibt, dass der Hintergrundpuffer jetzt zur Anzeige verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a371-281">Ending a frame, indicating the back buffer is now used to present.</span></span>


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



<span data-ttu-id="7a371-282">Beim Initialisieren einer Frameressource, die beim Start eines Frames aufgerufen wird, wird der Tiefen-Schablonenpuffer in schreibbar.</span><span class="sxs-lookup"><span data-stu-id="7a371-282">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


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



<span data-ttu-id="7a371-283">Barrieren werden im Rahmen getauscht, um die Schattenkarte von schreibbar in lesbar zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="7a371-283">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="7a371-284">Finish wird aufgerufen, wenn ein Frame beendet wird und die Schattenkarte in einen gemeinsamen Zustand über geht.</span><span class="sxs-lookup"><span data-stu-id="7a371-284">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="7a371-285">Beispiel für allgemeine Zustandsaufstufung und -zerfall</span><span class="sxs-lookup"><span data-stu-id="7a371-285">Common state promotion and decay sample</span></span>

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

## <a name="example-of-split-barriers"></a><span data-ttu-id="7a371-286">Beispiel für Teilungsbarrieren</span><span class="sxs-lookup"><span data-stu-id="7a371-286">Example of split barriers</span></span>

<span data-ttu-id="7a371-287">Das folgende Beispiel zeigt, wie Sie eine Teilungsbarriere verwenden, um Pipeline-Stags zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="7a371-287">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="7a371-288">Der folgende Code verwendet keine Teilungsbarrieren:</span><span class="sxs-lookup"><span data-stu-id="7a371-288">The code that follows does not use split barriers:</span></span>

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

<span data-ttu-id="7a371-289">Im folgenden Code werden getrennte Barrieren verwendet:</span><span class="sxs-lookup"><span data-stu-id="7a371-289">The following code uses split barriers:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7a371-290">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a371-290">Related topics</span></span>

[<span data-ttu-id="7a371-291">Videotutorials für erweitertes Lernen mit DirectX: Ressourcenbarrieren und Zustandsnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="7a371-291">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="7a371-292">Synchronisierung mit mehreren Modulen</span><span class="sxs-lookup"><span data-stu-id="7a371-292">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="7a371-293">Arbeitsübermittlung in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7a371-293">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="7a371-294">Ein Blick in D3D12-Ressourcenzustandsbarrieren</span><span class="sxs-lookup"><span data-stu-id="7a371-294">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

