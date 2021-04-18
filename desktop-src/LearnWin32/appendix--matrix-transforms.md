---
title: Anhang Matrixtransformationen
description: Dieses Thema bietet eine mathematische Übersicht über Matrix Transformationen für 2D-Grafiken.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104563886"
---
# <a name="appendix-matrix-transforms"></a>Anhang: Matrix Transformationen

Dieses Thema bietet eine mathematische Übersicht über Matrix Transformationen für 2D-Grafiken. Allerdings müssen Sie Matrizen Mathematik nicht kennen, um Transformationen in Direct2D verwenden zu können. Lesen Sie dieses Thema, wenn Sie an der Mathematik interessiert sind. Andernfalls können Sie dieses Thema überspringen.

-   [Einführung in Matrizen](#introduction-to-matrices)
    -   [Matrix Vorgänge](#matrix-operations)
-   [Affine Transformationen](#affine-transforms)
    -   [Übersetzungs Transformation](#translation-transform)
    -   [Skalierungs Transformation](#scaling-transform)
    -   [Drehung um den Ursprung](#rotation-around-the-origin)
    -   [Drehung um einen beliebigen Punkt](#rotation-around-an-arbitrary-point)
    -   [Verzerrungs Transformation](#skew-transform)
-   [Darstellen von Transformationen in Direct2D](#representing-transforms-in-direct2d)
-   [Nächste](#next)

## <a name="introduction-to-matrices"></a>Einführung in Matrizen

Eine Matrix ist ein rechteckiges Array von reellen Zahlen. Die *Reihenfolge* der Matrix entspricht der Anzahl von Zeilen und Spalten. Wenn die Matrix z. b. drei Zeilen und 2 Spalten enthält, ist die Reihenfolge 3 × 2. Matrizen werden normalerweise mit den Matrixelementen angezeigt, die in eckigen Klammern eingeschlossen sind:

![3 x 2-Matrix.](images/matrix01.png)

Notation: eine Matrix wird durch einen Großbuchstaben angegeben. -Elemente werden durch Kleinbuchstaben angegeben. Index gibt die Zeilen-und Spaltennummer eines Elements an. Ein *IJ* ist beispielsweise das Element in der Zeile "n" und der "j."-Spalte der Matrix a.

Das folgende Diagramm zeigt eine i × j-Matrix mit den einzelnen Elementen in den einzelnen Zellen der Matrix.

![eine Matrix mit i-Zeilen und j-Spalten.](images/matrix15.png)

### <a name="matrix-operations"></a>Matrix Vorgänge

Dieser Abschnitt beschreibt die grundlegenden Vorgänge, die für Matrizen definiert sind.

*Fügen Sie hinzu*. Die Summe A + B von zwei Matrizen wird durch Hinzufügen der entsprechenden Elemente von A und b abgerufen:

<dl> A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + b *IJ*\]
</dl>

*Skalare Multiplikation*. Durch diesen Vorgang wird eine Matrix mit einer reellen Zahl multipliziert. Bei einer reellen Zahl *k* wird das Skalarprodukt "Ka" abgerufen, indem jedes Element von a mit *k* multipliziert wird.

<dl> Ka = k \[ a *IJ* \]  =  \[ k × a *IJ*\]
</dl>

*Matrix Multiplikation*. Bei zwei Matrizen A und B mit der Reihenfolge (m × n) und (n × p) ist das Produkt C = a × b eine Matrix mit der Reihenfolge (m × p), die wie folgt definiert wird:

![Zeigt eine Formel für die Matrix Multiplikation an.](images/matrix02.png)

oder, gleichwertig:

<dl> c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *in* + b *NJ*  
</dl>

Um jedes Element c *IJ* zu berechnen, führen Sie die folgenden Schritte aus:

1.  Nehmen Sie in der Zeile "a" und in der "j."-Spalte den Typ "B".
2.  Multiplizieren Sie jedes Paar von Elementen in der Zeile und Spalte: der erste Zeileneintrag mit dem ersten Spalten Eintrag, der zweite Zeileneintrag mit dem zweiten Spalten Eintrag usw.
3.  Addieren Sie das Ergebnis.

Im folgenden finden Sie ein Beispiel für das Multiplizieren einer (2 × 2) Matrix mit einer Matrix (2 × 3).

![Matrix Multiplikation.](images/matrix03.png)

Die Matrix Multiplikation ist nicht kommutativ. Das heißt, ein × b ≠ B × a. Aus der Definition folgt auch, dass nicht jedes Matrizen paar multipliziert werden kann. Die Anzahl der Spalten in der linken Matrix muss gleich der Anzahl der Zeilen in der rechten Matrix sein. Andernfalls ist der ×-Operator nicht definiert.

*Identifizieren* Sie die Matrix. Eine Identitätsmatrix, die als I bezeichnet wird, ist eine quadratische Matrix, die wie folgt definiert wird:

<dl> Ich habe "*IJ* = 1", wenn *i*  =  *j*, andernfalls "0".  
</dl>

Mit anderen Worten: eine Identitätsmatrix enthält 1 für jedes Element, bei dem die Zeilennummer gleich der Spaltennummer ist, und 0 für alle anderen Elemente. Hier ist beispielsweise die 3 × 3-Identitätsmatrix.

![Identitätsmatrix.](images/matrix04.png)

Die folgenden equalitäten enthalten für jede Matrix M.

<dl> M x I = m  
I x m = m  
</dl>

## <a name="affine-transforms"></a>Affine Transformationen

Eine *affine Transformation* ist ein mathematischer Vorgang, der einen Koordinatenraum einem anderen zuordnet. Anders ausgedrückt, ordnet Sie einen Satz von Punkten einem anderen Satz von Punkten zu. Affine Transformationen verfügen über einige Features, die Sie in Computergrafiken nützlich machen.

-   Affine Transformationen bewahren die *Granularität*. Wenn drei oder mehr Punkte in eine Linie fallen, bilden Sie nach der Transformation weiterhin eine Zeile. Gerade Linien bleiben gleich.
-   Die Komposition zweier affininer Transformationen ist eine affine Transformation.

Affine Transformationen für 2D-Raum weisen die folgende Form auf:

![Zeigt eine affine Transformation für 2-D-Raum.](images/matrix05.png)

Wenn Sie die zuvor angegebene Definition der Matrix Multiplikation anwenden, können Sie anzeigen, dass das Produkt von zwei affinen Transformationen eine weitere affine Transformation ist. Um einen 2D-Punkt mithilfe einer affinen Transformation zu transformieren, wird der Punkt als 1 × 3-Matrix dargestellt.

<dl> P = \| x y 1 \|  
</dl>

Die ersten beiden Elemente enthalten die x-und y-Koordinaten des Punkts. Der Wert 1 wird in das dritte Element eingefügt, damit das mathematische Element ordnungsgemäß funktioniert. Um die Transformation anzuwenden, Multiplizieren Sie die beiden Matrizen wie folgt.

<dl> p ' = p × M  
</dl>

Dies wird wie folgt erweitert.

![affine Transformation.](images/matrix06.png)

where

<dl> x ' = AX + CY + e  
y ' = BX + dy + f  
</dl>

Um den transformierten Punkt zu erhalten, nehmen Sie die ersten beiden Elemente von Matrix P '.

<dl> p = (x ', y ') = (AX + CY + e, BX + dy + f)  
</dl>

> [!Note]  
> Eine Matrix mit 1 × *n* wird als *Zeilen Vektor* bezeichnet. Direct2D und Direct3D verwenden Zeilen Vektoren zur Darstellung von Punkten im 2D-oder 3D-Raum. Sie können ein entsprechendes Ergebnis mit einem Spalten Vektor (*n* × 1) und der Transformation der Transformationsmatrix erhalten. In den meisten Grafik Texten wird das Spalten Vektor Formular verwendet. In diesem Thema wird das Zeilen Vektor Formular für Konsistenz mit Direct2D und Direct3D dargestellt.

 

In den nächsten Abschnitten werden die grundlegenden Transformationen abgeleitet.

### <a name="translation-transform"></a>Übersetzungs Transformation

Die Übersetzungs Transformationsmatrix weist das folgende Format auf.

![Übersetzungs Transformation.](images/matrix07.png)

Das Plugging eines Punkt- *P* in diese Gleichung ergibt folgendes:

<dl> P ' = (*x*  +  *DX*, *y*  +  *dy*)
</dl>

Dies entspricht dem Punkt (x, y), der von *DX* in der x-Achse und *dy* auf der y-Achse übersetzt wurde.

![ein Diagramm, das die Übersetzung von zwei Punkten anzeigt.](images/graphics22.png)

### <a name="scaling-transform"></a>Skalierungs Transformation

Die Matrix der Skalierungs Transformation weist das folgende Format auf.

![Skalierungs Transformation.](images/matrix09.png)

Das Plugging eines Punkt- *P* in diese Gleichung ergibt folgendes:

<dl> P ' = (*x* ∙ *DX*, *y* ∙ *dy*)
</dl>

Dies entspricht dem Punkt (x, y), der von *DX* und *dy* skaliert wird.

![ein Diagramm, das die Skalierung von zwei Punkten anzeigt.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Drehung um den Ursprung

Die Matrix zum Drehen eines Punkts um den Ursprung weist das folgende Format auf.

![Zeigt eine Formel für eine Drehungs Transformation an.](images/matrix11.png)

Der transformierte Punkt ist:

<dl> P ' = (*x* cos;– ysin-, *x* Sin;+ *y*-Nr.)
</dl>

Fest. Um anzuzeigen, dass P "eine Drehung darstellt, sollten Sie das folgende Diagramm in Erwägung gezogen.

![ein Diagramm, das die Drehung um den Ursprung anzeigt.](images/graphics24.png)

Gegeben:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)
</dt> <dd>

Der ursprüngliche Punkt, der transformiert werden soll.

</dd> <dt>

Dargestellt
</dt> <dd>

Der Winkel, der durch die Zeile (0,0) bis P gebildet wird.

</dd> <dt>

COS
</dt> <dd>

Der Winkel, um den (x, y) zum Ursprung gedreht werden soll.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')
</dt> <dd>

Der transformierte Punkt.

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Die Länge der Zeile (0,0) bis P. Auch der Radius des Kreises der Drehung.

</dd> </dl>

> [!Note]  
> Dieses Diagramm verwendet das in Geometry verwendete Standard Koordinatensystem, bei dem die positive y-Achse nach oben zeigt. Direct2D verwendet das Windows-Koordinatensystem, bei dem die positive y-Achse nach unten zeigt.

 

Der Winkel zwischen der x-Achse und der Zeile (0, 0) bis P ' ist. +. Die folgenden Identitäten enthalten:

<dl> x = R.  
y = R  
x ' = R cos (es +-Taste)  
y ' = R Sin (es +-Taste)  
</dl>

Lösen Sie nun für x ' und y ' in Bezug auf den Bereich. Durch die dreisprachigen Additions Formeln:

<dl> x ' = R (COS;cos;– Sin;Sin;) = rcos;cos. – rsin;Sin;  
y ' = R (SIN;COS;+ cos;Sin;) = rsin;cos;+ rcos;Sin;  
</dl>

Dabei wird Folgendes ersetzt:

<dl> x ' = xcos;– ysin;  
y ' = xsin;+ ycos;  
</dl>

Dies entspricht dem zuvor gezeigten transformierten Punkt P.

### <a name="rotation-around-an-arbitrary-point"></a>Drehung um einen beliebigen Punkt

Um einen anderen Punkt (x, y) als den Ursprung zu drehen, wird die folgende Matrix verwendet.

![Drehungs Transformation.](images/matrix13.png)

Sie können diese Matrix ableiten, indem Sie den Punkt (x, y) als Ursprung nehmen.

![ein Diagramm, das die Drehung um einen Punkt zeigt.](images/graphics25.png)

Let (x1, Y1) ist der Punkt, der sich aus dem Drehen des Punkts (X0, Y0) um den Punkt (x, y) ergibt. Wir können x1 wie folgt ableiten.

<dl> x1 = (X0 – x) cos;– (y0 – y) sin;+ x  
x1 = x0cosΘ – y0sinΘ + \[ (1 – cosbe) + ysin; \]  
</dl>

Binden Sie diese Gleichung nun wieder in die Transformationsmatrix ein, indem Sie die Formel x1 = ax0 + cy0 + e aus früheren Versionen verwenden. Verwenden Sie das gleiche Verfahren, um Y1 abzuleiten.

### <a name="skew-transform"></a>Verzerrungs Transformation

Die Schiefe Transformation wird durch vier Parameter definiert:

-   $: Der Betrag, der entlang der x-Achse verzerrt werden soll, gemessen als Winkel von der y-Achse.
-   Ge: der Betrag, der entlang der y-Achse verzerrt werden soll, gemessen als Winkel von der x-Achse.
-   (*px*, *py*): die x-und y-Koordinaten des Punkts, an dem die Schiefe ausgeführt wird.

Die Schiefe Transformation verwendet die folgende Matrix.

![Schiefe-Transformation.](images/matrix14.png)

Der transformierte Punkt ist:

<dl> P ' = (*x*  +  *y* Tangente – *py* tantzte, *y*  +  *x* Tangens) – *py* Tangens
</dl>

oder gleichwertig:

<dl> P ' = (*x* + (*y* – *py*) Tangente, *y* + (*x* – *px*) Tangens)
</dl>

Um zu sehen, wie diese Transformation funktioniert, sollten Sie jede Komponente einzeln in Erwägung gezogen. Der Parameter "-Parameter" verschiebt jeden Punkt in der x-Richtung um einen Betrag, der gleich der Tand ist. Das folgende Diagramm zeigt die Beziehung zwischen der-und der-Achse der x-Achse.

![Diagramm, das die Schiefe entlang der x-Achse anzeigt.](images/graphics26.png)

Dies ist die gleiche Schiefe, die auf ein Rechteck angewendet wird:

![Diagramm, das die Schiefe entlang der x-Achse anzeigt, wenn es auf ein Rechteck angewendet wird.](images/graphics27.png)

Der-Parameter hat denselben Effekt, aber entlang der y-Achse:

![Diagramm, das die Schiefe entlang der y-Achse anzeigt.](images/graphics28.png)

Das nächste Diagramm zeigt die auf ein Rechteck angewendete y-Achsen Schiefe.

![Diagramm, das die Schiefe entlang der y-Achse anzeigt, wenn es auf ein Rechteck angewendet wird.](images/graphics29.png)

Schließlich verschieben die Parameter *px* und *py* den Mittelpunkt für die Schiefe entlang der x-und y-Achse.

## <a name="representing-transforms-in-direct2d"></a>Darstellen von Transformationen in Direct2D

Alle Direct2D-Transformationen sind affine Transformationen. Direct2D unterstützt keine nicht affinen Transformationen. Transformationen werden durch die [**D2D1 \_ Matrix \_ 3x2 \_ F-**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) Struktur dargestellt. Diese Struktur definiert eine 3 × 2-Matrix. Da die dritte Spalte einer affinen Transformation immer identisch ist ( \[ 0, 0, 1 \] ) und da Direct2D keine nicht affinen Transformationen unterstützt, ist es nicht erforderlich, die gesamte 3 × 3-Matrix anzugeben. Intern verwendet Direct2D 3 × 3 Matrizen, um die Transformationen zu berechnen.

Die Member der [**D2D1 \_ Matrix \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) werden gemäß ihrer Indexposition benannt: das **\_ 11** -Element ist Element (1, 1), der **\_ 12** -Member ist Element (1, 2) usw. Obwohl Sie die Strukturmember direkt initialisieren können, empfiehlt es sich, die [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse zu verwenden. Diese Klasse erbt **D2D1 \_ Matrix \_ 3x2 \_ F** und stellt Hilfsmethoden zum Erstellen einer der grundlegenden affinen Transformationen bereit. Die-Klasse definiert auch [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) zum Verfassen von zwei oder mehr Transformationen, wie in [Anwenden von Transformationen in Direct2D](applying-transforms-in-direct2d.md)beschrieben.

## <a name="next"></a>Nächste

[Modul 4. Benutzereingabe](module-4--user-input.md)

 

 