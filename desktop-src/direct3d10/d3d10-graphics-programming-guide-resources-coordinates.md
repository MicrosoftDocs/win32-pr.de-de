---
description: Koordinatensysteme für Direct3D 10 sind für Pixel und Texels definiert.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Koordinatensysteme (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748969"
---
# <a name="coordinate-systems-direct3d-10"></a>Koordinatensysteme (Direct3D 10)

Koordinatensysteme für Direct3D 10 sind für Pixel und Texels definiert.



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Direct3D 10 definiert die linke obere Ecke des linken oberen Pixels als Ursprung eines Renderziels.<br/> Direct3D 9 definiert den Mittelpunkt des linken oberen Pixels als Ursprung eines Renderziels.<br/> |



 

-   [Pixel Koordinaten System](#pixel-coordinate-system)
    -   [Pixel Koordinaten System für Direct3D 9](#pixel-coordinate-system-for-direct3d-9)
-   [Texel-Koordinaten System](#texel-coordinate-system)
    -   [Texel-Koordinaten System](#texel-coordinate-system)
-   [Zugehörige Themen](#related-topics)

## <a name="pixel-coordinate-system"></a>Pixel Koordinaten System

Das Pixelkoordinaten System in Direct3D 10 definiert den Ursprung eines Renderziels in der linken oberen Ecke. wie im folgenden Diagramm gezeigt. Pixel Center werden von ganzzahligen Speicherorten um (0,5 f, 0,5 f) versetzt.

![Diagramm des Pixelkoordinaten Systems in Direct3D 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a>Pixel Koordinaten System für Direct3D 9

Im folgenden finden Sie das Pixelkoordinaten System für Direct3D 9, das den Ursprung oder ein Renderziel als Mittelpunkt des linken oberen Pixels (0,5, 0,5) von der linken oberen Ecke definiert, wie im folgenden Diagramm dargestellt. In Direct3D 9 befinden sich Pixel Center an ganzzahligen Positionen.

![Diagramm des Pixelkoordinaten Systems in Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a>Texel-Koordinaten System

Das Texel-Koordinatensystem hat seinen Ursprung in der oberen linken Ecke der Textur, wie im folgenden Diagramm dargestellt. Dies macht das Rendern von Bildschirm Ausrichtung (in Direct3D 10) trivial, da das Pixelkoordinaten System am texelkoordinaten System ausgerichtet ist.

![Diagramm des Texel-Koordinatensystems](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a>Texel-Koordinaten System

Texturkoordinaten werden entweder durch eine normalisierte oder eine skalierte Zahl dargestellt. Jede Textur Koordinate wird wie folgt einem bestimmten Textem zugeordnet:

Für eine normalisierte Koordinate:

-   Punkt Stichproben: Texel \# = Floor (U \* Width)
-   Lineare Stichprobenentnahme: Left Texel \# = Floor (U \* Width), Right Texel \# = left Texel \# + 1

Für eine skalierte Koordinate:

-   Punkt Stichproben: Texel \# = Floor (U)
-   Lineare Stichprobenentnahme: Left Texel \# = Floor (U-0,5), Right Texel \# = left Texel \# + 1

Dabei ist die Breite die Breite der Textur (in Texels).

Das Umwickeln von Textur Adressen tritt auf, nachdem der textsort berechnet wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




