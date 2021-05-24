---
description: Koordinatensysteme für Direct3D 10 werden für Pixel und Texel definiert.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Koordinatensysteme (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3da846ae4b989f6d8cb4741f9df8f7228e8970
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335464"
---
# <a name="coordinate-systems-direct3d-10"></a>Koordinatensysteme (Direct3D 10)

Koordinatensysteme für Direct3D 10 werden für Pixel und Texel definiert.



Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Direct3D 10 definiert die linke obere Ecke des oberen linken Pixels als Ursprung eines Renderziels.
- Direct3D 9 definiert die Mitte des pixel oben links als Ursprung eines Renderziels.



 

[Pixelkoordinatensystem](#pixel-coordinate-system)
- [Pixelkoordinatensystem für Direct3D 9](#pixel-coordinate-system-for-direct3d-9)

[Texel-Koordinatensystem](#texel-coordinate-system)
- [Texel-Koordinatensystem](#texel-coordinate-system)

[Verwandte Themen](#related-topics)

## <a name="pixel-coordinate-system"></a>Pixelkoordinatensystem

Das Pixelkoordinatensystem in Direct3D 10 definiert den Ursprung eines Renderziels in der oberen linken Ecke. wie im folgenden Diagramm dargestellt. Pixelcenter werden von ganzzahligen Positionen um (0,5f, 0,5f) versetzt.

![Diagramm des Pixelkoordinatensystems in direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Pixelkoordinatensystem für Direct3D 9

Als Referenz ist hier das Pixelkoordinatensystem für Direct3D 9 angegeben, das den Ursprung oder ein Renderziel als Mitte des oberen linken Pixels (0,5,0,5) von der oberen linken Ecke entfernt definiert hat, wie im folgenden Diagramm dargestellt. In Direct3D 9 befinden sich Pixelcenter an ganzzahligen Positionen.

![Diagramm des Pixelkoordinatensystems in direct3d 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Texelkoordinatensystem

Das Texelkoordinatensystem hat seinen Ursprung in der oberen linken Ecke der Textur, wie im folgenden Diagramm dargestellt. Dies macht das Rendern bildschirmbündiger Texturen trivial (in Direct3D 10), da das Pixelkoordinatensystem am Texelkoordinatensystem ausgerichtet ist.

![Diagramm des Texelkoordinatensystems](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Texelkoordinatensystem

Texturkoordinaten werden entweder mit einer normalisierten oder einer skalierten Zahl dargestellt. Jede Texturkoordinate wird einem bestimmten Texel wie folgt zugeordnet:

Für eine normalisierte Koordinate:

-   Punktstichproben: Texel \# = floor(U \* Width)
-   Lineare Stichprobenentnahme: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel + \# 1

Für eine skalierte Koordinate:

-   Punktsampling: Texel \# = floor(U)
-   Lineare Stichprobenentnahme: Left Texel \# = floor(U - 0,5), Right Texel \# = Left Texel + \# 1

Wobei die Breite die Breite der Textur (in Texel) ist.

Die Texturadressumbruch erfolgt, nachdem die Texelposition berechnet wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




