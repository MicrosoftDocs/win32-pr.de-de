---
title: Rendern unter Verwendung eines benutzerdefinierten Textrenderers
description: Ein DirectWrite \ 160; Text Layout kann von einem benutzerdefinierten TextRenderer gezeichnet werden, der von idschreitetextrenderer abgeleitet wurde.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390601"
---
# <a name="render-using-a-custom-text-renderer"></a><span data-ttu-id="ae1d4-103">Rendern unter Verwendung eines benutzerdefinierten Textrenderers</span><span class="sxs-lookup"><span data-stu-id="ae1d4-103">Render Using a Custom Text Renderer</span></span>

<span data-ttu-id="ae1d4-104">Ein [DirectWrite](direct-write-portal.md)- [**Text Layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) kann von einem benutzerdefinierten TextRenderer gezeichnet werden, der von [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-104">A [DirectWrite](direct-write-portal.md) [**text layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) can be drawn by a custom text renderer derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="ae1d4-105">Ein benutzerdefinierter Renderer ist erforderlich, um einige erweiterte Features von DirectWrite zu nutzen, z. b. das Rendern einer Bitmap oder GDI-Oberfläche, von Inline Objekten und von Client Zeichnungs Effekten.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-105">A custom renderer is required to take advantage of some advanced features of DirectWrite, such as rendering to a bitmap or GDI surface, inline objects, and client drawing effects.</span></span> <span data-ttu-id="ae1d4-106">In diesem Tutorial werden die Methoden von **idschreitetextrenderer** beschrieben und eine Beispiel Implementierung bereitstellt, die [Direct2D](../direct2d/direct2d-portal.md) zum renderingtext mit einer Bitmap-Füllung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-106">This tutorial describes the methods of **IDWriteTextRenderer**, and provides an example implementation that uses [Direct2D](../direct2d/direct2d-portal.md) to render text with a bitmap fill.</span></span>

<span data-ttu-id="ae1d4-107">Dieses Tutorial enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="ae1d4-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="ae1d4-108">Der Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ae1d4-108">The Constructor</span></span>](#the-constructor)
-   [<span data-ttu-id="ae1d4-109">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-109">DrawGlyphRun()</span></span>](#drawglyphrun)
-   [<span data-ttu-id="ae1d4-110">Drawunder Line () und drawstrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-110">DrawUnderline() and DrawStrikethrough()</span></span>](#drawunderline-and-drawstrikethrough)
-   [<span data-ttu-id="ae1d4-111">Pixel-Snapping, Pixel pro DIP und Transformation</span><span class="sxs-lookup"><span data-stu-id="ae1d4-111">Pixel Snapping, Pixels per DIP, and Transform</span></span>](#pixel-snapping-pixels-per-dip-and-transform)
    -   [<span data-ttu-id="ae1d4-112">Ispixelsnappingdeaktiviert ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-112">IsPixelSnappingDisabled()</span></span>](#ispixelsnappingdisabled)
    -   [<span data-ttu-id="ae1d4-113">Getcurrenttransform ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-113">GetCurrentTransform()</span></span>](#getcurrenttransform)
    -   [<span data-ttu-id="ae1d4-114">Getpixelsperdip ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-114">GetPixelsPerDip()</span></span>](#getpixelsperdip)
-   [<span data-ttu-id="ae1d4-115">Drawinlineobject ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-115">DrawInlineObject()</span></span>](#drawinlineobject)
-   [<span data-ttu-id="ae1d4-116">Der Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="ae1d4-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="ae1d4-117">Verwenden des benutzerdefinierten textrenderers</span><span class="sxs-lookup"><span data-stu-id="ae1d4-117">Using the Custom Text Renderer</span></span>](#using-the-custom-text-renderer)

<span data-ttu-id="ae1d4-118">Der benutzerdefinierte TextRenderer muss die Methoden, die von IUnknown geerbt wurden, zusätzlich zu den Methoden implementieren, die auf der Referenzseite [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) und darunter aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-118">Your custom text renderer must implement the methods inherited from IUnknown in addition to the methods listed on the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page and below.</span></span>

<span data-ttu-id="ae1d4-119">Den vollständigen Quellcode für den benutzerdefinierten TextRenderer finden Sie in den Dateien "customtextrenderer. cpp" und "customtextrenderer. h" im [DirectWrite-Hallo Welt-Beispiel](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="ae1d4-119">For the full source code for the custom text renderer, see the CustomTextRenderer.cpp and CustomTextRenderer.h files of the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="the-constructor"></a><span data-ttu-id="ae1d4-120">Der Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ae1d4-120">The Constructor</span></span>

<span data-ttu-id="ae1d4-121">Der benutzerdefinierte TextRenderer benötigt einen Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-121">Your custom text renderer will need a constructor.</span></span> <span data-ttu-id="ae1d4-122">In diesem Beispiel werden sowohl Solid-als auch Bitmap- [Direct2D](../direct2d/direct2d-portal.md) Pinsel verwendet, um den Text zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-122">This example uses both solid and bitmap [Direct2D](../direct2d/direct2d-portal.md) brushes to render the text.</span></span>

<span data-ttu-id="ae1d4-123">Aus diesem Grund übernimmt der Konstruktor die in der Tabelle unten gefundenen Parameter mit Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-123">Because of this, the constructor takes the parameters found in the table below with descriptions.</span></span>



| <span data-ttu-id="ae1d4-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae1d4-124">Parameter</span></span>       | <span data-ttu-id="ae1d4-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae1d4-125">Description</span></span>                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1d4-126">*pD2DFactory*</span><span class="sxs-lookup"><span data-stu-id="ae1d4-126">*pD2DFactory*</span></span>   | <span data-ttu-id="ae1d4-127">Ein Zeiger auf ein [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt, das verwendet wird, um alle benötigten Direct2D-Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-127">A pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create any Direct2D resources that are needed.</span></span>                                                                                                        |
| <span data-ttu-id="ae1d4-128">*PRT*</span><span class="sxs-lookup"><span data-stu-id="ae1d4-128">*pRT*</span></span>           | <span data-ttu-id="ae1d4-129">Ein Zeiger auf das [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekt, in dem der Text gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-129">A pointer to the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object that the text will be rendered to.</span></span> |
| <span data-ttu-id="ae1d4-130">*poutlinebrush*</span><span class="sxs-lookup"><span data-stu-id="ae1d4-130">*pOutlineBrush*</span></span> | <span data-ttu-id="ae1d4-131">Ein Zeiger auf die [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) , die zum Zeichnen des Texts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-131">A pointer to the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) that will be use to draw outline of the text</span></span>                                                                                                                     |
| <span data-ttu-id="ae1d4-132">*pfillbrush*</span><span class="sxs-lookup"><span data-stu-id="ae1d4-132">*pFillBrush*</span></span>    | <span data-ttu-id="ae1d4-133">Ein Zeiger auf die [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , die verwendet wird, um den Text auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-133">A pointer to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that will be used to fill the text.</span></span>                                                                                                                                      |



 

<span data-ttu-id="ae1d4-134">Diese werden vom-Konstruktor gespeichert, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-134">These will be stored by the constructor as shown in the following code.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a><span data-ttu-id="ae1d4-135">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-135">DrawGlyphRun()</span></span>

<span data-ttu-id="ae1d4-136">Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode ist die Haupt Rückruf Methode des textrenderers.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-136">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method is the main callback method of the text renderer.</span></span> <span data-ttu-id="ae1d4-137">Es wird ein Ausführen von Symbolen, die gerendert werden sollen, sowie Informationen wie der Basis Linien Ursprung und der Mess Modus übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-137">It is passed a run of glyphs to be rendered in addition to information such as the baseline origin and measuring mode.</span></span> <span data-ttu-id="ae1d4-138">Außerdem übergibt Sie ein Client Zeichnungs Effekt-Objekt, das auf das Symbol "ausführen" angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-138">It also passes a client drawing effect object to be applied to the glyph run.</span></span> <span data-ttu-id="ae1d4-139">Weitere Informationen finden Sie im Thema [Hinzufügen von Client Zeichnungs Effekten zu einem Textlayout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="ae1d4-139">For more information, see the [How to Add Client Drawing Effects to a Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) topic.</span></span>

<span data-ttu-id="ae1d4-140">Diese Implementierung des textrenderers rendert Glyphe, indem Sie in [Direct2D](rendering-by-using-direct2d.md) Geometrien und anschließend die Geometrien gezeichnet und gefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-140">This text renderer implementation renders glyph runs by converting them to [Direct2D](rendering-by-using-direct2d.md) geometries and then drawing and filling the geometries.</span></span> <span data-ttu-id="ae1d4-141">Dies umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="ae1d4-141">This consists of the following steps.</span></span>

1.  <span data-ttu-id="ae1d4-142">Erstellen Sie ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Objekt, und rufen Sie dann das [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) -Objekt mithilfe der [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-142">Create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object, and then retrieve the [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) object by using the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  <span data-ttu-id="ae1d4-143">Die an [**DrawGlyphRun an DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) über gegebene [**dwrite- \_ Glyphe \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) enthält ein [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt mit dem Namen *fontface*, das die Schriftart für die gesamte Symbol Ausführung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-143">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the whole glyph run.</span></span> <span data-ttu-id="ae1d4-144">Fügen Sie den Umriss des Symbols in die Geometrie-Senke ein, indem Sie die [**idwrite-fontface:: getglyphrunoutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) -Methode verwenden, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-144">Put the outline of the glyph run into the geometry sink by using the [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, as shown in the following code.</span></span>

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  <span data-ttu-id="ae1d4-145">Nachdem Sie die Geometry-Senke ausgefüllt haben, schließen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-145">After filling the geometry sink, close it.</span></span>

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  <span data-ttu-id="ae1d4-146">Der Ursprung der Glyphe muss übersetzt werden, damit er aus dem richtigen Baseline-Ursprung gerendert wird, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-146">The origin of the glyph run must be translated so that it is rendered from the correct baseline origin, as shown in the following code.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    <span data-ttu-id="ae1d4-147">*Baselineoriginx* und *baselineoriginy* werden als Parameter an die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Rückruf Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-147">The *baselineOriginX* and *baselineOriginY* are passed as parameters to the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback method.</span></span>

5.  <span data-ttu-id="ae1d4-148">Erstellen Sie die transformierte Geometrie mithilfe der [**ID2D1Factory:: deatetransformedgeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) -Methode, und übergeben Sie die Pfad Geometrie und die Übersetzungs Matrix.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-148">Create the transformed geometry by using the [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method and passing the path geometry and the translation matrix.</span></span>

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  <span data-ttu-id="ae1d4-149">Zeichnen Sie schließlich den Umriss der transformierten Geometrie, und füllen Sie ihn mit den [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -und [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methoden und den [Direct2D](../direct2d/direct2d-portal.md) -Pinseln, die als Element Variablen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-149">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  <span data-ttu-id="ae1d4-150">Nachdem Sie das Zeichnen abgeschlossen haben, sollten Sie nicht vergessen, die Objekte zu bereinigen, die in dieser Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-150">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a><span data-ttu-id="ae1d4-151">Drawunder Line () und drawstrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-151">DrawUnderline() and DrawStrikethrough()</span></span>

<span data-ttu-id="ae1d4-152">[**Idwrite tetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) verfügt auch über Rückrufe zum Zeichnen der Unterstreichung und durchgestrichen.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) also has callbacks for drawing the underline and strikethrough.</span></span> <span data-ttu-id="ae1d4-153">In diesem Beispiel wird ein einfaches Rechteck für eine Unterstreichung oder durchgestrichen gezeichnet, aber andere Formen können gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-153">This example draws a simple rectangle for an underline or strikethrough, but other shapes can be drawn.</span></span>

<span data-ttu-id="ae1d4-154">Das Zeichnen einer Unterstreichung mithilfe von [Direct2D](../direct2d/direct2d-portal.md) besteht aus den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-154">Drawing an underline by using [Direct2D](../direct2d/direct2d-portal.md) consists of the following steps.</span></span>

1.  <span data-ttu-id="ae1d4-155">Erstellen Sie zuerst eine [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) -Struktur der Größe und Form der Unterstreichung.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-155">First, create a [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure of the size and shape of the underline.</span></span> <span data-ttu-id="ae1d4-156">Die [**dwrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) -Unterstreichung-Struktur, die an die [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) -Rückruf Methode übermittelt wird, bietet den Offset, die Breite und die Stärke der Unterstreichung.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-156">The [**DWRITE\_UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) structure that is passed to the [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) callback method provides the offset, width, and thickness of the underline.</span></span>

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  <span data-ttu-id="ae1d4-157">Erstellen Sie als nächstes ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) -Objekt, indem Sie die [**ID2D1Factory:: kreaterectanglegeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) -Methode und die initialisierte [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) -Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-157">Next, create an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object by using the [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) method and the initialized [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure.</span></span>

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  <span data-ttu-id="ae1d4-158">Wie bei der Symbol Führung muss der Ursprung der unterstrichsgeometrie mithilfe der Methode " [**kreatetransformedgeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) " basierend auf den Baseline-Ursprungs Werten übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-158">As with the glyph run, the origin of the underline geometry must be translated, based on the baseline origin values, by using the [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  <span data-ttu-id="ae1d4-159">Zeichnen Sie schließlich den Umriss der transformierten Geometrie, und füllen Sie ihn mit den [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -und [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methoden und den [Direct2D](../direct2d/direct2d-portal.md) -Pinseln, die als Element Variablen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-159">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  <span data-ttu-id="ae1d4-160">Nachdem Sie das Zeichnen abgeschlossen haben, sollten Sie nicht vergessen, die Objekte zu bereinigen, die in dieser Methode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-160">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

<span data-ttu-id="ae1d4-161">Der Prozess zum Zeichnen eines durchgestrichen ist identisch.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-161">The process for drawing a strikethrough is the same.</span></span> <span data-ttu-id="ae1d4-162">Allerdings hat das durchgestrichen eine andere Abweichung und wahrscheinlich eine andere Breite und Stärke.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-162">However, the strikethrough will have a different offset, and likely a different width and thickness.</span></span>

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a><span data-ttu-id="ae1d4-163">Pixel-Snapping, Pixel pro DIP und Transformation</span><span class="sxs-lookup"><span data-stu-id="ae1d4-163">Pixel Snapping, Pixels per DIP, and Transform</span></span>

### <a name="ispixelsnappingdisabled"></a><span data-ttu-id="ae1d4-164">Ispixelsnappingdeaktiviert ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-164">IsPixelSnappingDisabled()</span></span>

<span data-ttu-id="ae1d4-165">Diese Methode wird aufgerufen, um zu bestimmen, ob das Ausrichten von Pixeln deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-165">This method is called to determine whether pixel snapping is disabled.</span></span> <span data-ttu-id="ae1d4-166">Der empfohlene Standardwert ist **false**. Dies ist die Ausgabe dieses Beispiels.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-166">The recommended default is **FALSE**, and that is the output of this example.</span></span>


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a><span data-ttu-id="ae1d4-167">Getcurrenttransform ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-167">GetCurrentTransform()</span></span>

<span data-ttu-id="ae1d4-168">In diesem Beispiel wird in ein Direct2D-Renderziel gerendert, sodass die Transformation vom Renderziel mithilfe von [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform)weiterleiten soll.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-168">This example renders to a Direct2D render target, so forward the transform from the render target using [**ID2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span></span>


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a><span data-ttu-id="ae1d4-169">Getpixelsperdip ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-169">GetPixelsPerDip()</span></span>

<span data-ttu-id="ae1d4-170">Diese Methode wird aufgerufen, um die Anzahl der Pixel pro geräteunabhängigen Pixel (DIP) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-170">This method is called to get the number of pixels per Device Independent Pixel (DIP).</span></span>


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a><span data-ttu-id="ae1d4-171">Drawinlineobject ()</span><span class="sxs-lookup"><span data-stu-id="ae1d4-171">DrawInlineObject()</span></span>

<span data-ttu-id="ae1d4-172">Ein benutzerdefinierter TextRenderer verfügt auch über einen Rückruf zum Zeichnen von Inline Objekten.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-172">A custom text renderer also has a callback for drawing inline objects.</span></span> <span data-ttu-id="ae1d4-173">In diesem Beispiel gibt [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-173">In this example, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) returns E\_NOTIMPL.</span></span> <span data-ttu-id="ae1d4-174">Eine Erläuterung zum Zeichnen von Inline Objekten geht über den Rahmen dieses Tutorials hinaus.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-174">An explanation of how to draw inline objects is beyond the scope of this tutorial.</span></span> <span data-ttu-id="ae1d4-175">Weitere Informationen finden Sie im Thema Vorgehens [Weise beim Hinzufügen von Inline Objekten zu einem Text Layout](how-to-add-inline-objects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="ae1d4-175">For more information, see the [How to Add Inline Objects to a Text Layout](how-to-add-inline-objects-to-a-text-layout.md) topic.</span></span>

## <a name="the-destructor"></a><span data-ttu-id="ae1d4-176">Der Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="ae1d4-176">The Destructor</span></span>

<span data-ttu-id="ae1d4-177">Es ist wichtig, alle Zeiger freizugeben, die von der benutzerdefinierten TextRenderer-Klasse verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-177">It is important to release any pointers that were used by the custom text renderer class.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a><span data-ttu-id="ae1d4-178">Verwenden des benutzerdefinierten textrenderers</span><span class="sxs-lookup"><span data-stu-id="ae1d4-178">Using the Custom Text Renderer</span></span>

<span data-ttu-id="ae1d4-179">Sie werden mit dem benutzerdefinierten Renderer mithilfe der [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode gerengt, die eine von [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) abgeleitete Rückruf Schnittstelle als Argument annimmt, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-179">You render with the custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="ae1d4-180">Die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode ruft die Methoden des von Ihnen bereitgestellten benutzerdefinierten rendererrückrufs auf.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-180">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="ae1d4-181">Die oben beschriebenen Methoden [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)und [**drawstrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) führen die Zeichnungsfunktionen aus.</span><span class="sxs-lookup"><span data-stu-id="ae1d4-181">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods described above perform the drawing functions.</span></span>

 

 