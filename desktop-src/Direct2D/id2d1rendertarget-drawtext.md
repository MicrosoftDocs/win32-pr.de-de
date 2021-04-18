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
# <a name="id2d1rendertargetdrawtext-methods"></a>ID2D1RenderTarget::D rawtext-Methoden

Zeichnet den angegebenen Text mithilfe der Formatinformationen, die von einem [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Objekt bereitgestellt werden.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText (WChar \* , idschreitetextformat \* , D2D1 \_ Rect \_ F&, ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ options, dwrite \_ Text \_ Mess \_ method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Zeichnet den angegebenen Text mithilfe der Formatinformationen, die von einem [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Objekt bereitgestellt werden.<br/>  |
| [**DrawText (WChar \* , idschreitetextformat \* , D2D1 \_ Rect \_ F \* , ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ options, dwrite \_ Text \_ Mess \_ method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Zeichnet den angegebenen Text mithilfe der Formatinformationen, die von einem [**idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) -Objekt bereitgestellt werden. <br/> |



## <a name="remarks"></a>Bemerkungen

Um Text mit Direct2D zu zeichnen, verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode für Text, der ein einzelnes Format aufweist, oder die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode, wenn Sie mehrere Formate, erweiterte OpenType-Funktionen oder Treffer Tests benötigen. Diese Methoden verwenden die DirectWrite-API, um eine hochwertige Textdarstellung bereitzustellen.

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **DrawText**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter Gewusst [wie: Zeichnen von Text](how-to--draw-text.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**Idschreitetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Zeichnen von Text](how-to--draw-text.md)
</dt> <dt>

[Übersicht über Text Formatierung und Layout](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

