---
description: Dieses Beispiel basiert auf dem Beispiel für die Ink-Sammlung. Es zeigt, wie das Divider-Objekt zum Analysieren von Ink-Eingaben verwendet wird.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Beispiel für Ink Divider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c74592606ba98ec913dd419deda1b2b766066e17545e95f18a14980f36dafde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452097"
---
# <a name="ink-divider-sample"></a>Beispiel für Ink Divider

Dieses Beispiel basiert auf dem Beispiel für die [Ink-Sammlung.](ink-collection-sample.md) Es zeigt, wie das [Divider-Objekt](/previous-versions/ms839398(v=msdn.10)) zum Analysieren von Ink-Eingaben verwendet wird.

Ausführliche konzeptionelle Informationen zu [Divider](/previous-versions/ms839398(v=msdn.10))finden Sie unter [The Divider Object](the-divider-object.md).

Wenn das Formular aktualisiert wird, zeichnet das Beispiel ein umgebendes Rechteck um jede analysierte Einheit, unterteilt in Wörter, Zeilen, Absätze und Zeichnungen. Neben der Verwendung unterschiedlicher Farben werden diese Rechtecke um unterschiedliche Mengen vergrößert, um sicherzustellen, dass keines der Rechtecke von anderen verdeckt wird. Die folgende Tabelle gibt die Farbe und Färbung für jede analysierte Einheit an.



| Analysierte Einheit        | Color              | Pixelzunge |
|----------------------|--------------------|-------------------|
| Word<br/>      | Grün<br/>   | 1<br/>      |
| Linie<br/>      | Magenta<br/> | 3<br/>      |
| Paragraph<br/> | Blau<br/>    | 5<br/>      |
| Zeichnung<br/>   | Red<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>Einrichten des Formulars

Wenn das Formular geladen wird, wird ein [Divider-Objekt](/previous-versions/ms839398(v=msdn.10)) erstellt. Ein [InkOverlay-Objekt](/previous-versions/ms833057(v=msdn.10)) wird erstellt und einem Bereich im Formular zugeordnet. Anschließend werden Ereignishandler an das InkOverlay-Objekt angefügt, um nachzuverfolgen, wann Striche hinzugefügt und gelöscht werden. Wenn Erkennungen verfügbar sind, wird dem Divider ein [RecognizerContext-Objekt](/previous-versions/ms828542(v=msdn.10)) für die Standarderkennung zugewiesen. Anschließend wird die [LineHeight-Eigenschaft](/previous-versions/ms839409(v=msdn.10)) des Divider-Objekts festgelegt, und die [Strokes-Auflistung](/previous-versions/ms827799(v=msdn.10)) aus dem InkOverlay-Objekt wird dem Divider zugewiesen. Schließlich ist das InkOverlay-Objekt aktiviert.


```C++
// Create the ink overlay and associate it with the form
myInkOverlay = new Microsoft.Ink.InkOverlay(DrawArea.Handle);

// Set the erasing mode to stroke erase.
myInkOverlay.EraserMode = InkOverlayEraserMode.StrokeErase;

// Hook event handler for the Stroke event to myInkOverlay_Stroke.
// This is necessary since the application needs to pass the strokes 
// to the ink divider.
myInkOverlay.Stroke += new InkCollectorStrokeEventHandler(myInkOverlay_Stroke); 

// Hook the event handler for StrokeDeleting event to myInkOverlay_StrokeDeleting.
// This is necessary as the application needs to remove the strokes from 
// ink divider object as well.
myInkOverlay.StrokesDeleting += new InkOverlayStrokesDeletingEventHandler(myInkOverlay_StrokeDeleting);

// Hook the event handler for StrokeDeleted event to myInkOverlay_StrokeDeleted.
// This is necessary to update the layout analysis result when automatic layout analysis
// option is selected.
myInkOverlay.StrokesDeleted += new InkOverlayStrokesDeletedEventHandler(myInkOverlay_StrokeDeleted);

// Create the ink divider object
myInkDivider = new Divider();

// Add a default recognizer context to the divider object
// without adding the recognizer context, the divider would
// not use a recognizer to do its word segmentation and would
// have less accurate results.
// Adding the recognizer context slows down the call to 
// myInkDivider.Divide though.
// It is possible that there is no recognizer installed on the
// machine for this language. In that case the divider does
// not use a recognizer to improve its accuracy.
// Get the default recognizer if any
try
{
    Recognizers recognizers = new Recognizers();
     myInkDivider.RecognizerContext = recognizers.GetDefaultRecognizer().CreateRecognizerContext();
}
catch (InvalidOperationException)
{
     //We are in the case where no default recognizers can be found
}

    // The LineHeight property helps the InkDivider distinguish between 
    // drawing and handwriting. The value should be the expected height 
    // of the user's handwriting in ink space units (0.01mm).
    // Here we set the LineHeight to 840, which is about 1/3 of an inch.
    myInkDivider.LineHeight = 840;

// Assign ink overlay's strokes collection to the ink divider
// This strokes collection is updated in the event handler
myInkDivider.Strokes = myInkOverlay.Ink.Strokes;

// Enable ink collection
myInkOverlay.Enabled = true;
```



Die Strokes-Auflistung des [Divider-Objekts](/previous-versions/ms839398(v=msdn.10)) muss mit der [Strokes-Sammlung](/previous-versions/ms839422(v=msdn.10)) des [](/previous-versions/ms827799(v=msdn.10)) [InkOverlay-Objekts](/previous-versions/ms833057(v=msdn.10)) synchron gehalten werden (zugriff über die InkOverlay-Eigenschaft des [InkOverlay-Objekts).](/previous-versions/ms833110(v=msdn.10)) Um sicherzustellen, dass [](/previous-versions/ms835344(v=msdn.10)) dies geschieht, wird der Stroke-Ereignishandler für das InkOverlay-Objekt wie folgt geschrieben. Beachten Sie, dass der Ereignishandler zuerst testet, ob [EditingMode](/previous-versions/ms833105(v=msdn.10)) auf **Ink** festgelegt ist, um Radiererstriche herauszufiltern. Wenn der Benutzer die automatische Layoutanalyse angefordert hat, ruft die Anwendung die DivideInk-Methode des Formulars auf und aktualisiert den Zeichnungsbereich.


```C++
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e )
{
    // Filter out the eraser stroke.
    if(InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
    {
        // Add the new stroke to the ink divider's strokes collection
        myInkDivider.Strokes.Add(e.Stroke);
        
        if(miAutomaticLayoutAnalysis.Checked)
        {
            // Call DivideInk
            DivideInk();

            // Repaint the screen to reflect the change
            DrawArea.Refresh();
        }
    }
}
```



## <a name="dividing-the-ink"></a>Unterteilen der Ink-Spalte

Wenn der Benutzer im Menü Datei auf Dividieren klickt, wird die [Divide-Methode](/previous-versions/ms839461(v=msdn.10)) für das [Divider-Objekt](/previous-versions/ms839398(v=msdn.10)) aufgerufen. Die Standarderkennung wird verwendet, falls verfügbar.


```C++
DivisionResult divResult = myInkDivider.Divide();
```



Das resultierende [DivisionResult-Objekt,](/previous-versions/ms839371(v=msdn.10)) auf das von der Variablen verwiesen `divResult` wird, wird an die Hilfsprogrammfunktion `getUnitBBBoxes()` übergeben. Die Hilfsprogrammfunktion gibt ein Array von Rechtecke für den angeforderten Divisionstyp zurück: Segmente, Linien, Absätze oder Zeichnungen.


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



Schließlich wird der Formularbereich gezwungen, neu zu zeichnen, damit die umgrenzenden Rechtecke angezeigt werden.


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>Ergebnisse der Ink-Analyse

In der Hilfsprogrammfunktion wird das [DivisionResult-Objekt](/previous-versions/ms839371(v=msdn.10)) basierend auf dem vom Aufrufer angeforderten Divisionstyp mithilfe der [ResultByType-Methode](/previous-versions/ms839388(v=msdn.10)) nach seinen Ergebnissen abgefragt. Die ResultByType-Methode gibt eine [DivisionUnits-Auflistung](/previous-versions/ms837954(v=msdn.10)) zurück. Jede [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in der Auflistung stellt eine Zeichnung, ein einzelnes Erkennungssegment der Handschrift, eine Handschriftzeile oder einen Handschriftblock dar, je nachdem, was beim Aufruf der Hilfsprogrammfunktion angegeben wurde.


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



Wenn mindestens eine [DivisionUnit](/previous-versions/ms837976(v=msdn.10))vorhanden ist, wird ein Array von Rechtecke erstellt, das ein umgrenzendes Rechteck pro Einheit enthält. (Die Rechtecke werden für jeden Typ von Einheit um unterschiedliche Mengen aufgeblasen, die in der Flate-Variablen gehalten werden, um Überlappungen zu verhindern.)


```C++
// If there is at least one unit, we construct the rectangles
if((null != units) && (0 < units.Count))
{
    // We need to convert rectangles from ink units to
    // pixel units. For that, we need Graphics object
    // to pass to InkRenderer.InkSpaceToPixel method
    using (Graphics g = DrawArea.CreateGraphics())
    {

    // InkSpace to Pixel Space conversion setup done here. 
    // Not shown for brevity.

        // Iterate through the collection of division units to obtain the bounding boxes
        foreach(DivisionUnit unit in units)
        {
            // Get the bounding box of the strokes of the division unit
            divRects[i] = unit.Strokes.GetBoundingBox();

            // Div unit rect Ink space to Pixel space conversion done here. 
            // Not shown for brevity.

            // Inflate the rectangle by inflate pixels in both directions
            divRects[i].Inflate(inflate, inflate);

            // Increment the index
            ++i;
        }

    } // Relinquish the Graphics object
}
```



## <a name="redrawing-the-form"></a>Umformung des Formulars

Wenn die Neuzeichnung oben erzwungen wird, wird der folgende Code ausgeführt, um die Begrenzungsfelder für jede [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) im Formular um die Ink zu zeichnen.


```C++
private void DrawArea_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
        {
            // Create the Pen used to draw bounding boxes.
            // First set of bounding boxes drawn here are 
            // the bounding boxes of paragraphs.
            // These boxes are drawn with Blue pen.
            Pen penBox = new Pen(Color.Blue, 2);

            // First, draw the bounding boxes for Paragraphs
            if(null != myParagraphBoundingBoxes)
            {
                // Draw bounding boxes for Paragraphs
                e.Graphics.DrawRectangles(penBox, myParagraphBoundingBoxes);
            }

            // Next, draw the bounding boxes for Lines
            if(null != myLineBoundingBoxes)
            {
                // Color is Magenta pen
                penBox.Color = Color.Magenta;
                // Draw the bounding boxes for Lines
                e.Graphics.DrawRectangles(penBox, myLineBoundingBoxes);
            }
            
            // Then, draw the bounding boxes for Words
            if(null != myWordBoundingBoxes)
            {
                // Color is Green
                penBox.Color = Color.Green;
                // Draw bounding boxes for Words
                e.Graphics.DrawRectangles(penBox, myWordBoundingBoxes);
            }
            
            // Finally, draw the boxes for Drawings
            if(null != myDrawingBoundingBoxes)
            {
                // Color is Red pen
                penBox.Color = Color.Red;
                // Draw bounding boxes for Drawings
                e.Graphics.DrawRectangles(penBox, myDrawingBoundingBoxes);
            }
        }
```



## <a name="closing-the-form"></a>Schließen des Formulars

Die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) des Formulars gibt die [InkOverlay-,](/previous-versions/ms833057(v=msdn.10)) [Divider-,](/previous-versions/ms839398(v=msdn.10)) [RecognizerContext-Objekte](/previous-versions/ms828542(v=msdn.10)) und die im Beispiel verwendete [Strokes-Auflistung](/previous-versions/ms827799(v=msdn.10)) frei.

 

