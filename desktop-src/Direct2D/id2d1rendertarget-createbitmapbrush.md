---
title: ID2D1RenderTarget CreateBitmapBrush-Methoden
description: Erstellt einen ID2D1BitmapBrush aus der angegebenen Bitmap.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- CreateBitmapBrush-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 411ae2dd81fce88bec5d6a3717fe79d942de84f060c53a90b83cae461d6a49de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053090"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>ID2D1RenderTarget::CreateBitmapBrush-Methoden

Erstellt einen [**ID2D1BitmapBrush aus**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) der angegebenen Bitmap.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush(ID2D1Bitmap \* ,D2D1 \_ BITMAP BRUSH PROPERTIES \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Erstellt einen [**ID2D1BitmapBrush aus**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) der angegebenen Bitmap.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap \* ,D2D1 \_ BITMAP BRUSH PROPERTIES \_ \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Erstellt einen [**ID2D1BitmapBrush aus**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) der angegebenen Bitmap.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap \* ,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Erstellt einen [**ID2D1BitmapBrush aus**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) der angegebenen Bitmap. Der Pinsel verwendet die Standardwerte für den Erweiterungsmodus, interpolierten Modus, die Deckkraft und die Transformation.<br/> |
| [**CreateBitmapBrush(ID2D1Bitmap \* , D2D1 \_ BITMAP BRUSH PROPERTIES \_ \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Erstellt einen [**ID2D1BitmapBrush aus**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) der angegebenen Bitmap. Der Pinsel verwendet die Standardwerte für seine Deckkraft und Transformation.<br/>                                   |



## <a name="examples"></a>Beispiele

Ein Beispiel zum Zeichnen eines Bereichs mit einem Bitmappinsel finden Sie unter Erstellen eines [Bitmappinsels.](how-to-create-a-bitmap-brush.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Erstellen eines Bitmappinsels](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>

 

