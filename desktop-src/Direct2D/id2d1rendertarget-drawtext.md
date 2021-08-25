---
title: ID2D1RenderTarget DrawText-Methoden
description: Zeichnet den angegebenen Text mithilfe der Von einem IDWriteTextFormat-Objekt bereitgestellten Formatinformationen.
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
ms.openlocfilehash: 430607b09795be249a05398b1bfb749e9be45ae517c6374e001a4c3042bf316f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874190"
---
# <a name="id2d1rendertargetdrawtext-methods"></a>ID2D1RenderTarget::D rawText-Methoden

Zeichnet den angegebenen Text mithilfe der Von einem [**IDWriteTextFormat-Objekt bereitgestellten Formatinformationen.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText(WCHAR \* ,IDWriteTextFormat \* ,D2D1 \_ RECT \_ F&,ID2D1Brush \* ,D2D1 \_ DRAW \_ TEXT \_ OPTIONS,DWRITE \_ TEXT \_ MEASURING \_ METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Zeichnet den angegebenen Text mithilfe der Von einem [**IDWriteTextFormat-Objekt bereitgestellten Formatinformationen.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)<br/>  |
| [**DrawText(WCHAR \* , IDWriteTextFormat \* ,D2D1 \_ RECT F , \_ \* ID2D1Brush \* ,D2D1 \_ DRAW TEXT \_ \_ OPTIONS,DWRITE \_ TEXT MEASURING \_ \_ METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Zeichnet den angegebenen Text mithilfe der Von einem [**IDWriteTextFormat-Objekt bereitgestellten Formatinformationen.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) <br/> |



## <a name="remarks"></a>Hinweise

Verwenden Sie zum Zeichnen von Text mit Direct2D die [**ID2D1RenderTarget::D rawText-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) für Text mit einem einzelnen Format oder die [**ID2D1RenderTarget::D rawTextLayout-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) wenn Sie mehrere Formate, erweiterte OpenType-Features oder Treffertests benötigen. Diese Methoden verwenden die DirectWrite-API, um eine hochwertige Textanzeige zu ermöglichen.

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Um zu bestimmen, ob ein Zeichnungsvorgang (z. B. **DrawText**) fehlgeschlagen ist, überprüfen Sie das von den [**Methoden ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Zeichnen von Text.](how-to--draw-text.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**Idwritetextformat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Zeichnen von Text](how-to--draw-text.md)
</dt> <dt>

[Übersicht über Textformatierung und Layout](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

