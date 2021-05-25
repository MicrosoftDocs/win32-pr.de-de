---
title: Für den Shader nicht sichtbare Deskriptorheaps
description: Auf einige Deskriptorheaps kann von Shadern nicht über Deskriptortabellen verwiesen werden, sie sind jedoch entweder vorhanden, um die App beim Staging der Deskriptoren vor der Aufzeichnung einer Befehlsliste zu unterstützen, oder weil kein shader-sichtbarer Heap erforderlich ist.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343455"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="6fb77-103">Für den Shader nicht sichtbare Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="6fb77-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="6fb77-104">Auf einige Deskriptorheaps kann von Shadern nicht über Deskriptortabellen verwiesen werden, sie sind jedoch entweder vorhanden, um die App beim Staging der Deskriptoren vor der Aufzeichnung einer Befehlsliste zu unterstützen, oder weil kein shader-sichtbarer Heap erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6fb77-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="6fb77-105">Nicht sichtbare Ansichten</span><span class="sxs-lookup"><span data-stu-id="6fb77-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="6fb77-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6fb77-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="6fb77-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6fb77-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="6fb77-108">Nicht sichtbare Ansichten</span><span class="sxs-lookup"><span data-stu-id="6fb77-108">Non-visible views</span></span>

<span data-ttu-id="6fb77-109">Alle Deskriptorheaps, einschließlich der zuvor beschriebenen Shader-Deskriptorheaps, können von den CPU- und/oder Befehlslisten abhängig vom Arbeitsspeicherpool und den CPU-Zugriffseigenschaften bearbeitet werden, die die Anwendung für einen Deskriptorheap auswählt.</span><span class="sxs-lookup"><span data-stu-id="6fb77-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="6fb77-110">Für [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md)ist der offensichtliche Grund, shader den Zugriff auf diese Deskriptorheaps zu verweigern, während sie ge staget werden.</span><span class="sxs-lookup"><span data-stu-id="6fb77-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="6fb77-111">Anschließend werden diese Heaps als Shader sichtbar gemacht und über Deskriptortabellen bei der Ausführung der Befehlsliste aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6fb77-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="6fb77-112">Es ist jedoch nicht erforderlich, für Shader sichtbare Heaps zu stagen, da sie direkt aufgefüllt werden können.</span><span class="sxs-lookup"><span data-stu-id="6fb77-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="6fb77-113">Andere Deskriptoren werden an die Pipeline gebunden, indem ihre Inhalte direkt in der Befehlsliste aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6fb77-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="6fb77-114">Diese Deskriptoren dienen nur dazu, die Ansichtsparameter zum Zeitpunkt des Befehlslisten-Datensatzes zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="6fb77-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="6fb77-115">Diese Heaps sind immer nicht als Shader sichtbar und enthalten Folgendes.</span><span class="sxs-lookup"><span data-stu-id="6fb77-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="6fb77-116">Renderzielansichten (RTVs)</span><span class="sxs-lookup"><span data-stu-id="6fb77-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="6fb77-117">Tiefenschablonenansichten (DSVs)</span><span class="sxs-lookup"><span data-stu-id="6fb77-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="6fb77-118">Indexpuffersichten (IBVs), Vertexpuffersichten (VBVs) und Streamausgabesichten (Stream Output Views, SOVs) werden direkt an API-Methoden übergeben und weisen keine bestimmten Heaptypen auf.</span><span class="sxs-lookup"><span data-stu-id="6fb77-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="6fb77-119">Nach der Aufzeichnung in der Befehlsliste (z. B. mit einem Aufruf wie [**OMSetRenderTargets)**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)steht der Arbeitsspeicher, der zum Speichern der Deskriptoren für diesen Aufruf verwendet wird, sofort zur erneuten Verwendung nach dem Aufruf zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6fb77-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="6fb77-120">Selbst Deskriptortabellen verfügen über Optionen, bei denen eine App es der Implementierung ermöglichen kann, den Tabelleninhalt bei der Befehlslistenaufzeichnung aufzuzeichnen (anstatt den Tabellenzeiger bei der Ausführung zu dereferenzieren).</span><span class="sxs-lookup"><span data-stu-id="6fb77-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="6fb77-121">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6fb77-121">Summary</span></span>



|                   | <span data-ttu-id="6fb77-122">Shader sichtbar, nur CPU-Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="6fb77-122">Shader visible, CPU write only</span></span>                                   | <span data-ttu-id="6fb77-123">Nicht-Shader sichtbar, CPU-Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="6fb77-123">Non-shader visible, CPU read/write</span></span>                                       |
|-------------------|------------------------------------|----------------------------------------|
| <span data-ttu-id="6fb77-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="6fb77-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="6fb77-125">Ja</span><span class="sxs-lookup"><span data-stu-id="6fb77-125">yes</span></span>                                | <span data-ttu-id="6fb77-126">Ja</span><span class="sxs-lookup"><span data-stu-id="6fb77-126">yes</span></span>                                    |
| <span data-ttu-id="6fb77-127">**Sampler**</span><span class="sxs-lookup"><span data-stu-id="6fb77-127">**SAMPLER**</span></span>       | <span data-ttu-id="6fb77-128">Ja</span><span class="sxs-lookup"><span data-stu-id="6fb77-128">yes</span></span>                                | <span data-ttu-id="6fb77-129">Ja</span><span class="sxs-lookup"><span data-stu-id="6fb77-129">yes</span></span>                                    |
| <span data-ttu-id="6fb77-130">**RTV**</span><span class="sxs-lookup"><span data-stu-id="6fb77-130">**RTV**</span></span>           | <span data-ttu-id="6fb77-131">nein</span><span class="sxs-lookup"><span data-stu-id="6fb77-131">no</span></span>                                 | <span data-ttu-id="6fb77-132">Ja</span><span class="sxs-lookup"><span data-stu-id="6fb77-132">yes</span></span>                                    |
| <span data-ttu-id="6fb77-133">**Dsv**</span><span class="sxs-lookup"><span data-stu-id="6fb77-133">**DSV**</span></span>           | <span data-ttu-id="6fb77-134">nein</span><span class="sxs-lookup"><span data-stu-id="6fb77-134">no</span></span>                                 | <span data-ttu-id="6fb77-135">Ja</span><span class="sxs-lookup"><span data-stu-id="6fb77-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="6fb77-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fb77-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fb77-137">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="6fb77-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




