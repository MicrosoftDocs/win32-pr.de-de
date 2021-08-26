---
description: 'Kurz gesagt: Texturumbruch ändert die grundlegende Art und Weise, wie Direct3D texturierte Polygone mithilfe der für jeden Scheitelpunkt angegebenen Texturkoordinaten rastert.'
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

Kurz gesagt: Texturumbruch ändert die grundlegende Art und Weise, wie Direct3D texturierte Polygone mithilfe der für jeden Scheitelpunkt angegebenen Texturkoordinaten rastert. Beim Rastern eines Polygons interpoliert das System zwischen den Texturkoordinaten an jedem der Scheitelpunkte des Polygons, um die Texel zu bestimmen, die für jedes Pixel des Polygons verwendet werden sollen. Normalerweise behandelt das System die Textur als 2D-Ebene und interpoliert neue Texel, indem die kürzeste Route von Punkt A innerhalb einer Textur zu Punkt B genommen wird. Wenn Punkt A die Position u, v (0,8, 0,1) darstellt und Punkt B bei (0,1,0,1) ist, sieht die Interpolationslinie wie im folgenden Diagramm aus.

![Diagramm einer Interpolationslinie zwischen zwei Punkten](images/interp1.png)

Beachten Sie, dass die kürzeste Entfernung zwischen A und B in dieser Abbildung ungefähr durch die Mitte der Textur verläuft. Durch das Aktivieren von U-Textur- oder V-Texturkoordinatenumbrüchen ändert sich, wie Direct3D die kürzeste Route zwischen Texturkoordinaten in u- und v-Richtung wahrnimmt. Definitionsgemäß führt textur wrapping dazu, dass der Rasterizer die kürzeste Route zwischen Texturkoordinatensätzen nimmt, vorausgesetzt, dass 0,0 und 1,0 zufällig sind. Das letzte Bit ist der schwierige Teil: Sie können sich vorstellen, dass die Aktivierung der Texturumbruch in eine Richtung dazu führt, dass das System eine Textur so behandelt, als wäre sie um einen Zylinder umschlossen. Betrachten Sie beispielsweise das folgende Diagramm.

![Diagramm einer Textur und zwei Punkte, die um einen Zylinder umschlossen sind](images/interp2.png)

Die obige Abbildung zeigt, wie sich das Umschließen in der u-Richtung darauf auswirkt, wie das System Texturkoordinaten interpoliert. Wenn Sie die gleichen Punkte wie im Beispiel für normale oder nicht umschlossene Texturen verwenden, können Sie sehen, dass sich die kürzeste Route zwischen den Punkten A und B nicht mehr über die Mitte der Textur befindet. sie liegt nun über dem Rahmen, in dem 0.0 und 1.0 zusammen vorhanden sind. Das Umschließen in der V-Richtung ist ähnlich, mit der Ausnahme, dass die Textur um einen Zylinder umbrochen wird, der auf seiner Seite steht. Das Umschließen in u- und v-Richtung ist komplexer. In dieser Situation können Sie sich die Textur als Torus oder Ring vorstellen.

Die gängigste praktische Anwendung für Texturumbrüche ist die Durchführung der Umgebungszuordnung. Normalerweise erscheint ein Objekt, das mit einer Umgebungskarte strukturiert ist, sehr reflektierend und zeigt ein gespiegeltes Bild der Umgebung des Objekts in der Szene. Stellen Sie sich für diese Diskussion einen Raum mit vier Wänden vor, die jeweils mit den Buchstaben R, G, B, Y und den entsprechenden Farben gezeichnet wurden: Rot, Grün, Blau und Gelb. Die Umgebungskarte für einen so einfachen Raum könnte wie in der folgenden Abbildung aussehen.

![Abbildung der vertikalen Rot-, Grün-, Blau- und Gelbstreifen](images/envmap.png)

Imagine, dass die Raumobergrenze von einer perfekt reflektierenden, vierseitigen Säule gehalten wird. Das Zuordnen der Umgebungszuordnungstextur zur Säule ist einfach. die Säulen so aussehen zu lassen, als ob sie die Buchstaben und Farben widerspiegelt, ist nicht so einfach. Das folgende Diagramm zeigt einen Kabelrahmen der Säule mit den entsprechenden Texturkoordinaten, die in der Nähe der oberen Scheitelpunkte aufgeführt sind. Die Naht, bei der wrapping die Ränder der Textur überschreitet, wird mit einer gepunkteten Linie angezeigt.

![Diagramm eines Rechtecks mit einer gepunkteten Linie](images/seam.png)

Wenn wrapping in u-Richtung aktiviert ist, zeigt die texturierte Säule die Farben und Symbole aus der Umgebungskarte entsprechend an, und an der Naht am Anfang der Textur wählt der Rasterizer ordnungsgemäß die kürzeste Route zwischen den Texturkoordinaten aus, vorausgesetzt, die U-Koordinaten 0,0 und 1,0 teilen sich die gleiche Position. Die strukturierte Säule sieht wie in der folgenden Abbildung aus.

![Abbildung einer Säule, die aus roten, grünen, blauen und gelben Quadranten besteht](images/tex-seam.png)

Wenn textur wrapping nicht aktiviert ist, interpoliert der Rasterizer nicht in der Richtung, die erforderlich ist, um ein lesbares, reflektiertes Bild zu generieren. Stattdessen enthält der Bereich am Anfang der Säule eine horizontal komprimierte Version der Texel zwischen den U-Koordinaten 0,175 und 0,875, während sie die Mitte der Textur durchlaufen. Der Wrap-Effekt wird umbrochen.

## <a name="using-texture-wrapping"></a>Verwenden von Texturumbrüchen

Um textur wrapping zu aktivieren, rufen Sie die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) auf, wie im folgenden Codebeispiel gezeigt.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



Der erste von [**IDirect3DDevice9::SetRenderState akzeptierte**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) Parameter ist ein festzulegender Renderzustand. Geben Sie einen der D3DRS \_ WRAP0 bis D3DRS \_ WRAP7-Enumerationswerte an, die angeben, für welche Texturebene der Wrapping festgelegt werden soll. Geben Sie die Flags D3DWRAPCOORD \_ 0 bis D3DWRAPCOORD \_ 3 im zweiten Parameter an, um textur wrapping in der entsprechenden Richtung zu aktivieren, oder kombinieren Sie sie, um das Umschließen in mehrere Richtungen zu aktivieren. Wenn Sie ein Flag weglassen, ist das Texturumbruch in der entsprechenden Richtung deaktiviert. Um textur wrapping für eine Reihe von Texturkoordinaten zu deaktivieren, legen Sie den Wert für den entsprechenden Renderzustand auf 0 fest.

Verwechseln Sie textur wrapping nicht mit den ähnlich benannten Texturadressierungsmodi. Texturumbrüche werden vor der Texturadressierung durchgeführt. Stellen Sie sicher, dass die Texturumbruchdaten keine Texturkoordinaten außerhalb des Bereichs von \[ 0,0, 1,0 enthalten, \] da dies zu nicht definierten Ergebnissen führt. Weitere Informationen zur Texturadressierung finden Sie unter [Texturadressierungsmodi (Direct3D 9).](texture-addressing-modes.md)

## <a name="displacement-map-wrapping"></a>Umschließen von Verschiebungszuordnungen

Verschiebungszuordnungen werden von der Mosaik-Engine interpoliert. Da der Umbruchmodus für die Mosaik-Engine nicht angegeben werden kann, kann die Texturumbruchfunktion nicht mit Verschiebungszuordnungen durchgeführt werden. Eine Anwendung kann einen Satz von Scheitelpunkten verwenden, die die Interpolation zwingt, in beliebige Richtungen zu umschließen. Die Anwendung kann auch die Interpolation angeben, die als einfache lineare Interpolation erfolgen soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
