---
description: Auf dieser Seite wird beschrieben, wie Grafiken in einer XPS OM gezeichnet werden.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Zeichnen von Grafiken in einer XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2f9eacb19ba39263cff3898451479d8bed28e1d83ac6fe251fb9b4da62f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719310"
---
# <a name="draw-graphics-in-an-xps-om"></a>Zeichnen von Grafiken in einer XPS OM

Auf dieser Seite wird beschrieben, wie Grafiken in einer XPS OM gezeichnet werden.

Um vektorbasierte Grafiken auf einer Seite zu zeichnen, instanziieren Sie eine [**IXpsOMPath-Schnittstelle,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) füllen Sie sie mit dem gewünschten Inhalt auf, und fügen Sie sie der Liste der visuellen Objekte der Seite oder canvas hinzu. Eine **IXpsOMPath-Schnittstelle** enthält solche Eigenschaften einer vektorbasierten Form wie Kontur, Füllfarbe, Linienstil und Linienfarbe. Die Form des Pfads wird von einer [**IXpsOMGeometry-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) angegeben, die eine Auflistung von [**IXpsOMGeometryFigure-Schnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) und optional eine [**IXpsOMMatrixTransform-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) enthält. Sie können eine beliebige Schnittstelle verwenden, die von der [**IXpsOMBrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) erbt, um den Umkreis des Pfads und das Innere der Form zu füllen, die vom Pfad beschrieben wird.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss unter [Common XPS Document Programming Tasks (Allgemeine XPS-Dokumentprogrammierungsaufgaben).](common-xps-document-tasks.md)

## <a name="code-example"></a>Codebeispiel

Im folgenden Codebeispiel wird ein einfacher Pfad erstellt, der ein Rechteck beschreibt, das mit einer einzelnen Farbe gefüllt ist.

### <a name="create-the-stroke-and-the-fill-brushes"></a>Erstellen des Strichs und der Füllpinsel

Im ersten Abschnitt des Codebeispiels wird der [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) erstellt, der zum Füllen des Pfadobjekts verwendet wird.


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

Im zweiten Abschnitt des Codebeispiels wird die [**IXpsOMGeometry-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) erstellt. Anschließend wird die [**IXpsOMGeometryFigure-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) erstellt, die die Form der Figur angibt, und die Figur der **IXpsOMGeometry-Schnittstelle** hinzugefügt. Im Beispiel wird ein Rechteck erstellt, das durch *rect* angegeben wird. Segmente müssen nur für drei der vier Seiten des Rechtecks definiert werden. Der Umkreis der Form, in diesem Fall das Rechteck, beginnt am Anfangspunkt und erstreckt sich entsprechend der Definition durch die Segmente der Geometriefigur. Wenn Sie die **IsClosed-Eigenschaft** auf **TRUE** festlegen, wird das Rechteck geschlossen, indem ein zusätzliches Segment hinzugefügt wird, das das Ende des letzten Segments mit dem Startpunkt verbindet.


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



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a>Erstellen sie den Pfad, und fügen Sie ihn der visuellen Sammlung hinzu.

Der letzte Abschnitt dieses Codebeispiels erstellt und konfiguriert das Pfadobjekt und fügt es dann der Liste der visuellen Objekte der Seite hinzu.


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



## <a name="best-practices"></a>Empfehlungen

Fügen Sie eine Textbeschreibung der Form hinzu, die von der [**IXpsOMPath-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) angegeben wird. Verwenden Sie für Benutzer mit Sehbehinderung die Methoden [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) und [**SetAccessibilityLongDescription,**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) um Textinhalte für Barrierefreiheitsunterstützungsfunktionen wie Sprachausgaben bereitzustellen.

## <a name="additional-information"></a>Zusätzliche Informationen

Im Codebeispiel auf dieser Seite wird eine [**IXpsOMSolidColorBrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) als Füllpinsel und Strichpinsel für den Pfad verwendet. Zusätzlich zur **IXpsOMSolidColorBrush-Schnittstelle** können Sie eine [**IXpsOMGradientBrush-,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush) [**IXpsOMImageBrush-**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)oder [**IXpsOMVisualBrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) verwenden.

Der Strich ist die Linie, die um den Umkreis der Figur gezeichnet werden kann. Die [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) unterstützt viele verschiedene Strichlinienstile. Um die Strichlinienart anzugeben, legen Sie die Stricheigenschaften mit den folgenden Methoden der [**IXpsOMPath-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) fest:

-   [**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) oder [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) zum Festlegen des Strichpinsels
-   [**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) zum Abrufen der Strichstrichauflistung, die die Striche beschreibt
-   [**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) auf und [**SetStrokeDashOffset,**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) um die Darstellung eines gestrichelten Strichs zu beschreiben
-   [**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) und [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) zum Definieren des Stils für die Zeilenbeendigung
-   [**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) und [**SetStrokeMiterLimit,**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) um zu beschreiben, wie die Segmente verknüpft werden
-   [**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) zum Festlegen der Strichstärke

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Navigieren im XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[Schreiben von Text in eine XPS OM](write-text-to-an-xps-om.md)
</dt> <dt>

[Platzieren von Bildern in einer XPS OM](place-images-in-an-xps-om.md)
</dt> <dt>

[Schreiben einer XPS OM in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Drucken einer XPS OM](print-an-xps-om.md)
</dt> <dt>

**Wird auf dieser Seite verwendet**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**IXpsOMGeometryFigureCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren einer XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[REFERENZ ZUR XPS-Dokument-API](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
