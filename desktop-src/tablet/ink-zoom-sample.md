---
description: Dieses Beispielprogramm veranschaulicht das Zoomen und Scrollen von Ink.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Zoombeispiel für Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d786fe502e1510a44df39049e845f05694a1befae0d4a21bcfa2ba2bd2b19b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939440"
---
# <a name="ink-zoom-sample"></a>Zoombeispiel für Ink

Dieses Beispielprogramm veranschaulicht das Zoomen und Scrollen von Ink. Insbesondere ermöglicht es dem Benutzer, die Ink-Funktion in Schritten zu vergrößern und zu verkleinern. Außerdem wird veranschaulicht, wie sie mithilfe eines Zoomrechtecks in einen bestimmten Bereich zoomen. Schließlich wird in diesem Beispiel veranschaulicht, wie Sie Ink mit unterschiedlichen Zoomverhältnis erfassen und das Scrollen innerhalb des vergrößerten Zeichnungsbereichs einrichten.

Im Beispiel werden die Ansichts- und Objekttransformationen des [Rendererobjekts](/previous-versions/ms828481(v=msdn.10)) zum Zoomen und Scrollen verwendet. Die Ansichtstransformation gilt für die Punkte und die Stiftbreite. Die Objekttransformation gilt nur für die Punkte. Der Benutzer kann steuern, welche Transformation verwendet wird, indem er das Element Skalierungsstiftbreite im Menü Modus ändert.

> [!Note]  
> Es ist problematisch, einige COM-Aufrufe für bestimmte Schnittstellenmethoden (z. B.[**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) und [**InkRenderer.SetObjectTransform)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)durchzuführen, wenn eine Nachricht gesendet wurde. Wenn Nachrichten GESENDET werden, müssen sie in die POST-Nachrichtenwarteschlange ge marshallt werden. Um dieses Szenario zu behandeln, testen Sie, ob Sie eine Nachricht von POST behandeln, indem Sie [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) aufrufen und die Nachricht an sich selbst senden, wenn die Nachricht GESENDET wurde.

 

In diesem Beispiel werden die folgenden Features verwendet:

-   Das [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100))
-   Die [SetViewTransform-Methode des Rendererobjekts](/previous-versions/ms828514(v=msdn.10)) [](/previous-versions/ms828481(v=msdn.10))
-   Die [SetObjectTransform-Methode des Rendererobjekts](/previous-versions/ms828513(v=msdn.10)) [](/previous-versions/ms828481(v=msdn.10))

## <a name="initializing-the-form"></a>Initialisieren des Formulars

Zunächst verweist das Beispiel auf die Benutzeroberflächen der Tablet PC-Automatisierung, die im Windows Vista oder Windows XP Tablet PC Edition Software Development Kit (SDK) bereitgestellt werden.


```C++
using Microsoft.Ink;
```



Im Beispiel werden ein [InkCollector,](/previous-versions/ms583683(v=vs.100))und einige private Member deklariert, um `myInkCollector` die Skalierung zu unterstützen.


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



Anschließend erstellt und aktiviert das Beispiel den [InkCollector](/previous-versions/ms583683(v=vs.100)) im [Load-Ereignishandler des](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Formulars. Außerdem wird die [Width-Eigenschaft](/previous-versions/ms837941(v=msdn.10)) der [DefaultDrawingAttributes-Eigenschaft des InkCollector-Objekts](/previous-versions/ms836500(v=msdn.10)) festgelegt. Schließlich werden die Scrollleistenbereiche definiert und die `UpdateZoomAndScroll` -Methode der Anwendung aufgerufen.


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



## <a name="updating-the-zoom-and-scroll-values"></a>Aktualisieren der Zoom- und Bildlaufwerte

Der Zeichnungsbereich des Ink-Collectors wird von vielen Ereignissen beeinflusst. In der -Methode wird eine Transformationsmatrix verwendet, um den Ink-Collector innerhalb des Fensters zu skalieren `UpdateZoomAndScroll` und zu übersetzen.

> [!Note]  
> Die [SetViewTransform-Methode](/previous-versions/ms828514(v=msdn.10)) des [Rendererobjekts](/previous-versions/ms828481(v=msdn.10)) wendet die Transformation sowohl auf die Striche als auch auf die Stiftbreite an, während die [SetObjectTransform-Methode](/previous-versions/ms828513(v=msdn.10)) die Transformation nur auf die Striche angewendet.

 

Schließlich wird die -Methode `UpdateScrollBars` der Anwendung aufgerufen, und das Formular wird aktualisiert.


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

Die -Methode richtet die Scrollleisten so ein, dass sie ordnungsgemäß mit der aktuellen Fenstergröße, Zoomeinstellung und Bildlaufposition im `UpdateScrollBars` [InkCollector funktionieren.](/previous-versions/ms583683(v=vs.100)) Diese Methode berechnet die werte für große änderungen und kleine Änderungen für die vertikalen und horizontalen Scrollleisten. Außerdem wird der aktuelle Wert der Scrollleisten berechnet und ob sie sichtbar sein sollen. Die [PixelToInkSpace-Methode](/previous-versions/ms828505(v=msdn.10)) des [Rendererobjekts](/previous-versions/ms828481(v=msdn.10)) verarbeitet die Konvertierung von Pixeln in den vergrößerten Koordinatenbereich und übernimmt alle Skalierungs- und Bildlaufs, die durch die Ansichts- und Objekttransformationen angewendet werden.


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



## <a name="zooming-to-a-rectangle"></a>Zoomen auf ein Rechteck

Die `pnlDrawingArea` Panelereignishandler verwalten das Zeichnen des Rechtecks in das Fenster. Wenn der Befehl Zoom To Rect im Menü Modus aktiviert ist, ruft der [MouseUp-Ereignishandler](/previous-versions/ms567618(v=vs.100)) die -Methode der Anwendung `ZoomToRectangle` auf. Die -Methode berechnet die Breite und Höhe des Rechtecks, prüft auf Begrenzungsbedingungen, aktualisiert die Werte der Scrollleiste und den Skalierungsfaktor und ruft dann die -Methode der Anwendung auf, um die neuen Einstellungen `ZoomToRectangle` `UpdateZoomAndScroll` anzuwenden.

## <a name="closing-the-form"></a>Schließen des Formulars

Die Dispose-Methode [des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector-Objekt](/previous-versions/ms583683(v=vs.100)) zurück.

 

 
