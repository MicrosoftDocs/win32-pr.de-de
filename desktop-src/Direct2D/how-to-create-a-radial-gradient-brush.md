---
title: Erstellen eines Pinsels mit radialem Farbverlauf
description: Zeigt, wie Sie einen Radialverlaufspinsel mit Direct2D erstellen.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1932dc6506c625332d61f4e549ae2dd169060731bfbea344f64c3aa826540ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569265"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Erstellen eines Pinsels mit radialem Farbverlauf

Verwenden Sie zum Erstellen eines radialen Farbverlaufspinsels die [**ID2DRenderTarget::CreateRadialGradientBrush-Methode,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) und geben Sie die Eigenschaften des Radialverlaufspinsels und die Gradientenstoppsammlung an. Mit einigen Überladungen können Sie die Pinseleigenschaften angeben. Der folgende Code zeigt, wie Sie einen Radialverlaufspinsel erstellen, um einen Kreis zu füllen, und einen soliden schwarzen Pinsel, um die Umrisse des Kreises zu zeichnen.

Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Kreises, der mit einem radialen Farbverlaufspinsel gefüllt ist](images/brushes-ovw-radials.png)

1.  Deklarieren Sie eine Variable vom Typ [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Erstellen Sie ein Array von [**D2D1 \_ GRADIENT \_ STOP-Strukturen,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) die in der Gradientenstopp-Auflistung gespeichert werden. Die **D2D1 \_ GRADIENT \_ STOP-Struktur** enthält die Position und Farbe eines Farbverlaufsstopps. Die Position gibt die relative Position des Farbverlaufsstopps im Pinsel an. Der Wert liegt im Bereich \[ 0,0f, 1,0f, \] wie im folgenden Code gezeigt.

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

    

3.  Verwenden Sie die [**ID2D1RenderTarget::CreateGradientStopCollection-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) um die [**ID2D1GradientStopCollection-Auflistung**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus einem zuvor deklarierten Array von [**D2D1 \_ GRADIENT \_ STOP-Strukturen**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) zu erstellen. Verwenden Sie dann [**createRadialGradientBrush,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) um einen Radialverlaufspinsel zu erstellen.

    > [!Note]  
    > Ab Windows 8 können Sie die [**ID2D1DeviceContext::CreateGradientStopCollection-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) verwenden, um eine [**ID2D1GradientStopCollection1-Sammlung**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) anstelle der [**ID2D1RenderTarget::CreateGradientStopCollection-Methode zu**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) erstellen. Diese Schnittstelle fügt farblich hochwertige Farbverläufe und die Interpolation von Farbverläufen in geraden oder prmultipliierten Farben hinzu. Weitere Informationen finden Sie auf der Seite **ID2DDeviceContext::CreateGradientStopCollection.**

     

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

 

 