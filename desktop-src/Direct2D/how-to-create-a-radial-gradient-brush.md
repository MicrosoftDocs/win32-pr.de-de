---
title: Erstellen eines radialen Farbverlaufs Pinsels
description: Zeigt, wie ein radialer Farbverlaufs Pinsel mit Direct2D erstellt wird.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe3509a80f80132f4a5e5d65f62476be1cac61d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209268"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Erstellen eines radialen Farbverlaufs Pinsels

Um einen radialen Farbverlaufs Pinsel zu erstellen, verwenden Sie die [**ID2DRenderTarget:: samateradialgradientbrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) -Methode, und geben Sie die Eigenschaften des radialen Farbverlaufs Pinsels und die Auflistung der Mit einigen über Ladungen können Sie die Pinsel Eigenschaften angeben. Der folgende Code zeigt, wie Sie einen radialen Farbverlaufs Pinsel zum Auffüllen eines Kreises erstellen, und einen Pinsel mit einem Pinsel, um die Kontur des Kreises zu zeichnen.

Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Kreises, der mit einem radialen Farbverlaufs Pinsel gefüllt ist](images/brushes-ovw-radials.png)

1.  Deklarieren Sie eine Variable vom Typ [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Erstellen Sie ein Array [**von \_ D2D1 \_ Gradient**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) -Strukturen, die in die Auflistung der Farbverlaufs Stopps eingefügt werden sollen. Die **D2D1 \_ Gradient- \_ Ende** -Struktur enthält die Position und Farbe eines Farbverlaufs Stopps. Die Position gibt die relative Position des Farbverlaufs Stopps im Pinsel an. Der Wert liegt im Bereich \[ 0,0 f, 1.0 f \] , wie im folgenden Code dargestellt.

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  Verwenden Sie die [**ID2D1RenderTarget:: kreategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) -Methode, um die [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) -Sammlung aus einem zuvor deklarierten Array von [**D2D1 Gradient- \_ \_ Stopp**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) Strukturen zu erstellen. Verwenden Sie dann " [**" mit "**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) " "" "" ", um einen radialen Farbverlaufs Pinsel zu erstellen.

    > [!Note]  
    > Ab Windows 8 können Sie eine [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) -Auflistung anstelle der [**ID2D1RenderTarget:: foategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) -Methode mithilfe der [**ID2D1DeviceContext:: foategradientstopcollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) -Methode erstellen. Diese Schnittstelle fügt Farbverläufe mit hoher Farbe und die interpolung von Farbverläufen entweder in geraden oder in den Sonderfarben hinzu. Weitere Informationen finden Sie auf der Seite " **ID2DDeviceContext:: kreategradientstopcollection** ".

     

    ```C++
    // The center of the gradient is in the center of the box.
    // The gradient origin offset was set to zero(0, 0) or center in this case.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateRadialGradientBrush(
            D2D1::RadialGradientBrushProperties(
                D2D1::Point2F(75, 75),
                D2D1::Point2F(0, 0),
                75,
                75),
            pGradientStops,
            &m_pRadialGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
    m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 