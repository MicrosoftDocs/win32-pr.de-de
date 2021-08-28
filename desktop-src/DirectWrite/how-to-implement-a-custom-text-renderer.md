---
title: Rendern unter Verwendung eines benutzerdefinierten Textrenderers
description: Ein DirectWrite \ 160;Textlayout kann von einem benutzerdefinierten Textrenderer gezeichnet werden, der von IDWriteTextRenderer abgeleitet wird.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f8e08bb8af3ce7fa0ae4d423103feb597e17cf46ab53b42903fad143c675db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902874"
---
# <a name="render-using-a-custom-text-renderer"></a>Rendern unter Verwendung eines benutzerdefinierten Textrenderers

Ein [DirectWrite](direct-write-portal.md) [**Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) kann von einem benutzerdefinierten Textrenderer gezeichnet werden, der von [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)abgeleitet wird. Ein benutzerdefinierter Renderer ist erforderlich, um einige erweiterte Features von DirectWrite zu nutzen, z. B. das Rendern auf einer Bitmap- oder GDI-Oberfläche, Inlineobjekte und Clientzeichnungseffekte. Dieses Tutorial beschreibt die Methoden von **IDWriteTextRenderer** und stellt eine Beispielimplementierung bereit, die [Direct2D](../direct2d/direct2d-portal.md) verwendet, um Text mit einer Bitmapfüllung zu rendern.

Dieses Tutorial enthält die folgenden Teile:

-   [Der Konstruktor](#the-constructor)
-   [DrawGlyphRun()](#drawglyphrun)
-   [DrawUnderline() und DrawStrikethrough()](#drawunderline-and-drawstrikethrough)
-   [Pixel-Ausrichtung, Pixel pro DIP und Transformation](#pixel-snapping-pixels-per-dip-and-transform)
    -   [IsPixelSnappingDisabled()](#ispixelsnappingdisabled)
    -   [GetCurrentTransform()](#getcurrenttransform)
    -   [GetPixelsPerDip()](#getpixelsperdip)
-   [DrawInlineObject()](#drawinlineobject)
-   [Der Destruktor](#the-destructor)
-   [Verwenden des benutzerdefinierten Textrenderers](#using-the-custom-text-renderer)

Ihr benutzerdefinierter Textrenderer muss die von IUnknown geerbten Methoden zusätzlich zu den Methoden implementieren, die auf der [**Referenzseite IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) und unten aufgeführt sind.

Den vollständigen Quellcode für den benutzerdefinierten Textrenderer finden Sie in den Dateien CustomTextRenderer.cpp und CustomTextRenderer.h des [DirectWrite Hallo Welt Beispiels](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="the-constructor"></a>Der Konstruktor

Ihr benutzerdefinierter Textrenderer benötigt einen Konstruktor. In diesem Beispiel werden sowohl einfarbige als auch [Bitmap-Direct2D-Pinsel](../direct2d/direct2d-portal.md) verwendet, um den Text zu rendern.

Aus diesem Grund verwendet der Konstruktor die Parameter aus der folgenden Tabelle mit Beschreibungen.



| Parameter       | BESCHREIBUNG                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | Ein Zeiger auf ein [**ID2D1Factory-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) mit dem alle benötigten Direct2D-Ressourcen erstellt werden.                                                                                                        |
| *Prt*           | Ein Zeiger auf das [**ID2D1HwndRenderTarget-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) in das der Text gerendert wird. |
| *pOutlineBrush* | Ein Zeiger auf den [**ID2D1SolidColorBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) der zum Zeichnen der Kontur des Texts verwendet wird.                                                                                                                     |
| *pFillBrush*    | Ein Zeiger auf den [**ID2D1BitmapBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) der zum Ausfüllen des Texts verwendet wird.                                                                                                                                      |



 

Diese werden vom Konstruktor gespeichert, wie im folgenden Code gezeigt.


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



## <a name="drawglyphrun"></a>DrawGlyphRun()

Die [**DrawGlyphRun-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) ist die Hauptrückrufmethode des Textrenderers. Es wird eine Ausführung von Glyphen übergeben, die zusätzlich zu Informationen wie dem Baselineursprung und dem Messmodus gerendert werden sollen. Außerdem wird ein Client-Zeichnungseffektobjekt übergeben, das auf die Glyphen-Ausführung angewendet werden soll. Weitere Informationen finden Sie im Thema [Hinzufügen von Clientzeichnungseffekten zu einem Textlayout.](how-to-add-custom-drawing-efffects-to-a-text-layout.md)

Diese Textrendererimplementierung rendert Glyphenausführungen, indem sie sie in [Direct2D-Geometrien](rendering-by-using-direct2d.md) konvertiert und dann die Geometrien zeichnen und füllen. Dies umfasst die folgenden Schritte.

1.  Erstellen Sie ein [**ID2D1PathGeometry-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) und rufen Sie dann das [**ID2D1GeometrySink-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) mithilfe der [**ID2D1PathGeometry::Open-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) ab.

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

    

2.  Die [**\_ DWRITE-GLYPH-AUSFÜHRUNG, \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) die an [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) übergeben wird, enthält ein [**IDWriteFontFace-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) namens *fontFace,* das das Schriftartgesicht für die gesamte Glyphenrun darstellt. Legen Sie die Kontur des Glyphenlaufs wie im folgenden Code gezeigt mithilfe der [**IDWriteFontFace:: GetGlyphRunOutline-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) in die geometry-Senke ein.

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

    

3.  Schließen Sie die Geometriesenke, nachdem Sie sie gefüllt haben.

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  Der Ursprung der Glyphenlauf muss übersetzt werden, damit er vom richtigen Baselineursprung gerendert wird, wie im folgenden Code gezeigt.

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *BaselineOriginX* und *baselineOriginY* werden als Parameter an die [**DrawGlyphRun-Rückrufmethode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) übergeben.

5.  Erstellen Sie die transformierte Geometrie mithilfe der [**ID2D1Factory::CreateTransformedGeometry-Methode,**](../direct2d/id2d1factory-createtransformedgeometry.md) und übergeben Sie die Pfadgeometrie und die Übersetzungsmatrix.

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

    

6.  Zeichnen Sie abschließend die Kontur der transformierten Geometrie, und füllen Sie sie mithilfe der Methoden [**ID2D1RenderTarget::D rawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) und [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) und der [Direct2D-Pinsel,](../direct2d/direct2d-portal.md) die als Membervariablen gespeichert sind.

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

    

7.  Nachdem Sie das Zeichnen abgeschlossen haben, vergessen Sie nicht, die Objekte zu bereinigen, die in dieser Methode erstellt wurden.

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>DrawUnderline() und DrawStrikethrough()

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) verfügt auch über Rückrufe zum Zeichnen der Unterstreichung und des Durchstrichs. In diesem Beispiel wird ein einfaches Rechteck für eine Unterstreichung oder einen Durchstrich gezeichnet, aber andere Formen können gezeichnet werden.

Das Zeichnen einer Unterstreichung mit [Direct2D](../direct2d/direct2d-portal.md) besteht aus den folgenden Schritten.

1.  Erstellen Sie zunächst eine [**D2D1 \_ RECT \_ F-Struktur**](../direct2d/d2d1-rect-f.md) der Größe und Form der Unterstreichung. Die [**DWRITE \_ UNDERLINE-Struktur,**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) die an die [**DrawUnderline-Rückrufmethode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) übergeben wird, stellt den Offset, die Breite und die Stärke der Unterstreichung bereit.

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  Erstellen Sie als Nächstes ein [**ID2D1RectangleGeometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) mithilfe der [**ID2D1Factory::CreateRectangleGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) und der initialisierten [**D2D1 \_ RECT \_ F-Struktur.**](../direct2d/d2d1-rect-f.md)

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  Wie beim Glyphenlauf muss der Ursprung der Unterstreichungsgeometrie basierend auf den Basisursprungswerten mithilfe der [**CreateTransformedGeometry-Methode**](../direct2d/id2d1factory-createtransformedgeometry.md) übersetzt werden.

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

    

4.  Zeichnen Sie abschließend die Kontur der transformierten Geometrie, und füllen Sie sie mithilfe der Methoden [**ID2D1RenderTarget::D rawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) und [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) und der [Direct2D-Pinsel,](../direct2d/direct2d-portal.md) die als Membervariablen gespeichert sind.

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

    

5.  Nachdem Sie das Zeichnen abgeschlossen haben, vergessen Sie nicht, die Objekte zu bereinigen, die in dieser Methode erstellt wurden.

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

Der Prozess zum Zeichnen eines durchgestrichenen Vorgangs ist identisch. Der Durchstrich hat jedoch einen anderen Offset und wahrscheinlich eine andere Breite und Stärke.

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>Pixel-Ausrichtung, Pixel pro DIP und Transformation

### <a name="ispixelsnappingdisabled"></a>IsPixelSnappingDisabled()

Diese Methode wird aufgerufen, um zu bestimmen, ob das Pixel-Snapping deaktiviert ist. Der empfohlene Standardwert ist **FALSE,** und dies ist die Ausgabe dieses Beispiels.


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>GetCurrentTransform()

In diesem Beispiel wird in ein Direct2D-Renderziel gerendert. Leiten Sie daher die Transformation mit [**id2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform)vom Renderziel weiter.


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>GetPixelsPerDip()

Diese Methode wird aufgerufen, um die Anzahl der Pixel pro geräteunabhängiges Pixel (Device Independent Pixel, DIP) abzurufen.


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>DrawInlineObject()

Ein benutzerdefinierter Textrenderer verfügt auch über einen Rückruf zum Zeichnen von Inlineobjekten. In diesem Beispiel gibt [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) E \_ NOTIMPL zurück. Eine Erläuterung des Zeichnens von Inlineobjekten würde den Rahmen dieses Tutorials sprengen. Weitere Informationen finden Sie im Thema [Hinzufügen von Inlineobjekten zu einem Textlayout.](how-to-add-inline-objects-to-a-text-layout.md)

## <a name="the-destructor"></a>Der Destruktor

Es ist wichtig, alle Zeiger freizugeben, die von der benutzerdefinierten Textrendererklasse verwendet wurden.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>Verwenden des benutzerdefinierten Textrenderers

Sie rendern mit dem benutzerdefinierten Renderer mithilfe der [**IDWriteTextLayout::D raw-Methode,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) die eine von [**IDWriteTextRenderer abgeleitete**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) Rückrufschnittstelle als Argument verwendet, wie im folgenden Code gezeigt.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Die [**IDWriteTextLayout::D raw-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) ruft die Methoden des von Ihnen bereitzustellenden benutzerdefinierten Rendererrückrufs auf. Die oben [**beschriebenen DrawGlyphRun-,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) [**DrawUnderline-,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) [**DrawInlineObject-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)und [**DrawStrikethrough-Methoden**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) führen die Zeichnungsfunktionen aus.

 

 