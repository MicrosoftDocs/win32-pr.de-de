---
description: 'Windows GDI+ verwendet drei Koordinatenräume: Welt, Seite und Gerät.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Typen von Koordinatensystemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120625"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="b2fb0-103">Typen von Koordinatensystemen</span><span class="sxs-lookup"><span data-stu-id="b2fb0-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="b2fb0-104">Windows GDI+ verwendet drei Koordinatenräume: Welt, Seite und Gerät.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="b2fb0-105">Wenn Sie den Aufruf vornehmen, befinden sich `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` die Punkte, die Sie an die [**Graphics::D rawLine-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) übergeben – (0, 0) und (160, 80) – im Koordinatenraum der Welt.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="b2fb0-106">Bevor GDI+ die Linie auf dem Bildschirm zeichnen kann, durchlaufen die Koordinaten eine Sequenz von Transformationen.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="b2fb0-107">Eine Transformation konvertiert Weltkoordinaten in Seitenkoordinaten, und eine andere Transformation konvertiert Seitenkoordinaten in Gerätekoordinaten.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="b2fb0-108">Angenommen, Sie möchten mit einem Koordinatensystem arbeiten, das seinen Ursprung im Textkörper des Clientbereichs anstelle der oberen linken Ecke hat.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="b2fb0-109">Angenommen, Sie möchten, dass der Ursprung 100 Pixel vom linken Rand des Clientbereichs und 50 Pixel vom oberen Rand des Clientbereichs entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="b2fb0-110">Die folgende Abbildung zeigt ein solches Koordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-110">The following illustration shows such a coordinate system.</span></span>

![Screenshot eines Fensters mit bezeichneten Koordinatenachsen](images/aboutgdip05-art01.png)

<span data-ttu-id="b2fb0-112">Wenn Sie den Aufruf `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` ausführen, erhalten Sie die in der folgenden Abbildung dargestellte Zeile.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![Screenshot des vorherigen Fensters, jedoch mit einer blauen Linie, die sich diagonal vom Ursprung erstreckt](images/aboutgdip05-art02.png)

<span data-ttu-id="b2fb0-114">Die Koordinaten der Endpunkte Ihrer Linie in den drei Koordinatenbereichen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2fb0-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



| <span data-ttu-id="b2fb0-115">LeerZchn</span><span class="sxs-lookup"><span data-stu-id="b2fb0-115">Space</span></span>       |  <span data-ttu-id="b2fb0-116">Endpunktkoordinaten</span><span class="sxs-lookup"><span data-stu-id="b2fb0-116">Endpoint coordinates</span></span>                       |
|--------|-------------------------|
| <span data-ttu-id="b2fb0-117">World</span><span class="sxs-lookup"><span data-stu-id="b2fb0-117">World</span></span>  | <span data-ttu-id="b2fb0-118">(0, 0) bis (160, 80)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-118">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="b2fb0-119">Seite</span><span class="sxs-lookup"><span data-stu-id="b2fb0-119">Page</span></span>   | <span data-ttu-id="b2fb0-120">(100, 50) bis (260, 130)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-120">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="b2fb0-121">Gerät</span><span class="sxs-lookup"><span data-stu-id="b2fb0-121">Device</span></span> | <span data-ttu-id="b2fb0-122">(100, 50) bis (260, 130)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-122">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="b2fb0-123">Beachten Sie, dass der Seitenkoordinatenraum seinen Ursprung in der oberen linken Ecke des Clientbereichs hat. Dies ist immer der Fall.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-123">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="b2fb0-124">Beachten Sie außerdem, dass die Gerätekoordinaten mit den Seitenkoordinaten identisch sind, da die Maßeinheit das Pixel ist.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-124">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="b2fb0-125">Wenn Sie die Maßeinheit auf einen anderen Als Pixel (z. B. Zoll) festlegen, unterscheiden sich die Gerätekoordinaten von den Seitenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-125">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="b2fb0-126">Die Transformation, die Weltkoordinaten Seitenkoordinaten zuordnt, wird als *Welttransformation* bezeichnet und von einem [**Graphics-Objekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-126">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="b2fb0-127">Im vorherigen Beispiel ist die Welttransformation eine Übersetzung von 100 Einheiten in x-Richtung und 50 Einheiten in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-127">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="b2fb0-128">Im folgenden Beispiel wird die Welttransformation eines **Graphics-Objekts** festgelegt und dann dieses **Graphics-Objekt** verwendet, um die in der vorherigen Abbildung gezeigte Linie zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-128">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="b2fb0-129">Die Transformation, die Seitenkoordinaten Gerätekoordinaten zuordnt, wird als *Seitentransformation* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-129">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="b2fb0-130">Die [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) stellt vier Methoden zum Bearbeiten und Untersuchen der Seitentransformation bereit: [**Graphics::SetPageUnit,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) [**Graphics::GetPageUnit,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit) [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)und [**Graphics::GetPageScale.**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-130">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="b2fb0-131">Die **Graphics-Klasse** stellt auch zwei Methoden bereit: [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) und [**Graphics::GetDpiY,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy)um die horizontalen und vertikalen Punkte pro Zoll des Anzeigegeräts zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-131">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="b2fb0-132">Sie können die [**Graphics::SetPageUnit-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwenden, um eine Maßeinheit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-132">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="b2fb0-133">Das folgende Beispiel zeichnet eine Linie von (0, 0) bis (2, 1), wobei der Punkt (2, 1) 2 Zoll nach rechts und 1 Zoll vom Punkt (0, 0) nach unten liegt.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-133">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="b2fb0-134">Wenn Sie beim Erstellen des Stifts keine Stiftbreite angeben, wird im vorherigen Beispiel eine Linie gezeichnet, die einen Zoll breit ist.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-134">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="b2fb0-135">Sie können die Stiftbreite im zweiten Argument für den [**Stiftkonstruktor**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) angeben:</span><span class="sxs-lookup"><span data-stu-id="b2fb0-135">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="b2fb0-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="b2fb0-137">Wenn angenommen wird, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung hat, weisen die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinatenbereichen auf:</span><span class="sxs-lookup"><span data-stu-id="b2fb0-137">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="b2fb0-138">LeerZchn</span><span class="sxs-lookup"><span data-stu-id="b2fb0-138">Space</span></span>       | <span data-ttu-id="b2fb0-139">Endpunktkoordinaten</span><span class="sxs-lookup"><span data-stu-id="b2fb0-139">Endpoint coordinates</span></span>                    |
|--------|---------------------|
| <span data-ttu-id="b2fb0-140">World</span><span class="sxs-lookup"><span data-stu-id="b2fb0-140">World</span></span>  | <span data-ttu-id="b2fb0-141">(0, 0) bis (2, 1)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-141">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="b2fb0-142">Seite</span><span class="sxs-lookup"><span data-stu-id="b2fb0-142">Page</span></span>   | <span data-ttu-id="b2fb0-143">(0, 0) bis (2, 1)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-143">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="b2fb0-144">Gerät</span><span class="sxs-lookup"><span data-stu-id="b2fb0-144">Device</span></span> | <span data-ttu-id="b2fb0-145">(0, 0, bis (192, 96)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-145">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="b2fb0-146">Sie können die Welt- und Seitentransformationen kombinieren, um eine Vielzahl von Effekten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-146">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="b2fb0-147">Angenommen, Sie möchten Zoll als Maßeinheit verwenden und möchten, dass der Ursprung Ihres Koordinatensystems 2 Zoll vom linken Rand des Clientbereichs und 1/2 Zoll vom oberen Rand des Clientbereichs entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-147">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="b2fb0-148">Im folgenden Beispiel werden die Welt- und Seitentransformationen eines [**Graphics-Objekts**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) festgelegt und dann eine Linie von (0, 0) bis (2, 1) zeichnet.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-148">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="b2fb0-149">Die folgende Abbildung zeigt die Linie und das Koordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="b2fb0-149">The following illustration shows the line and coordinate system.</span></span>

![Screenshot des vorherigen Fensters, aber breiter, wobei die Achsen links positioniert und anders bezeichnet sind](images/aboutgdip05-art03.png)

<span data-ttu-id="b2fb0-151">Wenn angenommen wird, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung hat, weisen die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinatenbereichen auf:</span><span class="sxs-lookup"><span data-stu-id="b2fb0-151">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="b2fb0-152">LeerZchn</span><span class="sxs-lookup"><span data-stu-id="b2fb0-152">Space</span></span>       | <span data-ttu-id="b2fb0-153">Endpunktkoordinaten</span><span class="sxs-lookup"><span data-stu-id="b2fb0-153">Endpoint coordinates</span></span>                        |
|--------|-------------------------|
| <span data-ttu-id="b2fb0-154">World</span><span class="sxs-lookup"><span data-stu-id="b2fb0-154">World</span></span>  | <span data-ttu-id="b2fb0-155">(0, 0) bis (2, 1)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-155">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="b2fb0-156">Seite</span><span class="sxs-lookup"><span data-stu-id="b2fb0-156">Page</span></span>   | <span data-ttu-id="b2fb0-157">(2, 0,5) bis (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-157">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="b2fb0-158">Gerät</span><span class="sxs-lookup"><span data-stu-id="b2fb0-158">Device</span></span> | <span data-ttu-id="b2fb0-159">(192, 48) bis (384, 144)</span><span class="sxs-lookup"><span data-stu-id="b2fb0-159">(192, 48) to (384, 144)</span></span> |



 

 

 
