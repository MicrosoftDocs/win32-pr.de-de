---
description: In diesem Programm wird veranschaulicht, wie Sie Ink kopieren und in eine andere Anwendung einfügen. Außerdem kann der Benutzer eine Auswahl von Strichen kopieren und das Ergebnis in das vorhandene Ink-Objekt einfügen.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Beispiel für die Ink-Zwischenablage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aa8acdf785321dc01706d4a4de50e0a2673a31250edbfa4316a27aecd0ce3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032328"
---
# <a name="ink-clipboard-sample"></a>Beispiel für die Ink-Zwischenablage

In diesem Programm wird veranschaulicht, wie Sie Ink kopieren und in eine andere Anwendung einfügen. Außerdem kann der Benutzer eine Auswahl von Strichen kopieren und das Ergebnis in das vorhandene Ink-Objekt einfügen.

Die folgenden Zwischenablagemodi sind verfügbar:

-   Serialisiertes Ink-Format (ISF)
-   Metafile
-   Erweiterte Metadatei (Enhanced Metafile, EMF)
-   Bitmap
-   Text Ink
-   Sketch Ink

Text ink und sketch ink sind zwei Arten von Ink-Steuerelementen, die als Text oder Zeichnung verwendet werden. Es ist möglich, ISF, Text-Ink und Sketch-Ink in vorhandene Ink-Dateien einfüge.

Zusätzlich zur Zwischenablage veranschaulicht dieses Beispiel auch das Auswählen von Strichen mit dem lasso-Tool. Der Benutzer kann ausgewählte Striche verschieben und seine Zeichnungsattribute ändern. Diese Funktionalität ist eine Teilmenge der Auswahlfunktionalität, die bereits vom Steuerelement für die Ink-Überlagerung bereitgestellt wird. Sie wird hier zu Veranschaulichungszwecken implementiert.

In diesem Beispiel werden die folgenden Features verwendet:

-   Das [InkCollector-Objekt.](/previous-versions/ms583683(v=vs.100))
-   Unterstützung der Ink-Zwischenablage.
-   Die Verwendung des Lassos mit der [Microsoft.Ink.Ink.HitTest-Methode.](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90))

Dieses Beispiel veranschaulicht das Rendern von Ink, das Kopieren dieser Ink-Datei und das anschließende Kopieren der Ink-Datei in eine andere Anwendung, z. B. Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Sammeln von Ink und Einrichten des Formulars

Verweisen Sie zunächst auf die Tablet PC Automation-Schnittstellen, die mit dem Microsoft Windows <entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK) installiert sind.


```C++
using Microsoft.Ink;
```



Als Nächstes deklariert das Formular einige Konstanten und Felder, die später in diesem Beispiel notiert werden.


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



Schließlich wird im [Load-Ereignishandler](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) des Formulars das Formular initialisiert, ein [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100)) für das Formular erstellt und der Ink-Collector aktiviert.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Behandeln von Menüereignissen

Die Menüelement-Ereignishandler aktualisieren in erster Linie den Zustand des Formulars.

Der Clear-Befehl entfernt das Auswahlrechteck und löscht die Striche aus dem Freischaltobjekt des [Freischaltobjekts.](/previous-versions/ms583670(v=vs.100))

Der Befehl Exit deaktiviert den Ink Collector, bevor die Anwendung beendet wird.

Das Menü Bearbeiten aktiviert die Befehle Ausschneiden und Kopieren basierend auf dem Auswahlzustand des Formulars und aktiviert [](/previous-versions/ms583670(v=vs.100)) den Befehl Einfügen basierend auf dem Inhalt der Zwischenablage, der mithilfe der [CanPaste-Methode](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) des Freischaltobjekts bestimmt wird.

Die Befehle Ausschneiden und Kopieren verwenden beide eine Hilfsmethode, um Ink in die Zwischenablage zu kopieren. Der Befehl Cut verwendet eine Hilfsmethode, um die ausgewählten Striche zu löschen.

Der Befehl Einfügen überprüft zunächst die [CanPaste-Methode](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) des [Ink-Objekts,](/previous-versions/ms583670(v=vs.100)) um zu prüfen, ob das Objekt in der Zwischenablage eingefügt werden kann. Mit dem Befehl Einfügen wird dann die obere linke Ecke für den Einfügebereich berechnet, die Koordinaten von Pixeln in Freihandraum konvertiert und die Striche aus der Zwischenablage in den Freihandsammler eingefügt. Schließlich wird das Auswahlfeld aktualisiert.


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



Die Befehle Select und Ink aktualisieren den Anwendungsmodus und die Standardzeichnungsattribute, löschen die aktuelle Auswahl, aktualisieren den Menüzustand und aktualisieren das Formular. Andere Handler verlassen sich auf den Anwendungszustand, um die richtige Funktion durchzuführen, entweder beim Zuordnen oder beim Auflegen von Freit. Darüber hinaus fügt der Select-Befehl dem Ink-Collector die [NewPackets-](/previous-versions/ms567621(v=vs.100)) und [Stroke-Ereignishandler](/previous-versions/ms567622(v=vs.100)) hinzu, und der Ink-Befehl entfernt diese Ereignishandler aus dem Ink-Collector.

Die Formate, die beim Kopieren von Strichen in der Zwischenablage verfügbar sind, werden im Menü Format aufgeführt, und der Benutzer wählt das Format zum Kopieren der Freiart aus dieser Liste aus. Zu den verfügbaren Formattypen zählen serialisiertes Freihandformat (ISF), Metadatei, erweiterte Metadatei und Bitmap. Die Formate sketch ink und text ink schließen sich gegenseitig aus und verlassen sich darauf, dass die Ink als OLE-Objekt in die Zwischenablage kopiert wird.

Im Menü Stil kann der Benutzer die Farb- und Breiteneigenschaften des Stifts und aller ausgewählten Striche ändern.

Beispielsweise legt der Befehl Red die [Color-Eigenschaft](/previous-versions/ms582103(v=vs.100)) der [DefaultDrawingAttributes-Eigenschaft](/previous-versions/ms571711(v=vs.100)) des Ink-Collectors auf die Farbe Rot fest. Da die [DrawingAttributes-Eigenschaft](/previous-versions/ms581965(v=vs.100)) des [Cursor-Objekts](/previous-versions/ms552104(v=vs.100)) nicht festgelegt wurde, erbt jede neue in den Ink-Collector gezeichnete Ink-Farbe an die Standardzeichnungsfarbe. Wenn derzeit Striche ausgewählt sind, werden auch die Farbeigenschaften der einzelnen Striche aktualisiert.


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a>Behandeln von Mausereignissen

Der [MouseMove-Ereignishandler](/previous-versions/ms567617(v=vs.100)) überprüft den Anwendungsmodus. Wenn der Modus MoveInk ist und eine Maustaste nach unten ist, verschiebt der Handler die Striche mithilfe der Move-Methode der [Strokes-Sammlung](/previous-versions/ms552701(v=vs.100)) und aktualisiert das Auswahlfeld. Andernfalls überprüft der Handler, ob das Auswahlrechteck den Cursor enthält, aktiviert die Ink-Auflistung entsprechend und legt den Cursor entsprechend fest.

Der [MouseDown-Ereignishandler](/previous-versions/ms567616(v=vs.100)) überprüft die Cursoreinstellung. Wenn der Cursor auf [SizeAll festgelegt ist,](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1)legt der Handler den Anwendungsmodus auf MoveInk fest und zeichnet die Cursorposition auf. Wenn eine aktuelle Auswahl vor liegt, löschen Sie sie andernfalls.

Der [MouseUp-Ereignishandler](/previous-versions/ms567618(v=vs.100)) überprüft den Anwendungsmodus. Wenn der Modus MoveInk ist, legt der Handler den Anwendungsmodus basierend auf dem aktivierten Zustand des Select-Befehls fest.

Das [NewPackets-Ereignis](/previous-versions/ms567621(v=vs.100)) wird im Auswahlmodus ausgelöst, wenn der Ink Collector neue Paketdaten empfängt. Wenn sich die Anwendung im Auswahlmodus befindet, müssen die neuen Pakete abgefangen und zum Zeichnen des Auswahl-Lassos verwendet werden.

Die Koordinate jedes Pakets wird in Pixel konvertiert, auf den Zeichnungsbereich beschränkt und der Auflistung von Punkten des Lassos hinzugefügt. Anschließend wird eine Hilfsmethode aufgerufen, um den Lasso im Formular zu zeichnen.

## <a name="handling-a-new-stroke"></a>Behandeln eines neuen Strichs

Das [Stroke-Ereignis](/previous-versions/ms567622(v=vs.100)) wird im Auswahlmodus ausgelöst, wenn ein neuer Strich gezeichnet wird. Wenn sich die Anwendung im Auswahlmodus befindet, entspricht dieser Strich dem Lasso, und es ist erforderlich, die Informationen der ausgewählten Striche zu aktualisieren.

Der Handler bricht das [Stroke-Ereignis](/previous-versions/ms567622(v=vs.100)) ab, sucht nach mehr als zwei Lassopunkten, kopiert die Points-Auflistung in ein Array von [Point-Objekten](/dotnet/api/system.drawing.point?view=netcore-3.1) und konvertiert die Koordinaten der Punkte im Array von Pixeln in Freiraum. Anschließend verwendet der Handler [](/previous-versions/ms583670(v=vs.100)) die [HitTest-Methode](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) des Freiformobjekts, um die von den Lassopunkten ausgewählten Striche zu erhalten und den Auswahlzustand des Formulars zu aktualisieren. Schließlich wird der Strich, der das Ereignis ausgelöst hat, aus der Auflistung der ausgewählten Striche entfernt, die lasso Points-Auflistung wird geleert, und eine Hilfsmethode zeichnet das Auswahlrechteck.


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a>Kopieren von Ink in die Zwischenablage

Die CopyInkToClipboard-Hilfsmethode erstellt einen [InkClipboardFormats-Wert,](/previous-versions/ms583681(v=vs.100)) überprüft den Status des Menüs Format, um die Formate zu aktualisieren, die in die Zwischenablage eingefügt werden sollen, und verwendet die [ClipboardCopy-Methode](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) des [Ink-Objekts,](/previous-versions/ms583670(v=vs.100)) um die Striche in die Zwischenablage zu kopieren.


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a>Aktualisieren einer Auswahl

Die SetSelection-Hilfsmethode aktualisiert das gespeicherte selectedStrokes-Element. Wenn die Auflistung **NULL** oder **EMPTY** ist, wird das Auswahlrechteck auf das leere Rechteck festgelegt. Wenn die ausgewählte [Strokes-Auflistung](/previous-versions/ms552701(v=vs.100)) nicht leer ist, führt die SetSelection-Methode die folgenden Schritte aus:

-   Bestimmt das umgebundene Rechteck mithilfe der [GetBoundingBox-Methode](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) der Strichsammlung.
-   Konvertiert die Rechteckkoordinaten aus dem Freiraum in Pixel.
-   Verflässige das Rechteck, um einen visuellen Raum zwischen ihm und den ausgewählten Strichen zu schaffen.
-   Erstellt Auswahlhandles für das aktuelle Auswahlfeld.

Schließlich legt die SetSelection-Methode die Sichtbarkeit der Auswahlhandles und die [AutoRedraw-Eigenschaft](/previous-versions/ms571706(v=vs.100)) des Ink-Collectors auf **FALSE** fest, wenn Striche ausgewählt sind.


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a>Zeichnen des Lasso

Der Lasso wird als eine Reihe von offenen Punkten gezeichnet, die dem Pfad des Lassostrichs und einer gestrichelten Konnektorlinie zwischen den beiden Enden folgen. Das [NewPackets-Ereignis](/previous-versions/ms567621(v=vs.100)) wird ausgelöst, während der Lasso gezeichnet wird, und der Ereignishandler übergibt die Strichinformationen an die DrawLasso-Methode.

Die DrawLasso-Hilfsmethode entfernt zuerst die alte Verbindungslinie und durch iteriert dann die Punkte im Strich. DrawLasso berechnet dann, wo die Punkte entlang des Strichs zu platzieren sind, und zeichnet sie. Schließlich wird eine neue Verbindungslinie ge zeichnet.

## <a name="closing-the-form"></a>Schließen des Formulars

Die Dispose-Methode [des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100)) myInkCollector zurück.

 

 
