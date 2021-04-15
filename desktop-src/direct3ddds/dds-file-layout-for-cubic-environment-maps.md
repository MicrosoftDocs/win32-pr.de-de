---
title: Beispiel für DDS-cubemap
description: Bei kubischen Umgebungs Zuordnungen werden ein oder mehrere Gesichter eines Cubes in die Datei geschrieben. dabei werden entweder unkomprimierte oder komprimierte Formate verwendet, und alle Gesichter müssen dieselbe Größe aufweisen.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235749bc0cf95a2e2120f66f3bcfb8a46e158628
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515860"
---
# <a name="dds-cube-map-example"></a>Beispiel für DDS-cubemap

Bei kubischen Umgebungs Zuordnungen werden ein oder mehrere Gesichter eines Cubes in die Datei geschrieben. dabei werden entweder unkomprimierte oder komprimierte Formate verwendet, und alle Gesichter müssen dieselbe Größe aufweisen. Für jedes Gesicht können Mipmaps definiert sein, obwohl alle Gesichter die gleiche Anzahl von MipMap-Ebenen aufweisen müssen. Wenn eine Datei eine cubemap enthält, werden DDSCAPS \_ Complex, DDSCAPS2 \_ cubemap und mindestens eine DSCAPS2 \_ cubemap \_ positivex/y/z und/oder DDSCAPS2 \_ cubemap \_ negativex/y/z festgelegt. Die Gesichter werden in der Reihenfolge geschrieben: positive x, minus x, positives y, minus y, positives z, minus z, wobei fehlende Gesichter ausgelassen werden. Jedes Gesicht wird mit seinem Hauptbild, gefolgt von allen MipMap-Ebenen, geschrieben.

Beispielsweise eine 256-by-256-cubemap mit positiven x-, negativen y-und positiven z-Gesichtern, einem Pixel Format von DXT1 und allen MipMap-Ebenen, die Folgendes enthalten:



| DDS-Komponenten                                      | \# Satz |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| 256 x 256 positives x-Hauptbild                    | 32768    |
| 128-bis-128 positives x-MipMap-Bild                  | 8192     |
| 64-bis-64 positives x-MipMap-Bild                    | 2048     |
| 32-bis-32 positives x-MipMap-Bild                    | 512      |
| 16 x 16 positives x-MipMap-Bild                    | 128      |
| 8 x 8 positives x-MipMap-Bild                      | 32       |
| 4 x 4 positives x-MipMap-Bild                      | 8        |
| 2 x 2 positives x-MipMap-Bild                      | 8        |
| 1:1 positives x-MipMap-Bild                      | 8        |
| Wiederholen Sie die vorherigen 9 Ebenen für das y-MipMap-Bild. | 43704    |
| Wiederholen Sie die vorherigen 9 Ebenen für das z-MipMap-Bild. | 43704    |



 

Ab DirectX 8 wird eine cubemap mit allen definierten Gesichtern gespeichert.

## <a name="dxgi-cube-maps"></a>DXGI-Cubemaps

Die Karten der kubischen Umgebung in Direct3D 10. x und Direct3D 11 entsprechen einem 2D-Textur Array mit 6 Bildern und können in DDS-Dateien als solche gespeichert werden. Mit Direct3D 10,1 und Direct3D 11 kann die Hardware auch Arrays von Cubemaps unterstützen, bei denen es sich selbst um 2D-Textur Arrays mit einem Vielfachen von 6 Bildern (6, 12, 18, 24 usw.) handelt.

Hier sehen Sie beispielsweise eine 256-by-256-cubemap mit MipMap-Ebenen, die in einem BC6H-Format als 2D-Textur Array gespeichert werden:



| DDS-Komponenten                                                                                                                                                                                                  | \# Satz |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| Header (FourCC von "DX10")                                                                                                                                                                                       | 128      |
| Extended-Header (DXGI-Format, festgelegt auf 95 \[ DXGI- \_ Format \_ BC6H \_ UF16 \] , Dimensions Wert 3 \[ D3Dxx \_ Resource- \_ Dimension \_ TEXTURE2D \] , Array Größe von 6, sonstige Flags von 0x4 \[ D3Dxx \_ \_ ressourcenmisc \_ texturecube \] ) | 20       |
| 256-bis-256 Array Eintrag 0 (positives x) Hauptbild                                                                                                                                                                | 65536    |
| 128-bis-128 Array Eintrag 0 (positives x) MipMap-Bild                                                                                                                                                              | 16384    |
| 64-bis-64 Array Eintrag 0 (positives x) MipMap-Bild                                                                                                                                                                | 4096     |
| 32-bis-32 Array Eintrag 0 (positives x) MipMap-Bild                                                                                                                                                                | 1024     |
| 16-bis-16-Array Eintrag 0 (positives x) MipMap-Bild                                                                                                                                                                | 256      |
| 8-mal-8 Array Entry 0 (positives x) MipMap-Bild                                                                                                                                                                  | 64       |
| 4 x 4 Array Eintrag 0 (positives x) MipMap-Bild                                                                                                                                                                  | 16       |
| 2 x 2 Array Eintrag 0 (positives x) MipMap-Bild                                                                                                                                                                  | 16       |
| 1:1 Array Eintrag 0 (positives x) MipMap-Bild                                                                                                                                                                  | 16       |
| Wiederholen Sie die vorherigen 9 Ebenen für das Array Entry 1 (negatives x) MipMap-Image.                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für Array Eintrag 2 (positives y) MipMap-Bild.                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für Array Eintrag 3 (negatives y) MipMap-Bild.                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für Array Eintrag 4 (positives z) MipMap-Bild.                                                                                                                                        | 87408    |
| Wiederholen Sie die vorherigen 9 Ebenen für Array Eintrag 5 (negatives z) MipMap-Bild.                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




