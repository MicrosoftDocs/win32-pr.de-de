---
description: Das Beispiel für die einfache Ink-Analyse zeigt, wie die InkAnalyzer-Klasse frei Hand Eingaben in verschiedene Wort-und Zeichnungs Segmente unterteilt Bei diesem Beispiel handelt es sich um eine aktualisierte Version des frei Hand Teiler-Beispiels.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Beispiel für grundlegende Ink-Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94ac73ca9049169c6e406059665a66e8eaa6f3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342635"
---
# <a name="basic-ink-analysis-sample"></a><span data-ttu-id="5969f-103">Beispiel für grundlegende Ink-Analyse</span><span class="sxs-lookup"><span data-stu-id="5969f-103">Basic Ink Analysis Sample</span></span>

<span data-ttu-id="5969f-104">Das Beispiel für die einfache Ink-Analyse zeigt, wie die [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Klasse frei Hand Eingaben in verschiedene Wort-und Zeichnungs Segmente unterteilt</span><span class="sxs-lookup"><span data-stu-id="5969f-104">The Basic Ink Analysis sample shows how the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class divides ink into various word and drawing segments.</span></span>

<span data-ttu-id="5969f-105">Bei diesem Beispiel handelt es sich um eine aktualisierte Version des frei Hand [Teiler](ink-divider-sample.md)-Beispiels.</span><span class="sxs-lookup"><span data-stu-id="5969f-105">This sample is an updated version of the [Ink Divider Sample](ink-divider-sample.md).</span></span> <span data-ttu-id="5969f-106">Während das frei Hand Trennzeichen die [Divider](/previous-versions/ms839398(v=msdn.10)) -Klasse verwendet, wird in diesem Beispiel die neuere und bevorzugte InkAnalysis-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="5969f-106">Whereas the Ink Divider Sample uses the [Divider](/previous-versions/ms839398(v=msdn.10)) class, this sample uses the newer and preferred InkAnalysis API.</span></span> <span data-ttu-id="5969f-107">Die InkAnalysis-API kombiniert den [Erkennungs Kontext](/previous-versions/ms828542(v=msdn.10)) und den unter Teiler zu einer API und erweitert die Funktionalität beider Funktionen.</span><span class="sxs-lookup"><span data-stu-id="5969f-107">The InkAnalysis API combines the [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) and Divider into one API and expands on the functionality of both.</span></span>

<span data-ttu-id="5969f-108">Wenn Sie das Formular aktualisieren, zeichnet das Beispiel ein Rechteck um alle analysierten Einheiten: Wörter, Zeilen, Absätze, Schreib Bereiche, Zeichnungen und Aufzählungen.</span><span class="sxs-lookup"><span data-stu-id="5969f-108">When you update the form, the sample draws a rectangle around each analyzed unit: words, lines, paragraphs, writing regions, drawings and bullets.</span></span> <span data-ttu-id="5969f-109">Das Formular verwendet unterschiedliche Farben für die verschiedenen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="5969f-109">The form uses different colors for the different units.</span></span> <span data-ttu-id="5969f-110">Die Rechtecke werden ebenfalls durch unterschiedliche Beträge vergrößert, um sicherzustellen, dass kein Rechteck von anderen verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="5969f-110">The rectangles are also enlarged by different amounts to ensure that no one rectangle is obscured by any others.</span></span>

<span data-ttu-id="5969f-111">In der folgenden Tabelle werden die Farbe und die Vergrößerung der einzelnen analysierten Einheiten angegeben.</span><span class="sxs-lookup"><span data-stu-id="5969f-111">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="5969f-112">Analysierte Einheit</span><span class="sxs-lookup"><span data-stu-id="5969f-112">Analyzed unit</span></span>             | <span data-ttu-id="5969f-113">Farbe des Rechtecks</span><span class="sxs-lookup"><span data-stu-id="5969f-113">Color of rectangle</span></span> | <span data-ttu-id="5969f-114">Rechteck Vergrößerung (Pixel)</span><span class="sxs-lookup"><span data-stu-id="5969f-114">Rectangle enlargement (pixels)</span></span> |
|---------------------------|--------------------|--------------------------------|
| <span data-ttu-id="5969f-115">Word</span><span class="sxs-lookup"><span data-stu-id="5969f-115">Word</span></span><br/>           | <span data-ttu-id="5969f-116">Grün</span><span class="sxs-lookup"><span data-stu-id="5969f-116">Green</span></span><br/>   | <span data-ttu-id="5969f-117">1</span><span class="sxs-lookup"><span data-stu-id="5969f-117">1</span></span><br/>                   |
| <span data-ttu-id="5969f-118">Zeile</span><span class="sxs-lookup"><span data-stu-id="5969f-118">Line</span></span><br/>           | <span data-ttu-id="5969f-119">Magenta</span><span class="sxs-lookup"><span data-stu-id="5969f-119">Magenta</span></span><br/> | <span data-ttu-id="5969f-120">3</span><span class="sxs-lookup"><span data-stu-id="5969f-120">3</span></span><br/>                   |
| <span data-ttu-id="5969f-121">Paragraph</span><span class="sxs-lookup"><span data-stu-id="5969f-121">Paragraph</span></span><br/>      | <span data-ttu-id="5969f-122">Blau</span><span class="sxs-lookup"><span data-stu-id="5969f-122">Blue</span></span><br/>    | <span data-ttu-id="5969f-123">5</span><span class="sxs-lookup"><span data-stu-id="5969f-123">5</span></span><br/>                   |
| <span data-ttu-id="5969f-124">Bereich wird geschrieben</span><span class="sxs-lookup"><span data-stu-id="5969f-124">Writing region</span></span><br/> | <span data-ttu-id="5969f-125">Gelb</span><span class="sxs-lookup"><span data-stu-id="5969f-125">Yellow</span></span><br/>  | <span data-ttu-id="5969f-126">7</span><span class="sxs-lookup"><span data-stu-id="5969f-126">7</span></span><br/>                   |
| <span data-ttu-id="5969f-127">Zeichnung</span><span class="sxs-lookup"><span data-stu-id="5969f-127">Drawing</span></span><br/>        | <span data-ttu-id="5969f-128">Red</span><span class="sxs-lookup"><span data-stu-id="5969f-128">Red</span></span><br/>     | <span data-ttu-id="5969f-129">1</span><span class="sxs-lookup"><span data-stu-id="5969f-129">1</span></span><br/>                   |
| <span data-ttu-id="5969f-130">Streif</span><span class="sxs-lookup"><span data-stu-id="5969f-130">Bullet</span></span><br/>         | <span data-ttu-id="5969f-131">Orange</span><span class="sxs-lookup"><span data-stu-id="5969f-131">Orange</span></span><br/>  | <span data-ttu-id="5969f-132">1</span><span class="sxs-lookup"><span data-stu-id="5969f-132">1</span></span><br/>                   |



 

<span data-ttu-id="5969f-133">Sie können Striche im Formular löschen.</span><span class="sxs-lookup"><span data-stu-id="5969f-133">You can erase strokes in the form.</span></span> <span data-ttu-id="5969f-134">In der Beispielanwendung können Sie zwischen den Freihand-und den Lösch Modus wechseln, um die Funktion des Stifts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5969f-134">In the sample application, you can toggle between Ink and Erase mode to change the function of the pen.</span></span>


```C++
        private void miInk_Click(object sender, System.EventArgs e)
        {
            // Turn on the inking mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Ink;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = true;
            miErase.Checked = false;

            // Update the UI
            this.Refresh();
        }

        private void miErase_Click(object sender, System.EventArgs e)
        {
            // Turn on the ink deletion mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Delete;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = false;
            miErase.Checked = true;

            // Update the UI
            this.Refresh();
        }
```



<span data-ttu-id="5969f-135">Wenn Sie Striche hinzufügen oder löschen, aktualisiert die Beispiele den [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="5969f-135">When you add or delete strokes, the samples updates the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span></span>


```C++
        private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
        {
            // Filter out the eraser stroke.
            if (InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
            {

                // Add the new stroke to the InkAnalyzer's stroke collection
                myInkAnalyzer.AddStroke(e.Stroke);

                if (miAutomaticLayoutAnalysis.Checked)
                {
                    // Invoke an analysis operation on the background thread
                    myInkAnalyzer.BackgroundAnalyze();
                }
            }
        }

        void myInkOverlay_StrokeDeleting(object sender, InkOverlayStrokesDeletingEventArgs e)
        {
            // Remove the strokes to be deleted from the InkAnalyzer's stroke collection
            myInkAnalyzer.RemoveStrokes(e.StrokesToDelete);

            // If automatic layout analysis is turned on, analyze the ink on the background thread
            if ( miAutomaticLayoutAnalysis.Checked )
            {
                // Invoke an analysis operation on the background thread
                myInkAnalyzer.BackgroundAnalyze ( );
            }
        }
```



<span data-ttu-id="5969f-136">Beachten Sie, dass im Menü Modus die automatische Layoutanalyse standardmäßig aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5969f-136">Notice that in the Mode menu, Automatic Layout Analysis is on by default.</span></span> <span data-ttu-id="5969f-137">Wenn diese Option ausgewählt ist, [wird der](/previous-versions/ms833057(v=msdn.10)) [Stroke](/previous-versions/ms835344(v=msdn.10)) -Ereignishandler und der [strokeslösch](/previous-versions/ms835360(v=msdn.10)) -Ereignishandler die [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) -Methode jedes Mal aufgerufen, wenn ein Strich erstellt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="5969f-137">With this option selected, the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Stroke](/previous-versions/ms835344(v=msdn.10)) and [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) event handlers call the [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method every time a stroke is created or deleted.</span></span>

> [!Note]  
> <span data-ttu-id="5969f-138">Wenn die [Analyse](/previous-versions/ms568971(v=vs.100)) Methode des [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Objekts mit mehr als wenigen Strichen aufgerufen wird, wird eine merkliche Verzögerung in einer Anwendung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="5969f-138">Calling the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object's [Analyze](/previous-versions/ms568971(v=vs.100)) method with more than a few strokes present creates a noticeable delay in an application.</span></span> <span data-ttu-id="5969f-139">Der Grund hierfür ist, dass "analysieren" eine synchrone Handschrift Analyse ist</span><span class="sxs-lookup"><span data-stu-id="5969f-139">This is because Analyze is a synchronous ink analysis operation.</span></span> <span data-ttu-id="5969f-140">In der Praxis wird die Analysemethode nur aufgerufen, wenn Sie das Ergebnis benötigen.</span><span class="sxs-lookup"><span data-stu-id="5969f-140">In practice, call the Analyze method only when you need the result.</span></span> <span data-ttu-id="5969f-141">Andernfalls verwenden Sie die asynchrone [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) -Methode, wie im Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5969f-141">Otherwise use the asynchronous [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method, as shown in the sample.</span></span>

 

## <a name="handling-the-analysis-results"></a><span data-ttu-id="5969f-142">Verarbeiten der Analyseergebnisse</span><span class="sxs-lookup"><span data-stu-id="5969f-142">Handling the Analysis Results</span></span>

<span data-ttu-id="5969f-143">Im Beispiel werden zwei Arrays erstellt, die die verschiedenen Rechtecke enthalten, entweder horizontal oder gedreht.</span><span class="sxs-lookup"><span data-stu-id="5969f-143">The sample creates two arrays to hold the various rectangles, either horizontal or rotated.</span></span> <span data-ttu-id="5969f-144">Verwenden Sie ein gedrehtes Begrenzungsfeld, um den Winkel zu erhalten, in dem eine Zeile von Wörtern geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5969f-144">Use a rotated bounding box to get the angle on which a line of words is written.</span></span> <span data-ttu-id="5969f-145">Das Beispiel zeigt die Eigenschaften, die vom [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) zurückgegeben werden, und zeigt das umgebende Feld oder das gedrehte umgebende Feld an (abhängig von der Menü Auswahl).</span><span class="sxs-lookup"><span data-stu-id="5969f-145">The sample shows the properties returned by the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) and displays the bounding box or the rotated bounding box (depending on the menu selection).</span></span>


```C++
      private Rectangle[] GetHorizontalBBoxes(Guid nodeType, int inflate)
        {
            // Declare the array of rectangles to hold the result
            Rectangle[] analysisRects;

            // Get the division units from the division result of division type
            ContextNodeCollection nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // If there is at least one unit, we construct the rectangles
            if ((null != nodes) && (0 < nodes.Count))
            {
                // We need to convert rectangles from ink units to
                // pixel units. For that, we need Graphics object
                // to pass to InkRenderer.InkSpaceToPixel method
                using (Graphics g = drawArea.CreateGraphics())
                {
                    // Construct the rectangles
                    analysisRects = new Rectangle[nodes.Count];

                    // InkRenderer.InkSpaceToPixel takes Point as parameter. 
                    // Create two Point objects to point to (Top, Left) and
                    // (Width, Height) properties of rectangle. (Width, Height)
                    // is used instead of (Right, Bottom) because (Right, Bottom)
                    // are read-only properties on Rectangle
                    Point ptLocation = new Point();
                    Point ptSize = new Point();

                    // Index into the bounding boxes
                    int i = 0;

                    // Iterate through the collection of division units to obtain the bounding boxes
                    foreach (ContextNode node in nodes)
                    {
                        // Get the bounding box of the strokes of the division unit
                        analysisRects[i] = node.Location.GetBounds();

                        // The bounding box is in ink space unit. Convert them into pixel unit. 
                        ptLocation = analysisRects[i].Location;
                        ptSize.X = analysisRects[i].Width;
                        ptSize.Y = analysisRects[i].Height;

                        // Convert the Location from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptLocation);

                        // Convert the Size from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptSize);

                        // Assign the result back to the corresponding properties
                        analysisRects[i].Location = ptLocation;
                        analysisRects[i].Width = ptSize.X;
                        analysisRects[i].Height = ptSize.Y;

                        // Inflate the rectangle by inflate pixels in both directions
                        analysisRects[i].Inflate(inflate, inflate);

                        // Increment the index
                        ++i;
                    }

                } // Relinquish the Graphics object
            }
            else
            {
                // Otherwise we return null
                analysisRects = null;
            }

            // Return the Rectangle[] object
            return analysisRects;
        }

        private System.Collections.ArrayList GetRotatedBBoxes(Guid nodeType, int inflate)
        {
            //Find the correct collection of results nodes.
            ContextNodeCollection Nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // Declare the array list to hold the results; 
            // This array represents the four points of a rectangle, with the first point
            // copied again to complete the cycle of points.

            ArrayList polygonPoints = new ArrayList(Nodes.Count);

            // Cycle through each results node, get and convert the
            // rotated bounding box points
            foreach (ContextNode node in Nodes)
            {
                //Declare the point array
                Point[] rotatedBoundingBox = null;

                //Switch on the type of ContextNode to cast into the
                //appropriate type.  This is required to access the 
                //type specific property "RotatedBoundingBox" which
                //is not found on all ContextNode types.
                if (nodeType == ContextNodeType.InkWord)
                {
                    rotatedBoundingBox = ((InkWordNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Line)
                {
                    rotatedBoundingBox = ((LineNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Paragraph)
                {
                    rotatedBoundingBox = ((ParagraphNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.WritingRegion ||
                         nodeType == ContextNodeType.InkDrawing ||
                         nodeType == ContextNodeType.InkBullet )
                {

                    // Rotated Bounding Boxes are not a supported option for 
                    // Writing Regions or Drawings.  We return the axis aligned 
                    // bounding box instead
                    Rectangle rect = node.Location.GetBounds();

                    // We need to create a looped list of 4 points to be consistent
                    // with the way InkAnalysis represents rotated bounding boxes.  
                    rotatedBoundingBox = new Point[4];

                    rotatedBoundingBox[0] = new Point(rect.X, rect.Y);
                    rotatedBoundingBox[1] = new Point(rect.Right, rect.Y);
                    rotatedBoundingBox[2] = new Point(rect.Right, rect.Bottom);
                    rotatedBoundingBox[3] = new Point(rect.X, rect.Bottom);

                }


                if (null != rotatedBoundingBox)
                {
                    // We need to convert rectangles from ink units to
                    // pixel units. For that, we need Graphics object
                    // to pass to InkRenderer.InkSpaceToPixel method
                    using (Graphics g = drawArea.CreateGraphics())
                    {
                        // convert each of the points from ink space to pixel space
                        for (int i = 0; i < rotatedBoundingBox.Length; i++)
                        {
                            myInkOverlay.Renderer.InkSpaceToPixel(g, ref rotatedBoundingBox[i]);
                        }

                        //inflate the points by calling helper method
                        InflateHelperMethod(ref rotatedBoundingBox, inflate);

                        // increment the node portion of the polygonPoints array
                        polygonPoints.Add(rotatedBoundingBox);
                    }
                }
            }
            //Return the results
            return polygonPoints;
        }
```



<span data-ttu-id="5969f-146">Der Parser berechnet [getrotatedboundingbox](/previous-versions/ms569544(v=vs.100)) während der Analyse.</span><span class="sxs-lookup"><span data-stu-id="5969f-146">The parser calculates [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) during analysis.</span></span> <span data-ttu-id="5969f-147">Sie können aus verschiedenen nützlichen Gründen auf die Informationen aus den gedrehten umgebenden Feldern in der Anwendung zugreifen:</span><span class="sxs-lookup"><span data-stu-id="5969f-147">You can access the information from the rotated bounding boxes in your application for a number of useful reasons:</span></span>

-   <span data-ttu-id="5969f-148">Erkennen oder zeichnen Sie die Begrenzungen einer einzelnen Zeile, eines Absatzes oder einer anderen Einheit.</span><span class="sxs-lookup"><span data-stu-id="5969f-148">Detect or draw the bounds of a single line, paragraph, or other unit.</span></span>
-   <span data-ttu-id="5969f-149">Bestimmen Sie den Winkel, in dem eine Zeile oder ein Absatz geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5969f-149">Determine the angle at which a line or paragraph is written.</span></span>
-   <span data-ttu-id="5969f-150">Implementieren Sie Funktionen wie die Auswahl für eine Zeile, einen Absatz oder eine andere Einheit.</span><span class="sxs-lookup"><span data-stu-id="5969f-150">Implement features such as selection for a line, paragraph, or other unit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5969f-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5969f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5969f-152">Grundlegende Erkennungs-und Handschrift Analyse</span><span class="sxs-lookup"><span data-stu-id="5969f-152">Basic Recognition and Ink Analysis</span></span>](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[<span data-ttu-id="5969f-153">Beispiel für gescannte Papier Form</span><span class="sxs-lookup"><span data-stu-id="5969f-153">Scanned Paper Form Sample</span></span>](scanned-paper-form-sample.md)
</dt> <dt>

[<span data-ttu-id="5969f-154">Ink-Divider-Beispiel</span><span class="sxs-lookup"><span data-stu-id="5969f-154">Ink Divider Sample</span></span>](ink-divider-sample.md)
</dt> </dl>

 

