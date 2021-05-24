---
description: Koordinatensysteme für Direct3D 10 werden für Pixel und Texel definiert.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Koordinatensysteme (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3da846ae4b989f6d8cb4741f9df8f7228e8970
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335464"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="43c7e-103">Koordinatensysteme (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="43c7e-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="43c7e-104">Koordinatensysteme für Direct3D 10 werden für Pixel und Texel definiert.</span><span class="sxs-lookup"><span data-stu-id="43c7e-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



<span data-ttu-id="43c7e-105">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="43c7e-105">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="43c7e-106">Direct3D 10 definiert die linke obere Ecke des oberen linken Pixels als Ursprung eines Renderziels.</span><span class="sxs-lookup"><span data-stu-id="43c7e-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span>
- <span data-ttu-id="43c7e-107">Direct3D 9 definiert die Mitte des pixel oben links als Ursprung eines Renderziels.</span><span class="sxs-lookup"><span data-stu-id="43c7e-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span>



 

[<span data-ttu-id="43c7e-108">Pixelkoordinatensystem</span><span class="sxs-lookup"><span data-stu-id="43c7e-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
- [<span data-ttu-id="43c7e-109">Pixelkoordinatensystem für Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="43c7e-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)

[<span data-ttu-id="43c7e-110">Texel-Koordinatensystem</span><span class="sxs-lookup"><span data-stu-id="43c7e-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
- [<span data-ttu-id="43c7e-111">Texel-Koordinatensystem</span><span class="sxs-lookup"><span data-stu-id="43c7e-111">Texel Coordinate System</span></span>](#texel-coordinate-system)

[<span data-ttu-id="43c7e-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="43c7e-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="43c7e-113">Pixelkoordinatensystem</span><span class="sxs-lookup"><span data-stu-id="43c7e-113">Pixel Coordinate System</span></span>

<span data-ttu-id="43c7e-114">Das Pixelkoordinatensystem in Direct3D 10 definiert den Ursprung eines Renderziels in der oberen linken Ecke.</span><span class="sxs-lookup"><span data-stu-id="43c7e-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="43c7e-115">wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="43c7e-115">as shown in the following diagram.</span></span> <span data-ttu-id="43c7e-116">Pixelcenter werden von ganzzahligen Positionen um (0,5f, 0,5f) versetzt.</span><span class="sxs-lookup"><span data-stu-id="43c7e-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![Diagramm des Pixelkoordinatensystems in direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="43c7e-118">Pixelkoordinatensystem für Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="43c7e-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="43c7e-119">Als Referenz ist hier das Pixelkoordinatensystem für Direct3D 9 angegeben, das den Ursprung oder ein Renderziel als Mitte des oberen linken Pixels (0,5,0,5) von der oberen linken Ecke entfernt definiert hat, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="43c7e-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="43c7e-120">In Direct3D 9 befinden sich Pixelcenter an ganzzahligen Positionen.</span><span class="sxs-lookup"><span data-stu-id="43c7e-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![Diagramm des Pixelkoordinatensystems in direct3d 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="43c7e-122">Texelkoordinatensystem</span><span class="sxs-lookup"><span data-stu-id="43c7e-122">Texel Coordinate System</span></span>

<span data-ttu-id="43c7e-123">Das Texelkoordinatensystem hat seinen Ursprung in der oberen linken Ecke der Textur, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="43c7e-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="43c7e-124">Dies macht das Rendern bildschirmbündiger Texturen trivial (in Direct3D 10), da das Pixelkoordinatensystem am Texelkoordinatensystem ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="43c7e-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![Diagramm des Texelkoordinatensystems](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="43c7e-126">Texelkoordinatensystem</span><span class="sxs-lookup"><span data-stu-id="43c7e-126">Texel Coordinate System</span></span>

<span data-ttu-id="43c7e-127">Texturkoordinaten werden entweder mit einer normalisierten oder einer skalierten Zahl dargestellt. Jede Texturkoordinate wird einem bestimmten Texel wie folgt zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="43c7e-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="43c7e-128">Für eine normalisierte Koordinate:</span><span class="sxs-lookup"><span data-stu-id="43c7e-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="43c7e-129">Punktstichproben: Texel \# = floor(U \* Width)</span><span class="sxs-lookup"><span data-stu-id="43c7e-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="43c7e-130">Lineare Stichprobenentnahme: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel + \# 1</span><span class="sxs-lookup"><span data-stu-id="43c7e-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="43c7e-131">Für eine skalierte Koordinate:</span><span class="sxs-lookup"><span data-stu-id="43c7e-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="43c7e-132">Punktsampling: Texel \# = floor(U)</span><span class="sxs-lookup"><span data-stu-id="43c7e-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="43c7e-133">Lineare Stichprobenentnahme: Left Texel \# = floor(U - 0,5), Right Texel \# = Left Texel + \# 1</span><span class="sxs-lookup"><span data-stu-id="43c7e-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="43c7e-134">Wobei die Breite die Breite der Textur (in Texel) ist.</span><span class="sxs-lookup"><span data-stu-id="43c7e-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="43c7e-135">Die Texturadressumbruch erfolgt, nachdem die Texelposition berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="43c7e-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43c7e-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43c7e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43c7e-137">Ressourcen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="43c7e-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




