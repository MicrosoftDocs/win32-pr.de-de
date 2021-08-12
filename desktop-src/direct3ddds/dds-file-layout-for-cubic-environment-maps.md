---
title: Beispiel für DDS-Cubezuordnung
description: Bei kubischen Umgebungszuordnungen werden ein oder mehrere Gesichter eines Cubes in die Datei geschrieben, wobei entweder unkomprimierte oder komprimierte Formate verwendet werden, und alle Gesichter müssen die gleiche Größe aufweisen.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a51526570a775eb0cff8ec5ed665ac3dc4b218a876743b29e983bd9c03e9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289862"
---
# <a name="dds-cube-map-example"></a>Beispiel für DDS-Cubezuordnung

Bei kubischen Umgebungszuordnungen werden ein oder mehrere Gesichter eines Cubes in die Datei geschrieben, wobei entweder unkomprimierte oder komprimierte Formate verwendet werden, und alle Gesichter müssen die gleiche Größe aufweisen. Für jedes Gesicht können Mipmaps definiert sein, obwohl alle Gesichter die gleiche Anzahl von Mipmapebenen aufweisen müssen. Wenn eine Datei eine Cubezuordnung enthält, sollten DDSCAPS \_ COMPLEX, DDSCAPS2 \_ CUBEMAP und mindestens eine DSCAPS2 \_ CUBEMAP \_ POSITIVEX/Y/Z und/oder DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX/Y/Z festgelegt werden. Die Gesichter werden in der Reihenfolge geschrieben: positives x, negatives x, positives y, negatives y, positives z, negatives z, wobei fehlende Gesichter weggelassen werden. Jedes Gesicht wird mit seinem Hauptbild geschrieben, gefolgt von beliebigen Mipmapebenen.

Beispielsweise würde eine 256 x 256-Cubemap mit positiven x-, negativen y- und positiven Z-Gesichtern, einem Pixelformat von DXT1 und allen Mipmapebenen Folgendes enthalten:



| DDS-Komponenten                                      | \# Bytes |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| 256 x 256 positives x Hauptbild                    | 32768    |
| 128 x 128 positives x mipmap-Bild                  | 8192     |
| 64 x 64 positives x mipmap-Bild                    | 2048     |
| 32 x 32 positives x mipmap-Bild                    | 512      |
| 16 x 16 positives x mipmap-Bild                    | 128      |
| 8 x 8 positives x mipmap-Bild                      | 32       |
| 4 x 4 positives x mipmap-Bild                      | 8        |
| 2 x 2 positives x mipmap-Bild                      | 8        |
| 1-by-1 positives x mipmap-Bild                      | 8        |
| Wiederholen Sie die vorherigen 9 Ebenen für das y-Mipmap-Bild. | 43704    |
| Wiederholen Sie die vorherigen 9 Ebenen für das z-mipmap-Bild. | 43704    |



 

Ab DirectX 8 wird eine Cubemap mit allen definierten Gesichtern gespeichert.

## <a name="dxgi-cube-maps"></a>DXGI Cube Karten

Kubische Umgebungszuordnungen in Direct3D 10.x und Direct3D 11 entsprechen einem 2D-Texturarray mit 6 Bildern und können als solche in DDS-Dateien gespeichert werden. Mit Direct3D 10.1 und Direct3D 11 kann die Hardware auch Arrays von Cubemaps unterstützen, die selbst 2D-Texturarrays mit einem Vielfachen von 6 Bildern (6, 12, 18, 24 usw.) sind.

Hier sehen Sie beispielsweise eine 256 mal 256 Cubemap mit Mipmapebenen, die in einem BC6H-Format als 2D-Texturarray gespeichert sind:



| DDS-Komponenten                                                                                                                                                                                                  | \# Bytes |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| header (FourCC von "DX10")                                                                                                                                                                                       | 128      |
| erweiterter Header (DXGI-Format auf 95 \[ DXGI \_ FORMAT \_ BC6H \_ UF16 \] festgelegt, Dimensionswert von \[ 3 D3Dxx \_ RESOURCE DIMENSION \_ \_ TEXTURE2D, \] Arraygröße 6, Verschiedene Flags von 0x4 \[ D3Dxx \_ RESOURCE \_ MISC \_ TEXTURECUBE \] ) | 20       |
| 256 x 256 Arrayeintrag 0 (positives x) Hauptbild                                                                                                                                                                | 65536    |
| 128 x 128 Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                              | 16384    |
| 64 x 64 Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                                | 4096     |
| 32 x 32 Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                                | 1024     |
| 16 x 16 Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                                | 256      |
| 8-mal-8-Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                                  | 64       |
| 4-mal-4-Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                                  | 16       |
| 2-mal-2-Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                                  | 16       |
| 1-by-1-Arrayeintrag 0 (positives x) mipmap-Bild                                                                                                                                                                  | 16       |
| Wiederholen Sie die vorherigen 9 Ebenen für das Mipmap-Bild des Arrayeintrags 1 (negativ x).                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für das Mipmap-Bild des Arrayeintrags 2 (positiv y).                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für das Mipmap-Bild des Arrayeintrags 3 (negativ y).                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für das Mipmap-Bild des Arrayeintrags 4 (positives z).                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für das Mipmap-Bild des Arrayeintrags 5 (negatives z).                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




