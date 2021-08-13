---
description: 'Diese Anwendung baut auf dem Beispiel für die Ink-Sammlung auf, indem das Löschen von Ink-Strichen demonstriert wird. Das Beispiel stellt dem Benutzer ein Menü zur Verfügung, aus dem vier Modi zur Auswahl stehen: Freischrift aktiviert, Löschen am Cusp, Löschen an Schnittmengen und Löschen von Strichen.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Beispiel für das Löschen von Ink-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b56885835a2d42c3f4c050938658cfc7cdf5a5d5463309ae2f0a6d8021c817e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452078"
---
# <a name="ink-erasing-sample"></a>Beispiel für das Löschen von Ink-Daten

Diese Anwendung baut auf dem [Beispiel für die Ink-Sammlung auf,](ink-collection-sample.md) indem das Löschen von Ink-Strichen demonstriert wird. Das Beispiel stellt dem Benutzer ein Menü zur Verfügung, aus dem vier Modi zur Auswahl stehen: Freischrift aktiviert, Löschen am Cusp, Löschen an Schnittmengen und Löschen von Strichen.

Im Ink-fähigen Modus erfasst das [InkCollector-Objekt Ink-Objekte,](/previous-versions/ms836493(v=msdn.10)) wie im [Ink Collection Sample (Ink-Sammlungsbeispiel) gezeigt.](ink-collection-sample.md)

In einem Löschmodus werden Segmente vorhandener Ink-Striche, die der Benutzer mit dem Cursor berührt, gelöscht. Außerdem können die Cusps oder Schnittpunkte mit einem roten Kreis markiert werden.

Die interessantesten Teile dieses Beispiels liegen im Ereignishandler des Formulars und in den Löschen-Funktionen, die vom Ereignishandler des `InkErase` `OnPaint` Formulars `OnMouseMove` aufgerufen werden.

## <a name="circling-the-cusps-and-intersections"></a>Kreisen der Cusps und Schnittmengen

Der Ereignishandler des Formulars zeichnet zuerst die Striche und kann je nach Anwendungsmodus alle Cusps oder Schnittpunkte mit einem kleinen roten Kreis suchen `OnPaint` und markieren. Ein Cusp markiert den Punkt, an dem ein Strich die Richtung plötzlich ändert. Eine Schnittmenge markiert einen Punkt, an dem sich ein Strich mit sich selbst oder einem anderen Strich überschneidet.

Das [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) tritt auf, wenn ein Steuerelement neu gezeichnet wird.

> [!Note]  
> Das Beispiel erzwingt, dass das Formular sich selbst neu gezeichnet, wenn ein Strich gelöscht wird oder wenn sich der Anwendungsmodus ändert, indem die Refresh-Methode des [Formulars verwendet](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) wird.

 


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



In durch iteriert der Code jeden Cusp in jedem Strich und zeichnet einen `PaintCusps` roten Kreis um ihn. Die [PolylineCusps-Eigenschaft](/previous-versions/ms827853(v=msdn.10)) des Strichs gibt die Indizes der Punkte innerhalb eines Strichs zurück, die Cusps entsprechen. Beachten Sie außerdem die [InkSpaceToPixel-Methode](/previous-versions/ms828495(v=msdn.10)) des [Rendererobjekts,](/previous-versions/ms828481(v=msdn.10)) die den Punkt in Koordinaten konvertiert, die für die DrawEllipse-Methode relevant sind.


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



In durch iteriert der Code jeden Strich, um seine Schnittmengen mit `PaintIntersections` dem gesamten Satz von Strichen zu finden. Beachten Sie, dass der [FindIntersections-Methode](/previous-versions/ms827856(v=msdn.10)) des Strichs eine [Strokes-Auflistung](/previous-versions/ms827799(v=msdn.10)) übergeben wird und ein Array von Gleitkommaindexwerten zurückgibt, die die Schnittmengen darstellen. Der Code berechnet dann eine X-Y-Koordinate für jede Schnittmenge und zeichnet einen roten Kreis um sie.


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

Für das [InkCollector-Objekt](/previous-versions/ms836493(v=msdn.10)) werden drei Ereignishandler für die [CursorDown-,](/previous-versions/ms567611(v=vs.100)) [NewPackets-](/previous-versions/ms567621(v=vs.100))und [Stroke-Ereignisse](/previous-versions/ms567622(v=vs.100)) definiert. Jeder Ereignishandler überprüft die [Inverted-Eigenschaft](/previous-versions/ms839525(v=msdn.10)) des [Cursorobjekts,](/previous-versions/ms839521(v=msdn.10)) um zu sehen, welches Ende des Stifts verwendet wird. Wenn der Stift invertiert ist:

-   Die `myInkCollector_CursorDown` -Methode macht den Strich transparent.
-   Die `myInkCollector_NewPackets` -Methode löscht Striche.
-   Die `myInkCollector_Stroke` -Methode bricht das Ereignis ab. [NewPackets-Ereignisse](/previous-versions/ms567621(v=vs.100)) werden vor dem [Stroke-Ereignis](/previous-versions/ms567622(v=vs.100)) generiert.

## <a name="tracking-the-cursor"></a>Nachverfolgen des Cursors

Unabhängig davon, ob der Benutzer einen Stift oder eine Maus verwendet, [werden MouseMove-Ereignisse](/previous-versions/ms567617(v=vs.100)) generiert. Der MouseMove-Ereignishandler überprüft zunächst, ob der aktuelle Modus ein Löschmodus ist und ob eine Maustaste gedrückt wird, und ignoriert das Ereignis, wenn diese Zustände nicht vorhanden sind. Anschließend konvertiert der Ereignishandler die Pixelkoordinaten für den Cursor mithilfe der [PixelToInkSpace-Methode](/previous-versions/ms828505(v=msdn.10)) des [Rendererobjekts](/previous-versions/ms828481(v=msdn.10)) in Freiraumkoordinaten und ruft abhängig vom aktuellen Löschmodus eine der Methoden zum Löschen des Codes auf.

## <a name="erasing-strokes"></a>Löschen von Strichen

Die -Methode verwendet die Position des Cursors im Freiraum und generiert eine Auflistung von Strichen, `EraseStrokes` die sich innerhalb von Einheiten `HitTestRadius` befinden. Der `currentStroke` -Parameter gibt ein [Stroke-Objekt](/previous-versions/ms827842(v=msdn.10)) an, das nicht gelöscht werden soll. Anschließend wird die Strichsammlung aus dem Collector gelöscht, und das Formular wird neu gezeichnet.


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



## <a name="erasing-at-intersections"></a>Löschen an Schnittmengen

Die -Methode durch iteriert jeden Strich, der innerhalb des Testradius liegt, und generiert ein Array von Schnittmengen zwischen diesem Strich und allen anderen Strichen `EraseAtIntersections` in der Auflistung. Wenn keine Schnittpunkte gefunden werden, wird der gesamte Strich gelöscht. Andernfalls wird der nächste Punkt auf dem Strich zum Testpunkt gefunden, und von diesem Punkt aus werden die Schnittpunkte auf beiden Seiten des Punkts gefunden, die das zu entfernende Segment beschreiben.

Die [Split-Methode](/previous-versions/ms827842(v=msdn.10)) des [Stroke-Objekts](/previous-versions/ms828477(v=msdn.10)) wird verwendet, um das Segment vom Rest des Strichs zu trennen. Anschließend wird das Segment gelöscht, und der Rest des Strichs bleibt erhalten. Wie in `EraseStrokes` wird das Formular neu gezeichnet, bevor die Methode zurückgegeben wird.


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



## <a name="erasing-at-cusps"></a>Löschen bei Cusps

Für jeden Strich, der innerhalb des Testradius liegt, ruft die -Methode das Array von Cusps aus der `EraseAtCusps` [PolylineCusps-Methode](/previous-versions/ms827853(v=msdn.10)) des [Stroke-Objekts](/previous-versions/ms827842(v=msdn.10)) ab. Jedes Ende des Strichs ist auch ein Cusp. Wenn der Strich also nur zwei Cusps auft, wird der gesamte Strich gelöscht. Andernfalls wird der nächste Punkt auf dem Strich zum Testpunkt gefunden, und von diesem Punkt werden die Schnittpunkte auf beiden Seiten des Punkts gefunden, was das zu entfernende Segment beschreibt.

Die [Split-Methode](/previous-versions/ms827842(v=msdn.10)) des [Stroke-Objekts](/previous-versions/ms828477(v=msdn.10)) wird verwendet, um das Segment vom Rest des Strichs zu trennen. Anschließend wird das Segment gelöscht, und der Rest des Strichs bleibt erhalten. Wie in `EraseStrokes` wird das Formular neu gezeichnet, bevor die Methode zurückgegeben wird.


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

Die Dispose-Methode [des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector-Objekt](/previous-versions/ms836493(v=msdn.10)) `myInkCollector` zurück.

 

 
