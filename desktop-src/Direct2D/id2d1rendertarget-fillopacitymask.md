---
title: ID2D1RenderTarget fillopacitymask-Methoden
description: Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Fillopacitymask-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368304"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>ID2D1RenderTarget:: fillopacitymask-Methoden

Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fillopacitymask (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ Opacity \_ mask \_ Content, D2D \_ Rect \_ f&, D2D \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels. <br/> |
| [**Fillopacitymask (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ Opacity \_ mask \_ Content, D2D \_ Rect \_ f \* , D2D \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels. <br/> |



## <a name="remarks"></a>Bemerkungen

Damit diese Methode ordnungsgemäß funktioniert, muss das Renderziel den Antialiasing-Modus für den [**D2D1- \_ Antialias \_ Modus \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) verwenden. Sie können den Antialiasing Modus festlegen, indem Sie die [**ID2D1RenderTarget:: setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) -Methode aufrufen.

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **fillopacitymask**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

