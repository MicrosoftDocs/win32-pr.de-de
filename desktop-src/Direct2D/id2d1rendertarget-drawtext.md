---
title: ID2D1RenderTarget DrawText-Methoden
description: Zeichnet den angegebenen Text mithilfe der Formatinformationen, die von einem idschreitetextformat-Objekt bereitgestellt werden.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- DrawText-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371021"
---
# <a name="id2d1rendertargetdrawtext-methods"></a><span data-ttu-id="8840c-104">ID2D1RenderTarget::D rawtext-Methoden</span><span class="sxs-lookup"><span data-stu-id="8840c-104">ID2D1RenderTarget::DrawText methods</span></span>

<span data-ttu-id="8840c-105">Zeichnet den angegebenen Text mithilfe der Formatinformationen, die von einem [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8840c-105">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8840c-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="8840c-106">Overload list</span></span>



| <span data-ttu-id="8840c-107">Methode</span><span class="sxs-lookup"><span data-stu-id="8840c-107">Method</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="8840c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8840c-108">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8840c-109">[**DrawText (WChar \* , idschreitetextformat \* , D2D1 \_ Rect \_ F&, ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ options, dwrite \_ Text \_ Mess \_ method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="8840c-109">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F&,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>  | <span data-ttu-id="8840c-110">Zeichnet den angegebenen Text mithilfe der Formatinformationen, die von einem [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8840c-110">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span><br/>  |
| <span data-ttu-id="8840c-111">[**DrawText (WChar \* , idschreitetextformat \* , D2D1 \_ Rect \_ F \* , ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ options, dwrite \_ Text \_ Mess \_ method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="8840c-111">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F\*,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> | <span data-ttu-id="8840c-112">Zeichnet den angegebenen Text mithilfe der Formatinformationen, die von einem [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8840c-112">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8840c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8840c-113">Remarks</span></span>

<span data-ttu-id="8840c-114">Um Text mit Direct2D zu zeichnen, verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode für Text, der ein einzelnes Format aufweist, oder die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode, wenn Sie mehrere Formate, erweiterte OpenType-Funktionen oder Treffer Tests benötigen.</span><span class="sxs-lookup"><span data-stu-id="8840c-114">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format, or the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method when you need multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="8840c-115">Diese Methoden verwenden die DirectWrite-API, um eine hochwertige Textdarstellung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8840c-115">These methods use the DirectWrite API to provide high-quality text display.</span></span>

<span data-ttu-id="8840c-116">Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8840c-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="8840c-117">Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **DrawText**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="8840c-117">To determine whether a drawing operation (such as **DrawText**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="8840c-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8840c-118">Examples</span></span>

<span data-ttu-id="8840c-119">Ein Beispiel finden Sie unter Gewusst [wie: Zeichnen von Text](how-to--draw-text.md).</span><span class="sxs-lookup"><span data-stu-id="8840c-119">For an example, see [How to Draw Text](how-to--draw-text.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8840c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8840c-120">Requirements</span></span>



| <span data-ttu-id="8840c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8840c-121">Requirement</span></span> | <span data-ttu-id="8840c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8840c-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8840c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8840c-123">Library</span></span><br/> | <dl> <span data-ttu-id="8840c-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8840c-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="8840c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8840c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8840c-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8840c-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8840c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8840c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8840c-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="8840c-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="8840c-129">**Idschreitetextformat**</span><span class="sxs-lookup"><span data-stu-id="8840c-129">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="8840c-130">Zeichnen von Text</span><span class="sxs-lookup"><span data-stu-id="8840c-130">How to Draw Text</span></span>](how-to--draw-text.md)
</dt> <dt>

[<span data-ttu-id="8840c-131">Übersicht über Text Formatierung und Layout</span><span class="sxs-lookup"><span data-stu-id="8840c-131">Text Formatting and Layout Overview</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

