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
# <a name="creating-a-path-gradient"></a><span data-ttu-id="beb87-103">Erstellen eines Pfad Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="beb87-103">Creating a Path Gradient</span></span>

<span data-ttu-id="beb87-104">Die [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) -Klasse ermöglicht es Ihnen, die Art und Weise anzupassen, in der Sie eine Form ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="beb87-104">The [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class allows you to customize the way you fill a shape with gradually changing colors.</span></span> <span data-ttu-id="beb87-105">Ein **PathGradientBrush** -Objekt verfügt über einen Begrenzungs Pfad und einen Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="beb87-105">A **PathGradientBrush** object has a boundary path and a center point.</span></span> <span data-ttu-id="beb87-106">Sie können eine Farbe für den Mittelpunkt und eine andere Farbe für die Grenze angeben.</span><span class="sxs-lookup"><span data-stu-id="beb87-106">You can specify one color for the center point and another color for the boundary.</span></span> <span data-ttu-id="beb87-107">Sie können auch separate Farben für jeden der einzelnen Punkte entlang der Grenze angeben.</span><span class="sxs-lookup"><span data-stu-id="beb87-107">You can also specify separate colors for each of several points along the boundary.</span></span>

> [!Note]  
> <span data-ttu-id="beb87-108">In GDI+ ist ein Pfad eine Sequenz von Linien und Kurven, die von einem [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="beb87-108">In GDI+, a path is a sequence of lines and curves maintained by a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="beb87-109">Weitere Informationen zu GDI+-Pfaden finden Sie unter [Pfade](-gdiplus-paths-about.md) und erstellen [und Zeichnen von Pfaden](-gdiplus-constructing-and-drawing-paths-use.md).</span><span class="sxs-lookup"><span data-stu-id="beb87-109">For more information about GDI+ paths, see [Paths](-gdiplus-paths-about.md) and [Constructing and Drawing Paths](-gdiplus-constructing-and-drawing-paths-use.md).</span></span>

 

<span data-ttu-id="beb87-110">Im folgenden Beispiel wird eine Ellipse mit einem Pfad Farbverlaufs Pinsel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="beb87-110">The following example fills an ellipse with a path gradient brush.</span></span> <span data-ttu-id="beb87-111">Die Mittel Farbe ist auf Blau festgelegt, und die Begrenzungs Farbe ist auf Aqua festgelegt.</span><span class="sxs-lookup"><span data-stu-id="beb87-111">The center color is set to blue and the boundary color is set to aqua.</span></span>


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



<span data-ttu-id="beb87-112">Die folgende Abbildung zeigt die gefüllte Ellipse.</span><span class="sxs-lookup"><span data-stu-id="beb87-112">The following illustration shows the filled ellipse.</span></span>

![Abbildung, die eine Ellipse mit einer Farbverlaufsfüllung anzeigt](images/pathgradient1.png)

<span data-ttu-id="beb87-114">Standardmäßig wird der Pinsel mit dem Pfad Farbverlauf nicht außerhalb der Grenze des Pfads erweitert.</span><span class="sxs-lookup"><span data-stu-id="beb87-114">By default, a path gradient brush does not extend outside the boundary of the path.</span></span> <span data-ttu-id="beb87-115">Wenn Sie den Pfad Farbverlaufs Pinsel zum Auffüllen einer Form verwenden, die über die Grenze des Pfads hinausgeht, wird der Bereich des Bildschirms außerhalb des Pfades nicht aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="beb87-115">If you use the path gradient brush to fill a shape that extends beyond the boundary of the path, the area of the screen outside the path will not be filled.</span></span> <span data-ttu-id="beb87-116">In der folgenden Abbildung wird gezeigt, was geschieht, wenn Sie den [**Grafik:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) -Aufrufe im vorangehenden Code in ändern `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .</span><span class="sxs-lookup"><span data-stu-id="beb87-116">The following illustration shows what happens if you change the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) call in the preceding code to `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)`.</span></span>

![Abbildung eines horizontalen Slice der vorherigen Ellipse](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a><span data-ttu-id="beb87-118">Angeben von Punkten an der Grenze</span><span class="sxs-lookup"><span data-stu-id="beb87-118">Specifying Points on the Boundary</span></span>

<span data-ttu-id="beb87-119">Im folgenden Beispiel wird ein Pfad Farbverlaufs Pinsel aus einem sternförmigen Pfad konstruiert.</span><span class="sxs-lookup"><span data-stu-id="beb87-119">The following example constructs a path gradient brush from a star-shaped path.</span></span> <span data-ttu-id="beb87-120">Der Code Ruft die [**PathGradientBrush:: setcentercolor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) -Methode auf, um die Farbe auf den Schwerpunkt des Sterns auf "rot" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="beb87-120">The code calls the [**PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) method to set the color at the centroid of the star to red.</span></span> <span data-ttu-id="beb87-121">Anschließend ruft der Code die [**PathGradientBrush:: setsurroundcolors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) -Methode auf, um verschiedene Farben (im [**Farb**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) Array gespeichert) an den einzelnen Punkten im [**Points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) -Array anzugeben.</span><span class="sxs-lookup"><span data-stu-id="beb87-121">Then the code calls the [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) method to specify various colors (stored in the [**colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) array) at the individual points in the [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) array.</span></span> <span data-ttu-id="beb87-122">Die abschließende Code Anweisung füllt den sternförmigen Pfad mit dem Pfad Farbverlaufs Pinsel.</span><span class="sxs-lookup"><span data-stu-id="beb87-122">The final code statement fills the star-shaped path with the path gradient brush.</span></span>


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



<span data-ttu-id="beb87-123">Die folgende Abbildung zeigt den gefüllten Stern.</span><span class="sxs-lookup"><span data-stu-id="beb87-123">The following illustration shows the filled star.</span></span>

![Abbildung mit einem fünf-Spitzen-Stern, der sich von rot in der Mitte in verschiedene Farben an jedem Punkt des Stern füllt](images/pathgradient3.png)

<span data-ttu-id="beb87-125">Im folgenden Beispiel wird ein Pfad Farbverlaufs Pinsel basierend auf einem Array von Punkten erstellt.</span><span class="sxs-lookup"><span data-stu-id="beb87-125">The following example constructs a path gradient brush based on an array of points.</span></span> <span data-ttu-id="beb87-126">Jedem der fünf Punkte im Array wird eine Farbe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="beb87-126">A color is assigned to each of the five points in the array.</span></span> <span data-ttu-id="beb87-127">Wenn Sie die fünf Punkte durch gerade Linien verbinden, erhalten Sie ein fünfseitiges Polygon.</span><span class="sxs-lookup"><span data-stu-id="beb87-127">If you were to connect the five points by straight lines, you would get a five-sided polygon.</span></span> <span data-ttu-id="beb87-128">Außerdem wird der Mitte (Schwerpunkt) dieses Polygons eine Farbe zugewiesen – in diesem Beispiel wird das Mittelpunkt (80, 75) auf weiß festgelegt.</span><span class="sxs-lookup"><span data-stu-id="beb87-128">A color is also assigned to the center (centroid) of that polygon — in this example, the center (80, 75) is set to white.</span></span> <span data-ttu-id="beb87-129">Die abschließende Code Anweisung im Beispiel füllt ein Rechteck mit dem Pfad Farbverlaufs Pinsel.</span><span class="sxs-lookup"><span data-stu-id="beb87-129">The final code statement in the example fills a rectangle with the path gradient brush.</span></span>

<span data-ttu-id="beb87-130">Die Farbe, die zum Ausfüllen des Rechtecks verwendet wird, ist weiß at (80, 75) und ändert sich allmählich, wenn Sie von (80, 75) zu den Punkten im Array wechseln.</span><span class="sxs-lookup"><span data-stu-id="beb87-130">The color used to fill the rectangle is white at (80, 75) and changes gradually as you move away from (80, 75) toward the points in the array.</span></span> <span data-ttu-id="beb87-131">Wenn Sie z. b. von (80, 75) zu (0,0) wechseln, ändert sich die Farbe allmählich von weiß in rot. während Sie von (80, 75) zu (160, 0) wechseln, ändert sich die Farbe allmählich von weiß zu grün.</span><span class="sxs-lookup"><span data-stu-id="beb87-131">For example, as you move from (80, 75) to (0, 0), the color changes gradually from white to red, and as you move from (80, 75) to (160, 0), the color changes gradually from white to green.</span></span>


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



<span data-ttu-id="beb87-132">Beachten Sie, dass im vorangehenden Code kein [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="beb87-132">Note that there is no [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object in the preceding code.</span></span> <span data-ttu-id="beb87-133">Der bestimmte [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) -Konstruktor im Beispiel empfängt einen Zeiger auf ein Array von Punkten, erfordert jedoch kein **GraphicsPath** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="beb87-133">The particular [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) constructor in the example receives a pointer to an array of points but does not require a **GraphicsPath** object.</span></span> <span data-ttu-id="beb87-134">Beachten Sie außerdem, dass der Pfad Farbverlaufs Pinsel zum Ausfüllen eines Rechtecks verwendet wird, nicht als Pfad.</span><span class="sxs-lookup"><span data-stu-id="beb87-134">Also, note that the path gradient brush is used to fill a rectangle, not a path.</span></span> <span data-ttu-id="beb87-135">Das Rechteck ist größer als der Pfad, der zum Definieren des Pinsels verwendet wird, sodass einige des Rechtecks nicht durch den Pinsel gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="beb87-135">The rectangle is larger than the path used to define the brush, so some of the rectangle is not painted by the brush.</span></span> <span data-ttu-id="beb87-136">Die folgende Abbildung zeigt das Rechteck (gepunktete Linie) und den Teil des Rechtecks, gezeichnet durch den Pinsel mit dem Pfad Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="beb87-136">The following illustration shows the rectangle (dotted line) and the portion of the rectangle painted by the path gradient brush.</span></span>

![Darstellung eines Rechtecks, das durch eine gepunktete Linie begrenzt ist, teilweise durch einen mehrfarbigen Farbverlauf gezeichnet](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a><span data-ttu-id="beb87-138">Anpassen eines Pfad Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="beb87-138">Customizing a Path Gradient</span></span>

<span data-ttu-id="beb87-139">Eine Möglichkeit, einen Pfad Farbverlaufs Pinsel anzupassen, besteht darin, die Skalierung des Fokus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="beb87-139">One way to customize a path gradient brush is to set its focus scales.</span></span> <span data-ttu-id="beb87-140">Die Fokus Skalen geben einen inneren Pfad an, der sich innerhalb des Haupt Pfads befindet.</span><span class="sxs-lookup"><span data-stu-id="beb87-140">The focus scales specify an inner path that lies inside the main path.</span></span> <span data-ttu-id="beb87-141">Die Mittel Farbe wird überall innerhalb dieses inneren Pfades anstelle des Mittelpunkts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="beb87-141">The center color is displayed everywhere inside that inner path rather than only at the center point.</span></span> <span data-ttu-id="beb87-142">Um die Fokus Skalen eines Path-Farbverlaufs Pinsels festzulegen, müssen Sie die [**PathGradientBrush:: setfocusscales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="beb87-142">To set the focus scales of a path gradient brush, call the [**PathGradientBrush::SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) method.</span></span>

<span data-ttu-id="beb87-143">Im folgenden Beispiel wird ein Pfad Farbverlaufs Pinsel auf der Grundlage eines elliptischen Pfads erstellt.</span><span class="sxs-lookup"><span data-stu-id="beb87-143">The following example creates a path gradient brush based on an elliptical path.</span></span> <span data-ttu-id="beb87-144">Der Code legt die Begrenzungs Farbe auf blau fest, legt die Mittel Farbe auf Aqua fest und verwendet dann den Pfad Farbverlaufs Pinsel, um den Ellipsen Pfad auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="beb87-144">The code sets the boundary color to blue, sets the center color to aqua, and then uses the path gradient brush to fill the elliptical path.</span></span>

<span data-ttu-id="beb87-145">Als nächstes legt der Code die Fokus Skalen des Pinsel mit dem Pfad Farbverlauf fest.</span><span class="sxs-lookup"><span data-stu-id="beb87-145">Next the code sets the focus scales of the path gradient brush.</span></span> <span data-ttu-id="beb87-146">Die x-Fokus Skala ist auf 0,3 festgelegt, und die y-Fokus Skala ist auf 0,8 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="beb87-146">The x focus scale is set to 0.3, and the y focus scale is set to 0.8.</span></span> <span data-ttu-id="beb87-147">Der Code Ruft die [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts auf, sodass der nachfolgende Aufruf von [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) eine Ellipse füllt, die sich rechts von der ersten Ellipse befindet.</span><span class="sxs-lookup"><span data-stu-id="beb87-147">The code calls the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills an ellipse that sits to the right of the first ellipse.</span></span>

<span data-ttu-id="beb87-148">Um die Auswirkung der Fokus Skalen anzuzeigen, stellen Sie sich eine kleine Ellipse vor, die das Zentrum mit der Haupt Ellipse teilt.</span><span class="sxs-lookup"><span data-stu-id="beb87-148">To see the effect of the focus scales, imagine a small ellipse that shares its center with the main ellipse.</span></span> <span data-ttu-id="beb87-149">Die kleine (innere) Ellipse ist die Hauptellipse, die horizontal um den Faktor 0,3 und vertikal um den Faktor 0,8 skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="beb87-149">The small (inner) ellipse is the main ellipse scaled (about its center) horizontally by a factor of 0.3 and vertically by a factor of 0.8.</span></span> <span data-ttu-id="beb87-150">Wenn Sie von der Grenze der äußeren Ellipse zur Grenze der inneren Ellipse wechseln, ändert sich die Farbe allmählich von blau zu Aqua.</span><span class="sxs-lookup"><span data-stu-id="beb87-150">As you move from the boundary of the outer ellipse to the boundary of the inner ellipse, the color changes gradually from blue to aqua.</span></span> <span data-ttu-id="beb87-151">Wenn Sie von der Begrenzung der inneren Ellipse zum Shared Center wechseln, bleibt die Farbe Aqua.</span><span class="sxs-lookup"><span data-stu-id="beb87-151">As you move from the boundary of the inner ellipse to the shared center, the color remains aqua.</span></span>


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



<span data-ttu-id="beb87-152">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="beb87-152">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="beb87-153">Die Ellipse auf der linken Seite ist nur für Aqua am Mittelpunkt.</span><span class="sxs-lookup"><span data-stu-id="beb87-153">The ellipse on the left is aqua only at the center point.</span></span> <span data-ttu-id="beb87-154">Die Ellipse auf der rechten Seite ist Aqua Everywhere innerhalb des inneren Pfades.</span><span class="sxs-lookup"><span data-stu-id="beb87-154">The ellipse on the right is aqua everywhere inside the inner path.</span></span>

![die Abbildung zeigt zwei Ellipsen, die von Aqua zu Blue schattiert werden: das erste hat nur sehr wenig Aqua. die zweite hat noch viel mehr](images/focusscales1.png)

<span data-ttu-id="beb87-156">Eine andere Möglichkeit zum Anpassen eines Farbverlaufs Pinsels besteht darin, ein Array von vordefinierten Farben und ein Array von Interpolations Positionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="beb87-156">Another way to customize a path gradient brush is to specify an array of preset colors and an array of interpolation positions.</span></span>

<span data-ttu-id="beb87-157">Im folgenden Beispiel wird ein auf einem Dreieck basierender Pfad Farbverlauf erstellt.</span><span class="sxs-lookup"><span data-stu-id="beb87-157">The following example creates a path gradient brush based on a triangle.</span></span> <span data-ttu-id="beb87-158">Der Code Ruft die Methode [**PathGradientBrush:: setinterpolationcolors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) des Pinsel mit dem Pfad Farbverlauf auf, um ein Array von Interpolations Farben (dunkelgrün, Aqua, Blue) und ein Array von Interpolations Positionen (0, 0,25, 1) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="beb87-158">The code calls the [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) method of the path gradient brush to specify an array of interpolation colors (dark green, aqua, blue) and an array of interpolation positions (0, 0.25, 1).</span></span> <span data-ttu-id="beb87-159">Wenn Sie von der Grenze des Dreiecks zum Mittelpunkt wechseln, ändert sich die Farbe allmählich von Dunkelgrün zu Aqua und dann von Aqua zu blau.</span><span class="sxs-lookup"><span data-stu-id="beb87-159">As you move from the boundary of the triangle to the center point, the color changes gradually from dark green to aqua and then from aqua to blue.</span></span> <span data-ttu-id="beb87-160">Die Änderung von Dunkelgrün zu Aqua erfolgt in 25 Prozent der Entfernung von Dunkelgrün zu blau.</span><span class="sxs-lookup"><span data-stu-id="beb87-160">The change from dark green to aqua happens in 25 percent of the distance from dark green to blue.</span></span>


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



<span data-ttu-id="beb87-161">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="beb87-161">The following illustration shows the output of the preceding code.</span></span>

![die Abbildung zeigt ein Dreieck, das sich von blau in der Mitte, auf Aqua, auf grün an den Rändern schattiert.](images/pathgradient4.png)

## <a name="setting-the-center-point"></a><span data-ttu-id="beb87-163">Festlegen des Mittelpunkts</span><span class="sxs-lookup"><span data-stu-id="beb87-163">Setting the Center Point</span></span>

<span data-ttu-id="beb87-164">Standardmäßig befindet sich der Mittelpunkt eines Pfad Farbverlaufs Pinsels im Schwerpunkt des Pfads, der zum Erstellen des Pinsels verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="beb87-164">By default, the center point of a path gradient brush is at the centroid of the path used to construct the brush.</span></span> <span data-ttu-id="beb87-165">Sie können den Speicherort des Mittelpunkts ändern, indem Sie die [**PathGradientBrush:: setcenterpoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) -Methode der [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) -Klasse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="beb87-165">You can change the location of the center point by calling the [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) method of the [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class.</span></span>

<span data-ttu-id="beb87-166">Im folgenden Beispiel wird ein auf einer Ellipse basierender Pfad Farbverlauf erstellt.</span><span class="sxs-lookup"><span data-stu-id="beb87-166">The following example creates a path gradient brush based on an ellipse.</span></span> <span data-ttu-id="beb87-167">Der Mittelpunkt der Ellipse liegt bei (70, 35), aber der Mittelpunkt des Farbverlaufs Pinsels ist auf (120, 40) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="beb87-167">The center of the ellipse is at (70, 35), but the center point of the path gradient brush is set to (120, 40).</span></span>


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



<span data-ttu-id="beb87-168">In der folgenden Abbildung werden die gefüllten Ellipse und der Mittelpunkt des Pfads für den Pfad Farbverlauf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="beb87-168">The following illustration shows the filled ellipse and the center point of the path gradient brush.</span></span>

![Abbildung: eine Ellipse, die von einem Mittelpunkt in der Nähe eines Endes von blau zu Aqua füllt](images/pathgradient5.png)

<span data-ttu-id="beb87-170">Sie können den Mittelpunkt eines Farbverlaufs Pinsels auf einen Speicherort außerhalb des Pfads festlegen, der zum Erstellen des Pinsels verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="beb87-170">You can set the center point of a path gradient brush to a location outside the path that was used to construct the brush.</span></span> <span data-ttu-id="beb87-171">Wenn Sie im vorangehenden Code den Aufrufen von [**PathGradientBrush:: setcenterpoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) durch ersetzen `pthGrBrush.SetCenterPoint(Point(145, 35))` , wird das folgende Ergebnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="beb87-171">In the preceding code, if you replace the call to [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) with `pthGrBrush.SetCenterPoint(Point(145, 35))`, you will get the following result.</span></span>

![Abbildung, die eine Ellipse anzeigt, die von einem Mittelpunkt, der sich außerhalb des Rands der Ellipse befindet, von rot zu gelb ausfüllt](images/pathgradient6.png)

<span data-ttu-id="beb87-173">In der obigen Abbildung sind die Punkte ganz rechts von der Ellipse nicht rein blau (obwohl Sie sehr nah sind).</span><span class="sxs-lookup"><span data-stu-id="beb87-173">In the preceding illustration, the points at the far right of the ellipse are not pure blue (although they are very close).</span></span> <span data-ttu-id="beb87-174">Die Farben im Farbverlauf werden so positioniert, als ob die Füllung den Punkt erreichen würde (145, 35), die Farbe hätte rein blau (0, 0, 255) erreicht.</span><span class="sxs-lookup"><span data-stu-id="beb87-174">The colors in the gradient are positioned as if the fill had been allowed to reach the point (145, 35), the color would have reached pure blue (0, 0, 255).</span></span> <span data-ttu-id="beb87-175">Die Füllung erreicht jedoch nie (145, 35), da ein Pfad Farbverlaufs Pinsel nur innerhalb des Pfads zeichnet.</span><span class="sxs-lookup"><span data-stu-id="beb87-175">But the fill never reaches (145, 35) because a path gradient brush paints only inside its path.</span></span>

 

 
