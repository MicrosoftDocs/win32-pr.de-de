---
title: Nicht Shader sichtbare deskriptorheaps
description: Auf einige deskriptorheaps kann nicht durch Shader durch deskriptortabellen verwiesen werden. Sie ist jedoch entweder vorhanden, um der APP das Staging der Deskriptoren vor dem Aufzeichnen einer Befehlsliste zu unterstützen, oder weil kein Shader-sichtbarer Heap erforderlich ist.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548665"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="b4108-103">Nicht Shader sichtbare deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="b4108-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="b4108-104">Auf einige deskriptorheaps kann nicht durch Shader durch deskriptortabellen verwiesen werden. Sie ist jedoch entweder vorhanden, um der APP das Staging der Deskriptoren vor dem Aufzeichnen einer Befehlsliste zu unterstützen, oder weil kein Shader-sichtbarer Heap erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b4108-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="b4108-105">Nicht sichtbare Sichten</span><span class="sxs-lookup"><span data-stu-id="b4108-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="b4108-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b4108-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="b4108-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b4108-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="b4108-108">Nicht sichtbare Sichten</span><span class="sxs-lookup"><span data-stu-id="b4108-108">Non-visible views</span></span>

<span data-ttu-id="b4108-109">Alle deskriptorheaps, einschließlich der zuvor beschriebenen deskriptorheaps für Shader, können je nach Arbeitsspeicher Pool und den CPU-Zugriffs Eigenschaften, die von der Anwendung für einen deskriptorheap ausgewählt werden, von der CPU-und/oder der Befehlsliste bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b4108-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="b4108-110">Für [Shader sichtbare deskriptorheaps](shader-visible-descriptor-heaps.md)ist der offensichtliche Grund, den Shader-Zugriff auf diese deskriptorheaps zu verweigern, während Sie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4108-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="b4108-111">Anschließend werden diese Heaps in den Shader-sichtbar umgewandelt, und der Zugriff erfolgt über deskriptortabellen bei der Ausführung der Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="b4108-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="b4108-112">Es ist jedoch nicht erforderlich, für Shader sichtbare Heaps bereitzustellen. Sie können direkt ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="b4108-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="b4108-113">Andere Deskriptoren werden an die Pipeline gebunden, indem ihre Inhalte direkt in der Befehlsliste aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b4108-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="b4108-114">Diese Deskriptoren dienen nur zur Übersetzung der Ansichts Parameter in der Befehlslisten-Daten Satz Zeit.</span><span class="sxs-lookup"><span data-stu-id="b4108-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="b4108-115">Diese Heaps sind immer nicht-Shader sichtbar und enthalten Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b4108-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="b4108-116">Renderzielsichten (rtvs)</span><span class="sxs-lookup"><span data-stu-id="b4108-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="b4108-117">Tiefen Schablonen Ansichten (DSVs)</span><span class="sxs-lookup"><span data-stu-id="b4108-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="b4108-118">Index Puffer Sichten (ibvs), Vertex-Puffer Sichten (vbvs) und Stream-Ausgabe Sichten (sovs) werden direkt an API-Methoden übermittelt, verfügen nicht über bestimmte Heap Typen.</span><span class="sxs-lookup"><span data-stu-id="b4108-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="b4108-119">Nach dem aufzeichnen in der Befehlsliste (z. b. mit einem-Befehl wie z. b. [**omstrendertargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)) steht der Arbeitsspeicher, der zum Speichern der Deskriptoren für diesen Befehl verwendet wurde, sofort zur erneuten Verwendung nach dem-Befehl zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b4108-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="b4108-120">Auch deskriptortabellen haben Optionen, bei denen eine APP es der Implementierung ermöglicht, den Tabelleninhalt bei der Aufzeichnung der Befehlsliste aufzuzeichnen (anstatt den Tabellen Zeiger bei der Ausführung zu dereferenzieren).</span><span class="sxs-lookup"><span data-stu-id="b4108-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="b4108-121">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b4108-121">Summary</span></span>



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | <span data-ttu-id="b4108-122">**Shader sichtbar, nur CPU-Schreibvorgänge**</span><span class="sxs-lookup"><span data-stu-id="b4108-122">**shader visible, CPU write only**</span></span> | <span data-ttu-id="b4108-123">**nicht-Shader sichtbar, CPU-Lese-/Schreibzugriff**</span><span class="sxs-lookup"><span data-stu-id="b4108-123">**non-shader visible, CPU read/write**</span></span> |
| <span data-ttu-id="b4108-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="b4108-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="b4108-125">ja</span><span class="sxs-lookup"><span data-stu-id="b4108-125">yes</span></span>                                | <span data-ttu-id="b4108-126">ja</span><span class="sxs-lookup"><span data-stu-id="b4108-126">yes</span></span>                                    |
| <span data-ttu-id="b4108-127">**Sammel**</span><span class="sxs-lookup"><span data-stu-id="b4108-127">**SAMPLER**</span></span>       | <span data-ttu-id="b4108-128">ja</span><span class="sxs-lookup"><span data-stu-id="b4108-128">yes</span></span>                                | <span data-ttu-id="b4108-129">ja</span><span class="sxs-lookup"><span data-stu-id="b4108-129">yes</span></span>                                    |
| <span data-ttu-id="b4108-130">**RTV**</span><span class="sxs-lookup"><span data-stu-id="b4108-130">**RTV**</span></span>           | <span data-ttu-id="b4108-131">Nein</span><span class="sxs-lookup"><span data-stu-id="b4108-131">no</span></span>                                 | <span data-ttu-id="b4108-132">ja</span><span class="sxs-lookup"><span data-stu-id="b4108-132">yes</span></span>                                    |
| <span data-ttu-id="b4108-133">**DSV**</span><span class="sxs-lookup"><span data-stu-id="b4108-133">**DSV**</span></span>           | <span data-ttu-id="b4108-134">Nein</span><span class="sxs-lookup"><span data-stu-id="b4108-134">no</span></span>                                 | <span data-ttu-id="b4108-135">ja</span><span class="sxs-lookup"><span data-stu-id="b4108-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b4108-136">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b4108-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4108-137">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="b4108-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




