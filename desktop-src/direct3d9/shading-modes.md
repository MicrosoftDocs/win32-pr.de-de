---
description: Der Schattierungs Modus zum rendieren eines Polygons hat eine Tiefe Auswirkung auf seine Darstellung. Mit den Schattierungs Modi wird die Intensität der Farbe und der Beleuchtung an einem beliebigen Punkt auf einer Polygon Seite festgelegt. Direct3D unterstützt zwei Schattierungs Modi.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Schattierungs Modi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564619"
---
# <a name="shading-modes-direct3d-9"></a>Schattierungs Modi (Direct3D 9)

Der Schattierungs Modus zum rendieren eines Polygons hat eine Tiefe Auswirkung auf seine Darstellung. Mit den Schattierungs Modi wird die Intensität der Farbe und der Beleuchtung an einem beliebigen Punkt auf einer Polygon Seite festgelegt. Direct3D unterstützt zwei Schattierungs Modi.

-   [Flatschattierung](#flat-shading)
-   [Gouraud-Schattierung](#gouraud-shading)

## <a name="flat-shading"></a>Flatschattierung

Im Flatshading-Modus rendert die Direct3D-Renderingpipeline ein Polygon und verwendet dabei die Farbe des Polygon Materials im ersten Scheitelpunkt als Farbe für das gesamte Polygon. 3D-Objekte, die mit flacher Schattierung gerendert werden, haben sichtbare Kanten zwischen Polygonen, wenn Sie nicht Coplanar sind.

Die folgende Abbildung zeigt eine mit flacher Schattierung gerenderte Teekanne. Die Gliederung der einzelnen Polygon ist eindeutig sichtbar. Die flache Schattierung ist die schnellste Form der Schattierung.

![Darstellung eines Teekanne mit flacher Schattierung](images/flattea.png)

## <a name="gouraud-shading"></a>Gouraud-Schattierung

Wenn Direct3D ein Polygon mithilfe von Gouraud-Schattierung rendert, wird für jeden Scheitelpunkt eine Farbe berechnet, indem der Scheitelpunkt normale und Beleuchtungs Parameter verwendet werden. Dann interpoliert Sie die Farbe auf der Vorderseite der Polygone, die die Interpolation linear durchführt. Wenn z. b. die rote Komponente der Farbe von Vertex 1 0,8 und die rote Komponente von Vertex 2 0,4 ist, wenn der Modus "Gouraud-Schattierung" und das RGB-Farbmodell verwendet werden, weist das Direct3D-Beleuchtungs Modul dem Pixel in der Mitte der Linie zwischen diesen Scheitel Punkten eine rote Komponente von 0,6 zu.

In der folgenden Abbildung wird die Schattierung von Gouraud veranschaulicht. Diese Teekanne besteht aus vielen flachen, dreieckigen Polygonen. Allerdings wird durch die Schattierung von Gouraud die Oberfläche des Objekts gekrümmert und glatt angezeigt.

![Abbildung von "Teekanne" mithilfe von "Gouraud-Schattierung"](images/gourtea.png)

Mithilfe von Gouraud-Schattierung können auch Objekte mit Spitzen Kanten angezeigt werden.

Weitere Informationen finden Sie unter [Gesichts-und Scheitel Punkte (normale Vektoren) (Direct3D 9)](face-and-vertex-normal-vectors.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schattierung](shading.md)
</dt> </dl>

 

 



