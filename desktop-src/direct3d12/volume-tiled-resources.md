---
title: Volumekachelressourcen (Direct3D 12)
description: Volumentexturen (3D) können als kachelbasierte Ressourcen verwendet werden. Dabei wird darauf hinzuweisen, dass die Kachelauflösung dreidimensional ist.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5371926b38415a84803155c67ea70ed902b915
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436305"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Volumekachelressourcen (Direct3D 12)

Volumentexturen (3D) können als kachelbasierte Ressourcen verwendet werden. Dabei wird darauf hinzuweisen, dass die Kachelauflösung dreidimensional ist.

## <a name="overview"></a>Übersicht

Gekachelte Ressourcen entkoppeln ein Direct3D-Ressourcenobjekt vom unterstützungsspeicher (in der Vergangenheit hatten Ressourcen eine 1:1-Beziehung mit ihrem Sicherungsspeicher). Dies ermöglicht eine Vielzahl interessanter Szenarien, z. B. das Streamen von Texturdaten und das Wiederverwenden oder Reduzieren der Speicherauslastung.

2D-Texturkachelressourcen werden in Direct3D 11.2 unterstützt. Optionale Unterstützung für 3D-kachelte Texturen ist für Direct3D 12 und Direct3D 11.3 verfügbar (siehe [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Die typischen Ressourcendimensionen, die beim Kacheln verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.

| Bits/Pixel (1 Stichprobe/Pixel) | Kacheldimensionen (Pixel, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64 x 32 x 32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128 x 64 x 16                           |
| BC 2,3,5,6,7                | 64 x 64 x 16                            |

Beachten Sie, dass die folgenden Formate bei kachelten Ressourcen nicht unterstützt werden: 96bpp-Formate, **Videoformate, R1_UNORM**, **R8G8_B8G8_UNORM** **, R8R8_G8B8_UNORM**.

In den folgenden Diagrammen stellt Dunkelgrau NULL-Kacheln dar.

* [Standardmäßige Zuordnung der gekachelten Textur-3D-Ressource (ausführlichstes MIP)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Standardmäßige Zuordnung der kachelten Textur-3D-Ressource (am weitesten detaillierter Mip)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Texture 3D Tiled Resource (most detailed mip) (Textur-3D-Kachelressource (ausführlichste mip))](#texture-3d-tiled-resource-most-detailed-mip)
* [Texture 3D Tiled Resource (second most detailed mip) (Textur-3D-Kachelressource (zweite detaillierteste mip))](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Textur-3D-Kachelressource (einzelne Kachel)](#texture-3d-tiled-resource-single-tile)
* [Textur-3D-Kachelressource (Uniform Box)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Standardmäßige Zuordnung der 3D-Kachelressource für Texturen (ausführlichstes MIP)

![Standardzuordnung einer gekachelten dreidimensionalen Ressource](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Standardmäßige Zuordnung der 3D-Kachelressource für Texturen (äußerst detaillierter Mip)

![zeigt den zweitdeweiterten Mip an.](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Textur-3D-Kachelressource (ausführlichste mip)

Mit dem folgenden Code wird eine 3D-Kachelressource mit dem ausführlichsten Mip eingerichtet.

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

![Ausführlichste mip-Struktur für eine dreidimensionale Textur](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Texture 3D tiled resource (second-most-detailed mip)

Mit dem folgenden Code wird eine 3D-kachelte Ressource und der zweite detaillierteste Mip eingerichtet.

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

![das zweitdeweiterte Mip für eine dreidimensionale Textur](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Textur-3D-Kachelressource (einzelne Kachel)

Mit dem folgenden Code wird eine einzelne Kachelressource eingerichtet.

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Textur-3D-Kachelressource (einheitliches Feld)

Der folgende Code richtet eine gekachelte Uniform Box-Ressource ein (beachten Sie die -Anweisung. `trSize.bUseBox = true;) :`

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

## <a name="tiled-resource-apis"></a>Gekachelte Ressourcen-APIs

Die gleichen API-Aufrufe werden sowohl für 2D- als auch für 3D-kachelte Ressourcen verwendet.

Enumerationen

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : bestimmt die Ebene der Unterstützung für gekachelte Ressourcen.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : wird verwendet, um die Unterstützung von gekachelten Ressourcen zu testen.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : Bestimmt die Unterstützung von gekachelten Ressourcen in einer Ressource mit mehreren Stichproben.
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : enthält Flags zum Kopieren in und aus gezischen Kachelressourcen und linearen Puffern.

Strukturen

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : enthält die x-, y- und z-Co-Direktions- und Unterressourcenreferenz. Beachten Sie, dass eine Hilfsstruktur vorhanden ist: [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : Gibt die Größe und Anzahl der Kacheln des gekachelten Bereichs an.
* [**D3D12_TILE_SHAPE:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) Die Kachelform als Breite, Höhe und Tiefe in Texel.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : enthält die unterstützte Ebene der Kachelressourcenebene und den booleschen *Wert VolumeTiledResourcesSupported,* der angibt, ob volumekachelte Ressourcen unterstützt werden.

Methoden

* [**ID3D12Device::CheckFeatureSupport:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) Wird verwendet, um zu bestimmen, welche Features und auf welchem Tarif von der aktuellen Hardware unterstützt werden.
* [**ID3D12GraphicsCommandList::CopyTiles:**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) Kopiert Kacheln aus dem Puffer in die gekachelte Ressource oder umgekehrt.
* [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) Aktualisiert Zuordnungen von Kachelspeicherorten in gekachelten Ressourcen zu Speicherspeicherorten in einem Ressourcenheap.
* [**ID3D12CommandQueue::CopyTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) Kopiert Zuordnungen aus einer quellkachelten Ressource in eine zielkachelte Ressource.
* [**ID3D12Device::GetResourceTiling:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) Ruft Informationen dazu ab, wie eine gekachelte Ressource in Kacheln aufgeteilt wird.

## <a name="related-topics"></a>Zugehörige Themen

* [Ressourcenbindung](resource-binding.md)
