---
title: Multi-Engine-Synchronisierung
description: In diesem Thema wird die Synchronisierung des Zugriffs auf mehrere unabhängige Engines in den meisten modernen GPUs erläutert.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548633"
---
# <a name="multi-engine-synchronization"></a><span data-ttu-id="5eacc-103">Multi-Engine-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="5eacc-103">Multi-engine synchronization</span></span>

<span data-ttu-id="5eacc-104">Die meisten modernen GPUs enthalten mehrere unabhängige Engines, die spezialisierte Funktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-104">Most modern GPUs contain multiple independent engines that provide specialized functionality.</span></span> <span data-ttu-id="5eacc-105">Viele verfügen über ein oder mehrere dedizierte Kopier Module und eine COMPUTE-Engine, die sich in der Regel von der 3D-Engine unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="5eacc-105">Many have one or more dedicated copy engines, and a compute engine, usually distinct from the 3D engine.</span></span> <span data-ttu-id="5eacc-106">Jedes dieser Engines kann Befehle parallel untereinander ausführen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-106">Each of these engines can execute commands in parallel with each other.</span></span> <span data-ttu-id="5eacc-107">Direct3D 12 bietet differenzierten Zugriff auf 3D-, COMPUTE-und Kopier Module mithilfe von Warteschlangen und Befehlslisten.</span><span class="sxs-lookup"><span data-stu-id="5eacc-107">Direct3D 12 provides fine-grained access to the 3D, compute, and copy engines, using queues and command lists.</span></span>

## <a name="gpu-engines"></a><span data-ttu-id="5eacc-108">GPU-Engines</span><span class="sxs-lookup"><span data-stu-id="5eacc-108">GPU engines</span></span>

<span data-ttu-id="5eacc-109">Das folgende Diagramm zeigt die CPU-Threads eines Titels, von denen jede eine oder mehrere der Copy-, COMPUTE-und 3D-Warteschlangen füllt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-109">The following diagram shows a title's CPU threads, each populating one or more of the copy, compute, and 3D queues.</span></span> <span data-ttu-id="5eacc-110">Die 3D-Warteschlange kann alle drei GPU-Engines steuern. Die COMPUTE-Warteschlange kann die COMPUTE-und Kopier Module steuern. und die Kopier Warteschlange ist einfach die Kopier-Engine.</span><span class="sxs-lookup"><span data-stu-id="5eacc-110">The 3D queue can drive all three GPU engines; the compute queue can drive the compute and copy engines; and the copy queue simply the copy engine.</span></span>

<span data-ttu-id="5eacc-111">Da die verschiedenen Threads die Warteschlangen auffüllen, kann es keine einfache Garantie für die Ausführungsreihenfolge geben, daher ist es erforderlich, dass Synchronisierungs Mechanismen erforderlich sind, &mdash; Wenn der Titel Sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-111">As the different threads populate the queues, there can be no simple guarantee of the order of execution, hence the need for synchronization mechanisms&mdash;when the title requires them.</span></span>

![vier Threads, die Befehle an drei Warteschlangen senden](images/gpu-engines.png)

<span data-ttu-id="5eacc-113">In der folgenden Abbildung wird veranschaulicht, wie ein Titel die Arbeit über mehrere GPU-Engines hinweg planen kann, einschließlich der zwischen Modul Synchronisierung, falls erforderlich: Er zeigt die Workloads pro Engine mit Abhängigkeiten zwischen den Engines.</span><span class="sxs-lookup"><span data-stu-id="5eacc-113">The following image illustrate how a title might schedule work across multiple GPU engines, including inter-engine synchronization where necessary: it shows the per-engine workloads with inter-engine dependencies.</span></span> <span data-ttu-id="5eacc-114">In diesem Beispiel kopiert die Copy-Engine zuerst eine Geometrie, die für das Rendering erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5eacc-114">In this example, the copy engine first copies some geometry necessary for rendering.</span></span> <span data-ttu-id="5eacc-115">Die 3D-Engine wartet auf den Abschluss dieser Kopien und rendert einen vorab Durchlauf über die Geometrie.</span><span class="sxs-lookup"><span data-stu-id="5eacc-115">The 3D engine waits for these copies to complete, and renders a pre-pass over the geometry.</span></span> <span data-ttu-id="5eacc-116">Diese wird dann von der COMPUTE-Engine verwendet.</span><span class="sxs-lookup"><span data-stu-id="5eacc-116">This is then consumed by the compute engine.</span></span> <span data-ttu-id="5eacc-117">Die Ergebnisse der Verteilung der computeengine werden zusammen mit mehreren Textur Kopier Vorgängen für die Kopier [**-Engine von**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)der 3D-Engine für den abschließenden [**Zeichnen**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) -Befehl genutzt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-117">The results of the compute engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch), along with several texture copy operations on the copy engine, are consumed by the 3D engine for the final [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) call.</span></span>

![Kopieren, Grafiken und Compute-Engines kommunizieren](images/gpu-sync.png)

<span data-ttu-id="5eacc-119">Der folgende Pseudo Code veranschaulicht, wie ein Titel eine solche Arbeitsauslastung übermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="5eacc-119">The following pseudo-code illustrates how a title might submit such a workload.</span></span>

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

<span data-ttu-id="5eacc-120">Der folgende Pseudo Code veranschaulicht die Synchronisierung zwischen den Kopier-und 3D-Engines, um eine Heap ähnliche Speicher Belegung über einen Ringpuffer zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-120">The following pseudo-code illustrates synchronization between the copy and 3D engines to accomplish heap-like memory allocation via a ring buffer.</span></span> <span data-ttu-id="5eacc-121">Titel haben die Flexibilität, das richtige Gleichgewicht zwischen der Maximierung der Parallelität (über einen großen Puffer) und der Reduzierung der Arbeitsspeicher Nutzung und Latenz (über einen kleinen Puffer) auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-121">Titles have the flexibility to choose the right balance between maximizing parallelism (via a large buffer) and reducing memory consumption and latency (via a small buffer).</span></span>

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a><span data-ttu-id="5eacc-122">Szenarios mit mehreren Engines</span><span class="sxs-lookup"><span data-stu-id="5eacc-122">Multi-engine scenarios</span></span>

<span data-ttu-id="5eacc-123">Mit Direct3D 12 können Sie versehentlich zu Ineffizienzen führen, die durch unerwartete Synchronisierungs Verzögerungen verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-123">Direct3D 12 allows you to avoid accidentally running into inefficiencies caused by unexpected synchronization delays.</span></span> <span data-ttu-id="5eacc-124">Außerdem können Sie die Synchronisierung auf einer höheren Ebene einführen, bei der die erforderliche Synchronisierung mit größerer Sicherheit bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5eacc-124">It also allows you to introduce synchronization at a higher level where the required synchronization can be determined with greater certainty.</span></span> <span data-ttu-id="5eacc-125">Ein zweites Problem ist, dass mehrere-Engine-Adressen teure Vorgänge expliziter machen müssen. Dies schließt Übergänge zwischen 3D und Video ein, die aufgrund der Synchronisierung zwischen mehreren Kernel Kontexten traditionell aufwendig waren.</span><span class="sxs-lookup"><span data-stu-id="5eacc-125">A second issue that multi-engine addresses is to make expensive operations more explicit, which includes transitions between 3D and video that were traditionally costly because of synchronization between multiple kernel contexts.</span></span>

<span data-ttu-id="5eacc-126">Insbesondere können die folgenden Szenarien mit Direct3D 12 adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-126">In particular, the following scenarios can be addressed with Direct3D 12.</span></span>

-   <span data-ttu-id="5eacc-127">GPU-Arbeit mit asynchroner und niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="5eacc-127">Asynchronous and low priority GPU work.</span></span> <span data-ttu-id="5eacc-128">Dies ermöglicht die gleichzeitige Ausführung von GPU-arbeiten mit niedriger Priorität und atomaren Vorgängen, die es einem GPU-Thread ermöglichen, die Ergebnisse eines anderen nicht synchronisierten Threads ohne Blockierung zu nutzen</span><span class="sxs-lookup"><span data-stu-id="5eacc-128">This enables concurrent execution of low priority GPU work and atomic operations that enable one GPU thread to consume the results of another unsynchronized thread without blocking.</span></span>
-   <span data-ttu-id="5eacc-129">Compute-Arbeit mit hoher Priorität.</span><span class="sxs-lookup"><span data-stu-id="5eacc-129">High priority compute work.</span></span> <span data-ttu-id="5eacc-130">Mit background Compute ist es möglich, das 3D-Rendering zu unterbrechen, um eine kleine Menge von computeaufgaben mit hoher Priorität zu erledigen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-130">With background compute it is possible to interrupt 3D rendering to do a small amount of high priority compute work.</span></span> <span data-ttu-id="5eacc-131">Die Ergebnisse dieser Arbeit können frühzeitig zur weiteren Verarbeitung auf der CPU abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-131">The results of this work can be obtained early for additional processing on the CPU.</span></span>
-   <span data-ttu-id="5eacc-132">Computearbeit im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="5eacc-132">Background compute work.</span></span> <span data-ttu-id="5eacc-133">Eine separate Warteschlange mit niedriger Priorität für computeworkloads ermöglicht es einer Anwendung, freie GPU-Zyklen zu verwenden, um eine Hintergrund Berechnung ohne negative Auswirkung auf die primären Renderingaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-133">A separate low priority queue for compute workloads allows an application to utilize spare GPU cycles to perform background computation without negative impact on the primary rendering (or other) tasks.</span></span> <span data-ttu-id="5eacc-134">Hintergrundaufgaben können die Dekomprimierung von Ressourcen oder das Aktualisieren von Simulationen oder beschleunigungsstrukturen umfassen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-134">Background tasks may include decompression of resources or updating simulations or acceleration structures.</span></span> <span data-ttu-id="5eacc-135">Hintergrundaufgaben sollten auf der CPU selten (ungefähr einmal pro Frame) synchronisiert werden, um das stecken bleiben oder verlangsamen der Vordergrund Arbeit zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-135">Background tasks should be synchronized on the CPU infrequently (approximately once per frame) to avoid stalling or slowing foreground work.</span></span>
-   <span data-ttu-id="5eacc-136">Streaming und Hochladen von Daten.</span><span class="sxs-lookup"><span data-stu-id="5eacc-136">Streaming and uploading data.</span></span> <span data-ttu-id="5eacc-137">Eine separate Kopier Warteschlange ersetzt die D3D11-Konzepte der Anfangsdaten und Aktualisierungs Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-137">A separate copy queue replaces the D3D11 concepts of initial data and updating resources.</span></span> <span data-ttu-id="5eacc-138">Obwohl die Anwendung für weitere Details im Direct3D 12-Modell verantwortlich ist, ist diese Verantwortung in Kraft.</span><span class="sxs-lookup"><span data-stu-id="5eacc-138">Although the application is responsible for more details in the Direct3D 12 model, this responsibility comes with power.</span></span> <span data-ttu-id="5eacc-139">Die Anwendung kann steuern, wie viel System Arbeitsspeicher für die Pufferung von uploaddaten aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5eacc-139">The application can control how much system memory is devoted to buffering upload data.</span></span> <span data-ttu-id="5eacc-140">Die APP kann auswählen, wann und wie (CPU-und GPU-Leistung, Blockierung und nicht Blockierung) synchronisiert werden soll, und kann den Fortschritt nachverfolgen und die Menge der in der Warteschlange befindlichen Aufgaben steuern</span><span class="sxs-lookup"><span data-stu-id="5eacc-140">The app can choose when and how (CPU vs GPU, blocking vs non-blocking) to synchronize, and can track progress and control the amount of queued work.</span></span>
-   <span data-ttu-id="5eacc-141">Erhöhung der Parallelität.</span><span class="sxs-lookup"><span data-stu-id="5eacc-141">Increased parallelism.</span></span> <span data-ttu-id="5eacc-142">Anwendungen können tiefere Warteschlangen für hintergrundworkloads (z. b. Video Decodierung) verwenden, wenn Sie über separate Warteschlangen für Vordergrund arbeiten verfügen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-142">Applications can use deeper queues for background workloads (e.g. video decode) when they have separate queues for foreground work.</span></span>

<span data-ttu-id="5eacc-143">In Direct3D 12 ist das Konzept einer Befehls Warteschlange die API-Darstellung einer ungefähr seriellen Abfolge von Arbeitsaufgaben, die von der Anwendung übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5eacc-143">In Direct3D 12 the concept of a command queue is the API representation of a roughly serial sequence of work submitted by the application.</span></span> <span data-ttu-id="5eacc-144">Mithilfe von Barrieren und anderen Techniken können diese Aufgaben in einer Pipeline oder außerhalb der Reihenfolge ausgeführt werden, aber die Anwendung sieht nur eine einzelne Vervollständigungs Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="5eacc-144">Barriers and other techniques allow this work to be executed in a pipeline or out of order, but the application only sees a single completion timeline.</span></span> <span data-ttu-id="5eacc-145">Dies entspricht dem unmittelbaren Kontext in D3D11.</span><span class="sxs-lookup"><span data-stu-id="5eacc-145">This corresponds to the immediate context in D3D11.</span></span>

## <a name="synchronization-apis"></a><span data-ttu-id="5eacc-146">Synchronisierungs-APIs</span><span class="sxs-lookup"><span data-stu-id="5eacc-146">Synchronization APIs</span></span>

### <a name="devices-and-queues"></a><span data-ttu-id="5eacc-147">Geräte und Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="5eacc-147">Devices and queues</span></span>

<span data-ttu-id="5eacc-148">Das Gerät Direct3D 12 verfügt über Methoden zum Erstellen und Abrufen von Befehls Warteschlangen mit unterschiedlichen Typen und Prioritäten.</span><span class="sxs-lookup"><span data-stu-id="5eacc-148">The Direct3D 12 device has methods to create and retrieve command queues of different types and priorities.</span></span> <span data-ttu-id="5eacc-149">Die meisten Anwendungen sollten die standardmäßigen Befehls Warteschlangen verwenden, da diese die gemeinsame Verwendung durch andere Komponenten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-149">Most applications should use the default command queues because these allow for shared usage by other components.</span></span> <span data-ttu-id="5eacc-150">Anwendungen mit zusätzlichen Parallelitäts Anforderungen können zusätzliche Warteschlangen erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-150">Applications with additional concurrency requirements can create additional queues.</span></span> <span data-ttu-id="5eacc-151">Warteschlangen werden durch den von Ihnen genutzten Befehls Auflistungstyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="5eacc-151">Queues are specified by the command list type that they consume.</span></span>

<span data-ttu-id="5eacc-152">Weitere Informationen finden Sie in den folgenden Erstellungs Methoden [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="5eacc-152">Refer to the following creation methods of [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span></span>

-   <span data-ttu-id="5eacc-153">[**Erstellungscommandqueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : erstellt eine Befehls Warteschlange basierend auf Informationen in der DESC-Struktur einer [**Direct3D 12- \_ Befehls \_ Warteschlange \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .</span><span class="sxs-lookup"><span data-stu-id="5eacc-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : creates a command queue based on information in a [**Direct3D 12\_COMMAND\_QUEUE\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) structure.</span></span>
-   <span data-ttu-id="5eacc-154">" [**Kreatecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ": erstellt eine Befehlsliste vom Typ " [**Direct3D 12 \_ Command \_ List \_ Type**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)".</span><span class="sxs-lookup"><span data-stu-id="5eacc-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : creates a command list of type [**Direct3D 12\_COMMAND\_LIST\_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>
-   <span data-ttu-id="5eacc-155">[**Kreatefence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : erstellt einen Fence und notiert die Flags in [**Direct3D 12- \_ fence- \_ Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span><span class="sxs-lookup"><span data-stu-id="5eacc-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : creates a fence, noting the flags in [**Direct3D 12\_FENCE\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span></span> <span data-ttu-id="5eacc-156">Zum Synchronisieren von Warteschlangen werden Zäune verwendet.</span><span class="sxs-lookup"><span data-stu-id="5eacc-156">Fences are used to synchronize queues.</span></span>

<span data-ttu-id="5eacc-157">Warteschlangen aller Typen (3D, COMPUTE und Copy) verwenden die gleiche Schnittstelle und sind alle auf der Befehlsliste basierende.</span><span class="sxs-lookup"><span data-stu-id="5eacc-157">Queues of all types (3D, compute and copy) share the same interface and are all command-list based.</span></span>

<span data-ttu-id="5eacc-158">Weitere Informationen finden Sie in den folgenden Methoden von [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span><span class="sxs-lookup"><span data-stu-id="5eacc-158">Refer to the following methods of [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span></span>

-   <span data-ttu-id="5eacc-159">[**Executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : übermittelt ein Array von Befehlslisten zur Ausführung.</span><span class="sxs-lookup"><span data-stu-id="5eacc-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : submits an array of command lists for execution.</span></span> <span data-ttu-id="5eacc-160">Jede durch [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)definierte Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="5eacc-160">Each command list being defined by [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>
-   <span data-ttu-id="5eacc-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : legt einen Fence Wert fest, wenn die Warteschlange (die auf der GPU ausgeführt wird) einen bestimmten Punkt erreicht.</span><span class="sxs-lookup"><span data-stu-id="5eacc-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : sets a fence value when the queue (running on the GPU) reaches a certain point.</span></span>
-   <span data-ttu-id="5eacc-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : die Warteschlange wartet, bis der angegebene Fence den angegebenen Wert erreicht.</span><span class="sxs-lookup"><span data-stu-id="5eacc-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : the queue waits until the specified fence reaches the specified value.</span></span>

<span data-ttu-id="5eacc-163">Beachten Sie, dass Pakete nicht von Warteschlangen genutzt werden. Daher kann dieser Typ nicht zum Erstellen einer Warteschlange verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-163">Note that bundles are not consumed by any queues and therefore this type cannot be used to create a queue.</span></span>

### <a name="fences"></a><span data-ttu-id="5eacc-164">Zäune</span><span class="sxs-lookup"><span data-stu-id="5eacc-164">Fences</span></span>

<span data-ttu-id="5eacc-165">Die Multi-Engine-API stellt explizite APIs zum Erstellen und Synchronisieren mithilfe von Zäunen bereit.</span><span class="sxs-lookup"><span data-stu-id="5eacc-165">The multi-engine API provides explicit APIs to create and synchronize using fences.</span></span> <span data-ttu-id="5eacc-166">Ein Fence ist ein Synchronisierungs Konstrukt, das von einem UINT64-Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="5eacc-166">A fence is a synchronization construct controlled by a UINT64 value.</span></span> <span data-ttu-id="5eacc-167">Die Fence Werte werden von der Anwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-167">Fence values are set by the application.</span></span> <span data-ttu-id="5eacc-168">Durch einen Signal Vorgang werden der Fence-Wert und ein warte Vorgangs Block geändert, bis der Fence den angeforderten Wert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="5eacc-168">A signal operation modifies the fence value and a wait operation blocks until the fence has reached the requested value or greater.</span></span> <span data-ttu-id="5eacc-169">Ein Ereignis kann ausgelöst werden, wenn ein Fence einen bestimmten Wert erreicht.</span><span class="sxs-lookup"><span data-stu-id="5eacc-169">An event can be fired when a fence reaches a certain value.</span></span>

<span data-ttu-id="5eacc-170">Weitere Informationen finden Sie in den Methoden der [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5eacc-170">Refer to the methods of the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface.</span></span>

-   <span data-ttu-id="5eacc-171">[**Getcompletedvalue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : gibt den aktuellen Wert des Fence zurück.</span><span class="sxs-lookup"><span data-stu-id="5eacc-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : returns the current value of the fence.</span></span>
-   <span data-ttu-id="5eacc-172">[](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) "Enumerationsvervollständigen": bewirkt, dass ein Ereignis ausgelöst wird, wenn der Fence einen bestimmten Wert erreicht.</span><span class="sxs-lookup"><span data-stu-id="5eacc-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : causes an event to fire when the fence reaches a given value.</span></span>
-   <span data-ttu-id="5eacc-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : legt den Fence auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="5eacc-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : sets the fence to the given value.</span></span>

<span data-ttu-id="5eacc-174">Durch Zäune wird der CPU-Zugriff auf den aktuellen Fence-Wert und CPU-warte Vorgänge und-Signale ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5eacc-174">Fences allow CPU access to the current fence value, and CPU waits and signals.</span></span>

<span data-ttu-id="5eacc-175">Die [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) -Methode der [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) -Schnittstelle aktualisiert einen Fence von der CPU-Seite.</span><span class="sxs-lookup"><span data-stu-id="5eacc-175">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) method on the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface updates a fence from the CPU side.</span></span> <span data-ttu-id="5eacc-176">Dieses Update erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="5eacc-176">This update occurs immediately.</span></span> <span data-ttu-id="5eacc-177">Die [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) -Methode auf [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) aktualisiert einen Fence von der GPU-Seite.</span><span class="sxs-lookup"><span data-stu-id="5eacc-177">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) method on [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) updates a fence from the GPU side.</span></span> <span data-ttu-id="5eacc-178">Dieses Update erfolgt, nachdem alle anderen Vorgänge in der Befehls Warteschlange abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-178">This update occurs after all other operations on the command queue have been completed.</span></span>

<span data-ttu-id="5eacc-179">Alle Knoten in einem Setup mit mehreren Engines können alle Endpunkte lesen und darauf reagieren, die den richtigen Wert erreichen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-179">All nodes in a multi-engine setup can read and react to any fence reaching the right value.</span></span>

<span data-ttu-id="5eacc-180">Anwendungen legen ihre eigenen Fence-Werte fest. ein guter Ausgangspunkt könnte einen Fence einmal pro Frame erhöhen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-180">Applications set their own fence values, a good starting point might be increasing a fence once per frame.</span></span>

<span data-ttu-id="5eacc-181">Ein fence *kann* *zurück* gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-181">A fence *may* be *rewound*.</span></span> <span data-ttu-id="5eacc-182">Dies bedeutet, dass der Fence-Wert nicht allein erhöht werden muss.</span><span class="sxs-lookup"><span data-stu-id="5eacc-182">This means that the fence value does not need to solely increment.</span></span> <span data-ttu-id="5eacc-183">Wenn ein **Signal** Vorgang in eine Warteschlange für zwei unterschiedliche Befehls Warteschlangen eingereiht wird, oder wenn zwei CPU-Threads beide als **Signal** an einem Fence aufrufen, kann es zu einem Wettlauf kommen, um zu bestimmen, welches **Signal** zuletzt abgeschlossen wurde, und welcher Fence Wert dem Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="5eacc-183">If a **Signal** operation is enqueued on two different command queues, or if two CPU threads are both calling **Signal** on a fence, there may be a race to determine which **Signal** completes last, and therefore which fence value is the one which will remain.</span></span> <span data-ttu-id="5eacc-184">Wenn ein Fence regger zurückgesetzt wird, werden alle neuen warte Vorgänge (einschließlich der Anforderungen an den "Abgleich" **) mit dem** neuen niedrigeren Fence-Wert verglichen und daher möglicherweise nicht erfüllt, auch wenn der Fence-Wert zuvor hoch genug war, um Sie zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-184">If a fence is rewound, any new waits (including **SetEventOnCompletion** requests) will be compared against the new lower fence value, and therefore may not be satisfied, even if the fence value had previously been high enough to satisfy them.</span></span> <span data-ttu-id="5eacc-185">Wenn ein racevorgang stattfindet, *wird* zwischen einem Wert, der einen ausstehenden warte Vorgang erfüllt, und einem niedrigeren Wert, der nicht ist, der Warte Vorgang unabhängig davon, welcher Wert später verbleibt, erfüllt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-185">If a race does occur, between a value which will satisfy an outstanding wait, and a lower value which will not, the wait *will* be satisfied regardless of which value remains afterwards.</span></span>

<span data-ttu-id="5eacc-186">Die Fence-APIs bieten leistungsstarke Synchronisierungs Funktionen, können aber potenziell schwer zu debuggende Probleme führen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-186">The fence APIs provide powerful synchronization functionality but can create potentially difficult to debug issues.</span></span> <span data-ttu-id="5eacc-187">Es wird empfohlen, dass jeder Fence nur verwendet wird, um den Fortschritt in einer Zeitachse anzugeben, um die Ausführung von Races zwischen Signal</span><span class="sxs-lookup"><span data-stu-id="5eacc-187">It is recommended that each fence only be used to indicate progress on one timeline to prevent races between signalers.</span></span>

### <a name="copy-and-compute-command-lists"></a><span data-ttu-id="5eacc-188">Befehlslisten "Kopieren" und "Compute"</span><span class="sxs-lookup"><span data-stu-id="5eacc-188">Copy and compute command lists</span></span>

<span data-ttu-id="5eacc-189">Alle drei Typen der Befehlsliste verwenden die [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle, es wird jedoch nur eine Teilmenge der Methoden für kopieren und berechnen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-189">All three types of command list use the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface, however only a subset of the methods are supported for copy and compute.</span></span>

<span data-ttu-id="5eacc-190">In den Befehlslisten "Kopieren" und "Compute" können folgende Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-190">Copy and compute command lists can use the following methods.</span></span>

-   [<span data-ttu-id="5eacc-191">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="5eacc-191">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [<span data-ttu-id="5eacc-192">**Copybufferregion**</span><span class="sxs-lookup"><span data-stu-id="5eacc-192">**CopyBufferRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="5eacc-193">**Copyresource**</span><span class="sxs-lookup"><span data-stu-id="5eacc-193">**CopyResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="5eacc-194">**Copytextureregion**</span><span class="sxs-lookup"><span data-stu-id="5eacc-194">**CopyTextureRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="5eacc-195">**Copytiles**</span><span class="sxs-lookup"><span data-stu-id="5eacc-195">**CopyTiles**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="5eacc-196">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5eacc-196">**Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [<span data-ttu-id="5eacc-197">**Resourcebarrier**</span><span class="sxs-lookup"><span data-stu-id="5eacc-197">**ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

<span data-ttu-id="5eacc-198">Compute-Befehlslisten können auch die folgenden Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-198">Compute command lists can also use the following methods.</span></span>

-   [<span data-ttu-id="5eacc-199">**Clearstate**</span><span class="sxs-lookup"><span data-stu-id="5eacc-199">**ClearState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [<span data-ttu-id="5eacc-200">**Clearunorderedaccessviewfloat**</span><span class="sxs-lookup"><span data-stu-id="5eacc-200">**ClearUnorderedAccessViewFloat**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="5eacc-201">**Clearunorderedaccessviewuint**</span><span class="sxs-lookup"><span data-stu-id="5eacc-201">**ClearUnorderedAccessViewUint**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="5eacc-202">**Verwerfen von Quelle**</span><span class="sxs-lookup"><span data-stu-id="5eacc-202">**DiscardResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [<span data-ttu-id="5eacc-203">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="5eacc-203">**Dispatch**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="5eacc-204">**Executin Direct**</span><span class="sxs-lookup"><span data-stu-id="5eacc-204">**ExecuteIndirect**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [<span data-ttu-id="5eacc-205">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="5eacc-205">**SetComputeRoot32BitConstant**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="5eacc-206">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="5eacc-206">**SetComputeRoot32BitConstants**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [<span data-ttu-id="5eacc-207">**Setcomputerootconstantbufferview**</span><span class="sxs-lookup"><span data-stu-id="5eacc-207">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="5eacc-208">**Setcomputerootdescriptor Table**</span><span class="sxs-lookup"><span data-stu-id="5eacc-208">**SetComputeRootDescriptorTable**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [<span data-ttu-id="5eacc-209">**Setcomputerootshaderresourceview**</span><span class="sxs-lookup"><span data-stu-id="5eacc-209">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="5eacc-210">**Setcomputerootsignature**</span><span class="sxs-lookup"><span data-stu-id="5eacc-210">**SetComputeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [<span data-ttu-id="5eacc-211">**Setcomputerootunorderedaccessview**</span><span class="sxs-lookup"><span data-stu-id="5eacc-211">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="5eacc-212">**Setdescriptorheaps**</span><span class="sxs-lookup"><span data-stu-id="5eacc-212">**SetDescriptorHeaps**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [<span data-ttu-id="5eacc-213">**Setpipelinestate**</span><span class="sxs-lookup"><span data-stu-id="5eacc-213">**SetPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [<span data-ttu-id="5eacc-214">**Setprediation**</span><span class="sxs-lookup"><span data-stu-id="5eacc-214">**SetPredication**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

<span data-ttu-id="5eacc-215">Compute-Befehlslisten müssen eine COMPUTE-PSO festlegen, wenn [**setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5eacc-215">Compute command lists must set a compute PSO when calling [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span></span>

<span data-ttu-id="5eacc-216">Bündel können nicht mit COMPUTE-oder Kopier Befehlslisten oder-Warteschlangen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-216">Bundles cannot be used with compute or copy command lists or queues.</span></span>

## <a name="pipelined-compute-and-graphics-example"></a><span data-ttu-id="5eacc-217">Beispiel für eine Pipeline und Grafiken mit Pipelines</span><span class="sxs-lookup"><span data-stu-id="5eacc-217">Pipelined compute and graphics example</span></span>

<span data-ttu-id="5eacc-218">Dieses Beispiel zeigt, wie die Fence-Synchronisierung verwendet werden kann, um eine Pipeline von computeaufgaben in einer Warteschlange (auf die von verwiesen wird) zu erstellen `pComputeQueue` , die von Grafiken in der Warteschlange genutzt wird `pGraphicsQueue`</span><span class="sxs-lookup"><span data-stu-id="5eacc-218">This example shows how fence synchronization can be used to create a pipeline of compute work on a queue (referenced by `pComputeQueue`) that's consumed by graphics work on queue `pGraphicsQueue`.</span></span> <span data-ttu-id="5eacc-219">Die COMPUTE-und Grafik Vorgänge werden mit der Grafik Warteschlange zusammengefasst, die das Ergebnis der computearbeit aus mehreren Frames zurückgibt, und ein CPU-Ereignis wird verwendet, um die Gesamtsumme der Arbeitsauslastung insgesamt zu drosseln.</span><span class="sxs-lookup"><span data-stu-id="5eacc-219">The compute and graphics work is pipelined with the graphics queue consuming the result of compute work from several frames back, and a CPU event is used to throttle the total work queued overall.</span></span>

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

<span data-ttu-id="5eacc-220">Um diese Pipeline zu unterstützen, muss ein Puffer mit `ComputeGraphicsLatency+1` unterschiedlichen Kopien der Daten vorhanden sein, die von der computewarteschlange an die Grafik Warteschlange übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-220">To support this pipelining, there must be a buffer of `ComputeGraphicsLatency+1` different copies of the data passing from the compute queue to the graphics queue.</span></span> <span data-ttu-id="5eacc-221">In den Befehlslisten müssen UAVs und Dereferenzierung verwendet werden, um die entsprechende "Version" der Daten im Puffer zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="5eacc-221">The command lists must use UAVs and indirection to read and write from the appropriate “version” of the data in the buffer.</span></span> <span data-ttu-id="5eacc-222">Die computewarteschlange muss warten, bis die Grafik Warteschlange das Lesen aus den Daten für Frame N abgeschlossen hat, bevor Frame geschrieben werden kann `N+ComputeGraphicsLatency` .</span><span class="sxs-lookup"><span data-stu-id="5eacc-222">The compute queue must wait until the graphics queue has finished reading from the data for frame N before it can write frame `N+ComputeGraphicsLatency`.</span></span>

<span data-ttu-id="5eacc-223">Beachten Sie, dass die Menge an computewarteschlangen, die relativ zur CPU verwendet werden, nicht direkt von der erforderlichen Puffer Menge abhängig ist. in der Warteschlange von GPU funktioniert die Menge des verfügbaren Puffer Platzes jedoch weniger wertvoll.</span><span class="sxs-lookup"><span data-stu-id="5eacc-223">Note that the amount of compute queue worked relative to the CPU does not depend directly on the amount of buffering required, however, queuing GPU work beyond the amount of buffer space available is less valuable.</span></span>

<span data-ttu-id="5eacc-224">Eine alternative Methode, um die Dereferenzierung zu vermeiden, besteht darin, mehrere Befehlslisten zu erstellen, die den "umbenannten" Versionen der Daten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-224">An alternative mechanism to avoid indirection would be to create multiple command lists corresponding to each of the “renamed” versions of the data.</span></span> <span data-ttu-id="5eacc-225">Im nächsten Beispiel wird dieses Verfahren verwendet, während das vorherige Beispiel erweitert wird, damit die COMPUTE-und Grafik Warteschlangen asynchron ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5eacc-225">The next example uses this technique while extending the previous example to allow the compute and graphics queues to run more asynchronously.</span></span>

## <a name="asynchronous-compute-and-graphics-example"></a><span data-ttu-id="5eacc-226">Beispiel für asynchrone COMPUTE und Grafiken</span><span class="sxs-lookup"><span data-stu-id="5eacc-226">Asynchronous compute and graphics example</span></span>

<span data-ttu-id="5eacc-227">Im nächsten Beispiel wird das asynchrone Rendering von Grafiken aus der computewarteschlange ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5eacc-227">This next example allows graphics to render asynchronously from the compute queue.</span></span> <span data-ttu-id="5eacc-228">Zwischen den beiden Phasen besteht immer noch eine Fixed-Menge an gepufferten Daten, die Grafik Arbeit erfolgt jedoch unabhängig voneinander und verwendet das aktuellste Ergebnis der computephase, wenn sich die Grafik Arbeit in der Warteschlange befindet.</span><span class="sxs-lookup"><span data-stu-id="5eacc-228">There is still a fixed amount of buffered data between the two stages, however now graphics work proceeds independently and uses the most up-to-date result of the compute stage as known on the CPU when the graphics work is queued.</span></span> <span data-ttu-id="5eacc-229">Dies wäre hilfreich, wenn die Grafik Arbeit von einer anderen Quelle, z. b. Benutzereingaben, aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5eacc-229">This would be useful if the graphics work was being updated by another source, for example user input.</span></span> <span data-ttu-id="5eacc-230">Es müssen mehrere Befehlslisten vorhanden sein, damit die `ComputeGraphicsLatency` Rahmen der Grafik Arbeit gleichzeitig aktiv sein können, und die Funktion `UpdateGraphicsCommandList` stellt das Aktualisieren der Befehlsliste dar, um die neuesten Eingabedaten einzubeziehen und aus den Compute-Daten aus dem entsprechenden Puffer zu lesen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-230">There must be multiple command lists to allow the `ComputeGraphicsLatency` frames of graphics work to be in flight at a time, and the function `UpdateGraphicsCommandList` represents updating the command list to include the most recent input data and read from the compute data from the appropriate buffer.</span></span>

<span data-ttu-id="5eacc-231">Die computewarteschlange muss immer noch warten, bis die Grafik Warteschlange mit den pipepuffern fertiggestellt ist, aber es wird ein Dritter fence ( `pGraphicsComputeFence` ) eingeführt, sodass der Fortschritt von Grafiken, die Compute-Arbeit und Grafik Fortschritt im Allgemeinen lesen, verfolgt werden kann</span><span class="sxs-lookup"><span data-stu-id="5eacc-231">The compute queue must still wait for the graphics queue to finish with the pipe buffers, but a third fence (`pGraphicsComputeFence`) is introduced so that the progress of graphics reading compute work versus graphics progress in general can be tracked.</span></span> <span data-ttu-id="5eacc-232">Dies spiegelt die Tatsache wider, dass jetzt aufeinander folgende Grafik Frames aus demselben computeergebnis lesen oder ein computeergebnis überspringen könnten.</span><span class="sxs-lookup"><span data-stu-id="5eacc-232">This reflects the fact that now consecutive graphics frames could read from the same compute result or could skip a compute result.</span></span> <span data-ttu-id="5eacc-233">Ein effizienterer, aber etwas komplizierteres Design würde nur den einzelnen Grafik Zaun verwenden und eine Zuordnung zu den von den einzelnen Grafik Frames verwendeten computeframes speichern.</span><span class="sxs-lookup"><span data-stu-id="5eacc-233">A more efficient but slightly more complicated design would use just the single graphics fence and store a mapping to the compute frames used by each graphics frame.</span></span>

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a><span data-ttu-id="5eacc-234">Ressourcen Zugriff mit mehreren Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="5eacc-234">Multi-queue resource access</span></span>

<span data-ttu-id="5eacc-235">Für den Zugriff auf eine Ressource in mehr als einer Warteschlange muss eine Anwendung den folgenden Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-235">To access a resource on more than one queue an application must adhere to the following rules.</span></span>

-   <span data-ttu-id="5eacc-236">Der Ressourcen Zugriff (siehe [**Direct3D 12 \_ Resource \_ States**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) wird durch Queue Type class not Queue Object festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5eacc-236">Resource access (refer to [**Direct3D 12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) is determined by queue type class not queue object.</span></span> <span data-ttu-id="5eacc-237">Es gibt zwei Typklassen von Queue: Compute/3D Queue ist eine Typklasse, Copy ist eine zweite Typklasse.</span><span class="sxs-lookup"><span data-stu-id="5eacc-237">There are two type classes of queue: Compute/3D queue is one type class, Copy is a second type class.</span></span> <span data-ttu-id="5eacc-238">Daher kann eine Ressource, die eine Barriere für den \_ Ressourcen Zustand "nicht Pixel- \_ Shader" in \_ einer 3D-Warteschlange aufweist, in diesem Zustand in jeder 3D-oder computewarteschlange verwendet werden, je nach Synchronisierungs Anforderungen, bei denen die meisten Schreibvorgänge serialisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-238">So a resource that has a barrier to the NON\_PIXEL\_SHADER\_RESOURCE state on one 3D queue can be used in that state on any 3D or Compute queue, subject to synchronization requirements which require most writes to be serialized.</span></span> <span data-ttu-id="5eacc-239">Die Ressourcen Zustände, die von den beiden Typklassen gemeinsam genutzt werden (Kopier \_ Quelle und Kopie \_ dest), werden für jede Typklasse als unterschiedliche Zustände angesehen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-239">The resource states that are shared between the two type classes (COPY\_SOURCE and COPY\_DEST) are considered different states for each type class.</span></span> <span data-ttu-id="5eacc-240">Wenn also eine Ressource in einer Kopier Warteschlange zum Kopieren dest wechselt, kann \_ Sie nicht als Kopier Ziel aus 3D-oder computewarteschlangen und umgekehrt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-240">So that if a resource transitions to COPY\_DEST on a Copy queue it is not accessible as a copy destination from 3D or Compute queues and vice versa.</span></span>

    <span data-ttu-id="5eacc-241">Zusammenfassend.</span><span class="sxs-lookup"><span data-stu-id="5eacc-241">To summarize.</span></span>

    -   <span data-ttu-id="5eacc-242">Ein Warteschlangen Objekt ist eine beliebige einzelne Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="5eacc-242">A queue "object" is any single queue.</span></span>
    -   <span data-ttu-id="5eacc-243">Eine Warteschlange "Type" ist eine dieser drei: COMPUTE, 3D und Copy.</span><span class="sxs-lookup"><span data-stu-id="5eacc-243">A queue "type" is any one of these three: Compute, 3D, and Copy.</span></span>
    -   <span data-ttu-id="5eacc-244">Eine Warteschlange "Type class" ist eine der folgenden beiden: Compute/3D und Copy.</span><span class="sxs-lookup"><span data-stu-id="5eacc-244">A queue "type class" is any one of these two: Compute/3D and Copy.</span></span>

-   <span data-ttu-id="5eacc-245">Die als Ausgangszustände verwendeten kopierflags (Kopie \_ dest und Copy \_ Source) stellen Zustände in der 3D/Compute Type-Klasse dar.</span><span class="sxs-lookup"><span data-stu-id="5eacc-245">The COPY flags (COPY\_DEST and COPY\_SOURCE) used as initial states represent states in the 3D/Compute type class.</span></span> <span data-ttu-id="5eacc-246">Um eine Ressource anfänglich in einer Kopier Warteschlange zu verwenden, sollte Sie im allgemeinen Zustand beginnen.</span><span class="sxs-lookup"><span data-stu-id="5eacc-246">To use a resource initially on a Copy queue it should start in the COMMON state.</span></span> <span data-ttu-id="5eacc-247">Der gemeinsame Zustand kann für alle Verwendungen in einer Kopier Warteschlange mithilfe der impliziten Zustandsübergänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eacc-247">The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.</span></span> 
-   <span data-ttu-id="5eacc-248">Obwohl der Ressourcen Status über alle Compute-und 3D-Warteschlangen hinweg gemeinsam genutzt wird, ist es nicht zulässig, gleichzeitig in verschiedene Warteschlangen in die Ressource zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="5eacc-248">Although resource state is shared across all Compute and 3D queues, it is not permitted to write to the resource simultaneously on different queues.</span></span> <span data-ttu-id="5eacc-249">"Gleichzeitig" bedeutet "nicht synchronisiert", was bedeutet, dass die nicht synchronisierte Ausführung auf bestimmter Hardware nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="5eacc-249">"Simultaneously" here means unsynchronized, noting unsynchronized execution is not possible on some hardware.</span></span> <span data-ttu-id="5eacc-250">Die folgenden Regeln gelten.</span><span class="sxs-lookup"><span data-stu-id="5eacc-250">The following rules apply.</span></span>

    -   <span data-ttu-id="5eacc-251">Nur eine Warteschlange kann gleichzeitig in eine Ressource schreiben.</span><span class="sxs-lookup"><span data-stu-id="5eacc-251">Only one queue can write to a resource at a time.</span></span>
    -   <span data-ttu-id="5eacc-252">Mehrere Warteschlangen können aus der Ressource lesen, solange Sie nicht die vom Writer geänderten Bytes lesen (das Lesen von gleichzeitig geschriebenen Bytes erzeugt nicht definierte Ergebnisse).</span><span class="sxs-lookup"><span data-stu-id="5eacc-252">Multiple queues can read from the resource as long as they don’t read the bytes being modified by the writer (reading bytes being simultaneously written produces undefined results).</span></span>
    -   <span data-ttu-id="5eacc-253">Ein Fence muss verwendet werden, um nach dem Schreiben zu synchronisieren, bevor eine andere Warteschlange die geschriebenen Bytes lesen oder Schreibzugriffe ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="5eacc-253">A fence must be used to synchronize after writing before another queue can read the written bytes or make any write access.</span></span>

-   <span data-ttu-id="5eacc-254">Die angezeigten backpuffer müssen sich im Status "Direct3D 12" im \_ Ressourcen Status "Allgemein" befinden \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5eacc-254">Back buffers being presented must be in the Direct3D 12\_RESOURCE\_STATE\_COMMON state.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="5eacc-255">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5eacc-255">Related topics</span></span>

[<span data-ttu-id="5eacc-256">Direct3D 12-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="5eacc-256">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)

[<span data-ttu-id="5eacc-257">Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5eacc-257">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[<span data-ttu-id="5eacc-258">Arbeitsspeicherverwaltung in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5eacc-258">Memory management in Direct3D 12</span></span>](memory-management.md)
