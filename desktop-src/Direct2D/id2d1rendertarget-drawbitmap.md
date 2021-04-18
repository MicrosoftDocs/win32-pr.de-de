---
title: ID2D1RenderTarget drawbitmap-Methoden
description: Zeichnet das angegebene ID2D1Bitmap.
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- Drawbitmap-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357585"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a>ID2D1RenderTarget::D rawbitmap-Methoden

Zeichnet das angegebene [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Drawbitmap (ID2D1Bitmap \* , D2D1 \_ Rect \_ f&, float, D2D1 \_ Bitmap \_ Interpolations \_ Mode, D2D1 \_ Rect \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))   | Zeichnet die angegebene Bitmap, nachdem Sie auf die Größe des angegebenen Rechtecks skaliert wurde. <br/> |
| [**Drawbitmap (ID2D1Bitmap \* , D2D1 \_ Rect \_ f&, float, D2D1 \_ Bitmap \_ Interpolations \_ Mode, D2D1 \_ Rect \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))  | Zeichnet die angegebene Bitmap, nachdem Sie auf die Größe des angegebenen Rechtecks skaliert wurde. <br/> |
| [**Drawbitmap (ID2D1Bitmap \* , D2D1 \_ Rect \_ f \* , float, D2D1 \_ Bitmap \_ Interpolations \_ Mode, D2D1 \_ Rect \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) | Zeichnet die angegebene Bitmap, nachdem Sie auf die Größe des angegebenen Rechtecks skaliert wurde. <br/> |



## <a name="remarks"></a>Bemerkungen

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **drawbitmap**) fehlgeschlagen ist, überprüfen Sie das Ergebnis, das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegeben wurde

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Zeichnen einer Bitmap](how-to-draw-a-bitmap.md). Ein Beispiel, das zeigt, wie eine Bitmap aus einer Ressource oder einer Datei geladen wird, finden Sie unter Gewusst wie: Laden einer Bitmap [aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md) und Gewusst wie: [Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Zeichnen einer Bitmap](how-to-draw-a-bitmap.md)
</dt> <dt>

[Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

