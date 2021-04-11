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
# <a name="render-using-direct2d"></a><span data-ttu-id="08aff-103">Rendering mithilfe von Direct2D</span><span class="sxs-lookup"><span data-stu-id="08aff-103">Render Using Direct2D</span></span>

<span data-ttu-id="08aff-104">Direct2D stellt Methoden zum Rendern von Text mit einer Formatierung bereit, die nur von einem [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) oder einem [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) auf eine Direct2D-Oberfläche beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="08aff-104">Direct2D provides methods for rendering either text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) or an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to a Direct2D surface.</span></span>

## <a name="rendering-text-described-by-idwritetextformat"></a><span data-ttu-id="08aff-105">Renderingtext, der von idschreitetextformat beschrieben wird</span><span class="sxs-lookup"><span data-stu-id="08aff-105">Rendering Text Described by IDWriteTextFormat</span></span>

<span data-ttu-id="08aff-106">Verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode, die von [Direct2D](../direct2d/direct2d-portal.md)bereitgestellt wird, um eine Zeichenfolge mithilfe eines [**idwrite Items Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekts zu renderingelemente zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="08aff-106">To render a string using an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to describe the formatting for the entire string, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method provided by [Direct2D](../direct2d/direct2d-portal.md).</span></span>

1.  <span data-ttu-id="08aff-107">Definieren Sie den Bereich für das Text Layout, indem Sie die Dimensionen des Renderingbereichs abrufen, und erstellen Sie ein [Direct2D](../direct2d/direct2d-portal.md) -Rechteck, das die gleichen Dimensionen aufweist.</span><span class="sxs-lookup"><span data-stu-id="08aff-107">Define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="08aff-108">Verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode und das [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt, um Text auf dem Bildschirm zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="08aff-108">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="08aff-109">Die **ID2D1RenderTarget::D rawtext** -Methode übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="08aff-109">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="08aff-110">Eine zu Rendering-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="08aff-110">A string to render.</span></span>
    -   <span data-ttu-id="08aff-111">Ein Zeiger auf eine [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="08aff-111">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="08aff-112">Ein [Direct2D](../direct2d/direct2d-portal.md) -Layoutrechteck.</span><span class="sxs-lookup"><span data-stu-id="08aff-112">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="08aff-113">Ein Zeiger auf eine-Schnittstelle, die [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="08aff-113">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a><span data-ttu-id="08aff-114">Rendern eines idwrite-Text-Layoutobjekte</span><span class="sxs-lookup"><span data-stu-id="08aff-114">Rendering a IDWriteText Layout Object</span></span>

<span data-ttu-id="08aff-115">Ändern Sie den Code in der multiformattedtext::D rawtext-Methode, um [**idschreitetextlayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)zu verwenden, um den Text mit den textlayouteinstellungen zu zeichnen, die vom [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08aff-115">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="08aff-116">Sie müssen eine [**D2D1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) -Variable und die Variable auf den oberen linken Punkt des Fensters festlegen.</span><span class="sxs-lookup"><span data-stu-id="08aff-116">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="08aff-117">Zeichnen Sie den Text auf dem Bildschirm, indem Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode des [Direct2D](../direct2d/direct2d-portal.md) -Renderziels aufrufen und den [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Zeiger übergeben.</span><span class="sxs-lookup"><span data-stu-id="08aff-117">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 