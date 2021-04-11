---
description: Die Grafik Pipeline Direct3D 10 stellt eine grundlegende Architektur Änderung dar, die von Grund auf für Hardware und Software neu erstellt wird, um die nächste Generation von spielen und 3D-Multimedia-Anwendungen zu unterhalten.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: API-Features (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214086"
---
# <a name="api-features-direct3d-10"></a><span data-ttu-id="a998a-103">API-Features (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a998a-103">API Features (Direct3D 10)</span></span>

<span data-ttu-id="a998a-104">Die Grafik Pipeline Direct3D 10 stellt eine grundlegende Architektur Änderung dar, die von Grund auf für Hardware und Software neu erstellt wird, um die nächste Generation von spielen und 3D-Multimedia-Anwendungen zu unterhalten.</span><span class="sxs-lookup"><span data-stu-id="a998a-104">The Direct3D 10 graphics pipeline represents a fundamental architecture change, rebuilt from the ground-up in hardware and software to power the next-generation of games and 3D multimedia applications.</span></span> <span data-ttu-id="a998a-105">Es verwendet das Windows-Anzeigetreiber Modell (WDDM), das Leistungs-und Verhaltens Verbesserungen wie den virtuellen GPU-Speicher ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a998a-105">It uses the Windows Display Driver Model (WDDM), which enables performance and behavioral enhancements such as virtual GPU memory.</span></span>

<span data-ttu-id="a998a-106">Entwickler, die mit Direct3D 9 vertraut sind, werden eine Reihe von funktionalen Erweiterungen und Leistungsverbesserungen in Direct3D 10 ermitteln, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="a998a-106">Developers familiar with Direct3D 9 will discover a series of functional enhancements and performance improvements in Direct3D 10, including:</span></span>

-   <span data-ttu-id="a998a-107">Die Fähigkeit zum Verarbeiten ganzer primitiver Elemente in der neuen [Geometry-Shader-Stufe](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a998a-107">The ability to process entire primitives in the new [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>
-   <span data-ttu-id="a998a-108">Die Möglichkeit zum Ausgeben von Pipeline generierten Vertex-Daten in den Arbeitsspeicher mithilfe der [Stream-Output-Phase](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span><span class="sxs-lookup"><span data-stu-id="a998a-108">The ability to output pipeline-generated vertex data to memory using the [stream-output stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span></span>
-   <span data-ttu-id="a998a-109">Organisation des Pipeline Zustands in 5 unveränderliche [Zustands Objekte](d3d10-graphics-programming-guide-api-features-state-objects.md), die eine schnelle Konfiguration der Pipeline ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a998a-109">Organization of pipeline state into 5 immutable [state objects](d3d10-graphics-programming-guide-api-features-state-objects.md), enabling fast configuration of the pipeline.</span></span>
-   <span data-ttu-id="a998a-110">Organisation von shaderkonstanten in [Konstante Puffer](d3d10-graphics-programming-guide-resources-types.md), wodurch der Bandbreiten Aufwand für die Bereitstellung von Shader-Konstanten Daten minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="a998a-110">Organization of shader constants into [constant buffers](d3d10-graphics-programming-guide-resources-types.md), minimizing bandwidth overhead for supplying shader-constant data.</span></span>
-   <span data-ttu-id="a998a-111">Die Möglichkeit, das austauschen und einrichten pro primitiver Materialien mithilfe eines Geometry-Shaders durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a998a-111">The ability to perform per-primitive material swapping and setup using a geometry shader.</span></span>
-   <span data-ttu-id="a998a-112">Neue [Ressourcentypen](d3d10-graphics-programming-guide-resources-types.md) (einschließlich Textur Arrays, die von Shader indiziert werden können) und Ressourcen Formate.</span><span class="sxs-lookup"><span data-stu-id="a998a-112">New [resource types](d3d10-graphics-programming-guide-resources-types.md) (including texture arrays that can be indexed from shaders) and resource formats.</span></span>
-   <span data-ttu-id="a998a-113">Erhöhung der Generalisierung des Ressourcen Zugriffs mithilfe einer [Ansicht](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="a998a-113">Increased generalization of resource access using a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>
-   <span data-ttu-id="a998a-114">Ältere hardwarefunktionsbits (Caps) wurden zugunsten eines umfangreichen Satzes von garantierten Funktionen entfernt, die auf Direct3D 10-Class Hardware (minimal) ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="a998a-114">Legacy hardware capability bits (caps) have been removed in favor of a rich set of guaranteed functionality, which targets Direct3D 10-class hardware (minimum).</span></span>
-   <span data-ttu-id="a998a-115">[Geschichtete Laufzeit](d3d10-graphics-programming-guide-api-features-layers.md) : die Direct3D 10-API wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen (Debug usw.) in äußeren Ebenen.</span><span class="sxs-lookup"><span data-stu-id="a998a-115">[Layered Runtime](d3d10-graphics-programming-guide-api-features-layers.md) - The Direct3D 10 API is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality (debug, etc.) in outer layers.</span></span>
-   <span data-ttu-id="a998a-116">Vollständige HLSL-Integration-alle Direct3D 10-Shader werden in HLSL geschrieben und mit dem [Common-Shader-Kern](../direct3dhlsl/dx-graphics-hlsl-common-core.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="a998a-116">Full HLSL integration - All Direct3D 10 shaders are written in HLSL and implemented with the [common-shader core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span></span>
-   <span data-ttu-id="a998a-117">Eine Erhöhung der Anzahl von renderzielen, Texturen und Samplern.</span><span class="sxs-lookup"><span data-stu-id="a998a-117">An increase in the number of render targets, textures, and samplers.</span></span> <span data-ttu-id="a998a-118">Es gibt auch keine Längen Beschränkung für Shader.</span><span class="sxs-lookup"><span data-stu-id="a998a-118">There is also no shader length limit.</span></span>
-   <span data-ttu-id="a998a-119">Ganzzahlige und bitweise shadervorgänge.</span><span class="sxs-lookup"><span data-stu-id="a998a-119">Integer and bitwise shader operations.</span></span>
-   <span data-ttu-id="a998a-120">Ein Rückschlag einer tiefen-/Schablone-Oberfläche oder einer Multisampling-Ressource, sobald Sie nicht mehr als Renderziel gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="a998a-120">Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.</span></span>
-   <span data-ttu-id="a998a-121">Multisampling-Unterstützung für Alpha-zu-Abdeckung.</span><span class="sxs-lookup"><span data-stu-id="a998a-121">Multisampled alpha-to-coverage support.</span></span>

<span data-ttu-id="a998a-122">Es gibt zusätzliche Verhaltensunterschiede, die Direct3D 9-Entwicklern auch bekannt sein sollten (siehe [Direct3D 9 bis Direct3D 10 Überlegungen](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span><span class="sxs-lookup"><span data-stu-id="a998a-122">There are additional behavioral differences that Direct3D 9 developers should also be aware of (see [Direct3D 9 to Direct3D 10 Considerations](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span></span>

<span data-ttu-id="a998a-123">Im folgenden finden Sie eine Liste der Direct3D 9-Features, die entweder nicht mehr unterstützt werden oder in Direct3D 10 geändert wurden (siehe [Veraltete Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span><span class="sxs-lookup"><span data-stu-id="a998a-123">Here is a list of Direct3D 9 features that either are no longer supported, or have been revised in Direct3D 10 (see [Deprecated Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a998a-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a998a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a998a-125">Programmier Handbuch für Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="a998a-125">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
