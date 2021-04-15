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
# <a name="ink-erasing-sample"></a>Ink-Lösch Beispiel

Diese Anwendung baut auf dem [Beispiel](ink-collection-sample.md) für eine Handschrift Sammlung auf, indem Sie das Löschen von Hand Strichen veranschaulicht. Das Beispiel stellt dem Benutzer ein Menü mit vier Modi zur Auswahl: Ink-fähig, löschen bei Cusp, löschen bei Schnittstellen und Löschen von Strichen.

Im frei Hand Eingabe fähigen Modus sammelt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei Hand Eingaben, wie im frei Hand Eingabe [Beispiel](ink-collection-sample.md)gezeigt.

In einem Lösch Modus werden Segmente vorhandener Hand Striche, die der Benutzer mit dem Cursor berührt, gelöscht. Außerdem können die cusps oder Schnittmengen mit einem roten Kreis markiert werden.

Die interessantesten Teile dieses Beispiels liegen im `InkErase` -Ereignishandler des Formulars `OnPaint` und in den Löschfunktionen, die vom-Ereignishandler des Formulars aufgerufen werden `OnMouseMove` .

## <a name="circling-the-cusps-and-intersections"></a>Umschließen der cusps und Schnittmengen

Der- `OnPaint` Ereignishandler des Formulars zeichnet zuerst die Striche, und in Abhängigkeit vom Anwendungsmodus werden möglicherweise alle cusps oder Schnittmengen mit einem kleinen roten Kreis gefunden und markiert. Mit einem Cusp wird der Punkt gekennzeichnet, an dem ein Strich abrupt geändert wird. Eine Schnittmenge markiert einen Punkt, an dem sich ein Strich mit sich selbst oder einem anderen Strich überschneidet.

Das [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignis tritt auf, wenn ein Steuerelement neu gezeichnet wird.

> [!Note]  
> Im Beispiel wird das Formular gezwungen, sich selbst neu zu zeichnen, wenn ein Strich gelöscht wird, oder wenn sich der Anwendungsmodus ändert, indem die [Aktualisierungs](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) Methode des Formulars verwendet wird.

 


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



In `PaintCusps` durchläuft der Code die einzelnen Cusp in jedem Strich und zeichnet einen roten Kreis herum. Die [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) -Eigenschaft des Strichs gibt die Indizes der Punkte in einem Stoke zurück, die den cusps entsprechen. Beachten Sie auch die [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) , die den Punkt in die für die DrawEllipse-Methode relevanten Koordinaten konvertiert.


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



In `PaintIntersections` durchläuft der Code jeden Strich, um seine Schnittmengen mit dem gesamten Satz von Strichen zu finden. Beachten Sie, dass die [findinterabschnitts](/previous-versions/ms827856(v=msdn.10)) -Methode des Strichs an eine [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung übergeben wird und ein Array von Gleit Komma-Indexwerten zurückgibt, die die Schnittpunkte darstellen. Der Code berechnet dann eine X-Y-Koordinate für jede Schnittmenge und zeichnet einen roten Kreis um.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Behandeln eines Stifts mit zwei Enden

Für das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt werden drei Ereignishandler für die Ereignisse " [Cursor](/previous-versions/ms567611(v=vs.100))", " [newpaketen](/previous-versions/ms567621(v=vs.100))" und " [Stroke](/previous-versions/ms567622(v=vs.100)) " definiert. Jeder Ereignishandler überprüft die [invertierte](/previous-versions/ms839525(v=msdn.10)) Eigenschaft des [Cursor](/previous-versions/ms839521(v=msdn.10)) Objekts, um festzustellen, welches Ende des Stifts verwendet wird. Wenn der Stift invertiert ist:

-   Mit der- `myInkCollector_CursorDown` Methode wird der Strich transparent.
-   Die- `myInkCollector_NewPackets` Methode löscht Striche.
-   Die- `myInkCollector_Stroke` Methode bricht das-Ereignis ab. [Newpakete](/previous-versions/ms567621(v=vs.100)) -Ereignisse werden vor dem [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignis generiert.

## <a name="tracking-the-cursor"></a>Nachverfolgen des Cursors

Unabhängig davon, ob der Benutzer einen Stift oder eine Maus verwendet, werden [MouseMove](/previous-versions/ms567617(v=vs.100)) -Ereignisse generiert. Der MouseMove-Ereignishandler prüft zunächst, ob der aktuelle Modus ein Lösch Modus ist und ob eine Maustaste gedrückt ist, und ignoriert das Ereignis, wenn diese Zustände nicht vorhanden sind. Anschließend konvertiert der Ereignishandler die Pixelkoordinaten für den Cursor mithilfe der [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) in frei Hand Raumkoordinaten und ruft abhängig vom aktuellen Lösch Modus eine der Löschmethoden des Codes auf.

## <a name="erasing-strokes"></a>Löschen von Strichen

Die `EraseStrokes` -Methode übernimmt die Position des Cursors im frei Handzeichen Bereich und generiert eine Auflistung von Strichen, die sich innerhalb von `HitTestRadius` Einheiten befinden. Der- `currentStroke` Parameter gibt ein [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekt an, das nicht gelöscht werden soll. Anschließend wird die Striche-Auflistung aus dem Collector gelöscht, und das Formular wird neu gezeichnet.


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



## <a name="erasing-at-intersections"></a>Löschen bei Schnittmengen

Die `EraseAtIntersections` -Methode durchläuft jeden Strich, der innerhalb des Test RADIUS liegt, und generiert ein Array von Schnittpunkten zwischen diesem Strich und allen anderen Strichen in der Auflistung. Wenn keine Schnittmengen gefunden werden, wird der gesamte Strich gelöscht. Andernfalls befindet sich der nächste Punkt auf dem Strich zum Testpunkt, und von diesem wird die Schnittstelle auf beiden Seiten des Punkts gefunden, in der das zu entfernende Segment beschrieben wird.

Die [Split](/previous-versions/ms828477(v=msdn.10)) -Methode des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts wird verwendet, um das Segment vom restlichen Strich zu trennen, und dann wird das Segment gelöscht, sodass der restliche Strich intakt bleibt. Wie in `EraseStrokes` wird das Formular neu gezeichnet, bevor die Methode zurückgibt.


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



## <a name="erasing-at-cusps"></a>Löschen bei cusps

Für jeden Strich, der innerhalb des Test RADIUS liegt, `EraseAtCusps` Ruft die-Methode das Array von-Daten aus der [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) -Methode des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts ab. Jedes Ende des Strichs ist ebenfalls ein Cusp. wenn der Strich nur zwei cusps hat, wird der gesamte Strich gelöscht. Andernfalls befindet sich der nächste Punkt auf dem Strich zum Testpunkt, und von diesem wird die Schnittstelle auf beiden Seiten des Punkts gefunden, in der das zu entfernende Segment beschrieben wird.

Die [Split](/previous-versions/ms828477(v=msdn.10)) -Methode des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts wird verwendet, um das Segment vom restlichen Strich zu trennen, und dann wird das Segment gelöscht, sodass der restliche Strich intakt bleibt. Wie in `EraseStrokes` wird das Formular neu gezeichnet, bevor die Methode zurückgibt.


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



## <a name="closing-the-form"></a>Schließen des Formulars

Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei `myInkCollector` .

 

 
