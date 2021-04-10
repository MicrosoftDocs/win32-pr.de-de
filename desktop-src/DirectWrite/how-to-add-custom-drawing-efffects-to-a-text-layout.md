---
title: Hinzufügen von Client Zeichnungs Effekten zu einem Text Layout
description: Bietet ein kurzes Tutorial zum Hinzufügen von Client Zeichnungs Effekten zu einer DirectWrite-Anwendung, die mithilfe der idwrite-Textlayout-Schnittstelle und einem benutzerdefinierten TextRenderer Text anzeigt.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338dc1a720bde80c1daf2b4baf7c7a4bad6d2cff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039245"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Hinzufügen von Client Zeichnungs Effekten zu einem Text Layout

Bietet ein kurzes Tutorial zum Hinzufügen von Client Zeichnungs Effekten zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle und einem benutzerdefinierten TextRenderer Text anzeigt.

Das Endergebnis dieses Tutorials ist eine Anwendung, die Text enthält, der Textbereiche mit jeweils einem anderen Farb Zeichnungs Effekt anzeigt, wie im folgenden Screenshot gezeigt.

![Screenshot des Beispiels "Beispiel für den Client Zeichnungs Effekt!" in unterschiedlichen Farben](images/drawingeffects.png)

> [!Note]  
> Dieses Lernprogramm soll ein vereinfachtes Beispiel für das Erstellen von benutzerdefinierten Client Zeichnungs Effekten sein, nicht als Beispiel für eine einfache Methode zum Zeichnen von Farbtext. Weitere Informationen finden Sie auf der Referenzseite zu [**idschreitetextlayout:: setdrawingeffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .

 

Dieses Tutorial enthält die folgenden Teile:

-   [Schritt 1: Erstellen eines Text Layouts](#step-1-create-a-text-layout)
-   [Schritt 2: Implementieren einer benutzerdefinierten Zeichnungs Effekt Klasse](#step-2-implement-a-custom-drawing-effect-class)
-   [Schritt 3: Implementieren einer benutzerdefinierten TextRenderer-Klasse](#step-3-implement-a-custom-text-renderer-class)
    -   [Der Konstruktor](#the-constructor)
    -   [Die DrawGlyphRun-Methode](#the-drawglyphrun-method)
    -   [Der Dekonstruktor](#the-destructor)
-   [Schritt 4: Erstellen des textrenderers](#step-4-create-the-text-renderer)
-   [Schritt 5: Instanziieren der Farb Zeichnungs Effekt-Objekte](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Schritt 6: Festlegen des Zeichnungs Effekts für bestimmte Text Bereiche](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Schritt 7: Zeichnen des Text Layouts mithilfe des benutzerdefinierten Renderers](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Schritt 8: Bereinigen](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Schritt 1: Erstellen eines Text Layouts

Zunächst benötigen Sie eine Anwendung mit einem [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt. Wenn Sie bereits über eine Anwendung verfügen, in der Text mit einem Text Layout angezeigt wird, oder Sie den benutzerdefinierten drawingeffect-Beispiel Code verwenden, fahren Sie mit Schritt 2 fort.

Zum Hinzufügen eines Textlayouts müssen Sie die folgenden Schritte ausführen:

1.  Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der-Klasse.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Erstellen Sie am Ende der **createdeviceindependentresources** -Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen.
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

3.  Vergessen Sie schließlich nicht, das Text Layout im Dekonstruktor freizugeben.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Schritt 2: Implementieren einer benutzerdefinierten Zeichnungs Effekt Klasse

Abgesehen von den Methoden, die von IUnknown geerbt wurden, hat eine benutzerdefinierte Schnittstelle für den Client Zeichnungs Effekt keine Anforderungen bezüglich der Implementierung, die implementiert werden muss. In diesem Fall enthält die **colordrawingeffect** -Klasse einfach einen [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) -Wert und deklariert Methoden zum erhalten und Festlegen dieses Werts sowie einen Konstruktor, der die Farbe anfänglich festlegen kann.

Nachdem ein Client Zeichnungs Effekt auf einen Textbereich in einem [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt angewendet wurde, wird der Zeichnungs Effekt an die [**idschreitetextrenderer::D rawglyphrun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode einer beliebigen Symbol Ausführung, die gerendert werden soll, übermittelt. Die Methoden des Zeichnungs Effekts sind dann für den TextRenderer verfügbar.

Ein Client Zeichnungs Effekt kann so komplex sein, wie Sie ihn machen möchten, indem er mehr Informationen als in diesem Beispiel bietet und Methoden zum Ändern von Symbolen, zum Erstellen von Objekten, die zum Zeichnen verwendet werden, und so weiter.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Schritt 3: Implementieren einer benutzerdefinierten TextRenderer-Klasse

Um einen Client Zeichnungs Effekt zu nutzen, müssen Sie einen benutzerdefinierten TextRenderer implementieren. Dieser TextRenderer wendet den Zeichnungs Effekt an, der durch die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode an das gezeichnete Symbol ausgeführt wird.

### <a name="the-constructor"></a>Der Konstruktor

Der Konstruktor für den benutzerdefinierten TextRenderer speichert das [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt, das zum Erstellen von [Direct2D](../direct2d/direct2d-portal.md) -Objekten verwendet wird, und das Direct2D-Renderziel, für das der Text gezeichnet wird.


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
}
```



### <a name="the-drawglyphrun-method"></a>Die DrawGlyphRun-Methode

Eine Symbol Führung ist ein Satz von Symbolen, die das gleiche Format aufweisen, einschließlich des Client Zeichnungs Effekts. Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode kümmert sich um das Text Rendering für eine angegebene Symbol Ausführung.

Erstellen Sie zuerst ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Element und ein [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)-Element, und rufen Sie dann die Symbol Lauf Gliederung mithilfe von [**idschreitefontface:: getglyphrunumriss**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline)ab. Transformieren Sie anschließend den Ursprung der Geometrie mithilfe der [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: deatetransformedgeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) -Methode, wie im folgenden Code gezeigt.


```C++
HRESULT hr = S_OK;

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

// Close the geometry sink
if (SUCCEEDED(hr))
{
    hr = pSink->Close();
}

// Initialize a matrix to translate the origin of the glyph run.
D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
    1.0f, 0.0f,
    0.0f, 1.0f,
    baselineOriginX, baselineOriginY
    );

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



Deklarieren Sie als nächstes ein [Direct2D](../direct2d/direct2d-portal.md) -Solid Brush-Objekt.


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Wenn der *clientdrawingeffect* -Parameter nicht NULL ist, Fragen Sie das-Objekt nach der **colordrawingeffect** -Schnittstelle ab. Dies funktioniert, da Sie diese Klasse als Client Zeichnungs Effekt für Textbereiche des textlayoutobjekts festlegen.

Sobald Sie über einen Zeiger auf die **colordrawingeffect** -Schnittstelle verfügen, können Sie den Wert von [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) mithilfe der **GetColor** -Methode abrufen. Verwenden Sie dann die **D2D1- \_ Farbe \_ F** , um eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in dieser Farbe zu erstellen.

Wenn der *clientdrawingeffect* -Parameter **null** ist, erstellen Sie einfach ein schwarzes [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).


```C++
// If there is a drawing effect create a color brush using it, otherwise create a black brush.
if (clientDrawingEffect != NULL)
{
    // Go from IUnknown to ColorDrawingEffect.
    ColorDrawingEffect *colorDrawingEffect;

    clientDrawingEffect->QueryInterface(__uuidof(ColorDrawingEffect), reinterpret_cast<void**>(&colorDrawingEffect));

    // Get the color from the ColorDrawingEffect object.
    D2D1_COLOR_F color;

    colorDrawingEffect->GetColor(&color);

    // Create the brush using the color pecified by our ColorDrawingEffect object.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            color,
            &pBrush);
    }

    SafeRelease(&colorDrawingEffect);
}
else
{
    // Create a black brush.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            D2D1::ColorF(
            D2D1::ColorF::Black
            ),
            &pBrush);
    }
}
```



Zeichnen Sie schließlich die Gliederungs Geometrie, und füllen Sie Sie mit dem voll Tonfarbe aus, den Sie soeben erstellt haben.


```C++
if (SUCCEEDED(hr))
{
    // Draw the outline of the glyph run
    pRT_->DrawGeometry(
        pTransformedGeometry,
        pBrush
        );

    // Fill in the glyph run
    pRT_->FillGeometry(
        pTransformedGeometry,
        pBrush
        );
}
```



### <a name="the-destructor"></a>Der Dekonstruktor

Vergessen Sie nicht, die [Direct2D](../direct2d/direct2d-portal.md) Factory und das Renderziel im debugtor freizugeben.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>Schritt 4: Erstellen des textrenderers

Erstellen Sie in den **createdevicedependent** -Ressourcen das benutzerdefinierte TextRenderer-Objekt. Er ist Geräte abhängig, da er das **ID2D1RenderTarget**-Gerät verwendet, das selbst vom Gerät abhängig ist.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Schritt 5: Instanziieren der Farb Zeichnungs Effekt-Objekte

Instanziieren Sie **colordrawingeffect** -Objekte in rot, grün und blau.


```C++
// Instantiate some custom color drawing effects.
redDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Red
        )
    );

blueDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Blue
        )
    );

greenDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Green
        )
    );
```



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Schritt 6: Festlegen des Zeichnungs Effekts für bestimmte Text Bereiche

Legen Sie den Zeichnungs Effekt für bestimmte Textbereiche fest, indem Sie die [**idwrite tetextlayou:: setdrawingeffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) -Methode und eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Struktur verwenden.


```C++
// Set the drawing effects.

// Red.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {0,
                                   14};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(redDrawingEffect_, textRange);
    }
}

// Blue.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {14,
                                   7};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(blueDrawingEffect_, textRange);
    }
}

// Green.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {21,
                                   8};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(greenDrawingEffect_, textRange);
    }
}
```



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Schritt 7: Zeichnen des Text Layouts mithilfe des benutzerdefinierten Renderers

Sie müssen die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode anstelle der Methoden [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) oder [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) aufgerufen haben.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Schritt 8: Bereinigen

Geben Sie im demoApp-Dekonstruktor den benutzerdefinierten TextRenderer frei.


```C++
SafeRelease(&pTextRenderer_);
```



Fügen Sie anschließend Code hinzu, um die Klassen für den Client Zeichnungs Effekt freizugeben.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 