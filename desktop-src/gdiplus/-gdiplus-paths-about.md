---
description: Pfade werden gebildet, indem Linien, Rechtecke und einfache Kurven kombiniert werden. Erinnern Sie sich aus der Übersicht über Vektorgrafiken, dass die folgenden grundlegenden Bausteine sich als besonders nützlich für das Zeichnen von Bildern erwiesen haben.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Pfade (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554529"
---
# <a name="paths-gdi"></a><span data-ttu-id="2e72e-104">Pfade (GDI+)</span><span class="sxs-lookup"><span data-stu-id="2e72e-104">Paths (GDI+)</span></span>

<span data-ttu-id="2e72e-105">Pfade werden gebildet, indem Linien, Rechtecke und einfache Kurven kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="2e72e-105">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="2e72e-106">Erinnern Sie sich aus der [Übersicht über Vektorgrafiken](-gdiplus-overview-of-vector-graphics-about.md) , dass die folgenden grundlegenden Bausteine sich als besonders nützlich für das Zeichnen von Bildern erwiesen haben.</span><span class="sxs-lookup"><span data-stu-id="2e72e-106">Recall from the [Overview of Vector Graphics](-gdiplus-overview-of-vector-graphics-about.md) that the following basic building blocks have proven to be the most useful for drawing pictures.</span></span>

-   <span data-ttu-id="2e72e-107">Linien</span><span class="sxs-lookup"><span data-stu-id="2e72e-107">Lines</span></span>
-   <span data-ttu-id="2e72e-108">Rechtecke</span><span class="sxs-lookup"><span data-stu-id="2e72e-108">Rectangles</span></span>
-   <span data-ttu-id="2e72e-109">Ellipsen</span><span class="sxs-lookup"><span data-stu-id="2e72e-109">Ellipses</span></span>
-   <span data-ttu-id="2e72e-110">Bögen</span><span class="sxs-lookup"><span data-stu-id="2e72e-110">Arcs</span></span>
-   <span data-ttu-id="2e72e-111">Polygone</span><span class="sxs-lookup"><span data-stu-id="2e72e-111">Polygons</span></span>
-   <span data-ttu-id="2e72e-112">Kardinale Splines</span><span class="sxs-lookup"><span data-stu-id="2e72e-112">Cardinal splines</span></span>
-   <span data-ttu-id="2e72e-113">Bézier-Splines</span><span class="sxs-lookup"><span data-stu-id="2e72e-113">Bézier splines</span></span>

<span data-ttu-id="2e72e-114">In Windows GDI+ ermöglicht das [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt, eine Sequenz dieser Bausteine in einer einzelnen Einheit zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="2e72e-114">In Windows GDI+, the [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="2e72e-115">Die gesamte Sequenz von Linien, Rechtecke, Polygonen und Kurven kann dann mit einem aufzurufenden [**:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="2e72e-115">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="2e72e-116">Die folgende Abbildung zeigt einen Pfad, der durch das Kombinieren einer Linie, eines Bogens, eines Bézier-Spline und eines kardinaler Spline erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e72e-116">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>

![Abbildung eines Pfads, der eine Linie, einen Bogen, eine Bézier-Spline und einen kardinalspline kombiniert](images/aboutgdip02-art14.png)

<span data-ttu-id="2e72e-118">Die [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Klasse stellt die folgenden Methoden zum Erstellen einer Sequenz von Elementen bereit, die gezeichnet werden sollen: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [addrechteck](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [addelta lipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (für Kardinal-Splines) und [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="2e72e-118">The [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) class provides the following methods for creating a sequence of items to be drawn: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (for cardinal splines), and [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span></span> <span data-ttu-id="2e72e-119">Jede dieser Methoden ist überladen. Das heißt, jede Methode kommt in verschiedene Variationen mit unterschiedlichen Parameterlisten.</span><span class="sxs-lookup"><span data-stu-id="2e72e-119">Each of these methods is overloaded; that is, each method comes in several variations with different parameter lists.</span></span> <span data-ttu-id="2e72e-120">Beispielsweise empfängt eine Variation der AddLine-Methode vier ganze Zahlen, und eine andere Variation der AddLine-Methode empfängt zwei [**Punkt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) Objekte.</span><span class="sxs-lookup"><span data-stu-id="2e72e-120">For example, one variation of the AddLine method receives four integers, and another variation of the AddLine method receives two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span>

<span data-ttu-id="2e72e-121">Die Methoden zum Hinzufügen von Linien, Rechtecke und Bézier-Splines zu einem Pfad verfügen über Plural-Begleit Methoden, mit denen dem Pfad in einem einzelnen-Befehl mehrere Elemente hinzugefügt werden: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [addrechgles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))und [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span><span class="sxs-lookup"><span data-stu-id="2e72e-121">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint)), and [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span></span> <span data-ttu-id="2e72e-122">Außerdem verfügt die [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) -Methode über eine Begleit Methode, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), die dem Pfad eine geschlossene Kurve hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2e72e-122">Also, the [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) method has a companion method, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), that adds a closed curve to the path.</span></span>

<span data-ttu-id="2e72e-123">Zum Zeichnen eines Pfads benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt und ein [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e72e-123">To draw a path, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="2e72e-124">Das **Grafik** Objekt stellt die [**Grafik::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode bereit, und das **Stift** -Objekt speichert Attribute des Pfads, z. b. Linienstärke und Farbe.</span><span class="sxs-lookup"><span data-stu-id="2e72e-124">The **Graphics** object provides the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method, and the **Pen** object stores attributes of the path, such as line width and color.</span></span> <span data-ttu-id="2e72e-125">Das **GraphicsPath** -Objekt speichert die Sequenz von Linien, Rechtecke und Kurven, die den Pfad bilden.</span><span class="sxs-lookup"><span data-stu-id="2e72e-125">The **GraphicsPath** object stores the sequence of lines, rectangles, and curves that make up the path.</span></span> <span data-ttu-id="2e72e-126">Die Adressen des **Stift** Objekts und des **GraphicsPath** -Objekts werden als Argumente an die **Grafik::D rawpath** -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="2e72e-126">The addresses of the **Pen** object and the **GraphicsPath** object are passed as arguments to the **Graphics::DrawPath** method.</span></span> <span data-ttu-id="2e72e-127">Im folgenden Beispiel wird ein Pfad gezeichnet, der aus einer Zeile, einer Ellipse und einem Bézier-Spline besteht.</span><span class="sxs-lookup"><span data-stu-id="2e72e-127">The following example draws a path that consists of a line, an ellipse, and a Bézier spline.</span></span>


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="2e72e-128">In der folgenden Abbildung ist der Pfad dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2e72e-128">The following illustration shows the path.</span></span>

![Abbildung eines Pfads, der aus einer Zeile, einer Ellipse und einer Bézier-Spline besteht](images/aboutgdip02-art15.png)

<span data-ttu-id="2e72e-130">Zusätzlich zum Hinzufügen von Linien, Rechtecke und Kurven zu einem Pfad können Sie Pfade zu einem Pfad hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2e72e-130">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="2e72e-131">Dies ermöglicht Ihnen das Kombinieren vorhandener Pfade, um große und komplexe Pfade zu bilden.</span><span class="sxs-lookup"><span data-stu-id="2e72e-131">This allows you to combine existing paths to form large, complex paths.</span></span> <span data-ttu-id="2e72e-132">Der folgende Code fügt " **graphicsPath1** " und " **graphicsPath2** " zu **myGraphicsPath** hinzu.</span><span class="sxs-lookup"><span data-stu-id="2e72e-132">The following code adds **graphicsPath1** and **graphicsPath2** to **myGraphicsPath**.</span></span> <span data-ttu-id="2e72e-133">Der zweite Parameter der [**GraphicsPath:: Addpath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) -Methode gibt an, ob der hinzugefügte Pfad mit dem vorhandenen Pfad verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="2e72e-133">The second parameter of the [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) method specifies whether the added path is connected to the existing path.</span></span>


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



<span data-ttu-id="2e72e-134">Es gibt zwei weitere Elemente, die Sie einem Pfad hinzufügen können: Strings und Pies.</span><span class="sxs-lookup"><span data-stu-id="2e72e-134">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="2e72e-135">Ein Kreis ist ein Teil des Inneren einer Ellipse.</span><span class="sxs-lookup"><span data-stu-id="2e72e-135">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="2e72e-136">Im folgenden Beispiel wird ein Pfad von einem Bogen, ein kardinaler Spline, eine Zeichenfolge und ein Kreis erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e72e-136">The following example creates a path from an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="2e72e-137">In der folgenden Abbildung ist der Pfad dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2e72e-137">The following illustration shows the path.</span></span> <span data-ttu-id="2e72e-138">Beachten Sie, dass für einen Pfad keine Verbindung hergestellt werden muss. der Bogen, der kardinalspline, die Zeichenfolge und der Kreis werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="2e72e-138">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>

![Abbildung eines Pfads, der aus getrennten Zeilen besteht: einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis](images/aboutgdip02-art16.png)

 

 



