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
# <a name="volume-tiled-resources"></a>Menge gekachelter Ressourcen

Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.

-   [Übersicht](#overview)
-   [D3D 11.3 gekachelte Ressourcen-APIs](#d3d113-tiled-resource-apis)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Gekachelte Ressourcen entkoppeln ein D3D-Ressourcen Objekt von seinem Unterstützungs Speicher (die Ressourcen in der Vergangenheit verfügten über eine 1:1-Beziehung mit Ihrem Sicherungs Speicher). Dies ermöglicht eine Vielzahl interessanter Szenarien, z. b. das Streaming in Textur Daten und die Wiederverwendung oder Reduzierung der Speicherauslastung.

2D-Textur-Kachel Ressourcen werden in D3D 11.2 unterstützt. D3D12 und D3D 11.3 fügen Unterstützung für 3D-Kacheln hinzu.

Die typischen Ressourcen Dimensionen, die beim tichen verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.



|                             |                                     |
|-----------------------------|-------------------------------------|
| Bits/Pixel (1 Stichprobe/Pixel) | Kachel Dimensionen (Pixel, w x h x d) |
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

![Standard Zuordnung der detaillierteren MIP-](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Standard Zuordnung für textur 3D-Kacheln (zweit ausführlichere MIP)

![Standard Zuordnung der zweit detailliertesten MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Textur 3D-Kachel Ressource (ausführlichste MIP)

Mit dem folgenden Code wird eine 3D-Kachel Ressource in der detaillierteren MIP-Datei eingerichtet.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Textur 3D-Kachel Ressource (zweites detaillierteres MIP)

Der folgende Code richtet eine gekachelte 3D-Ressource und die zweit ausführlichste MIP-Datei ein:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Textur 3D-Kachel Ressource (einzelne Kachel)

Der folgende Code richtet eine einzelne Kachel Ressource ein:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Textur 3D-Kachel (Uniform Box)

Der folgende Code richtet eine einheitliche Box-Kachel Ressource ein (Beachten Sie die-Anweisung. `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>D3D 11.3 gekachelte Ressourcen-APIs

Die gleichen API-Aufrufe werden sowohl für 2D-als auch für 3D-Kachel Ressourcen verwendet:

Enumerationen

-   [**D3D11 \_ Kachel mit Kachel \_ Ressourcen \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : bestimmt die Ebene der Unterstützung für gekachelte Ressourcen.
-   [**D3D11 \_ Format \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : wird zum Testen der Unterstützung für gekachelte Ressourcen verwendet.
-   [**D3D11 \_ Überprüfen der \_ Multisample \_ Quality \_ Levels- \_ Flag**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : bestimmt die Unterstützung von unterstützten Ressourcen in einer Multisampling-Ressource.
-   [**D3D11 \_ \_Kachelkopierflags \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : enthält Flags zum Kopieren in und aus gekachelten Ressourcen und linearen Puffern.

Strukturen

-   [**D3D11 \_ Gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : enthält die x-, y-und z-Koordinaten und den untergeordneten Quell Verweis. Beachten Sie, dass es eine Hilfsklasse gibt: CD3D11 \_ Kachel \_ Ressourcen \_ Koordinate.
-   [**D3D11 \_ Kachel \_ Regions \_ Größe**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : gibt die Größe und die Anzahl der Kacheln des gekachelten Bereichs an.
-   [**D3D11 \_ Kachel \_ Form**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : die Kachel Form als Breite, Höhe und Tiefe in texeln.
-   [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): enthält die unterstützte Kachel Ressourcenebene.

Methoden

-   [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : wird verwendet, um zu bestimmen, welche Features und auf welcher Ebene von der aktuellen Hardware unterstützt werden.
-   [**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : kopiert Kacheln aus dem Puffer in eine gekachelte Ressource oder umgekehrt.
-   [**ID3D11DeviceContext2:: updatetilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : aktualisiert Zuordnungen von Kachel Positionen in gekachelten Ressourcen zu Speicherorten in einem Kachel Pool.
-   [**ID3D11DeviceContext2:: copytilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : kopiert Zuordnungen aus einer Ressource mit Kachel Kachel in eine gekachelte Ziel Ressource.
-   [**ID3D11DeviceContext2:: getresourcetielt**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln aufgeteilt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11,3-Features](direct3d-11-3-features.md)
</dt> </dl>

 

 




