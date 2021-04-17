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
# <a name="how-to-draw-text"></a>Zeichnen von Text

Um Text mit Direct2D zu zeichnen, verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode für Text, der ein einzelnes Format aufweist. Oder verwenden Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode für mehrere Formate, erweiterte OpenType-Funktionen oder Treffer Tests. Diese Methoden verwenden die DirectWrite-API, um eine hochwertige Textdarstellung bereitzustellen.

## <a name="the-drawtext-method"></a>Die DrawText-Methode

Um Text mit einem einzelnen Format zu zeichnen, verwenden Sie die [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode. Um diese Methode zu verwenden, verwenden Sie zuerst einen [**idwrite-Factory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) , um eine [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Instanz zu erstellen.

Der folgende Code erstellt ein [**idschreitetextformat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Objekt und speichert es in der *m \_ ptextformat* -Variablen.


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



Da [**idwrite tefactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) -und [**idwrite-Textformat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Objekte [geräteunabhängige Ressourcen](resources-and-resource-domains.md)sind, können Sie die Leistung einer Anwendung verbessern, indem Sie Sie nur einmal erstellen, anstatt Sie jedes Mal neu zu erstellen, wenn ein Frame gerendert wird.

Nachdem Sie das Textformat Objekt erstellt haben, können Sie es mit einem Renderziel verwenden. Der folgende Code zeichnet den Text mithilfe der [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode des *Renderziels (die m \_ prendertarget* -Variable).


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



## <a name="the-drawtextlayout-method"></a>Die drawtextlayout-Methode

Die [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode rendert ein [**idwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt. Mit dieser Methode können Sie mehrere Formate auf einen Textblock anwenden (z. b. einen Teil des Texts unterstreichen), erweiterte OpenType-Features verwenden oder die Unterstützung für Treffer Tests durchführen.

Die [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode bietet auch Leistungsvorteile beim wiederholten zeichnen desselben Texts. Das [**idwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt misst und legt den Text fest, wenn Sie es erstellen. Wenn Sie ein **idwrite-Textlayout** -Objekt nur ein Mal erstellen und es jedes Mal wieder verwenden, wenn Sie den Text neu zeichnen müssen, wird die Leistung verbessert, da das System den Text nicht mehr messen und anordnen muss.

Bevor Sie die [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode verwenden können, müssen Sie [**idschreitefactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) zum Erstellen von [**idwrite-Textformat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -und [**idwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekten verwenden. Nachdem diese Objekte erstellt wurden, wird die **drawtextlayout** -Methode aufgerufen.

Weitere Informationen und Beispiele finden Sie in der Übersicht über [Text Formatierung und Layout](/windows/desktop/DirectWrite/text-formatting-and-layout) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))
</dt> <dt>

[**Drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[**Idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[**Idschreitetextlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[Text Formatierung und Layout](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 