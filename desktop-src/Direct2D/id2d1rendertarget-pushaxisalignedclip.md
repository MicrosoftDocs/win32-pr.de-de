---
title: ID2D1RenderTarget PushAxisAlignedClip-Methoden (D2d1 \_ 1.h)
description: Gibt ein Rechteck an, an das alle nachfolgenden Zeichnungsvorgänge abgeschnitten werden.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- PushAxisAlignedClip-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3ce76db0608ccd79ecd8ea1be716f8cbdf4313f95bfdda9cfac7b63474e3f412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873990"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget::P ushAxisAlignedClip-Methoden

Gibt ein Rechteck an, an das alle nachfolgenden Zeichnungsvorgänge abgeschnitten werden.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                         | Beschreibung                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip(D2D1 \_ RECT \_ F&,D2D1 \_ ANTIALIAS \_ MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Gibt ein Rechteck an, an das alle nachfolgenden Zeichnungsvorgänge abgeschnitten werden. <br/> |
| [**PushAxisAlignedClip(D2D1 \_ RECT \_ F \* ,D2D1 \_ ANTIALIAS \_ MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Gibt ein Rechteck an, an das alle nachfolgenden Zeichnungsvorgänge abgeschnitten werden. <br/> |



## <a name="remarks"></a>Hinweise

Ein [**PushAxisAlignedClip-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) und [**PopAxisAlignedClip-Paar**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) kann um oder innerhalb von [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)auftreten, darf sich jedoch nicht überlappen. Beispielsweise ist die Sequenz von **PushAxisAlignedClip,** [**PushLayer,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) **PopLayer,** **PopAxisAlignedClip** gültig, aber die Sequenz von **PushAxisAlignedClip,** **PushLayer,** **PopAxisAlignedClip** und **PopLayer** ist ungültig.

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Überprüfen Sie das von den Methoden [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis, um zu ermitteln, ob bei einem Zeichnungsvorgang (z. B. **PushAxisAlignedClip)** ein Fehler auftrat.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1.h (einschließlich D2d1.h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
