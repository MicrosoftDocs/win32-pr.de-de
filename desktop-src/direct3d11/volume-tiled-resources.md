---
title: Gekachelte Ressourcen (Direct3D 11)
description: Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb8b35e522ef3298abad1322d6fb7a2fe65bfcf
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "103719283"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="55be8-103">Menge gekachelter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="55be8-103">Volume Tiled Resources</span></span>

<span data-ttu-id="55be8-104">Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.</span><span class="sxs-lookup"><span data-stu-id="55be8-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="55be8-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="55be8-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="55be8-106">D3D 11.3 gekachelte Ressourcen-APIs</span><span class="sxs-lookup"><span data-stu-id="55be8-106">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="55be8-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55be8-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="55be8-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="55be8-108">Overview</span></span>

<span data-ttu-id="55be8-109">Gekachelte Ressourcen entkoppeln ein D3D-Ressourcen Objekt von seinem Unterstützungs Speicher (die Ressourcen in der Vergangenheit verfügten über eine 1:1-Beziehung mit Ihrem Sicherungs Speicher).</span><span class="sxs-lookup"><span data-stu-id="55be8-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="55be8-110">Dies ermöglicht eine Vielzahl interessanter Szenarien, z. b. das Streaming in Textur Daten und die Wiederverwendung oder Reduzierung der Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="55be8-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="55be8-111">2D-Textur-Kachel Ressourcen werden in D3D 11.2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55be8-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="55be8-112">D3D12 und D3D 11.3 fügen Unterstützung für 3D-Kacheln hinzu.</span><span class="sxs-lookup"><span data-stu-id="55be8-112">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="55be8-113">Die typischen Ressourcen Dimensionen, die beim tichen verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.</span><span class="sxs-lookup"><span data-stu-id="55be8-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



|                             |                                     |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="55be8-114">Bits/Pixel (1 Stichprobe/Pixel)</span><span class="sxs-lookup"><span data-stu-id="55be8-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="55be8-115">Kachel Dimensionen (Pixel, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="55be8-115">Tile dimensions (pixels, w x h x d)</span></span> |
| <span data-ttu-id="55be8-116">8</span><span class="sxs-lookup"><span data-stu-id="55be8-116">8</span></span>                           | <span data-ttu-id="55be8-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="55be8-117">64x32x32</span></span>                            |
| <span data-ttu-id="55be8-118">16</span><span class="sxs-lookup"><span data-stu-id="55be8-118">16</span></span>                          | <span data-ttu-id="55be8-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="55be8-119">32x32x32</span></span>                            |
| <span data-ttu-id="55be8-120">32</span><span class="sxs-lookup"><span data-stu-id="55be8-120">32</span></span>                          | <span data-ttu-id="55be8-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="55be8-121">32x32x16</span></span>                            |
| <span data-ttu-id="55be8-122">64</span><span class="sxs-lookup"><span data-stu-id="55be8-122">64</span></span>                          | <span data-ttu-id="55be8-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="55be8-123">32x16x16</span></span>                            |
| <span data-ttu-id="55be8-124">128</span><span class="sxs-lookup"><span data-stu-id="55be8-124">128</span></span>                         | <span data-ttu-id="55be8-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="55be8-125">16x16x16</span></span>                            |
| <span data-ttu-id="55be8-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="55be8-126">BC 1,4</span></span>                      | <span data-ttu-id="55be8-127">128 x 64x16</span><span class="sxs-lookup"><span data-stu-id="55be8-127">128x64x16</span></span>                           |
| <span data-ttu-id="55be8-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="55be8-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="55be8-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="55be8-129">64x64x16</span></span>                            |



 

<span data-ttu-id="55be8-130">Beachten Sie, dass die folgenden Formate für die gekachelten Ressourcen nicht unterstützt werden: 96bpp-Formate, Videoformate, R1 \_ unorm, R8G8 \_ B8G8 \_ unorm, R8R8 \_ G8B8 \_ unorm.</span><span class="sxs-lookup"><span data-stu-id="55be8-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="55be8-131">In den Diagrammen unten steht dunkelgrau für NULL-Kacheln.</span><span class="sxs-lookup"><span data-stu-id="55be8-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="55be8-132">Standard Zuordnung für textur 3D-Kacheln (ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="55be8-133">Standard Zuordnung für textur 3D-Kacheln (zweit ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="55be8-134">Textur 3D-Kachel Ressource (ausführlichste MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="55be8-135">Textur 3D-Kachel Ressource (zweites detaillierteres MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="55be8-136">Textur 3D-Kachel Ressource (einzelne Kachel)</span><span class="sxs-lookup"><span data-stu-id="55be8-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="55be8-137">Textur 3D-Kachel (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="55be8-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="55be8-138">Standard Zuordnung für textur 3D-Kacheln (ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![Standard Zuordnung der detaillierteren MIP-](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="55be8-140">Standard Zuordnung für textur 3D-Kacheln (zweit ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![Standard Zuordnung der zweit detailliertesten MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="55be8-142">Textur 3D-Kachel Ressource (ausführlichste MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="55be8-143">Mit dem folgenden Code wird eine 3D-Kachel Ressource in der detaillierteren MIP-Datei eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="55be8-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![die ausführlichste Zuordnung einer 3D--Kachel Ressource](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="55be8-145">Textur 3D-Kachel Ressource (zweites detaillierteres MIP)</span><span class="sxs-lookup"><span data-stu-id="55be8-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="55be8-146">Der folgende Code richtet eine gekachelte 3D-Ressource und die zweit ausführlichste MIP-Datei ein:</span><span class="sxs-lookup"><span data-stu-id="55be8-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![zweit ausführlichste Zuordnung einer 3D--Kachel Ressource](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="55be8-148">Textur 3D-Kachel Ressource (einzelne Kachel)</span><span class="sxs-lookup"><span data-stu-id="55be8-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="55be8-149">Der folgende Code richtet eine einzelne Kachel Ressource ein:</span><span class="sxs-lookup"><span data-stu-id="55be8-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![eine einzelne Kachel](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="55be8-151">Textur 3D-Kachel (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="55be8-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="55be8-152">Der folgende Code richtet eine einheitliche Box-Kachel Ressource ein (Beachten Sie die-Anweisung. `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="55be8-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![ein einheitliches Feld](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="55be8-154">D3D 11.3 gekachelte Ressourcen-APIs</span><span class="sxs-lookup"><span data-stu-id="55be8-154">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="55be8-155">Die gleichen API-Aufrufe werden sowohl für 2D-als auch für 3D-Kachel Ressourcen verwendet:</span><span class="sxs-lookup"><span data-stu-id="55be8-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="55be8-156">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="55be8-156">Enums</span></span>

-   <span data-ttu-id="55be8-157">[**D3D11 \_ Kachel mit Kachel \_ Ressourcen \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : bestimmt die Ebene der Unterstützung für gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="55be8-157">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="55be8-158">[**D3D11 \_ Format \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : wird zum Testen der Unterstützung für gekachelte Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="55be8-158">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="55be8-159">[**D3D11 \_ Überprüfen der \_ Multisample \_ Quality \_ Levels- \_ Flag**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : bestimmt die Unterstützung von unterstützten Ressourcen in einer Multisampling-Ressource.</span><span class="sxs-lookup"><span data-stu-id="55be8-159">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="55be8-160">[**D3D11 \_ \_Kachelkopierflags \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : enthält Flags zum Kopieren in und aus gekachelten Ressourcen und linearen Puffern.</span><span class="sxs-lookup"><span data-stu-id="55be8-160">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="55be8-161">Strukturen</span><span class="sxs-lookup"><span data-stu-id="55be8-161">Structures</span></span>

-   <span data-ttu-id="55be8-162">[**D3D11 \_ Gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : enthält die x-, y-und z-Koordinaten und den untergeordneten Quell Verweis.</span><span class="sxs-lookup"><span data-stu-id="55be8-162">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="55be8-163">Beachten Sie, dass es eine Hilfsklasse gibt: CD3D11 \_ Kachel \_ Ressourcen \_ Koordinate.</span><span class="sxs-lookup"><span data-stu-id="55be8-163">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="55be8-164">[**D3D11 \_ Kachel \_ Regions \_ Größe**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : gibt die Größe und die Anzahl der Kacheln des gekachelten Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="55be8-164">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="55be8-165">[**D3D11 \_ Kachel \_ Form**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : die Kachel Form als Breite, Höhe und Tiefe in texeln.</span><span class="sxs-lookup"><span data-stu-id="55be8-165">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="55be8-166">[**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): enthält die unterstützte Kachel Ressourcenebene.</span><span class="sxs-lookup"><span data-stu-id="55be8-166">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="55be8-167">Methoden</span><span class="sxs-lookup"><span data-stu-id="55be8-167">Methods</span></span>

-   <span data-ttu-id="55be8-168">[**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : wird verwendet, um zu bestimmen, welche Features und auf welcher Ebene von der aktuellen Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="55be8-168">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="55be8-169">[**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : kopiert Kacheln aus dem Puffer in eine gekachelte Ressource oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="55be8-169">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="55be8-170">[**ID3D11DeviceContext2:: updatetilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : aktualisiert Zuordnungen von Kachel Positionen in gekachelten Ressourcen zu Speicherorten in einem Kachel Pool.</span><span class="sxs-lookup"><span data-stu-id="55be8-170">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="55be8-171">[**ID3D11DeviceContext2:: copytilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : kopiert Zuordnungen aus einer Ressource mit Kachel Kachel in eine gekachelte Ziel Ressource.</span><span class="sxs-lookup"><span data-stu-id="55be8-171">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="55be8-172">[**ID3D11DeviceContext2:: getresourcetielt**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="55be8-172">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55be8-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55be8-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55be8-174">Direct3D 11,3-Features</span><span class="sxs-lookup"><span data-stu-id="55be8-174">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




