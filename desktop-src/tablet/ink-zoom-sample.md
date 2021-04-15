---
description: In diesem Beispielprogramm wird veranschaulicht, wie frei Hand Eingaben vergrößert und angezeigt werden.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Ink Zoom-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525286"
---
# <a name="ink-zoom-sample"></a>Ink Zoom-Beispiel

In diesem Beispielprogramm wird veranschaulicht, wie frei Hand Eingaben vergrößert und angezeigt werden. Insbesondere ermöglicht der Benutzer das Vergrößern und Verkleinern von frei Hand Eingaben in Inkrementen. Außerdem wird veranschaulicht, wie Sie mithilfe eines Zoom Rechtecks in eine bestimmte Region zoomen. Schließlich wird in diesem Beispiel veranschaulicht, wie frei Hand Eingaben mit unterschiedlichen Zoom Verhältnissen gesammelt werden und wie der Bildlauf innerhalb des gezogenen Zeichnungs Bereichs eingerichtet wird.

Im Beispiel werden die Ansichts-und Objekt Transformationen des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) verwendet, um Zoom und Bildlauf auszuführen. Die Ansichts Transformation gilt für die Punkte und die Stift Breite. Die Objekt Transformation gilt nur für Punkte. Der Benutzer kann steuern, welche Transformation verwendet wird, indem er im Menü Modus die Breite für das Pen-Breite-Element ändert.

> [!Note]  
> Es ist problematisch, einige com-Aufrufe für bestimmte Schnittstellen Methoden auszuführen (z. b.[**inkrenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) und [**inkrenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)), wenn eine Nachricht gesendet wurde. Wenn Nachrichten gesendet werden, müssen Sie in die Warteschlange Nachrichten gemarshallt werden. Um dieses Szenario zu beheben, testen Sie, ob Sie eine Nachricht von Post verarbeiten, indem Sie [**insendmesssageex**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) aufrufen und die Nachricht an Sie senden, wenn die Nachricht gesendet wurde.

 

In diesem Beispiel werden die folgenden Funktionen verwendet:

-   Das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt
-   Die [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) -Methode des [Renderer](/previous-versions/ms828481(v=msdn.10)) -Objekts
-   Die [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) .

## <a name="initializing-the-form"></a>Initialisieren des Formulars

Zunächst wird im Beispiel auf die Tablet PC-Automatisierungs Schnittstellen verwiesen, die im Windows Vista-oder Windows XP Tablet PC Edition Software Development Kit (SDK) bereitgestellt werden.


```C++
using Microsoft.Ink;
```



Das Beispiel deklariert einen [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` und einige private Member, um die Skalierung zu unterstützen.


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



Anschließend [wird im Beispiel](/previous-versions/ms583683(v=vs.100)) der [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignishandler des Formulars erstellt und aktiviert. Außerdem wird die [Width](/previous-versions/ms837941(v=msdn.10)) -Eigenschaft der [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des InkCollector-Objekts festgelegt. Schließlich werden die Schiebe leisten Bereiche definiert, und die-Methode der Anwendung `UpdateZoomAndScroll` wird aufgerufen.


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a>Aktualisieren von Zoom-und Bild Lauf Werten

Der Zeichenbereich des frei Hand Sammlers ist von vielen Ereignissen betroffen. In der- `UpdateZoomAndScroll` Methode wird eine Transformationsmatrix verwendet, um den frei Hand Sammler innerhalb des Fensters zu skalieren und zu übersetzen.

> [!Note]  
> Die [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) wendet die Transformation auf die Striche und die Stift Breite an, während die [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) -Methode nur die Transformation auf die Striche anwendet.

 

Schließlich wird die-Methode der Anwendung `UpdateScrollBars` aufgerufen, und das Formular wird zum Aktualisieren gezwungen.


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a>Verwalten der Scrollleisten

Die-Methode richtet die Bild Lauf leisten so ein, dass Sie `UpdateScrollBars` ordnungsgemäß mit der aktuellen Fenstergröße, der Zoomeinstellung und der Scrollposition innerhalb von [InkCollector](/previous-versions/ms583683(v=vs.100))funktionieren. Diese Methode berechnet die großen Änderungen und kleinen Änderungs Werte für die vertikalen und horizontalen Scrollleisten. Außerdem wird der aktuelle Wert der Scrollleisten berechnet und ob Sie sichtbar sein sollten. Die [Pixel toinkspace](/previous-versions/ms828505(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) behandelt die Konvertierung von Pixeln in den Zoom-Koordinaten Bereich und die Konten für die Skalierung und den Bildlauf, die durch die Ansichts-und Objekt Transformationen angewendet werden.


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a>Zoomen zu einem Rechteck

Der `pnlDrawingArea` Panel-Ereignishandler verwaltet das Zeichnen des Rechtecks in das Fenster. Wenn der Befehl Zoom to Rect im Menü Modus aktiviert ist, ruft der [MouseUp](/previous-versions/ms567618(v=vs.100)) -Ereignishandler die-Methode der Anwendung auf `ZoomToRectangle` . Die `ZoomToRectangle` -Methode berechnet die Breite und Höhe des Rechtecks, prüft auf begrenzungsbedingungen, aktualisiert die ScrollBar-Werte und den Skalierungsfaktor und ruft dann die-Methode der Anwendung `UpdateZoomAndScroll` auf, um die neuen Einstellungen anzuwenden.

## <a name="closing-the-form"></a>Schließen des Formulars

Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt frei.

 

 
