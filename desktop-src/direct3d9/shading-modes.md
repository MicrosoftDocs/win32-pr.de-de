---
description: Der Schattierungsmodus, der zum Rendern eines Polygons verwendet wird, wirkt sich auf seine Darstellung aus. Schattierungsmodi bestimmen die Intensität von Farbe und Beleuchtung an jedem Punkt eines Polygongesichts. Direct3D unterstützt zwei Schattierungsmodi.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Schattierungsmodi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714e9610e1cae344148bf78ef39bc5e8355cb2af6395e3f92a3bc01b87860605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092227"
---
# <a name="shading-modes-direct3d-9"></a>Schattierungsmodi (Direct3D 9)

Der Schattierungsmodus, der zum Rendern eines Polygons verwendet wird, wirkt sich auf seine Darstellung aus. Schattierungsmodi bestimmen die Intensität von Farbe und Beleuchtung an jedem Punkt eines Polygongesichts. Direct3D unterstützt zwei Schattierungsmodi.

-   [Flache Schattierung](#flat-shading)
-   [Gouraud Shading](#gouraud-shading)

## <a name="flat-shading"></a>Flache Schattierung

Im flachen Schattierungsmodus rendert die Direct3D-Renderingpipeline ein Polygon, indem die Farbe des Polygonmaterials am ersten Scheitelpunkt als Farbe für das gesamte Polygon verwendet wird. 3D-Objekte, die mit flacher Schattierung gerendert werden, haben sichtbar spitze Kanten zwischen Polygonen, wenn sie nicht koplanar sind.

Die folgende Abbildung zeigt eine Teekanne, die mit flacher Schattierung gerendert wird. Die Kontur der einzelnen Polygone ist deutlich sichtbar. Flache Schattierung ist die schnellste Form der Schattierung.

![Abbildung einer Teekanne mit flacher Schattierung](images/flattea.png)

## <a name="gouraud-shading"></a>Gouraud Shading

Wenn Direct3D ein Polygon mit Gouraud-Schattierung rendert, berechnet es eine Farbe für jeden Scheitelpunkt unter Verwendung der Normal- und Beleuchtungsparameter des Scheitelpunkts. Anschließend interpoliert sie die Farbe über das Gesicht der Polygone. Die Interpolation erfolgt linear. Wenn beispielsweise die rote Komponente der Farbe von Scheitelpunkt 1 0,8 und die rote Komponente von Scheitelpunkt 2 mit dem Gouraud-Schattierungsmodus und dem RGB-Farbmodell 0,8 ist, weist das Direct3D-Beleuchtungsmodul dem Pixel am Mittelpunkt der Linie zwischen diesen Scheitelpunkten eine rote Komponente von 0,6 zu.

Die folgende Abbildung veranschaulicht die Gouraud-Schattierung. Dieser Teepot besteht aus vielen flachen, dreieckigen Polygonen. Die Gouraud-Schattierung sorgt jedoch dafür, dass die Oberfläche des Objekts gekrümmt und glättt.

![Abbildung der Teekanne mit Gouraud-Schattierung](images/gourtea.png)

Gouraud-Schattierung kann auch verwendet werden, um Objekte mit spitzen Kanten anzuzeigen.

Weitere Informationen finden Sie unter [Normale Vektoren für Gesichtserkennung und Scheitelpunkt (Direct3D 9).](face-and-vertex-normal-vectors.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schattierung](shading.md)
</dt> </dl>

 

 



