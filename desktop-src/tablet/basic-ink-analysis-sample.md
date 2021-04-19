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
# <a name="basic-ink-analysis-sample"></a>Beispiel für grundlegende Ink-Analyse

Das Beispiel für die einfache Ink-Analyse zeigt, wie die [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Klasse frei Hand Eingaben in verschiedene Wort-und Zeichnungs Segmente unterteilt

Bei diesem Beispiel handelt es sich um eine aktualisierte Version des frei Hand [Teiler](ink-divider-sample.md)-Beispiels. Während das frei Hand Trennzeichen die [Divider](/previous-versions/ms839398(v=msdn.10)) -Klasse verwendet, wird in diesem Beispiel die neuere und bevorzugte InkAnalysis-API verwendet. Die InkAnalysis-API kombiniert den [Erkennungs Kontext](/previous-versions/ms828542(v=msdn.10)) und den unter Teiler zu einer API und erweitert die Funktionalität beider Funktionen.

Wenn Sie das Formular aktualisieren, zeichnet das Beispiel ein Rechteck um alle analysierten Einheiten: Wörter, Zeilen, Absätze, Schreib Bereiche, Zeichnungen und Aufzählungen. Das Formular verwendet unterschiedliche Farben für die verschiedenen Einheiten. Die Rechtecke werden ebenfalls durch unterschiedliche Beträge vergrößert, um sicherzustellen, dass kein Rechteck von anderen verdeckt wird.

In der folgenden Tabelle werden die Farbe und die Vergrößerung der einzelnen analysierten Einheiten angegeben.



| Analysierte Einheit             | Farbe des Rechtecks | Rechteck Vergrößerung (Pixel) |
|---------------------------|--------------------|--------------------------------|
| Word<br/>           | Grün<br/>   | 1<br/>                   |
| Zeile<br/>           | Magenta<br/> | 3<br/>                   |
| Paragraph<br/>      | Blau<br/>    | 5<br/>                   |
| Bereich wird geschrieben<br/> | Gelb<br/>  | 7<br/>                   |
| Zeichnung<br/>        | Red<br/>     | 1<br/>                   |
| Streif<br/>         | Orange<br/>  | 1<br/>                   |



 

Sie können Striche im Formular löschen. In der Beispielanwendung können Sie zwischen den Freihand-und den Lösch Modus wechseln, um die Funktion des Stifts zu ändern.


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



Wenn Sie Striche hinzufügen oder löschen, aktualisiert die Beispiele den [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).


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



Beachten Sie, dass im Menü Modus die automatische Layoutanalyse standardmäßig aktiviert ist. Wenn diese Option ausgewählt ist, [wird der](/previous-versions/ms833057(v=msdn.10)) [Stroke](/previous-versions/ms835344(v=msdn.10)) -Ereignishandler und der [strokeslösch](/previous-versions/ms835360(v=msdn.10)) -Ereignishandler die [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) -Methode jedes Mal aufgerufen, wenn ein Strich erstellt oder gelöscht wird.

> [!Note]  
> Wenn die [Analyse](/previous-versions/ms568971(v=vs.100)) Methode des [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) -Objekts mit mehr als wenigen Strichen aufgerufen wird, wird eine merkliche Verzögerung in einer Anwendung erzeugt. Der Grund hierfür ist, dass "analysieren" eine synchrone Handschrift Analyse ist In der Praxis wird die Analysemethode nur aufgerufen, wenn Sie das Ergebnis benötigen. Andernfalls verwenden Sie die asynchrone [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) -Methode, wie im Beispiel gezeigt.

 

## <a name="handling-the-analysis-results"></a>Verarbeiten der Analyseergebnisse

Im Beispiel werden zwei Arrays erstellt, die die verschiedenen Rechtecke enthalten, entweder horizontal oder gedreht. Verwenden Sie ein gedrehtes Begrenzungsfeld, um den Winkel zu erhalten, in dem eine Zeile von Wörtern geschrieben wird. Das Beispiel zeigt die Eigenschaften, die vom [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) zurückgegeben werden, und zeigt das umgebende Feld oder das gedrehte umgebende Feld an (abhängig von der Menü Auswahl).


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



Der Parser berechnet [getrotatedboundingbox](/previous-versions/ms569544(v=vs.100)) während der Analyse. Sie können aus verschiedenen nützlichen Gründen auf die Informationen aus den gedrehten umgebenden Feldern in der Anwendung zugreifen:

-   Erkennen oder zeichnen Sie die Begrenzungen einer einzelnen Zeile, eines Absatzes oder einer anderen Einheit.
-   Bestimmen Sie den Winkel, in dem eine Zeile oder ein Absatz geschrieben wird.
-   Implementieren Sie Funktionen wie die Auswahl für eine Zeile, einen Absatz oder eine andere Einheit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Erkennungs-und Handschrift Analyse](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[Beispiel für gescannte Papier Form](scanned-paper-form-sample.md)
</dt> <dt>

[Ink-Divider-Beispiel](ink-divider-sample.md)
</dt> </dl>

 

