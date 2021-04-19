---
description: Beschreibt das Platzieren von Bildern in einem XPS-om.
ms.assetid: 4c7e3630-7331-47d7-91cc-da3cc2b7f8c9
title: Platzieren von Bildern in einem XPS-OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f72b5d1b1380cd870f9ff6b7a1cd15763e5b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360789"
---
# <a name="place-images-in-an-xps-om"></a>Platzieren von Bildern in einem XPS-OM

Beschreibt das Platzieren von Bildern in einem XPS-om.

Um Bilder in einem XPS-OM zu platzieren, erstellen Sie ein Pfad Objekt, das die Position und Gliederung eines Bilds definiert, und verwenden Sie dann einen Bild Pinsel, um den Pfad auszufüllen. Fügen Sie das erstellte Pfad Objekt der Liste von visuellen Objekten der Seite oder der Canvas hinzu, sodass es mit dem anderen visuellen Inhalt gerendert werden kann.

Bevor Sie diese Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

## <a name="code-example"></a>Codebeispiel

### <a name="create-image-resource"></a>Image Ressource erstellen

Wenn das Quell Image im XPS-om nicht als Bildressource verfügbar ist, erstellen Sie zunächst die Image-Ressource:


```C++
    HRESULT                hr = S_OK;
    IStreamPtr             imageStream; // the resulting image stream
    IOpcPartUri            *imagePartUri;
    IXpsOMImageResource    *imageResource;

     XPS_RECT    rect = {0.0f, 0.0f, 0.0f, 0.0f}; // set to image size

    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
            imageFileName, &imageStream );

    hr = xpsFactory->CreatePartUri( imagePartName, &imagePartUri );

    imageType; // set to type of image being read in
    hr = xpsFactory->CreateImageResource ( 
        imageStream,
        imageType,
        imagePartUri,
        &imageResource);
    imagePartUri->Release();
    imageStream->Release();

    // imageResource can now be used by other parts in the XPS OM.
```



### <a name="place-image-into-visual-collection"></a>Bild in visueller Auflistung platzieren

Wenn das Quell Image im XPS-OM als Bildressource verfügbar ist, kann es verwendet werden, um ein Bild Pinsel Objekt zu erstellen und dem Pfad, der die Bildposition und-Größe auf der Seite beschreibt, als Füll Pinsel hinzuzufügen.


```C++
    // These variables are initialized outside of this code example,
    //  for example, as the parameters of a method or from some 
    //  preceding program code.

    // dimensions of the image in pixels
    XPS_SIZE    bmpDim = {0,0} ; 

    // DPI resolution values obtained from image
    FLOAT        dpiX = 96.0f;
    FLOAT        dpiY = 96.0f;
    
    // initialize viewport values 
    XPS_RECT    viewPort = {0.0,0.0,0.0,0.0};

    // initialize viewbox values
    XPS_RECT    viewBox = {0.0,0.0,0.0,0.0}; 

    // These are part of this code example.
    IXpsOMPath *imageRectPath;
    IXpsOMImageBrush *imageBrush;
    IXpsOMVisualCollection *pageVisuals;

    // Describe image source dimensions and set viewbox to be the 
    // entire image DIP width of image. 
    //  Example: 
    //    600 image pixels, 300 dpi -> 2 inches -> 2 * 96 = 192 DIP width
    viewBox.width = FLOAT((double)bmpDim.width * 96.0 / dpiX); 
    viewBox.height = FLOAT((double)bmpDim.height * 96.0 / dpiY);

    // Describe the size and position of the image destination.
    //  rect is an XPS_RECT structure that is initialized outside
    //  of this sample for example, it might be passed in as a parameter.

    // destination rectangle
    viewPort.x = rect.x;
    viewPort.y = rect.y;
    viewPort.width = rect.width;
    viewPort.height = rect.height;

    // Create the image brush.
    hr = xpsFactory->CreateImageBrush(imageResource, &viewBox, &viewPort, 
        reinterpret_cast<IXpsOMImageBrush**>(&imageBrush));

    // Create the path that describes the outline of the image on the page.
    //  This step uses the function described in the next code example.
    hr = CreateRectanglePath(xpsFactory, &rect,
        reinterpret_cast<IXpsOMPath**>(&imageRectPath));

    // Set the accessibility description for the path object as required.
    hr = imageRectPath->SetAccessibilityShortDescription( shortDescText );

    // Set the image brush to be the fill brush for this path.
    hr = imageRectPath->SetFillBrushLocal( imageBrush );

    // Get the list of visuals for this page...
    hr = xpsPage->GetVisuals( &pageVisuals );

    // ...and add the completed path to the list.
    hr = pageVisuals->Append( imageRectPath );

    // Release locally created interfaces.
    if (NULL != pageVisuals) pageVisuals->Release();
    if (NULL != imageRectPath) imageRectPath->Release();
    if (NULL != imageBrush) imageBrush->Release();

```



### <a name="create-path-object-for-image"></a>Pfad Objekt für Image erstellen

Die folgende Methode akzeptiert eine **XPS- \_ Rect** -Struktur und erstellt einen rechteckigen Pfad.


```C++
HRESULT 
CreateRectanglePath(
    __in  IXpsOMObjectFactory   *xpsFactory,
    __in  const XPS_RECT        *rect,
    __out IXpsOMPath            **rectPath
)
{
   
    HRESULT hr = S_OK;

    IXpsOMGeometryFigure           *rectFigure;
    IXpsOMGeometry                 *imageRectGeometry;
    IXpsOMGeometryFigureCollection *geomFigureCollection;

    // Define start point and three of the four sides of the rectangle.
    //  The fourth side is implied by setting the path type to CLOSED.
    XPS_POINT            startPoint = {rect->x, rect->y};
    XPS_SEGMENT_TYPE     segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };
    FLOAT segmentData[6] = {
        rect->x,              rect->y+rect->height, 
        rect->x+rect->width,  rect->y+rect->height, 
        rect->x+rect->width,  rect->y 
    };
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE
    };

    // Create a closed geometry figure using the three 
    //  segments defined above.

    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
    hr = rectFigure->SetSegments( 3, 6, 
            segmentTypes, segmentData, segmentStrokes );

    // Create a geometry that consists of the figure created above.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );
    hr = geomFigureCollection->Append( rectFigure );

    // Create the path that consists of the geometry created above
    //  and return the pointer in the parameter passed in to the function.
    hr = xpsFactory->CreatePath( reinterpret_cast<IXpsOMPath**>(rectPath) );
    hr = (*rectPath)->SetGeometryLocal( imageRectGeometry );

    // The calling method will release these interfaces when 
    //  it is done with them.

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Navigieren im XPS-OM](navigate-the-xps-om.md)
</dt> <dt>

[Schreiben von Text in ein XPS-OM](write-text-to-an-xps-om.md)
</dt> <dt>

[Zeichnen von Grafiken in einem XPS-OM](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Schreiben eines XPS-om in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Drucken eines XPS-OM](print-an-xps-om.md)
</dt> <dt>

**Auf dieser Seite verwendet**
</dt> <dt>

[**Iopcparamei**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**Ixpsomimagebrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[**Ixpsomimageresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[**Ixpsomgeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**Ixpsomgeometryfigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**Ixpsomgeometryfigurückruf**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[**Ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Ixpsompath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
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

 

 
