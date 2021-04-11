---
title: Rendering mithilfe von Direct2D
description: Direct2D stellt Methoden zum Rendern von Text mit einer Formatierung bereit, die nur von einem idwrite-Textformat oder einem idwrite-TextLayout auf eine Direct2D-Oberfläche beschrieben wird.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039531"
---
# <a name="render-using-direct2d"></a>Rendering mithilfe von Direct2D

Direct2D stellt Methoden zum Rendern von Text mit einer Formatierung bereit, die nur von einem [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) oder einem [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) auf eine Direct2D-Oberfläche beschrieben wird.

## <a name="rendering-text-described-by-idwritetextformat"></a>Renderingtext, der von idschreitetextformat beschrieben wird

Verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode, die von [Direct2D](../direct2d/direct2d-portal.md)bereitgestellt wird, um eine Zeichenfolge mithilfe eines [**idwrite Items Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekts zu renderingelemente zu beschreiben.

1.  Definieren Sie den Bereich für das Text Layout, indem Sie die Dimensionen des Renderingbereichs abrufen, und erstellen Sie ein [Direct2D](../direct2d/direct2d-portal.md) -Rechteck, das die gleichen Dimensionen aufweist.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode und das [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt, um Text auf dem Bildschirm zu Rendering. Die **ID2D1RenderTarget::D rawtext** -Methode übernimmt die folgenden Parameter:
    -   Eine zu Rendering-Zeichenfolge.
    -   Ein Zeiger auf eine [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle.
    -   Ein [Direct2D](../direct2d/direct2d-portal.md) -Layoutrechteck.
    -   Ein Zeiger auf eine-Schnittstelle, die [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)verfügbar macht.

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a>Rendern eines idwrite-Text-Layoutobjekte

Ändern Sie den Code in der multiformattedtext::D rawtext-Methode, um [**idschreitetextlayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)zu verwenden, um den Text mit den textlayouteinstellungen zu zeichnen, die vom [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt angegeben werden.

1.  Sie müssen eine [**D2D1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) -Variable und die Variable auf den oberen linken Punkt des Fensters festlegen.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Zeichnen Sie den Text auf dem Bildschirm, indem Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode des [Direct2D](../direct2d/direct2d-portal.md) -Renderziels aufrufen und den [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Zeiger übergeben.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 