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
# <a name="volume-tiled-resources-direct3d-12"></a>Gekachelte Ressourcen (Direct3D 12)

Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.

-   [Übersicht](#overview)
-   [Ressourcen-APIs mit Kachel](#tiled-resource-apis)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Überblick

Gekachelte Ressourcen entkoppeln ein D3D-Ressourcen Objekt von seinem Unterstützungs Speicher (die Ressourcen in der Vergangenheit verfügten über eine 1:1-Beziehung mit Ihrem Sicherungs Speicher). Dies ermöglicht eine Vielzahl interessanter Szenarien, z. b. das Streaming in Textur Daten und die Wiederverwendung oder Reduzierung der Speicherauslastung.

2D-Textur-Kachel Ressourcen werden in D3D 11.2 unterstützt. Optionale Unterstützung für 3D-Kacheln mit Kacheln ist für D3D12 und D3D 11.3 verfügbar (siehe [**D3D12- \_ Kachel \_ Ressourcen \_ Ebene**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Die typischen Ressourcen Dimensionen, die beim tichen verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.



| Bits/Pixel (1 Stichprobe/Pixel) | Kachel Dimensionen (Pixel, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1, 4                      | 128 x 64x16                           |
| BC 2, 3, 5, 6, 7                | 64x64x16                            |

Beachten Sie, dass die folgenden Formate für die gekachelten Ressourcen nicht unterstützt werden: 96bpp-Formate, Videoformate, R1 \_ unorm, R8G8 \_ B8G8 \_ unorm, R8R8 \_ G8B8 \_ unorm.

In den Diagrammen unten steht dunkelgrau für NULL-Kacheln.

-   [Standard Zuordnung für textur 3D-Kacheln (ausführlichere MIP)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Standard Zuordnung für textur 3D-Kacheln (zweit ausführlichere MIP)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Textur 3D-Kachel Ressource (ausführlichste MIP)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Textur 3D-Kachel Ressource (zweites detaillierteres MIP)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Textur 3D-Kachel Ressource (einzelne Kachel)](#texture-3d-tiled-resource-single-tile)
-   [Textur 3D-Kachel (Uniform Box)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Standard Zuordnung für textur 3D-Kacheln (ausführlichere MIP)

![Standard Zuordnung einer gekachelten 3 dimensionalen Ressource](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Standard Zuordnung für textur 3D-Kacheln (zweit ausführlichere MIP)

![zeigt das zweit ausführlichste MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Textur 3D-Kachel Ressource (ausführlichste MIP)

Mit dem folgenden Code wird eine 3D-Kachel Ressource in der detaillierteren MIP-Datei eingerichtet.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Textur 3D-Kachel Ressource (zweites detaillierteres MIP)

Der folgende Code richtet eine gekachelte 3D-Ressource und die zweit ausführlichste MIP-Datei ein:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Textur 3D-Kachel Ressource (einzelne Kachel)

Der folgende Code richtet eine einzelne Kachel Ressource ein:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Textur 3D-Kachel (Uniform Box)

Der folgende Code richtet eine einheitliche Box-Kachel Ressource ein (Beachten Sie die-Anweisung. `trSize.bUseBox = true;) :`

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

## <a name="tiled-resource-apis"></a>Ressourcen-APIs mit Kachel

Die gleichen API-Aufrufe werden sowohl für 2D-als auch für 3D-Kachel Ressourcen verwendet:

Enumerationen

-   [**D3D12 \_ Kachel mit Kachel \_ Ressourcen \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : bestimmt die Ebene der Unterstützung für gekachelte Ressourcen.
-   [**D3D12 \_ Format \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : wird zum Testen der Unterstützung für gekachelte Ressourcen verwendet.
-   [**D3D12 \_ Multisample \_ - \_ \_ qualitätsebenenflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : bestimmt die Unterstützung von untergeordneten Ressourcen in einer Ressource mit mehreren Stichproben
-   [**D3D12 \_ \_Kachelkopierflags \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : enthält Flags zum Kopieren in und aus gekachelten Ressourcen und linearen Puffern.

Strukturen

-   [**D3D12 \_ Gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : enthält die x-, y-und z-Koordinaten und den untergeordneten Quell Verweis. Beachten Sie, dass es eine hilfsstruktur gibt: [**CD3DX12 \_ Kachel \_ Ressourcen \_ Koordinate**](cd3dx12-tiled-resource-coordinate.md).
-   [**D3D12 \_ Kachel \_ Regions \_ Größe**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : gibt die Größe und die Anzahl der Kacheln des gekachelten Bereichs an.
-   [**D3D12 \_ Kachel \_ Form**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : die Kachel Form als Breite, Höhe und Tiefe in texeln.
-   [**D3D12 \_ Feature \_ Data \_ D3D12 \_ Optionen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : enthält die unterstützte Kachel Ressourcenebene und einen booleschen Wert ( *volumetiledresourcessupported*), der angibt, ob volumenkachel-Ressourcen unterstützt werden.

Methoden

-   [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : wird verwendet, um zu bestimmen, welche Features und auf welcher Ebene von der aktuellen Hardware unterstützt werden.
-   [**ID3D12GraphcisCommandList:: copytiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : kopiert Kacheln aus dem Puffer in eine gekachelte Ressource oder umgekehrt.
-   [**ID3D12CommandQueue:: updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : aktualisiert Zuordnungen von Kachel Positionen in gekachelten Ressourcen zu Speicherorten in einem Ressourcenheap.
-   [**ID3D12CommandQueue:: copytilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : kopiert Zuordnungen aus einer Ressource mit Kachel Kachel in eine gekachelte Ziel Ressource.
-   [**ID3D12Device:: getresourcetielt**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln aufgeteilt wird.

## <a name="related-topics"></a>Verwandte Themen
* [Ressourcen Bindung](resource-binding.md)
