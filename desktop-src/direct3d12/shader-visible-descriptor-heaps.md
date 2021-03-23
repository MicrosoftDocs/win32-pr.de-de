---
title: Shader sichtbare deskriptorheaps
description: Shader sichtbare deskriptorheaps, sind deskriptorheaps, auf die Shader durch deskriptortabellen verweisen können.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103723"
---
# <a name="shader-visible-descriptor-heaps"></a><span data-ttu-id="a95e6-103">Shader sichtbare deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a95e6-103">Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="a95e6-104">Shader sichtbare deskriptorheaps, sind deskriptorheaps, auf die Shader durch deskriptortabellen verweisen können.</span><span class="sxs-lookup"><span data-stu-id="a95e6-104">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span>

-   [<span data-ttu-id="a95e6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a95e6-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="a95e6-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a95e6-106">An example</span></span>](#an-example)
-   [<span data-ttu-id="a95e6-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a95e6-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="a95e6-108">Überblick</span><span class="sxs-lookup"><span data-stu-id="a95e6-108">Overview</span></span>

<span data-ttu-id="a95e6-109">Deskriptorheaps, auf die durch Shader durch deskriptortabellen verwiesen werden kann, sind in einigen Varianten enthalten: ein heaptyp, der D3D12 \_ SRV \_ UAV \_ CBV- \_ \_ deskriptorheap, kann Shader-Ressourcen Sichten, ungeordnete Zugriffs Sichten und Konstante Puffer Ansichten enthalten, die alle gemischt sind.</span><span class="sxs-lookup"><span data-stu-id="a95e6-109">Descriptor heaps that can be referenced by shaders through descriptor tables come in a couple of flavors: One heap type, D3D12\_SRV\_UAV\_CBV\_DESCRIPTOR\_HEAP, can hold Shader Resource Views, Unordered Access Views, and Constant Buffer Views, all intermixed.</span></span> <span data-ttu-id="a95e6-110">Jeder angegebene Speicherort im Heap kann einer der aufgelisteten deskriptortypen sein.</span><span class="sxs-lookup"><span data-stu-id="a95e6-110">Any given location in the heap can be any one of the listed types of descriptors.</span></span> <span data-ttu-id="a95e6-111">Ein anderer heaptyp, D3D12 \_ Descriptor \_ Heap \_ Type \_ Sampler, speichert nur Samplern. Dies spiegelt die Tatsache wider, dass Samplern bei der Mehrzahl der Hardware getrennt von Srvs, UAVs, cbvs verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a95e6-111">Another heap type, D3D12\_DESCRIPTOR\_HEAP\_TYPE\_SAMPLER, only stores samplers, reflecting the fact that for the majority of hardware, samplers are managed separately from SRVs, UAVs, CBVs.</span></span>

<span data-ttu-id="a95e6-112">Deskriptorheaps dieser Typen können als Shader angezeigt werden, oder nicht, wenn der Heap erstellt wird (der zweite – nicht-Shader, der für die stagingdeskriptoren auf der CPU sichtbar ist).</span><span class="sxs-lookup"><span data-stu-id="a95e6-112">Descriptor heaps of these types may be requested to be shader visible or not when the heap is created (the latter – non shader visible - can be useful for staging descriptors on the CPU).</span></span> <span data-ttu-id="a95e6-113">Bei angeforderter Shader-Anforderung kann jeder der oben genannten Heap Typen eine Hardware Größenbeschränkung für jede einzelne deskriptorheap-Zuordnung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a95e6-113">When requested to be shader visible, each of the above heap types may have a hardware size limit for any individual descriptor heap allocation.</span></span>

<span data-ttu-id="a95e6-114">Anwendungen können eine beliebige Anzahl von deskriptorheaps erstellen, und nicht Shader sichtbare deskriptorheaps sind nicht in der Größe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a95e6-114">Applications can create any number of descriptor heaps , and non shader visible descriptor heaps are not constrained in size.</span></span> <span data-ttu-id="a95e6-115">Wenn ein vom Shader sichtbarer deskriptorheap, der von der Anwendung erstellt wird, kleiner ist als das Limit für die Hardware Größe, kann der Treiber den deskriptorheap aus einem größeren zugrunde liegenden deskriptorheap unterzuordnen, sodass mehrere API-deskriptorheaps in einen Hardware deskriptorheap passen.</span><span class="sxs-lookup"><span data-stu-id="a95e6-115">If a shader visible descriptor heap that is created by the application is smaller than the hardware size limit, the driver may choose to sub-allocate the descriptor heap out of a larger underlying descriptor heap so that multiple API descriptor heaps fit within one hardware descriptor heap.</span></span> <span data-ttu-id="a95e6-116">Der Grund hierfür ist, dass für einige Hardware bei der Umstellung zwischen den Hardware Deskriptor-Heaps während der Ausführung eine GPU-Wartezeit für den Leerlauf erforderlich ist (um sicherzustellen, dass GPU-Verweise auf den zuvor deskriptorheap abgeschlossen sind).</span><span class="sxs-lookup"><span data-stu-id="a95e6-116">The reason this may happen is that for some hardware, switching between hardware descriptor heaps during execution requires a GPU wait for idle (to ensure that GPU references to the previously descriptor heap are finished).</span></span> <span data-ttu-id="a95e6-117">Wenn alle deskriptorheaps, die von einer Anwendung erstellt werden, in die maximalen Kapazitäten des betreffenden Hardware Heaps passen, werden beim Wechseln von API-deskriptorheaps während des Renderings keine solchen warte Vorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a95e6-117">If all of the descriptor heaps that an application creates fit into the applicable hardware heap's maximum capacities, then no such waits will occur when switching API descriptor heaps during rendering.</span></span> <span data-ttu-id="a95e6-118">Anwendungen müssen jedoch die Möglichkeit zulassen, dass durch das Wechseln des aktuellen deskriptorheaps eine Wartezeit auf den Leerlauf verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="a95e6-118">Applications must allow for the possibility, however, that switching the current descriptor heap may incur a wait for idle.</span></span>

<span data-ttu-id="a95e6-119">Um zu vermeiden, dass diese mögliche Wartezeit auf den deskriptorheap-Schalter beeinträchtigt wird, können Anwendungen die Unterbrechung beim Rendering ausnutzen, die dazu führen, dass sich die GPU aus anderen Gründen im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="a95e6-119">To avoid being impacted by this possible wait for idle on the descriptor heap switch, applications can take advantage of breaks in rendering that would cause the GPU to idle for other reasons as the time to do descriptor heap switches, since a wait for idle is happening anyway.</span></span>

<span data-ttu-id="a95e6-120">Der Mechanismus und die Semantik zum Identifizieren von deskriptorheaps für Shader während der Befehlsliste/Paket Aufzeichnung werden in der API-Referenz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a95e6-120">The mechanism and semantics for identifying descriptor heaps to shaders during command list / bundle recording are described in the API reference.</span></span>

## <a name="an-example"></a><span data-ttu-id="a95e6-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a95e6-121">An example</span></span>

<span data-ttu-id="a95e6-122">Die folgende Abbildung zeigt zwei deskriptorheaps, die auf zwei separate 2D-Texturen verweisen, die in zwei Slots eines großen Standard Heaps gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a95e6-122">The image below shows two descriptor heaps referencing two separate 2D textures being stored in two slots of a large default heap.</span></span> <span data-ttu-id="a95e6-123">Der deskriptorheap, der als Shader sichtbar ist, kann von der Grafik Pipeline (einschließlich der Shader) aufgerufen werden. Daher ist die 2D-Textur für die Pipeline verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a95e6-123">The descriptor heap that is shader visible can be accessed by the graphics pipeline (including the shaders), and hence the 2D texture is available to the pipeline.</span></span>

![sichtbare und nicht sichtbare deskriptorheaps](images/descriptor-heaps.png)

> [!Note]  
> <span data-ttu-id="a95e6-125">Es gibt oftmals eine Beschränkung der GPU-Hardware, die von der CPU (als Schreib kombinierter Arbeitsspeicher bezeichnet) für deskriptorheaps beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="a95e6-125">There is often a limit on GPU hardware of the amount of GPU local memory writeable by the CPU (referred to as write-combined memory) for descriptor heaps.</span></span> <span data-ttu-id="a95e6-126">In der Regel beträgt dieser Grenzwert bei allen Prozessen etwa 96 MB.</span><span class="sxs-lookup"><span data-stu-id="a95e6-126">Typically this limit is around 96MB for all processes.</span></span> <span data-ttu-id="a95e6-127">Ein 1 Million-Member-deskriptorheap mit 32-Byte-Deskriptoren verwendet beispielsweise bis zu 32 MB.</span><span class="sxs-lookup"><span data-stu-id="a95e6-127">A one million member descriptor heap, with 32byte descriptors, would use up 32MB, for example.</span></span> <span data-ttu-id="a95e6-128">Der Treiber wird bei Bedarf auf den System Arbeitsspeicher zurückgreifen, aber es wird empfohlen, keine große Anzahl von großen deskriptorheaps zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a95e6-128">The driver will fall back on system memory if needed, though it is good practice not to create large numbers of large descriptor heaps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a95e6-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a95e6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a95e6-130">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a95e6-130">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




