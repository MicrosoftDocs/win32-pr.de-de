---
description: Der Teil von Direct3D, der die Geometrie durch die Geometriepipeline der festen Funktion pusht, ist die Transformations-Engine.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5570562c02f2283b869bbb5e60143ed4badac94eb10651b002a89aedf1cd60f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519702"
---
# <a name="transforms-direct3d-9"></a>Transformationen (Direct3D 9)

Der Teil von Direct3D, der die Geometrie durch die Geometriepipeline der festen Funktion pusht, ist die Transformations-Engine. Es sucht das Modell und den Viewer in der Welt, projektet Scheiteltices für die Anzeige auf dem Bildschirm und clipt Scheiteltices zum Viewport. Die Transformations-Engine führt auch Beleuchtungsberechnungen durch, um diffuse und specular-Komponenten an jedem Scheitelpunkt zu bestimmen.

Die Geometriepipeline nimmt Scheitelungen als Eingabe an. Die Transformations-Engine wendet die Welt-, Ansichts- und Projektionstransformationen auf die Scheitelungen an, schneide das Ergebnis aus und übergibt alles an den Rasterizer.

Am Anfang der Pipeline werden die Scheitelungen eines Modells relativ zu einem lokalen Koordinatensystem deklariert. Dies ist ein lokaler Ursprung und eine Ausrichtung. Diese Ausrichtung von Koordinaten wird häufig als Modellraum bezeichnet, und einzelne Koordinaten werden als Modellkoordinaten bezeichnet.

In der ersten Phase der Geometriepipeline werden die Scheitelungen eines Modells aus dem lokalen Koordinatensystem in ein Koordinatensystem transformiert, das von allen Objekten in einer Szene verwendet wird. Der Prozess der Neuorganisation der Scheitelungen wird als Welttransformation bezeichnet. Diese neue Ausrichtung wird häufig als Weltraum bezeichnet, und jeder Scheitelpunkt im Weltraum wird mithilfe von Weltkoordinaten deklariert.

In der nächsten Phase sind die Scheitelungen, die Ihre 3D-Welt beschreiben, in Bezug auf eine Kamera ausgerichtet. Das heißt, Ihre Anwendung wählt einen Standpunkt für die Szene aus, und Raumkoordinaten werden verschoben und um die Kameraansicht gedreht, was den Raum in den Kameraraum umdreht. Dies ist die Ansichtstransformation.

Die nächste Phase ist die Projektionstransformation. In diesem Teil der Pipeline werden Objekte in der Regel in Relation zu ihrer Entfernung vom Betrachter skaliert, um einer Szene die Schärfe der Tiefe zu geben. Close-Objekte werden so gemacht, dass sie größer als entfernte Objekte sind, und so weiter. Der Einfachheit halber bezieht sich diese Dokumentation auf den Raum, in dem Scheitelräume nach der Projektionstransformation als Projektionsraum vorhanden sind. Einige Grafikbücher verweisen möglicherweise auf Projektionsraum als postperspektiven homogenen Raum. Nicht alle Projektionstransformationen skalieren die Größe von Objekten in einer Szene. Eine Projektion wie diese wird manchmal als affine oder orthogonale Projektion bezeichnet.

Im letzten Teil der Pipeline werden alle Scheitelungen entfernt, die auf dem Bildschirm nicht sichtbar sind, sodass sich der Rasterizer nicht die Zeit nimmt, die Farben und Schattierung für etwas zu berechnen, das nie angezeigt wird. Dieser Prozess wird als Clipping bezeichnet. Nach dem Clipping werden die verbleibenden Scheitelungen gemäß den Viewportparametern skaliert und in Bildschirmkoordinaten konvertiert. Die resultierenden Scheitelungen, die beim Rastern der Szene auf dem Bildschirm angezeigt werden, sind im Bildschirmbereich vorhanden.

Transformationen werden verwendet, um die Objektgeometrie von einem Koordinatenraum in einen anderen zu konvertieren. Direct3D verwendet Matrizen, um 3D-Transformationen durchzuführen. In diesem Abschnitt wird erläutert, wie Matrizen 3D-Transformationen erstellen. Außerdem werden einige häufige Verwendungsmöglichkeiten für Transformationen beschrieben. Außerdem wird erläutert, wie Sie Matrizen kombinieren können, um eine einzelne Matrix zu erzeugen, die mehrere Transformationen umfasst.

-   [World Transform (Direct3D 9):](world-transform.md) Konvertieren aus dem Modellraum in den Weltraum
-   [Ansichtstransformation (Direct3D 9):](view-transform.md) Konvertieren aus dem Raum in den Ansichtsraum
-   [Projektionstransformation (Direct3D 9):](projection-transform.md) Konvertieren vom Ansichtsraum in den Projektionsraum

## <a name="matrix-transforms"></a>Matrixtransformationen

In Anwendungen, die mit 3D-Grafiken arbeiten, können Sie geometrische Transformationen verwenden, um Folgendes zu tun:

-   Geben Sie die Position eines Objekts relativ zu einem anderen Objekt an.
-   Drehen und Größe von Objekten.
-   Ändern von Ansichtspositionen, Wegbeschreibungen und Perspektiven.

Sie können einen beliebigen Punkt (x,y,z) in einen anderen Punkt (x', y', z') transformieren, indem Sie eine 4x4-Matrix verwenden, wie in der folgenden Gleichung gezeigt.

![Gleichung der Transformation eines beliebigen Punkts in einen anderen Punkt](images/matmult.png)

Führen Sie die folgenden Gleichungen für (x, y, z) und die Matrix aus, um den Punkt (x', y', z') zu erzeugen.

![Gleichungen für den neuen Punkt](images/matexpnd.png)

Die gängigsten Transformationen sind Übersetzung, Drehung und Skalierung. Sie können die Matrizen, die diese Effekte erzeugen, zu einer einzelnen Matrix kombinieren, um mehrere Transformationen gleichzeitig zu berechnen. Beispielsweise können Sie eine einzelne Matrix erstellen, um eine Reihe von Punkten zu übersetzen und zu drehen.

Matrizen werden in Zeilenspaltenreihen reihenfolge geschrieben. Eine Matrix, die Scheitelzeichen gleichmäßig entlang jeder Achse skaliert, die als einheitliche Skalierung bezeichnet wird, wird durch die folgende Matrix mit mathematischer Notation dargestellt.

![Gleichung einer Matrix für einheitliche Skalierung](images/matrix.png)

In C++ deklariert Direct3D Matrizen mithilfe der [**D3DMATRIX-Struktur als zweidimensionales**](d3dmatrix.md) Array. Das folgende Beispiel zeigt, wie eine **D3DMATRIX-Struktur** initialisiert wird, um als einheitliche Skalierungsmatrix zu fungieren.


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a>Translate

Die folgende Gleichung übersetzt den Punkt (x, y, z) in einen neuen Punkt (x', y', z').

![Gleichung einer Übersetzungsmatrix für einen neuen Punkt](images/transl8.png)

Sie können manuell eine Übersetzungsmatrix in C++ erstellen. Das folgende Beispiel zeigt den Quellcode für eine Funktion, die eine Matrix zum Übersetzen von Scheitelungen erstellt.


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



Der Einfachheit halber stellt die D3DX-Hilfsprogrammbibliothek die [**D3DXMatrixTranslation-Funktion**](d3dxmatrixtranslation.md) zur Verfügung.

## <a name="scale"></a>Skalieren

Die folgende Gleichung skaliert den Punkt (x, y, z) um beliebige Werte in der x-, y- und z-Richtung auf einen neuen Punkt (x', y', z').

![Gleichung einer Skalierungsmatrix für einen neuen Punkt](images/matscale.png)

## <a name="rotate"></a>Rotate

Die hier beschriebenen Transformationen gelten für linkshändige Koordinatensysteme und können sich daher von Transformationsmatrizen unterscheiden, die Sie an anderer Stelle gesehen haben.

Die folgende Gleichung dreht den Punkt (x, y, z) um die X-Achse und erzeugt einen neuen Punkt (x', y', z').

![Gleichung einer X-Drehungsmatrix für einen neuen Punkt](images/matxrot.png)

Mit der folgenden Gleichung wird der Punkt um die y-Achse gedreht.

![Gleichung einer y-Rotationsmatrix für einen neuen Punkt](images/matyrot.png)

Die folgende Gleichung dreht den Punkt um die Z-Achse.

![Gleichung einer Z-Drehungsmatrix für einen neuen Punkt](images/matzrot.png)

In diesen Beispielmatrizen steht der griechisch-Buchstabe theta für den Drehwinkel im Bogenmaß. Winkel werden im Uhrzeigersinn gemessen, wenn sie entlang der Drehachse zum Ursprung hin betrachtet werden.

Verwenden Sie in einer C++-Anwendung die Funktionen [**D3DXMatrixRotationX,**](d3dxmatrixrotationx.md) [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)und [**D3DXMatrixRotationZ,**](d3dxmatrixrotationz.md) die von der D3DX-Hilfsprogrammbibliothek bereitgestellt werden, um Drehungsmatrizen zu erstellen. Im Folgenden finden Sie den Code für die **D3DXMatrixRotationX-Funktion.**


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a>Verkettung von Matrizen

Ein Vorteil der Verwendung von Matrizen ist, dass Sie die Auswirkungen von zwei oder mehr Matrizen kombinieren können, indem Sie sie multiplizieren. Dies bedeutet, dass Sie keine zwei Matrizen anwenden müssen, um ein Modell zu drehen und es dann an einen Speicherort zu übersetzen. Stattdessen multiplizieren Sie die Drehungs- und Übersetzungsmatrizen, um eine zusammengesetzte Matrix zu erstellen, die alle ihre Auswirkungen enthält. Dieser Prozess, der als Matrixkonkettung bezeichnet wird, kann mit der folgenden Gleichung geschrieben werden.

![Gleichung der Matrixkonkettung](images/matrxcat.png)

In dieser Gleichung ist C die zusammengesetzte Matrix, die erstellt wird, und M₁ bis Mn sind die einzelnen Matrizen. In den meisten Fällen werden nur zwei oder drei Matrizen verkettet, es gibt jedoch keine Beschränkung.

Verwenden Sie [**die D3DXMatrixMultiply-Funktion,**](d3dxmatrixmultiply.md) um die Matrixmultiplikation durchzuführen.

Die Reihenfolge, in der die Matrixmultiplikation ausgeführt wird, ist entscheidend. Die obige Formel spiegelt die Von-rechts-Regel der Matrixverkettung wider. Das heißt, die sichtbaren Auswirkungen der Matrizen, die Sie zum Erstellen einer zusammengesetzten Matrix verwenden, treten in der Reihenfolge von links nach rechts auf. Eine typische Weltmatrix wird im folgenden Beispiel gezeigt. Imagine, dass Sie die Weltmatrix für eine stereotypische Kastensauce erstellen. Wahrscheinlich möchten Sie die Y-Achse des Modellraums um seinen Mittelpunkt drehen und an einen anderen Ort in Ihrer Szene übersetzen. Um diesen Effekt zu erreichen, erstellen Sie zunächst eine Rotationsmatrix und multiplizieren sie dann mit einer Übersetzungsmatrix, wie in der folgenden Gleichung gezeigt.

![Drehungsgleichung basierend auf einer Rotationsmatrix und einer Übersetzungsmatrix](images/wrldexpl.png)

In dieser Formel ist R<sub>y</sub> eine Matrix für die Drehung um die y-Achse, und T<sub>w</sub> ist eine Übersetzung zu einer Position in Weltkoordinaten.

Die Reihenfolge, in der Sie die Matrizen multiplizieren, ist wichtig, da die Matrixmultiplikation im Gegensatz zum Multiplizieren von zwei Skalarwerten nicht kommutativ ist. Das Multiplizieren der Matrizen in der entgegengesetzten Reihenfolge hat den visuellen Effekt, dass die 300000-n-Menschen in ihre Weltraumposition übersetzt und dann um den Ursprung der Welt gedreht werden.

Unabhängig davon, welche Art von Matrix Sie erstellen, merken Sie sich die Regel von links nach rechts, um sicherzustellen, dass Sie die erwarteten Auswirkungen erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 



