---
title: Gekachelte Ressourcen (Direct3D 12)
description: Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42679155bbd8dc2cec560d2724e430c860f54bc0
ms.sourcegitcommit: 05e7efd3d8de6926d08802669f37e825a2fa2f46
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2020
ms.locfileid: "104548648"
---
# <a name="volume-tiled-resources-direct3d-12"></a><span data-ttu-id="03c46-103">Gekachelte Ressourcen (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="03c46-103">Volume tiled resources (Direct3D 12)</span></span>

<span data-ttu-id="03c46-104">Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.</span><span class="sxs-lookup"><span data-stu-id="03c46-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="03c46-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="03c46-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="03c46-106">Ressourcen-APIs mit Kachel</span><span class="sxs-lookup"><span data-stu-id="03c46-106">Tiled Resource APIs</span></span>](#tiled-resource-apis)
-   [<span data-ttu-id="03c46-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="03c46-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="03c46-108">Überblick</span><span class="sxs-lookup"><span data-stu-id="03c46-108">Overview</span></span>

<span data-ttu-id="03c46-109">Gekachelte Ressourcen entkoppeln ein D3D-Ressourcen Objekt von seinem Unterstützungs Speicher (die Ressourcen in der Vergangenheit verfügten über eine 1:1-Beziehung mit Ihrem Sicherungs Speicher).</span><span class="sxs-lookup"><span data-stu-id="03c46-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="03c46-110">Dies ermöglicht eine Vielzahl interessanter Szenarien, z. b. das Streaming in Textur Daten und die Wiederverwendung oder Reduzierung der Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="03c46-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage.</span></span>

<span data-ttu-id="03c46-111">2D-Textur-Kachel Ressourcen werden in D3D 11.2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03c46-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="03c46-112">Optionale Unterstützung für 3D-Kacheln mit Kacheln ist für D3D12 und D3D 11.3 verfügbar (siehe [**D3D12- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span><span class="sxs-lookup"><span data-stu-id="03c46-112">Optional support for 3D tiled textures is available for D3D12 and D3D11.3 (refer to [**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span></span>

<span data-ttu-id="03c46-113">Die typischen Ressourcen Dimensionen, die beim tichen verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.</span><span class="sxs-lookup"><span data-stu-id="03c46-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="03c46-114">Bits/Pixel (1 Stichprobe/Pixel)</span><span class="sxs-lookup"><span data-stu-id="03c46-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="03c46-115">Kachel Dimensionen (Pixel, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="03c46-115">Tile dimensions (pixels, w x h x d)</span></span> |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="03c46-116">8</span><span class="sxs-lookup"><span data-stu-id="03c46-116">8</span></span>                           | <span data-ttu-id="03c46-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="03c46-117">64x32x32</span></span>                            |
| <span data-ttu-id="03c46-118">16</span><span class="sxs-lookup"><span data-stu-id="03c46-118">16</span></span>                          | <span data-ttu-id="03c46-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="03c46-119">32x32x32</span></span>                            |
| <span data-ttu-id="03c46-120">32</span><span class="sxs-lookup"><span data-stu-id="03c46-120">32</span></span>                          | <span data-ttu-id="03c46-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="03c46-121">32x32x16</span></span>                            |
| <span data-ttu-id="03c46-122">64</span><span class="sxs-lookup"><span data-stu-id="03c46-122">64</span></span>                          | <span data-ttu-id="03c46-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="03c46-123">32x16x16</span></span>                            |
| <span data-ttu-id="03c46-124">128</span><span class="sxs-lookup"><span data-stu-id="03c46-124">128</span></span>                         | <span data-ttu-id="03c46-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="03c46-125">16x16x16</span></span>                            |
| <span data-ttu-id="03c46-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="03c46-126">BC 1,4</span></span>                      | <span data-ttu-id="03c46-127">128 x 64x16</span><span class="sxs-lookup"><span data-stu-id="03c46-127">128x64x16</span></span>                           |
| <span data-ttu-id="03c46-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="03c46-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="03c46-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="03c46-129">64x64x16</span></span>                            |

<span data-ttu-id="03c46-130">Beachten Sie, dass die folgenden Formate für die gekachelten Ressourcen nicht unterstützt werden: 96bpp-Formate, Videoformate, R1 \_ unorm, R8G8 \_ B8G8 \_ unorm, R8R8 \_ G8B8 \_ unorm.</span><span class="sxs-lookup"><span data-stu-id="03c46-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="03c46-131">In den Diagrammen unten steht dunkelgrau für NULL-Kacheln.</span><span class="sxs-lookup"><span data-stu-id="03c46-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="03c46-132">Standard Zuordnung für textur 3D-Kacheln (ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="03c46-133">Standard Zuordnung für textur 3D-Kacheln (zweit ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="03c46-134">Textur 3D-Kachel Ressource (ausführlichste MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="03c46-135">Textur 3D-Kachel Ressource (zweites detaillierteres MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="03c46-136">Textur 3D-Kachel Ressource (einzelne Kachel)</span><span class="sxs-lookup"><span data-stu-id="03c46-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="03c46-137">Textur 3D-Kachel (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="03c46-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="03c46-138">Standard Zuordnung für textur 3D-Kacheln (ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![Standard Zuordnung einer gekachelten 3 dimensionalen Ressource](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="03c46-140">Standard Zuordnung für textur 3D-Kacheln (zweit ausführlichere MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![zeigt das zweit ausführlichste MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="03c46-142">Textur 3D-Kachel Ressource (ausführlichste MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="03c46-143">Mit dem folgenden Code wird eine 3D-Kachel Ressource in der detaillierteren MIP-Datei eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="03c46-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![ausführlichste MIP für eine dreidimensionale Textur](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="03c46-145">Textur 3D-Kachel Ressource (zweites detaillierteres MIP)</span><span class="sxs-lookup"><span data-stu-id="03c46-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="03c46-146">Der folgende Code richtet eine gekachelte 3D-Ressource und die zweit ausführlichste MIP-Datei ein:</span><span class="sxs-lookup"><span data-stu-id="03c46-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![zweites detaillierteres MIP für eine dreidimensionale Textur](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="03c46-148">Textur 3D-Kachel Ressource (einzelne Kachel)</span><span class="sxs-lookup"><span data-stu-id="03c46-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="03c46-149">Der folgende Code richtet eine einzelne Kachel Ressource ein:</span><span class="sxs-lookup"><span data-stu-id="03c46-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![eine einzelne gekachelte dreidimensionale Ressource](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="03c46-151">Textur 3D-Kachel (Uniform Box)</span><span class="sxs-lookup"><span data-stu-id="03c46-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="03c46-152">Der folgende Code richtet eine einheitliche Box-Kachel Ressource ein (Beachten Sie die-Anweisung. `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="03c46-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![ein einheitliches Feld](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a><span data-ttu-id="03c46-154">Ressourcen-APIs mit Kachel</span><span class="sxs-lookup"><span data-stu-id="03c46-154">Tiled Resource APIs</span></span>

<span data-ttu-id="03c46-155">Die gleichen API-Aufrufe werden sowohl für 2D-als auch für 3D-Kachel Ressourcen verwendet:</span><span class="sxs-lookup"><span data-stu-id="03c46-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="03c46-156">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="03c46-156">Enums</span></span>

-   <span data-ttu-id="03c46-157">[**D3D12 \_ Kachel mit Kachel \_ Ressourcen \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : bestimmt die Ebene der Unterstützung für gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="03c46-157">[**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="03c46-158">[**D3D12 \_ Format \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : wird zum Testen der Unterstützung für gekachelte Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="03c46-158">[**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="03c46-159">[**D3D12 \_ Multisample \_ - \_ \_ qualitätsebenenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : bestimmt die Unterstützung von untergeordneten Ressourcen in einer Ressource mit mehreren Stichproben</span><span class="sxs-lookup"><span data-stu-id="03c46-159">[**D3D12\_MULTISAMPLE\_QUALITY\_LEVEL\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="03c46-160">[**D3D12 \_ \_Kachelkopierflags \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : enthält Flags zum Kopieren in und aus gekachelten Ressourcen und linearen Puffern.</span><span class="sxs-lookup"><span data-stu-id="03c46-160">[**D3D12\_TILE\_COPY\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="03c46-161">Strukturen</span><span class="sxs-lookup"><span data-stu-id="03c46-161">Structs</span></span>

-   <span data-ttu-id="03c46-162">[**D3D12 \_ Gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : enthält die x-, y-und z-Koordinaten und den untergeordneten Quell Verweis.</span><span class="sxs-lookup"><span data-stu-id="03c46-162">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="03c46-163">Beachten Sie, dass es eine hilfsstruktur gibt: [**CD3DX12 \_ Kachel \_ Ressourcen \_ Koordinate**](cd3dx12-tiled-resource-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="03c46-163">Note there is a helper structure: [**CD3DX12\_TILED\_RESOURCE\_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).</span></span>
-   <span data-ttu-id="03c46-164">[**D3D12 \_ Kachel \_ Regions \_ Größe**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : gibt die Größe und die Anzahl der Kacheln des gekachelten Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="03c46-164">[**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="03c46-165">[**D3D12 \_ Kachel \_ Form**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : die Kachel Form als Breite, Höhe und Tiefe in texeln.</span><span class="sxs-lookup"><span data-stu-id="03c46-165">[**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="03c46-166">[**D3D12 \_ Feature \_ Data \_ D3D12 \_ Optionen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : enthält die unterstützte Kachel Ressourcenebene und einen booleschen Wert ( *volumetiledresourcessupported*), der angibt, ob volumenkachel-Ressourcen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="03c46-166">[**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : holds the supported tile resource tier level and a boolean, *VolumeTiledResourcesSupported*, indicated whether volume tiled resources are supported.</span></span>

<span data-ttu-id="03c46-167">Methoden</span><span class="sxs-lookup"><span data-stu-id="03c46-167">Methods</span></span>

-   <span data-ttu-id="03c46-168">[**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : wird verwendet, um zu bestimmen, welche Features und auf welcher Ebene von der aktuellen Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="03c46-168">[**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="03c46-169">[**ID3D12GraphcisCommandList:: copytiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : kopiert Kacheln aus dem Puffer in eine gekachelte Ressource oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="03c46-169">[**ID3D12GraphcisCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="03c46-170">[**ID3D12CommandQueue:: updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : aktualisiert Zuordnungen von Kachel Positionen in gekachelten Ressourcen zu Speicherorten in einem Ressourcenheap.</span><span class="sxs-lookup"><span data-stu-id="03c46-170">[**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a resource heap.</span></span>
-   <span data-ttu-id="03c46-171">[**ID3D12CommandQueue:: copytilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : kopiert Zuordnungen aus einer Ressource mit Kachel Kachel in eine gekachelte Ziel Ressource.</span><span class="sxs-lookup"><span data-stu-id="03c46-171">[**ID3D12CommandQueue::CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="03c46-172">[**ID3D12Device:: getresourcetielt**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="03c46-172">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03c46-173">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="03c46-173">Related topics</span></span>
* [<span data-ttu-id="03c46-174">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="03c46-174">Resource Binding</span></span>](resource-binding.md)
