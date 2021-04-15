---
description: 'Diese Anwendung baut auf dem Beispiel für eine Handschrift Sammlung auf, indem Sie das Löschen von Hand Strichen veranschaulicht. Das Beispiel stellt dem Benutzer ein Menü mit vier Modi zur Auswahl: Ink-fähig, löschen bei Cusp, löschen bei Schnittstellen und Löschen von Strichen.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Ink-Lösch Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525292"
---
# <a name="ink-erasing-sample"></a><span data-ttu-id="1cb1e-104">Ink-Lösch Beispiel</span><span class="sxs-lookup"><span data-stu-id="1cb1e-104">Ink Erasing Sample</span></span>

<span data-ttu-id="1cb1e-105">Diese Anwendung baut auf dem [Beispiel](ink-collection-sample.md) für eine Handschrift Sammlung auf, indem Sie das Löschen von Hand Strichen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-105">This application builds on the [Ink Collection Sample](ink-collection-sample.md) sample by demonstrating ink strokes deletion.</span></span> <span data-ttu-id="1cb1e-106">Das Beispiel stellt dem Benutzer ein Menü mit vier Modi zur Auswahl: Ink-fähig, löschen bei Cusp, löschen bei Schnittstellen und Löschen von Strichen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-106">The sample provides the user with a menu that has four modes to choose from: ink-enabled, erasing at cusp, erasing at intersections, and erasing strokes.</span></span>

<span data-ttu-id="1cb1e-107">Im frei Hand Eingabe fähigen Modus sammelt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei Hand Eingaben, wie im frei Hand Eingabe [Beispiel](ink-collection-sample.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-107">In ink-enabled mode, the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object collects ink as shown in [Ink Collection Sample](ink-collection-sample.md).</span></span>

<span data-ttu-id="1cb1e-108">In einem Lösch Modus werden Segmente vorhandener Hand Striche, die der Benutzer mit dem Cursor berührt, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-108">In an erasing mode, segments of existing ink strokes that the user touches with the cursor are erased.</span></span> <span data-ttu-id="1cb1e-109">Außerdem können die cusps oder Schnittmengen mit einem roten Kreis markiert werden.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-109">Also, the cusps or intersections may be marked with a red circle.</span></span>

<span data-ttu-id="1cb1e-110">Die interessantesten Teile dieses Beispiels liegen im `InkErase` -Ereignishandler des Formulars `OnPaint` und in den Löschfunktionen, die vom-Ereignishandler des Formulars aufgerufen werden `OnMouseMove` .</span><span class="sxs-lookup"><span data-stu-id="1cb1e-110">The most interesting parts of this sample lie in the `InkErase` form's `OnPaint` event handler and in the erasing functions that are called from the form's `OnMouseMove` event handler.</span></span>

## <a name="circling-the-cusps-and-intersections"></a><span data-ttu-id="1cb1e-111">Umschließen der cusps und Schnittmengen</span><span class="sxs-lookup"><span data-stu-id="1cb1e-111">Circling the Cusps and Intersections</span></span>

<span data-ttu-id="1cb1e-112">Der- `OnPaint` Ereignishandler des Formulars zeichnet zuerst die Striche, und in Abhängigkeit vom Anwendungsmodus werden möglicherweise alle cusps oder Schnittmengen mit einem kleinen roten Kreis gefunden und markiert.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-112">The form's `OnPaint` event handler first paints the strokes, and depending on the application mode, may find and mark all of the cusps or intersections with a small red circle.</span></span> <span data-ttu-id="1cb1e-113">Mit einem Cusp wird der Punkt gekennzeichnet, an dem ein Strich abrupt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-113">A cusp marks the point where a stroke changes direction abruptly.</span></span> <span data-ttu-id="1cb1e-114">Eine Schnittmenge markiert einen Punkt, an dem sich ein Strich mit sich selbst oder einem anderen Strich überschneidet.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-114">An intersection marks a point where one stroke intersects with itself or another stroke.</span></span>

<span data-ttu-id="1cb1e-115">Das [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignis tritt auf, wenn ein Steuerelement neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-115">The [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event occurs whenever a control is redrawn.</span></span>

> [!Note]  
> <span data-ttu-id="1cb1e-116">Im Beispiel wird das Formular gezwungen, sich selbst neu zu zeichnen, wenn ein Strich gelöscht wird, oder wenn sich der Anwendungsmodus ändert, indem die [Aktualisierungs](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) Methode des Formulars verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-116">The sample forces the form to redraw itself whenever a stroke is erased, or when the application mode changes, using the form's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method.</span></span>

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



<span data-ttu-id="1cb1e-117">In `PaintCusps` durchläuft der Code die einzelnen Cusp in jedem Strich und zeichnet einen roten Kreis herum.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-117">In `PaintCusps`, the code iterates through each cusp in each stroke, and draws a red circle around it.</span></span> <span data-ttu-id="1cb1e-118">Die [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) -Eigenschaft des Strichs gibt die Indizes der Punkte in einem Stoke zurück, die den cusps entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-118">The stroke's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) property returns the indices of the points within a stoke that correspond to cusps.</span></span> <span data-ttu-id="1cb1e-119">Beachten Sie auch die [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) , die den Punkt in die für die DrawEllipse-Methode relevanten Koordinaten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-119">Also, note the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) method, which converts the point to coordinates relevant to the DrawEllipse method.</span></span>


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



<span data-ttu-id="1cb1e-120">In `PaintIntersections` durchläuft der Code jeden Strich, um seine Schnittmengen mit dem gesamten Satz von Strichen zu finden.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-120">In `PaintIntersections`, the code iterates through each stroke to find its intersections with the entire set of strokes.</span></span> <span data-ttu-id="1cb1e-121">Beachten Sie, dass die [findinterabschnitts](/previous-versions/ms827856(v=msdn.10)) -Methode des Strichs an eine [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung übergeben wird und ein Array von Gleit Komma-Indexwerten zurückgibt, die die Schnittpunkte darstellen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-121">Note that the stroke's [FindIntersections](/previous-versions/ms827856(v=msdn.10)) method is passed a [Strokes](/previous-versions/ms827799(v=msdn.10)) collection and returns an array of floating point index values representing the intersections.</span></span> <span data-ttu-id="1cb1e-122">Der Code berechnet dann eine X-Y-Koordinate für jede Schnittmenge und zeichnet einen roten Kreis um.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-122">The code then calculates an X-Y coordinate for each intersection, and draws a red circle around it.</span></span>


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a><span data-ttu-id="1cb1e-123">Behandeln eines Stifts mit zwei Enden</span><span class="sxs-lookup"><span data-stu-id="1cb1e-123">Handling a Pen That Has Two Ends</span></span>

<span data-ttu-id="1cb1e-124">Für das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt werden drei Ereignishandler für die Ereignisse " [Cursor](/previous-versions/ms567611(v=vs.100))", " [newpaketen](/previous-versions/ms567621(v=vs.100))" und " [Stroke](/previous-versions/ms567622(v=vs.100)) " definiert.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-124">Three event handlers are defined for the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)), and [Stroke](/previous-versions/ms567622(v=vs.100)) events.</span></span> <span data-ttu-id="1cb1e-125">Jeder Ereignishandler überprüft die [invertierte](/previous-versions/ms839525(v=msdn.10)) Eigenschaft des [Cursor](/previous-versions/ms839521(v=msdn.10)) Objekts, um festzustellen, welches Ende des Stifts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-125">Each event handler checks the [Cursor](/previous-versions/ms839521(v=msdn.10)) object's [Inverted](/previous-versions/ms839525(v=msdn.10)) property to see which end of the pen is being used.</span></span> <span data-ttu-id="1cb1e-126">Wenn der Stift invertiert ist:</span><span class="sxs-lookup"><span data-stu-id="1cb1e-126">When the pen is inverted:</span></span>

-   <span data-ttu-id="1cb1e-127">Mit der- `myInkCollector_CursorDown` Methode wird der Strich transparent.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-127">The `myInkCollector_CursorDown` method makes the stroke transparent.</span></span>
-   <span data-ttu-id="1cb1e-128">Die- `myInkCollector_NewPackets` Methode löscht Striche.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-128">The `myInkCollector_NewPackets` method erases strokes.</span></span>
-   <span data-ttu-id="1cb1e-129">Die- `myInkCollector_Stroke` Methode bricht das-Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-129">The `myInkCollector_Stroke` method cancels the event.</span></span> <span data-ttu-id="1cb1e-130">[Newpakete](/previous-versions/ms567621(v=vs.100)) -Ereignisse werden vor dem [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) events are generated prior to the [Stroke](/previous-versions/ms567622(v=vs.100)) event.</span></span>

## <a name="tracking-the-cursor"></a><span data-ttu-id="1cb1e-131">Nachverfolgen des Cursors</span><span class="sxs-lookup"><span data-stu-id="1cb1e-131">Tracking the Cursor</span></span>

<span data-ttu-id="1cb1e-132">Unabhängig davon, ob der Benutzer einen Stift oder eine Maus verwendet, werden [MouseMove](/previous-versions/ms567617(v=vs.100)) -Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-132">Whether the user is using a pen or a mouse, [MouseMove](/previous-versions/ms567617(v=vs.100)) events are generated.</span></span> <span data-ttu-id="1cb1e-133">Der MouseMove-Ereignishandler prüft zunächst, ob der aktuelle Modus ein Lösch Modus ist und ob eine Maustaste gedrückt ist, und ignoriert das Ereignis, wenn diese Zustände nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-133">The MouseMove event handler first checks to determine whether the current mode is an erase mode and if any mouse button is pressed, and ignores the event if these states are not present.</span></span> <span data-ttu-id="1cb1e-134">Anschließend konvertiert der Ereignishandler die Pixelkoordinaten für den Cursor mithilfe der [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) in frei Hand Raumkoordinaten und ruft abhängig vom aktuellen Lösch Modus eine der Löschmethoden des Codes auf.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-134">Then, the event handler converts the pixel coordinates for the cursor into ink space coordinates by using the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method, and calls one of the code's erase methods depending on the current erase mode.</span></span>

## <a name="erasing-strokes"></a><span data-ttu-id="1cb1e-135">Löschen von Strichen</span><span class="sxs-lookup"><span data-stu-id="1cb1e-135">Erasing Strokes</span></span>

<span data-ttu-id="1cb1e-136">Die `EraseStrokes` -Methode übernimmt die Position des Cursors im frei Handzeichen Bereich und generiert eine Auflistung von Strichen, die sich innerhalb von `HitTestRadius` Einheiten befinden.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-136">The `EraseStrokes` method takes the cursor's location in ink space and generates a collection of strokes that are within `HitTestRadius` units.</span></span> <span data-ttu-id="1cb1e-137">Der- `currentStroke` Parameter gibt ein [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekt an, das nicht gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-137">The `currentStroke` parameter specifies a [Stroke](/previous-versions/ms827842(v=msdn.10)) object that should not be deleted.</span></span> <span data-ttu-id="1cb1e-138">Anschließend wird die Striche-Auflistung aus dem Collector gelöscht, und das Formular wird neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-138">Then the strokes collection is deleted from the collector, and the form is redrawn.</span></span>


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a><span data-ttu-id="1cb1e-139">Löschen bei Schnittmengen</span><span class="sxs-lookup"><span data-stu-id="1cb1e-139">Erasing at Intersections</span></span>

<span data-ttu-id="1cb1e-140">Die `EraseAtIntersections` -Methode durchläuft jeden Strich, der innerhalb des Test RADIUS liegt, und generiert ein Array von Schnittpunkten zwischen diesem Strich und allen anderen Strichen in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-140">The `EraseAtIntersections` method iterates over each stroke that falls within the test radius and generates an array of intersections between that stroke and all the other strokes in the collection.</span></span> <span data-ttu-id="1cb1e-141">Wenn keine Schnittmengen gefunden werden, wird der gesamte Strich gelöscht. Andernfalls befindet sich der nächste Punkt auf dem Strich zum Testpunkt, und von diesem wird die Schnittstelle auf beiden Seiten des Punkts gefunden, in der das zu entfernende Segment beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-141">If no intersections are found, then that entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="1cb1e-142">Die [Split](/previous-versions/ms828477(v=msdn.10)) -Methode des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts wird verwendet, um das Segment vom restlichen Strich zu trennen, und dann wird das Segment gelöscht, sodass der restliche Strich intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-142">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="1cb1e-143">Wie in `EraseStrokes` wird das Formular neu gezeichnet, bevor die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-143">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a><span data-ttu-id="1cb1e-144">Löschen bei cusps</span><span class="sxs-lookup"><span data-stu-id="1cb1e-144">Erasing at Cusps</span></span>

<span data-ttu-id="1cb1e-145">Für jeden Strich, der innerhalb des Test RADIUS liegt, `EraseAtCusps` Ruft die-Methode das Array von-Daten aus der [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) -Methode des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-145">For each stroke that falls within the test radius, the `EraseAtCusps` method retrieves the array of cusps from the [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) method.</span></span> <span data-ttu-id="1cb1e-146">Jedes Ende des Strichs ist ebenfalls ein Cusp. wenn der Strich nur zwei cusps hat, wird der gesamte Strich gelöscht. Andernfalls befindet sich der nächste Punkt auf dem Strich zum Testpunkt, und von diesem wird die Schnittstelle auf beiden Seiten des Punkts gefunden, in der das zu entfernende Segment beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-146">Each end of the stroke is also a cusp, so if the stroke only has two cusps, then the entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="1cb1e-147">Die [Split](/previous-versions/ms828477(v=msdn.10)) -Methode des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts wird verwendet, um das Segment vom restlichen Strich zu trennen, und dann wird das Segment gelöscht, sodass der restliche Strich intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-147">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="1cb1e-148">Wie in `EraseStrokes` wird das Formular neu gezeichnet, bevor die Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-148">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a><span data-ttu-id="1cb1e-149">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="1cb1e-149">Closing the Form</span></span>

<span data-ttu-id="1cb1e-150">Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="1cb1e-150">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
