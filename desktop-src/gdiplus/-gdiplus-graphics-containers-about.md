---
description: Der Grafikzustand &\# 8212; Clippingbereich, Transformationen und Qualitätseinstellungen &\# 8212; wird in einem Grafikobjekt gespeichert.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Grafikcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26af00a17f793a1f3ce587963343556b8c4ad685f930b707bd81de1008d610ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248669"
---
# <a name="graphics-containers"></a>Grafikcontainer

Der Grafikzustand – Clippingbereich, Transformationen und Qualitätseinstellungen – wird in einem [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gespeichert. Windows GDI+ ermöglicht es Ihnen, einen Teil des Zustands in einem **Graphics-Objekt** mithilfe eines Containers vorübergehend zu ersetzen oder zu erweitern. Sie starten einen Container, indem Sie die [**Graphics::BeginContainer-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) eines **Graphics-Objekts** aufrufen, und Sie beenden einen Container, indem Sie die [**Graphics::EndContainer-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) aufrufen. Zwischen **Graphics::BeginContainer** und **Graphics::EndContainer** gehören alle Zustandsänderungen, die Sie am **Graphics-Objekt** vornehmen, zum Container und überschreiben nicht den vorhandenen Zustand des **Graphics-Objekts.**

Im folgenden Beispiel wird ein Container in einem [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) erstellt. Die weltumwandlung des **Grafikobjekts** ist eine Übersetzung von 200 Einheiten nach rechts, und die weltweite Transformation des Containers ist eine Übersetzung von 100 Einheiten nach unten.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Beachten Sie, dass im vorherigen Beispiel die `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` -Anweisung zwischen den Aufrufen von [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) ein anderes Rechteck erzeugt als die gleiche Anweisung, die nach dem Aufruf von **Graphics::EndContainer** erfolgt ist. Nur die horizontale Übersetzung gilt für den **DrawRectangle-Aufruf,** der außerhalb des Containers erfolgt. Beide Transformationen – die horizontale Übersetzung von 200 Einheiten und die vertikale Übersetzung von 100 Einheiten – gelten für den [**Graphics::D rawRectangle-Aufruf**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) im Container. Die folgende Abbildung zeigt die beiden Rechtecke.

![Screenshot eines Fensters mit zwei Rechtecke, die mit einem blauen Stift gezeichnet wurden, eines über dem anderen positioniert](images/aboutgdip05-art17.png)

Container können in Containern geschachtelt werden. Im folgenden Beispiel wird ein Container in einem [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein weiterer Container innerhalb des ersten Containers erstellt. Die Welttransformation des **Grafikobjekts** ist eine Übersetzung von 100 Einheiten in x- und 80 Einheiten in y-Richtung. Die weltweite Transformation des ersten Containers ist eine Drehung um 30 Grad. Die weltweite Transformation des zweiten Containers ist eine Skalierung um den Faktor 2 in x Richtung. Die [**Graphics::D rawEllipse-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) wird im zweiten Container aufgerufen.


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

![Screenshot eines Fensters, das eine gedrehte blaue Ellipse mit der zentrierten Bezeichnung (100,80) enthält](images/aboutgdip05-art18.png)

Beachten Sie, dass alle drei Transformationen für den [**Graphics::D rawEllipse-Aufruf**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) gelten, der im zweiten (innersten) Container erfolgt. Beachten Sie auch die Reihenfolge der Transformationen: zuerst skalieren, dann drehen und dann übersetzen. Die innerste Transformation wird zuerst angewendet, und die äußerste Transformation wird zuletzt angewendet.

Jede Eigenschaft eines [**Graphics-Objekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) kann innerhalb eines Containers festgelegt werden (zwischen Aufrufen von [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) und [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Beispielsweise kann ein Clippingbereich innerhalb eines Containers festgelegt werden. Alle im Container ausgeführten Zeichnungen sind auf den Ausschneidebereich dieses Containers und auch auf die Ausschneidebereiche von äußeren Containern und den Ausschneidebereich des **Grafikobjekts** selbst beschränkt.

Die bisher besprochenen Eigenschaften – die Transformation für die Welt und der Clippingbereich – werden durch geschachtelte Container kombiniert. Andere Eigenschaften werden vorübergehend durch einen geschachtelten Container ersetzt. Wenn Sie z. B. den Glättungsmodus in einem Container auf SmoothingModeAntiAlias festlegen, verwenden alle in diesem Container aufgerufenen Zeichnungsmethoden den Glättungsmodus antialias. Zeichenmethoden, die nach [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) aufgerufen werden, verwenden jedoch den Glättungsmodus, der vor dem Aufruf von [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))vorhanden war.

Ein weiteres Beispiel für die Kombination der Welttransformationen eines [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und eines Containers: Angenommen, Sie möchten ein Auge zeichnen und es an verschiedenen Stellen auf einer Sequenz von Gesichtern platzieren. Im folgenden Beispiel wird ein Auge zentriert am Ursprung des Koordinatensystems zentriert.


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



Die folgende Abbildung zeigt das Auge und die Koordinatenachsen.

![Abbildung, die ein Auge zeigt, das aus drei Ellipsen besteht: jeweils eins für kontur, iris und ellipse](images/aboutgdip05-art19.png)

Die im vorherigen Beispiel definierte DrawEye-Funktion empfängt die Adresse eines [**Graphics-Objekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und erstellt sofort einen Container in diesem **Graphics-Objekt.** Dieser Container isoliert jeglichen Code, der die DrawEye-Funktion aufruft, von den Eigenschafteneinstellungen, die während der Ausführung der DrawEye-Funktion vorgenommen wurden. Code in der DrawEye-Funktion legt z. B. den Clippingbereich des **Graphics-Objekts** fest, aber wenn DrawEye das Steuerelement an die aufrufende Routine zurückgibt, ist der Clippingbereich wie vor dem Aufruf von DrawEye.

Im folgenden Beispiel werden drei Ellipsen (Gesichter) mit jeweils einem Inneren des Auges gezogen.


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



Die folgende Abbildung zeigt die drei Ausellipsen.

![Screenshot eines Fensters mit drei Ausellipsen, von denen jede ein Auge mit einer anderen Größe und Drehung enthält](images/aboutgdip05-art20.png)

Im vorherigen Beispiel werden alle Ellipsen mit dem Aufruf gezeichnet, der `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` eine Ellipse zeichnet, die am Ursprung des Koordinatensystems zentriert ist. Die Ellipsen werden von der oberen linken Ecke des Clientbereichs entfernt, indem die Welttransformation des [**Grafikobjekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) festgelegt wird. Die -Anweisung bewirkt, dass die erste Ellipse auf (100, 100) zentriert wird. Die -Anweisung bewirkt, dass der Mittelpunkt der zweiten Ellipse 100 Einheiten rechts von der Mitte der ersten Ellipse ist. Ebenso beträgt der Mittelpunkt der dritten Ellipse 100 Einheiten rechts von der Mitte der zweiten Ellipse.

Die Container im vorherigen Beispiel werden verwendet, um das Auge relativ zur Mitte einer angegebenen Ellipse zu transformieren. Das erste Auge wird in der Mitte der Ellipse ohne Transformation gezeichnet, sodass sich der DrawEye-Aufruf nicht in einem Container befindet. Das zweite Auge wird um 40 Grad gedreht und 30 Einheiten über der Mitte der Ellipse gezeichnet, sodass die DrawEye-Funktion und die Methoden, die die Transformation festlegen, in einem Container aufgerufen werden. Das dritte Auge wird gestreckt und gedreht und in der Mitte der Ellipse gezeichnet. Wie beim zweiten Auge werden die DrawEye-Funktion und die Methoden, die die Transformation festlegen, in einem Container aufgerufen.

 

 
