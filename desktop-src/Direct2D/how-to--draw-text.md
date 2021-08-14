---
title: Zeichnen von Text
description: Zeigt, wie Text mit Direct2D gerendert wird.
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd9b98417d81cf1cd3222faf771f56cb009f9a327c44f0f0962feb9bf41cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259980"
---
# <a name="how-to-draw-text"></a>Zeichnen von Text

Verwenden Sie zum Zeichnen von Text mit Direct2D die [**ID2D1RenderTarget::D rawText-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) für Text mit einem einzelnen Format. Verwenden Sie alternativ die [**ID2D1RenderTarget::D rawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) für mehrere Formate, erweiterte OpenType-Features oder Treffertests. Diese Methoden verwenden die DirectWrite-API, um eine hochwertige Textanzeige bereitzustellen.

## <a name="the-drawtext-method"></a>Die DrawText-Methode

Verwenden Sie die [**DrawText-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) um Text mit einem einzelnen Format zu zeichnen. Um diese Methode zu verwenden, verwenden Sie zunächst eine [**IDWriteFactory,**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) um eine [**IDWriteTextFormat-Instanz**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) zu erstellen.

Der folgende Code erstellt ein [**IDWriteTextFormat-Objekt**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) und speichert es in der Variablen *m \_ pTextFormat.*


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



Da [**idWriteFactory-**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) und [**IDWriteTextFormat-Objekte**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [geräteunabhängige Ressourcen](resources-and-resource-domains.md)sind, können Sie die Leistung einer Anwendung verbessern, indem Sie sie nur einmal erstellen, anstatt sie jedes Mal neu zu erstellen, wenn ein Frame gerendert wird.

Nachdem Sie das Textformatobjekt erstellt haben, können Sie es mit einem Renderziel verwenden. Der folgende Code zeichnet den Text mithilfe der [**DrawText-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) des Renderziels (variable *m \_ pRenderTarget).*


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



## <a name="the-drawtextlayout-method"></a>Die DrawTextLayout-Methode

Die [**DrawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) rendert ein [**IDWriteTextLayout-Objekt.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) Verwenden Sie diese Methode, um mehrere Formate auf einen Textblock anzuwenden (z. B. um einen Teil des Texts zu unterlinten), erweiterte OpenType-Features zu verwenden oder Treffertests durchzuführen.

Die [**DrawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) bietet auch Leistungsvorteile beim wiederholten Zeichnen desselben Texts. Das [**IDWriteTextLayout-Objekt**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) misst und legt seinen Text beim Erstellen fest. Wenn Sie ein **IDWriteTextLayout-Objekt** nur einmal erstellen und es jedes Mal wiederverwenden, wenn Sie den Text neu zeichnen müssen, verbessert sich die Leistung, da das System den Text nicht erneut messen und neu erstellen muss.

Bevor Sie die [**DrawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) verwenden können, müssen Sie [**idWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) verwenden, um [**IDWriteTextFormat-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) und [**IDWriteTextLayout-Objekte**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) zu erstellen. Nachdem diese Objekte erstellt wurden, rufen Sie die **DrawTextLayout-Methode** auf.

Weitere Informationen und Beispiele finden Sie in der Übersicht über [Textformatierung und Layout.](/windows/desktop/DirectWrite/text-formatting-and-layout)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Drawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))
</dt> <dt>

[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[**Idwritetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[**Idwritetextlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[Textformatierung und Layout](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
