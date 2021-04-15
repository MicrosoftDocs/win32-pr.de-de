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
# <a name="ink-zoom-sample"></a><span data-ttu-id="f6ee1-103">Ink Zoom-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f6ee1-103">Ink Zoom Sample</span></span>

<span data-ttu-id="f6ee1-104">In diesem Beispielprogramm wird veranschaulicht, wie frei Hand Eingaben vergrößert und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-104">This sample program demonstrates how to zoom and scroll ink.</span></span> <span data-ttu-id="f6ee1-105">Insbesondere ermöglicht der Benutzer das Vergrößern und Verkleinern von frei Hand Eingaben in Inkrementen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-105">In particular, it enables the user to zoom in and out of ink in increments.</span></span> <span data-ttu-id="f6ee1-106">Außerdem wird veranschaulicht, wie Sie mithilfe eines Zoom Rechtecks in eine bestimmte Region zoomen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-106">It also demonstrates how to zoom into a particular region using a zoom rectangle.</span></span> <span data-ttu-id="f6ee1-107">Schließlich wird in diesem Beispiel veranschaulicht, wie frei Hand Eingaben mit unterschiedlichen Zoom Verhältnissen gesammelt werden und wie der Bildlauf innerhalb des gezogenen Zeichnungs Bereichs eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-107">Finally, this sample illustrates how to collect ink at different zoom ratios and how to set up scrolling within the zoomed drawing area.</span></span>

<span data-ttu-id="f6ee1-108">Im Beispiel werden die Ansichts-und Objekt Transformationen des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) verwendet, um Zoom und Bildlauf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-108">In the sample, the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's view and object transforms are used to perform zooming and scrolling.</span></span> <span data-ttu-id="f6ee1-109">Die Ansichts Transformation gilt für die Punkte und die Stift Breite.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-109">The view transform applies to the points and the pen width.</span></span> <span data-ttu-id="f6ee1-110">Die Objekt Transformation gilt nur für Punkte.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-110">The object transform applies only to the points.</span></span> <span data-ttu-id="f6ee1-111">Der Benutzer kann steuern, welche Transformation verwendet wird, indem er im Menü Modus die Breite für das Pen-Breite-Element ändert.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-111">The user can control which transform is used by changing the Scale Pen Width item on the Mode menu.</span></span>

> [!Note]  
> <span data-ttu-id="f6ee1-112">Es ist problematisch, einige com-Aufrufe für bestimmte Schnittstellen Methoden auszuführen (z. b.[**inkrenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) und [**inkrenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)), wenn eine Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-112">It is problematic to perform some COM calls on certain interface methods ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) and [**InkRenderer.SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), for example) when a message has been SENT.</span></span> <span data-ttu-id="f6ee1-113">Wenn Nachrichten gesendet werden, müssen Sie in die Warteschlange Nachrichten gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-113">When messages are SENT, they need to be marshalled to the POST message queue.</span></span> <span data-ttu-id="f6ee1-114">Um dieses Szenario zu beheben, testen Sie, ob Sie eine Nachricht von Post verarbeiten, indem Sie [**insendmesssageex**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) aufrufen und die Nachricht an Sie senden, wenn die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-114">To address this scenario, test whether you are handling a message from POST by calling [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) and POST the message to yourself if the message was SENT.</span></span>

 

<span data-ttu-id="f6ee1-115">In diesem Beispiel werden die folgenden Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="f6ee1-115">The following features are used in this sample:</span></span>

-   <span data-ttu-id="f6ee1-116">Das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt</span><span class="sxs-lookup"><span data-stu-id="f6ee1-116">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object</span></span>
-   <span data-ttu-id="f6ee1-117">Die [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) -Methode des [Renderer](/previous-versions/ms828481(v=msdn.10)) -Objekts</span><span class="sxs-lookup"><span data-stu-id="f6ee1-117">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method</span></span>
-   <span data-ttu-id="f6ee1-118">Die [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f6ee1-118">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method</span></span>

## <a name="initializing-the-form"></a><span data-ttu-id="f6ee1-119">Initialisieren des Formulars</span><span class="sxs-lookup"><span data-stu-id="f6ee1-119">Initializing the Form</span></span>

<span data-ttu-id="f6ee1-120">Zunächst wird im Beispiel auf die Tablet PC-Automatisierungs Schnittstellen verwiesen, die im Windows Vista-oder Windows XP Tablet PC Edition Software Development Kit (SDK) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-120">First, the sample references the Tablet PC Automation interfaces, which are provided in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="f6ee1-121">Das Beispiel deklariert einen [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` und einige private Member, um die Skalierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-121">The sample declares an [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector`, and some private members to help with scaling.</span></span>


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



<span data-ttu-id="f6ee1-122">Anschließend [wird im Beispiel](/previous-versions/ms583683(v=vs.100)) der [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignishandler des Formulars erstellt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-122">Then the sample creates and enables the [InkCollector](/previous-versions/ms583683(v=vs.100)) in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="f6ee1-123">Außerdem wird die [Width](/previous-versions/ms837941(v=msdn.10)) -Eigenschaft der [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des InkCollector-Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-123">Also, the [Width](/previous-versions/ms837941(v=msdn.10)) property of the InkCollector object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property is set.</span></span> <span data-ttu-id="f6ee1-124">Schließlich werden die Schiebe leisten Bereiche definiert, und die-Methode der Anwendung `UpdateZoomAndScroll` wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-124">Finally, the scroll bar ranges are defined and the application's `UpdateZoomAndScroll` method is called.</span></span>


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



## <a name="updating-the-zoom-and-scroll-values"></a><span data-ttu-id="f6ee1-125">Aktualisieren von Zoom-und Bild Lauf Werten</span><span class="sxs-lookup"><span data-stu-id="f6ee1-125">Updating the Zoom and Scroll Values</span></span>

<span data-ttu-id="f6ee1-126">Der Zeichenbereich des frei Hand Sammlers ist von vielen Ereignissen betroffen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-126">The drawing area of the ink collector is affected by many events.</span></span> <span data-ttu-id="f6ee1-127">In der- `UpdateZoomAndScroll` Methode wird eine Transformationsmatrix verwendet, um den frei Hand Sammler innerhalb des Fensters zu skalieren und zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-127">In the `UpdateZoomAndScroll` method, a transformation matrix is used to both scale and translate the ink collector within the window.</span></span>

> [!Note]  
> <span data-ttu-id="f6ee1-128">Die [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) wendet die Transformation auf die Striche und die Stift Breite an, während die [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) -Methode nur die Transformation auf die Striche anwendet.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-128">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method applies the transform to both the strokes and the pen width, while the [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method only applies the transform to the strokes.</span></span>

 

<span data-ttu-id="f6ee1-129">Schließlich wird die-Methode der Anwendung `UpdateScrollBars` aufgerufen, und das Formular wird zum Aktualisieren gezwungen.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-129">Finally, the application's `UpdateScrollBars` method is called and the form is forced to refresh.</span></span>


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



## <a name="managing-the-scroll-bars"></a><span data-ttu-id="f6ee1-130">Verwalten der Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="f6ee1-130">Managing the Scroll Bars</span></span>

<span data-ttu-id="f6ee1-131">Die-Methode richtet die Bild Lauf leisten so ein, dass Sie `UpdateScrollBars` ordnungsgemäß mit der aktuellen Fenstergröße, der Zoomeinstellung und der Scrollposition innerhalb von [InkCollector](/previous-versions/ms583683(v=vs.100))funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-131">The `UpdateScrollBars` method sets up the scroll bars to work correctly with the current window size, zoom setting, and scroll location within the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span> <span data-ttu-id="f6ee1-132">Diese Methode berechnet die großen Änderungen und kleinen Änderungs Werte für die vertikalen und horizontalen Scrollleisten.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-132">This method calculates the large change and small change values for the vertical and horizontal scroll bars.</span></span> <span data-ttu-id="f6ee1-133">Außerdem wird der aktuelle Wert der Scrollleisten berechnet und ob Sie sichtbar sein sollten.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-133">It also calculates the current value of the scroll bars and whether they should be visible.</span></span> <span data-ttu-id="f6ee1-134">Die [Pixel toinkspace](/previous-versions/ms828505(v=msdn.10)) -Methode des [rendererobjekts](/previous-versions/ms828481(v=msdn.10)) behandelt die Konvertierung von Pixeln in den Zoom-Koordinaten Bereich und die Konten für die Skalierung und den Bildlauf, die durch die Ansichts-und Objekt Transformationen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-134">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method handles the conversion from pixels to the zoomed coordinate space and accounts for any scaling and scrolling that is applied through the view and object transforms.</span></span>


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



## <a name="zooming-to-a-rectangle"></a><span data-ttu-id="f6ee1-135">Zoomen zu einem Rechteck</span><span class="sxs-lookup"><span data-stu-id="f6ee1-135">Zooming to a Rectangle</span></span>

<span data-ttu-id="f6ee1-136">Der `pnlDrawingArea` Panel-Ereignishandler verwaltet das Zeichnen des Rechtecks in das Fenster.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-136">The `pnlDrawingArea` panel event handlers manage drawing the rectangle to the window.</span></span> <span data-ttu-id="f6ee1-137">Wenn der Befehl Zoom to Rect im Menü Modus aktiviert ist, ruft der [MouseUp](/previous-versions/ms567618(v=vs.100)) -Ereignishandler die-Methode der Anwendung auf `ZoomToRectangle` .</span><span class="sxs-lookup"><span data-stu-id="f6ee1-137">If the Zoom To Rect command is checked on the Mode menu, then the [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler calls the application's `ZoomToRectangle` method.</span></span> <span data-ttu-id="f6ee1-138">Die `ZoomToRectangle` -Methode berechnet die Breite und Höhe des Rechtecks, prüft auf begrenzungsbedingungen, aktualisiert die ScrollBar-Werte und den Skalierungsfaktor und ruft dann die-Methode der Anwendung `UpdateZoomAndScroll` auf, um die neuen Einstellungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-138">The `ZoomToRectangle` method calculates the width and height of the rectangle, checks for boundary conditions, updates the scroll bar values and the scale factor, and then calls the application's `UpdateZoomAndScroll` method to apply the new settings.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="f6ee1-139">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="f6ee1-139">Closing the Form</span></span>

<span data-ttu-id="f6ee1-140">Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms583683(v=vs.100)) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="f6ee1-140">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
