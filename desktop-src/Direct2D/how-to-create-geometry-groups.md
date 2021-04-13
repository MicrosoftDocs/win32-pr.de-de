---
title: Erstellen von Geometrie Gruppen
description: In diesem Thema wird beschrieben, wie Geometrie Gruppen erstellt werden.
ms.assetid: be364440-75ab-4d8f-a359-39da275272fd
keywords:
- Direct2D, Beispiel für Füll Modus
- Geometrie Gruppen
- Direct2D, Geometrie Gruppen
- Pfadgeometrien
- Direct2D, Pfadgeometrien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb4a0e63a3274473153e1871a8a085bb04d5146
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390420"
---
# <a name="how-to-create-geometry-groups"></a>Erstellen von Geometrie Gruppen

In diesem Thema wird beschrieben, wie Geometrie Gruppen erstellt werden.

Um eine Geometrie Gruppe zu erstellen, rufen Sie die [**ID2D1Factory:: deategeometrygroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) -Methode auf, und geben Sie ein Array von Geometrien und einen Füll Modus an.

Wenn Sie Geometrien in einer Geometrie Gruppe kombinieren, stellen Sie sicher, dass die Geometrien ähnlich ausgerichtet sind. Wenn Sie sich nicht sicher sind, wie die Geometrien ausgerichtet sind, müssen Sie [**ID2D1Geometry:: Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink)) für jede einzelne einzeln aufrufen und dann die resultierenden Geometrien in die Geometrie Gruppe einfügen.

Das folgende Codebeispiel zeigt die Erstellung von vier konzentrischen Kreisen: der erste Kreis weist einen Radius von 25, das zweite 50, das dritte 75 und das vierte 100 auf. Der Code zeigt auch die Instanziierung eines Arrays von Geometrien sowie die zwei Aufrufe von " [**kreategeometrygroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup)".


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr;

    const D2D1_ELLIPSE ellipse1 = D2D1::Ellipse(
        D2D1::Point2F(105.0f, 105.0f),
        25.0f,
        25.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        ellipse1,
        &m_pEllipseGeometry1
        );

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse2 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse2,
            &m_pEllipseGeometry2
            );
    }

    if (SUCCEEDED(hr))
    {

        const D2D1_ELLIPSE ellipse3 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            75.0f,
            75.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse3,
            &m_pEllipseGeometry3
            );
    }

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse4 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            100.0f,
            100.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse4,
            &m_pEllipseGeometry4
            );
    }

    if (SUCCEEDED(hr))
    {
        ID2D1Geometry *ppGeometries[] =
        {
            m_pEllipseGeometry1,
            m_pEllipseGeometry2,
            m_pEllipseGeometry3,
            m_pEllipseGeometry4
        };

        hr = m_pD2DFactory->CreateGeometryGroup(
            D2D1_FILL_MODE_ALTERNATE,
            ppGeometries,
            ARRAYSIZE(ppGeometries),
            &m_pGeoGroup_AlternateFill
            );

        if (SUCCEEDED(hr))
        {
            hr = m_pD2DFactory->CreateGeometryGroup(
                D2D1_FILL_MODE_WINDING,
                ppGeometries,
                ARRAYSIZE(ppGeometries),
                &m_pGeoGroup_WindingFill
                );
        }

    }
    return hr;
}
```



## <a name="drawing-and-filling-of-geometry-groups"></a>Zeichnen und Auffüllen von Geometrie Gruppen

Verwenden Sie die [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode und die [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode, um eine Geometrie Gruppe zu zeichnen und auszufüllen. Im folgenden Codebeispiel wird gezeigt, wie eine Geometrie Gruppe gezeichnet und ausgefüllt wird.


```C++
HRESULT DemoApp::OnRender()
{
    HRESULT hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_fillModeAlternateText[] = L"D2D1_FILL_MODE_ALTERNATE";
        static const WCHAR sc_fillModeWindingText[] = L"D2D1_FILL_MODE_WINDING";

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, rtSize.width, rtSize.height),
            m_pGridPatternBitmapBrush
            );

        // Centers the text in a layout rectangle.
        hr = m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

        if (SUCCEEDED(hr))
        {
            // Fill the geometry group with D2D1_FILL_MODE_ALTERNATE and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_AlternateFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_AlternateFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeAlternateText,
                ARRAYSIZE(sc_fillModeAlternateText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

            // Fill the geometry group with D2D1_FILL_MODE_WINDING and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_WindingFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_WindingFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeWindingText,
                ARRAYSIZE(sc_fillModeWindingText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            hr = m_pRenderTarget->EndDraw();

            if (hr == D2DERR_RECREATE_TARGET)
            {
                hr = S_OK;
                DiscardDeviceResources();
            }
        }
    }
    return hr;
}
```



Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung von zwei Sätzen von vier konzentrischen Kreisen, von denen eine mit dem zweiten und vierten Ringen gefüllt ist und eine mit allen Ringen gefüllt ist](images/create-geometry-group.png)

 

 