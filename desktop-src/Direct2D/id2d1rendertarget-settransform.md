---
title: ID2D1RenderTarget SetTransform-Methoden
description: Wendet die angegebene Transformation auf das Renderziel an und ersetzt die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.
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
ms.openlocfilehash: f23ffcd8d64df02b0be2287a33eff63a6a680200c0e051a15c77958dafd81438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873960"
---
# <a name="id2d1rendertargetsettransform-methods"></a>ID2D1RenderTarget::SetTransform-Methoden

Wendet die angegebene Transformation auf das Renderziel an und ersetzt die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                              | Beschreibung                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | Wendet die angegebene Transformation auf das Renderziel an und ersetzt die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum. <br/> |
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | Wendet die angegebene Transformation auf das Renderziel an und ersetzt die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.<br/>  |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **SetTransform-Methode** verwendet, um eine Drehung auf das Renderziel anzuwenden. Das vollständige Beispiel finden Sie unter [Rotieren eines Objekts.](how-to-rotate.md)


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



Weitere Beispiele zum Transformieren eines Renderziels finden Sie unter [How to Scale an Object](how-to-scale.md), How to [Skew an Object](how-to-skew.md)und How to Translate an [Object](how-to-translate.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Übersicht über Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Drehen eines Objekts](how-to-rotate.md)
</dt> <dt>

[Skalieren eines Objekts](how-to-scale.md)
</dt> <dt>

[Verzerren eines Objekts](how-to-skew.md)
</dt> <dt>

[Übersetzen eines Objekts](how-to-translate.md)
</dt> <dt>

[Anwenden mehrerer Transformationen auf ein Objekt](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

