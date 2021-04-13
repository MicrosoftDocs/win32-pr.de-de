---
description: Dieses Beispiel basiert auf dem Ink Collection-Beispiel. Es wird gezeigt, wie das Divider-Objekt verwendet wird, um frei Hand Eingaben zu analysieren.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Ink-Divider-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a272d6a5530938e6fecfeefc9f46ffdd0835d045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484379"
---
# <a name="ink-divider-sample"></a>Ink-Divider-Beispiel

Dieses Beispiel basiert auf dem [Ink Collection-Beispiel](ink-collection-sample.md). Es wird gezeigt, wie das [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekt verwendet wird, um frei Hand Eingaben zu analysieren.

Ausführliche konzeptionelle Informationen zum unter [Teiler](/previous-versions/ms839398(v=msdn.10))finden Sie [unter Divider-Objekt](the-divider-object.md).

Wenn das Formular aktualisiert wird, zeichnet das Beispiel ein umschließendes Rechteck um jede analysierte Einheit, das in Wörter, Zeilen, Absätze und Zeichnungen unterteilt ist. Abgesehen von der Verwendung verschiedener Farben werden diese Rechtecke um unterschiedliche Beträge vergrößert, um sicherzustellen, dass keine der Rechtecke von anderen Personen verdeckt wird. In der folgenden Tabelle werden die Farbe und die Vergrößerung der einzelnen analysierten Einheiten angegeben.



| analysierte Einheit        | Color              | Pixel Vergrößerung |
|----------------------|--------------------|-------------------|
| Word<br/>      | Grün<br/>   | 1<br/>      |
| Zeile<br/>      | Magenta<br/> | 3<br/>      |
| Paragraph<br/> | Blau<br/>    | 5<br/>      |
| Zeichnung<br/>   | Red<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>Einrichten des Formulars

Wenn das Formular geladen wird, wird ein [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekt erstellt. Ein [InkOverlay](/previous-versions/ms833057(v=msdn.10)) -Objekt wird erstellt und einem Panel auf dem Formular zugeordnet. Anschließend werden Ereignishandler an das InkOverlay-Objekt angefügt, um zu verfolgen, wann Striche hinzugefügt und gelöscht werden. Wenn Erkennungs Tools verfügbar sind, wird dem unter Teiler ein [Erkennungs Kontext](/previous-versions/ms828542(v=msdn.10)) Objekt für die Standard Erkennung zugewiesen. Anschließend wird die [LineHeight](/previous-versions/ms839409(v=msdn.10)) -Eigenschaft des Divider-Objekts festgelegt, und die [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung aus dem InkOverlay-Objekt wird dem unter Teiler zugewiesen. Zum Schluss ist das InkOverlay-Objekt aktiviert.


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



Die [Striche](/previous-versions/ms839422(v=msdn.10)) -Auflistung des [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekts muss mit der [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung des [InkOverlay](/previous-versions/ms833057(v=msdn.10)) -Objekts synchron gehalten werden (der Zugriff erfolgt über die [Ink](/previous-versions/ms833110(v=msdn.10)) -Eigenschaft des InkOverlay-Objekts). Um sicherzustellen, dass dies geschieht, wird der [Stroke](/previous-versions/ms835344(v=msdn.10)) -Ereignishandler für das InkOverlay-Objekt wie folgt geschrieben. Beachten Sie, dass der Ereignishandler zuerst testet, ob [EditingMode](/previous-versions/ms833105(v=msdn.10)) auf **Ink** festgelegt ist, um radiererstriche herauszufiltern. Wenn der Benutzer eine automatische Layoutanalyse angefordert hat, ruft die Anwendung die divideink-Methode des Formulars auf und aktualisiert den Zeichnungs Bereich.


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



## <a name="dividing-the-ink"></a>Aufteilen der frei Hand Eingaben

Wenn der Benutzer im Menü Datei auf aufteilen klickt, wird die [Divide](/previous-versions/ms839461(v=msdn.10)) -Methode für das [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekt aufgerufen. Die Standard Erkennung wird verwendet, falls verfügbar.


```C++
DivisionResult divResult = myInkDivider.Divide();
```



Das resultierende [DivisionResult](/previous-versions/ms839371(v=msdn.10)) -Objekt, auf das von der-Variable verwiesen wird, `divResult` wird an eine Utility-Funktion,, übergeben `getUnitBBBoxes()` . Die Utility-Funktion gibt ein Array von Rechtecke für alle angeforderten Divisions Typen zurück: Segmente, Linien, Absätze oder Zeichnungen.


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



Schließlich muss der Formular Bereich neu gezeichnet werden, damit die umgebenden Rechtecke angezeigt werden.


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>Ergebnisse der frei Hand Analyse

In der Utility-Funktion wird das [DivisionResult](/previous-versions/ms839371(v=msdn.10)) -Objekt mithilfe der Methode [ResultByType](/previous-versions/ms839388(v=msdn.10)) auf Grundlage des vom Aufrufer angeforderten Divisions Typs abgefragt. Die ResultByType-Methode gibt eine [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) -Auflistung zurück. Jede [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in der Auflistung stellt eine Zeichnung, ein einzelnes Erkennungs Segment der Handschrift, eine Handschrift Zeile oder einen Hand schriftblock dar, je nachdem, was beim Aufrufen der Hilfsprogrammfunktion angegeben wurde.


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



Wenn mindestens eine [DivisionUnit](/previous-versions/ms837976(v=msdn.10))vorhanden ist, wird ein Array mit Rechtecke erstellt, das ein umschließendes Rechteck pro Einheit enthält. (Die Rechtecke werden durch unterschiedliche Beträge für jeden Typ von Einheit aufgeblasen, der in der Vergrößerung-Variablen enthalten ist, um Überschneidungen zu vermeiden.)


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



## <a name="redrawing-the-form"></a>Das Formular wird neu gezeichnet.

Wenn das Neuzeichnen überschritten wird, wird der folgende Code ausgeführt, um die umgebenden Felder für jede [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) im Formular um das frei Handzeichen zu zeichnen.


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

Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) löscht die Objekte [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [erkenzercontext](/previous-versions/ms828542(v=msdn.10)) und die im Beispiel verwendete [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung.

 

