---
title: Pipeline Zugriff auf gekachelte Ressourcen
description: Gekachelte Ressourcen können in Shader-Ressourcen Ansichten (SRV), renderzielsichten (RTV), Datenquellen Sichten (Datenquellen Sicht) und unsortierter Zugriffs Ansichten (UAV) sowie einigen Bindungs Punkten verwendet werden, bei denen Sichten nicht verwendet werden, wie z. b. Vertex-Puffer Bindungen.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729256"
---
# <a name="pipeline-access-to-tiled-resources"></a><span data-ttu-id="740d8-103">Pipeline Zugriff auf gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="740d8-103">Pipeline access to tiled resources</span></span>

<span data-ttu-id="740d8-104">Gekachelte Ressourcen können in Shader-Ressourcen Ansichten (SRV), renderzielsichten (RTV), Datenquellen Sichten (Datenquellen Sicht) und unsortierter Zugriffs Ansichten (UAV) sowie einigen Bindungs Punkten verwendet werden, bei denen Sichten nicht verwendet werden, wie z. b. Vertex-Puffer Bindungen.</span><span class="sxs-lookup"><span data-stu-id="740d8-104">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <span data-ttu-id="740d8-105">Eine Liste der unterstützten Bindungen finden Sie unter Parameter für die [Kachel Ressourcen Erstellung](tiled-resource-creation-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="740d8-105">For the list of supported bindings, see [Tiled resource creation parameters](tiled-resource-creation-parameters.md).</span></span> <span data-ttu-id="740d8-106">Kopier \* Vorgänge funktionieren auch für gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="740d8-106">Copy\* operations also work on tiled resources.</span></span>

<span data-ttu-id="740d8-107">Wenn mehrere Kachel Koordinaten in einer oder mehreren Ansichten an denselben Speicherort gebunden sind, werden Lese-und Schreibvorgänge aus unterschiedlichen Pfaden desselben Speichers in einer nicht deterministischen und nicht wiederholbaren Reihenfolge von Speicherzugriffen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="740d8-107">If multiple tile coordinates in one or more views is bound to the same memory location, reads and writes from different paths to the same memory will occur in a non-deterministic and non-repeatable order of memory accesses.</span></span>

<span data-ttu-id="740d8-108">Wenn alle Kacheln hinter einer Speicherzugriffs Beanspruchung von einem Shader eindeutigen Kacheln zugeordnet sind, ist das Verhalten auf allen Implementierungen mit der Oberfläche identisch, die den gleichen Speicherinhalt auf nicht gekachelte Weise aufweisen.</span><span class="sxs-lookup"><span data-stu-id="740d8-108">If all tiles behind a memory access footprint from a shader are mapped to unique tiles, behavior is identical on all implementations to the surface having the same memory contents in a non-tiled fashion.</span></span>

<span data-ttu-id="740d8-109">In diesem Abschnitt finden Sie weitere Informationen über den Pipeline Zugriff auf gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="740d8-109">This section provides more info about pipeline access to tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="740d8-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="740d8-110">In this section</span></span>



| <span data-ttu-id="740d8-111">Thema</span><span class="sxs-lookup"><span data-stu-id="740d8-111">Topic</span></span>                                                                                                              | <span data-ttu-id="740d8-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="740d8-112">Description</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="740d8-113">SRV-verhalten bei nicht zugeordneten Kacheln</span><span class="sxs-lookup"><span data-stu-id="740d8-113">SRV behavior with non-mapped tiles</span></span>](srv-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="740d8-114">Das Verhalten von Lesevorgängen in der Shader-Ressourcen Ansicht (SRV), die nicht zugeordnete Kacheln einschließen, hängt von der Hardwareunterstützung ab.</span><span class="sxs-lookup"><span data-stu-id="740d8-114">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <br/>                                          |
| [<span data-ttu-id="740d8-115">UAV-verhalten bei nicht zugeordneten Kacheln</span><span class="sxs-lookup"><span data-stu-id="740d8-115">UAV behavior with non-mapped tiles</span></span>](uav-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="740d8-116">Das Verhalten von Lese-und Schreibvorgängen für die ungeordnete Zugriffs Ansicht (UAV) hängt von der Hardwareunterstützung ab.</span><span class="sxs-lookup"><span data-stu-id="740d8-116">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <br/>                                                            |
| [<span data-ttu-id="740d8-117">Rasterizerverhalten bei nicht zugeordneten Kacheln</span><span class="sxs-lookup"><span data-stu-id="740d8-117">Rasterizer behavior with non-mapped tiles</span></span>](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | <span data-ttu-id="740d8-118">In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.</span><span class="sxs-lookup"><span data-stu-id="740d8-118">This section describes rasterizer behavior with non-mapped tiles.</span></span><br/>                                                                                              |
| [<span data-ttu-id="740d8-119">Kachelzugriffseinschränkungen bei doppelten Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="740d8-119">Tile access limitations with duplicate mappings</span></span>](tile-access-limitations-with-duplicate-mappings-.md)<br/> | <span data-ttu-id="740d8-120">In diesem Abschnitt werden Kachel Zugriffs Einschränkungen mit doppelten Zuordnungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="740d8-120">This section describes tile access limitations with duplicate mappings.</span></span><br/>                                                                                        |
| [<span data-ttu-id="740d8-121">Funktionen für Textur Stichproben der Kachel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="740d8-121">Tiled resources texture sampling features</span></span>](tiled-resources-texture-sampling-features.md)<br/>              | <span data-ttu-id="740d8-122">In diesem Abschnitt werden die Funktionen für Textur Stichproben von Kacheln beschrieben</span><span class="sxs-lookup"><span data-stu-id="740d8-122">This section describes tiled resources texture sampling features.</span></span><br/>                                                                                              |
| [<span data-ttu-id="740d8-123">Verfügbar machen von HLSL-Kacheln</span><span class="sxs-lookup"><span data-stu-id="740d8-123">HLSL tiled resources exposure</span></span>](hlsl-tiled-resources-exposure.md)<br/>                                      | <span data-ttu-id="740d8-124">Die neue Syntax von Microsoft High Level Shader Language (HLSL) ist erforderlich, um gekachelte Ressourcen in [Shader-Modell 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="740d8-124">New Microsoft High Level Shader Language (HLSL) syntax is required to support tiled resources in [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="740d8-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="740d8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="740d8-126">Gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="740d8-126">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

