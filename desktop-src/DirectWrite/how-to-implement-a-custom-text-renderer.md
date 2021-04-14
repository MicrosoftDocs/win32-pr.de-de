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
# <a name="render-using-a-custom-text-renderer"></a>Rendern unter Verwendung eines benutzerdefinierten Textrenderers

Ein [DirectWrite](direct-write-portal.md)- [**Text Layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) kann von einem benutzerdefinierten TextRenderer gezeichnet werden, der von [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)abgeleitet wurde. Ein benutzerdefinierter Renderer ist erforderlich, um einige erweiterte Features von DirectWrite zu nutzen, z. b. das Rendern einer Bitmap oder GDI-Oberfläche, von Inline Objekten und von Client Zeichnungs Effekten. In diesem Tutorial werden die Methoden von **idschreitetextrenderer** beschrieben und eine Beispiel Implementierung bereitstellt, die [Direct2D](../direct2d/direct2d-portal.md) zum renderingtext mit einer Bitmap-Füllung verwendet.

Dieses Tutorial enthält die folgenden Teile:

-   [Der Konstruktor](#the-constructor)
-   [DrawGlyphRun ()](#drawglyphrun)
-   [Drawunder Line () und drawstrikethrough ()](#drawunderline-and-drawstrikethrough)
-   [Pixel-Snapping, Pixel pro DIP und Transformation](#pixel-snapping-pixels-per-dip-and-transform)
    -   [Ispixelsnappingdeaktiviert ()](#ispixelsnappingdisabled)
    -   [Getcurrenttransform ()](#getcurrenttransform)
    -   [Getpixelsperdip ()](#getpixelsperdip)
-   [Drawinlineobject ()](#drawinlineobject)
-   [Der Dekonstruktor](#the-destructor)
-   [Verwenden des benutzerdefinierten textrenderers](#using-the-custom-text-renderer)

Der benutzerdefinierte TextRenderer muss die Methoden, die von IUnknown geerbt wurden, zusätzlich zu den Methoden implementieren, die auf der Referenzseite [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) und darunter aufgeführt sind.

Den vollständigen Quellcode für den benutzerdefinierten TextRenderer finden Sie in den Dateien "customtextrenderer. cpp" und "customtextrenderer. h" im [DirectWrite-Hallo Welt-Beispiel](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="the-constructor"></a>Der Konstruktor

Der benutzerdefinierte TextRenderer benötigt einen Konstruktor. In diesem Beispiel werden sowohl Solid-als auch Bitmap- [Direct2D](../direct2d/direct2d-portal.md) Pinsel verwendet, um den Text zu erzeugen.

Aus diesem Grund übernimmt der Konstruktor die in der Tabelle unten gefundenen Parameter mit Beschreibungen.



| Parameter       | BESCHREIBUNG                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | Ein Zeiger auf ein [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt, das verwendet wird, um alle benötigten Direct2D-Ressourcen zu erstellen.                                                                                                        |
| *PRT*           | Ein Zeiger auf das [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekt, in dem der Text gerendert wird. |
| *poutlinebrush* | Ein Zeiger auf die [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) , die zum Zeichnen des Texts verwendet wird.                                                                                                                     |
| *pfillbrush*    | Ein Zeiger auf die [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , die verwendet wird, um den Text auszufüllen.                                                                                                                                      |



 

Diese werden vom-Konstruktor gespeichert, wie im folgenden Code gezeigt.


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



## <a name="drawglyphrun"></a>DrawGlyphRun ()

Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode ist die Haupt Rückruf Methode des textrenderers. Es wird ein Ausführen von Symbolen, die gerendert werden sollen, sowie Informationen wie der Basis Linien Ursprung und der Mess Modus übermittelt. Außerdem übergibt Sie ein Client Zeichnungs Effekt-Objekt, das auf das Symbol "ausführen" angewendet werden soll. Weitere Informationen finden Sie im Thema [Hinzufügen von Client Zeichnungs Effekten zu einem Textlayout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .

Diese Implementierung des textrenderers rendert Glyphe, indem Sie in [Direct2D](rendering-by-using-direct2d.md) Geometrien und anschließend die Geometrien gezeichnet und gefüllt werden. Dies umfasst die folgenden Schritte:

1.  Erstellen Sie ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Objekt, und rufen Sie dann das [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) -Objekt mithilfe der [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode ab.

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

    

2.  Die an [**DrawGlyphRun an DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) über gegebene [**dwrite- \_ Glyphe \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) enthält ein [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt mit dem Namen *fontface*, das die Schriftart für die gesamte Symbol Ausführung darstellt. Fügen Sie den Umriss des Symbols in die Geometrie-Senke ein, indem Sie die [**idwrite-fontface:: getglyphrunoutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) -Methode verwenden, wie im folgenden Code gezeigt.

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

    

3.  Nachdem Sie die Geometry-Senke ausgefüllt haben, schließen Sie Sie.

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  Der Ursprung der Glyphe muss übersetzt werden, damit er aus dem richtigen Baseline-Ursprung gerendert wird, wie im folgenden Code gezeigt.

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *Baselineoriginx* und *baselineoriginy* werden als Parameter an die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Rückruf Methode übermittelt.

5.  Erstellen Sie die transformierte Geometrie mithilfe der [**ID2D1Factory:: deatetransformedgeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) -Methode, und übergeben Sie die Pfad Geometrie und die Übersetzungs Matrix.

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

    

6.  Zeichnen Sie schließlich den Umriss der transformierten Geometrie, und füllen Sie ihn mit den [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -und [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methoden und den [Direct2D](../direct2d/direct2d-portal.md) -Pinseln, die als Element Variablen gespeichert sind.

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

    

7.  Nachdem Sie das Zeichnen abgeschlossen haben, sollten Sie nicht vergessen, die Objekte zu bereinigen, die in dieser Methode erstellt wurden.

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>Drawunder Line () und drawstrikethrough ()

[**Idwrite tetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) verfügt auch über Rückrufe zum Zeichnen der Unterstreichung und durchgestrichen. In diesem Beispiel wird ein einfaches Rechteck für eine Unterstreichung oder durchgestrichen gezeichnet, aber andere Formen können gezeichnet werden.

Das Zeichnen einer Unterstreichung mithilfe von [Direct2D](../direct2d/direct2d-portal.md) besteht aus den folgenden Schritten.

1.  Erstellen Sie zuerst eine [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) -Struktur der Größe und Form der Unterstreichung. Die [**dwrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) -Unterstreichung-Struktur, die an die [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) -Rückruf Methode übermittelt wird, bietet den Offset, die Breite und die Stärke der Unterstreichung.

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  Erstellen Sie als nächstes ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) -Objekt, indem Sie die [**ID2D1Factory:: kreaterectanglegeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) -Methode und die initialisierte [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) -Struktur verwenden.

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  Wie bei der Symbol Führung muss der Ursprung der unterstrichsgeometrie mithilfe der Methode " [**kreatetransformedgeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) " basierend auf den Baseline-Ursprungs Werten übersetzt werden.

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

    

4.  Zeichnen Sie schließlich den Umriss der transformierten Geometrie, und füllen Sie ihn mit den [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -und [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methoden und den [Direct2D](../direct2d/direct2d-portal.md) -Pinseln, die als Element Variablen gespeichert sind.

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

    

5.  Nachdem Sie das Zeichnen abgeschlossen haben, sollten Sie nicht vergessen, die Objekte zu bereinigen, die in dieser Methode erstellt wurden.

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

Der Prozess zum Zeichnen eines durchgestrichen ist identisch. Allerdings hat das durchgestrichen eine andere Abweichung und wahrscheinlich eine andere Breite und Stärke.

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>Pixel-Snapping, Pixel pro DIP und Transformation

### <a name="ispixelsnappingdisabled"></a>Ispixelsnappingdeaktiviert ()

Diese Methode wird aufgerufen, um zu bestimmen, ob das Ausrichten von Pixeln deaktiviert ist. Der empfohlene Standardwert ist **false**. Dies ist die Ausgabe dieses Beispiels.


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>Getcurrenttransform ()

In diesem Beispiel wird in ein Direct2D-Renderziel gerendert, sodass die Transformation vom Renderziel mithilfe von [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform)weiterleiten soll.


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>Getpixelsperdip ()

Diese Methode wird aufgerufen, um die Anzahl der Pixel pro geräteunabhängigen Pixel (DIP) zu erhalten.


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>Drawinlineobject ()

Ein benutzerdefinierter TextRenderer verfügt auch über einen Rückruf zum Zeichnen von Inline Objekten. In diesem Beispiel gibt [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) E \_ notimpl zurück. Eine Erläuterung zum Zeichnen von Inline Objekten geht über den Rahmen dieses Tutorials hinaus. Weitere Informationen finden Sie im Thema Vorgehens [Weise beim Hinzufügen von Inline Objekten zu einem Text Layout](how-to-add-inline-objects-to-a-text-layout.md) .

## <a name="the-destructor"></a>Der Dekonstruktor

Es ist wichtig, alle Zeiger freizugeben, die von der benutzerdefinierten TextRenderer-Klasse verwendet wurden.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>Verwenden des benutzerdefinierten textrenderers

Sie werden mit dem benutzerdefinierten Renderer mithilfe der [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode gerengt, die eine von [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) abgeleitete Rückruf Schnittstelle als Argument annimmt, wie im folgenden Code gezeigt.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode ruft die Methoden des von Ihnen bereitgestellten benutzerdefinierten rendererrückrufs auf. Die oben beschriebenen Methoden [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)und [**drawstrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) führen die Zeichnungsfunktionen aus.

 

 