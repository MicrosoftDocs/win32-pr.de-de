---
title: Pipelines und Shader mit Direct3D 12
description: Die programmierbare Pipeline Direct3D 12 erhöht die Renderingleistung im Vergleich zu den Schnittstellen Schnittstellen für die Grafik Programmierung.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548671"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a><span data-ttu-id="40f36-103">Pipelines und Shader mit Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="40f36-103">Pipelines and Shaders with Direct3D 12</span></span>

<span data-ttu-id="40f36-104">Die programmierbare Pipeline Direct3D 12 erhöht die Renderingleistung im Vergleich zu den Schnittstellen Schnittstellen für die Grafik Programmierung.</span><span class="sxs-lookup"><span data-stu-id="40f36-104">The Direct3D 12 programmable pipeline significantly increases rendering performance compared to previous generation graphics programming interfaces.</span></span>

-   [<span data-ttu-id="40f36-105">Direct3D 12-Grafik Pipeline</span><span class="sxs-lookup"><span data-stu-id="40f36-105">Direct3D 12 graphics pipeline</span></span>](#direct3d-12-graphics-pipeline)
-   [<span data-ttu-id="40f36-106">Pipeline Zustands Objekte</span><span class="sxs-lookup"><span data-stu-id="40f36-106">Pipeline state objects</span></span>](#pipeline-state-objects)
-   [<span data-ttu-id="40f36-107">Direct3D 12 Compute-Pipeline</span><span class="sxs-lookup"><span data-stu-id="40f36-107">Direct3D 12 compute pipeline</span></span>](#direct3d-12-compute-pipeline)
-   [<span data-ttu-id="40f36-108">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="40f36-108">Related topics</span></span>](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a><span data-ttu-id="40f36-109">Direct3D 12-Grafik Pipeline</span><span class="sxs-lookup"><span data-stu-id="40f36-109">Direct3D 12 graphics pipeline</span></span>

<span data-ttu-id="40f36-110">Im folgenden Diagramm werden die Direct3D 12-Grafik Pipeline und der-Zustand veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="40f36-110">The following diagram illustrates the Direct3D 12 graphics pipeline and state.</span></span>

![Diagramm zur Veranschaulichung von Direct3D 12 Pipeline und Status](images/pipeline.png)

<span data-ttu-id="40f36-112">Eine Grafik Pipeline ist der sequenzielle Fluss von Dateneingaben und-Ausgaben, wenn die GPU Frames rendert.</span><span class="sxs-lookup"><span data-stu-id="40f36-112">A graphics pipeline is the sequential flow of data inputs and outputs as the GPU renders frames.</span></span> <span data-ttu-id="40f36-113">Aufgrund des Pipeline Zustands und der Eingaben führt die GPU eine Reihe von Vorgängen aus, um die resultierenden Images zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="40f36-113">Given the pipeline state and inputs, the GPU performs a series of operations to create the resulting images.</span></span> <span data-ttu-id="40f36-114">Eine Grafik Pipeline enthält Shader, die programmierbare renderingoffekte und Berechnungen ausführen, sowie fixierte Funktions Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="40f36-114">A graphics pipeline contains shaders, which perform programmable rendering effects and calculations, and fixed function operations.</span></span>

<span data-ttu-id="40f36-115">Beachten Sie beim Verweis auf das Pipeline Status Diagramm Folgendes:</span><span class="sxs-lookup"><span data-stu-id="40f36-115">Note the following when referring to the pipeline state diagram:</span></span>

-   <span data-ttu-id="40f36-116">Die deskriptortabellen und Heaps können beliebig angeordnet werden: Srvs, cbvs und UAVs können referenziert und in beliebiger Reihenfolge zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="40f36-116">The descriptor tables and heaps can be arbitrarily arranged: SRVs, CBVs and UAVs can be referenced and allocated in any order.</span></span>
-   <span data-ttu-id="40f36-117">Einige Vorgänge der Pipeline sind konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="40f36-117">Some operations of the pipeline are configurable.</span></span> <span data-ttu-id="40f36-118">Beispielsweise wird bei der Ausgabe Zusammenführung in der Regel eine Lese-/Schreib-Schreibweise mit den Ansichten "Renderziel" und "tiefen Schablone" angewendet.</span><span class="sxs-lookup"><span data-stu-id="40f36-118">For example, the output merger typically operates on a read-modify-write basis with the render target and depth stencil views.</span></span> <span data-ttu-id="40f36-119">Die Pipeline kann jedoch so konfiguriert werden, dass beide Sichten schreibgeschützt oder schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="40f36-119">However the pipeline can be configured so that either of these views are read-only or write-only.</span></span>
-   <span data-ttu-id="40f36-120">Statische Samplern sind nicht Teil der root-Argumente, da Sie statisch sind.</span><span class="sxs-lookup"><span data-stu-id="40f36-120">Static samplers are not part of the root arguments since they are static.</span></span>

## <a name="pipeline-state-objects"></a><span data-ttu-id="40f36-121">Pipeline Zustands Objekte</span><span class="sxs-lookup"><span data-stu-id="40f36-121">Pipeline state objects</span></span>

<span data-ttu-id="40f36-122">Direct3D 12 führt das Pipeline State Object (PSO) ein.</span><span class="sxs-lookup"><span data-stu-id="40f36-122">Direct3D 12 introduces the pipeline state object (PSO).</span></span> <span data-ttu-id="40f36-123">Anstatt den Pipeline Zustand für eine große Anzahl von Objekten auf hoher Ebene zu speichern und darzustellen, werden die Zustände von Pipeline Komponenten wie der Eingabe Assembler, der Rasterizer, der Pixelshader und die Ausgabe Zusammenführung in einem PSO gespeichert.</span><span class="sxs-lookup"><span data-stu-id="40f36-123">Rather than storing and representing pipeline state across a large number of high-level objects, the states of pipeline components like the input assembler, rasterizer, pixel shader, and output merger are stored in a PSO.</span></span> <span data-ttu-id="40f36-124">Bei einem PSO handelt es sich um ein einheitliches Pipeline Zustands Objekt, das nach der Erstellung unveränderlich ist.</span><span class="sxs-lookup"><span data-stu-id="40f36-124">A PSO is a unified pipeline state object that is immutable after creation.</span></span> <span data-ttu-id="40f36-125">Das aktuell ausgewählte PSO kann schnell und dynamisch geändert werden, und die Hardware und Treiber können ein PSO direkt in systemeigene Hardware Anweisungen und den Status konvertieren, indem Sie die GPU für die Grafik Verarbeitung lesen.</span><span class="sxs-lookup"><span data-stu-id="40f36-125">The currently selected PSO can be changed quickly and dynamically, and the hardware and drivers can directly convert a PSO into native hardware instructions and state, readying the GPU for graphics processing.</span></span> <span data-ttu-id="40f36-126">Zum Anwenden eines PSO wird von der Hardware eine minimale Menge vorberechneter Zustände direkt in die Hardware Register kopiert.</span><span class="sxs-lookup"><span data-stu-id="40f36-126">To apply a PSO, the hardware copies a minimal amount of pre-computed state directly to the hardware registers.</span></span> <span data-ttu-id="40f36-127">Dadurch entfällt der Aufwand, der durch den Grafiktreiber aufgrund der aktuellen Rendering-und Pipeline Einstellungen durch den Grafiktreiber ständig neu berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="40f36-127">This removes the overhead caused by the graphics driver continually recomputing hardware state based on all currently applicable rendering and pipeline settings.</span></span> <span data-ttu-id="40f36-128">Das Ergebnis ist erheblich Reduzierter Aufwand für den Draw-Aufruf, eine höhere Leistung und mehr Draw-Aufrufe pro Frame.</span><span class="sxs-lookup"><span data-stu-id="40f36-128">The result is significantly reduced draw call overhead, increased performance, and more draw calls per frame.</span></span>

<span data-ttu-id="40f36-129">Der aktuell angewendete PSO definiert und verbindet alle Shader, die in der Renderingpipeline verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40f36-129">The currently applied PSO defines and connects all of the shaders being used in the rendering pipeline.</span></span> <span data-ttu-id="40f36-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) wird in Shader-Objekte vorkompiliert, die dann zur Laufzeit als Eingabe für Pipeline Zustands Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40f36-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) is pre-compiled into shader objects, which are then used at run time as input for pipeline state objects.</span></span> <span data-ttu-id="40f36-131">Weitere Informationen zur Funktionsweise von PSO in der Grafik Pipeline finden Sie unter [Verwalten des Grafik Pipeline Zustands in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="40f36-131">For more information about how the PSO functions within the graphics pipeline, see [Managing graphics pipeline state in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="direct3d-12-compute-pipeline"></a><span data-ttu-id="40f36-132">Direct3D 12 Compute-Pipeline</span><span class="sxs-lookup"><span data-stu-id="40f36-132">Direct3D 12 compute pipeline</span></span>

<span data-ttu-id="40f36-133">Das folgende Diagramm veranschaulicht die Compute-Pipeline und den Direct3D 12-computebereich.</span><span class="sxs-lookup"><span data-stu-id="40f36-133">The following diagram illustrates the Direct3D 12 compute pipeline and state.</span></span>

![Diagramm, das die Direct3D 12-Compute-Pipeline anzeigt.](images/compute-pipeline.png)

<span data-ttu-id="40f36-135">Diese Pipeline enthält keine Fixed-Funktionseinheiten, aber deskriptorheaps, samplingheaps und statische Samplern sind weiterhin in Compute verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40f36-135">There are no fixed function units in this pipeline, however descriptor heaps, sampler heaps and static samplers are still available in compute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40f36-136">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="40f36-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f36-137">Arbeits Übermittlung in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="40f36-137">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 