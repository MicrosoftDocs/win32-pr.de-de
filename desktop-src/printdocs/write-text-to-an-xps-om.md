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
# <a name="write-text-to-an-xps-om"></a><span data-ttu-id="36070-103">Schreiben von Text in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="36070-103">Write Text to an XPS OM</span></span>

<span data-ttu-id="36070-104">In diesem Thema wird beschrieben, wie Text in ein XPS-OM geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="36070-104">This topic describes how to write text to an XPS OM.</span></span>

<span data-ttu-id="36070-105">Der Text wird in ein XPS-OM eingefügt, indem eine [**ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) -Schnittstelle erstellt und formatiert und dann die **ixpsomglyphs** -Schnittstelle zur Liste der visuellen Objekte der Seite oder Canvas hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="36070-105">Text is placed in an XPS OM by creating and formatting an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface and then adding the **IXpsOMGlyphs** interface to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="36070-106">Jede **ixpsomglyphs** -Schnittstelle stellt eine Symbol Führung dar, bei der es sich um eine fortlaufende Zeichenfolge handelt, die ein gemeinsames Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="36070-106">Each **IXpsOMGlyphs** interface represents a glyph run, which is a continuous run of characters that share a common format.</span></span> <span data-ttu-id="36070-107">Wenn sich ein Zeichenformat Element (z. b. Schriftart Type oder size) ändert oder wenn ein Zeilenumbruch durchgeführt wird, muss eine neue **ixpsomglyphs** -Schnittstelle erstellt und der Liste der visuellen Objekte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="36070-107">When a character format element (such as font type or size) changes or when a line breaks, a new **IXpsOMGlyphs** interface must be created and added to the list of visual objects.</span></span>

<span data-ttu-id="36070-108">Einige der Eigenschaften einer Glyphe können mithilfe der Methoden der [**ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) -Schnittstelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="36070-108">Some of the properties of a glyph run can be set by using the methods of the [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface.</span></span> <span data-ttu-id="36070-109">Einige Eigenschaften interagieren jedoch mit anderen und müssen mithilfe einer [**ixpsomglyphseditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) -Schnittstelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="36070-109">Some properties, however, interact with others and must be set by using an [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) interface.</span></span>

<span data-ttu-id="36070-110">Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="36070-110">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="36070-111">Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="36070-111">Code Example</span></span>

### <a name="create-a-glyph-run-from-a-string"></a><span data-ttu-id="36070-112">Erstellen eines Symbols, das aus einer Zeichenfolge ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="36070-112">Create a glyph run from a string</span></span>

<span data-ttu-id="36070-113">Eine Symbol Führung wird häufig in mehreren Schritten erstellt, die das Laden der Schriftart Ressourcen, die von der Symbol Suche verwendet werden, das Festlegen eines Füll Pinsel, das Festlegen des Schrift Grads und des Start Orts sowie das Festlegen der Unicode-Zeichenfolge beinhalten.</span><span class="sxs-lookup"><span data-stu-id="36070-113">A glyph run is commonly created in several steps that include loading the font resources that are used by the glyph run, setting a fill brush, specifying the font size and starting location, and setting the Unicode string.</span></span>

<span data-ttu-id="36070-114">Der folgende Abschnitt des Code Beispiels enthält eine Routine, die einige Variablen annimmt, einschließlich Schriftart Größe, Farbe und Position sowie der zu schreibenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="36070-114">The following section of the code example contains a routine that accepts some variables, including the font size, color and location, and the characters to be written.</span></span> <span data-ttu-id="36070-115">Der Code erstellt dann ein Symbol, das ausgeführt wird, und fügt es einer Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="36070-115">The code then creates a glyph run and then adds it to a page.</span></span> <span data-ttu-id="36070-116">Im Codebeispiel wird davon ausgegangen, dass die in [Initialisieren eines XPS-OMS](xps-object-model-initialization.md) beschriebene Initialisierung aufgetreten ist und dass das Dokument mindestens eine Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="36070-116">The code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has occurred and that the document has at least one page.</span></span> <span data-ttu-id="36070-117">Weitere Informationen zum Erstellen eines leeren XPS-OMS finden Sie unter [Erstellen eines leeren XPS-OMS](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="36070-117">For more information about creating a blank XPS OM, refer to [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


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



### <a name="load-and-create-resources"></a><span data-ttu-id="36070-118">Laden und Erstellen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="36070-118">Load and create resources</span></span>

<span data-ttu-id="36070-119">Die Erstellung einer [**ixpsomglyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) -Schnittstelle erfordert eine Schriftart Ressource.</span><span class="sxs-lookup"><span data-stu-id="36070-119">Creation of an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface requires a font resource.</span></span> <span data-ttu-id="36070-120">In vielen Fällen verwendet ein TextBlock die gleiche Schriftart und Farbe.</span><span class="sxs-lookup"><span data-stu-id="36070-120">In many cases, a block of text uses the same font and color.</span></span> <span data-ttu-id="36070-121">Daher werden in diesem Abschnitt des Code Beispiels die Schriftart Ressourcen Schnittstellen erstellt, die in den Aufrufen verwendet werden, die den Text auf der Seite platzieren.</span><span class="sxs-lookup"><span data-stu-id="36070-121">Hence, this section of the code example will create the font resource interfaces that will be used in the calls that place the text on the page.</span></span>


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



### <a name="draw-text-in-a-page"></a><span data-ttu-id="36070-122">Zeichnen von Text auf einer Seite</span><span class="sxs-lookup"><span data-stu-id="36070-122">Draw text in a page</span></span>

<span data-ttu-id="36070-123">Im letzten Abschnitt des Code Beispiels werden die Symbole für jede Ausführung von ähnlich formatiertem Text erstellt.</span><span class="sxs-lookup"><span data-stu-id="36070-123">The final section of the code example creates the glyph runs for each run of similarly formatted text.</span></span> <span data-ttu-id="36070-124">Um den Code in diesem letzten Abschnitt auszuführen, sind die **xpsfactory** -Schnittstelle sowie die Schriftart Ressource und ein Text Pinsel erforderlich und müssen instanziiert und initialisiert worden sein.</span><span class="sxs-lookup"><span data-stu-id="36070-124">To execute the code in this final section, the **xpsFactory** interface as well as the font resource and a text color brush are necessary and must have been instantiated and initialized.</span></span> <span data-ttu-id="36070-125">In diesem Beispiel wird die im ersten Abschnitt beschriebene Funktion verwendet, um die ausgeführten Symbole zu erstellen und Sie der Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="36070-125">In this example, the function described in the first section is used to create the glyph runs and to add them to the page.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="36070-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36070-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="36070-127">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="36070-127">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="36070-128">Navigieren im XPS-OM</span><span class="sxs-lookup"><span data-stu-id="36070-128">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="36070-129">Zeichnen von Grafiken in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="36070-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="36070-130">Platzieren von Bildern in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="36070-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="36070-131">Schreiben eines XPS-om in ein XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="36070-131">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="36070-132">Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="36070-132">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="36070-133">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="36070-133">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="36070-134">**Iopcparamei**</span><span class="sxs-lookup"><span data-stu-id="36070-134">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="36070-135">**Ixpsomfontresource**</span><span class="sxs-lookup"><span data-stu-id="36070-135">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="36070-136">**Ixpsomglyphs**</span><span class="sxs-lookup"><span data-stu-id="36070-136">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[<span data-ttu-id="36070-137">**Ixpsomglyphseditor**</span><span class="sxs-lookup"><span data-stu-id="36070-137">**IXpsOMGlyphsEditor**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[<span data-ttu-id="36070-138">**Ixpsomobjectfactory**</span><span class="sxs-lookup"><span data-stu-id="36070-138">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="36070-139">**Ixpsompage**</span><span class="sxs-lookup"><span data-stu-id="36070-139">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="36070-140">**Ixpsomsolidcolorbrush**</span><span class="sxs-lookup"><span data-stu-id="36070-140">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="36070-141">**Ixpsomvisual**</span><span class="sxs-lookup"><span data-stu-id="36070-141">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="36070-142">**Ixpsomvisualcollection**</span><span class="sxs-lookup"><span data-stu-id="36070-142">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="36070-143">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="36070-143">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="36070-144">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="36070-144">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="36070-145">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="36070-145">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="36070-146">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="36070-146">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
