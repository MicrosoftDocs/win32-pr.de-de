---
title: Hardware Tarife
description: Die Hardware Ebenen von Ebene 1 bis Ebene 3 verbessern die Ressourcen, die für die Pipeline verfügbar sind.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548638"
---
# <a name="hardware-tiers"></a><span data-ttu-id="7e13c-103">Hardware Tarife</span><span class="sxs-lookup"><span data-stu-id="7e13c-103">Hardware Tiers</span></span>

<span data-ttu-id="7e13c-104">Die Hardware Ebenen von Ebene 1 bis Ebene 3 verbessern die Ressourcen, die für die Pipeline verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7e13c-104">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span>

-   [<span data-ttu-id="7e13c-105">Von hardwareabhängige Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="7e13c-105">Limits dependant on hardware</span></span>](#limits-dependant-on-hardware)
-   [<span data-ttu-id="7e13c-106">Invariablenlimits</span><span class="sxs-lookup"><span data-stu-id="7e13c-106">Invariable limits</span></span>](#invariable-limits)
-   [<span data-ttu-id="7e13c-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7e13c-107">Related topics</span></span>](#related-topics)

## <a name="limits-dependant-on-hardware"></a><span data-ttu-id="7e13c-108">Von hardwareabhängige Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="7e13c-108">Limits dependant on hardware</span></span>



| <span data-ttu-id="7e13c-109">Verfügbare Ressourcen für die Pipeline</span><span class="sxs-lookup"><span data-stu-id="7e13c-109">Resources Available to the Pipeline</span></span>                                                                                                              | <span data-ttu-id="7e13c-110">Ebene 1</span><span class="sxs-lookup"><span data-stu-id="7e13c-110">Tier 1</span></span>                                                                   | <span data-ttu-id="7e13c-111">Ebene 2</span><span class="sxs-lookup"><span data-stu-id="7e13c-111">Tier 2</span></span>        | <span data-ttu-id="7e13c-112">Ebene 3</span><span class="sxs-lookup"><span data-stu-id="7e13c-112">Tier 3</span></span>        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| <span data-ttu-id="7e13c-113">Featureebenen</span><span class="sxs-lookup"><span data-stu-id="7e13c-113">Feature levels</span></span>                                                                                                                                   | <span data-ttu-id="7e13c-114">11.0 und höher</span><span class="sxs-lookup"><span data-stu-id="7e13c-114">11.0+</span></span>                                                                    | <span data-ttu-id="7e13c-115">11.0 und höher</span><span class="sxs-lookup"><span data-stu-id="7e13c-115">11.0+</span></span>         | <span data-ttu-id="7e13c-116">11.1 +</span><span class="sxs-lookup"><span data-stu-id="7e13c-116">11.1+</span></span>         |
| <span data-ttu-id="7e13c-117">Maximale Anzahl von Deskriptoren in einer Konstanten Puffer Ansicht (CBV), Shader Ressourcenansicht (SRV) oder unsortierter Zugriffs Ansicht-Heap (UAV), der für das Rendering verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7e13c-117">Maximum number of descriptors in a Constant Buffer View (CBV), Shader Resource View (SRV), or Unordered Access View(UAV) heap used for rendering</span></span> | <span data-ttu-id="7e13c-118">1\.000.000</span><span class="sxs-lookup"><span data-stu-id="7e13c-118">1,000,000</span></span>                                                                | <span data-ttu-id="7e13c-119">1\.000.000</span><span class="sxs-lookup"><span data-stu-id="7e13c-119">1,000,000</span></span>     | <span data-ttu-id="7e13c-120">1000000 +</span><span class="sxs-lookup"><span data-stu-id="7e13c-120">1,000,000+</span></span>    |
| <span data-ttu-id="7e13c-121">Maximale Anzahl konstanter Puffer Sichten in allen deskriptortabellen pro Shader-Stufe</span><span class="sxs-lookup"><span data-stu-id="7e13c-121">Maximum number of Constant Buffer Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="7e13c-122">14</span><span class="sxs-lookup"><span data-stu-id="7e13c-122">14</span></span>                                                                       | <span data-ttu-id="7e13c-123">14</span><span class="sxs-lookup"><span data-stu-id="7e13c-123">14</span></span>            | <span data-ttu-id="7e13c-124">**vollständiger Heap**</span><span class="sxs-lookup"><span data-stu-id="7e13c-124">**full heap**</span></span> |
| <span data-ttu-id="7e13c-125">Maximale Anzahl von Shader-Ressourcen Sichten in allen deskriptortabellen pro Shader-Stufe</span><span class="sxs-lookup"><span data-stu-id="7e13c-125">Maximum number of Shader Resource Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="7e13c-126">128</span><span class="sxs-lookup"><span data-stu-id="7e13c-126">128</span></span>                                                                      | <span data-ttu-id="7e13c-127">**vollständiger Heap**</span><span class="sxs-lookup"><span data-stu-id="7e13c-127">**full heap**</span></span> | <span data-ttu-id="7e13c-128">vollständiger Heap</span><span class="sxs-lookup"><span data-stu-id="7e13c-128">full heap</span></span>     |
| <span data-ttu-id="7e13c-129">Maximale Anzahl von ungeordneten Zugriffs Sichten in allen deskriptortabellen in allen Phasen</span><span class="sxs-lookup"><span data-stu-id="7e13c-129">Maximum number of Unordered Access Views in all descriptor tables across all stages</span></span>                                                              | <span data-ttu-id="7e13c-130">64 für Funktionsebenen 11.1 und höher</span><span class="sxs-lookup"><span data-stu-id="7e13c-130">64 for feature levels 11.1+</span></span><br/> <span data-ttu-id="7e13c-131">8 für Featureebene 11</span><span class="sxs-lookup"><span data-stu-id="7e13c-131">8 for feature level 11</span></span><br/> | <span data-ttu-id="7e13c-132">64</span><span class="sxs-lookup"><span data-stu-id="7e13c-132">64</span></span>            | <span data-ttu-id="7e13c-133">**vollständiger Heap**</span><span class="sxs-lookup"><span data-stu-id="7e13c-133">**full heap**</span></span> |
| <span data-ttu-id="7e13c-134">Maximale Anzahl von Samplern in allen deskriptortabellen pro Shader-Phase</span><span class="sxs-lookup"><span data-stu-id="7e13c-134">Maximum number of Samplers in all descriptor tables per shader stage</span></span>                                                                             | <span data-ttu-id="7e13c-135">16</span><span class="sxs-lookup"><span data-stu-id="7e13c-135">16</span></span>                                                                       | <span data-ttu-id="7e13c-136">**2048**</span><span class="sxs-lookup"><span data-stu-id="7e13c-136">**2048**</span></span> | <span data-ttu-id="7e13c-137">2048</span><span class="sxs-lookup"><span data-stu-id="7e13c-137">2048</span></span>     |



 

<span data-ttu-id="7e13c-138">In **fetten** Einträgen werden deutliche Verbesserungen gegenüber der vorherigen Ebene hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="7e13c-138">**Bold** entries highlight significant improvements over the previous tier.</span></span>

<span data-ttu-id="7e13c-139">Es gibt eine zusätzliche Einschränkung für die Hardware der Ebene 1, die für alle Heaps gilt. und auf Ebene 2-Hardware, die für CBV und UAV-Heaps gilt, dass alle deskriptorheap-Einträge, die von deskriptortabellen in der Stamm Signatur abgedeckt werden, beim Ausführen des Shaders mit Deskriptoren aufgefüllt werden *müssen* , selbst wenn der Shader (möglicherweise aufgrund einer Verzweigung) den Deskriptor nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="7e13c-139">There is an additional restriction for Tier 1 hardware that applies to all heaps, and to Tier 2 hardware that applies to CBV and UAV heaps, that all descriptor heap entries covered by descriptor tables in the root signature *must* be populated with descriptors by the time the shader executes, even if the shader (perhaps due to branching) does not need the descriptor.</span></span> <span data-ttu-id="7e13c-140">Es gibt keine Einschränkung für die Hardware der Ebene 3.</span><span class="sxs-lookup"><span data-stu-id="7e13c-140">There is no such restriction for Tier 3 hardware.</span></span> <span data-ttu-id="7e13c-141">Eine Entschärfung für diese Einschränkung ist die sorgfältige Verwendung von [null-Deskriptoren](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="7e13c-141">One mitigation for this restriction is the diligent use of [Null descriptors](descriptors.md).</span></span>

## <a name="invariable-limits"></a><span data-ttu-id="7e13c-142">Invariablenlimits</span><span class="sxs-lookup"><span data-stu-id="7e13c-142">Invariable limits</span></span>

<span data-ttu-id="7e13c-143">Die maximale Anzahl von Samplern in einem sichtbaren Shader-deskriptorheap ist 2048.</span><span class="sxs-lookup"><span data-stu-id="7e13c-143">The maximum number of samplers in a shader visible descriptor heap is 2048.</span></span>

<span data-ttu-id="7e13c-144">Die maximale Anzahl von eindeutigen statischen Samplern in Live Stamm Signaturen beträgt 2032 (bei Treibern, die eigene Samplern benötigen), wird der Wert "16" beibehalten.</span><span class="sxs-lookup"><span data-stu-id="7e13c-144">The maximum number of unique static samplers across live root signatures is 2032 (which leaves 16 for drivers that need their own samplers).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e13c-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7e13c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e13c-146">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="7e13c-146">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="7e13c-147">Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="7e13c-147">Hardware Feature Levels</span></span>](hardware-feature-levels.md)
</dt> </dl>

 

 





