---
description: Ein einzelnes Matrix Objekt kann eine einzelne Transformation oder eine Sequenz von Transformationen speichern.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Bedeutung der Transformationsreihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977528"
---
# <a name="why-transformation-order-is-significant"></a>Bedeutung der Transformationsreihenfolge

Ein einzelnes [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt kann eine einzelne Transformation oder eine Sequenz von Transformationen speichern. Letzteres wird als zusammen *gesetzte*  *Transformation* bezeichnet. Die Matrix einer zusammengesetzten Transformation wird durch Multiplikation der Matrizen der einzelnen Transformationen abgerufen.

In einer zusammengesetzten Transformation ist die Reihenfolge der einzelnen Transformationen wichtig. Wenn Sie z. b. zuerst drehen, dann skalieren und dann übersetzen, erhalten Sie ein anderes Ergebnis als bei der ersten Übersetzung, dann drehen und skalieren. In Windows GDI+ werden zusammengesetzte Transformationen von links nach rechts erstellt. Wenn es sich bei S, R und T um Skalierungs-, Rotations-und Übersetzungs Matrizen handelt, ist das Produkt SRT (in dieser Reihenfolge) die Matrix der zusammengesetzten Transformation, die zuerst skaliert, dann rotiert und dann übersetzt. Die vom Produkt SRT erzeugte Matrix unterscheidet sich von der Matrix, die vom Produkt TRS erzeugt wird.

Eine Grundordnung ist wichtig, wenn Transformationen wie Drehung und Skalierung in Bezug auf den Ursprung des Koordinatensystems ausgeführt werden. Das Skalieren eines Objekts, das am Ursprung zentriert ist, erzeugt ein anderes Ergebnis als das Skalieren eines Objekts, das vom Ursprung entfernt wurde. Entsprechend erzeugt das Drehen eines Objekts, das am Ursprung zentriert ist, ein anderes Ergebnis als das Drehen eines Objekts, das vom Ursprung entfernt wurde.

Im folgenden Beispiel werden die Skalierung, Drehung und Übersetzung (in dieser Reihenfolge) kombiniert, um eine zusammengesetzte Transformation zu bilden. Das Argument [* * * matrixorderappend * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) , das an die [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) -Methode übermittelt wird, gibt an, dass die Drehung der Skalierung folgt. Ebenso gibt das Argument [* * * matrixorderappend * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) , das an die [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) -Methode übergebenen wird, an, dass die Übersetzung der Drehung folgt.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Im folgenden Beispiel wird dieselbe Methode wie im vorherigen Beispiel aufgerufen, aber die Reihenfolge der Aufrufe wird umgekehrt. Die sich ergebende Reihenfolge der Vorgänge erfolgt zunächst übersetzen, dann drehen, dann skalieren, was zu einem sehr anderen Ergebnis als der ersten Skalierung, zum anschließenden drehen und zum Übersetzen führt:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Eine Möglichkeit, die Reihenfolge der einzelnen Transformationen in einer zusammengesetzten Transformation umzukehren, besteht darin, die Reihenfolge einer Sequenz von Methoden aufrufen umzukehren. Eine zweite Möglichkeit, die Reihenfolge der Vorgänge zu steuern, besteht darin, das Matrix Reihen folgen Argument zu ändern. Das folgende Beispiel ist mit dem vorherigen Beispiel identisch, mit der Ausnahme, dass [* * * * matrixorderappend * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) in [* * * * matrixorderprepend * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)* geändert wurde. Die Matrix Multiplikation erfolgt in der Reihenfolge SRT, in der "S", "R" und "T" die Matrizen für "Scale", "Rotation" und "Translation" sind. Die Reihenfolge der zusammengesetzten Transformation ist die erste Skalierung, dann drehen und dann übersetzen.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



Das Ergebnis des vorhergehenden Beispiels ist das gleiche Ergebnis, das wir im ersten Beispiel dieses Abschnitts erzielt haben. Dies liegt daran, dass wir sowohl die Reihenfolge der Methodenaufrufe als auch die Reihenfolge der Matrix Multiplikation rückgängig gemacht haben.

 

 



