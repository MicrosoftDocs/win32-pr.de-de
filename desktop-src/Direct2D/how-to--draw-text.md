---
title: Zeichnen von Text
description: Zeigt, wie Text mit Direct2D gerendert wird.
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd841f3b07edbde5e3fc6ed70f679cd58b3725f4
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349969"
---
# <a name="how-to-draw-text"></a><span data-ttu-id="f22c6-103">Zeichnen von Text</span><span class="sxs-lookup"><span data-stu-id="f22c6-103">How to Draw Text</span></span>

<span data-ttu-id="f22c6-104">Verwenden Sie zum Zeichnen von Text mit Direct2D die [**ID2D1RenderTarget::D rawText-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) für Text mit einem einzelnen Format.</span><span class="sxs-lookup"><span data-stu-id="f22c6-104">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format.</span></span> <span data-ttu-id="f22c6-105">Oder verwenden Sie die [**ID2D1RenderTarget::D rawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) für mehrere Formate, erweiterte OpenType-Features oder Treffertests.</span><span class="sxs-lookup"><span data-stu-id="f22c6-105">Or, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method for multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="f22c6-106">Diese Methoden verwenden die DirectWrite-API, um eine hochwertige Textanzeige zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f22c6-106">These methods use the DirectWrite API to provide high-quality text display.</span></span>

## <a name="the-drawtext-method"></a><span data-ttu-id="f22c6-107">Die DrawText-Methode</span><span class="sxs-lookup"><span data-stu-id="f22c6-107">The DrawText Method</span></span>

<span data-ttu-id="f22c6-108">Verwenden Sie zum Zeichnen von Text mit einem einzelnen Format die [**DrawText-Methode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="f22c6-108">To draw text that has a single format, use the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method.</span></span> <span data-ttu-id="f22c6-109">Um diese Methode zu verwenden, verwenden Sie zunächst eine [**IDWriteFactory,**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) um eine [**IDWriteTextFormat-Instanz zu**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) erstellen.</span><span class="sxs-lookup"><span data-stu-id="f22c6-109">To use this method, first use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) instance.</span></span>

<span data-ttu-id="f22c6-110">Der folgende Code erstellt ein [**IDWriteTextFormat-Objekt**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) und speichert es in der *Variablen m \_ pTextFormat.*</span><span class="sxs-lookup"><span data-stu-id="f22c6-110">The following code creates an [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) object and stores it in the *m\_pTextFormat* variable.</span></span>


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



<span data-ttu-id="f22c6-111">Da [**es sich bei IDWriteFactory-**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) und [**IDWriteTextFormat-Objekten**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) um geräteunabhängige Ressourcen handelt, können Sie die Leistung einer Anwendung verbessern, indem Sie sie nur einmal erstellen, anstatt sie jedes Mal neu zu erstellen, wenn ein Frame gerendert wird. [](resources-and-resource-domains.md)</span><span class="sxs-lookup"><span data-stu-id="f22c6-111">Because [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) objects are [device-independent resources](resources-and-resource-domains.md), you can improve an application's performance by creating them only one time, instead of re-creating them every time that a frame is rendered.</span></span>

<span data-ttu-id="f22c6-112">Nachdem Sie das Textformatobjekt erstellt haben, können Sie es mit einem Renderziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="f22c6-112">After you create the text format object, you can use it with a render target.</span></span> <span data-ttu-id="f22c6-113">Der folgende Code zeichnet den Text mithilfe der [**DrawText-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) des Renderziels *(die Variable m \_ pRenderTarget).*</span><span class="sxs-lookup"><span data-stu-id="f22c6-113">The following code draws the text by using the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method of the render target (the *m\_pRenderTarget* variable).</span></span>


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



## <a name="the-drawtextlayout-method"></a><span data-ttu-id="f22c6-114">Die DrawTextLayout-Methode</span><span class="sxs-lookup"><span data-stu-id="f22c6-114">The DrawTextLayout Method</span></span>

<span data-ttu-id="f22c6-115">Die [**DrawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) rendert ein [**IDWriteTextLayout-Objekt.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="f22c6-115">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method renders an [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="f22c6-116">Verwenden Sie diese Methode, um mehrere Formate auf einen Textblock anzuwenden (z. B. das Unterlining eines Teils des Texts), erweiterte OpenType-Features zu verwenden oder Treffertests zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f22c6-116">Use this method to apply multiple formats to a block of text (such as underlining a part of text), to use advanced OpenType features, or to perform hit testing support.</span></span>

<span data-ttu-id="f22c6-117">Die [**DrawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) bietet auch Leistungsvorteile für das wiederholte Zeichnen desselben Texts.</span><span class="sxs-lookup"><span data-stu-id="f22c6-117">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method also provides performance benefits for drawing the same text repeatedly.</span></span> <span data-ttu-id="f22c6-118">Das [**IDWriteTextLayout-Objekt**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) misst und legt seinen Text fest, wenn Sie es erstellen.</span><span class="sxs-lookup"><span data-stu-id="f22c6-118">The [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object measures and lays out its text when you create it.</span></span> <span data-ttu-id="f22c6-119">Wenn Sie ein **IDWriteTextLayout-Objekt** nur einmal erstellen und jedes Mal wiederverwenden, wenn Sie den Text neu gezeichnet haben, verbessert sich die Leistung, da das System den Text nicht erneut messen und neu erstellen muss.</span><span class="sxs-lookup"><span data-stu-id="f22c6-119">If you create an **IDWriteTextLayout** object only one time and reuse it every time that you have to redraw the text, the performance improves because the system does not have to measure and lay out the text again.</span></span>

<span data-ttu-id="f22c6-120">Bevor Sie die [**DrawTextLayout-Methode verwenden**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) können, müssen Sie [**eine IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) verwenden, um [**IDWriteTextFormat-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) und [**IDWriteTextLayout-Objekte zu**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) erstellen.</span><span class="sxs-lookup"><span data-stu-id="f22c6-120">Before you can use the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, you must use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) and [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) objects.</span></span> <span data-ttu-id="f22c6-121">Nachdem diese Objekte erstellt wurden, rufen Sie die **DrawTextLayout-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="f22c6-121">After these objects are created, call the **DrawTextLayout** method.</span></span>

<span data-ttu-id="f22c6-122">Weitere Informationen und Beispiele finden Sie in der [Übersicht über Textformatierung und Layout.](/windows/desktop/DirectWrite/text-formatting-and-layout)</span><span class="sxs-lookup"><span data-stu-id="f22c6-122">For more information and examples, see the [Text Formatting and Layout](/windows/desktop/DirectWrite/text-formatting-and-layout) overview.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f22c6-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f22c6-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f22c6-124">[**Drawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="f22c6-124">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>
</dt> <dt>

[<span data-ttu-id="f22c6-125">**DrawTextLayout**</span><span class="sxs-lookup"><span data-stu-id="f22c6-125">**DrawTextLayout**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[<span data-ttu-id="f22c6-126">**Idwritetextformat**</span><span class="sxs-lookup"><span data-stu-id="f22c6-126">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="f22c6-127">**Idwritetextlayout**</span><span class="sxs-lookup"><span data-stu-id="f22c6-127">**IDWriteTextLayout**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="f22c6-128">Textformatierung und Layout</span><span class="sxs-lookup"><span data-stu-id="f22c6-128">Text Formatting and Layout</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
