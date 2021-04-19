---
title: Zeichnen und Ausfüllen einer komplexen Form
description: Direct2D stellt die ID2D1PathGeometry-Schnittstelle zum Beschreiben komplexer Formen bereit, die Kurven, Arcs und Linien enthalten können. In diesem Thema wird beschrieben, wie eine Pfad Geometrie definiert und dargestellt wird.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a163e85d76a65f6b807ad1e4a9c9f740a32bf1
ms.sourcegitcommit: 4859402a45b9928c3e1354ded06b1d6a682a0be9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "106372800"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a>Zeichnen und Ausfüllen einer komplexen Form

Direct2D stellt die [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Schnittstelle zum Beschreiben komplexer Formen bereit, die Kurven, Arcs und Linien enthalten können. In diesem Thema wird beschrieben, wie eine Pfad Geometrie definiert und dargestellt wird.

Zum Definieren einer Pfad Geometrie verwenden Sie zunächst die [**ID2D1Factory:: kreatepathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) -Methode, um die Pfad Geometrie zu erstellen, und verwenden Sie dann die [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode der Pfad Geometrie zum Abrufen eines [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Anschließend können Sie Zeilen, Kurven und Bögen hinzufügen, indem Sie die verschiedenen Add-Methoden der Senke aufrufen.

Im folgenden Beispiel wird ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)erstellt, eine Senke abgerufen und verwendet, um eine Sanduhr Form zu definieren.


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

Beachten Sie, dass ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) eine geräteunabhängige Ressource ist und daher einmalig erstellt und für die Lebensdauer der Anwendung beibehalten werden kann. (Weitere Informationen zu verschiedenen Arten von Ressourcen finden Sie in der [Übersicht über Ressourcen](resources-and-resource-domains.md).)

Im nächsten Beispiel werden zwei Pinsel erstellt, die zum Zeichnen der Kontur und Füllung der Pfad Geometrie verwendet werden.


```C++
if (SUCCEEDED(hr))
{
    // Create a black brush.
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &m_pBlackBrush
        );
}

if (SUCCEEDED(hr))
{
    // Create a linear gradient.
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 0.25f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = m_pRenderTarget->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(100, 0),
                D2D1::Point2F(100, 200)),
            D2D1::BrushProperties(),
            pGradientStops,
            &m_pLGBrush
            );
    }

    SafeRelease(&pGradientStops);
}
```



Im abschließenden Beispiel werden die Methoden [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) und [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) verwendet, um die Kontur und das Innere der Geometrie zu zeichnen. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung einer Sanduhr förmigen Geometrie](images/transformgeometryexample-1.png)


```C++
void DemoApp::RenderGeometryExample()
{
    // Translate subsequent drawings by 20 device-independent pixels.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Translation(20.f, 20.f)
        );

    // Draw the hour glass geometry at the upper left corner of the client area.
    m_pRenderTarget->DrawGeometry(m_pPathGeometry, m_pBlackBrush, 10.f);
    m_pRenderTarget->FillGeometry(m_pPathGeometry, m_pLGBrush);
}
```

Code wurde in diesem Beispiel ausgelassen. Weitere Informationen zu Geometrien finden Sie in der [Übersicht über Geometrien](direct2d-geometries-overview.md).
