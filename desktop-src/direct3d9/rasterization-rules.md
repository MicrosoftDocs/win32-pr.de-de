---
description: Häufig Stimmen die für Scheitel Punkte angegebenen Punkte nicht exakt mit den Pixeln auf dem Bildschirm identisch. In diesem Fall wendet Direct3D Dreiecks rasterisierungsregeln an, um zu entscheiden, welche Pixel für ein bestimmtes Dreieck gelten.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Rasterisierungsregeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218910"
---
# <a name="rasterization-rules-direct3d-9"></a>Rasterisierungsregeln (Direct3D 9)

Häufig Stimmen die für Scheitel Punkte angegebenen Punkte nicht exakt mit den Pixeln auf dem Bildschirm identisch. In diesem Fall wendet Direct3D Dreiecks rasterisierungsregeln an, um zu entscheiden, welche Pixel für ein bestimmtes Dreieck gelten.

-   [Dreiecks rasterisierungsregeln](#triangle-rasterization-rules)
-   [Punkt-und Linien Regeln](#point-and-line-rules)
-   [Punkt Sprite-Regeln](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Dreiecks rasterisierungsregeln

Direct3D verwendet zum Auffüllen der Geometrie eine obere linke Füllungs Konvention. Dabei handelt es sich um dieselbe Konvention, die für Rechtecke in GDI und OpenGL verwendet wird. In Direct3D ist der Mittelpunkt des Pixels der entscheidende Punkt. Wenn sich das Zentrum in einem Dreieck befindet, ist das Pixel Teil des Dreiecks. Pixel Center sind an ganzzahligen Koordinaten.

Diese Beschreibung der von Direct3D verwendeten Dreiecks rasterisierungsregeln gilt nicht notwendigerweise für alle verfügbaren Hardware. Die Tests können kleinere Abweichungen in der Implementierung dieser Regeln aufdecken.

Die folgende Abbildung zeigt ein Rechteck, dessen linke obere Ecke bei (0,0) liegt und dessen untere rechte Ecke um (5, 5) liegt. Dieses Rechteck füllt 25 Pixel wie erwartet aus. Die Breite des Rechtecks wird als rechts minus Links definiert. Die Höhe ist als "Bottom minus Top" definiert.

![Abbildung eines nummerierten Quadrats, das in sechs Zeilen und Spalten aufgeteilt ist](images/pixmap.png)

In der oberen linken Füllungs Konvention verweist *Top* auf die vertikale Position horizontaler spannen, und *left* bezieht sich auf die horizontale Position der Pixel innerhalb einer Spanne. Ein Edge darf kein oberer Rand sein, es sei denn, er ist horizontal. Im Allgemeinen haben die meisten Dreiecke nur den linken und rechten Rand. Die folgende Abbildung zeigt einen oberen und einen rechten Rand.

![Abbildung eines nummerierten Quadrats, das zwei Dreiecke enthält](images/triedge.png)

Die obere linke Füllungs Konvention bestimmt die Aktion, die von Direct3D ausgeführt wird, wenn ein Dreieck den Mittelpunkt eines Pixels durchläuft. Die folgende Abbildung zeigt zwei Dreiecke: eins bei (0,0), (5, 0) und (5, 5) und das andere bei (0,0), (0, 0) und (5, 5). Das erste Dreieck in diesem Fall erhält 15 Pixel (schwarz dargestellt), während das zweite nur 10 Pixel (grau dargestellt) erhält, da der freigegebene Rand der linke Rand des ersten Dreiecks ist.

![Abbildung eines nummerierten Quadrats, das zwei Dreiecke anzeigt](images/twotris.png)

Wenn Sie ein Rechteck mit der linken oberen Ecke bei (0,5, 0,5) und der unteren rechten Ecke um (2,5, 4,5) definieren, befindet sich der Mittelpunkt dieses Rechtecks bei (1,5, 2,5). Wenn das Direct3D Raster-Element dieses Rechteck durchläuft, ist die Mitte der einzelnen Pixel eindeutig innerhalb der vier Dreiecke, und die obere linke Füllungs Konvention ist nicht erforderlich. Dies wird in der folgenden Abbildung veranschaulicht. Die Pixel im Rechteck sind entsprechend dem Dreieck gekennzeichnet, in dem Direct3D Sie enthält.

![Zeigt ein nummeriertes Quadrat an, das ein Rechteck enthält, das in vier Dreiecke aufgeteilt ist.](images/noambig.png)

Wenn Sie das Rechteck in der obigen Abbildung verschieben, sodass sich die obere linke Ecke bei (1,0, 1,0), der unteren rechten Ecke bei (3,0, 5,0) und dem zugehörigen Mittelpunkt bei (2,0, 3,0) befindet, wendet Direct3D die obere Füllungs Konvention an. Die meisten Pixel dieses Rechtecks verspannen den Rahmen zwischen zwei oder mehr Dreiecken, wie in der folgenden Abbildung dargestellt.

![Abbildung eines nummerierten Quadrats, das ein Rechteck enthält, das in vier Dreiecke aufgeteilt ist](images/fillrule.png)

Bei beiden Rechtecke sind die gleichen Pixel betroffen, wie in der folgenden Abbildung dargestellt.

![Abbildung von Pixeln, die von den vorangehenden zwei nummerierten Quadraten betroffen sind](images/samepix.png)

## <a name="point-and-line-rules"></a>Punkt-und Linien Regeln

Punkte werden genauso wie Punkt Sprite gerendert, die beide als Bildschirm ausgerichtete vierpunkte gerendert werden und somit denselben Regeln wie das Polygon Rendering entsprechen.

Zeilen Rendering-Regeln mit nicht-Antialiasing sind identisch mit denen für [GDI-Zeilen](../gdi/lines.md).

Weitere Informationen zum Rendern von Zeilen mit Antialiasing finden Sie unter [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Punkt Sprite-Regeln

Punkt Sprite und patchprimitiver werden so rasterisiert, als ob die primitiven zuerst in Dreiecke und die resultierenden Dreiecke in Dreiecke unterteilt wurden. Weitere Informationen finden Sie unter [Punkt Sprites (Direct3D 9)](point-sprites.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
