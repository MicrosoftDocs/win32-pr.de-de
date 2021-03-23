---
title: Deskriptorheaps
description: Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104241"
---
# <a name="descriptor-heaps"></a><span data-ttu-id="a39c1-103">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a39c1-103">Descriptor Heaps</span></span>

<span data-ttu-id="a39c1-104">Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="a39c1-104">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a39c1-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a39c1-105">In this section</span></span>



| <span data-ttu-id="a39c1-106">Thema</span><span class="sxs-lookup"><span data-stu-id="a39c1-106">Topic</span></span>                                                                                             | <span data-ttu-id="a39c1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a39c1-107">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a39c1-108">Übersicht über deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a39c1-108">Descriptor Heaps Overview</span></span>](descriptor-heaps-overview.md)<br/>                             | <span data-ttu-id="a39c1-109">Deskriptorheaps enthalten viele Objekttypen, die nicht Teil eines Pipeline Zustands Objekts (PSO) sind, wie z. b. Shader-Ressourcen Sichten (Srvs), ungeordnete Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers.</span><span class="sxs-lookup"><span data-stu-id="a39c1-109">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span> <br/>                |
| [<span data-ttu-id="a39c1-110">Hardware Tarife</span><span class="sxs-lookup"><span data-stu-id="a39c1-110">Hardware Tiers</span></span>](hardware-support.md)<br/>                                                 | <span data-ttu-id="a39c1-111">Die Hardware Ebenen von Ebene 1 bis Ebene 3 verbessern die Ressourcen, die für die Pipeline verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a39c1-111">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="a39c1-112">Shader sichtbare deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a39c1-112">Shader Visible Descriptor Heaps</span></span>](shader-visible-descriptor-heaps.md)<br/>                 | <span data-ttu-id="a39c1-113">Shader sichtbare deskriptorheaps, sind deskriptorheaps, auf die Shader durch deskriptortabellen verweisen können.</span><span class="sxs-lookup"><span data-stu-id="a39c1-113">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="a39c1-114">Nicht Shader sichtbare deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a39c1-114">Non Shader Visible Descriptor Heaps</span></span>](non-shader-visible-descriptor-heaps.md)<br/>         | <span data-ttu-id="a39c1-115">Auf einige deskriptorheaps kann nicht durch Shader durch deskriptortabellen verwiesen werden. Sie ist jedoch entweder vorhanden, um der APP das Staging der Deskriptoren vor dem Aufzeichnen einer Befehlsliste zu unterstützen, oder weil kein Shader-sichtbarer Heap erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a39c1-115">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span><br/> |
| [<span data-ttu-id="a39c1-116">Erstellen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a39c1-116">Creating Descriptor Heaps</span></span>](creating-descriptor-heaps.md)<br/>                             | <span data-ttu-id="a39c1-117">Zum Erstellen und Konfigurieren eines deskriptorheaps müssen Sie einen deskriptorheap auswählen, die Anzahl der enthaltenen Deskriptoren bestimmen und Flags festlegen, die angeben, ob CPU-sichtbar und/oder Shader sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="a39c1-117">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span> <br/>                    |
| [<span data-ttu-id="a39c1-118">Festlegen und Auffüllen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="a39c1-118">Setting and Populating Descriptor Heaps</span></span>](setting-descriptor-heaps.md)<br/>                | <span data-ttu-id="a39c1-119">Die deskriptorheap-Typen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die deskriptortabellen verwendet werden können (höchstens jeweils jeweils jeweils).</span><span class="sxs-lookup"><span data-stu-id="a39c1-119">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span> <br/>                                                        |
| [<span data-ttu-id="a39c1-120">Deskriptorheap-Konfigurations Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a39c1-120">Descriptor Heap Configurability Summary</span></span>](descriptor-heap-configurability-summary.md)<br/> | <span data-ttu-id="a39c1-121">In der folgenden Tabelle werden Informationen zur Unterstützung von Shader und nicht-Shader-sichtbarem Heap zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="a39c1-121">The following table summarizes information about Shader and non-Shader visible heap support.</span></span><br/>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a39c1-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a39c1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a39c1-123">Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="a39c1-123">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="a39c1-124">Deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="a39c1-124">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="a39c1-125">**ID3D12DescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="a39c1-125">**ID3D12DescriptorHeap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[<span data-ttu-id="a39c1-126">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="a39c1-126">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="a39c1-127">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="a39c1-127">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





