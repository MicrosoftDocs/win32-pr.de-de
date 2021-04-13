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
# <a name="ink-divider-sample"></a><span data-ttu-id="2e462-104">Ink-Divider-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e462-104">Ink Divider Sample</span></span>

<span data-ttu-id="2e462-105">Dieses Beispiel basiert auf dem [Ink Collection-Beispiel](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2e462-105">This sample is based on the [Ink Collection Sample](ink-collection-sample.md).</span></span> <span data-ttu-id="2e462-106">Es wird gezeigt, wie das [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekt verwendet wird, um frei Hand Eingaben zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="2e462-106">It shows how to use the [Divider](/previous-versions/ms839398(v=msdn.10)) object to analyze ink input.</span></span>

<span data-ttu-id="2e462-107">Ausführliche konzeptionelle Informationen zum unter [Teiler](/previous-versions/ms839398(v=msdn.10))finden Sie [unter Divider-Objekt](the-divider-object.md).</span><span class="sxs-lookup"><span data-stu-id="2e462-107">For detailed conceptual information about [Divider](/previous-versions/ms839398(v=msdn.10)), see [The Divider Object](the-divider-object.md).</span></span>

<span data-ttu-id="2e462-108">Wenn das Formular aktualisiert wird, zeichnet das Beispiel ein umschließendes Rechteck um jede analysierte Einheit, das in Wörter, Zeilen, Absätze und Zeichnungen unterteilt ist.</span><span class="sxs-lookup"><span data-stu-id="2e462-108">When the form is updated, the sample draws a bounding rectangle around each analyzed unit, broken into words, lines, paragraphs, and drawings.</span></span> <span data-ttu-id="2e462-109">Abgesehen von der Verwendung verschiedener Farben werden diese Rechtecke um unterschiedliche Beträge vergrößert, um sicherzustellen, dass keine der Rechtecke von anderen Personen verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="2e462-109">Besides using different colors, these rectangles are enlarged by different amounts to ensure that none of the rectangles is obscured by others.</span></span> <span data-ttu-id="2e462-110">In der folgenden Tabelle werden die Farbe und die Vergrößerung der einzelnen analysierten Einheiten angegeben.</span><span class="sxs-lookup"><span data-stu-id="2e462-110">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="2e462-111">analysierte Einheit</span><span class="sxs-lookup"><span data-stu-id="2e462-111">analyzed Unit</span></span>        | <span data-ttu-id="2e462-112">Color</span><span class="sxs-lookup"><span data-stu-id="2e462-112">Color</span></span>              | <span data-ttu-id="2e462-113">Pixel Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="2e462-113">Pixel Enlargement</span></span> |
|----------------------|--------------------|-------------------|
| <span data-ttu-id="2e462-114">Word</span><span class="sxs-lookup"><span data-stu-id="2e462-114">Word</span></span><br/>      | <span data-ttu-id="2e462-115">Grün</span><span class="sxs-lookup"><span data-stu-id="2e462-115">Green</span></span><br/>   | <span data-ttu-id="2e462-116">1</span><span class="sxs-lookup"><span data-stu-id="2e462-116">1</span></span><br/>      |
| <span data-ttu-id="2e462-117">Zeile</span><span class="sxs-lookup"><span data-stu-id="2e462-117">Line</span></span><br/>      | <span data-ttu-id="2e462-118">Magenta</span><span class="sxs-lookup"><span data-stu-id="2e462-118">Magenta</span></span><br/> | <span data-ttu-id="2e462-119">3</span><span class="sxs-lookup"><span data-stu-id="2e462-119">3</span></span><br/>      |
| <span data-ttu-id="2e462-120">Paragraph</span><span class="sxs-lookup"><span data-stu-id="2e462-120">Paragraph</span></span><br/> | <span data-ttu-id="2e462-121">Blau</span><span class="sxs-lookup"><span data-stu-id="2e462-121">Blue</span></span><br/>    | <span data-ttu-id="2e462-122">5</span><span class="sxs-lookup"><span data-stu-id="2e462-122">5</span></span><br/>      |
| <span data-ttu-id="2e462-123">Zeichnung</span><span class="sxs-lookup"><span data-stu-id="2e462-123">Drawing</span></span><br/>   | <span data-ttu-id="2e462-124">Red</span><span class="sxs-lookup"><span data-stu-id="2e462-124">Red</span></span><br/>     | <span data-ttu-id="2e462-125">1</span><span class="sxs-lookup"><span data-stu-id="2e462-125">1</span></span><br/>      |



 

## <a name="setting-up-the-form"></a><span data-ttu-id="2e462-126">Einrichten des Formulars</span><span class="sxs-lookup"><span data-stu-id="2e462-126">Setting Up the Form</span></span>

<span data-ttu-id="2e462-127">Wenn das Formular geladen wird, wird ein [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e462-127">When the form loads, a [Divider](/previous-versions/ms839398(v=msdn.10)) object is created.</span></span> <span data-ttu-id="2e462-128">Ein [InkOverlay](/previous-versions/ms833057(v=msdn.10)) -Objekt wird erstellt und einem Panel auf dem Formular zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2e462-128">An [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object is created and associated with a panel on the form.</span></span> <span data-ttu-id="2e462-129">Anschließend werden Ereignishandler an das InkOverlay-Objekt angefügt, um zu verfolgen, wann Striche hinzugefügt und gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2e462-129">Then event handlers are attached to the InkOverlay object to track when strokes are added and deleted.</span></span> <span data-ttu-id="2e462-130">Wenn Erkennungs Tools verfügbar sind, wird dem unter Teiler ein [Erkennungs Kontext](/previous-versions/ms828542(v=msdn.10)) Objekt für die Standard Erkennung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2e462-130">Then if recognizers are available, a [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) object for the default recognizer is assigned to the Divider.</span></span> <span data-ttu-id="2e462-131">Anschließend wird die [LineHeight](/previous-versions/ms839409(v=msdn.10)) -Eigenschaft des Divider-Objekts festgelegt, und die [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung aus dem InkOverlay-Objekt wird dem unter Teiler zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2e462-131">Then the Divider object's [LineHeight](/previous-versions/ms839409(v=msdn.10)) property is set and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection from the InkOverlay object is assigned to the Divider.</span></span> <span data-ttu-id="2e462-132">Zum Schluss ist das InkOverlay-Objekt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2e462-132">Finally, the InkOverlay object is enabled.</span></span>


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



<span data-ttu-id="2e462-133">Die [Striche](/previous-versions/ms839422(v=msdn.10)) -Auflistung des [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekts muss mit der [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung des [InkOverlay](/previous-versions/ms833057(v=msdn.10)) -Objekts synchron gehalten werden (der Zugriff erfolgt über die [Ink](/previous-versions/ms833110(v=msdn.10)) -Eigenschaft des InkOverlay-Objekts).</span><span class="sxs-lookup"><span data-stu-id="2e462-133">The [Divider](/previous-versions/ms839398(v=msdn.10)) object's [Strokes](/previous-versions/ms839422(v=msdn.10)) collection must be kept in sync with the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Strokes](/previous-versions/ms827799(v=msdn.10)) collection (accessed through the InkOverlay object's [Ink](/previous-versions/ms833110(v=msdn.10)) property).</span></span> <span data-ttu-id="2e462-134">Um sicherzustellen, dass dies geschieht, wird der [Stroke](/previous-versions/ms835344(v=msdn.10)) -Ereignishandler für das InkOverlay-Objekt wie folgt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2e462-134">To ensure that this happens, the [Stroke](/previous-versions/ms835344(v=msdn.10)) event handler for the InkOverlay object is written as follows.</span></span> <span data-ttu-id="2e462-135">Beachten Sie, dass der Ereignishandler zuerst testet, ob [EditingMode](/previous-versions/ms833105(v=msdn.10)) auf **Ink** festgelegt ist, um radiererstriche herauszufiltern.</span><span class="sxs-lookup"><span data-stu-id="2e462-135">Note that the event handler first tests to see if the [EditingMode](/previous-versions/ms833105(v=msdn.10)) is set to **Ink** to filter out eraser strokes.</span></span> <span data-ttu-id="2e462-136">Wenn der Benutzer eine automatische Layoutanalyse angefordert hat, ruft die Anwendung die divideink-Methode des Formulars auf und aktualisiert den Zeichnungs Bereich.</span><span class="sxs-lookup"><span data-stu-id="2e462-136">If the user has requested automatic layout analysis, then the application calls the form's DivideInk method and refreshes the drawing area.</span></span>


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



## <a name="dividing-the-ink"></a><span data-ttu-id="2e462-137">Aufteilen der frei Hand Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e462-137">Dividing the Ink</span></span>

<span data-ttu-id="2e462-138">Wenn der Benutzer im Menü Datei auf aufteilen klickt, wird die [Divide](/previous-versions/ms839461(v=msdn.10)) -Methode für das [Divider](/previous-versions/ms839398(v=msdn.10)) -Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2e462-138">When the user clicks Divide on the File menu, the [Divide](/previous-versions/ms839461(v=msdn.10)) method is called on the [Divider](/previous-versions/ms839398(v=msdn.10)) object.</span></span> <span data-ttu-id="2e462-139">Die Standard Erkennung wird verwendet, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2e462-139">The default recognizer is used, if available.</span></span>


```C++
DivisionResult divResult = myInkDivider.Divide();
```



<span data-ttu-id="2e462-140">Das resultierende [DivisionResult](/previous-versions/ms839371(v=msdn.10)) -Objekt, auf das von der-Variable verwiesen wird, `divResult` wird an eine Utility-Funktion,, übergeben `getUnitBBBoxes()` .</span><span class="sxs-lookup"><span data-stu-id="2e462-140">The resulting [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object, referenced by the variable `divResult`, is passed to a utility function, `getUnitBBBoxes()`.</span></span> <span data-ttu-id="2e462-141">Die Utility-Funktion gibt ein Array von Rechtecke für alle angeforderten Divisions Typen zurück: Segmente, Linien, Absätze oder Zeichnungen.</span><span class="sxs-lookup"><span data-stu-id="2e462-141">The utility function returns an array of rectangles for whatever division type is requested: segments, lines, paragraphs, or drawings.</span></span>


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



<span data-ttu-id="2e462-142">Schließlich muss der Formular Bereich neu gezeichnet werden, damit die umgebenden Rechtecke angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2e462-142">Finally, the form panel is forced to redraw so that the bounding rectangles appear.</span></span>


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a><span data-ttu-id="2e462-143">Ergebnisse der frei Hand Analyse</span><span class="sxs-lookup"><span data-stu-id="2e462-143">Ink Analysis Results</span></span>

<span data-ttu-id="2e462-144">In der Utility-Funktion wird das [DivisionResult](/previous-versions/ms839371(v=msdn.10)) -Objekt mithilfe der Methode [ResultByType](/previous-versions/ms839388(v=msdn.10)) auf Grundlage des vom Aufrufer angeforderten Divisions Typs abgefragt.</span><span class="sxs-lookup"><span data-stu-id="2e462-144">In the utility function, the [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object is queried for its results by using the [ResultByType](/previous-versions/ms839388(v=msdn.10)) method, based on the division type requested by the caller.</span></span> <span data-ttu-id="2e462-145">Die ResultByType-Methode gibt eine [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) -Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="2e462-145">The ResultByType method returns a [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) collection.</span></span> <span data-ttu-id="2e462-146">Jede [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in der Auflistung stellt eine Zeichnung, ein einzelnes Erkennungs Segment der Handschrift, eine Handschrift Zeile oder einen Hand schriftblock dar, je nachdem, was beim Aufrufen der Hilfsprogrammfunktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2e462-146">Each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in the collection represents a drawing, a single recognition segment of handwriting, a line of handwriting, or a block of handwriting, depending upon what was specified when the utility function was called.</span></span>


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



<span data-ttu-id="2e462-147">Wenn mindestens eine [DivisionUnit](/previous-versions/ms837976(v=msdn.10))vorhanden ist, wird ein Array mit Rechtecke erstellt, das ein umschließendes Rechteck pro Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="2e462-147">If there is at least one [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), an array of rectangles is created containing one bounding rectangle per unit.</span></span> <span data-ttu-id="2e462-148">(Die Rechtecke werden durch unterschiedliche Beträge für jeden Typ von Einheit aufgeblasen, der in der Vergrößerung-Variablen enthalten ist, um Überschneidungen zu vermeiden.)</span><span class="sxs-lookup"><span data-stu-id="2e462-148">(The rectangles are inflated by differing amounts for each type of unit, held in the inflate variable, to prevent overlapping.)</span></span>


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



## <a name="redrawing-the-form"></a><span data-ttu-id="2e462-149">Das Formular wird neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2e462-149">Redrawing the Form</span></span>

<span data-ttu-id="2e462-150">Wenn das Neuzeichnen überschritten wird, wird der folgende Code ausgeführt, um die umgebenden Felder für jede [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) im Formular um das frei Handzeichen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="2e462-150">When the redraw is forced above, the following code executes to paint the bounding boxes for each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) on the form around the ink.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="2e462-151">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="2e462-151">Closing the Form</span></span>

<span data-ttu-id="2e462-152">Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) löscht die Objekte [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [erkenzercontext](/previous-versions/ms828542(v=msdn.10)) und die im Beispiel verwendete [Striche](/previous-versions/ms827799(v=msdn.10)) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="2e462-152">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) objects and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection used in the sample.</span></span>

 

