---
title: Transformieren einer Geometrie
description: Zeigt, wie eine Geometrie mithilfe von Direct2D transformiert wird.
ms.assetid: de434615-14b1-4b66-b09b-e90468e03d58
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ae15d0b1da304f9dfe24ff5de33a9f1582e2ca05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338286"
---
# <a name="how-to-transform-a-geometry"></a>Transformieren einer Geometrie

Zum Transformieren einer Geometrie können Sie entweder die Transformation auf das Renderziel anwenden, indem Sie [**setTransform**](id2d1rendertarget-settransform.md) aufrufen oder die Transformation auf die Geometrie anwenden, indem Sie [**createtransformedgeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))aufrufen. Obwohl beide Ansätze eine Geometrie transformieren, haben Sie einige grundlegende Unterschiede. " **Kreatetransformedgeometry** " wirkt sich auf die Füllung aus, wirkt sich jedoch nicht auf die Strichbreite aus. Außerdem wandelt " **foratetransformedgeometry** " die Geometrie allein um, ohne dass andere Formen auf dem Renderziel beeinträchtigt werden, während [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) die Transformation auf alle Formen auf dem Renderziel anwendet.

In diesem Thema wird beschrieben, wie Sie eine Geometrie durch Aufrufen von [**createtransformedgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))transformieren.

**So transformieren Sie eine Geometrie**

1.  Deklarieren Sie eine [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) -Variable.
2.  Rufen Sie [**die Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) "Methode" auf, um eine transformierte Geometrie zu erstellen.

Der folgende Code zeigt, wie Sie ein Stundenglas erstellen, das Stundenglas transformieren und die ursprüngliche und resultierende Stunden-Brille zeichnen.


```C++
// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}

if (SUCCEEDED(hr))
{
    // Create a transformed geometry which is tilted at an angle to the previous geometry
    hr = m_pD2DFactory->CreateTransformedGeometry(
        m_pPathGeometry,
        D2D1::Matrix3x2F::Rotation(
            45.f,
            D2D1::Point2F(100, 100)),
        &m_pTransformedGeometry
        );
}
```



 

 