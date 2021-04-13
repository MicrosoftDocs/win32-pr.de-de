---
description: Dieses Programm veranschaulicht, wie frei Hand Eingaben in eine andere Anwendung kopiert und eingefügt werden. Außerdem kann der Benutzer eine Auswahl von Strichen kopieren und das Ergebnis in das vorhandene Ink-Objekt einfügen.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Beispiel für frei Hand Ablage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525970"
---
# <a name="ink-clipboard-sample"></a>Beispiel für frei Hand Ablage

Dieses Programm veranschaulicht, wie frei Hand Eingaben in eine andere Anwendung kopiert und eingefügt werden. Außerdem kann der Benutzer eine Auswahl von Strichen kopieren und das Ergebnis in das vorhandene Ink-Objekt einfügen.

Die folgenden Zwischenablage Modi sind verfügbar:

-   Ink-serialisiertes Format (ISF)
-   Metadatei
-   Erweiterte Metadatei (Enhanced Metafile, EMF)
-   Bitmap
-   Text Freihand
-   Skizzen frei

Text Freihand-und Skizzen frei Hand Eingaben sind zwei Arten von frei Hand Steuerelementen, die als Text bzw. gezeichnet werden Es ist möglich, ISF, Text Freihand und Skizzen Freihand in vorhandene Freihand einzufügen.

Neben der Zwischenablage veranschaulicht dieses Beispiel auch, wie Striche mit dem Lassopfad-Tool ausgewählt werden. Der Benutzer kann ausgewählte Striche verschieben und seine Zeichnungs Attribute ändern. Diese Funktion ist eine Teilmenge der Auswahl Funktionen, die bereits vom Handschrift Steuerelement bereitgestellt werden. Sie wird hier zur Veranschaulichung implementiert.

In diesem Beispiel werden die folgenden Funktionen verwendet:

-   Das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt.
-   Unterstützung für frei Hand Zwischenablage
-   Die Verwendung von Lassopfad mit der [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) -Methode.

Dieses Beispiel veranschaulicht das Rendern von frei Hand Eingaben, das Kopieren der frei Hand Eingaben und das anschließende Einfügen der frei Hand Eingaben in eine andere Anwendung wie Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Sammeln von frei Hand Eingaben und Einrichten des Formulars

Verweisen Sie zunächst auf die Tablet PC Automation-Schnittstellen, die mit dem Microsoft Windows <entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK) installiert werden.


```C++
using Microsoft.Ink;
```



Im nächsten Schritt deklariert das Formular einige Konstanten und Felder, die später in diesem Beispiel notiert werden.


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



Schließlich wird das Formular im [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignishandler des Formulars initialisiert, ein [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt für das Formular erstellt und der frei Hand Sammler aktiviert.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Behandeln von Menü Ereignissen

Die Ereignishandler für Menü Elemente aktualisieren hauptsächlich den Status des Formulars.

Der Befehl CLEAR entfernt das Auswahl Rechteck und löscht die Striche aus dem [Ink](/previous-versions/ms583670(v=vs.100)) -Objekt des frei Hand Sammlers.

Der Exit-Befehl deaktiviert den Ink Collector, bevor die Anwendung beendet wird.

Im Menü bearbeiten können Sie die Befehle zum Ausschneiden und kopieren basierend auf dem Auswahl Zustand des Formulars aktivieren und den Befehl Einfügen basierend auf dem Inhalt der Zwischenablage aktivieren, der mithilfe der [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts festgelegt wurde.

Die Befehle zum Ausschneiden und kopieren verwenden beide eine Hilfsmethode, um frei Hand Eingaben in die Zwischenablage zu kopieren. Der Ausschneide Befehl verwendet eine Hilfsmethode, um die ausgewählten Striche zu löschen.

Der Befehl "Einfügen" prüft zunächst die [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts, um festzustellen, ob das Objekt in der Zwischenablage eingefügt werden kann. Der Befehl "Einfügen" berechnet dann die linke obere Ecke des Einfügebereichs, konvertiert die Koordinaten von Pixeln in frei Hand Raum und fügt die Striche aus der Zwischenablage in den frei Hand Sammler ein. Schließlich wird das Auswahlfeld aktualisiert.


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



Die SELECT-und Ink-Befehle aktualisieren den Anwendungsmodus und die Standard Zeichnungs Attribute, löschen die aktuelle Auswahl, aktualisieren den Menü Zustand und aktualisieren das Formular. Andere Handler greifen auf den Anwendungs Zustand zurück, um die richtige Funktion auszuführen, entweder das Auslagern oder das Ablegen von frei Hand Eingaben. Außerdem fügt der Befehl Select dem Ink Collector die [newcollector](/previous-versions/ms567621(v=vs.100)) -und [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignishandler hinzu, und der Ink-Befehl entfernt diese Ereignishandler aus dem Ink Collector.

Die Formate, die in der Zwischenablage verfügbar sind, wenn Striche kopiert werden, werden im Menü Format aufgelistet, und der Benutzer wählt das Format zum Kopieren der frei Hand Eingabe aus der Liste aus. Zu den verfügbaren Typen von Formaten gehören das frei Hand Format (Ink Serialized Format, ISF), Metadateien, Erweiterte Metadateien und Bitmap. Die Formatierungen von Skizzen Freihand und Text Freihand schließen sich gegenseitig aus und basieren darauf, dass die frei Hand Eingaben als OLE-Objekt in die Zwischenablage kopiert werden

Das Menü Format ermöglicht dem Benutzer das Ändern der Farb-und breiten Eigenschaften des Stifts und aller ausgewählten Striche.

Beispielsweise wird mit dem roten Befehl die [Color](/previous-versions/ms582103(v=vs.100)) -Eigenschaft der [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) -Eigenschaft des Ink Collector auf die Farbe Rot festgelegt. Da die [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) -Eigenschaft des [Cursor](/previous-versions/ms552104(v=vs.100)) Objekts nicht festgelegt wurde, erben alle neuen frei Hand Eingaben, die in den Ink Collector gezeichnet werden, auf die Standard Zeichenfarbe. Wenn derzeit eine beliebige Striche ausgewählt sind, wird auch die Farb Eigenschaft der Zeichnungs Attribute des Strichs ebenfalls aktualisiert.


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

Der [MouseMove](/previous-versions/ms567617(v=vs.100)) -Ereignishandler überprüft den Anwendungsmodus. Wenn der Modus moveink ist und eine Maustaste gedrückt ist, verschiebt der Handler die Striche mithilfe der Move-Methode der [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung und aktualisiert das Auswahlfeld. Andernfalls prüft der Handler, ob das Auswahl Rechteck den Cursor enthält, aktiviert die Ink-Auflistung entsprechend und legt den Cursor entsprechend fest.

Der [mousetdown](/previous-versions/ms567616(v=vs.100)) -Ereignishandler überprüft die Cursor Einstellung. Wenn der Cursor auf [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1)festgelegt ist, legt der Handler den Anwendungsmodus auf moveink fest und zeichnet die Cursorposition auf. Wenn eine aktuelle Auswahl vorliegt, löschen Sie Sie.

Der [MouseUp](/previous-versions/ms567618(v=vs.100)) -Ereignishandler überprüft den Anwendungsmodus. Wenn der Modus "moveink" ist, legt der Handler den Anwendungsmodus basierend auf dem aktivierten Zustand des Select-Befehls fest.

Das [newpacket](/previous-versions/ms567621(v=vs.100)) -Ereignis wird im Auswahlmodus ausgelöst, wenn der Ink Collector neue Paketdaten empfängt. Wenn sich die Anwendung im Auswahlmodus befindet, müssen die neuen Pakete abgefangen und zum Zeichnen der Auswahl-Lasso verwendet werden.

Die Koordinaten jedes Pakets werden in Pixel konvertiert, auf den Zeichenbereich beschränkt und der Auflistung von Punkten von Lasso hinzugefügt. Anschließend wird eine Hilfsmethode aufgerufen, um die Lassopfad im Formular zu zeichnen.

## <a name="handling-a-new-stroke"></a>Behandeln eines neuen Strichs

Das [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignis wird im Auswahlmodus ausgelöst, wenn ein neuer Strich gezeichnet wird. Wenn sich die Anwendung im Auswahlmodus befindet, entspricht dieser Strich dem Lassopfad, und es ist erforderlich, die Informationen zu den ausgewählten Strichen zu aktualisieren.

Der Handler bricht das [Stroke](/previous-versions/ms567622(v=vs.100)) -Ereignis ab, prüft auf mehr als zwei Lassopfad-Punkte, kopiert die Points-Auflistung in ein Array von [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) -Objekten und konvertiert die Koordinaten der Punkte im Array von Pixel in frei Hand Raum. Anschließend verwendet der Handler die [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts, um die von den Lassopfad-Punkten ausgewählten Striche zu erhalten und den Auswahl Zustand des Formulars zu aktualisieren. Schließlich wird der Strich, der das Ereignis ausgelöst hat, aus der Auflistung ausgewählter Striche entfernt, die Lassopfad Points-Auflistung wird geleert, und eine Hilfsmethode zeichnet das Auswahl Rechteck.


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



## <a name="copying-ink-to-the-clipboard"></a>Kopieren von Freihand in die Zwischenablage

Die Hilfsmethode copyinktoclipboard erstellt einen [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) -Wert, überprüft den Status des Menüs, um die Formate zu aktualisieren, die in die Zwischenablage eingefügt werden sollen, und verwendet die [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) -Methode des [Ink](/previous-versions/ms583670(v=vs.100)) -Objekts, um die Striche in die Zwischenablage zu kopieren.


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

Mit der setSelection-Hilfsmethode wird die protokollierte selectedStrokes-Methode aktualisiert. wenn die Auflistung **null** oder **leer** ist, wird das Auswahl Rechteck auf das leere Rechteck festgelegt. Wenn die ausgewählte [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistung nicht leer ist, führt die setSelection-Methode die folgenden Schritte aus:

-   Bestimmt das umgebende Rechteck mithilfe der [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) -Methode der Striche-Auflistung.
-   Konvertiert die Rechteck Koordinaten aus dem frei Handzeichen Bereich in Pixel.
-   Vergrößert das Rechteck, um zwischen ihm und den ausgewählten Strichen einen visuellen Bereich bereitzustellen.
-   Erstellt Auswahl Handles für das aktuelle Auswahlfeld.

Schließlich legt die setSelection-Methode die Sichtbarkeit der Auswahl Handles fest und legt die [AutoRedraw](/previous-versions/ms571706(v=vs.100)) -Eigenschaft des Ink Collector auf **false** fest, wenn Striche ausgewählt werden.


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



## <a name="drawing-the-lasso"></a>Zeichnen von Lasso

Der Lassopfad wird als eine Reihe von offenen Punkten gezeichnet, die dem Pfad des Lassopfad-Strichs und einer gestrichelten Verbindungslinie zwischen den beiden Enden folgen. Das [newpakete](/previous-versions/ms567621(v=vs.100)) -Ereignis wird ausgelöst, wenn das Lassopfad gezeichnet wird, und der Ereignishandler übergibt die Strich Informationen an die drawlasso-Methode.

Die drawlasso-Hilfsmethode entfernt zuerst die alte Verbindungslinie und durchläuft dann die Punkte im Strich. Dann berechnet drawlasso, wo die Punkte auf dem Strich platziert werden, und zeichnet Sie. Schließlich zeichnet er eine neue Connector-Linie.

## <a name="closing-the-form"></a>Schließen des Formulars

Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt myinkcollector frei.

 

 
