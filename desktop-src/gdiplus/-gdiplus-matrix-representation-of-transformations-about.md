---
description: Eine m&215;n-Matrix ist ein Satz von Zahlen, die in m Zeilen und \# n Spalten angeordnet sind. Die folgende Abbildung zeigt mehrere Matrizen.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Matrixdarstellung von Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122d59787038cd75a9806cac6cb0d225e8660eb13d7482d3ee1f47ff0732ca5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036658"
---
# <a name="matrix-representation-of-transformations"></a>Matrixdarstellung von Transformationen

Eine *m×n-Matrix* ist ein Satz von Zahlen, die in *m* Zeilen und *n Spalten angeordnet* sind. Die folgende Abbildung zeigt mehrere Matrizen.

![Abbildung mit sechs Matrizen mit unterschiedlichen Dimensionen](images/aboutgdip05-art04.png)

Sie können zwei Matrizen derselben Größe hinzufügen, indem Sie einzelne Elemente hinzufügen. Die folgende Abbildung zeigt zwei Beispiele für das Hinzufügen von Matrizen.

![Abbildung, die zeigt, wie matrix addition](images/aboutgdip05-art05.png)

Eine *m×n-Matrix* kann mit einer *n×p-Matrix* multipiert werden, und das Ergebnis ist eine *m×p-Matrix.* Die Anzahl der Spalten in der ersten Matrix muss mit der Anzahl der Zeilen in der zweiten Matrix identisch sein. Beispielsweise kann eine 4 ×2-Matrix mit einer 2 ×3-Matrix multipliziert werden, um eine 4 ×3-Matrix zu erzeugen.

Punkte in der Ebene und Zeilen und Spalten einer Matrix können als Vektoren bezeichnet werden. Beispielsweise ist (2, 5) ein Vektor mit zwei Komponenten, und (3, 7, 1) ist ein Vektor mit drei Komponenten. Das Punktprodukt von zwei Vektoren ist wie folgt definiert:

(a, b) • (c, d) = ac + bd

(a, b, c) • (d, e, f) = ad + be + cf

Beispielsweise ist das Punktprodukt von (2, 3) und (5, 4) (2)(5) + (3)(4) = 22. Das Punktprodukt von (2, 5, 1) und (4, 3, 1) ist (2)(4) + (5)(3) + (1)(1) = 24. Beachten Sie, dass das Punktprodukt von zwei Vektoren eine Zahl und kein anderer Vektor ist. Beachten Sie auch, dass Sie das Punktprodukt nur berechnen können, wenn die beiden Vektoren die gleiche Anzahl von Komponenten haben.

Lassen Sie A(i, j) der Eintrag in Matrix A in der **ersten** Zeile und die Spalte j **th** sein. Beispielsweise ist A(3, 2) der Eintrag in Matrix A in der Zeile 3 **rd** und die **2.** Spalte. Angenommen, A, B und C sind Matrizen und AB = C. Die Einträge von C werden wie folgt berechnet:

C(i, j) = (Zeile i von A) • (Spalte j von B)

Die folgende Abbildung zeigt mehrere Beispiele für die Matrixmultiplikation.

![Abbildung zur Durchführung der Matrixmultiplikation](images/aboutgdip05-art06.png)

Wenn Sie sich einen Punkt in der Ebene als 1 × 2-Matrix denken, können Sie diesen Punkt transformieren, indem Sie ihn mit einer 2 × 2 Matrix multiplizieren. Die folgende Abbildung zeigt mehrere Transformationen, die auf den Punkt angewendet werden (2, 1).

![Abbildung zur Verwendung der Matrixmultiplikation zum Skalieren, Drehen oder Spiegeln eines Punkts in einer Ebene](images/aboutgdip05-art07.png)

Alle in der vorherigen Abbildung gezeigten Transformationen sind lineare Transformationen. Bestimmte andere Transformationen, z. B. die Übersetzung, sind nicht linear und können nicht als Multiplikation durch eine 2- × 2-Matrix ausgedrückt werden. Angenommen, Sie möchten mit dem Punkt (2, 1) beginnen, ihn um 90 Grad drehen, 3 Einheiten in x-Richtung übersetzen und 4 Einheiten in y-Richtung übersetzen. Sie können dies erreichen, indem Sie eine Matrixmultiplikation gefolgt von einer Matrixer addition ausführen.

![Abbildung, die zeigt, wie Matrixmultiplikation und Addition einen Punkt drehen und zweimal übersetzen können](images/aboutgdip05-art08.png)

Eine lineare Transformation (Multiplikation durch eine 2 × 2-Matrix) gefolgt von einer Übersetzung (Addition einer 1 × 2-Matrix) wird als affine Transformation bezeichnet. Eine Alternative zum Speichern einer affinen Transformation in einem Paar von Matrizen (eine für den linearen Teil und eine für die Übersetzung) besteht im Speichern der gesamten Transformation in einer 3- × 3-Matrix. Damit dies funktioniert, muss ein Punkt in der Ebene in einer 1-× 3-Matrix mit einer Dummy-3-Koordinate gespeichert werden. Die übliche Technik besteht in der Gleichung aller dritten Koordinaten auf 1. Beispielsweise wird der Punkt (2, 1) durch die Matrix \[ 2 1 1 \] dargestellt. Die folgende Abbildung zeigt eine affine Transformation (90 Grad drehen; 3 Einheiten in x-Richtung, 4 Einheiten in y-Richtung übersetzen), ausgedrückt als Multiplikation durch eine einzelne 3 × 3 Matrix.

![Abbildung, die zeigt, wie die Matrixmultiplikation eine affine Transformation ausführen kann](images/aboutgdip05-art09.png)

Im vorherigen Beispiel wird der Punkt (2, 1) dem Punkt (2, 6) zugeordnet. Beachten Sie, dass die dritte Spalte der 3 × 3-Matrix die Zahlen 0, 0, 1 enthält. Dies ist immer der Fall für die 3 × 3 Matrix einer affinen Transformation. Die wichtigen Zahlen sind die sechs Zahlen in den Spalten 1 und 2. Der obere linke 2 × 2 Teil der Matrix stellt den linearen Teil der Transformation dar, und die ersten beiden Einträge in der dritten Zeile stellen die Übersetzung dar.

![Abbildung, die zeigt, dass die ersten beiden Spalten für eine 3x3-Matrix einer affinen Transformation am wichtigsten sind](images/aboutgdip05-art10.png)

In Windows GDI+ Sie eine affine Transformation in einem [**Matrixobjekt**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) speichern. Da die dritte Spalte einer Matrix, die eine affine Transformation darstellt, immer ist (0, 0, 1), geben Sie beim Erstellen eines **Matrixobjekts** nur die sechs Zahlen in den ersten beiden Spalten an. Die `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` -Anweisung erstellt die in der vorherigen Abbildung gezeigte Matrix.

## <a name="composite-transformations"></a>Zusammengesetzte Transformationen

Eine zusammengesetzte Transformation ist eine Sequenz von Transformationen, eine gefolgt von der anderen. Betrachten Sie die Matrizen und Transformationen in der folgenden Liste:

-   Matrix A Um 90° drehen Grad
-   Matrix B Skalieren um den Faktor 2 in x-Richtung
-   Matrix C Translate 3 units in the y direction (Matrix C: 3 Einheiten in y-Richtung übersetzen)

Wenn Sie mit dem Punkt (2, 1) beginnen – dargestellt durch die Matrix 2 1 1 – und mit A multiplizieren, dann B, dann C, wird der Punkt \[ (2,1) den drei Transformationen in der aufgeführten Reihenfolge \] unterzogen.

\[2 1 1 \] ABC = \[ –2 5 1\]

Anstatt die drei Teile der zusammengesetzten Transformation in drei separaten Matrizen zu speichern, können Sie A, B und C multiplizieren, um eine einzelne 3 × 3-Matrix zu erhalten, die die gesamte zusammengesetzte Transformation speichert. Angenommen, ABC = D. Anschließend ergibt ein punkt multipliziert mit D das gleiche Ergebnis wie ein Punkt multipliziert mit A, dann B und dann C.

\[2 1 1 \] D = \[ –2 5 1\]

Die folgende Abbildung zeigt die Matrizen A, B, C und D.

![Abbildung: Ausführen mehrerer Transformationen durch Multiplizieren der konstituierenden Matrizen](images/aboutgdip05-art12.png)

Die Tatsache, dass die Matrix einer zusammengesetzten Transformation durch Multiplizieren der einzelnen Transformationsmatrizen gebildet werden kann, bedeutet, dass jede Sequenz von affinen Transformationen in einem einzelnen [**Matrixobjekt gespeichert werden**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) kann.

> [!Note]  
> Die Reihenfolge einer zusammengesetzten Transformation ist wichtig. Im Allgemeinen ist die Drehung, die Skalierung und die Übersetzung nicht mit der Skalierung identisch, und anschließend werden sie gedreht und übersetzt. Ebenso ist die Reihenfolge der Matrixmultiplikation wichtig. Im Allgemeinen ist ABC nicht mit BAC identisch.

 

Die [**Matrix-Klasse**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) bietet mehrere Methoden zum Erstellen einer zusammengesetzten Transformation: [**Matrix::Multiply,**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply) [**Matrix::Rotate,**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate) [**Matrix::RotateAt,**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat) [**Matrix::Scale,**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale) [**Matrix::Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)und [**Matrix::Translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). Im folgenden Beispiel wird die Matrix einer zusammengesetzten Transformation erstellt, die zuerst um 30 Grad gedreht wird, dann um den Faktor 2 in y-Richtung skaliert und dann 5 Einheiten in x-Richtung übersetzt.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



Die folgende Abbildung zeigt die Matrix.

![Abbildung, die eine Matrix mit Werten zeigt, die als trigonometrische Funktionen ausgedrückt werden, und eine Matrix mit ungefähren Werten dieser Funktionen](images/aboutgdip05-art13.png)

 

 



