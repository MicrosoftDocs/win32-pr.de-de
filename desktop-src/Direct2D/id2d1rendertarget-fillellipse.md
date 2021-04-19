---
title: ID2D1RenderTarget FillEllipse-Methoden (D2d1. h)
description: Zeichnet das Innere der angegebenen Ellipse.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- FillEllipse-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359246"
---
# <a name="id2d1rendertargetfillellipse-methods"></a>ID2D1RenderTarget:: FillEllipse-Methoden

Zeichnet das Innere der angegebenen Ellipse.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                             | BESCHREIBUNG                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| [**FillEllipse (D2D1 \_ Ellipse&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))  | Zeichnet das Innere der angegebenen Ellipse. <br/> |
| [**FillEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) | Zeichnet das Innere der angegebenen Ellipse. <br/> |



## <a name="remarks"></a>Bemerkungen

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **FillEllipse**) fehlgeschlagen ist, überprüfen Sie das Ergebnis, das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegeben wurde

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

[Zeichnen und Ausfüllen einer einfachen Form](how-to-draw-an-ellipse.md)
</dt> </dl>

�

�
