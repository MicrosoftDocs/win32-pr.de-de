---
title: ID2D1Factory-Methode für die Methode "kreatetransformedgeometry" (D2d1. h)
description: Transformiert die angegebene Geometrie und speichert das Ergebnis als ID2D1TransformedGeometry-Objekt.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Methoden der Methode "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360335"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>ID2D1Factory:: kreatetransformedgeometry-Methoden

Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) -Objekt.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) -Objekt. <br/> |
| [**ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) -Objekt. <br/> |



## <a name="remarks"></a>Bemerkungen

Wie andere Ressourcen erbt eine transformierte Geometrie den Ressourcenbereich und die Threading Richtlinie der Factory, von der Sie erstellt wurde. Dieses Objekt ist unveränderlich.

Beim Übertragen einer transformierten Geometrie mit der [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode wird die Strichbreite von der auf die Geometrie angewendeten Transformation nicht beeinträchtigt. Die Strichbreite wird nur von der Welt Transformation beeinflusst.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))erstellt und dann gezeichnet, ohne es zu transformieren. Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Rechtecks](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



Im nächsten Beispiel wird das Renderziel verwendet, um die Geometrie um den Faktor 3 zu skalieren, und dann gezeichnet. Die folgende Abbildung zeigt das Ergebnis des Zeichnens des Rechtecks ohne die Transformation und mit der Transformation. Gibt an, dass der Strich nach der Transformation dicker ist, auch wenn die Strichstärke 1 ist.

![Darstellung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit einem dickeren Strich](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



Im nächsten Beispiel wird die Methode " **kreatetransformedgeometry** " verwendet, um die Geometrie mit dem Faktor 3 zu skalieren, und dann gezeichnet. Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe. Beachten Sie, dass, obwohl das Rechteck größer ist, der Strich nicht vergrößert wurde.

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
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
