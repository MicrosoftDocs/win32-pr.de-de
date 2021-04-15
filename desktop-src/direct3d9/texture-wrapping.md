---
description: Kurz gesagt, die Textur Umbrüchen ändert die grundlegende Methode, mit der Direct3D strukturierte Polygone mithilfe der für die einzelnen Scheitel Punkte angegebenen Texturkoordinaten rasteriert.
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Textur Wrapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7c0f8cb6d7793536999d5f3df128849572d3dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521419"
---
# <a name="texture-wrapping-direct3d-9"></a>Textur Wrapping (Direct3D 9)

Kurz gesagt, die Textur Umbrüchen ändert die grundlegende Methode, mit der Direct3D strukturierte Polygone mithilfe der für die einzelnen Scheitel Punkte angegebenen Texturkoordinaten rasteriert. Während der rasterisierung eines Polygons interpoliert das System zwischen den Texturkoordinaten an jedem der Scheitel Punkte des Polygons, um die texeln zu ermitteln, die für jedes Pixel des Polygons verwendet werden sollen. Normalerweise behandelt das System die Textur als 2D-Ebene und interpolieren neue texeln durch die kürzeste Route von Punkt a innerhalb einer Textur zu Punkt B. Wenn Punkt A die u, v-Position (0,8, 0,1) und Punkt B bei (0,1, 0,1) darstellt, sieht die Interpolations Linie wie im folgenden Diagramm aus.

![Diagramm einer interinterpolations Linie zwischen zwei Punkten](images/interp1.png)

Beachten Sie, dass die kürzeste Entfernung zwischen A und B in dieser Abbildung ungefähr durch die Mitte der Textur verläuft. Durch das Aktivieren der u-Textur oder der v-Texture-Koordinate werden Änderungen geändert, wie Direct3D die kürzeste Route zwischen den Texturkoordinaten in der u-Richtung und der v-Richtung wahrnimmt. Definitionsgemäß bewirkt, dass der Raster die kürzeste Route zwischen Texturkoordinaten Sätzen annimmt, wobei angenommen wird, dass 0,0 und 1,0 Coincident sind. Das letzte Bit ist der schwierige Teil: Sie können sich vorstellen, dass das Aktivieren von Textur Umbrüchen in einer Richtung bewirkt, dass das System eine Textur behandelt, als ob es sich um einen Zylinder umschließt. Betrachten Sie beispielsweise das folgende Diagramm.

![Diagramm einer Textur und zwei Punkte, die um einen Zylinder umschlossen sind](images/interp2.png)

In der obigen Abbildung wird gezeigt, wie die Umbrüchen in der u-Richtung beeinflussen, wie Texturkoordinaten vom System interpoliert werden. Wenn Sie dieselben Punkte wie im Beispiel für normale oder nicht umschließende Texturen verwenden, sehen Sie, dass die kürzeste Route zwischen den Punkten A und B nicht mehr in der Mitte der Textur liegt. Sie befindet sich jetzt über dem Rahmen, in dem 0,0 und 1,0 nebeneinander vorhanden sind. Das umschließen in die v-Richtung ist ähnlich, außer dass es die Textur um einen Zylinder umschließt, der auf seiner Seite liegt. Das Umwickeln von u-Richtung und v-Richtung ist komplexer. In diesem Fall können Sie die Textur als ein-oder Ring Diagramm umsehen.

Die häufigste praktische Anwendung für Textur Wrapping ist das Durchführen einer Umgebungs Zuordnung. Normalerweise wird ein Objekt, das mit einer Umgebungs Zuordnung strukturiert ist, sehr reflektiert und zeigt ein gespiegeltes Bild der Umgebung des Objekts in der Szene. Im Rahmen dieser Erläuterung wird ein Raum mit vier Wänden angezeigt, von denen jeder mit dem Buchstaben R, G, B, Y und den entsprechenden Farben gezeichnet wurde: rot, grün, blau und gelb. Die Umgebungs Zuordnung für einen solchen einfachen Raum könnte wie in der folgenden Abbildung aussehen.

![Darstellung vertikaler Streifen von rot, grün, blau und gelb](images/envmap.png)

Stellen Sie sich vor, dass die Obergrenze des Raums von einer vollständig reflektierenden, vierseitigen Säule gehalten wird. Die Zuordnung der Umgebungs Struktur zum Säulen Schema ist einfach. Es ist nicht so einfach, die Säule so zu gestalten, als ob die Buchstaben und Farben reflektiert werden. Das folgende Diagramm zeigt einen Drahtrahmen der Säule mit den anwendbaren Texturkoordinaten, die in der Nähe der oberen Vertices aufgeführt sind. Die Naht, in der die Ränder der Textur überschreiten, wird mit einer gepunkteten Linie angezeigt.

![Diagramm eines Rechtecks mit einer ich-gepunkteten Linie](images/seam.png)

Wenn Wrapping in der u-Richtung aktiviert ist, zeigt die strukturierte Säule die Farben und Symbole aus der Umgebungs Zuordnung entsprechend an. bei der Ausrichtung am Anfang der Textur wählt der Raster ordnungsgemäß die kürzeste Route zwischen den Texturkoordinaten aus, vorausgesetzt, dass die u-Koordinaten 0,0 und 1,0 denselben Speicherort aufweisen. Die strukturierte Säule sieht in etwa wie in der folgenden Abbildung aus.

![Abbildung einer Säule, die aus roten, grünen, blauen und gelben Quadranten besteht](images/tex-seam.png)

Wenn Textur Wrapping nicht aktiviert ist, Interpolieren die Raster nicht in der Richtung, die zum Generieren eines glaubwürdigen, reflektierten Bilds erforderlich ist. Stattdessen enthält der Bereich am Anfang der Säule eine horizontal komprimierte Version der texeln zwischen u-Koordinaten 0,175 und 0,875, während Sie den Mittelpunkt der Textur durchlaufen. Der Umbruch Effekt ist zerstört.

## <a name="using-texture-wrapping"></a>Verwenden von Textur Wrapping

Um das Textur Wrapping zu aktivieren, nennen Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode, wie im folgenden Codebeispiel gezeigt.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



Der erste Parameter, der von [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) akzeptiert wird, ist ein zu fest gelegender renderzustand. Geben Sie einen der D3DRS- \_ WRAP0 bis D3DRS \_ WRAP7-Enumerationswerte an, die angeben, für welche Textur Ebene das Wrapping festgelegt werden soll. Geben Sie die D3DWRAPCOORD \_ 0 bis D3DWRAPCOORD \_ 3 Flags im zweiten Parameter an, um die textur umschließen in die entsprechende Richtung zu aktivieren, oder kombinieren Sie Sie, um das umschließen in mehrere Richtungen zu ermöglichen Wenn Sie ein Flag weglassen, wird die Textur Umbrüchen in der entsprechenden Richtung deaktiviert. Legen Sie den Wert für den entsprechenden Rendering-Zustand auf 0 fest, um das Textur umwickeln für einen Satz von Texturkoordinaten zu deaktivieren.

Verwechseln Sie die Textur Umbrüchen nicht mit den ähnlich benannten Textur Adressierungs Modi. Das Textur umwickeln erfolgt vor der Textur Adressierung. Stellen Sie sicher, dass die Textur Wrapping Daten keine Texturkoordinaten außerhalb des Bereichs von \[ 0,0, 1,0 enthalten \] , da dadurch nicht definierte Ergebnisse erzeugt werden. Weitere Informationen zur Textur Adressierung finden Sie unter [Textur Adressierungs Modi (Direct3D 9)](texture-addressing-modes.md).

## <a name="displacement-map-wrapping"></a>Umwickeln von Verschiebungs

Verschiebungs Zuordnungen werden von der Tesselations-Engine interpoliert. Da der Umbruch Modus für die Mosaik-Engine nicht angegeben werden kann, kann die Textur Umbrüche nicht mit Verschiebungs Zuordnungen ausgeführt werden. Eine Anwendung kann eine Reihe von Vertices verwenden, die erzwingen, dass die Interpolations in eine beliebige Richtung eingebunden wird. Die Anwendung kann auch die Interpolationen angeben, die als einfache lineare Interpolationen durchgeführt werden sollen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
