---
title: Zeichnen von Text
description: Zeigt, wie Text mit Direct2D dargestellt wird.
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30f15704673c63c4bf44a31c64843250cceafd4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390803"
---
# <a name="how-to-draw-text"></a><span data-ttu-id="cdb6d-103">Zeichnen von Text</span><span class="sxs-lookup"><span data-stu-id="cdb6d-103">How to Draw Text</span></span>

<span data-ttu-id="cdb6d-104">Um Text mit Direct2D zu zeichnen, verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode für Text, der ein einzelnes Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-104">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format.</span></span> <span data-ttu-id="cdb6d-105">Oder verwenden Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode für mehrere Formate, erweiterte OpenType-Funktionen oder Treffer Tests.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-105">Or, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method for multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="cdb6d-106">Diese Methoden verwenden die DirectWrite-API, um eine hochwertige Textdarstellung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-106">These methods use the DirectWrite API to provide high-quality text display.</span></span>

## <a name="the-drawtext-method"></a><span data-ttu-id="cdb6d-107">Die DrawText-Methode</span><span class="sxs-lookup"><span data-stu-id="cdb6d-107">The DrawText Method</span></span>

<span data-ttu-id="cdb6d-108">Um Text mit einem einzelnen Format zu zeichnen, verwenden Sie die [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-108">To draw text that has a single format, use the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method.</span></span> <span data-ttu-id="cdb6d-109">Um diese Methode zu verwenden, verwenden Sie zuerst einen [**idwrite-Factory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) , um eine [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Instanz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-109">To use this method, first use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) instance.</span></span>

<span data-ttu-id="cdb6d-110">Der folgende Code erstellt ein [**idschreitetextformat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Objekt und speichert es in der *m \_ ptextformat* -Variablen.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-110">The following code creates an [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) object and stores it in the *m\_pTextFormat* variable.</span></span>


```C++
// Create resources which are not bound
// to any device. Their lifetime effectively extends for the
// duration of the app. These resources include the Direct2D and
// DirectWrite factories,  and a DirectWrite Text Format object
// (used for identifying particular font characteristics).
//
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    static const WCHAR msc_fontName[] = L"Verdana";
    static const FLOAT msc_fontSize = 50;
    HRESULT hr;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pD2DFactory);

    if (SUCCEEDED(hr))
    {
        
        // Create a DirectWrite factory.
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(m_pDWriteFactory),
            reinterpret_cast<IUnknown **>(&m_pDWriteFactory)
            );
    }
    if (SUCCEEDED(hr))
    {
        // Create a DirectWrite text format object.
        hr = m_pDWriteFactory->CreateTextFormat(
            msc_fontName,
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            msc_fontSize,
            L"", //locale
            &m_pTextFormat
            );
    }
    if (SUCCEEDED(hr))
    {
        // Center the text horizontally and vertically.
        m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

        m_pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
       

    }

    return hr;
}
```



<span data-ttu-id="cdb6d-111">Da [**idwrite tefactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) -und [**idwrite-Textformat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Objekte [geräteunabhängige Ressourcen](resources-and-resource-domains.md)sind, können Sie die Leistung einer Anwendung verbessern, indem Sie Sie nur einmal erstellen, anstatt Sie jedes Mal neu zu erstellen, wenn ein Frame gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-111">Because [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) objects are [device-independent resources](resources-and-resource-domains.md), you can improve an application's performance by creating them only one time, instead of re-creating them every time that a frame is rendered.</span></span>

<span data-ttu-id="cdb6d-112">Nachdem Sie das Textformat Objekt erstellt haben, können Sie es mit einem Renderziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-112">After you create the text format object, you can use it with a render target.</span></span> <span data-ttu-id="cdb6d-113">Der folgende Code zeichnet den Text mithilfe der [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode des *Renderziels (die m \_ prendertarget* -Variable).</span><span class="sxs-lookup"><span data-stu-id="cdb6d-113">The following code draws the text by using the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method of the render target (the *m\_pRenderTarget* variable).</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="the-drawtextlayout-method"></a><span data-ttu-id="cdb6d-114">Die drawtextlayout-Methode</span><span class="sxs-lookup"><span data-stu-id="cdb6d-114">The DrawTextLayout Method</span></span>

<span data-ttu-id="cdb6d-115">Die [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode rendert ein [**idwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-115">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method renders an [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="cdb6d-116">Mit dieser Methode können Sie mehrere Formate auf einen Textblock anwenden (z. b. einen Teil des Texts unterstreichen), erweiterte OpenType-Features verwenden oder die Unterstützung für Treffer Tests durchführen.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-116">Use this method to apply multiple formats to a block of text (such as underlining a part of text), to use advanced OpenType features, or to perform hit testing support.</span></span>

<span data-ttu-id="cdb6d-117">Die [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode bietet auch Leistungsvorteile beim wiederholten zeichnen desselben Texts.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-117">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method also provides performance benefits for drawing the same text repeatedly.</span></span> <span data-ttu-id="cdb6d-118">Das [**idwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt misst und legt den Text fest, wenn Sie es erstellen.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-118">The [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object measures and lays out its text when you create it.</span></span> <span data-ttu-id="cdb6d-119">Wenn Sie ein **idwrite-Textlayout** -Objekt nur ein Mal erstellen und es jedes Mal wieder verwenden, wenn Sie den Text neu zeichnen müssen, wird die Leistung verbessert, da das System den Text nicht mehr messen und anordnen muss.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-119">If you create an **IDWriteTextLayout** object only one time and reuse it every time that you have to redraw the text, the performance improves because the system does not have to measure and lay out the text again.</span></span>

<span data-ttu-id="cdb6d-120">Bevor Sie die [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode verwenden können, müssen Sie [**idschreitefactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) zum Erstellen von [**idwrite-Textformat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -und [**idwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekten verwenden.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-120">Before you can use the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, you must use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) and [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) objects.</span></span> <span data-ttu-id="cdb6d-121">Nachdem diese Objekte erstellt wurden, wird die **drawtextlayout** -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cdb6d-121">After these objects are created, call the **DrawTextLayout** method.</span></span>

<span data-ttu-id="cdb6d-122">Weitere Informationen und Beispiele finden Sie in der Übersicht über [Text Formatierung und Layout](/windows/desktop/DirectWrite/text-formatting-and-layout) .</span><span class="sxs-lookup"><span data-stu-id="cdb6d-122">For more information and examples, see the [Text Formatting and Layout](/windows/desktop/DirectWrite/text-formatting-and-layout) overview.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdb6d-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cdb6d-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cdb6d-124">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="cdb6d-124">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>
</dt> <dt>

[<span data-ttu-id="cdb6d-125">**Drawtextlayout**</span><span class="sxs-lookup"><span data-stu-id="cdb6d-125">**DrawTextLayout**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[<span data-ttu-id="cdb6d-126">**Idschreitetextformat**</span><span class="sxs-lookup"><span data-stu-id="cdb6d-126">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="cdb6d-127">**Idschreitetextlayout**</span><span class="sxs-lookup"><span data-stu-id="cdb6d-127">**IDWriteTextLayout**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="cdb6d-128">Text Formatierung und Layout</span><span class="sxs-lookup"><span data-stu-id="cdb6d-128">Text Formatting and Layout</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 