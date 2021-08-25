---
title: Rendern mit Direct2D
description: Direct2D bietet Methoden zum Rendern von Text mit Formatierung, die nur durch ein IDWriteTextFormat oder ein IDWriteTextLayout auf einer Direct2D-Oberfläche beschrieben wird.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad297a8fdf2078c966989baf5e81c69cf515427340f8de8d073035fcf98f434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048480"
---
# <a name="render-using-direct2d"></a>Rendern mit Direct2D

Direct2D bietet Methoden zum Rendern von Text mit Formatierung, die nur durch [**ein IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) oder ein [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) auf einer Direct2D-Oberfläche beschrieben wird.

## <a name="rendering-text-described-by-idwritetextformat"></a>Renderingtext, der von IDWriteTextFormat beschrieben wird

Um eine Zeichenfolge mithilfe eines [**IDWriteTextFormat-Objekts**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) zu rendern, um die Formatierung für die gesamte Zeichenfolge zu beschreiben, verwenden Sie die [**id2D1RenderTarget::D rawText-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) die von [Direct2D](../direct2d/direct2d-portal.md)bereitgestellt wird.

1.  Definieren Sie den Bereich für das Textlayout, indem Sie die Dimensionen des Renderingbereichs abrufen, und erstellen Sie ein [Direct2D-Rechteck](../direct2d/direct2d-portal.md) mit den gleichen Dimensionen.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Verwenden Sie [**die ID2D1RenderTarget::D rawText-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) und das [**IDWriteTextFormat-Objekt,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) um Text auf dem Bildschirm zu rendern. Die **ID2D1RenderTarget::D rawText-Methode** nimmt die folgenden Parameter an:
    -   Eine zu rendernde Zeichenfolge.
    -   Ein Zeiger auf eine [**IDWriteTextFormat-Schnittstelle.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
    -   Ein [Direct2D-Layoutrechteck.](../direct2d/direct2d-portal.md)
    -   Ein Zeiger auf eine Schnittstelle, die [**ID2D1Brush verfügbar macht.**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a>Rendern eines IDWriteText-Layoutobjekts

Um den Text mit den vom [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) angegebenen Textlayouteinstellungen zu zeichnen, ändern Sie den Code in der MultiformattedText::D rawText-Methode so, dass [**IDWriteTextLayout::D rawTextLayout verwendet**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)wird.

1.  Entsorgen Sie [**eine D2D1 \_ POINT \_ 2F-Variable,**](../direct2d/d2d1-point-2f.md) und legen Sie sie auf den oberen linken Punkt des Fensters fest.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Zeichnen Sie den Text auf den Bildschirm, indem Sie die [**ID2D1RenderTarget::D rawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) des [Direct2D-Renderziels](../direct2d/direct2d-portal.md) aufrufen und den [**IDWriteTextLayout-Zeiger**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) übergeben.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 