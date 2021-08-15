---
description: 'Kurz gesagt: Texturumbruch ändert die grundlegende Methode, mit der Direct3D texturierte Polygone mithilfe der für jeden Scheitelpunkt angegebenen Texturkoordinaten rastert.'
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Texturumbruch (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c29ebe78bcfa237f46eacb247432185adedd1e53ae0774e767807269bb3bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984765"
---
# <a name="texture-wrapping-direct3d-9"></a>Texturumbruch (Direct3D 9)

Kurz gesagt: Texturumbruch ändert die grundlegende Methode, mit der Direct3D texturierte Polygone mithilfe der für jeden Scheitelpunkt angegebenen Texturkoordinaten rastert. Beim Rastern eines Polygons interpoliert das System zwischen den Texturkoordinaten an jedem Scheitelpunkt des Polygons, um die Texel zu bestimmen, die für jedes Pixel des Polygons verwendet werden sollen. Normalerweise behandelt das System die Textur als 2D-Ebene und interpoliert neue Texel, indem die kürzeste Route von Punkt A innerhalb einer Textur zu Punkt B verwendet wird. Wenn Punkt A die Position u, v (0,8, 0,1) darstellt und Punkt B bei (0,1,0,1) ist, sieht die Interpolationszeile wie im folgenden Diagramm aus.

![Diagramm einer Interpolationslinie zwischen zwei Punkten](images/interp1.png)

Beachten Sie, dass die kürzeste Entfernung zwischen A und B in dieser Abbildung ungefähr durch die Mitte der Textur verläuft. Das Aktivieren der U-Textur- oder V-Textur-Koordinatenumbruchs ändert, wie Direct3D die kürzeste Route zwischen Texturkoordinaten in U-Richtung und V-Richtung wahrnimmt. Definitionsgemäß bewirkt texturiertes Umschließen, dass der Rasterizer die kürzeste Route zwischen Texturkoordinatensätzen nimmt, vorausgesetzt, dass 0,0 und 1,0 zufällig sind. Das letzte Bit ist der knifflige Teil: Sie können sich vorstellen, dass das Aktivieren des Texturumbruchs in einer Richtung dazu führt, dass das System eine Textur so behandelt, als ob sie um einen Zylinder umschlossen wäre. Betrachten Sie beispielsweise das folgende Diagramm.

![Diagramm einer Textur und zweier Punkte, die um einen Zylinder umschlossen sind](images/interp2.png)

Die obige Abbildung zeigt, wie sich das Umschließen in u- Richtung auf die Interpolation von Texturkoordinaten durch das System auswirken kann. Wenn Sie die gleichen Punkte wie im Beispiel für normale oder nicht gerappte Texturen verwenden, können Sie sehen, dass sich die kürzeste Route zwischen den Punkten A und B nicht mehr in der Mitte der Textur befindet. Sie liegt nun über die Grenze, an der 0,0 und 1,0 zusammen vorhanden sind. Das Umschließen in v-Richtung ist ähnlich, mit der Ausnahme, dass die Textur um einen Zylinder umschließt wird, der auf seiner Seite liegt. Das Umschließen in U-Richtung und V-Richtung ist komplexer. In dieser Situation können Sie die Textur als Torus oder Ring vorstellen.

Die gängigste praktische Anwendung für Texturumbruch ist das Durchführen der Umgebungszuordnung. Normalerweise erscheint ein Objekt, das mit einer Umgebungskarte texturiert ist, sehr reflektierend und zeigt ein gespiegeltes Bild der Umgebung des Objekts in der Szene. Stellen Sie sich für diese Diskussion einen Raum mit vier Wänden vor, die jeweils mit dem Buchstaben R, G, B, Y und den entsprechenden Farben gestrichen sind: Rot, Grün, Blau und Gelb. Die Umgebungszuordnung für einen so einfachen Raum könnte wie in der folgenden Abbildung aussehen.

![Abbildung der vertikalen Stripesets von Rot, Grün, Blau und Gelb](images/envmap.png)

Imagine, dass die Raumobergrenze durch eine perfekt reflektierende vierseitige Säule gehalten wird. Die Zuordnung der Umgebungszuordnungstextur zur Säule ist einfach. Die Säule so aussehen zu lassen, als ob sie die Buchstaben und Farben wiederspiegelt, ist nicht so einfach. Das folgende Diagramm zeigt einen Kabelrahmen der Säule mit den entsprechenden Texturkoordinaten, die in der Nähe der oberen Scheitelungen aufgeführt sind. Die Naht, an der die Ränder der Textur umgebrochen werden, wird mit einer gepunkteten Linie angezeigt.

![Diagramm eines Rechtecks mit einer gepunkteten Linie](images/seam.png)

Bei aktivierter Umbruchrichtung in u-Richtung zeigt die texturierte Säule die Farben und Symbole aus der Umgebungskarte entsprechend an, und an der Naht am Anfang der Textur wählt der Rasterizer ordnungsgemäß die kürzeste Route zwischen den Texturkoordinaten aus, vorausgesetzt, dass die U-Koordinaten 0,0 und 1,0 dieselbe Position aufweisen. Die strukturierte Säule sieht wie in der folgenden Abbildung aus.

![Abbildung einer Säule, die aus roten, grünen, blauen und gelben Quadranten besteht](images/tex-seam.png)

Wenn Texturumbruch nicht aktiviert ist, interpoliert der Rasterizer nicht in der Richtung, die erforderlich ist, um ein lesbares, reflektiertes Bild zu generieren. Stattdessen enthält der Bereich am Anfang der Säule eine horizontal komprimierte Version der Texel zwischen den U-Koordinaten 0,175 und 0,875, während sie durch die Mitte der Textur übergeben werden. Der Wrap-Effekt wird gerümmt.

## <a name="using-texture-wrapping"></a>Verwenden von Texturumbruch

Rufen Sie zum Aktivieren des Texturumbruchs die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) auf, wie im folgenden Codebeispiel gezeigt.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



Der erste parameter, der von [**IDirect3DDevice9::SetRenderState akzeptiert**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) wird, ist ein zu setzender Renderzustand. Geben Sie einen der aufzählten \_ D3DRS WRAP0 bis D3DRS WRAP7-Werte an, die angeben, für welche Texturebene der Umbruch \_ festgelegt werden soll. Geben Sie die Flags D3DWRAPCOORD 0 bis \_ D3DWRAPCOORD 3 im zweiten Parameter an, um das Texturumbruch in der entsprechenden Richtung zu aktivieren, oder kombinieren Sie sie, um das Umschließen in mehrere Richtungen zu \_ aktivieren. Wenn Sie ein Flag weglassen, wird der Texturumbruch in der entsprechenden Richtung deaktiviert. Legen Sie den Wert für den entsprechenden Renderzustand auf 0 fest, um den Texturumbruch für einen Satz von Texturkoordinaten zu deaktivieren.

Verwechseln Sie Texturumbruch nicht mit den ähnlich benannten Textur-Adressierungsmodi. Texturumbruch wird vor der Textur adressierung ausgeführt. Stellen Sie sicher, dass die Texturumbruchdaten keine Texturkoordinaten außerhalb des Bereichs \[ von 0,0, 1,0 enthalten, da dies zu nicht definierten \] Ergebnissen führt. Weitere Informationen zur Textur adressierung finden Sie unter [Texture Addressing Modes (Direct3D 9) (Textur adressierungsmodi (Direct3D 9)).](texture-addressing-modes.md)

## <a name="displacement-map-wrapping"></a>Umschließen von Verschiebungszuordnungen

Verschiebungszuordnungen werden von der Mosaik-Engine interpoliert. Da der Wrap-Modus für die Mosaik-Engine nicht angegeben werden kann, kann texture wrapping nicht mit Verschiebungszuordnungen durchgeführt werden. Eine Anwendung kann eine Reihe von Scheitelzeichen verwenden, die erzwingt, dass die Interpolation in beliebiger Richtung umschließt. Die Anwendung kann auch die Interpolation angeben, die als einfache lineare Interpolation erfolgen soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
