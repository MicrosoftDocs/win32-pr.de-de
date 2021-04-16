---
title: Vorgehensweise beim Hinzufügen von Inline Objekten zu einem Text Layout
description: Bietet ein kurzes Tutorial zum Hinzufügen von Inline Objekten zu einer DirectWrite-Anwendung, die Text mithilfe der idwrite-Textlayout-Schnittstelle anzeigt.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d9ef34e38ec9b84afd887e565e76efb9618b88
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104565487"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a><span data-ttu-id="61903-103">Vorgehensweise beim Hinzufügen von Inline Objekten zu einem Text Layout</span><span class="sxs-lookup"><span data-stu-id="61903-103">How to Add Inline Objects to a Text Layout</span></span>

<span data-ttu-id="61903-104">Bietet ein kurzes Tutorial zum Hinzufügen von Inline Objekten zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die Text mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="61903-104">Provides a short tutorial on adding inline objects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="61903-105">Das Endprodukt dieses Tutorials ist eine Anwendung, die Text mit einem eingebetteten Inline Bild anzeigt, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="61903-105">The end product of this tutorial is an application that displays text with an inline image embedded in it, as shown in the following screen shot.</span></span>

![Screenshot des "Inline Objekt Beispiels" mit einem eingebetteten Bild](images/inlineobject.png)

<span data-ttu-id="61903-107">Dieses Tutorial enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="61903-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="61903-108">Schritt 1: Erstellen eines Text Layouts</span><span class="sxs-lookup"><span data-stu-id="61903-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="61903-109">Schritt 2: Definieren einer Klasse, die von der idschreiteinlineobject-Schnittstelle abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="61903-109">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [<span data-ttu-id="61903-110">Schritt 3: Implementieren Sie die Inline Objektklasse.</span><span class="sxs-lookup"><span data-stu-id="61903-110">Step 3: Implement the Inline Object Class.</span></span>](#step-3-implement-the-inline-object-class)
    -   [<span data-ttu-id="61903-111">Der Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="61903-111">The Constructor.</span></span>](#the-constructor)
    -   [<span data-ttu-id="61903-112">Die Draw-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-112">The Draw Method.</span></span>](#the-draw-method)
    -   [<span data-ttu-id="61903-113">Die getmetrics-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-113">The GetMetrics Method.</span></span>](#the-getmetrics-method)
    -   [<span data-ttu-id="61903-114">Die gedeverhangmetrics-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-114">The GetOverhangMetrics Method.</span></span>](#the-getoverhangmetrics-method)
    -   [<span data-ttu-id="61903-115">Die getbreakconditions-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-115">The GetBreakConditions Method.</span></span>](#the-getbreakconditions-method)
-   [<span data-ttu-id="61903-116">Schritt 4: Erstellen Sie eine Instanz der InlineImage-Klasse, und fügen Sie Sie dem Text Layout hinzu.</span><span class="sxs-lookup"><span data-stu-id="61903-116">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="61903-117">Schritt 1: Erstellen eines Text Layouts</span><span class="sxs-lookup"><span data-stu-id="61903-117">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="61903-118">Zunächst benötigen Sie eine Anwendung mit einem [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="61903-118">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="61903-119">Wenn Sie bereits über eine Anwendung verfügen, in der Text mit einem Text Layout angezeigt wird, fahren Sie mit Schritt 2 fort.</span><span class="sxs-lookup"><span data-stu-id="61903-119">If you already have an application that displays text with a text layout, skip to Step 2.</span></span>

<span data-ttu-id="61903-120">Zum Hinzufügen eines Textlayouts müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="61903-120">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="61903-121">Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="61903-121">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="61903-122">Erstellen Sie am Ende der createdeviceindependentresources-Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="61903-122">At the end of the CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="61903-123">Anschließend müssen Sie den aufrufsbefehl der [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)ändern, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="61903-123">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), as shown in the following code.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a><span data-ttu-id="61903-124">Schritt 2: Definieren einer Klasse, die von der idschreiteinlineobject-Schnittstelle abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="61903-124">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>

<span data-ttu-id="61903-125">Die Unterstützung für Inline Objekte in [DirectWrite](direct-write-portal.md) wird von der [**idwrite teinlineobject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) -Schnittstelle bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="61903-125">Support for inline objects in [DirectWrite](direct-write-portal.md) is provided by the [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) interface.</span></span> <span data-ttu-id="61903-126">Um Inline Objekte verwenden zu können, müssen Sie diese Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="61903-126">To use inline objects, you must implement this interface.</span></span> <span data-ttu-id="61903-127">Sie behandelt das Zeichnen des Inline Objekts sowie das Bereitstellen von Metriken und anderen Informationen für den Renderer.</span><span class="sxs-lookup"><span data-stu-id="61903-127">It handles the drawing of the inline object, as well as providing metrics and other information to the renderer.</span></span>

<span data-ttu-id="61903-128">Erstellen Sie eine neue Header Datei, und deklarieren Sie eine Schnittstelle mit dem Namen InlineImage, die von [**idschreiteinlineobject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="61903-128">Create a new header file and declare an interface called InlineImage, derived from [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span></span>

<span data-ttu-id="61903-129">Zusätzlich zu "QueryInterface", "adressf" und "Release", die von "IUnknown" geerbt wurden, muss diese Klasse die folgenden Methoden aufweisen:</span><span class="sxs-lookup"><span data-stu-id="61903-129">In addition to QueryInterface, AddRef, and Release inherited from IUnknown, this class must have the following methods:</span></span>

-   [<span data-ttu-id="61903-130">**Draw**</span><span class="sxs-lookup"><span data-stu-id="61903-130">**Draw**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [<span data-ttu-id="61903-131">**Getmetrics**</span><span class="sxs-lookup"><span data-stu-id="61903-131">**GetMetrics**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [<span data-ttu-id="61903-132">**Gedeverhangmetrics**</span><span class="sxs-lookup"><span data-stu-id="61903-132">**GetOverhangMetrics**</span></span>](idwriteinlineobject-getoverhangmetrics.md)
-   [<span data-ttu-id="61903-133">**Getbreakconditions**</span><span class="sxs-lookup"><span data-stu-id="61903-133">**GetBreakConditions**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a><span data-ttu-id="61903-134">Schritt 3: Implementieren Sie die Inline Objektklasse.</span><span class="sxs-lookup"><span data-stu-id="61903-134">Step 3: Implement the Inline Object Class.</span></span>

<span data-ttu-id="61903-135">Erstellen Sie eine neue C++-Datei mit dem Namen "InlineImage. cpp" für die Klassen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="61903-135">Create a new C++ file, named InlineImage.cpp, for the class implementation.</span></span> <span data-ttu-id="61903-136">Zusätzlich zur loadbitmapfromfile-Methode und den Methoden, die von der IUnknown-Schnittstelle geerbt werden, besteht die InlineImage-Klasse aus den folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="61903-136">In addition to the LoadBitmapFromFile method and the methods inherited from the IUnknown interface, the InlineImage class is made up of the following methods.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="61903-137">Der Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="61903-137">The Constructor.</span></span>


```C++
InlineImage::InlineImage(
    ID2D1RenderTarget *pRenderTarget, 
    IWICImagingFactory *pIWICFactory,
    PCWSTR uri
    )
{
    // Save the render target for later.
    pRT_ = pRenderTarget;

    pRT_->AddRef();

    // Load the bitmap from a file.
    LoadBitmapFromFile(
        pRenderTarget,
        pIWICFactory,
        uri,
        &pBitmap_
        );
}
```



<span data-ttu-id="61903-138">Das erste Argument des Konstruktors ist die ID2D1RenderTarget, für die das Inline Bild gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="61903-138">The first argument of the constructor is the ID2D1RenderTarget that the inline image will be rendered to.</span></span> <span data-ttu-id="61903-139">Diese wird für die spätere Verwendung gespeichert, wenn gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="61903-139">This is stored for use later when drawing.</span></span>

<span data-ttu-id="61903-140">Das Renderziel, IWICImagingFactory und der Dateiname-URI werden an die loadbitmapfromfile-Methode übergeben, die die Bitmap lädt und die Bitmapgröße (Breite und Höhe) in der Rect-Element \_ Variablen speichert.</span><span class="sxs-lookup"><span data-stu-id="61903-140">The render target, IWICImagingFactory, and the filename uri are all passed to the LoadBitmapFromFile method that loads the bitmap and stores the bitmap size (width and height) in the rect\_ member variable.</span></span>

### <a name="the-draw-method"></a><span data-ttu-id="61903-141">Die Draw-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-141">The Draw Method.</span></span>

<span data-ttu-id="61903-142">Die [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) -Methode ist ein Rückruf, der vom [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) -Objekt aufgerufen wird, wenn das Inline Objekt gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="61903-142">The [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) method is a callback that is called by the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) object when the inline object needs to be drawn.</span></span> <span data-ttu-id="61903-143">Das Text Layout ruft diese Methode nicht direkt auf.</span><span class="sxs-lookup"><span data-stu-id="61903-143">The text layout does not call this method directly.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::Draw(
    __maybenull void* clientDrawingContext,
    IDWriteTextRenderer* renderer,
    FLOAT originX,
    FLOAT originY,
    BOOL isSideways,
    BOOL isRightToLeft,
    IUnknown* clientDrawingEffect
    )
{
    float height    = rect_.bottom - rect_.top;
    float width     = rect_.right  - rect_.left;
    D2D1_RECT_F destRect  = {originX, originY, originX + width, originY + height};

    pRT_->DrawBitmap(pBitmap_, destRect);

    return S_OK;
}
```



<span data-ttu-id="61903-144">In diesem Fall wird das Zeichnen der Bitmap mithilfe der [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) -Methode durchgeführt. Allerdings kann jede Methode zum Zeichnen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61903-144">In this case, drawing the bitmap is done by using the [**ID2D1RenderTarget::DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) method; however, any method for drawing can be used.</span></span>

### <a name="the-getmetrics-method"></a><span data-ttu-id="61903-145">Die getmetrics-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-145">The GetMetrics Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetMetrics(
    __out DWRITE_INLINE_OBJECT_METRICS* metrics
    )
{
    DWRITE_INLINE_OBJECT_METRICS inlineMetrics = {};
    inlineMetrics.width     = rect_.right  - rect_.left;
    inlineMetrics.height    = rect_.bottom - rect_.top;
    inlineMetrics.baseline  = baseline_;
    *metrics = inlineMetrics;
    return S_OK;
}
```



<span data-ttu-id="61903-146">Speichern Sie für die [**getmetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) -Methode die Breite, die Höhe und die Baseline in einer [**dwrite- \_ Inline- \_ \_ objektmetrikstruktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) .</span><span class="sxs-lookup"><span data-stu-id="61903-146">For the [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) method, store the width, height and baseline in an [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) structure.</span></span> <span data-ttu-id="61903-147">[**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ruft diese Rückruffunktion auf, um die Maßeinheit für das Inline Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61903-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the measurement of the inline object.</span></span>

### <a name="the-getoverhangmetrics-method"></a><span data-ttu-id="61903-148">Die gedeverhangmetrics-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-148">The GetOverhangMetrics Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetOverhangMetrics(
    __out DWRITE_OVERHANG_METRICS* overhangs
    )
{
    overhangs->left      = 0;
    overhangs->top       = 0;
    overhangs->right     = 0;
    overhangs->bottom    = 0;
    return S_OK;
}
```



<span data-ttu-id="61903-149">In diesem Fall ist kein Überlauf erforderlich, daher gibt die [**gedeverhangmetrics**](idwriteinlineobject-getoverhangmetrics.md) -Methode alle Nullen zurück.</span><span class="sxs-lookup"><span data-stu-id="61903-149">In this case, no overhang is necessary, so the [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) method returns all zeros.</span></span>

### <a name="the-getbreakconditions-method"></a><span data-ttu-id="61903-150">Die getbreakconditions-Methode.</span><span class="sxs-lookup"><span data-stu-id="61903-150">The GetBreakConditions Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetBreakConditions(
    __out DWRITE_BREAK_CONDITION* breakConditionBefore,
    __out DWRITE_BREAK_CONDITION* breakConditionAfter
    )
{
    *breakConditionBefore = DWRITE_BREAK_CONDITION_NEUTRAL;
    *breakConditionAfter  = DWRITE_BREAK_CONDITION_NEUTRAL;
    return S_OK;
}
```



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a><span data-ttu-id="61903-151">Schritt 4: Erstellen Sie eine Instanz der InlineImage-Klasse, und fügen Sie Sie dem Text Layout hinzu.</span><span class="sxs-lookup"><span data-stu-id="61903-151">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>

<span data-ttu-id="61903-152">Erstellen Sie schließlich in der createdevicedependentresources-Methode eine Instanz der InlineImage-Klasse, und fügen Sie Sie dem Text Layout hinzu.</span><span class="sxs-lookup"><span data-stu-id="61903-152">Finally, in the CreateDeviceDependentResources method, create an instance of the InlineImage class and add it to the text layout.</span></span> <span data-ttu-id="61903-153">Da Sie einen Verweis auf den [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)enthält, bei dem es sich um eine Geräte abhängige Ressource handelt und die [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit dem Renderziel erstellt wird, ist InlineImage ebenfalls Geräte abhängig und muss neu erstellt werden, wenn das Renderziel neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="61903-153">Because it holds a reference to the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), which is a device dependent resource, and the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is created by using the render target, the InlineImage is also device dependent and must be recreated if the render target is recreated.</span></span>


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



<span data-ttu-id="61903-154">Die [**idwrite tetextlayout:: setinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) -Methode nimmt eine Text Bereichs Struktur an.</span><span class="sxs-lookup"><span data-stu-id="61903-154">The [**IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) method takes a text range structure.</span></span> <span data-ttu-id="61903-155">Das-Objekt gilt für den hier angegebenen Bereich, und jeder Text im Bereich wird unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="61903-155">The object applies to the range specified here, and any text in the range will be suppressed.</span></span> <span data-ttu-id="61903-156">Wenn die Länge des Text Bereichs 0 ist, wird das Objekt nicht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="61903-156">If the length of the text range is 0, the object will not be drawn.</span></span>

<span data-ttu-id="61903-157">In diesem Beispiel gibt es ein Sternchen ( \* ) als Platzhalter an der Position, an der das Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="61903-157">In this example, there is an asterisk (\*) as a place holder in the position where the image will be displayed.</span></span>


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



<span data-ttu-id="61903-158">Da die InlineImage-Klasse von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)abhängig ist, müssen Sie Sie freigeben, wenn Sie das Renderziel freigeben.</span><span class="sxs-lookup"><span data-stu-id="61903-158">Since the InlineImage class is dependent on the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), you must release it when you release the render target.</span></span>


```C++
SafeRelease(&pInlineImage_);
```



 

 