---
title: ID2D1RenderTarget pushaxisalignedclip-Methoden (D2d1 \_ 1. h)
description: Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Pushaxisalignedclip-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361063"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget::P ushaxisalignedclip-Methoden

Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                         | BESCHREIBUNG                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Pushaxisalignedclip (D2D1 \_ Rect \_ F&, D2D1 \_ Antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden. <br/> |
| [**Pushaxisalignedclip (D2D1 \_ Rect \_ F \* , D2D1 \_ Antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden. <br/> |



## <a name="remarks"></a>Bemerkungen

Ein [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) -und [**popaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) -Paar kann um oder innerhalb einer [**pushschicht**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)auftreten, sich aber nicht überlappen. Beispielsweise ist die Sequenz von **pushaxisalignedclip**, [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **poplayer** und **popaxisalignedclip** gültig, aber die Sequenz von **pushaxisalignedclip**, **pushlayer**, **popaxisalignedclip** und **poplayer** ist ungültig.

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **pushaxisalignedclip**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.

## <a name="examples"></a>Beispiele

Ein Beispiel finden [Sie unter How to Clip with an Axis-Aligned Clip Rechteck](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1. h (Include D2d1. h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
