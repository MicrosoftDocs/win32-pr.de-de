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
# <a name="volume-tiled-resources"></a>Menge gekachelter Ressourcen

Volumentexturen (3D) können als kachelbasierte Ressourcen verwendet werden. Dabei wird darauf hinzuweisen, dass die Kachelauflösung dreidimensional ist.

-   [Übersicht](#overview)
-   [D3D11.3-Ressourcen-APIs mit Kachel](#d3d113-tiled-resource-apis)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Übersicht

Gekachelte Ressourcen entkoppeln ein D3D-Ressourcenobjekt vom Sicherungsspeicher (ressourcen in der Vergangenheit hatten eine 1:1-Beziehung mit ihrem Sicherungsspeicher). Dies ermöglicht eine Vielzahl von interessanten Szenarien, z. B. das Streamen von Texturdaten und das Wiederverwenden oder Reduzieren der Speicherauslastung.

2D-Texturkachelressourcen werden in D3D11.2 unterstützt. D3D12 und D3D11.3 fügen Unterstützung für 3D-Kacheltexturen hinzu.

Die typischen Ressourcendimensionen, die beim Kacheln verwendet werden, sind 4 x 4 Kacheln für 2D-Texturen und 4 x 4 x 4 Kacheln für 3D-Texturen.



| Bits/Pixel (1 Stichprobe/Pixel)                            | Kacheldimensionen (Pixel, w x h x d)                                    |
|-----------------------------|-------------------------------------|
| 8                           | 64 x 32 x 32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128 x 64 x 16                           |
| BC 2,3,5,6,7                | 64 x 64 x 16                            |



 

Beachten Sie, dass die folgenden Formate bei gekachelten Ressourcen nicht unterstützt werden: 96bpp-Formate, Videoformate, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.

In den folgenden Diagrammen stellt dunkelgrau NULL-Kacheln dar.

-   [Standardzuordnung der texturierten 3D-Kachelressource (am ausführlichsten)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Standardzuordnung der texturierten 3D-Kachelressource (zweit ausführlichste mip)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Textur-3D-Kachelressource (ausführlichste mip)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Textur-3D-Kachelressource (zweit ausführlichste mip)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Textur-3D-Kachelressource (einzelne Kachel)](#texture-3d-tiled-resource-single-tile)
-   [Textur-3D-Kachelressource (Uniform Box)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Standardzuordnung der texturierten 3D-Kachelressource (am ausführlichsten)

![Standardzuordnung des ausführlichsten MIP](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Standardzuordnung der texturierten 3D-Kachelressource (zweit ausführlichste mip)

![Standardzuordnung des zweit ausführlichsten MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Textur-3D-Kachelressource (ausführlichste mip)

Mit dem folgenden Code wird eine gekachelte 3D-Ressource mit dem ausführlichsten MIP eingerichtet.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Textur-3D-Kachelressource (zweit ausführlichste mip)

Der folgende Code richtet eine gekachelte 3D-Ressource und den zweit ausführlichsten MIP ein:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Textur-3D-Kachelressource (einzelne Kachel)

Mit dem folgenden Code wird eine Einzelkachelressource eingerichtet:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Textur-3D-Kachelressource (Uniform Box)

Der folgende Code richtet eine uniform Box-Kachelressource ein (beachten Sie die -Anweisung. `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>D3D11.3-Ressourcen-APIs mit Kachel

Die gleichen API-Aufrufe werden sowohl für 2D- als auch für 3D-kachelte Ressourcen verwendet:

Enumerationen

-   [**D3D11 \_ TILED \_ RESOURCES \_ TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : Bestimmt die Ebene der Unterstützung für gekachelte Ressourcen.
-   [**D3D11 \_ FORMAT \_ SUPPORT2:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) Wird verwendet, um die Unterstützung für gekachelte Ressourcen zu testen.
-   [**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY LEVELS \_ \_ FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : Bestimmt die Unterstützung von kachelbasierten Ressourcen in einer Ressource mit mehreren Stichproben.
-   [**D3D11 \_ TILE \_ COPY \_ FLAGS:**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) Enthält Flags zum Kopieren in und aus gekachelten Ressourcen und linearen Puffern.

Strukturen

-   [**D3D11 \_ TILED \_ RESOURCE \_ COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : enthält die x-, y- und z-Koordinate sowie den Unterressourcenverweis. Beachten Sie, dass eine Hilfsklasse vorhanden ist: CD3D11 \_ TILED \_ RESOURCE \_ COORDINATE.
-   [**D3D11 \_ TILE \_ REGION \_ SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : Gibt die Größe und Anzahl der Kacheln des gekachelten Bereichs an.
-   [**D3D11 \_ TILE \_ SHAPE:**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) Die Kachelform als Breite, Höhe und Tiefe in Texel.
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): enthält die unterstützte Ebene der Kachelressourcenebene.

Methoden

-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) Wird verwendet, um zu bestimmen, welche Features und auf welchem Tarif von der aktuellen Hardware unterstützt werden.
-   [**ID3D11DeviceContext2::CopyTiles:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) Kopiert Kacheln aus dem Puffer in eine gekachelte Ressource oder umgekehrt.
-   [**ID3D11DeviceContext2::UpdateTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) aktualisiert Zuordnungen von Kachelspeicherorten in gekachelten Ressourcen zu Arbeitsspeicherspeicherorten in einem Kachelpool.
-   [**ID3D11DeviceContext2::CopyTileMappings:**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Kopiert Zuordnungen aus einer gekachelten Quellressource in eine gekachelte Zielressource.
-   [**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : Ruft Informationen darüber ab, wie eine gekachelte Ressource in Kacheln zerbrochen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11.3-Features](direct3d-11-3-features.md)
</dt> </dl>

 

 




