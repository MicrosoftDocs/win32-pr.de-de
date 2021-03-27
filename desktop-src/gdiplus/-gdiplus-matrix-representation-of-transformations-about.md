---
description: Eine m&\# 215; n-Matrix ist ein Satz von Zahlen, der in m Zeilen und n Spalten angeordnet ist. Die folgende Abbildung zeigt mehrere Matrizen.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Matrixdarstellung von Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751336"
---
# <a name="matrix-representation-of-transformations"></a>Matrixdarstellung von Transformationen

Eine *m × n* -Matrix ist ein Satz von Zahlen, der in *m* Zeilen und *n* Spalten angeordnet ist. Die folgende Abbildung zeigt mehrere Matrizen.

![Darstellung von sechs Matrizen unterschiedlicher Dimensionen](images/aboutgdip05-art04.png)

Sie können zwei Matrizen derselben Größe hinzufügen, indem Sie einzelne Elemente hinzufügen. Die folgende Abbildung zeigt zwei Beispiele für das Hinzufügen von Matrizen.

![Abbildung, die zeigt, wie Matrix Addition durchgeführt wird](images/aboutgdip05-art05.png)

Eine *m × n* -Matrix kann mit einer *n × p* -Matrix multipliziert werden, und das Ergebnis ist eine *m × p* -Matrix. Die Anzahl der Spalten in der ersten Matrix muss mit der Anzahl der Zeilen in der zweiten Matrix identisch sein. Beispielsweise kann eine 4 × 2-Matrix mit einer 2 × 3-Matrix multipliziert werden, um eine 4 × 3-Matrix zu schaffen.

Punkte in der Ebene und die Zeilen und Spalten einer Matrix können als Vektoren betrachtet werden. (2, 5) ist z. b. ein Vektor mit zwei Komponenten, und (3, 7, 1) ist ein Vektor mit drei Komponenten. Das Punktprodukt von zwei Vektoren wird wie folgt definiert:

(a, b) • (c, d) = AC + BD

(a, b, c) • (d, e, f) = AD + be + CF

Beispielsweise ist das Punktprodukt von (2, 3) und (5, 4) (2) (5) + (3) (4) = 22. Das Punktprodukt von (2, 5, 1) und (4, 3, 1) ist (2) (4) + (5) (3) + (1) (1) = 24. Beachten Sie, dass es sich bei dem Punktprodukt zweier Vektoren um eine Zahl, nicht um einen anderen Vektor handelt. Beachten Sie außerdem, dass Sie das Punktprodukt nur berechnen können, wenn die beiden Vektoren über die gleiche Anzahl von Komponenten verfügen.

Let a (i, j) ist der Eintrag in Matrix A in der Zeile i **th** und in der **Spalte j.** Beispielsweise ist a (3, 2) der Eintrag in Matrix A in der 3-**RD** -Zeile und in **der Spalte 2.** Angenommen, a, B und C sind Matrizen, und ab = c. Die Einträge von C werden wie folgt berechnet:

C (i, j) = (Zeile i von a) • (Spalte j von B)

Die folgende Abbildung zeigt mehrere Beispiele für die Matrix Multiplikation.

![Darstellung der Matrix Multiplikation](images/aboutgdip05-art06.png)

Wenn Sie sich einen Punkt in der Ebene als 1 × 2-Matrix vorstellen, können Sie diesen Punkt transformieren, indem Sie ihn mit einer 2 × 2-Matrix multiplizieren. Die folgende Abbildung zeigt mehrere Transformationen, die auf den Punkt (2, 1) angewendet werden.

![Abbildung, die zeigt, wie die Matrix Multiplikation verwendet wird, um einen Punkt in einer Ebene zu skalieren, zu drehen oder wiederzugeben](images/aboutgdip05-art07.png)

Alle in der vorherigen Abbildung gezeigten Transformationen sind lineare Transformationen. Bestimmte andere Transformationen, z. b. die Übersetzung, sind nicht linear und können nicht durch eine 2 × 2-Matrix als Multiplikation ausgedrückt werden. Angenommen, Sie möchten mit dem Punkt (2, 1) beginnen, ihn um 90 Grad drehen, 3 Einheiten in die x-Richtung übersetzen und vier Einheiten in y-Richtung übersetzen. Dies erreichen Sie, indem Sie eine Matrix Multiplikation ausführen, gefolgt von einer Matrix Addition.

![Abbildung, die zeigt, wie die Matrix Multiplikation und Addition einen Punkt drehen und zweimal übersetzen können](images/aboutgdip05-art08.png)

Eine lineare Transformation (Multiplikation durch eine 2 × 2-Matrix), gefolgt von einer Übersetzung (Addition einer 1 × 2-Matrix), wird als affine Transformation bezeichnet. Eine Alternative zum Speichern einer affinen Transformation in einem Matrizen-Paar (eines für den linearen Teil und eines für die Übersetzung) ist das Speichern der gesamten Transformation in einer 3 × 3-Matrix. Um dies zu ermöglichen, muss ein Punkt in der Ebene in einer 1 × 3-Matrix mit einer Dummy-Dritt-Koordinate gespeichert werden. Die übliche Vorgehensweise besteht darin, alle Dritt-Koordinaten gleich 1 zu erstellen. Der Punkt (2, 1) wird z. b. durch die Matrix \[ 2 1 1 dargestellt \] . Die folgende Abbildung zeigt eine affine Transformation (Drehen von 90 Grad) und übersetzt 3 Einheiten in der x-Richtung, 4 Einheiten in der y-Richtung), die durch eine einzelne 3 × 3-Matrix als Multiplikation ausgedrückt werden.

![Abbildung, die zeigt, wie die Matrix Multiplikation eine affine Transformation ausführen kann](images/aboutgdip05-art09.png)

Im vorherigen Beispiel wird der Punkt (2, 1) dem Punkt (2, 6) zugeordnet. Beachten Sie, dass die dritte Spalte der 3 × 3-Matrix die Zahlen 0, 0, 1 enthält. Dies ist immer die Groß-/Kleinschreibung für die 3 × 3-Matrix einer affinen Transformation. Die wichtigsten Zahlen sind die sechs Zahlen in den Spalten 1 und 2. Der obere linke 2 × 2-Teil der Matrix stellt den linearen Teil der Transformation dar, und die ersten beiden Einträge in der dritten Zeile stellen die Übersetzung dar.

![Abbildung, die anzeigt, dass die ersten beiden Spalten für eine 3X3-Matrix einer affinen Transformation am signifikantesten sind](images/aboutgdip05-art10.png)

In Windows GDI+ können Sie eine affine Transformation in einem [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt speichern. Da die dritte Spalte einer Matrix, die eine affine-Transformation darstellt, immer (0, 0, 1) ist, geben Sie nur die sechs Zahlen in den ersten beiden Spalten an, wenn Sie ein **Matrix** Objekt erstellen. Die-Anweisung erstellt `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` die in der vorherigen Abbildung gezeigte Matrix.

## <a name="composite-transformations"></a>Zusammengesetzte Transformationen

Eine zusammengesetzte Transformation ist eine Sequenz von Transformationen, von denen eine nacheinander folgt. Beachten Sie die Matrizen und Transformationen in der folgenden Liste:

-   Matrix Drehung um 90 Grad
-   Matrix B Skalieren mit dem Faktor 2 in der x-Richtung
-   Matrix C übersetzt 3 Einheiten in y-Richtung.

Wenn Sie mit dem Punkt (2, 1) – dargestellt durch die Matrix \[ 2 1 1 \] – und Multiplizieren von a, dann C, wird der Punkt (2, 1) die drei Transformationen in der aufgelisteten Reihenfolge durchlaufen.

\[2 1 1 \] ABC = \[ – 2 5 1\]

Anstatt die drei Teile der zusammengesetzten Transformation in drei separaten Matrizen zu speichern, können Sie a, B und C zusammen multiplizieren, um eine einzelne 3 × 3-Matrix zu erhalten, in der die gesamte zusammengesetzte Transformation gespeichert wird. Angenommen, ABC = D. Ein Punkt, der mit D multipliziert ist, gibt das gleiche Ergebnis wie ein Punkt multipliziert mit a, dann B und dann C.

\[2 1 1 \] D = \[ – 2 5 1\]

Die folgende Abbildung zeigt die Matrizen A, B, C und D.

![Darstellung der Durchführung mehrerer Transformationen durch Multiplizieren der einzelnen Matrizen](images/aboutgdip05-art12.png)

Die Tatsache, dass die Matrix einer zusammengesetzten Transformation durch Multiplizieren der einzelnen Transformations Matrizen gebildet werden kann, bedeutet, dass jede Sequenz von affinen Transformationen in einem einzelnen [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt gespeichert werden kann.

> [!Note]  
> Die Reihenfolge einer zusammengesetzten Transformation ist wichtig. Im Allgemeinen ist die Drehung, Skalierung und Übersetzung nicht dasselbe wie die Skalierung, dann drehen und übersetzen. Ebenso ist die Reihenfolge der Matrix Multiplikation wichtig. Im Allgemeinen ist ABC nicht mit der Bac identisch.

 

Die [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Klasse bietet mehrere Methoden zum Aufbauen einer zusammengesetzten Transformation: [**Matrix:: Multiplizieren**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix:: Rotation**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix:: RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix:: Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix:: Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)und [**Matrix:: Translation**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). Im folgenden Beispiel wird die Matrix einer zusammengesetzten Transformation erstellt, die zuerst 30 Grad rotiert, dann mit einem Faktor von 2 in der y-Richtung skaliert und dann 5 Einheiten in der x-Richtung übersetzt.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



Die folgende Abbildung zeigt die Matrix.

![die Abbildung zeigt eine Matrix mit Werten, die als drei-und-Werte ausgedrückt werden, und eine Matrix mit ungefähren Werten dieser Funktionen.](images/aboutgdip05-art13.png)

 

 



