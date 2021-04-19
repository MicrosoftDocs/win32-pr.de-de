---
title: ID2D1RenderTarget DrawEllipse-Methoden (D2d1. h)
description: Zeichnet den Umriss einer Ellipse mit den angegebenen Dimensionen und dem angegebenen Strich.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- DrawEllipse-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370010"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a>ID2D1RenderTarget::D rawellipse-Methoden

Zeichnet den Umriss einer Ellipse mit den angegebenen Dimensionen und dem angegebenen Strich.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                 | BESCHREIBUNG                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**DrawEllipse (D2D1 \_ Ellipse&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))  | Zeichnet den Umriss der angegebenen Ellipse mit dem angegebenen Strich Stil. <br/> |
| [**DrawEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) | Zeichnet den Umriss der angegebenen Ellipse mit dem angegebenen Strich Stil. <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn ein Fehler auftritt, wird von der **DrawEllipse** -Methode kein Fehlercode zurückgegeben. Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **DrawEllipse**) fehlgeschlagen ist, überprüfen Sie das Ergebnis, das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegeben wurde

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Zeichnen und Ausfüllen einer einfachen Form](how-to-draw-an-ellipse.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))
</dt> </dl>

�

�
