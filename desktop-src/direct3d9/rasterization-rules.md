---
description: Häufig stimmen die für Scheitelpunkte angegebenen Punkte nicht genau mit den Pixeln auf dem Bildschirm überein. In diesem Fall wendet Direct3D Rasterungsregeln für Dreiecke an, um zu entscheiden, welche Pixel für ein bestimmtes Dreieck gelten.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Rasterungsregeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d241248f5a69262129f60fc005582dc5e03b2a6931cf024bc4613d81558cdb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746667"
---
# <a name="rasterization-rules-direct3d-9"></a>Rasterungsregeln (Direct3D 9)

Häufig stimmen die für Scheitelpunkte angegebenen Punkte nicht genau mit den Pixeln auf dem Bildschirm überein. In diesem Fall wendet Direct3D Rasterungsregeln für Dreiecke an, um zu entscheiden, welche Pixel für ein bestimmtes Dreieck gelten.

-   [Rasterungsregeln für Dreiecke](#triangle-rasterization-rules)
-   [Punkt- und Linienregeln](#point-and-line-rules)
-   [Punkt-Sprite-Regeln](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Rasterungsregeln für Dreiecke

Direct3D verwendet eine Füllkonvention von oben links zum Füllen von Geometrie. Dies ist die gleiche Konvention, die auch für Rechtecke in GDI und OpenGL verwendet wird. In Direct3D ist die Mitte des Pixels der Endpunkt. Wenn sich der Mittelpunkt innerhalb eines Dreiecks befindet, ist das Pixel Teil des Dreiecks. Pixelcenter befinden sich an ganzzahligen Koordinaten.

Diese Beschreibung der von Direct3D verwendeten Dreiecksrasterungsregeln gilt nicht unbedingt für alle verfügbaren Hardwarekomponenten. Ihre Tests können geringfügige Abweichungen bei der Implementierung dieser Regeln erkennen.

Die folgende Abbildung zeigt ein Rechteck, dessen obere linke Ecke sich bei (0, 0) und dessen untere rechte Ecke bei (5, 5) befindet. Dieses Rechteck füllt wie erwartet 25 Pixel. Die Breite des Rechtecks wird als rechts minus links definiert. Die Höhe ist als unten minus oben definiert.

![Abbildung eines nummerierten Quadrats, unterteilt in sechs Zeilen und Spalten](images/pixmap.png)

In der Füllkonvention oben links bezieht sich *top* auf die vertikale Position von horizontalen Spannen, und *links* auf die horizontale Position von Pixeln innerhalb einer Spanne. Ein Rand kann nur dann ein oberer Rand sein, wenn er horizontal ist. Im Allgemeinen weisen die meisten Dreiecke nur linke und rechte Ränder auf. Die folgende Abbildung zeigt einen oberen und einen rechten Rand.

![Abbildung eines nummerierten Quadrats, das zwei Dreiecke enthält](images/triedge.png)

Die Füllkonvention oben links bestimmt die Von Direct3D ausgeführte Aktion, wenn ein Dreieck durch die Mitte eines Pixels verläuft. Die folgende Abbildung zeigt zwei Dreiecke: eins bei (0, 0), (5, 0) und (5, 5) und das andere bei (0, 5), (0, 0) und (5, 5). Das erste Dreieck erhält in diesem Fall 15 Pixel (schwarz dargestellt), während das zweite nur 10 Pixel (grau dargestellt) erhält, da der gemeinsame Rand der linke Rand des ersten Dreiecks ist.

![Abbildung eines nummerierten Quadrats, das zwei Dreiecke zeigt](images/twotris.png)

Wenn Sie ein Rechteck mit der oberen linken Ecke bei (0,5, 0,5) und der unteren rechten Ecke bei (2,5, 4,5) definieren, ist der Mittelpunkt dieses Rechtecks bei (1,5, 2,5). Wenn der Direct3D-Rasterizer dieses Rechteck mosaikiert, befindet sich der Mittelpunkt jedes Pixels eindeutig innerhalb jedes der vier Dreiecke, und die Konvention für die obere linke Füllung ist nicht erforderlich. Die folgende Abbildung zeigt dies. Die Pixel im Rechteck werden entsprechend dem Dreieck bezeichnet, in dem Direct3D sie enthält.

![Zeigt ein nummeriertes Quadrat an, das ein Rechteck enthält, das in vier Dreiecke unterteilt ist.](images/noambig.png)

Wenn Sie das Rechteck in der vorherigen Abbildung so verschieben, dass sich die obere linke Ecke bei (1,0, 1,0), die untere rechte Ecke bei (3,0, 5,0) und der Mittelpunkt bei (2,0, 3,0) befindet, wendet Direct3D die Ober-links-Füllkonvention an. Die meisten Pixel in diesem Rechteck umschließen den Rahmen zwischen zwei oder mehr Dreiecken, wie in der folgenden Abbildung dargestellt.

![Abbildung eines nummerierten Quadrats, das ein Rechteck enthält, das in vier Dreiecke unterteilt ist](images/fillrule.png)

Für beide Rechtecke sind die gleichen Pixel betroffen, wie in der folgenden Abbildung dargestellt.

![Abbildung von Pixeln, die von den beiden vorangehenden nummerierten Quadraten betroffen sind](images/samepix.png)

## <a name="point-and-line-rules"></a>Punkt- und Linienregeln

Punkte werden genauso wie Punkt-Sprites gerendert, die beide als bildschirmbündig ausgerichtete Quadquaraterale gerendert werden und somit den gleichen Regeln wie beim Polygonrendering entsprechen.

Nicht gealiaste Zeilenrenderingregeln sind identisch mit denen für [GDI-Zeilen.](../gdi/lines.md)

Informationen zum Rendern von antialiasierten Zeilen finden Sie unter [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Punkt-Sprite-Regeln

Punkt-Sprites und Patchprimitiven werden so gerastert, als ob die Primitiven zum ersten Mal in Dreiecke und die resultierenden Dreiecke gerastert wurden. Weitere Informationen finden Sie unter [Point Sprites (Direct3D 9)](point-sprites.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
