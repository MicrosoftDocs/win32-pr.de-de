---
title: Hinzufügen von Clientzeichnungseffekten zu einem Textlayout
description: Enthält ein kurzes Tutorial zum Hinzufügen von Clientzeichnungseffekten zu einer DirectWrite-Anwendung, die Text mithilfe der IDWriteTextLayout-Schnittstelle und eines benutzerdefinierten Textrenderers anzeigt.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bae98813d8f8aa8fc8a7df0a1a53d11a0329c93abb22a7f60d60754b8edc91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071709"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Hinzufügen von Clientzeichnungseffekten zu einem Textlayout

Enthält ein kurzes Tutorial zum [](direct-write-portal.md) Hinzufügen von Clientzeichnungseffekten zu einer DirectWrite-Anwendung, die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) und eines benutzerdefinierten Textrenderers anzeigt.

Das Endprodukt dieses Tutorials ist eine Anwendung, die Text mit Textbereichen mit unterschiedlichen Farbzeichnungseffekten anzeigt, wie im folgenden Screenshot gezeigt.

![Screenshot des Beispiels "Client drawing effect!" in verschiedenen Farben](images/drawingeffects.png)

> [!Note]  
> Dieses Tutorial soll ein vereinfachtes Beispiel für das Erstellen benutzerdefinierter Clientzeichnungseffekte sein, nicht ein Beispiel für eine einfache Methode zum Zeichnen von Farbtext. Weitere Informationen finden Sie auf der Referenzseite [**IDWriteTextLayout::SetDrawingEffect.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect)

 

Dieses Tutorial enthält die folgenden Teile:

-   [Schritt 1: Erstellen eines Textlayouts](#step-1-create-a-text-layout)
-   [Schritt 2: Implementieren einer benutzerdefinierten Drawing Effect-Klasse](#step-2-implement-a-custom-drawing-effect-class)
-   [Schritt 3: Implementieren einer benutzerdefinierten Textrendererklasse](#step-3-implement-a-custom-text-renderer-class)
    -   [Der Konstruktor](#the-constructor)
    -   [Die DrawGlyphRun-Methode](#the-drawglyphrun-method)
    -   [Der Destruktor](#the-destructor)
-   [Schritt 4: Erstellen des Textrenderers](#step-4-create-the-text-renderer)
-   [Schritt 5: Instanziieren der Farbzeichnungseffekt-Objekte](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Schritt 6: Festlegen des Zeichnungseffekts für bestimmte Textbereiche](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Schritt 7: Zeichnen des Textlayouts mit dem benutzerdefinierten Renderer](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Schritt 8: Bereinigt](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Schritt 1: Erstellen eines Textlayouts

Zunächst benötigen Sie eine Anwendung mit einem [**IDWriteTextLayout-Objekt.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Wenn Sie bereits über eine Anwendung verfügen, die Text mit einem Textlayout anzeigt, oder wenn Sie den Beispielcode "Custom DrawingEffect" verwenden, fahren Sie mit Schritt 2 fort.

Gehen Sie wie folgt vor, um ein Textlayout hinzuzufügen:

1.  Deklarieren Sie einen Zeiger auf eine [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) als Member der -Klasse.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Erstellen Sie am Ende der **CreateDeviceIndependentResources-Methode** ein [**IDWriteTextLayout-Schnittstellenobjekt,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) indem Sie die [**CreateTextLayout-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) aufrufen.
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

    

3.  Denken Sie abschließend daran, das Textlayout im Destruktor frei zu geben.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Schritt 2: Implementieren einer benutzerdefinierten Drawing Effect-Klasse

Abgesehen von den von IUnknown geerbten Methoden hat eine benutzerdefinierte Schnittstelle zum Zeichnen von Effekten für Clients keine Anforderungen an das, was sie implementieren muss. In diesem Fall enthält die **ColorDrawingEffect-Klasse** einfach einen [**D2D1 \_ COLOR \_ F-Wert**](../direct2d/d2d1-color-f.md) und deklariert Methoden zum Erhalten und Festlegen dieses Werts sowie einen Konstruktor, der die Farbe anfänglich festlegen kann.

Nachdem ein Clientzeichnungseffekt auf einen Textbereich in einem [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) angewendet wurde, wird der Zeichnungseffekt an die [**IDWriteTextRenderer::D rawGlyphRun-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) aller Glyphenläufe übergeben, die gerendert werden sollen. Die Methoden des Zeichnungseffekts sind dann für den Textrenderer verfügbar.

Ein Clientzeichnungseffekt kann so komplex sein, wie Sie ihn erstellen möchten. Er enthält mehr Informationen als in diesem Beispiel und stellt Methoden zum Ändern von Glyphen, zum Erstellen von Objekten für das Zeichnen und so weiter zur Verfügung.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Schritt 3: Implementieren einer benutzerdefinierten Textrendererklasse

Um einen Clientzeichnungseffekt nutzen zu können, müssen Sie einen benutzerdefinierten Textrenderer implementieren. Dieser Textrenderer verwendet den Zeichnungseffekt, der von der [**IDWriteTextLayout::D raw-Methode übergeben**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) wird, auf die gezeichnete Glyphen-Ausführung.

### <a name="the-constructor"></a>Der Konstruktor

Der Konstruktor für den benutzerdefinierten Textrenderer speichert das [**ID2D1Factory-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) das zum Erstellen von [Direct2D-Objekten](../direct2d/direct2d-portal.md) verwendet wird, und das Direct2D-Renderziel, auf das der Text gezeichnet wird.


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

Eine Glyphen-Ausführung ist ein Satz von Glyphen, die das gleiche Format haben, einschließlich des Clientzeichnungseffekts. Die [**DrawGlyphRun-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) übernimmt das Textrendering für eine angegebene Glyphenlauf.

Erstellen Sie zunächst eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) und eine [**ID2D1GeometrySink,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)und rufen Sie dann die Ausführungsgliederung des Glyphen mithilfe von [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline)ab. Transformieren Sie dann den Ursprung der Geometrie mithilfe der [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry-Methode,**](../direct2d/id2d1factory-createtransformedgeometry.md) wie im folgenden Code gezeigt.


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



Deklarieren Sie als Nächstes ein [Direct2D-Vollbildpinselobjekt.](../direct2d/direct2d-portal.md)


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Wenn der *clientDrawingEffect-Parameter* nicht NULL ist, fragen Sie das -Objekt für die **ColorDrawingEffect-Schnittstelle** ab. Dies funktioniert, da Sie diese Klasse als Clientzeichnungseffekt für Textbereiche des Textlayoutobjekts festlegen.

Sobald Sie über einen Zeiger auf die **ColorDrawingEffect-Schnittstelle** verfügen, können Sie den [**D2D1 \_ COLOR \_ F-Wert**](../direct2d/d2d1-color-f.md) abrufen, den sie mit der **GetColor-Methode** speichert. Verwenden Sie dann **D2D1 \_ COLOR \_ F,** um einen [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in dieser Farbe zu erstellen.

Wenn der *clientDrawingEffect-Parameter* **NULL ist,** erstellen Sie einfach einen schwarzen [**ID2D1SolidColorBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)


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



Zeichnen Sie abschließend die Konturgeometrie, und füllen Sie sie mit dem gerade erstellten Volltonfarbpinsel aus.


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



### <a name="the-destructor"></a>Der Destruktor

Vergessen Sie nicht, die [Direct2D-Factory](../direct2d/direct2d-portal.md) frei zu geben und das Ziel im Destruktor zu rendern.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>Schritt 4: Erstellen des Textrenderers

Erstellen Sie **in den CreateDeviceDependent-Ressourcen** das benutzerdefinierte Textrendererobjekt. Es ist geräteabhängig, da es **id2D1RenderTarget** verwendet, das selbst geräteabhängig ist.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Schritt 5: Instanziieren der Farbzeichnungseffekt-Objekte

Instanziieren Sie **ColorDrawingEffect-Objekte** in Rot, Grün und Blau.


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Schritt 6: Festlegen des Zeichnungseffekts für bestimmte Textbereiche

Legen Sie den Zeichnungseffekt für bestimmte Textbereiche fest, indem Sie die [**IDWriteTextLayou::SetDrawingEffect-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) und eine [**DWRITE \_ TEXT \_ RANGE-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) verwenden.


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Schritt 7: Zeichnen des Textlayouts mit dem benutzerdefinierten Renderer

Sie müssen anstelle der Methoden [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) oder [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) die [**IDWriteTextLayout::D raw-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) aufrufen.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Schritt 8: Bereinigt

Geben Sie im DemoApp-Destruktor den benutzerdefinierten Textrenderer frei.


```C++
SafeRelease(&pTextRenderer_);
```



Fügen Sie anschließend Code hinzu, um die Zeichnungseffektklassen des Clients frei zu geben.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 