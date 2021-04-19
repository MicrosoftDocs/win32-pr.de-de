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
# <a name="draw-graphics-in-an-xps-om"></a>Zeichnen von Grafiken in einem XPS-OM

Auf dieser Seite wird beschrieben, wie Grafiken in einem XPS-OM gezeichnet werden.

Um vektorbasierte Grafiken in einer Seite zu zeichnen, instanziieren Sie eine [**ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) -Schnittstelle, füllen Sie Sie mit dem gewünschten Inhalt auf, und fügen Sie Sie der Liste der visuellen Objekte der Seite oder Canvas hinzu. Eine **ixpsompath** -Schnittstelle enthält solche Eigenschaften einer vektorbasierten Form als Kontur, Füllfarbe, Linienart und Linien Farbe. Die Form des Pfads wird durch eine [**ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) -Schnittstelle angegeben, die eine Auflistung von [**ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) -Schnittstellen und optional eine [**ixpsommatrixtransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) -Schnittstelle enthält. Sie können jede beliebige Schnittstelle verwenden, die von der [**ixpsombrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) -Schnittstelle erbt, um den Umkreis des Pfads und das Innere der Form auszufüllen, die durch den Pfad beschrieben wird.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

## <a name="code-example"></a>Codebeispiel

Im folgenden Codebeispiel wird ein einfacher Pfad zum Beschreiben eines Rechtecks erstellt, das mit einer einzelnen Farbe gefüllt ist.

### <a name="create-the-stroke-and-the-fill-brushes"></a>Erstellen der Striche und Füll Pinsel

Im ersten Abschnitt des Code Beispiels wird [**ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) erstellt, das zum Ausfüllen des Path-Objekts verwendet wird.


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



### <a name="define-the-shape"></a>Definieren der Form

Im zweiten Abschnitt des Code Beispiels wird die [**ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) -Schnittstelle erstellt. Anschließend wird die [**ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) -Schnittstelle erstellt, die die Form der Abbildung angibt, und die Abbildung wird der **ixpsomgeometry** -Schnittstelle hinzugefügt. Im Beispiel wird ein Rechteck erstellt, das von *Rect* angegeben wird. Segmente müssen nur für drei der vier Seiten des Rechtecks definiert werden. Der Umkreis der Form, das Rechteck in diesem Fall, beginnt am Startpunkt und erweitert die Definition durch die Segmente der Geometrie-Abbildung. Wenn die **IsClosed** -Eigenschaft auf **true** festgelegt wird, wird angegeben, dass das Rechteck geschlossen wird, indem ein zusätzliches Segment hinzugefügt wird, das das Ende des letzten Segments mit dem Startpunkt verbindet.


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



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a>Erstellen Sie den Pfad, und fügen Sie ihn der visuellen Auflistung hinzu.

Im letzten Abschnitt dieses Code Beispiels wird das Path-Objekt erstellt und konfiguriert und dann der Liste der visuellen Objekte der Seite hinzugefügt.


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



## <a name="best-practices"></a>Bewährte Methoden

Fügen Sie eine Textbeschreibung der Form hinzu, die durch die [**ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) -Schnittstelle angegeben wird. Verwenden Sie die Methoden [**setaccessibilityshortdescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) und [**setaccessibilitylongdescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) , um Textinhalte für Barrierefreiheits Funktionen bereitzustellen, z. b. Sprachausgaben.

## <a name="additional-information"></a>Zusätzliche Informationen

Das Codebeispiel auf dieser Seite verwendet eine [**ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) -Schnittstelle als Füll Pinsel und einen Strich Pinsel für den Pfad. Zusätzlich zur **ixpsomsolidcolorbrush** -Schnittstelle können Sie eine [**ixpsomgradientbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)-, [**ixpsomimagebrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)-oder [**ixpsomvisualbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) -Schnittstelle verwenden.

Der Strich ist die Linie, die um den Umkreis der Abbildung herum gezeichnet werden kann. Die [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) unterstützt viele verschiedene Strich Linienstile. Um den Strich Linienstil anzugeben, legen Sie die Stroke-Eigenschaften mit den folgenden Methoden der [**ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) -Schnittstelle fest:

-   [**Setstrokebrushlocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) oder [**setstrokebrushlookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) zum Festlegen des Pinselstrichs
-   [**Getstrokedashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) zum Aufrufen der Stroke Dash-Auflistung, in der die Striche beschrieben werden.
-   [**Setstrokedashcap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) auf und [**setstrokedashoffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) , um die Darstellung eines gestrichelten Strichs zu beschreiben
-   [**Setstrokeendlinecap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) und [**setstrokestartlinecap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) zum Definieren des linienbeendigungs Stils
-   [**Setstrokelinejoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) und [**setstrokemiterlimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) , um zu beschreiben, wie die Segmente verknüpft werden
-   [**Setstrokedicke**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) zum Festlegen der Strichstärke

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Navigieren im XPS-OM](navigate-the-xps-om.md)
</dt> <dt>

[Schreiben von Text in ein XPS-OM](write-text-to-an-xps-om.md)
</dt> <dt>

[Platzieren von Bildern in einem XPS-OM](place-images-in-an-xps-om.md)
</dt> <dt>

[Schreiben eines XPS-om in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Drucken eines XPS-OM](print-an-xps-om.md)
</dt> <dt>

**Auf dieser Seite verwendet**
</dt> <dt>

[**Iopcparamei**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**Ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**Ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**Ixpsomgeometryfigurückruf**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[**Ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**Ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**Ixpsomvisualcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren eines XPS-OMS](xps-object-model-initialization.md)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
