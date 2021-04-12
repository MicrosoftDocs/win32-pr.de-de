---
description: Der Teil von Direct3D, der die Geometrie über die Geometrie Pipeline mit fester Funktionsweise überträgt, ist die Transform-Engine.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392881"
---
# <a name="transforms-direct3d-9"></a>Transformationen (Direct3D 9)

Der Teil von Direct3D, der die Geometrie über die Geometrie Pipeline mit fester Funktionsweise überträgt, ist die Transform-Engine. Er sucht das Modell und den Viewer auf der Welt, projiziert die Scheitel Punkte, die auf dem Bildschirm angezeigt werden, und schneidet Scheitel Punkte an den Viewport. Die Transformations-Engine führt auch Beleuchtungsberechnungen durch, um die diffusen und Glanz Komponenten in jedem Scheitelpunkt zu bestimmen.

Die Geometrie Pipeline nimmt Vertices als Eingabe. Die Transformations-Engine wendet die Transformationen "World", "View" und "Projection" auf die Scheitel Punkte an, schneidet das Ergebnis ab und übergibt alles an den Rasterizer.

Am Anfang der Pipeline werden die Vertices eines Modells relativ zu einem lokalen Koordinatensystem deklariert. Dies ist ein lokaler Ursprung und eine Ausrichtung. Diese Ausrichtung von Koordinaten wird häufig als Modellbereich bezeichnet, und einzelne Koordinaten werden als Modell Koordinaten bezeichnet.

In der ersten Phase der Geometrie Pipeline werden die Scheitel Punkte eines Modells von Ihrem lokalen Koordinatensystem in ein Koordinatensystem transformiert, das von allen Objekten in einer Szene verwendet wird. Der Prozess der Umgestaltung der Scheitel Punkte wird als Welt Transformation bezeichnet. Diese neue Ausrichtung wird häufig als Welt Raum bezeichnet, und jeder Scheitelpunkt im Raum wird mit Weltkoordinaten deklariert.

In der nächsten Phase sind die Scheitel Punkte, die Ihre 3D-Welt beschreiben, in Bezug auf eine Kamera orientiert. Das heißt, Ihre Anwendung wählt eine Sicht Ansicht für die Szene aus, und die Raumkoordinaten der Welt werden verschoben und um die Ansicht der Kamera gedreht. Dadurch wird der Raum in den Kamerabereich verwandelt. Dies ist die Ansichts Transformation.

Die nächste Phase ist die Projektions Transformation. In diesem Teil der Pipeline werden Objekte in der Regel auf die Entfernung des Viewers skaliert, um die Illusion von Tiefe an eine Szene zu vermitteln. Close-Objekte werden so erstellt, dass Sie größer als entfernte Objekte sind usw. Der Einfachheit halber bezieht sich diese Dokumentation auf den Raum, in dem Scheitel Punkte nach der Projektions Transformation als Projektionsraum vorhanden sind. In einigen Grafik Büchern wird der Projektionsraum möglicherweise als homogener Perspektiven Raum bezeichnet. Nicht alle Projektions Transformationen Skalieren die Größe von Objekten in einer Szene. Eine Projektion wie diese wird mitunter als affine oder orthogonale Projektion bezeichnet.

Im letzten Teil der Pipeline werden alle Scheitel Punkte, die auf dem Bildschirm nicht sichtbar sind, entfernt, sodass der Raster nicht mehr die Zeit zum Berechnen der Farben und Schattierung für etwas hat, das nie angezeigt wird. Dieser Vorgang wird als Clipping bezeichnet. Nach dem Clipping werden die verbleibenden Scheitel Punkte entsprechend den viewportparametern skaliert und in Bildschirm Koordinaten konvertiert. Die resultierenden Scheitel Punkte, die auf dem Bildschirm angezeigt werden, wenn die Szene rasteriert ist, sind im Bildschirmbereich vorhanden.

Transformationen werden verwendet, um die Objekt Geometrie von einem Koordinaten Bereich in einen anderen zu konvertieren. Direct3D verwendet Matrizen, um 3D-Transformationen auszuführen. In diesem Abschnitt wird erläutert, wie Matrizen 3D-Transformationen erstellen, einige gängige Verwendungsmöglichkeiten für Transformationen beschreiben und wie Sie Matrizen kombinieren können, um eine einzelne Matrix zu erstellen, die mehrere Transformationen umfasst.

-   [World Transform (Direct3D 9)](world-transform.md) : Konvertieren vom Modellbereich in den Raum
-   [Transformation anzeigen (Direct3D 9)](view-transform.md) -Konvertieren von Welt Raum zum Anzeigen von Speicherplatz
-   [Projektions Transformation (Direct3D 9)](projection-transform.md) -Konvertieren von Sichtbereich in Projektionsraum

## <a name="matrix-transforms"></a>Matrixtransformationen

In Anwendungen, die mit 3D-Grafiken funktionieren, können Sie mithilfe geometrischer Transformationen folgende Aktionen ausführen:

-   Gibt den Speicherort eines Objekts relativ zu einem anderen Objekt an.
-   Drehen und Größe von Objekten.
-   Ändern der Anzeige von Positionen, Richtungen und Perspektiven.

Sie können beliebige Punkte (x, y, z) mit einer 4 x 4-Matrix in einen anderen Punkt (x ", y", z ") umwandeln, wie in der folgenden Gleichung gezeigt.

![Gleichung der Umwandlung eines Punkts in einen anderen Punkt](images/matmult.png)

Führen Sie die folgenden Gleichungen für (x, y, z) und die Matrix aus, um den Punkt (x ', y ', z ') zu schaffen.

![Gleichungen für den neuen Punkt](images/matexpnd.png)

Die gängigsten Transformationen sind Übersetzung, Drehung und Skalierung. Sie können die Matrizen, die diese Effekte erzeugen, in einer einzelnen Matrix kombinieren, um mehrere Transformationen gleichzeitig zu berechnen. Beispielsweise können Sie eine einzelne Matrix erstellen, um eine Reihe von Punkten zu übersetzen und zu drehen.

Matrizen werden in der Reihenfolge der Zeilen Spalten geschrieben. Eine Matrix, die Scheitel Punkte entlang jeder Achse gleichmäßig skaliert, die als einheitliche Skalierung bezeichnet wird, wird durch die folgende Matrix mithilfe der mathematischen Notation dargestellt.

![Gleichung einer Matrix für die einheitliche Skalierung](images/matrix.png)

In C++ deklariert Direct3D Matrizen als zweidimensionales Array mit der [**D3DMATRIX**](d3dmatrix.md) -Struktur. Im folgenden Beispiel wird gezeigt, wie eine **D3DMATRIX** -Struktur initialisiert wird, die als einheitliche Skalierungs Matrix fungiert.


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

Mit der folgenden Gleichung wird der Punkt (x, y, z) in einen neuen Punkt (x ", y", z ") übersetzt.

![Gleichung einer Übersetzungs Matrix für einen neuen Punkt](images/transl8.png)

Sie können eine Übersetzungs Matrix in C++ manuell erstellen. Das folgende Beispiel zeigt den Quellcode für eine Funktion, die eine Matrix erstellt, um Vertices zu übersetzen.


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



Zur einfacheren bereitstellt die D3DX Utility Library die [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) -Funktion bereit.

## <a name="scale"></a>Skalieren

Die folgende Gleichung skaliert den Punkt (x, y, z) um beliebige Werte in der x-, y-und z-Richtung zu einem neuen Punkt (x ', y ', z ').

![Gleichung einer Skalierungs Matrix für einen neuen Punkt](images/matscale.png)

## <a name="rotate"></a>Rotate

Die hier beschriebenen Transformationen gelten für Links gesteuerte Koordinatensysteme und können sich daher von Transformations Matrizen unterscheiden, die Sie an anderer Stelle gesehen haben.

Die folgende Gleichung dreht den Punkt (x, y, z) um die x-Achse und erzeugt einen neuen Punkt (x ', y ', z ').

![Gleichung einer x-Rotations Matrix für einen neuen Punkt](images/matxrot.png)

Die folgende Gleichung dreht den Punkt um die y-Achse.

![Gleichung einer y-Rotations Matrix für einen neuen Punkt](images/matyrot.png)

Die folgende Gleichung dreht den Punkt um die z-Achse.

![Gleichung einer z-Rotations Matrix für einen neuen Punkt](images/matzrot.png)

In diesen Beispiel Matrizen steht der griechische Buchstabe der TA für den Drehwinkel im Bogenmaße. Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.

Verwenden Sie in einer C++-Anwendung die [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)-, [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)-und [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) -Funktionen, die von der D3DX Utility Library bereitgestellt werden, um Rotations Matrizen zu erstellen. Im folgenden finden Sie den Code für die **D3DXMatrixRotationX** -Funktion.


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



## <a name="concatenating-matrices"></a>Verketten von Matrizen

Ein Vorteil der Verwendung von Matrizen besteht darin, dass Sie die Auswirkungen von zwei oder mehr Matrizen kombinieren können, indem Sie diese multiplizieren. Dies bedeutet, dass Sie keine zwei Matrizen anwenden müssen, um ein Modell zu drehen und es dann an einen Speicherort zu übersetzen. Stattdessen multiplizieren Sie die Drehung und die Übersetzungs Matrizen, um eine zusammengesetzte Matrix zu erzeugen, die all ihre Auswirkungen enthält. Dieser Prozess, der als Matrix Verkettung bezeichnet wird, kann mit der folgenden Gleichung geschrieben werden.

![Gleichung der Matrix Verkettung](images/matrxcat.png)

In dieser Gleichung ist C die zusammengesetzte Matrix, die erstellt wird, und M ₁ bis MN sind die einzelnen Matrizen. In den meisten Fällen werden nur zwei oder drei Matrizen verkettet, aber es gibt keine Begrenzung.

Verwenden Sie die [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) -Funktion, um die Matrix Multiplikation auszuführen.

Die Reihenfolge, in der die Matrix Multiplikation durchgeführt wird, ist entscheidend. Die vorangehende Formel reflektiert die Regel von links nach rechts der Matrix Verkettung. Das heißt, die sichtbaren Auswirkungen der Matrizen, die Sie zum Erstellen einer zusammengesetzten Matrix verwenden, treten in der Reihenfolge von links nach rechts auf. Im folgenden Beispiel wird eine typische Weltmatrix gezeigt. Stellen Sie sich vor, dass Sie die Weltmatrix für einen Stereo typischen Flugtyp erstellen. Vielleicht möchten Sie den fliegenden Schlauch um seine Mitte drehen, die y-Achse des Modell Raums, und ihn an eine andere Stelle in Ihrer Szene übersetzen. Um diesen Effekt zu erreichen, erstellen Sie zunächst eine Rotations Matrix und multiplizieren Sie dann mit einer Übersetzungs Matrix, wie in der folgenden Gleichung gezeigt.

![Gleichung der Drehung basierend auf einer Rotations Matrix und einer Übersetzungs Matrix](images/wrldexpl.png)

In dieser Formel ist R<sub>y</sub> eine Matrix für die Drehung der y-Achse, und T<sub>w</sub> ist eine Übersetzung an eine Position in globalen Koordinaten.

Die Reihenfolge, in der Sie die Matrizen multiplizieren, ist wichtig, da im Gegensatz zu multiplizieren zweier Skalarwerte die Matrix Multiplikation nicht commutativ ist. Das Multiplizieren der Matrizen in umgekehrter Reihenfolge hat den visuellen Effekt, dass der fliegende Unterbereich in seine Welt Raum Position übersetzt und dann um den Ursprung der Welt gedreht wird.

Unabhängig von der Art der Matrix, die Sie erstellen, merken Sie sich die Regel von links nach rechts, um sicherzustellen, dass Sie die erwarteten Auswirkungen erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 



