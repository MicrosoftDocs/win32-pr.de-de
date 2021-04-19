---
title: ID2D1RenderTarget-Methode
description: Erstellt ein ID2D1BitmapBrush-aus der angegebenen Bitmap.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- Methoden der Methode "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: fcd512393a3f037cd3def40d4aa55003d9fddcef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355963"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>ID2D1RenderTarget:: kreatebitmapbrush-Methoden

Erstellt ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -aus der angegebenen Bitmap.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kreatebitmapbrush (ID2D1Bitmap \* , D2D1 \_ Bitmap \_ Brush \_ Properties&, D2D1 \_ Brush \_ Properties&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Erstellt ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -aus der angegebenen Bitmap.<br/>                                                                                                    |
| [**Kreatebitmapbrush (ID2D1Bitmap \* , D2D1 \_ Bitmap- \_ Pinsel \_ Eigenschaften \* , D2D1 \_ Brush- \_ Eigenschaften \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Erstellt ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -aus der angegebenen Bitmap.<br/>                                                                                                    |
| [**"Kreatebitmapbrush" (ID2D1Bitmap \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Erstellt ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -aus der angegebenen Bitmap. Der Pinsel verwendet die Standardwerte für den Erweiterungsmodus, Interpolations Modus, Deckkraft und Transformation.<br/> |
| [**"Kreatebitmapbrush" (ID2D1Bitmap \* , D2D1 \_ Bitmap \_ Brush \_ Properties&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Erstellt ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -aus der angegebenen Bitmap. Der Pinsel verwendet die Standardwerte für seine Deckkraft und Transformation.<br/>                                   |



## <a name="examples"></a>Beispiele

Ein Beispiel für das Zeichnen eines Bereichs mit einem Bitmap-Pinsel finden Sie unter [Erstellen eines bitmappinsels](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Erstellen eines Bitmap-Pinsels](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>

 

