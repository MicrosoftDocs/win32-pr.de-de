---
title: Volumekachelressourcen (Direct3D 11-Grafiken)
description: Erfahren Sie, wie Volumentexturen (3D) als gekachelte Ressourcen verwendet werden können. Beachten Sie, dass die Kachelauflösung dreidimensional ist.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf9b3ed8b1db89d9718fa904eefd23ce2e871db
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335434"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="3572e-104">Menge gekachelter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3572e-104">Volume Tiled Resources</span></span>

<span data-ttu-id="3572e-105">Volumentexturen (3D) können als kachelbasierte Ressourcen verwendet werden. Dabei wird darauf hinzuweisen, dass die Kachelauflösung dreidimensional ist.</span><span class="sxs-lookup"><span data-stu-id="3572e-105">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="3572e-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="3572e-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="3572e-107">D3D11.3-Ressourcen-APIs mit Kachel</span><span class="sxs-lookup"><span data-stu-id="3572e-107">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="3572e-108">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3572e-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="3572e-109">Übersicht</span><span class="sxs-lookup"><span data-stu-id="3572e-109">Overview</span></span>

<span data-ttu-id="3572e-110">Gekachelte Ressourcen entkoppeln ein D3D-Ressourcenobjekt vom Sicherungsspeicher (ressourcen in der Vergangenheit hatten eine 1:1-Beziehung mit ihrem Sicherungsspeicher).</span><span class="sxs-lookup"><span data-stu-id="3572e-110">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="3572e-111">Dies ermöglicht eine Vielzahl von interessanten Szenarien, z. B. das Streamen von Texturdaten und das Wiederverwenden oder Reduzieren der Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="3572e-111">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="3572e-112">2D-Texturkachelressourcen werden in D3D11.2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3572e-112">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="3572e-113">D3D12 und D3D11.3 fügen Unterstützung für 3D-Kacheltexturen hinzu.</span><span class="sxs-lookup"><span data-stu-id="3572e-113">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="3572e-114">Die typischen Ressourcendimensionen, die beim Kacheln verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.</span><span class="sxs-lookup"><span data-stu-id="3572e-114">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="3572e-115">Bits/Pixel (1 Stichprobe/Pixel)</span><span class="sxs-lookup"><span data-stu-id="3572e-115">Bits/pixel (1 sample/pixel)</span></span>                            | <span data-ttu-id="3572e-116">Kacheldimensionen (Pixel, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="3572e-116">Tile dimensions (pixels, w x h x d)</span></span>                                    |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="3572e-117">8</span><span class="sxs-lookup"><span data-stu-id="3572e-117">8</span></span>                           | <span data-ttu-id="3572e-118">64 x 32 x 32</span><span class="sxs-lookup"><span data-stu-id="3572e-118">64x32x32</span></span>                            |
| <span data-ttu-id="3572e-119">16</span><span class="sxs-lookup"><span data-stu-id="3572e-119">16</span></span>                          | <span data-ttu-id="3572e-120">32x32x32</span><span class="sxs-lookup"><span data-stu-id="3572e-120">32x32x32</span></span>                            |
| <span data-ttu-id="3572e-121">32</span><span class="sxs-lookup"><span data-stu-id="3572e-121">32</span></span>                          | <span data-ttu-id="3572e-122">32x32x16</span><span class="sxs-lookup"><span data-stu-id="3572e-122">32x32x16</span></span>                            |
| <span data-ttu-id="3572e-123">64</span><span class="sxs-lookup"><span data-stu-id="3572e-123">64</span></span>                          | <span data-ttu-id="3572e-124">32x16x16</span><span class="sxs-lookup"><span data-stu-id="3572e-124">32x16x16</span></span>                            |
| <span data-ttu-id="3572e-125">128</span><span class="sxs-lookup"><span data-stu-id="3572e-125">128</span></span>                         | <span data-ttu-id="3572e-126">16x16x16</span><span class="sxs-lookup"><span data-stu-id="3572e-126">16x16x16</span></span>                            |
| <span data-ttu-id="3572e-127">BC 1,4</span><span class="sxs-lookup"><span data-stu-id="3572e-127">BC 1,4</span></span>                      | <span data-ttu-id="3572e-128">128 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="3572e-128">128x64x16</span></span>                           |
| <span data-ttu-id="3572e-129">BC 2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="3572e-129">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="3572e-130">64 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="3572e-130">64x64x16</span></span>                            |



 

<span data-ttu-id="3572e-131">Beachten Sie, dass die folgenden Formate bei gekachelten Ressourcen nicht unterstützt werden: 96bpp-Formate, Videoformate, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="3572e-131">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="3572e-132">In den folgenden Diagrammen stellt dunkelgrau NULL-Kacheln dar.</span><span class="sxs-lookup"><span data-stu-id="3572e-132">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="3572e-133">Standardzuordnung der texturierten 3D-Kachelressource (am ausführlichsten)</span><span class="sxs-lookup"><span data-stu-id="3572e-133">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="3572e-134">Standardzuordnung der texturierten 3D-Kachelressource (zweit ausführlichste mip)</span><span class="sxs-lookup"><span data-stu-id="3572e-134">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="3572e-135">Textur-3D-Kachelressource (ausführlichste mip)</span><span class="sxs-lookup"><span data-stu-id="3572e-135">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="3572e-136">Textur-3D-Kachelressource (zweit ausführlichste mip)</span><span class="sxs-lookup"><span data-stu-id="3572e-136">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="3572e-137">Textur-3D-Kachelressource (einzelne Kachel)</span><span class="sxs-lookup"><span data-stu-id="3572e-137">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="3572e-138">Textur-3D-Kachelressource (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="3572e-138">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="3572e-139">Standardzuordnung der texturierten 3D-Kachelressource (am ausführlichsten)</span><span class="sxs-lookup"><span data-stu-id="3572e-139">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![Standardzuordnung des ausführlichsten MIP](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="3572e-141">Standardzuordnung der texturierten 3D-Kachelressource (zweit ausführlichste mip)</span><span class="sxs-lookup"><span data-stu-id="3572e-141">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![Standardzuordnung des zweit ausführlichsten MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="3572e-143">Textur-3D-Kachelressource (ausführlichste mip)</span><span class="sxs-lookup"><span data-stu-id="3572e-143">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="3572e-144">Mit dem folgenden Code wird eine gekachelte 3D-Ressource mit dem ausführlichsten MIP eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3572e-144">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

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

![Detailliertere Zuordnung einer gekachelten 3D-Ressource](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="3572e-146">Textur-3D-Kachelressource (zweit ausführlichste mip)</span><span class="sxs-lookup"><span data-stu-id="3572e-146">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="3572e-147">Der folgende Code richtet eine gekachelte 3D-Ressource und den zweit ausführlichsten MIP ein:</span><span class="sxs-lookup"><span data-stu-id="3572e-147">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

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

![Zweit ausführlichste Zuordnung einer 3D-Kachelressource](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="3572e-149">Textur-3D-Kachelressource (einzelne Kachel)</span><span class="sxs-lookup"><span data-stu-id="3572e-149">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="3572e-150">Mit dem folgenden Code wird eine Einzelkachelressource eingerichtet:</span><span class="sxs-lookup"><span data-stu-id="3572e-150">The following code sets up a Single Tile resource:</span></span>

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

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="3572e-152">Textur-3D-Kachelressource (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="3572e-152">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="3572e-153">Der folgende Code richtet eine uniform Box-Kachelressource ein (beachten Sie die -Anweisung. `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="3572e-153">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

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

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="3572e-155">D3D11.3-Ressourcen-APIs mit Kachel</span><span class="sxs-lookup"><span data-stu-id="3572e-155">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="3572e-156">Die gleichen API-Aufrufe werden sowohl für 2D- als auch für 3D-kachelte Ressourcen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3572e-156">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="3572e-157">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="3572e-157">Enums</span></span>

-   <span data-ttu-id="3572e-158">[**D3D11 \_ TILED \_ RESOURCES \_ TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : Bestimmt die Ebene der Unterstützung für gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3572e-158">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="3572e-159">[**D3D11 \_ FORMAT \_ SUPPORT2:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) Wird verwendet, um die Unterstützung für gekachelte Ressourcen zu testen.</span><span class="sxs-lookup"><span data-stu-id="3572e-159">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="3572e-160">[**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY LEVELS \_ \_ FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : Bestimmt die Unterstützung von kachelbasierten Ressourcen in einer Ressource mit mehreren Stichproben.</span><span class="sxs-lookup"><span data-stu-id="3572e-160">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="3572e-161">[**D3D11 \_ TILE \_ COPY \_ FLAGS:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) Enthält Flags zum Kopieren in und aus gekachelten Ressourcen und linearen Puffern.</span><span class="sxs-lookup"><span data-stu-id="3572e-161">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="3572e-162">Strukturen</span><span class="sxs-lookup"><span data-stu-id="3572e-162">Structures</span></span>

-   <span data-ttu-id="3572e-163">[**D3D11 \_ TILED \_ RESOURCE \_ COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : enthält die x-, y- und z-Koordinate sowie den Unterressourcenverweis.</span><span class="sxs-lookup"><span data-stu-id="3572e-163">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="3572e-164">Beachten Sie, dass eine Hilfsklasse vorhanden ist: CD3D11 \_ TILED \_ RESOURCE \_ COORDINATE.</span><span class="sxs-lookup"><span data-stu-id="3572e-164">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="3572e-165">[**D3D11 \_ TILE \_ REGION \_ SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : Gibt die Größe und Anzahl der Kacheln des gekachelten Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="3572e-165">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="3572e-166">[**D3D11 \_ TILE \_ SHAPE:**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) Die Kachelform als Breite, Höhe und Tiefe in Texel.</span><span class="sxs-lookup"><span data-stu-id="3572e-166">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="3572e-167">[**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): enthält die unterstützte Ebene der Kachelressourcenebene.</span><span class="sxs-lookup"><span data-stu-id="3572e-167">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="3572e-168">Methoden</span><span class="sxs-lookup"><span data-stu-id="3572e-168">Methods</span></span>

-   <span data-ttu-id="3572e-169">[**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) Wird verwendet, um zu bestimmen, welche Features und auf welchem Tarif von der aktuellen Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3572e-169">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="3572e-170">[**ID3D11DeviceContext2::CopyTiles:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) Kopiert Kacheln aus dem Puffer in eine gekachelte Ressource oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="3572e-170">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="3572e-171">[**ID3D11DeviceContext2::UpdateTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) aktualisiert Zuordnungen von Kachelspeicherorten in gekachelten Ressourcen zu Arbeitsspeicherspeicherorten in einem Kachelpool.</span><span class="sxs-lookup"><span data-stu-id="3572e-171">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="3572e-172">[**ID3D11DeviceContext2::CopyTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Kopiert Zuordnungen aus einer gekachelten Quellressource in eine gekachelte Zielressource.</span><span class="sxs-lookup"><span data-stu-id="3572e-172">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="3572e-173">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln zerbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="3572e-173">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3572e-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3572e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3572e-175">Direct3D 11.3-Features</span><span class="sxs-lookup"><span data-stu-id="3572e-175">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




