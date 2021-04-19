---
description: Auf dieser Seite wird beschrieben, wie Grafiken in einem XPS-OM gezeichnet werden.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Zeichnen von Grafiken in einem XPS-OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabbf8cfb821c80dfff43e2e7844331c8920f726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356700"
---
# <a name="draw-graphics-in-an-xps-om"></a><span data-ttu-id="ef479-103">Zeichnen von Grafiken in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ef479-103">Draw Graphics in an XPS OM</span></span>

<span data-ttu-id="ef479-104">Auf dieser Seite wird beschrieben, wie Grafiken in einem XPS-OM gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ef479-104">This page describes how to draw graphics in an XPS OM.</span></span>

<span data-ttu-id="ef479-105">Um vektorbasierte Grafiken in einer Seite zu zeichnen, instanziieren Sie eine [**ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) -Schnittstelle, füllen Sie Sie mit dem gewünschten Inhalt auf, und fügen Sie Sie der Liste der visuellen Objekte der Seite oder Canvas hinzu.</span><span class="sxs-lookup"><span data-stu-id="ef479-105">To draw vector-based graphics in a page, instantiate an [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface, populate it with the desired content, and add it to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="ef479-106">Eine **ixpsompath** -Schnittstelle enthält solche Eigenschaften einer vektorbasierten Form als Kontur, Füllfarbe, Linienart und Linien Farbe.</span><span class="sxs-lookup"><span data-stu-id="ef479-106">An **IXpsOMPath** interface contains such properties of a vector-based shape as the outline, fill color, line style, and line color.</span></span> <span data-ttu-id="ef479-107">Die Form des Pfads wird durch eine [**ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) -Schnittstelle angegeben, die eine Auflistung von [**ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) -Schnittstellen und optional eine [**ixpsommatrixtransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) -Schnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="ef479-107">The path's shape is specified by an [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface, which contains a collection of [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interfaces and, optionally, an [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) interface.</span></span> <span data-ttu-id="ef479-108">Sie können jede beliebige Schnittstelle verwenden, die von der [**ixpsombrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) -Schnittstelle erbt, um den Umkreis des Pfads und das Innere der Form auszufüllen, die durch den Pfad beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ef479-108">You can use any interface that inherits from the [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) interface to fill the perimeter of the path and the interior of the shape that is described by the path.</span></span>

<span data-ttu-id="ef479-109">Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="ef479-109">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="ef479-110">Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ef479-110">Code Example</span></span>

<span data-ttu-id="ef479-111">Im folgenden Codebeispiel wird ein einfacher Pfad zum Beschreiben eines Rechtecks erstellt, das mit einer einzelnen Farbe gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ef479-111">The following code example creates a simple path that describes a rectangle that is filled with a single color.</span></span>

### <a name="create-the-stroke-and-the-fill-brushes"></a><span data-ttu-id="ef479-112">Erstellen der Striche und Füll Pinsel</span><span class="sxs-lookup"><span data-stu-id="ef479-112">Create the stroke and the fill brushes</span></span>

<span data-ttu-id="ef479-113">Im ersten Abschnitt des Code Beispiels wird [**ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) erstellt, das zum Ausfüllen des Path-Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef479-113">The first section of the code example creates the [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) that will be used to fill the path object.</span></span>


```C++
    HRESULT               hr = S_OK;

    XPS_COLOR             xpsColor;
    IXpsOMSolidColorBrush *xpsFillBrush = NULL;
    IXpsOMSolidColorBrush *xpsStrokeBrush = NULL;

    // Set the fill brush color to RED.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColor,
        NULL,          // color profile resource
        &xpsFillBrush);
    // The color profile resource parameter is NULL because
    //  this color type does not use a color profile resource.

    // Set the stroke brush color to BLACK.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0x00;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
            &xpsColor,
            NULL, // This color type does not use a color profile resource.
            &xpsStrokeBrush);

    // The brushes are released below after they have been used.
```



### <a name="define-the-shape"></a><span data-ttu-id="ef479-114">Definieren der Form</span><span class="sxs-lookup"><span data-stu-id="ef479-114">Define the shape</span></span>

<span data-ttu-id="ef479-115">Im zweiten Abschnitt des Code Beispiels wird die [**ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) -Schnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef479-115">The second section of the code example creates the [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface.</span></span> <span data-ttu-id="ef479-116">Anschließend wird die [**ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) -Schnittstelle erstellt, die die Form der Abbildung angibt, und die Abbildung wird der **ixpsomgeometry** -Schnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ef479-116">It then creates the [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interface that specifies the figure's shape, and adds the figure to the **IXpsOMGeometry** interface.</span></span> <span data-ttu-id="ef479-117">Im Beispiel wird ein Rechteck erstellt, das von *Rect* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef479-117">The example creates a rectangle that is specified by *rect*.</span></span> <span data-ttu-id="ef479-118">Segmente müssen nur für drei der vier Seiten des Rechtecks definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef479-118">Segments must be defined for only three of the four sides of the rectangle.</span></span> <span data-ttu-id="ef479-119">Der Umkreis der Form, das Rechteck in diesem Fall, beginnt am Startpunkt und erweitert die Definition durch die Segmente der Geometrie-Abbildung.</span><span class="sxs-lookup"><span data-stu-id="ef479-119">The perimeter of the shape, the rectangle in this case, starts from the start point and extends as defined by the segments of the geometry figure.</span></span> <span data-ttu-id="ef479-120">Wenn die **IsClosed** -Eigenschaft auf **true** festgelegt wird, wird angegeben, dass das Rechteck geschlossen wird, indem ein zusätzliches Segment hinzugefügt wird, das das Ende des letzten Segments mit dem Startpunkt verbindet.</span><span class="sxs-lookup"><span data-stu-id="ef479-120">Setting the **IsClosed** property to **TRUE** indicates that the rectangle is closed by adding one additional segment that connects the end of the last segment to the start point.</span></span>


```C++
    // rect is initialized outside of the sample and 
    //  contains the coordinates of the rectangular geometry to create.
    XPS_RECT                            rect = {0,0,100,100};       

    HRESULT                             hr = S_OK;
    IXpsOMGeometryFigure                *rectFigure;
    IXpsOMGeometry                      *imageRectGeometry;
    IXpsOMGeometryFigureCollection      *geomFigureCollection;

    // Define the start point and create an empty figure.
    XPS_POINT                           startPoint = {rect.x, rect.y};
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    // Define the segments of the geometry figure.
    //  First, define the type of each segment.
    XPS_SEGMENT_TYPE segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE,  // each segment is a straight line
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // Define the x and y coordinates of each corner of the figure
    //  the start point has already been defined so only the 
    //  remaining three corners need to be defined.
    FLOAT segmentData[6] = {
        rect.x,                (rect.y + rect.height),
        (rect.x + rect.width), (rect.y + rect.height), 
        (rect.x + rect.width), rect.y 
    };

    // Describe if the segments are stroked (that is if the segment lines
    //  should be drawn as a line).
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE // Yes, draw each of the segment lines.
    };

    // Add the segment data to the figure.
    hr = rectFigure->SetSegments(
                        3, 
                        6, 
                        segmentTypes, 
                        segmentData, 
                        segmentStrokes);

    // Set the closed and filled properties of the figure.
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
 
    // Create the geometry object.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    
    // Get a pointer to the figure collection interface of the geometry...
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );

    // ...and then add the figure created above to this geometry.
    hr = geomFigureCollection->Append( rectFigure );
    // If not needed for anything else, release the rectangle figure.
    rectFigure->Release();

    // when done adding figures, release the figure collection. 
    geomFigureCollection->Release();

    //  When done with the geometry object, release the object.
    // imageRectGeometry->Release();
    //  In this case, imageRectGeometry is used in the next sample
    //  so the geometry object is not released, yet.
    
```



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a><span data-ttu-id="ef479-121">Erstellen Sie den Pfad, und fügen Sie ihn der visuellen Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ef479-121">Create the path and add it to the visual collection</span></span>

<span data-ttu-id="ef479-122">Im letzten Abschnitt dieses Code Beispiels wird das Path-Objekt erstellt und konfiguriert und dann der Liste der visuellen Objekte der Seite hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ef479-122">The final section of this code example creates and configures the path object, then adds it to the page's list of visual objects.</span></span>


```C++
    HRESULT                    hr = S_OK;
    // The page interface pointer is initialized outside of this sample.
    IXpsOMPath                *rectPath = NULL;
    IXpsOMVisualCollection    *pageVisuals = NULL;

    // Create the new path object.
    hr = xpsFactory->CreatePath( &rectPath );

    // Add the geometry to the path.
    //  imageRectGeometry is initialized outside of this example.
    hr = rectPath->SetGeometryLocal( imageRectGeometry );

    // Set the short description of the path to provide
    //  a textual description of the object for accessibility.
    hr = rectPath->SetAccessibilityShortDescription( L"Red Rectangle" );
    
    // Set the fill and stroke brushes to use the brushes 
    //  created in the first section.
    hr = rectPath->SetFillBrushLocal( xpsFillBrush );
    hr = rectPath->SetStrokeBrushLocal( xpsStrokeBrush);

    // Get the visual collection of this page and add this path to it.
    hr = xpsPage->GetVisuals( &pageVisuals );
    hr = pageVisuals->Append( rectPath );
    // If not needed for anything else, release the rectangle path.
    rectPath->Release();
    
    // When done with the visual collection, release it.
    pageVisuals->Release();

    // When finished with the brushes, release the interface pointers.
    if (NULL != xpsFillBrush) xpsFillBrush->Release();
    if (NULL != xpsStrokeBrush) xpsStrokeBrush->Release();

    // When done with the geometry interface, release it.
    imageRectGeometry->Release();

    // When done with the path interface, release it.
    rectPath->Release();

```



## <a name="best-practices"></a><span data-ttu-id="ef479-123">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="ef479-123">Best Practices</span></span>

<span data-ttu-id="ef479-124">Fügen Sie eine Textbeschreibung der Form hinzu, die durch die [**ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) -Schnittstelle angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef479-124">Add a textual description of the shape that is specified by the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface.</span></span> <span data-ttu-id="ef479-125">Verwenden Sie die Methoden [**setaccessibilityshortdescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) und [**setaccessibilitylongdescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) , um Textinhalte für Barrierefreiheits Funktionen bereitzustellen, z. b. Sprachausgaben.</span><span class="sxs-lookup"><span data-stu-id="ef479-125">For the benefit of visually impaired users, use the [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) and [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) methods to provide textual content for accessibility support features, such as screen readers.</span></span>

## <a name="additional-information"></a><span data-ttu-id="ef479-126">Zusätzliche Informationen</span><span class="sxs-lookup"><span data-stu-id="ef479-126">Additional Information</span></span>

<span data-ttu-id="ef479-127">Das Codebeispiel auf dieser Seite verwendet eine [**ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) -Schnittstelle als Füll Pinsel und einen Strich Pinsel für den Pfad.</span><span class="sxs-lookup"><span data-stu-id="ef479-127">The code example on this page uses an [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) interface as the fill brush and stroke brush for the path.</span></span> <span data-ttu-id="ef479-128">Zusätzlich zur **ixpsomsolidcolorbrush** -Schnittstelle können Sie eine [**ixpsomgradientbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)-, [**ixpsomimagebrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)-oder [**ixpsomvisualbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef479-128">In addition to the **IXpsOMSolidColorBrush** interface, you can use an [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush), or [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) interface.</span></span>

<span data-ttu-id="ef479-129">Der Strich ist die Linie, die um den Umkreis der Abbildung herum gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef479-129">The stroke is the line that can be drawn around the perimeter of the figure.</span></span> <span data-ttu-id="ef479-130">Die [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) unterstützt viele verschiedene Strich Linienstile.</span><span class="sxs-lookup"><span data-stu-id="ef479-130">The [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supports many different stroke line styles.</span></span> <span data-ttu-id="ef479-131">Um den Strich Linienstil anzugeben, legen Sie die Stroke-Eigenschaften mit den folgenden Methoden der [**ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) -Schnittstelle fest:</span><span class="sxs-lookup"><span data-stu-id="ef479-131">To specify the stroke line style, set the stroke properties with the following methods of the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface:</span></span>

-   <span data-ttu-id="ef479-132">[**Setstrokebrushlocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) oder [**setstrokebrushlookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) zum Festlegen des Pinselstrichs</span><span class="sxs-lookup"><span data-stu-id="ef479-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) or [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) to set the stroke brush</span></span>
-   <span data-ttu-id="ef479-133">[**Getstrokedashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) zum Aufrufen der Stroke Dash-Auflistung, in der die Striche beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ef479-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) to get the stroke dash collection that describes the strokes</span></span>
-   <span data-ttu-id="ef479-134">[**Setstrokedashcap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) auf und [**setstrokedashoffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) , um die Darstellung eines gestrichelten Strichs zu beschreiben</span><span class="sxs-lookup"><span data-stu-id="ef479-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to and [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) to describe the appearance of a dashed stroke</span></span>
-   <span data-ttu-id="ef479-135">[**Setstrokeendlinecap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) und [**setstrokestartlinecap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) zum Definieren des linienbeendigungs Stils</span><span class="sxs-lookup"><span data-stu-id="ef479-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) and [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) to define the line termination style</span></span>
-   <span data-ttu-id="ef479-136">[**Setstrokelinejoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) und [**setstrokemiterlimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) , um zu beschreiben, wie die Segmente verknüpft werden</span><span class="sxs-lookup"><span data-stu-id="ef479-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) and [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) to describe how the segments are joined</span></span>
-   <span data-ttu-id="ef479-137">[**Setstrokedicke**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) zum Festlegen der Strichstärke</span><span class="sxs-lookup"><span data-stu-id="ef479-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) to set the stroke thickness</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef479-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef479-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ef479-139">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="ef479-139">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="ef479-140">Navigieren im XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ef479-140">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="ef479-141">Schreiben von Text in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ef479-141">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="ef479-142">Platzieren von Bildern in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ef479-142">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="ef479-143">Schreiben eines XPS-om in ein XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="ef479-143">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="ef479-144">Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ef479-144">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="ef479-145">**Auf dieser Seite verwendet**</span><span class="sxs-lookup"><span data-stu-id="ef479-145">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="ef479-146">**Iopcparamei**</span><span class="sxs-lookup"><span data-stu-id="ef479-146">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="ef479-147">**Ixpsomgeometry**</span><span class="sxs-lookup"><span data-stu-id="ef479-147">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="ef479-148">**Ixpsomgeometryfigure**</span><span class="sxs-lookup"><span data-stu-id="ef479-148">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="ef479-149">**Ixpsomgeometryfigurückruf**</span><span class="sxs-lookup"><span data-stu-id="ef479-149">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="ef479-150">**Ixpsomobjectfactory**</span><span class="sxs-lookup"><span data-stu-id="ef479-150">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="ef479-151">**Ixpsompage**</span><span class="sxs-lookup"><span data-stu-id="ef479-151">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="ef479-152">**Ixpsompath**</span><span class="sxs-lookup"><span data-stu-id="ef479-152">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="ef479-153">**Ixpsomsolidcolorbrush**</span><span class="sxs-lookup"><span data-stu-id="ef479-153">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="ef479-154">**Ixpsomvisualcollection**</span><span class="sxs-lookup"><span data-stu-id="ef479-154">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="ef479-155">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="ef479-155">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="ef479-156">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="ef479-156">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="ef479-157">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="ef479-157">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="ef479-158">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="ef479-158">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
