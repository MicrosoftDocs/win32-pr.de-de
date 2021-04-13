---
description: Jedes Gesicht in einem Mesh weist einen senkrechten Einheits Vektor auf, wie in der folgenden Abbildung dargestellt.
ms.assetid: 86e2a460-7b58-4612-8f72-5a4e864ceb58
title: Gesicht-und Scheitelpunkt normale Vektoren (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0ef6fd8eba85b770cbfe71477655ddbafd8ee7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559383"
---
# <a name="face-and-vertex-normal-vectors-direct3d-9"></a>Gesicht-und Scheitelpunkt normale Vektoren (Direct3D 9)

Jedes Gesicht in einem Mesh weist einen senkrechten Einheits Vektor auf, wie in der folgenden Abbildung dargestellt. Die Richtung des Vektors wird durch die Reihenfolge bestimmt, in der die Scheitel Punkte definiert werden, und durch die Festlegung, ob das Koordinatensystem von rechts oder Links übergeben wird. Der Vordergrund zeigt sich von der Vorderseite der Vorderseite Weg. In Direct3D ist nur der Vordergrund einer Fläche sichtbar. Eine Vorderseite ist eine, in der Scheitel Punkte im Uhrzeigersinn definiert werden.

![Abbildung eines normalen Vektors für eine Vorderseite](images/nrmlvect.png)

Jedes Gesicht, das kein Vordergrund ist, ist ein Hintergrund. Direct3D gibt nicht immer wieder Gesichter zurück. Daher werden die Hinterflächen als "culled" bezeichnet. Wenn Sie möchten, können Sie den Modus ändern, um die Gesichter zu rendereln. Weitere Informationen finden Sie unter [culck State (Direct3D 9)](culling-state.md) .

Direct3D verwendet die Vertex-Einheits normale für die Schattierung, Beleuchtung und Texturierung von Gouraud. Die folgende Abbildung zeigt Beispiel normale.

![Abbildung von Scheitelpunkt normalen](images/vertnrml.png)

Beim Anwenden von Gouraud-Schattierung auf ein Polygon verwendet Direct3D die Scheitelpunkt normale, um den Winkel zwischen der Lichtquelle und der Oberfläche zu berechnen. Sie berechnet die Farb-und Intensitätswerte für die Scheitel Punkte und interpoliert Sie für jeden Punkt in allen primitiven Oberflächen. Direct3D berechnet den Wert für die helle Intensität mithilfe des Winkels. Je größer der Winkel ist, desto weniger hell wird auf der Oberfläche angezeigt.

Wenn Sie ein Objekt erstellen, das flach ist, legen Sie die vertexnormale so fest, dass Sie auf die Oberfläche, wie in der folgenden Abbildung gezeigt, auf die Oberfläche zeigen.

![Abbildung einer flachen Oberfläche, die aus zwei Dreiecken mit Scheitelpunkt normalen besteht](images/flatvert.png)

Es ist jedoch wahrscheinlicher, dass das Objekt aus Dreiecks Streifen besteht und die Dreiecke nicht Coplanar sind. Eine einfache Möglichkeit, eine nahtlose Schattierung über alle Dreiecke des Streifens hinweg zu erreichen, besteht darin, zuerst den Oberflächen normal Vektor für jedes polygonale Gesicht zu berechnen, dem der Scheitelpunkt zugeordnet ist. Der Scheitelpunkt normal kann so festgelegt werden, dass er für jede Oberflächen normale den gleichen Winkel hat. Diese Methode ist jedoch möglicherweise nicht effizient genug für komplexe primitive.

Diese Methode wird anhand des folgenden Diagramms veranschaulicht, das zwei Oberflächen anzeigt: S1 und S2: Edge-on von oben. Die normalen Vektoren für S1 und S2 sind blau dargestellt. Der Vertex-normal Vektor wird rot dargestellt. Der Winkel, den der normal Vektor des Scheitel Punkts mit der Oberflächen Norm S1 herstellt, ist derselbe wie der Winkel zwischen der Scheitelpunkt-normal und der Oberflächen Norm von S2. Wenn diese beiden Oberflächen mit der Gouraud-Schattierung beleuchtet und schattiert werden, ist das Ergebnis ein reibungslos schattierter, nahtlos Abgerundeter Rand zwischen Ihnen.

![Diagramm von zwei Oberflächen (S1 und S2) und ihren normalen Vektoren und Scheitelpunkt normal Vektor](images/gvert.png)

Wenn sich der Scheitelpunkt normal zu einem der Gesichter bewegt, mit denen er verknüpft ist, bewirkt dies, dass die helle Intensität für Punkte auf dieser Oberfläche vergrößert oder verringert wird, je nachdem, wie sich die Lichtquelle ergibt. Das folgende Diagramm zeigt ein Beispiel. Diese Oberflächen werden auch in Edge-on angezeigt. Der Scheitelpunkt normal ist in Richtung S1 und bewirkt, dass er einen kleineren Winkel mit der Lichtquelle hat, als wenn der Scheitelpunkt normal mit den Oberflächen Normals gleich groß ist.

![Diagramm von zwei Oberflächen (S1 und S2) mit einem Vertex-normal Vektor, der sich auf ein Gesicht bewegt](images/gvert2.png)

Mithilfe von Gouraud-Schattierung können Sie einige Objekte in einer 3D-Szene mit Spitzen Kanten anzeigen. Zu diesem Zweck duplizieren Sie die Scheitel Punkte des Scheitel Punkts bei jeder Schnittmenge, bei der ein starker Rand erforderlich ist, wie in der folgenden Abbildung dargestellt.

![Abbildung der doppelten Vertex-normal Vektoren bei Spitzen Rändern](images/shade1.png)

Wenn Sie die drawprimitive-Methoden zum renderingihrer Szene verwenden, definieren Sie das Objekt mit Spitzen Rändern als Dreiecks Liste und nicht als Dreiecks Streifen. Wenn Sie ein Objekt als Dreiecks Streifen definieren, behandelt Direct3D es als ein einzelnes Polygon, das aus mehreren dreieckigen Flächen besteht. Die Schattierung von Gouraud wird sowohl über jedes Gesicht des Polygons als auch zwischen angrenzenden Gesichtern angewendet. Das Ergebnis ist ein Objekt, das nahtlos von Gesicht zu Gesicht schattiert wird. Da eine Dreiecks Liste ein Polygon ist, das aus einer Reihe nicht zusammenhängender Dreiecks Flächen besteht, wendet Direct3D die Gouraud-Schattierung auf jedes Gesicht des Polygons an. Sie wird jedoch nicht von Gesicht zu Gesicht angewendet. Wenn zwei oder mehr Dreiecke einer Dreiecks Liste nebeneinander liegen, scheinen Sie einen Spitzen Rand dazwischen zu haben.

Eine andere Alternative besteht darin, beim Rendern von Objekten mit Spitzen Kanten zu einer flachen Schattierung zu wechseln. Dies ist rechnerisch die effizienteste Methode, kann jedoch zu Objekten in der Szene führen, die nicht so realistisch gerendert werden wie die Objekte, bei denen es sich um eine Gouraud-Schattierung handelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



