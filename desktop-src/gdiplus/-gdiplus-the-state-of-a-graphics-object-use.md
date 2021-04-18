---
description: Die Grafikklasse ist das Herzstück von Windows GDI+. Um etwas zu zeichnen, erstellen Sie ein Grafik Objekt, legen seine Eigenschaften fest und rufen seine Methoden auf (DrawLine, DrawImage, DrawString und like).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Status eines Grafikobjekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555247"
---
# <a name="the-state-of-a-graphics-object"></a><span data-ttu-id="add82-104">Status eines Grafikobjekts</span><span class="sxs-lookup"><span data-stu-id="add82-104">The State of a Graphics Object</span></span>

<span data-ttu-id="add82-105">Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse ist das Herzstück von Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="add82-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is at the heart of Windows GDI+.</span></span> <span data-ttu-id="add82-106">Um etwas zu zeichnen, erstellen Sie ein **Grafik** Objekt, legen seine Eigenschaften fest und rufen seine Methoden auf ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))und like).</span><span class="sxs-lookup"><span data-stu-id="add82-106">To draw anything, you create a **Graphics** object, set its properties, and call its methods ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)), and the like).</span></span>

<span data-ttu-id="add82-107">Im folgenden Beispiel werden ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellt und dann die [**Grafik::D rawrechteck**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Methode des **Grafik** Objekts aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="add82-107">The following example constructs a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and then calls the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object:</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



<span data-ttu-id="add82-108">Im vorangehenden Code gibt die [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) -Methode ein Handle für einen Gerätekontext zurück, und dieses Handle wird an den [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) -Konstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="add82-108">In the preceding code, the [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) method returns a handle to a device context, and that handle is passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="add82-109">Ein Gerätekontext ist eine (von Windows betreute) Struktur, die Informationen über das jeweilige angeverwendete Anzeigegerät enthält.</span><span class="sxs-lookup"><span data-stu-id="add82-109">A device context is a structure (maintained by Windows) that holds information about the particular display device being used.</span></span>

## <a name="graphics-state"></a><span data-ttu-id="add82-110">Grafikzustand</span><span class="sxs-lookup"><span data-stu-id="add82-110">Graphics State</span></span>

<span data-ttu-id="add82-111">Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt bietet mehr als Zeichnungs Methoden, z. b. [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) und [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="add82-111">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object does more than provide drawing methods, such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span></span> <span data-ttu-id="add82-112">Ein **Grafik** Objekt verwaltet auch den Grafik Zustand, der in die folgenden Kategorien unterteilt werden kann:</span><span class="sxs-lookup"><span data-stu-id="add82-112">A **Graphics** object also maintains graphics state, which can be divided into the following categories:</span></span>

-   <span data-ttu-id="add82-113">Ein Link zu einem Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="add82-113">A link to a device context</span></span>
-   <span data-ttu-id="add82-114">Qualitätseinstellungen</span><span class="sxs-lookup"><span data-stu-id="add82-114">Quality settings</span></span>
-   <span data-ttu-id="add82-115">Transformationen</span><span class="sxs-lookup"><span data-stu-id="add82-115">Transformations</span></span>
-   <span data-ttu-id="add82-116">Ein Clippingbereich</span><span class="sxs-lookup"><span data-stu-id="add82-116">A clipping region</span></span>

### <a name="device-context"></a><span data-ttu-id="add82-117">Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="add82-117">Device Context</span></span>

<span data-ttu-id="add82-118">Als Anwendungsprogrammierer müssen Sie sich keine Gedanken über die Interaktion zwischen einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und seinem Gerätekontext machen.</span><span class="sxs-lookup"><span data-stu-id="add82-118">As an application programmer, you don't have to think about the interaction between a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and its device context.</span></span> <span data-ttu-id="add82-119">Diese Interaktion wird von GDI+ im Hintergrund behandelt.</span><span class="sxs-lookup"><span data-stu-id="add82-119">This interaction is handled by GDI+ behind the scenes.</span></span>

### <a name="quality-settings"></a><span data-ttu-id="add82-120">Qualitätseinstellungen</span><span class="sxs-lookup"><span data-stu-id="add82-120">Quality Settings</span></span>

<span data-ttu-id="add82-121">Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verfügt über mehrere Eigenschaften, die die Qualität der Elemente beeinflussen, die auf dem Bildschirm gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="add82-121">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object has several properties that influence the quality of the items that are drawn on the screen.</span></span> <span data-ttu-id="add82-122">Sie können diese Eigenschaften anzeigen und bearbeiten, indem Sie Get-und Set-Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="add82-122">You can view and manipulate these properties by calling get and set methods.</span></span> <span data-ttu-id="add82-123">Beispielsweise können Sie die [**Graphics:: settextrenderinghint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) -Methode aufrufen, um den Typ des Antialiasing (sofern vorhanden) anzugeben, der auf Text angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="add82-123">For example, you can call the [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="add82-124">Andere Set-Methoden, die die Qualität beeinflussen, sind [**Grafiken:: sezmuothingmode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: setcompositingmode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: setcompositingquality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)und [**Graphics:: setinterpolationmode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span><span class="sxs-lookup"><span data-stu-id="add82-124">Other set methods that influence quality are [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality), and [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span></span>

<span data-ttu-id="add82-125">Im folgenden Beispiel werden zwei Ellipsen gezeichnet, wobei der Glättungs Modus auf [\* \* \* \* SmoothingModeAntiAlias \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) und einen mit dem Glättungs Modus \* \* \* [\* smoothingmodehighspeed \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="add82-125">The following example draws two ellipses, one with the smoothing mode set to [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) and one with the smoothing mode set to [\*\*\*\*SmoothingModeHighSpeed\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a><span data-ttu-id="add82-126">Transformationen</span><span class="sxs-lookup"><span data-stu-id="add82-126">Transformations</span></span>

<span data-ttu-id="add82-127">Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verwaltet zwei Transformationen (Welt und Seite), die auf alle Elemente angewendet werden, die von diesem **Grafik** Objekt gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="add82-127">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains two transformations (world and page) that are applied to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="add82-128">Jede affine Transformation kann in der Welt Transformation gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="add82-128">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="add82-129">Affine Transformationen umfassen Skalierung, Rotation, Spiegelung, Neigung und Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="add82-129">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="add82-130">Die Seiten Transformation kann für die Skalierung und für das Ändern von Einheiten (z. b. Pixel in Zoll) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="add82-130">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="add82-131">Weitere Informationen zu Transformationen finden Sie unter [Koordinatensysteme und Transformationen](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="add82-131">For more information on transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="add82-132">Im folgenden Beispiel werden die Welt-und Seiten Transformationen eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="add82-132">The following example sets the world and page transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="add82-133">Die Welt Transformation ist auf eine 30-Grad-Drehung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="add82-133">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="add82-134">Die Seiten Transformation wird so festgelegt, dass die an die zweite Grafik über gebenden Koordinaten [**:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) als Millimeter anstelle von Pixel behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="add82-134">The page transformation is set so that the coordinates passed to the second [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="add82-135">Der Code führt zwei identische Aufrufe der **Grafik aus::D rawellipse** -Methode.</span><span class="sxs-lookup"><span data-stu-id="add82-135">The code makes two identical calls to the **Graphics::DrawEllipse** method.</span></span> <span data-ttu-id="add82-136">Die globale Transformation wird auf die ersten **Grafiken angewendet::D rawellipse** -Aufrufe, und beide Transformationen (Welt und Seite) werden auf die zweite **Grafik angewendet::D rawellipse** -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="add82-136">The world transformation is applied to the first **Graphics::DrawEllipse** call, and both transformations (world and page) are applied to the second **Graphics::DrawEllipse** call.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



<span data-ttu-id="add82-137">Die folgende Abbildung zeigt die beiden Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="add82-137">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="add82-138">Beachten Sie, dass die 30-Grad-Drehung über den Ursprung des Koordinatensystems (obere linke Ecke des Client Bereichs) und nicht über die Mittelpunkte der Ellipsen liegt.</span><span class="sxs-lookup"><span data-stu-id="add82-138">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="add82-139">Beachten Sie außerdem, dass die Stift Breite 1 für die erste Ellipse 1 Pixel und für die zweite Ellipse 1 Millimeter bedeutet.</span><span class="sxs-lookup"><span data-stu-id="add82-139">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>

![Screenshot eines Fensters mit einer kleinen, dünnen Ellipse und einer großen, dickeren Ellipse](images/graphicsascon1.png)

 

### <a name="clipping-region"></a><span data-ttu-id="add82-141">Clippingbereich</span><span class="sxs-lookup"><span data-stu-id="add82-141">Clipping Region</span></span>

<span data-ttu-id="add82-142">Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verwaltet einen Clippingbereich, der für alle Elemente gilt, die von diesem **Grafik** Objekt gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="add82-142">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains a clipping region that applies to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="add82-143">Sie können den Clippingbereich festlegen, indem Sie die [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="add82-143">You can set the clipping region by calling the [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method.</span></span>

<span data-ttu-id="add82-144">Im folgenden Beispiel wird ein Plus förmiger Bereich erstellt, indem die Union von zwei Rechtecke gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="add82-144">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="add82-145">Diese Region wird als Clippingbereich eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="add82-145">That region is designated as the clipping region of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="add82-146">Anschließend zeichnet der Code zwei Zeilen, die auf das Innere des Clippingbereichs beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="add82-146">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



<span data-ttu-id="add82-147">In der folgenden Abbildung sind die ausgeschnittenen Zeilen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="add82-147">The following illustration shows the clipped lines.</span></span>

![Abbildung einer farbigen Form, die von zwei diagonalen roten Linien überschritten wird](images/graphicsascon2.png)

 

 
