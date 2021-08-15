---
title: Anhang Matrixtransformationen
description: Dieses Thema bietet eine mathematische Übersicht über Matrixtransformationen für 2D-Grafiken.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d02976446824bba07829173bb326338a55732b39c640c93319630a209096b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389260"
---
# <a name="appendix-matrix-transforms"></a>Anhang: Matrixtransformationen

Dieses Thema bietet eine mathematische Übersicht über Matrixtransformationen für 2D-Grafiken. Sie müssen jedoch keine Matrixmatrizen kennen, um Transformationen in Direct2D verwenden zu können. Lesen Sie dieses Thema, wenn Sie an der Mathematik interessiert sind. Andernfalls können Sie dieses Thema überspringen.

-   [Einführung in Matrizen](#introduction-to-matrices)
    -   [Matrixvorgänge](#matrix-operations)
-   [Affine Transformationen](#affine-transforms)
    -   [Übersetzungstransformation](#translation-transform)
    -   [Skalierungstransformation](#scaling-transform)
    -   [Drehung um den Ursprung](#rotation-around-the-origin)
    -   [Drehung um einen beliebigen Punkt](#rotation-around-an-arbitrary-point)
    -   [Schiefe transformieren](#skew-transform)
-   [Darstellen von Transformationen in Direct2D](#representing-transforms-in-direct2d)
-   [Nächste](#next)

## <a name="introduction-to-matrices"></a>Einführung in Matrizen

Eine Matrix ist ein rechteckiges Array aus echten Zahlen. Die *Reihenfolge* der Matrix ist die Anzahl der Zeilen und Spalten. Wenn die Matrix beispielsweise drei Zeilen und zwei Spalten enthält, beträgt die Reihenfolge 3 × 2. Matrizen werden in der Regel mit den Matrixelementen angezeigt, die in eckige Klammern eingeschlossen sind:

![3 x 2 Matrix.](images/matrix01.png)

Notation: Eine Matrix wird durch einen Großbuchstaben festgelegt. Elemente werden durch Kleinbuchstaben gekennzeichnet. In Inskripts wird die Zeilen- und Spaltennummer eines Elements angegeben. Beispielsweise ist ein *ij das* Element in der i'th-Zeile und der j'th-Spalte der Matrix A.

Das folgende Diagramm zeigt eine i × j-Matrix mit den einzelnen Elementen in jeder Zelle der Matrix.

![eine Matrix mit i-Zeilen und j-Spalten.](images/matrix15.png)

### <a name="matrix-operations"></a>Matrixvorgänge

In diesem Abschnitt werden die grundlegenden Vorgänge beschrieben, die für Matrizen definiert sind.

*Addition* von . Die Summe A + B von zwei Matrizen wird durch Hinzufügen der entsprechenden Elemente von A und B ermittelt:

<dl> A + B = \[ a *ij* \]  +  \[ b *ij* \]  =  \[ a *ij* + b *ij*\]
</dl>

*Skalar-Multiplikation*. Dieser Vorgang multipliziert eine Matrix mit einer echten Zahl. Bei einer echten *Zahl k wird* das Skalarprodukt kA durch Multiplikation jedes Elements von A mit k *ermittelt.*

<dl> kA = k \[ a *ij* \]  =  \[ k × ein *ij*\]
</dl>

*Matrixmultiplikation*. Bei zwei Matrizen A und B mit der Reihenfolge (m × n) und (n × p) ist das Produkt C = A × B eine Matrix mit bestellung (m × p), die wie folgt definiert ist:

![Zeigt eine Formel für die Matrixmultiplikation an.](images/matrix02.png)

oder entsprechend:

<dl> c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</dl>

Gehen Sie wie folgt vor, um jedes Element c *ij* zu berechnen:

1.  Nehmen Sie die i'th-Zeile von A und die j'th-Spalte von B.
2.  Multiplizieren Sie jedes Elementpaar in Zeile und Spalte: den ersten Zeileneintrag mit dem ersten Spalteneintrag, den zweiten Zeileneintrag mit dem zweiten Spalteneintrag usw.
3.  Summiert das Ergebnis.

Hier ist ein Beispiel für die Multiplikation einer Matrix (2 × 2) mit einer Matrix (2 × 3).

![Matrixmultiplikation.](images/matrix03.png)

Die Matrixmultiplikation ist nicht kommutativ. Das heißt, A × B ≠ B × A. Außerdem ergibt sich aus der Definition, dass nicht jedes Matrizenpaar multipliziert werden kann. Die Anzahl der Spalten in der linken Matrix muss der Anzahl der Zeilen in der rechten Matrix entspricht. Andernfalls ist × Operator nicht definiert.

*Identifizieren Sie die Matrix*. Eine Identitätsmatrix mit dem Design I ist eine quadratische Matrix, die wie folgt definiert ist:

<dl> I *ij* = 1, wenn *i*  =  *j*, andernfalls 0.  
</dl>

Anders ausgedrückt: Eine Identitätsmatrix enthält 1 für jedes Element, bei dem die Zeilennummer der Spaltennummer entspricht, und 0 (null) für alle anderen Elemente. Hier sehen Sie beispielsweise die drei × 3 Identitätsmatrix.

![Identitätsmatrix.](images/matrix04.png)

Die folgenden Gleichheiten gelten für jede Matrix M.

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>Affine Transformationen

Eine *affine Transformation ist eine* mathematische Operation, die einen Koordinatenbereich einem anderen zu ordnet. Anders ausgedrückt: Sie ordnet einen Satz von Punkten einem anderen Satz von Punkten zu. Affine Transformationen verfügen über einige Features, die sie für Computergrafiken nützlich machen.

-   Affine Transformationen behalten *die Sortierung bei.* Wenn drei oder mehr Punkte auf eine Linie fallen, bilden sie nach der Transformation immer noch eine Linie. Gerade Linien bleiben gerade.
-   Die Zusammensetzung von zwei affinen Transformationen ist eine affine Transformation.

Affine Transformationen für 2D-Leerzeichen haben das folgende Formular.

![Zeigt eine affine Transformation für 2D-Raum.](images/matrix05.png)

Wenn Sie die Zuvor gegebene Definition der Matrixmultiplikation anwenden, können Sie zeigen, dass das Produkt zweier affiner Transformationen eine weitere affine Transformation ist. Um einen 2D-Punkt mithilfe einer affinen Transformation zu transformieren, wird der Punkt als 1 × 3 Matrix dargestellt.

<dl> P = \| x y 1 \|  
</dl>

Die ersten beiden Elemente enthalten die x- und y-Koordinaten des Punkts. Die 1 wird im dritten Element platziert, damit die Mathematik ordnungsgemäß funktioniert. Multiplizieren Sie die beiden Matrizen wie folgt, um die Transformation anzuwenden.

<dl> P' = P × M  
</dl>

Dies wird auf Folgendes erweitert.

![affine Transformation.](images/matrix06.png)

where

<dl> x' = ax + cy + e  
y' = bx + dy + f  
</dl>

Um den transformierten Punkt zu erhalten, nehmen Sie die ersten beiden Elemente der Matrix P'.

<dl> p = (x', y') = (ax + cy + e, bx + dy + f)  
</dl>

> [!Note]  
> Eine 1 × *n* Matrix wird als *Zeilenvektor bezeichnet.* Sowohl Direct2D als auch Direct3D verwenden Zeilenvektoren, um Punkte im 2D- oder 3D-Raum zu darstellen. Sie können ein entsprechendes Ergebnis erhalten, indem Sie einen Spaltenvektor (*n* × 1) verwenden und die Transformationsmatrix transposieren. Die meisten Grafiktexte verwenden die Form des Spaltenvektors. In diesem Thema wird die Zeilenvektorform für Konsistenz mit Direct2D und Direct3D beschrieben.

 

Die nächsten Abschnitte leiten die grundlegenden Transformationen ab.

### <a name="translation-transform"></a>Übersetzungstransformation

Die Übersetzungstransformationsmatrix hat das folgende Formular.

![Übersetzungstransformation.](images/matrix07.png)

Wenn Sie einen Punkt *P in* diese Gleichung einstecken, ergibt sich Folgendes:

<dl> P' = (*x*  +  *dx*, *y*  +  *dy*)
</dl>

Dies entspricht dem Punkt (x, y), der von *dx* in der X-Achse und *dy* in der Y-Achse übersetzt wird.

![Ein Diagramm, das die Übersetzung von zwei Punkten zeigt.](images/graphics22.png)

### <a name="scaling-transform"></a>Skalierungstransformation

Die Skalierungstransformationsmatrix hat das folgende Formular.

![Skalierungstransformation.](images/matrix09.png)

Das Verbinden eines Punkts *P* in diese Gleichung ergibt Folgendes:

<dl> P' = (*x* × *dx*, *y* × *dy*)
</dl>

Dies entspricht dem Punkt (x,y), der durch *dx* und *dy* skaliert wird.

![Ein Diagramm, das die Skalierung von zwei Punkten zeigt.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Drehung um den Ursprung

Die Matrix, um die ein Punkt um den Ursprung gedreht werden soll, hat die folgende Form.

![Zeigt eine Formel für eine Drehungstransformation an.](images/matrix11.png)

Der transformierte Punkt ist:

<dl> P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)
</dl>

Beweis. Um zu zeigen, dass P' eine Drehung darstellt, sehen Sie sich das folgende Diagramm an.

![Ein Diagramm, das die Drehung um den Ursprung zeigt.](images/graphics24.png)

Gegeben:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)
</dt> <dd>

Der ursprüngliche zu transformierte Punkt.

</dd> <dt>

Φ
</dt> <dd>

Der Winkel, der von der Linie (0,0) bis P gebildet wird.

</dd> <dt>

Θ
</dt> <dd>

Der Winkel, um den (x,y) um den Ursprung gedreht werden soll.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')
</dt> <dd>

Der transformierte Punkt.

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Die Länge der Zeile (0,0) bis P. Auch der Radius des Drehkreiss.

</dd> </dl>

> [!Note]  
> In diesem Diagramm wird das Standardkoordinatensystem verwendet, das in der Geometrie verwendet wird, wobei die positive y-Achse nach oben zeigt. Direct2D verwendet das Windows Koordinatensystem, bei dem die positive Y-Achse nach unten zeigt.

 

Der Winkel zwischen der x-Achse und der Linie (0,0) bis P' beträgt 0 + Θ. Die folgenden Identitäten enthalten:

<dl> x = R cossstelle  
y = R sinsstelle  
x' = R cos(Θ + Θ)  
y' = R sin(Ü+ Θ)  
</dl>

Lösen Sie nun für x' und y' in Bezug auf Θ. Durch die trigonometrischen Additionsformeln:

<dl> x' = R(cosΘcosΘ – sinΘsinΘ) = RcosmosE – RSINSIN  
y' = R(sinΘcosΘ + coseinander) = Rsineinander + Rcos  
</dl>

Ersetzend erhalten wir:

<dl> x' = xcosΘ – ysin unicode  
y' = xsinΘ + ycos unicode  
</dl>

, was dem oben gezeigten transformierten Punkt P' entspricht.

### <a name="rotation-around-an-arbitrary-point"></a>Drehung um einen beliebigen Punkt

Um einen anderen Punkt (x,y) als den Ursprung zu drehen, wird die folgende Matrix verwendet.

![Drehungstransformation.](images/matrix13.png)

Sie können diese Matrix ableiten, indem Sie den Punkt (x,y) als Ursprung verwenden.

![Ein Diagramm, das die Drehung um einen Punkt zeigt.](images/graphics25.png)

Lassen Sie (x1, y1) der Punkt sein, der sich aus der Drehung des Punkts (x0, y0) um den Punkt (x,y) ergibt. Wir können x1 wie folgt ableiten.

<dl> x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x  
x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysin unicode \]  
</dl>

Schließen Sie diese Gleichung nun wieder in die Transformationsmatrix ein, indem Sie die Formel x1 = ax0 + cy0 + e von früher verwenden. Verwenden Sie die gleiche Prozedur, um y1 abzuleiten.

### <a name="skew-transform"></a>Schiefe Transformation

Die Schiefetransformation wird durch vier Parameter definiert:

-   Θ: Die Menge an Schiefe entlang der x-Achse, gemessen als Winkel von der y-Achse.
-   Ws: Die Menge, die entlang der y-Achse schief zugehen soll, gemessen als Winkel von der x-Achse.
-   (*px*, *py*): Die x- und y-Koordinaten des Punkts, an dem die Schiefe ausgeführt wird.

Die Schiefetransformation verwendet die folgende Matrix.

![Schiefe Transformation.](images/matrix14.png)

Der transformierte Punkt ist:

<dl> P' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΘ) – *py* tan unicode
</dl>

oder auf ähnliche Weise:

<dl> P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΘ)
</dl>

Um zu sehen, wie diese Transformation funktioniert, berücksichtigen Sie jede Komponente einzeln. Der Θ-Parameter verschiebt jeden Punkt in x Richtung um einen Betrag, der tanΘ entspricht. Das folgende Diagramm zeigt die Beziehung zwischen Θ und der X-Achsenschiefe.

![Diagramm, das die Schiefe entlang der x-Achse zeigt.](images/graphics26.png)

Hier sehen Sie die gleiche Schiefe, die auf ein Rechteck angewendet wird:

![Diagramm, das die Schiefe entlang der x-Achse zeigt, wenn sie auf ein Rechteck angewendet wird.](images/graphics27.png)

Der Y-Parameter hat die gleiche Wirkung, aber entlang der y-Achse:

![Diagramm, das die Schiefe entlang der y-Achse zeigt.](images/graphics28.png)

Das nächste Diagramm zeigt die y-Achsenschiefe, die auf ein Rechteck angewendet wird.

![Diagramm, das die Schiefe entlang der y-Achse zeigt, wenn sie auf ein Rechteck angewendet wird.](images/graphics29.png)

Schließlich verschieben die Parameter *px* und *py* den Mittelpunkt für die Schiefe entlang der x- und y-Achse.

## <a name="representing-transforms-in-direct2d"></a>Darstellen von Transformationen in Direct2D

Alle Direct2D-Transformationen sind affine Transformationen. Direct2D unterstützt keine nicht affinen Transformationen. Transformationen werden durch die [**D2D1 \_ MATRIX \_ 3X2 \_ F-Struktur**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) dargestellt. Diese Struktur definiert eine 3 × 2-Matrix. Da die dritte Spalte einer affinen Transformation immer gleich ist ( \[ 0, 0, 1 \] ), und Direct2D keine nicht affinen Transformationen unterstützt, ist es nicht erforderlich, die gesamte 3 × 3-Matrix anzugeben. Intern verwendet Direct2D drei × 3 Matrizen, um die Transformationen zu berechnen.

Die Member der [**D2D1 \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) werden entsprechend ihrer Indexposition benannt: Das **\_ 11-Element** ist element (1,1), das **\_ 12-Element** ist element (1,2) usw. Obwohl Sie die Strukturmember direkt initialisieren können, wird empfohlen, die [**D2D1::Matrix3x2F-Klasse**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) zu verwenden. Diese Klasse erbt **D2D1 \_ MATRIX \_ 3X2 \_ F** und stellt Hilfsmethoden zum Erstellen der grundlegenden affinen Transformationen bereit. Die -Klasse definiert auch [**den Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) zum Zusammenstellen von zwei oder mehr Transformationen, wie unter [Anwenden von Transformationen in Direct2D](applying-transforms-in-direct2d.md)beschrieben.

## <a name="next"></a>Nächste

[Modul 4. Benutzereingabe](module-4--user-input.md)

 

 