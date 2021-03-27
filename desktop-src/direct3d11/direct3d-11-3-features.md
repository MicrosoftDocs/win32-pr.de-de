---
title: Direct3D 11,3-Features
description: In den folgenden Abschnitten wird beschrieben, wie die Funktionalität in Direct3D 11,3 hinzugefügt wurde. Diese Features sind auch in Direct3D 12 verfügbar.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391261"
---
# <a name="direct3d-113-features"></a><span data-ttu-id="7d49b-104">Direct3D 11,3-Features</span><span class="sxs-lookup"><span data-stu-id="7d49b-104">Direct3D 11.3 Features</span></span>

<span data-ttu-id="7d49b-105">In den folgenden Abschnitten wird beschrieben, wie die Funktionalität in Direct3D 11,3 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d49b-105">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="7d49b-106">Diese Features sind auch in Direct3D 12 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d49b-106">These features are also available in Direct3D 12.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="7d49b-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7d49b-107">In this section</span></span>



| <span data-ttu-id="7d49b-108">Thema</span><span class="sxs-lookup"><span data-stu-id="7d49b-108">Topic</span></span>                                                                                               | <span data-ttu-id="7d49b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d49b-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d49b-110">Konservative Rasterung</span><span class="sxs-lookup"><span data-stu-id="7d49b-110">Conservative Rasterization</span></span>](conservative-rasterization.md)<br/>                             | <span data-ttu-id="7d49b-111">Die konservative rasterisierung sorgt für ein gewisses Maß an Sicherheit für das Pixel Rendering. Dies ist insbesondere bei Algorithmen zum Erkennen von Kollisionen hilfreich.</span><span class="sxs-lookup"><span data-stu-id="7d49b-111">Conservative rasterization adds some certainty to pixel rendering, which is helpful in particular to collision detection algorithms.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7d49b-112">Standard Textur Zuordnung</span><span class="sxs-lookup"><span data-stu-id="7d49b-112">Default Texture Mapping</span></span>](default-texture-mapping.md)<br/>                                   | <span data-ttu-id="7d49b-113">Die Verwendung der standardtextur Zuordnung reduziert das Kopieren und die Arbeitsspeicher Auslastung bei der Freigabe von Bilddaten zwischen GPU und CPU.</span><span class="sxs-lookup"><span data-stu-id="7d49b-113">The use of default texture mapping reduces copying and memory usage while sharing image data between the GPU and the CPU.</span></span> <span data-ttu-id="7d49b-114">Es sollte jedoch nur in bestimmten Situationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d49b-114">However, it should only be used in specific situations.</span></span> <span data-ttu-id="7d49b-115">Das standardmäßige Swizzle-Layout vermeidet das Kopieren oder Schwenken von Daten in mehreren Layouts.</span><span class="sxs-lookup"><span data-stu-id="7d49b-115">The standard swizzle layout avoids copying or swizzling data in multiple layouts.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="7d49b-116">Reihen folgen Ansichten für Rasterizer</span><span class="sxs-lookup"><span data-stu-id="7d49b-116">Rasterizer Order Views</span></span>](rasterizer-order-views.md)<br/>                                     | <span data-ttu-id="7d49b-117">Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.</span><span class="sxs-lookup"><span data-stu-id="7d49b-117">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="7d49b-118">Dadurch können OIT-Algorithmen (Order Independent Transparenz) funktionieren, die deutlich bessere renderingergebnisse bieten, wenn mehrere transparente Objekte in einer Ansicht aufeinander zueinander stehen.</span><span class="sxs-lookup"><span data-stu-id="7d49b-118">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span> <br/> |
| [<span data-ttu-id="7d49b-119">Von Shader festgelegter Schablonenreferenzwert</span><span class="sxs-lookup"><span data-stu-id="7d49b-119">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)<br/> | <span data-ttu-id="7d49b-120">Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.</span><span class="sxs-lookup"><span data-stu-id="7d49b-120">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="7d49b-121">Typisierte nicht geordnete zugriffsansichts Ladungen</span><span class="sxs-lookup"><span data-stu-id="7d49b-121">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)<br/>               | <span data-ttu-id="7d49b-122">Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .</span><span class="sxs-lookup"><span data-stu-id="7d49b-122">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7d49b-123">Einheitliche Speicherarchitektur</span><span class="sxs-lookup"><span data-stu-id="7d49b-123">Unified Memory Architecture</span></span>](unified-memory-architecture.md)<br/>                           | <span data-ttu-id="7d49b-124">Die Abfrage, ob eine einheitliche Speicherarchitektur (UMA) unterstützt wird, kann Ihnen dabei helfen zu bestimmen, wie einige Ressourcen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7d49b-124">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7d49b-125">Menge gekachelter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7d49b-125">Volume Tiled Resources</span></span>](volume-tiled-resources.md)<br/>                                     | <span data-ttu-id="7d49b-126">Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.</span><span class="sxs-lookup"><span data-stu-id="7d49b-126">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="7d49b-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d49b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d49b-128">Neuerungen in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7d49b-128">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





