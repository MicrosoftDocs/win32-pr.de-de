---
description: Um einen Pfad zu erstellen, erstellen Sie ein GraphicsPath-Objekt, und rufen Sie dann Methoden, wie z. b. AddLine und AddCurve, auf, um primitive dem Pfad hinzuzufügen.
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: Erstellen von Abbildungen Figuren aus Linien, Kurven und Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c473dfececcaa86347dc02efdfd62131eb9a63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959455"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a>Erstellen von Abbildungen Figuren aus Linien, Kurven und Formen

Um einen Pfad zu erstellen, erstellen Sie ein [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt, und rufen Sie dann Methoden, wie z. b. [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) und [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), auf, um primitive dem Pfad hinzuzufügen.

Im folgenden Beispiel wird ein Pfad mit einem einzelnen Bogen erstellt. Der Bogen hat einen Mittelpunktswinkel von – 180 Grad, der im Standard Koordinatensystem gegen den Uhrzeigersinn steht.


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



Im folgenden Beispiel wird ein Pfad mit zwei Abbildungen erstellt. Die erste Abbildung ist ein Bogen, gefolgt von einer Zeile. Die zweite Abbildung ist eine Zeile, auf die eine Kurve folgt, gefolgt von einer Zeile. Die erste Abbildung ist links geöffnet, und die zweite Abbildung ist geschlossen.


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



Zusätzlich zum Hinzufügen von Linien und Kurven zu Pfaden können Sie geschlossene Formen hinzufügen: Rechtecke, Ellipsen, Torten und Polygone. Im folgenden Beispiel wird ein Pfad mit zwei Zeilen erstellt, einem Rechteck und einer Ellipse. Der Code verwendet einen Stift zum Zeichnen des Pfads und einen Pinsel, um den Pfad auszufüllen.


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



Der Pfad im vorangehenden Beispiel enthält drei Abbildungen. Die erste Abbildung besteht aus den beiden Zeilen, die zweite Abbildung besteht aus dem Rechteck, und die dritte Abbildung besteht aus der Ellipse. Auch wenn es keine Aufrufe von [**GraphicsPath:: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) oder [**GraphicsPath:: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure)gibt, werden intrinsisch geschlossene Formen, wie z. b. Rechtecke und Ellipsen, als separate Abbildungen behandelt.

 

 



