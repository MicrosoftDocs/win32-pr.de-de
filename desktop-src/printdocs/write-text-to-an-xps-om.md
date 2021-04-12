---
description: In diesem Thema wird beschrieben, wie Text in ein XPS-OM geschrieben wird.
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: Schreiben von Text in ein XPS-OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cca953d5281620cf7b7d9b7b07c133bee0d4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216867"
---
# <a name="write-text-to-an-xps-om"></a>Schreiben von Text in ein XPS-OM

In diesem Thema wird beschrieben, wie Text in ein XPS-OM geschrieben wird.

Der Text wird in ein XPS-OM eingefügt, indem eine [**ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) -Schnittstelle erstellt und formatiert und dann die **ixpsomglyphs** -Schnittstelle zur Liste der visuellen Objekte der Seite oder Canvas hinzugefügt wird. Jede **ixpsomglyphs** -Schnittstelle stellt eine Symbol Führung dar, bei der es sich um eine fortlaufende Zeichenfolge handelt, die ein gemeinsames Format aufweist. Wenn sich ein Zeichenformat Element (z. b. Schriftart Type oder size) ändert oder wenn ein Zeilenumbruch durchgeführt wird, muss eine neue **ixpsomglyphs** -Schnittstelle erstellt und der Liste der visuellen Objekte hinzugefügt werden.

Einige der Eigenschaften einer Glyphe können mithilfe der Methoden der [**ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) -Schnittstelle festgelegt werden. Einige Eigenschaften interagieren jedoch mit anderen und müssen mithilfe einer [**ixpsomglyphseditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) -Schnittstelle festgelegt werden.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

## <a name="code-example"></a>Codebeispiel

### <a name="create-a-glyph-run-from-a-string"></a>Erstellen eines Symbols, das aus einer Zeichenfolge ausgeführt wird

Eine Symbol Führung wird häufig in mehreren Schritten erstellt, die das Laden der Schriftart Ressourcen, die von der Symbol Suche verwendet werden, das Festlegen eines Füll Pinsel, das Festlegen des Schrift Grads und des Start Orts sowie das Festlegen der Unicode-Zeichenfolge beinhalten.

Der folgende Abschnitt des Code Beispiels enthält eine Routine, die einige Variablen annimmt, einschließlich Schriftart Größe, Farbe und Position sowie der zu schreibenden Zeichen. Der Code erstellt dann ein Symbol, das ausgeführt wird, und fügt es einer Seite hinzu. Im Codebeispiel wird davon ausgegangen, dass die in [Initialisieren eines XPS-OMS](xps-object-model-initialization.md) beschriebene Initialisierung aufgetreten ist und dass das Dokument mindestens eine Seite enthält. Weitere Informationen zum Erstellen eines leeren XPS-OMS finden Sie unter [Erstellen eines leeren XPS-OMS](create-a-blank-xps-om.md).


```C++
// Write Text to an XPS OM
HRESULT
WriteText_AddTextToPage(
            // A pre-created object factory
    __in    IXpsOMObjectFactory   *xpsFactory,
            // The font resource to use for this run
    __in    IXpsOMFontResource    *xpsFont,
            // The font size
    __in    float                 fontEmSize,
            // The solid color brush to use for the font
    __in    IXpsOMSolidColorBrush *xpsBrush,
            // The starting location of this glyph run
    __in    XPS_POINT             *origin,
            // The text to use for this run
    __in    LPCWSTR               unicodeString,
            // The page on which to write this glyph run
    __inout IXpsOMPage            *xpsPage        
)
{
    // The data type definitions are included in this function
    // for the convenience of this code example. In an actual
    // implementation they would probably belong in a header file.
    HRESULT                       hr = S_OK;
    XPS_POINT                     glyphsOrigin = {origin->x, origin->y};
    IXpsOMGlyphsEditor            *glyphsEditor = NULL;
    IXpsOMGlyphs                  *xpsGlyphs = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;

    // Create a new Glyphs object and set its properties.
    hr = xpsFactory->CreateGlyphs(xpsFont, &xpsGlyphs);
    hr = xpsGlyphs->SetOrigin(&glyphsOrigin);
    hr = xpsGlyphs->SetFontRenderingEmSize(fontEmSize);
    hr = xpsGlyphs->SetFillBrushLocal(xpsBrush);

    // Some properties are inter-dependent so they
    //    must be changed by using a GlyphsEditor.
    hr = xpsGlyphs->GetGlyphsEditor(&glyphsEditor);
    hr = glyphsEditor->SetUnicodeString(unicodeString);
    hr = glyphsEditor->ApplyEdits();

    // Add the new Glyphs object to the page
    hr = xpsPage->GetVisuals(&pageVisuals);
    hr = pageVisuals->Append(xpsGlyphs);

    // Release interface pointers.
    if (NULL != xpsGlyphs) xpsGlyphs->Release();
    if (NULL != glyphsEditor) glyphsEditor->Release();
    if (NULL != pageVisuals) pageVisuals->Release();

    return hr;
}
```



### <a name="load-and-create-resources"></a>Laden und Erstellen von Ressourcen

Die Erstellung einer [**ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) -Schnittstelle erfordert eine Schriftart Ressource. In vielen Fällen verwendet ein TextBlock die gleiche Schriftart und Farbe. Daher werden in diesem Abschnitt des Code Beispiels die Schriftart Ressourcen Schnittstellen erstellt, die in den Aufrufen verwendet werden, die den Text auf der Seite platzieren.


```C++
    // fontFileName is the name of the font file and it 
    //  is defined outside of this example.

    HRESULT                       hr = S_OK;

    GUID                          fontNameGuid;
    WCHAR                         guidString[128] = {0};
    WCHAR                         uriString[256] = {0};

    IStream                       *fontStream  = NULL;
    IOpcPartUri                   *fontUri = NULL;
    IXpsOMFontResource            *fontResource = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;
    IXpsOMPage                    *page = NULL;
    IXpsOMVisual                  *canvasVisual = NULL;
    IXpsOMSolidColorBrush         *xpsTextColor = NULL;
    XPS_COLOR                     xpsColorBodyText;
 
    // Create font stream.
    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
        fontFileName, &fontStream );
    
    // Create new obfuscated part name for this resource using a GUID.
    hr = CoCreateGuid( &fontNameGuid );
    hr = StringFromGUID2( 
            fontNameGuid, 
            guidString, 
            ARRAYSIZE(guidString));

    // Create a URI string for this font resource that will place 
    //  the font part in the /Resources/Fonts folder of the package.
    wcscpy_s(uriString, ARRAYSIZE(uriString), L"/Resources/Fonts/");

    // Create the part name using the GUID string as the name and 
    //  ".odttf" as the extension GUID string start and ends with 
    //  curly braces so they are removed.
    wcsncat_s(uriString, ARRAYSIZE(uriString), 
        guidString + 1, wcslen(guidString) - 2); 
    wcscat_s(uriString, ARRAYSIZE(uriString), L".odttf");

    // Create the font URI interface.
    hr = xpsFactory->CreatePartUri(
        uriString,
        &fontUri);
    // Create the font resource.
    hr = xpsFactory->CreateFontResource(
        fontStream,
        XPS_FONT_EMBEDDING_OBFUSCATED,
        fontUri,
        FALSE,     // isObfSourceStream
        &fontResource);
    if (NULL != fontUri) fontUri->Release();

    // Create the brush to use for the font.
    xpsColorBodyText.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColorBodyText.value.sRGB.alpha = 0xFF;
    xpsColorBodyText.value.sRGB.red = 0x00;
    xpsColorBodyText.value.sRGB.green = 0x00;
    xpsColorBodyText.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColorBodyText,
        NULL, // This color type does not use a color profile resource.             
        &xpsTextColor);

    // xpsTextColor is released after it has been used.
```



### <a name="draw-text-in-a-page"></a>Zeichnen von Text auf einer Seite

Im letzten Abschnitt des Code Beispiels werden die Symbole für jede Ausführung von ähnlich formatiertem Text erstellt. Um den Code in diesem letzten Abschnitt auszuführen, sind die **xpsfactory** -Schnittstelle sowie die Schriftart Ressource und ein Text Pinsel erforderlich und müssen instanziiert und initialisiert worden sein. In diesem Beispiel wird die im ersten Abschnitt beschriebene Funktion verwendet, um die ausgeführten Symbole zu erstellen und Sie der Seite hinzuzufügen.


```C++
    // The following interfaces are created outside of this example.

    // The page on which to place the text.
    IXpsOMPage                *page = NULL;

    // The object factory used by this program.
    IXpsOMObjectFactory       *xpsFactory = NULL;

    // The font resource created in the previous snippet.
    IXpsOMFontResource        *fontResource = NULL;

    // The color brush created in the previous snippet.
    IXpsOMSolidColorBrush     *xpsTextColor = NULL;

    // The following variables are defined outside of this example.

    // An array of pointers to the Unicode strings to write.
    LPCWSTR                   *textRuns = NULL;

    // An array of start points that correspond to the 
    //    strings in textRuns.
    XPS_POINT                 *startPoints = NULL;

    // The number of text runs to add to the page.
    UINT32                    numRuns = 0;            

    HRESULT                   hr = S_OK;

    FLOAT                     fontSize = 7.56f;
    UINT32                    thisRun;

    // Add all the text runs to the page.
    thisRun = 0;
    while (thisRun < numRuns) {  
        hr = WriteText_AddTextToPage(
            xpsFactory, 
            fontResource,
            fontSize,
            xpsTextColor,
            &startPoints[thisRun],
            textRuns[thisRun],
            page);
        thisRun++;
    }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Navigieren im XPS-OM](navigate-the-xps-om.md)
</dt> <dt>

[Zeichnen von Grafiken in einem XPS-OM](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Platzieren von Bildern in einem XPS-OM](place-images-in-an-xps-om.md)
</dt> <dt>

[Schreiben eines XPS-om in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Drucken eines XPS-OM](print-an-xps-om.md)
</dt> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**Iopcparamei**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**Ixpsomfontresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[**Ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[**Ixpsomglyphseditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[**Ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Ixpsomsolidcolorbrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**Ixpsomvisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
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

 

 
