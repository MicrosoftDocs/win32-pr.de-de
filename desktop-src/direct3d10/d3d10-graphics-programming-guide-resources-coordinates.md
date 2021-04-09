---
description: Koordinatensysteme für Direct3D 10 sind für Pixel und Texels definiert.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Koordinatensysteme (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748969"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="15e6f-103">Koordinatensysteme (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="15e6f-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="15e6f-104">Koordinatensysteme für Direct3D 10 sind für Pixel und Texels definiert.</span><span class="sxs-lookup"><span data-stu-id="15e6f-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e6f-105">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="15e6f-105">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="15e6f-106">Direct3D 10 definiert die linke obere Ecke des linken oberen Pixels als Ursprung eines Renderziels.</span><span class="sxs-lookup"><span data-stu-id="15e6f-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span><br/> <span data-ttu-id="15e6f-107">Direct3D 9 definiert den Mittelpunkt des linken oberen Pixels als Ursprung eines Renderziels.</span><span class="sxs-lookup"><span data-stu-id="15e6f-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span><br/> |



 

-   [<span data-ttu-id="15e6f-108">Pixel Koordinaten System</span><span class="sxs-lookup"><span data-stu-id="15e6f-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
    -   [<span data-ttu-id="15e6f-109">Pixel Koordinaten System für Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="15e6f-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)
-   [<span data-ttu-id="15e6f-110">Texel-Koordinaten System</span><span class="sxs-lookup"><span data-stu-id="15e6f-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
    -   [<span data-ttu-id="15e6f-111">Texel-Koordinaten System</span><span class="sxs-lookup"><span data-stu-id="15e6f-111">Texel Coordinate System</span></span>](#texel-coordinate-system)
-   [<span data-ttu-id="15e6f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15e6f-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="15e6f-113">Pixel Koordinaten System</span><span class="sxs-lookup"><span data-stu-id="15e6f-113">Pixel Coordinate System</span></span>

<span data-ttu-id="15e6f-114">Das Pixelkoordinaten System in Direct3D 10 definiert den Ursprung eines Renderziels in der linken oberen Ecke.</span><span class="sxs-lookup"><span data-stu-id="15e6f-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="15e6f-115">wie im folgenden Diagramm gezeigt.</span><span class="sxs-lookup"><span data-stu-id="15e6f-115">as shown in the following diagram.</span></span> <span data-ttu-id="15e6f-116">Pixel Center werden von ganzzahligen Speicherorten um (0,5 f, 0,5 f) versetzt.</span><span class="sxs-lookup"><span data-stu-id="15e6f-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![Diagramm des Pixelkoordinaten Systems in Direct3D 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="15e6f-118">Pixel Koordinaten System für Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="15e6f-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="15e6f-119">Im folgenden finden Sie das Pixelkoordinaten System für Direct3D 9, das den Ursprung oder ein Renderziel als Mittelpunkt des linken oberen Pixels (0,5, 0,5) von der linken oberen Ecke definiert, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="15e6f-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="15e6f-120">In Direct3D 9 befinden sich Pixel Center an ganzzahligen Positionen.</span><span class="sxs-lookup"><span data-stu-id="15e6f-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![Diagramm des Pixelkoordinaten Systems in Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="15e6f-122">Texel-Koordinaten System</span><span class="sxs-lookup"><span data-stu-id="15e6f-122">Texel Coordinate System</span></span>

<span data-ttu-id="15e6f-123">Das Texel-Koordinatensystem hat seinen Ursprung in der oberen linken Ecke der Textur, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="15e6f-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="15e6f-124">Dies macht das Rendern von Bildschirm Ausrichtung (in Direct3D 10) trivial, da das Pixelkoordinaten System am texelkoordinaten System ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="15e6f-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![Diagramm des Texel-Koordinatensystems](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="15e6f-126">Texel-Koordinaten System</span><span class="sxs-lookup"><span data-stu-id="15e6f-126">Texel Coordinate System</span></span>

<span data-ttu-id="15e6f-127">Texturkoordinaten werden entweder durch eine normalisierte oder eine skalierte Zahl dargestellt. Jede Textur Koordinate wird wie folgt einem bestimmten Textem zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="15e6f-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="15e6f-128">Für eine normalisierte Koordinate:</span><span class="sxs-lookup"><span data-stu-id="15e6f-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="15e6f-129">Punkt Stichproben: Texel \# = Floor (U \* Width)</span><span class="sxs-lookup"><span data-stu-id="15e6f-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="15e6f-130">Lineare Stichprobenentnahme: Left Texel \# = Floor (U \* Width), Right Texel \# = left Texel \# + 1</span><span class="sxs-lookup"><span data-stu-id="15e6f-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="15e6f-131">Für eine skalierte Koordinate:</span><span class="sxs-lookup"><span data-stu-id="15e6f-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="15e6f-132">Punkt Stichproben: Texel \# = Floor (U)</span><span class="sxs-lookup"><span data-stu-id="15e6f-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="15e6f-133">Lineare Stichprobenentnahme: Left Texel \# = Floor (U-0,5), Right Texel \# = left Texel \# + 1</span><span class="sxs-lookup"><span data-stu-id="15e6f-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="15e6f-134">Dabei ist die Breite die Breite der Textur (in Texels).</span><span class="sxs-lookup"><span data-stu-id="15e6f-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="15e6f-135">Das Umwickeln von Textur Adressen tritt auf, nachdem der textsort berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="15e6f-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15e6f-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15e6f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15e6f-137">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="15e6f-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




