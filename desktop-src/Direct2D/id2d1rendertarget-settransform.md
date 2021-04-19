---
title: ID2D1RenderTarget setTransform-Methoden
description: Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- SetTransform-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362166"
---
# <a name="id2d1rendertargetsettransform-methods"></a>ID2D1RenderTarget:: setTransform-Methoden

Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                              | BESCHREIBUNG                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum. <br/> |
| [**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.<br/>  |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **setTransform** -Methode verwendet, um eine Drehung auf das Renderziel anzuwenden. Das komplette Beispiel finden Sie unter Gewusst [wie: Drehen eines Objekts](how-to-rotate.md).


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



Weitere Beispiele, die zeigen, wie Sie ein Renderziel transformieren, finden Sie unter [Skalieren eines Objekts](how-to-scale.md), Vorgehens [Weise beim Verzerren eines](how-to-skew.md)Objekts und [Übersetzen eines Objekts](how-to-translate.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Übersicht über Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Drehen eines Objekts](how-to-rotate.md)
</dt> <dt>

[Skalieren eines Objekts](how-to-scale.md)
</dt> <dt>

[Vorgehensweise beim Verzerren eines Objekts](how-to-skew.md)
</dt> <dt>

[Übersetzen eines Objekts](how-to-translate.md)
</dt> <dt>

[Anwenden mehrerer Transformationen auf ein Objekt](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

