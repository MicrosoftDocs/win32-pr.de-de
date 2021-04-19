---
title: ID2D1GeometrySink AddBezier-Methoden (D2d1. h)
description: Erstellt eine kubische Bezier-Kurve zwischen dem aktuellen Punkt und dem angegebenen Endpunkt und fügt Sie der Geometrie-Senke hinzu.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- AddBezier-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366777"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a>ID2D1GeometrySink:: AddBezier-Methoden

Erstellt eine kubische Bezier-Kurve zwischen dem aktuellen Punkt und dem angegebenen Endpunkt und fügt Sie der Geometrie-Senke hinzu.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                            | BESCHREIBUNG                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AddBezier (D2D1 \_ Bezier- \_ Segment&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))  | Erstellt eine kubische Bézierkurve zwischen dem aktuellen Punkt und dem angegebenen Endpunkt.<br/> |
| [**AddBezier (D2D1 \_ Bezier- \_ Segment \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment)) | Erstellt eine kubische Bezier-Kurve zwischen dem aktuellen Punkt und dem angegebenen Endpunkt.<br/>  |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)erstellt, eine Senke abgerufen und verwendet, um eine Sanduhr Form zu definieren. Das komplette Beispiel finden Sie unter [Zeichnen und Ausfüllen einer komplexen Form](how-to-draw-and-fill-a-complex-shape.md).


```C++
ID2D1GeometrySink *pSink = NULL;



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
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

�

�
