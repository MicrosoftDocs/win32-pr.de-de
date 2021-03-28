---
description: Eine globale Transformation ist eine Transformation, die auf jedes Element angewendet wird, das von einem angegebenen Grafik Objekt gezeichnet wird.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Globale und lokale Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551226"
---
# <a name="global-and-local-transformations"></a>Globale und lokale Transformationen

Eine globale Transformation ist eine Transformation, die auf jedes Element angewendet wird, das von einem angegebenen [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt gezeichnet wird. Um eine globale Transformation zu erstellen, erstellen Sie ein **Grafik** Objekt, und rufen Sie dann die zugehörige [**Graphics:: setTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) -Methode auf. Die **Graphics:: setTransform** -Methode manipuliert ein [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt, das dem **Grafik** Objekt zugeordnet ist. Die in diesem **Matrix** Objekt gespeicherte Transformation wird als *weltweite Transformation* bezeichnet. Die Welt Transformation kann eine einfache affine Transformation oder eine komplexe Sequenz von affinen Transformationen sein, aber unabhängig von ihrer Komplexität ist die globale Transformation in einem einzigen **Matrix** Objekt gespeichert.

Die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse bietet mehrere Methoden zum Aufbauen einer zusammengesetzten Welt Transformation: [**Graphics:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)und [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform). Im folgenden Beispiel wird eine Ellipse zweimal gezeichnet: einmal vor dem Erstellen einer Welt Transformation und einmal nach. Die Transformation skaliert zuerst mit dem Faktor 0,5 in der y-Richtung, übersetzt dann 50 Einheiten in die x-Richtung und dreht dann 30 Grad.


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



Die folgende Abbildung zeigt die ursprüngliche Ellipse und die transformierte Ellipse.

![Screenshot eines Fensters, das zwei überlappende Ellipsen enthält. eine ist schmaler und rotiert.](images/aboutgdip05-art14.png)

> [!Note]  
> Im vorherigen Beispiel wird die Ellipse um den Ursprung des Koordinatensystems gedreht, das sich in der oberen – linken Ecke des Client Bereichs befindet. Dies führt zu einem anderen Ergebnis als das Drehen der Ellipse über einen eigenen Mittelpunkt.

 

Eine lokale Transformation ist eine Transformation, die auf ein bestimmtes Element angewendet wird, das gezeichnet werden soll. Ein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt verfügt beispielsweise über eine [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) -Methode, die es Ihnen ermöglicht, die Datenpunkte dieses Pfades zu transformieren. Im folgenden Beispiel wird ein Rechteck ohne Transformation und ein Pfad mit einer Rotations Transformation gezeichnet. (Angenommen, es gibt keine Welt Transformation.)


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Sie können die Welt Transformation mit lokalen Transformationen kombinieren, um eine Vielzahl von Ergebnissen zu erzielen. Beispielsweise können Sie mit der Welt Transformation das Koordinatensystem überarbeiten und lokale Transformationen verwenden, um Objekte zu drehen und zu skalieren, die auf dem neuen Koordinatensystem gezeichnet werden.

Angenommen, Sie möchten ein Koordinatensystem, dessen Ursprung 200 Pixel vom linken Rand des Client Bereichs und 150 Pixel vom oberen Rand des Client Bereichs hat. Angenommen, Sie möchten, dass die Maßeinheit das Pixel ist, wobei die x-Achse nach rechts und die y-Achse nach oben zeigt. Beim Standard Koordinatensystem wird die y-Achse nach unten angezeigt, sodass Sie eine Reflektion auf der horizontalen Achse ausführen müssen. Die folgende Abbildung zeigt die Matrix einer solchen Reflektion.

![Abbildung: eine drei-nach-3-Matrix](images/aboutgdip05-art15.png)

Nehmen wir als nächstes an, dass Sie eine Translation 200-Einheiten nach rechts und 150-Einheiten ausführen müssen.

Im folgenden Beispiel wird das Koordinatensystem festgelegt, das gerade durch Festlegen der Welt Transformation eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts beschrieben wird.


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



Der folgende Code (nach dem Code im vorangehenden Beispiel eingefügt) erstellt einen Pfad, der aus einem einzelnen Rechteck mit der unteren linken Ecke am Ursprung des neuen Koordinatensystems besteht. Das Rechteck wird einmal ohne lokale Transformation und einmal mit einer lokalen Transformation aufgefüllt. Die lokale Transformation besteht aus einer horizontalen Skalierung mit dem Faktor 2, gefolgt von einer 30-Grad-Drehung.


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



Die folgende Abbildung zeigt das neue Koordinatensystem und die beiden Rechtecke.

![Screenshot einer x-und y-Achse, und ein blaues Quadrat, das von einem semitransparenten rectagle überlagert wurde um die linke untere Ecke gedreht](images/aboutgdip05-art16.png)

 

 



