---
description: Die PathGradientBrush-Klasse ermöglicht es Ihnen, die Art und Weise anzupassen, in der Sie eine Form ausfüllen.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Erstellen eines Pfad Farbverlaufs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551730"
---
# <a name="creating-a-path-gradient"></a>Erstellen eines Pfad Farbverlaufs

Die [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) -Klasse ermöglicht es Ihnen, die Art und Weise anzupassen, in der Sie eine Form ausfüllen. Ein **PathGradientBrush** -Objekt verfügt über einen Begrenzungs Pfad und einen Mittelpunkt. Sie können eine Farbe für den Mittelpunkt und eine andere Farbe für die Grenze angeben. Sie können auch separate Farben für jeden der einzelnen Punkte entlang der Grenze angeben.

> [!Note]  
> In GDI+ ist ein Pfad eine Sequenz von Linien und Kurven, die von einem [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt verwaltet werden. Weitere Informationen zu GDI+-Pfaden finden Sie unter [Pfade](-gdiplus-paths-about.md) und erstellen [und Zeichnen von Pfaden](-gdiplus-constructing-and-drawing-paths-use.md).

 

Im folgenden Beispiel wird eine Ellipse mit einem Pfad Farbverlaufs Pinsel gefüllt. Die Mittel Farbe ist auf Blau festgelegt, und die Begrenzungs Farbe ist auf Aqua festgelegt.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



Die folgende Abbildung zeigt die gefüllte Ellipse.

![Abbildung, die eine Ellipse mit einer Farbverlaufsfüllung anzeigt](images/pathgradient1.png)

Standardmäßig wird der Pinsel mit dem Pfad Farbverlauf nicht außerhalb der Grenze des Pfads erweitert. Wenn Sie den Pfad Farbverlaufs Pinsel zum Auffüllen einer Form verwenden, die über die Grenze des Pfads hinausgeht, wird der Bereich des Bildschirms außerhalb des Pfades nicht aufgefüllt. In der folgenden Abbildung wird gezeigt, was geschieht, wenn Sie den [**Grafik:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) -Aufrufe im vorangehenden Code in ändern `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .

![Abbildung eines horizontalen Slice der vorherigen Ellipse](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a>Angeben von Punkten an der Grenze

Im folgenden Beispiel wird ein Pfad Farbverlaufs Pinsel aus einem sternförmigen Pfad konstruiert. Der Code Ruft die [**PathGradientBrush:: setcentercolor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) -Methode auf, um die Farbe auf den Schwerpunkt des Sterns auf "rot" festzulegen. Anschließend ruft der Code die [**PathGradientBrush:: setsurroundcolors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) -Methode auf, um verschiedene Farben (im [**Farb**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) Array gespeichert) an den einzelnen Punkten im [**Points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) -Array anzugeben. Die abschließende Code Anweisung füllt den sternförmigen Pfad mit dem Pfad Farbverlaufs Pinsel.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
```



Die folgende Abbildung zeigt den gefüllten Stern.

![Abbildung mit einem fünf-Spitzen-Stern, der sich von rot in der Mitte in verschiedene Farben an jedem Punkt des Stern füllt](images/pathgradient3.png)

Im folgenden Beispiel wird ein Pfad Farbverlaufs Pinsel basierend auf einem Array von Punkten erstellt. Jedem der fünf Punkte im Array wird eine Farbe zugewiesen. Wenn Sie die fünf Punkte durch gerade Linien verbinden, erhalten Sie ein fünfseitiges Polygon. Außerdem wird der Mitte (Schwerpunkt) dieses Polygons eine Farbe zugewiesen – in diesem Beispiel wird das Mittelpunkt (80, 75) auf weiß festgelegt. Die abschließende Code Anweisung im Beispiel füllt ein Rechteck mit dem Pfad Farbverlaufs Pinsel.

Die Farbe, die zum Ausfüllen des Rechtecks verwendet wird, ist weiß at (80, 75) und ändert sich allmählich, wenn Sie von (80, 75) zu den Punkten im Array wechseln. Wenn Sie z. b. von (80, 75) zu (0,0) wechseln, ändert sich die Farbe allmählich von weiß in rot. während Sie von (80, 75) zu (160, 0) wechseln, ändert sich die Farbe allmählich von weiß zu grün.


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



Beachten Sie, dass im vorangehenden Code kein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt vorhanden ist. Der bestimmte [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) -Konstruktor im Beispiel empfängt einen Zeiger auf ein Array von Punkten, erfordert jedoch kein **GraphicsPath** -Objekt. Beachten Sie außerdem, dass der Pfad Farbverlaufs Pinsel zum Ausfüllen eines Rechtecks verwendet wird, nicht als Pfad. Das Rechteck ist größer als der Pfad, der zum Definieren des Pinsels verwendet wird, sodass einige des Rechtecks nicht durch den Pinsel gezeichnet werden. Die folgende Abbildung zeigt das Rechteck (gepunktete Linie) und den Teil des Rechtecks, gezeichnet durch den Pinsel mit dem Pfad Farbverlauf.

![Darstellung eines Rechtecks, das durch eine gepunktete Linie begrenzt ist, teilweise durch einen mehrfarbigen Farbverlauf gezeichnet](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a>Anpassen eines Pfad Farbverlaufs

Eine Möglichkeit, einen Pfad Farbverlaufs Pinsel anzupassen, besteht darin, die Skalierung des Fokus festzulegen. Die Fokus Skalen geben einen inneren Pfad an, der sich innerhalb des Haupt Pfads befindet. Die Mittel Farbe wird überall innerhalb dieses inneren Pfades anstelle des Mittelpunkts angezeigt. Um die Fokus Skalen eines Path-Farbverlaufs Pinsels festzulegen, müssen Sie die [**PathGradientBrush:: setfocusscales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) -Methode aufrufen.

Im folgenden Beispiel wird ein Pfad Farbverlaufs Pinsel auf der Grundlage eines elliptischen Pfads erstellt. Der Code legt die Begrenzungs Farbe auf blau fest, legt die Mittel Farbe auf Aqua fest und verwendet dann den Pfad Farbverlaufs Pinsel, um den Ellipsen Pfad auszufüllen.

Als nächstes legt der Code die Fokus Skalen des Pinsel mit dem Pfad Farbverlauf fest. Die x-Fokus Skala ist auf 0,3 festgelegt, und die y-Fokus Skala ist auf 0,8 festgelegt. Der Code Ruft die [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf, sodass der nachfolgende Aufruf von [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) eine Ellipse füllt, die sich rechts von der ersten Ellipse befindet.

Um die Auswirkung der Fokus Skalen anzuzeigen, stellen Sie sich eine kleine Ellipse vor, die das Zentrum mit der Haupt Ellipse teilt. Die kleine (innere) Ellipse ist die Hauptellipse, die horizontal um den Faktor 0,3 und vertikal um den Faktor 0,8 skaliert wird. Wenn Sie von der Grenze der äußeren Ellipse zur Grenze der inneren Ellipse wechseln, ändert sich die Farbe allmählich von blau zu Aqua. Wenn Sie von der Begrenzung der inneren Ellipse zum Shared Center wechseln, bleibt die Farbe Aqua.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes. Die Ellipse auf der linken Seite ist nur für Aqua am Mittelpunkt. Die Ellipse auf der rechten Seite ist Aqua Everywhere innerhalb des inneren Pfades.

![die Abbildung zeigt zwei Ellipsen, die von Aqua zu Blue schattiert werden: das erste hat nur sehr wenig Aqua. die zweite hat noch viel mehr](images/focusscales1.png)

Eine andere Möglichkeit zum Anpassen eines Farbverlaufs Pinsels besteht darin, ein Array von vordefinierten Farben und ein Array von Interpolations Positionen anzugeben.

Im folgenden Beispiel wird ein auf einem Dreieck basierender Pfad Farbverlauf erstellt. Der Code Ruft die Methode [**PathGradientBrush:: setinterpolationcolors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) des Pinsel mit dem Pfad Farbverlauf auf, um ein Array von Interpolations Farben (dunkelgrün, Aqua, Blue) und ein Array von Interpolations Positionen (0, 0,25, 1) anzugeben. Wenn Sie von der Grenze des Dreiecks zum Mittelpunkt wechseln, ändert sich die Farbe allmählich von Dunkelgrün zu Aqua und dann von Aqua zu blau. Die Änderung von Dunkelgrün zu Aqua erfolgt in 25 Prozent der Entfernung von Dunkelgrün zu blau.


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![die Abbildung zeigt ein Dreieck, das sich von blau in der Mitte, auf Aqua, auf grün an den Rändern schattiert.](images/pathgradient4.png)

## <a name="setting-the-center-point"></a>Festlegen des Mittelpunkts

Standardmäßig befindet sich der Mittelpunkt eines Pfad Farbverlaufs Pinsels im Schwerpunkt des Pfads, der zum Erstellen des Pinsels verwendet wird. Sie können den Speicherort des Mittelpunkts ändern, indem Sie die [**PathGradientBrush:: setcenterpoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) -Methode der [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) -Klasse aufrufen.

Im folgenden Beispiel wird ein auf einer Ellipse basierender Pfad Farbverlauf erstellt. Der Mittelpunkt der Ellipse liegt bei (70, 35), aber der Mittelpunkt des Farbverlaufs Pinsels ist auf (120, 40) festgelegt.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



In der folgenden Abbildung werden die gefüllten Ellipse und der Mittelpunkt des Pfads für den Pfad Farbverlauf angezeigt.

![Abbildung: eine Ellipse, die von einem Mittelpunkt in der Nähe eines Endes von blau zu Aqua füllt](images/pathgradient5.png)

Sie können den Mittelpunkt eines Farbverlaufs Pinsels auf einen Speicherort außerhalb des Pfads festlegen, der zum Erstellen des Pinsels verwendet wurde. Wenn Sie im vorangehenden Code den Aufrufen von [**PathGradientBrush:: setcenterpoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) durch ersetzen `pthGrBrush.SetCenterPoint(Point(145, 35))` , wird das folgende Ergebnis angezeigt.

![Abbildung, die eine Ellipse anzeigt, die von einem Mittelpunkt, der sich außerhalb des Rands der Ellipse befindet, von rot zu gelb ausfüllt](images/pathgradient6.png)

In der obigen Abbildung sind die Punkte ganz rechts von der Ellipse nicht rein blau (obwohl Sie sehr nah sind). Die Farben im Farbverlauf werden so positioniert, als ob die Füllung den Punkt erreichen würde (145, 35), die Farbe hätte rein blau (0, 0, 255) erreicht. Die Füllung erreicht jedoch nie (145, 35), da ein Pfad Farbverlaufs Pinsel nur innerhalb des Pfads zeichnet.

 

 
