---
description: Grafik Zustand &\# 8212; Clippingbereich, Transformationen und Qualitätseinstellungen &\# 8212; wird in einem Grafik Objekt gespeichert.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Grafikcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570857"
---
# <a name="graphics-containers"></a>Grafikcontainer

Grafik Zustand – Clippingbereich, Transformationen und Qualitätseinstellungen – wird in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt gespeichert. Windows GDI+ ermöglicht es Ihnen, einen Teil des Zustands in einem **Grafik** Objekt mithilfe eines Containers temporär zu ersetzen oder zu erweitern. Sie starten einen Container durch Aufrufen der [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) -Methode eines **Grafik** Objekts und Beenden einen Container durch Aufrufen der [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) -Methode. Zwischen **Grafiken:: BeginContainer** und **Graphics:: EndContainer** gehören alle Zustandsänderungen, die Sie am **Grafik** Objekt vornehmen, zum Container und überschreiben den vorhandenen Zustand des **Grafik** Objekts nicht.

Im folgenden Beispiel wird ein Container in einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt. Die globale Transformation des **Grafik** Objekts ist eine Übersetzung von 200 Einheiten auf der rechten Seite, und die weltweite Transformation des Containers ist eine Übersetzung von 100 Einheiten.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Beachten Sie, dass im vorherigen Beispiel die-Anweisung `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` zwischen den Aufrufen von [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) ein anderes Rechteck erzeugt als dieselbe Anweisung, die nach dem Aufruf von **Graphics:: EndContainer** erstellt wurde. Nur die horizontale Übersetzung gilt für den **drawrechteck** -Befehl, der außerhalb des Containers erstellt wurde. Beide Transformationen – die horizontale Übersetzung von 200 Einheiten und die vertikale Übersetzung von 100 Einheiten – gelten für die [**Grafiken::D rawrechteck**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Aufrufe innerhalb des Containers. Die folgende Abbildung zeigt die beiden Rechtecke.

![Screenshot eines Fensters mit zwei Rechtecke, die mit einem blauen Stift gezeichnet werden, einer mit der anderen Position](images/aboutgdip05-art17.png)

Container können in Containern geschachtelt werden. Im folgenden Beispiel wird ein Container innerhalb eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts und ein anderer Container innerhalb des ersten Containers erstellt. Die globale Transformation des **Grafik** Objekts ist eine Translation 100-Einheiten in der x-Richtung und 80-Einheiten in der y-Richtung. Die Welt Transformation des ersten Containers ist eine 30-Grad-Rotation. Die globale Transformation des zweiten Containers ist eine Skalierung mit einem Faktor von 2 in der x-Richtung. Ein aufzurufende [**Grafik::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) -Methode wird innerhalb des zweiten Containers erstellt.


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



Die folgende Abbildung zeigt die Ellipse.

![Screenshot eines Fensters, das eine gedrehte blaue Ellipse enthält, deren Mitte als (100, 80) bezeichnet wird](images/aboutgdip05-art18.png)

Beachten Sie, dass alle drei Transformationen auf die [**Grafiken zutreffen::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) -Aufrufe im zweiten Container (innersten). Beachten Sie auch die Reihenfolge der Transformationen: erste Skalierung, dann drehen und dann übersetzen. Die innerste Transformation wird zuerst angewendet, und die äußerste Transformation wird zuletzt angewendet.

Jede Eigenschaft eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts kann innerhalb eines Containers (zwischen den Aufrufen von [**Grafiken:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)) festgelegt werden. Beispielsweise kann ein Clippingbereich innerhalb eines Containers festgelegt werden. Jede im Container ausgeführte Zeichnung wird auf den Ausschneide Bereich dieses Containers beschränkt und wird auch auf die Ausschneide Bereiche beliebiger äußerer Container und den Ausschneide Bereich des **Grafik** Objekts beschränkt.

Die bisher erörterten Eigenschaften – die globale Transformation und der Clippingbereich – werden durch die Kombination aus den vorschangen Containern kombiniert. Andere Eigenschaften werden vorübergehend durch einen in einem Container ausgefallenen Container ersetzt. Wenn Sie z. b. den Glättungs Modus in einem Container auf "SmoothingModeAntiAlias" festlegen, verwenden alle in diesem Container aufgerufenen Zeichnungs Methoden den AntiAlias-Glättungs Modus, aber Zeichnungs Methoden, die nach " [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) " aufgerufen werden, verwenden den Glättungs Modus, der vor dem Aufruf von " [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))"

Ein weiteres Beispiel für die Kombination der weltweiten Transformationen eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts und eines Containers ist, dass Sie einen Augenblick zeichnen und an verschiedenen Positionen in einer Sequenz von Flächen platzieren möchten. Im folgenden Beispiel wird ein Auge gezeichnet, der sich am Ursprung des Koordinatensystems zentriert.


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



In der folgenden Abbildung sind die Augen-und Koordinatenachsen dargestellt.

![Darstellung eines Auges, das aus drei Ellipsen besteht: jeweils eine für die Kontur, Iris und Schülerin](images/aboutgdip05-art19.png)

Die im vorherigen Beispiel definierte DrawEye-Funktion empfängt die Adresse eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts und erstellt sofort einen Container in diesem **Grafik** Objekt. Dieser Container isoliert jeden Code, der die DrawEye-Funktion aus den Eigenschafts Einstellungen aufruft, die während der Ausführung der DrawEye-Funktion erstellt wurden. Beispielsweise legt der Code in der DrawEye-Funktion den Ausschneide Bereich des **Grafik** Objekts fest. wenn DrawEye jedoch die Steuerung an die aufrufende Routine zurückgibt, ist der Clippingbereich so, wie er vor dem Aufruf von DrawEye war.

Im folgenden Beispiel werden drei Ellipsen (Gesichter) gezeichnet, die jeweils einen Augenblick innerhalb von haben.


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



Die folgende Abbildung zeigt die drei Ellipsen.

![Screenshot eines Fensters mit drei Ellipsen, von denen jedes ein Auge auf eine andere Größe und Drehung enthält](images/aboutgdip05-art20.png)

Im vorherigen Beispiel werden alle Ellipsen mit dem-Befehl gezeichnet `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , der eine Ellipse zeichnet, die sich am Ursprung des Koordinatensystems zentriert. Die Ellipsen werden von der oberen linken Ecke des Client Bereichs durch Festlegen der Welt Transformation des [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts entfernt. Die-Anweisung bewirkt, dass die erste Ellipse um (100, 100) zentriert wird. Die-Anweisung bewirkt, dass der Mittelpunkt der zweiten Ellipse 100 Einheiten rechts neben der Mitte der ersten Ellipse ist. Ebenso ist der Mittelpunkt der dritten Ellipse 100 Einheiten rechts neben der Mitte der zweiten Ellipse.

Mithilfe der Container im vorherigen Beispiel wird das Auge relativ zum Mittelpunkt einer bestimmten Ellipse transformiert. Das erste Auge wird in der Mitte der Ellipse ohne Transformation gezeichnet, sodass sich der DrawEye-Befehl nicht in einem Container befindet. Das zweite Auge wird um 40 Grad gedreht und 30 Einheiten über dem Mittelpunkt der Ellipse gezeichnet, sodass die DrawEye-Funktion und die Methoden, die die Transformation festlegen, in einem Container aufgerufen werden. Das dritte Auge wird gestreckt, gedreht und in der Mitte der Ellipse gezeichnet. Wie beim zweiten Blick werden die DrawEye-Funktion und die Methoden, die die Transformation festlegen, in einem Container aufgerufen.

 

 
