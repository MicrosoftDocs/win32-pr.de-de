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
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>Vorgehensweise beim Hinzufügen von Inline Objekten zu einem Text Layout

Bietet ein kurzes Tutorial zum Hinzufügen von Inline Objekten zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die Text mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle anzeigt.

Das Endprodukt dieses Tutorials ist eine Anwendung, die Text mit einem eingebetteten Inline Bild anzeigt, wie im folgenden Screenshot gezeigt.

![Screenshot des "Inline Objekt Beispiels" mit einem eingebetteten Bild](images/inlineobject.png)

Dieses Tutorial enthält die folgenden Teile:

-   [Schritt 1: Erstellen eines Text Layouts](#step-1-create-a-text-layout)
-   [Schritt 2: Definieren einer Klasse, die von der idschreiteinlineobject-Schnittstelle abgeleitet ist.](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [Schritt 3: Implementieren Sie die Inline Objektklasse.](#step-3-implement-the-inline-object-class)
    -   [Der Konstruktor.](#the-constructor)
    -   [Die Draw-Methode.](#the-draw-method)
    -   [Die getmetrics-Methode.](#the-getmetrics-method)
    -   [Die gedeverhangmetrics-Methode.](#the-getoverhangmetrics-method)
    -   [Die getbreakconditions-Methode.](#the-getbreakconditions-method)
-   [Schritt 4: Erstellen Sie eine Instanz der InlineImage-Klasse, und fügen Sie Sie dem Text Layout hinzu.](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>Schritt 1: Erstellen eines Text Layouts

Zunächst benötigen Sie eine Anwendung mit einem [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt. Wenn Sie bereits über eine Anwendung verfügen, in der Text mit einem Text Layout angezeigt wird, fahren Sie mit Schritt 2 fort.

Zum Hinzufügen eines Textlayouts müssen Sie die folgenden Schritte ausführen:

1.  Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der-Klasse.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Erstellen Sie am Ende der createdeviceindependentresources-Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen.
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

    

3.  Anschließend müssen Sie den aufrufsbefehl der [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)ändern, wie im folgenden Code gezeigt.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>Schritt 2: Definieren einer Klasse, die von der idschreiteinlineobject-Schnittstelle abgeleitet ist.

Die Unterstützung für Inline Objekte in [DirectWrite](direct-write-portal.md) wird von der [**idwrite teinlineobject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) -Schnittstelle bereitgestellt. Um Inline Objekte verwenden zu können, müssen Sie diese Schnittstelle implementieren. Sie behandelt das Zeichnen des Inline Objekts sowie das Bereitstellen von Metriken und anderen Informationen für den Renderer.

Erstellen Sie eine neue Header Datei, und deklarieren Sie eine Schnittstelle mit dem Namen InlineImage, die von [**idschreiteinlineobject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)abgeleitet wird.

Zusätzlich zu "QueryInterface", "adressf" und "Release", die von "IUnknown" geerbt wurden, muss diese Klasse die folgenden Methoden aufweisen:

-   [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**Getmetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**Gedeverhangmetrics**](idwriteinlineobject-getoverhangmetrics.md)
-   [**Getbreakconditions**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>Schritt 3: Implementieren Sie die Inline Objektklasse.

Erstellen Sie eine neue C++-Datei mit dem Namen "InlineImage. cpp" für die Klassen Implementierung. Zusätzlich zur loadbitmapfromfile-Methode und den Methoden, die von der IUnknown-Schnittstelle geerbt werden, besteht die InlineImage-Klasse aus den folgenden Methoden.

### <a name="the-constructor"></a>Der Konstruktor.


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



Das erste Argument des Konstruktors ist die ID2D1RenderTarget, für die das Inline Bild gerendert wird. Diese wird für die spätere Verwendung gespeichert, wenn gezeichnet wird.

Das Renderziel, IWICImagingFactory und der Dateiname-URI werden an die loadbitmapfromfile-Methode übergeben, die die Bitmap lädt und die Bitmapgröße (Breite und Höhe) in der Rect-Element \_ Variablen speichert.

### <a name="the-draw-method"></a>Die Draw-Methode.

Die [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) -Methode ist ein Rückruf, der vom [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) -Objekt aufgerufen wird, wenn das Inline Objekt gezeichnet werden muss. Das Text Layout ruft diese Methode nicht direkt auf.


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



In diesem Fall wird das Zeichnen der Bitmap mithilfe der [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) -Methode durchgeführt. Allerdings kann jede Methode zum Zeichnen verwendet werden.

### <a name="the-getmetrics-method"></a>Die getmetrics-Methode.


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



Speichern Sie für die [**getmetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) -Methode die Breite, die Höhe und die Baseline in einer [**dwrite- \_ Inline- \_ \_ objektmetrikstruktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) . [**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ruft diese Rückruffunktion auf, um die Maßeinheit für das Inline Objekt zu erhalten.

### <a name="the-getoverhangmetrics-method"></a>Die gedeverhangmetrics-Methode.


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



In diesem Fall ist kein Überlauf erforderlich, daher gibt die [**gedeverhangmetrics**](idwriteinlineobject-getoverhangmetrics.md) -Methode alle Nullen zurück.

### <a name="the-getbreakconditions-method"></a>Die getbreakconditions-Methode.


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>Schritt 4: Erstellen Sie eine Instanz der InlineImage-Klasse, und fügen Sie Sie dem Text Layout hinzu.

Erstellen Sie schließlich in der createdevicedependentresources-Methode eine Instanz der InlineImage-Klasse, und fügen Sie Sie dem Text Layout hinzu. Da Sie einen Verweis auf den [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)enthält, bei dem es sich um eine Geräte abhängige Ressource handelt und die [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit dem Renderziel erstellt wird, ist InlineImage ebenfalls Geräte abhängig und muss neu erstellt werden, wenn das Renderziel neu erstellt wird.


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



Die [**idwrite tetextlayout:: setinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) -Methode nimmt eine Text Bereichs Struktur an. Das-Objekt gilt für den hier angegebenen Bereich, und jeder Text im Bereich wird unterdrückt. Wenn die Länge des Text Bereichs 0 ist, wird das Objekt nicht gezeichnet.

In diesem Beispiel gibt es ein Sternchen ( \* ) als Platzhalter an der Position, an der das Bild angezeigt wird.


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



Da die InlineImage-Klasse von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)abhängig ist, müssen Sie Sie freigeben, wenn Sie das Renderziel freigeben.


```C++
SafeRelease(&pInlineImage_);
```



 

 