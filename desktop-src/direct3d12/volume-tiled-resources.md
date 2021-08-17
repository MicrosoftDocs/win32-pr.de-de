---
title: Gekachelte Volumeressourcen (Direct3D 12)
description: Volumetexturen (3D) können als gekachelte Ressourcen verwendet werden, und es wird darauf hingeendet, dass die Kachelauflösung dreidimensional ist.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d6e9b4d7ae9ad4b93bae5cf29749c293bf7f55ea7fa35a1e1ca71040218e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123513"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Gekachelte Volumeressourcen (Direct3D 12)

Volumetexturen (3D) können als gekachelte Ressourcen verwendet werden, und es wird darauf hingeendet, dass die Kachelauflösung dreidimensional ist.

## <a name="overview"></a>Übersicht

Gekachelte Ressourcen entkoppeln ein Direct3D-Ressourcenobjekt vom speicherunterdingenden Speicher (Ressourcen hatten in der Vergangenheit eine 1:1-Beziehung mit ihrem speicherunterdingenden Speicher). Dies ermöglicht eine Vielzahl interessanter Szenarien, z. B. das Streamen von Texturdaten und das Wiederverwendnen oder Reduzieren der Speicherauslastung.

2D-Texturkachelressourcen werden in Direct3D 11.2 unterstützt. Optionale Unterstützung für 3D-Kacheltexturen ist für Direct3D 12 und Direct3D 11.3 verfügbar (siehe [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Die typischen Ressourcendimensionen, die beim Kacheln verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.

| Bits/Pixel (1 Beispiel/Pixel) | Kacheldimensionen (Pixel, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64 x 32 x 32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128 x 64 x 16                           |
| BC 2,3,5,6,7                | 64 x 64 x 16                            |

Beachten Sie, dass die folgenden Formate bei gekachelten Ressourcen nicht unterstützt **werden:** 96bpp-Formate, Videoformate, **R1_UNORM**, **R8G8_B8G8_UNORM**, R8R8_G8B8_UNORM .

In den folgenden Diagrammen stellt dunkelgrau NULL-Kacheln dar.

* [Standardzuordnung der texturierten 3D-Kachelressource (am ausführlichsten)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Standardzuordnung der texturierten 3D-Kachelressource (zweit ausführlichste mip)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Textur-3D-Kachelressource (ausführlichste mip)](#texture-3d-tiled-resource-most-detailed-mip)
* [Textur-3D-Kachelressource (zweit ausführlichste mip)](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Textur-3D-Kachelressource (einzelne Kachel)](#texture-3d-tiled-resource-single-tile)
* [Textur 3D-Kachelressource (Uniform Box)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Standardzuordnung der kachelgekachelten Texturressource (am ausführlichsten)

![Standardzuordnung einer gekachelten dreidimensionalen Ressource](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Standardzuordnung der kachelgekachelten Texturressource (zweitreichste mip-

![zeigt den zweitreichsten MIP an.](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Kachelressource für Textur 3D (ausführlichste mip)

Der folgende Code richtet eine gekachelte 3D-Ressource mit dem ausführlichsten MIP ein.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord{};
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize{};
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![Ausführlichste mip für eine dreidimensionale Textur](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Gekachelte Texturressource mit 3D-Textur (zweitreichste mip)

Der folgende Code richtet eine gekachelte 3D-Ressource und den zweit ausführlichsten MIP ein.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![zweitreichste mip für eine dreidimensionale Textur](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Kachelressource für Textur 3D (einzelne Kachel)

Der folgende Code richtet eine einzelne Kachelressource ein.

```cpp
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

![eine einkachelte dreidimensionale Ressource](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Kachelressource für Textur 3D (einheitliches Feld)

Der folgende Code richtet eine gekachelte Uniform Box-Ressource ein (beachten Sie die -Anweisung). `trSize.bUseBox = true;) :`

```cpp
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

## <a name="tiled-resource-apis"></a>APIs für gekachelte Ressourcen

Die gleichen API-Aufrufe werden sowohl für 2D- als auch für 3D-gekachelte Ressourcen verwendet.

Enumerationen

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : Bestimmt die Ebene der Unterstützung von gekachelten Ressourcen.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : Wird verwendet, um die Unterstützung von gekachelten Ressourcen zu testen.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : Bestimmt die Unterstützung von gekachelten Ressourcen in einer Ressource mit mehreren Stichproben.
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : enthält Flags für das Kopieren in und aus geschwenkten kachelierten Ressourcen und linearen Puffern.

Strukturen

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : enthält den x-, y- und z-Koordinaten- und Unterressourcenverweis. Beachten Sie, dass es eine Hilfsstruktur gibt: [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : Gibt die Größe und Anzahl der Kacheln des gekachelten Bereich an.
* [**D3D12_TILE_SHAPE:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) Die Kachelform als Breite, Höhe und Tiefe in Texeln.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : enthält die unterstützte Kachelressourcenebene und einen booleschen Wert, *VolumeTiledResourcesSupported,* der ankniff, ob volumenkachelte Ressourcen unterstützt werden.

Methoden

* [**ID3D12Device::CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : Wird verwendet, um zu bestimmen, welche Features und auf welcher Ebene von der aktuellen Hardware unterstützt werden.
* [**ID3D12GraphicsCommandList::CopyTiles:**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) Kopiert Kacheln aus dem Puffer in eine gekachelte Ressource oder umgekehrt.
* [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) Aktualisiert Zuordnungen von Kachelspeicherorten in gekachelten Ressourcen zu Speicherorten in einem Ressourcenhap.
* [**ID3D12CommandQueue::CopyTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) Kopiert Zuordnungen aus einer gekachelten Quellressource in eine gekachelte Zielressource.
* [**ID3D12Device::GetResourceTiling**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln zerbrochen wird.

## <a name="related-topics"></a>Zugehörige Themen

* [Ressourcenbindung](resource-binding.md)
