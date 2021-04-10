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
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a><span data-ttu-id="bfee2-103">Hinzufügen von Client Zeichnungs Effekten zu einem Text Layout</span><span class="sxs-lookup"><span data-stu-id="bfee2-103">How to Add Client Drawing Effects to a Text Layout</span></span>

<span data-ttu-id="bfee2-104">Bietet ein kurzes Tutorial zum Hinzufügen von Client Zeichnungs Effekten zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle und einem benutzerdefinierten TextRenderer Text anzeigt.</span><span class="sxs-lookup"><span data-stu-id="bfee2-104">Provides a short tutorial on adding client drawing effects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface and a custom text renderer.</span></span>

<span data-ttu-id="bfee2-105">Das Endergebnis dieses Tutorials ist eine Anwendung, die Text enthält, der Textbereiche mit jeweils einem anderen Farb Zeichnungs Effekt anzeigt, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bfee2-105">The end product of this tutorial is an application that displays text that has ranges of text with a different color drawing effect on each, as shown in the following screen shot.</span></span>

![Screenshot des Beispiels "Beispiel für den Client Zeichnungs Effekt!"](images/drawingeffects.png)

> [!Note]  
> <span data-ttu-id="bfee2-108">Dieses Lernprogramm soll ein vereinfachtes Beispiel für das Erstellen von benutzerdefinierten Client Zeichnungs Effekten sein, nicht als Beispiel für eine einfache Methode zum Zeichnen von Farbtext.</span><span class="sxs-lookup"><span data-stu-id="bfee2-108">This tutorial is meant to be a simplified example of how to create custom client drawing effects, not an example of a simple method for drawing color text.</span></span> <span data-ttu-id="bfee2-109">Weitere Informationen finden Sie auf der Referenzseite zu [**idschreitetextlayout:: setdrawingeffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .</span><span class="sxs-lookup"><span data-stu-id="bfee2-109">See the [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) reference page for more information.</span></span>

 

<span data-ttu-id="bfee2-110">Dieses Tutorial enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="bfee2-110">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="bfee2-111">Schritt 1: Erstellen eines Text Layouts</span><span class="sxs-lookup"><span data-stu-id="bfee2-111">Step 1: Create a Text Layout</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="bfee2-112">Schritt 2: Implementieren einer benutzerdefinierten Zeichnungs Effekt Klasse</span><span class="sxs-lookup"><span data-stu-id="bfee2-112">Step 2: Implement a Custom Drawing Effect Class</span></span>](#step-2-implement-a-custom-drawing-effect-class)
-   [<span data-ttu-id="bfee2-113">Schritt 3: Implementieren einer benutzerdefinierten TextRenderer-Klasse</span><span class="sxs-lookup"><span data-stu-id="bfee2-113">Step 3: Implement a Custom Text Renderer Class</span></span>](#step-3-implement-a-custom-text-renderer-class)
    -   [<span data-ttu-id="bfee2-114">Der Konstruktor</span><span class="sxs-lookup"><span data-stu-id="bfee2-114">The Constructor</span></span>](#the-constructor)
    -   [<span data-ttu-id="bfee2-115">Die DrawGlyphRun-Methode</span><span class="sxs-lookup"><span data-stu-id="bfee2-115">The DrawGlyphRun Method</span></span>](#the-drawglyphrun-method)
    -   [<span data-ttu-id="bfee2-116">Der Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="bfee2-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="bfee2-117">Schritt 4: Erstellen des textrenderers</span><span class="sxs-lookup"><span data-stu-id="bfee2-117">Step 4: Create the Text Renderer</span></span>](#step-4-create-the-text-renderer)
-   [<span data-ttu-id="bfee2-118">Schritt 5: Instanziieren der Farb Zeichnungs Effekt-Objekte</span><span class="sxs-lookup"><span data-stu-id="bfee2-118">Step 5: Instantiate the Color Drawing Effect Objects</span></span>](#step-5-instantiate-the-color-drawing-effect-objects)
-   [<span data-ttu-id="bfee2-119">Schritt 6: Festlegen des Zeichnungs Effekts für bestimmte Text Bereiche</span><span class="sxs-lookup"><span data-stu-id="bfee2-119">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [<span data-ttu-id="bfee2-120">Schritt 7: Zeichnen des Text Layouts mithilfe des benutzerdefinierten Renderers</span><span class="sxs-lookup"><span data-stu-id="bfee2-120">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [<span data-ttu-id="bfee2-121">Schritt 8: Bereinigen</span><span class="sxs-lookup"><span data-stu-id="bfee2-121">Step 8: Clean up</span></span>](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="bfee2-122">Schritt 1: Erstellen eines Text Layouts</span><span class="sxs-lookup"><span data-stu-id="bfee2-122">Step 1: Create a Text Layout</span></span>

<span data-ttu-id="bfee2-123">Zunächst benötigen Sie eine Anwendung mit einem [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bfee2-123">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="bfee2-124">Wenn Sie bereits über eine Anwendung verfügen, in der Text mit einem Text Layout angezeigt wird, oder Sie den benutzerdefinierten drawingeffect-Beispiel Code verwenden, fahren Sie mit Schritt 2 fort.</span><span class="sxs-lookup"><span data-stu-id="bfee2-124">If you already have an application that displays text with a text layout, or you are using the Custom DrawingEffect Example Code, skip to Step 2.</span></span>

<span data-ttu-id="bfee2-125">Zum Hinzufügen eines Textlayouts müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="bfee2-125">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="bfee2-126">Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="bfee2-126">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="bfee2-127">Erstellen Sie am Ende der **createdeviceindependentresources** -Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bfee2-127">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="bfee2-128">Vergessen Sie schließlich nicht, das Text Layout im Dekonstruktor freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bfee2-128">Finally, remember to release the text layout in the destructor.</span></span>
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a><span data-ttu-id="bfee2-129">Schritt 2: Implementieren einer benutzerdefinierten Zeichnungs Effekt Klasse</span><span class="sxs-lookup"><span data-stu-id="bfee2-129">Step 2: Implement a Custom Drawing Effect Class</span></span>

<span data-ttu-id="bfee2-130">Abgesehen von den Methoden, die von IUnknown geerbt wurden, hat eine benutzerdefinierte Schnittstelle für den Client Zeichnungs Effekt keine Anforderungen bezüglich der Implementierung, die implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bfee2-130">Other than the methods inherited from IUnknown, a custom client drawing effect interface has no requirements as to what it must implement.</span></span> <span data-ttu-id="bfee2-131">In diesem Fall enthält die **colordrawingeffect** -Klasse einfach einen [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) -Wert und deklariert Methoden zum erhalten und Festlegen dieses Werts sowie einen Konstruktor, der die Farbe anfänglich festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="bfee2-131">In this case, the **ColorDrawingEffect** class simply holds a [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value and declares methods to get and set this value, as well as a constructor that can set the color initially.</span></span>

<span data-ttu-id="bfee2-132">Nachdem ein Client Zeichnungs Effekt auf einen Textbereich in einem [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt angewendet wurde, wird der Zeichnungs Effekt an die [**idschreitetextrenderer::D rawglyphrun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode einer beliebigen Symbol Ausführung, die gerendert werden soll, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bfee2-132">After a client drawing effect is applied to a text range in a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, the drawing effect is passed to the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of any glyph run that is to be rendered.</span></span> <span data-ttu-id="bfee2-133">Die Methoden des Zeichnungs Effekts sind dann für den TextRenderer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bfee2-133">The methods of the drawing effect are then available to the text renderer.</span></span>

<span data-ttu-id="bfee2-134">Ein Client Zeichnungs Effekt kann so komplex sein, wie Sie ihn machen möchten, indem er mehr Informationen als in diesem Beispiel bietet und Methoden zum Ändern von Symbolen, zum Erstellen von Objekten, die zum Zeichnen verwendet werden, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="bfee2-134">A client drawing effect can be as complex as you want to make it, carrying more information than in this example, as well as providing methods to alter glyphs, create objects to be used for drawing, and so on.</span></span>

## <a name="step-3-implement-a-custom-text-renderer-class"></a><span data-ttu-id="bfee2-135">Schritt 3: Implementieren einer benutzerdefinierten TextRenderer-Klasse</span><span class="sxs-lookup"><span data-stu-id="bfee2-135">Step 3: Implement a Custom Text Renderer Class</span></span>

<span data-ttu-id="bfee2-136">Um einen Client Zeichnungs Effekt zu nutzen, müssen Sie einen benutzerdefinierten TextRenderer implementieren.</span><span class="sxs-lookup"><span data-stu-id="bfee2-136">In order to take advantage of a client drawing effect, you must implement a custom text renderer.</span></span> <span data-ttu-id="bfee2-137">Dieser TextRenderer wendet den Zeichnungs Effekt an, der durch die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode an das gezeichnete Symbol ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfee2-137">This text renderer will apply the drawing effect passed to it by the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method to the glyph run being drawn.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="bfee2-138">Der Konstruktor</span><span class="sxs-lookup"><span data-stu-id="bfee2-138">The Constructor</span></span>

<span data-ttu-id="bfee2-139">Der Konstruktor für den benutzerdefinierten TextRenderer speichert das [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt, das zum Erstellen von [Direct2D](../direct2d/direct2d-portal.md) -Objekten verwendet wird, und das Direct2D-Renderziel, für das der Text gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="bfee2-139">The constructor for the custom text renderer stores the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create [Direct2D](../direct2d/direct2d-portal.md) objects, and the Direct2D render target that the text will be drawn on to.</span></span>


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



### <a name="the-drawglyphrun-method"></a><span data-ttu-id="bfee2-140">Die DrawGlyphRun-Methode</span><span class="sxs-lookup"><span data-stu-id="bfee2-140">The DrawGlyphRun Method</span></span>

<span data-ttu-id="bfee2-141">Eine Symbol Führung ist ein Satz von Symbolen, die das gleiche Format aufweisen, einschließlich des Client Zeichnungs Effekts.</span><span class="sxs-lookup"><span data-stu-id="bfee2-141">A glyph run is a set of glyphs that share the same format, including the client drawing effect.</span></span> <span data-ttu-id="bfee2-142">Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode kümmert sich um das Text Rendering für eine angegebene Symbol Ausführung.</span><span class="sxs-lookup"><span data-stu-id="bfee2-142">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method takes care of the text rendering for a specified glyph run.</span></span>

<span data-ttu-id="bfee2-143">Erstellen Sie zuerst ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Element und ein [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)-Element, und rufen Sie dann die Symbol Lauf Gliederung mithilfe von [**idschreitefontface:: getglyphrunumriss**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline)ab.</span><span class="sxs-lookup"><span data-stu-id="bfee2-143">First, create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), and then retrieve the glyph run outline by using [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span></span> <span data-ttu-id="bfee2-144">Transformieren Sie anschließend den Ursprung der Geometrie mithilfe der [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: deatetransformedgeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) -Methode, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bfee2-144">Then transform the origin of the geometry by using the [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method, as shown in the following code.</span></span>


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



<span data-ttu-id="bfee2-145">Deklarieren Sie als nächstes ein [Direct2D](../direct2d/direct2d-portal.md) -Solid Brush-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bfee2-145">Next, declare a [Direct2D](../direct2d/direct2d-portal.md) solid brush object.</span></span>


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



<span data-ttu-id="bfee2-146">Wenn der *clientdrawingeffect* -Parameter nicht NULL ist, Fragen Sie das-Objekt nach der **colordrawingeffect** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="bfee2-146">If the *clientDrawingEffect* parameter is not NULL, query the object for the **ColorDrawingEffect** interface.</span></span> <span data-ttu-id="bfee2-147">Dies funktioniert, da Sie diese Klasse als Client Zeichnungs Effekt für Textbereiche des textlayoutobjekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="bfee2-147">This will work because you will set this class as the client drawing effect on text ranges of the text layout object.</span></span>

<span data-ttu-id="bfee2-148">Sobald Sie über einen Zeiger auf die **colordrawingeffect** -Schnittstelle verfügen, können Sie den Wert von [**D2D1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) mithilfe der **GetColor** -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="bfee2-148">Once you have a pointer to the **ColorDrawingEffect** interface, you can retrieve the [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value that it stores using the **GetColor** method.</span></span> <span data-ttu-id="bfee2-149">Verwenden Sie dann die **D2D1- \_ Farbe \_ F** , um eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in dieser Farbe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bfee2-149">Then, use the **D2D1\_COLOR\_F** to create a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in that color.</span></span>

<span data-ttu-id="bfee2-150">Wenn der *clientdrawingeffect* -Parameter **null** ist, erstellen Sie einfach ein schwarzes [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="bfee2-150">If the *clientDrawingEffect* parameter is **NULL**, then just create a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


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



<span data-ttu-id="bfee2-151">Zeichnen Sie schließlich die Gliederungs Geometrie, und füllen Sie Sie mit dem voll Tonfarbe aus, den Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="bfee2-151">Finally, draw the outline geometry and fill it using the solid color brush that you just created.</span></span>


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



### <a name="the-destructor"></a><span data-ttu-id="bfee2-152">Der Dekonstruktor</span><span class="sxs-lookup"><span data-stu-id="bfee2-152">The Destructor</span></span>

<span data-ttu-id="bfee2-153">Vergessen Sie nicht, die [Direct2D](../direct2d/direct2d-portal.md) Factory und das Renderziel im debugtor freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bfee2-153">Don't forget to release the [Direct2D](../direct2d/direct2d-portal.md) factory and render target in the destructor.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a><span data-ttu-id="bfee2-154">Schritt 4: Erstellen des textrenderers</span><span class="sxs-lookup"><span data-stu-id="bfee2-154">Step 4: Create the Text Renderer</span></span>

<span data-ttu-id="bfee2-155">Erstellen Sie in den **createdevicedependent** -Ressourcen das benutzerdefinierte TextRenderer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bfee2-155">In the **CreateDeviceDependent** resources, create the custom text renderer object.</span></span> <span data-ttu-id="bfee2-156">Er ist Geräte abhängig, da er das **ID2D1RenderTarget**-Gerät verwendet, das selbst vom Gerät abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="bfee2-156">It is device dependent because it uses the **ID2D1RenderTarget**, which is itself device dependent.</span></span>


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a><span data-ttu-id="bfee2-157">Schritt 5: Instanziieren der Farb Zeichnungs Effekt-Objekte</span><span class="sxs-lookup"><span data-stu-id="bfee2-157">Step 5: Instantiate the Color Drawing Effect Objects</span></span>

<span data-ttu-id="bfee2-158">Instanziieren Sie **colordrawingeffect** -Objekte in rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="bfee2-158">Instantiate **ColorDrawingEffect** objects in red, green, and blue.</span></span>


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a><span data-ttu-id="bfee2-159">Schritt 6: Festlegen des Zeichnungs Effekts für bestimmte Text Bereiche</span><span class="sxs-lookup"><span data-stu-id="bfee2-159">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>

<span data-ttu-id="bfee2-160">Legen Sie den Zeichnungs Effekt für bestimmte Textbereiche fest, indem Sie die [**idwrite tetextlayou:: setdrawingeffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) -Methode und eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="bfee2-160">Set the drawing effect for specific ranges of text by using the [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) method and a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) struct.</span></span>


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a><span data-ttu-id="bfee2-161">Schritt 7: Zeichnen des Text Layouts mithilfe des benutzerdefinierten Renderers</span><span class="sxs-lookup"><span data-stu-id="bfee2-161">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>

<span data-ttu-id="bfee2-162">Sie müssen die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode anstelle der Methoden [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) oder [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="bfee2-162">You must call the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method rather than the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) or [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) methods.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a><span data-ttu-id="bfee2-163">Schritt 8: Bereinigen</span><span class="sxs-lookup"><span data-stu-id="bfee2-163">Step 8: Clean up</span></span>

<span data-ttu-id="bfee2-164">Geben Sie im demoApp-Dekonstruktor den benutzerdefinierten TextRenderer frei.</span><span class="sxs-lookup"><span data-stu-id="bfee2-164">In the DemoApp destructor, release the custom text renderer.</span></span>


```C++
SafeRelease(&pTextRenderer_);
```



<span data-ttu-id="bfee2-165">Fügen Sie anschließend Code hinzu, um die Klassen für den Client Zeichnungs Effekt freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bfee2-165">After that, add code to release the client drawing effect classes.</span></span>


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 