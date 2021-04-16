---
description: 'In Windows GDI+ werden drei Koordinaten Bereiche verwendet: "World", "page" und "Device".'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Typen von Koordinatensystemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05908196662918eb93f4fa6e2b356a6989ed5a58
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104558304"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="91eed-103">Typen von Koordinatensystemen</span><span class="sxs-lookup"><span data-stu-id="91eed-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="91eed-104">In Windows GDI+ werden drei Koordinaten Bereiche verwendet: "World", "page" und "Device".</span><span class="sxs-lookup"><span data-stu-id="91eed-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="91eed-105">Wenn Sie den-Befehl ausführen `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , befinden sich die Punkte, die Sie an die [**Grafik übergeben::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) -Methode – (0,0) und (160, 80) – im weltweiten Koordinaten Bereich.</span><span class="sxs-lookup"><span data-stu-id="91eed-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="91eed-106">Bevor GDI+ die Linie auf dem Bildschirm zeichnen kann, durchlaufen die Koordinaten eine Sequenz von Transformationen.</span><span class="sxs-lookup"><span data-stu-id="91eed-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="91eed-107">Eine Transformation konvertiert globale Koordinaten in Seiten Koordinaten, und eine andere Transformation wandelt Seiten Koordinaten in Geräte Koordinaten um.</span><span class="sxs-lookup"><span data-stu-id="91eed-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="91eed-108">Angenommen, Sie möchten mit einem Koordinatensystem arbeiten, dessen Ursprung im Text des Client Bereichs liegt, und nicht in der oberen linken Ecke.</span><span class="sxs-lookup"><span data-stu-id="91eed-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="91eed-109">Angenommen, Sie möchten, dass der Ursprung 100 Pixel vom linken Rand des Client Bereichs und 50 Pixel vom oberen Rand des Client Bereichs sein soll.</span><span class="sxs-lookup"><span data-stu-id="91eed-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="91eed-110">Die folgende Abbildung zeigt ein solches Koordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="91eed-110">The following illustration shows such a coordinate system.</span></span>

![Screenshot eines Fensters mit der Bezeichnung "Koordinatenachsen"](images/aboutgdip05-art01.png)

<span data-ttu-id="91eed-112">Wenn Sie den-Befehl ausführen `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , erhalten Sie die in der folgenden Abbildung gezeigte Zeile.</span><span class="sxs-lookup"><span data-stu-id="91eed-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![Screenshot des vorherigen Fensters, aber mit einer blauen Linie, die diagonal vom Ursprung aus erweitert wird](images/aboutgdip05-art02.png)

<span data-ttu-id="91eed-114">Die Koordinaten der Endpunkte der Zeile in den drei Koordinaten Räumen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91eed-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="91eed-115">World</span><span class="sxs-lookup"><span data-stu-id="91eed-115">World</span></span>  | <span data-ttu-id="91eed-116">(0,0) bis (160, 80)</span><span class="sxs-lookup"><span data-stu-id="91eed-116">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="91eed-117">Seite</span><span class="sxs-lookup"><span data-stu-id="91eed-117">Page</span></span>   | <span data-ttu-id="91eed-118">(100, 50) bis (260, 130)</span><span class="sxs-lookup"><span data-stu-id="91eed-118">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="91eed-119">Sicherungsmedium</span><span class="sxs-lookup"><span data-stu-id="91eed-119">Device</span></span> | <span data-ttu-id="91eed-120">(100, 50) bis (260, 130)</span><span class="sxs-lookup"><span data-stu-id="91eed-120">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="91eed-121">Beachten Sie, dass der Seiten Koordinaten Bereich seinen Ursprung in der oberen linken Ecke des Client Bereichs hat. Dies ist immer der Fall.</span><span class="sxs-lookup"><span data-stu-id="91eed-121">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="91eed-122">Beachten Sie außerdem, dass die Geräte Koordinaten den Seiten Koordinaten entsprechen, da die Maßeinheit das Pixel ist.</span><span class="sxs-lookup"><span data-stu-id="91eed-122">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="91eed-123">Wenn Sie die Maßeinheit auf einen anderen Wert als Pixel festlegen (z. b. Zoll), unterscheiden sich die Geräte Koordinaten von den Seiten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="91eed-123">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="91eed-124">Die Transformation zum Zuordnen von Weltkoordinaten zu Seiten Koordinaten wird als globale *Transformation* bezeichnet und wird von einem [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verwaltet.</span><span class="sxs-lookup"><span data-stu-id="91eed-124">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="91eed-125">Im vorherigen Beispiel handelt es sich bei der Welt Transformation um eine Translation 100-Einheiten in der x-Richtung und 50-Einheiten in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="91eed-125">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="91eed-126">Im folgenden Beispiel wird die globale Transformation eines **Grafik** Objekts festgelegt, und anschließend wird das **Grafik** Objekt verwendet, um die in der vorherigen Abbildung gezeigte Zeile zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="91eed-126">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="91eed-127">Die Transformation, die den Geräte Koordinaten Seiten Koordinaten zuordnet, wird als *Seiten Transformation* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="91eed-127">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="91eed-128">Die [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse bietet vier Methoden zum Bearbeiten und Überprüfen der Seiten Transformation: [**Graphics:: setpageunit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics:: getpageunit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: setpagescale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)und [**Graphics:: getPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="91eed-128">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="91eed-129">Die **Grafik** Klasse bietet auch zwei Methoden, [**Graphics:: getdpix**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) und [**Graphics:: getdpiy**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), um die horizontalen und vertikalen Punkte pro Zoll des Anzeige Geräts zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="91eed-129">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="91eed-130">Sie können die [**Graphics:: setpageunit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse verwenden, um eine Maßeinheit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="91eed-130">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="91eed-131">Im folgenden Beispiel wird eine Zeile von (0,0) zu (2, 1) gezeichnet, wobei Punkt (2, 1) 2 Zoll nach rechts und 1 Zoll vom Punkt (0,0) ist.</span><span class="sxs-lookup"><span data-stu-id="91eed-131">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="91eed-132">Wenn Sie beim Erstellen des Stifts keine Stift Breite angeben, wird im vorherigen Beispiel eine Linie mit einer Breite von einem Zoll gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="91eed-132">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="91eed-133">Sie können die Stift Breite im zweiten Argument für den [**Stift**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Konstruktor angeben:</span><span class="sxs-lookup"><span data-stu-id="91eed-133">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="91eed-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="91eed-134">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="91eed-135">Wenn wir davon ausgehen, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung aufweist, haben die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinaten Räumen:</span><span class="sxs-lookup"><span data-stu-id="91eed-135">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                     |
|--------|---------------------|
| <span data-ttu-id="91eed-136">World</span><span class="sxs-lookup"><span data-stu-id="91eed-136">World</span></span>  | <span data-ttu-id="91eed-137">(0,0) bis (2, 1)</span><span class="sxs-lookup"><span data-stu-id="91eed-137">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="91eed-138">Seite</span><span class="sxs-lookup"><span data-stu-id="91eed-138">Page</span></span>   | <span data-ttu-id="91eed-139">(0,0) bis (2, 1)</span><span class="sxs-lookup"><span data-stu-id="91eed-139">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="91eed-140">Sicherungsmedium</span><span class="sxs-lookup"><span data-stu-id="91eed-140">Device</span></span> | <span data-ttu-id="91eed-141">(0,0, bis (192, 96)</span><span class="sxs-lookup"><span data-stu-id="91eed-141">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="91eed-142">Sie können die Transformationen für Welt und Seite kombinieren, um eine Vielzahl von Effekten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="91eed-142">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="91eed-143">Angenommen, Sie möchten Zoll als Maßeinheit verwenden, und Sie möchten, dass der Ursprung ihres Koordinatensystems 2 Zoll vom linken Rand des Client Bereichs und 1/2 Zoll vom oberen Rand des Client Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="91eed-143">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="91eed-144">Im folgenden Beispiel werden die Welt-und Seiten Transformationen eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts festgelegt, und anschließend wird eine Linie von (0,0) zu (2, 1) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="91eed-144">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="91eed-145">In der folgenden Abbildung ist die Linie und das Koordinatensystem dargestellt.</span><span class="sxs-lookup"><span data-stu-id="91eed-145">The following illustration shows the line and coordinate system.</span></span>

![Screenshot des vorherigen Fensters, aber breiter, wobei die Achsen auf der linken Seite positioniert sind und anders gekennzeichnet sind](images/aboutgdip05-art03.png)

<span data-ttu-id="91eed-147">Wenn wir davon ausgehen, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung aufweist, haben die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinaten Räumen:</span><span class="sxs-lookup"><span data-stu-id="91eed-147">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



|        |                         |
|--------|-------------------------|
| <span data-ttu-id="91eed-148">World</span><span class="sxs-lookup"><span data-stu-id="91eed-148">World</span></span>  | <span data-ttu-id="91eed-149">(0,0) bis (2, 1)</span><span class="sxs-lookup"><span data-stu-id="91eed-149">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="91eed-150">Seite</span><span class="sxs-lookup"><span data-stu-id="91eed-150">Page</span></span>   | <span data-ttu-id="91eed-151">(2, 0,5) bis (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="91eed-151">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="91eed-152">Sicherungsmedium</span><span class="sxs-lookup"><span data-stu-id="91eed-152">Device</span></span> | <span data-ttu-id="91eed-153">(192, 48) bis (384, 144)</span><span class="sxs-lookup"><span data-stu-id="91eed-153">(192, 48) to (384, 144)</span></span> |



 

 

 
