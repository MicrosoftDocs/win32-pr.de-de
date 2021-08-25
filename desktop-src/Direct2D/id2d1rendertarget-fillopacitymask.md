---
title: ID2D1RenderTarget FillOpacityMask-Methoden
description: Wendet die von der angegebenen Bitmap beschriebene Deckkraftmaske auf einen Pinsel an und verwendet diesen Pinsel, um einen Bereich des Renderziels zu zeichnen.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- FillOpacityMask-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 362043696e4cbd21dd64783f210cf2e24066645e7dac5e303a16cd83abb31307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874080"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>ID2D1RenderTarget::FillOpacityMask-Methoden

Wendet die von der angegebenen Bitmap beschriebene Deckkraftmaske auf einen Pinsel an und verwendet diesen Pinsel, um einen Bereich des Renderziels zu zeichnen.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**FillOpacityMask(ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ OPACITY \_ MASK \_ CONTENT,D2D \_ RECT F \_&,D2D \_ RECT F \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | Wendet die von der angegebenen Bitmap beschriebene Deckkraftmaske auf einen Pinsel an und verwendet diesen Pinsel, um einen Bereich des Renderziels zu zeichnen. <br/> |
| [**FillOpacityMask(ID2D1Bitmap \* ,ID2D1Brush \* ,D2D1 \_ OPACITY \_ MASK \_ CONTENT,D2D \_ RECT F \_ \* ,D2D \_ RECT F \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | Wendet die von der angegebenen Bitmap beschriebene Deckkraftmaske auf einen Pinsel an und verwendet diesen Pinsel, um einen Bereich des Renderziels zu zeichnen. <br/> |



## <a name="remarks"></a>Hinweise

Damit diese Methode ordnungsgemäß funktioniert, muss das Renderziel den [**Antialiasingmodus D2D1 \_ ANTIALIAS \_ MODE \_ ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) verwenden. Sie können den Antialiasingmodus festlegen, indem Sie die [**ID2D1RenderTarget::SetAntialiasMode-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) aufrufen.

Diese Methode gibt bei einem Fehler keinen Fehlercode zurück. Um zu bestimmen, ob bei einem Zeichnungsvorgang (z. B. **FillOpacityMask)** ein Fehler aufgetreten ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

