---
title: ID2D1Factory CreateTransformedGeometry-Methoden (D2d1.h)
description: Transformiert die angegebene Geometrie und speichert das Ergebnis als ID2D1TransformedGeometry-Objekt.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- CreateTransformedGeometry-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 8216b5b63951e3f393dc1c8a204a4a4e38ee652d79eb795ba4f4e97041aff3f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832850"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>ID2D1Factory::CreateTransformedGeometry-Methoden

Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry-Objekt.**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTransformedGeometry(ID2D1Geometry \* ,D2D \_ MATRIX \_ 3X2 \_ F \* ,ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry-Objekt.**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) <br/> |
| [**CreateTransformedGeometry(ID2D1Geometry \* ,D2D \_ MATRIX \_ 3X2 \_ F&,ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry-Objekt.**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) <br/> |



## <a name="remarks"></a>Hinweise

Wie andere Ressourcen erbt eine transformierte Geometrie den Ressourcenraum und die Threadingrichtlinie der Factory, die sie erstellt hat. Dieses Objekt ist unveränderlich.

Beim Zusammenstellen einer transformierten Geometrie mit der [**DrawGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) wird die Strichbreite von der auf die Geometrie angewendeten Transformation nicht beeinflusst. Die Strichbreite wird nur von der Welttransformation beeinflusst.

## <a name="examples"></a>Beispiele

Das folgende Beispiel erstellt eine [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))und zeichnet sie dann, ohne sie zu transformieren. Sie erzeugt die ausgabe, die in der folgenden Abbildung dargestellt wird.

![Abbildung eines Rechtecks](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



Im nächsten Beispiel wird das Renderziel verwendet, um die Geometrie um den Faktor 3 zu skalieren und dann zu zeichnen. Die folgende Abbildung zeigt das Ergebnis des Zeichnens des Rechtecks ohne die Transformation und mit der Transformation. erkennt, dass der Strich nach der Transformation breiter ist, obwohl die Strichstärke 1 ist.

![Abbildung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit einem breiteren Strich](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



Im nächsten Beispiel wird die **CreateTransformedGeometry-Methode** verwendet, um die Geometrie um den Faktor 3 zu skalieren und dann zu zeichnen. Sie erzeugt die ausgabe, die in der folgenden Abbildung dargestellt wird. Beachten Sie, dass das Rechteck zwar größer ist, aber sein Strich nicht erhöht wurde.

![Abbildung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit dem gleichen Strich](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
